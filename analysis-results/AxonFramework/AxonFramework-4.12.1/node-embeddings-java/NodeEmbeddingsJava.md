# Node Embeddings

This notebook demonstrates different methods for node embeddings and how to further reduce their dimensionality to be able to visualize them in a 2D plot. 

Node embeddings are essentially an array of floating point numbers (length = embedding dimension) that can be used as "features" in machine learning. These numbers approximate the relationship and similarity information of each node and can also be seen as a way to encode the topology of the graph.

## Considerations

Due to dimensionality reduction some information gets lost, especially when visualizing node embeddings in two dimensions. Nevertheless, it helps to get an intuition on what node embeddings are and how much of the similarity and neighborhood information is retained. The latter can be observed by how well nodes of the same color and therefore same community are placed together and how much bigger nodes with a high centrality score influence them. 

If the visualization doesn't show a somehow clear separation between the communities (colors) here are some ideas for tuning: 
- Clean the data, e.g. filter out very few nodes with extremely high degree that aren't actually that important
- Try directed vs. undirected projections
- Tune the embedding algorithm, e.g. use a higher dimensionality
- Tune t-SNE that is used to reduce the node embeddings dimension to two dimensions for visualization. 

It could also be the case that the node embeddings are good enough and well suited the way they are despite their visualization for the down stream task like node classification or link prediction. In that case it makes sense to see how the whole pipeline performs before tuning the node embeddings in detail. 

## Note about data dependencies

PageRank centrality and Leiden community are also fetched from the Graph and need to be calculated first.
This makes it easier to see if the embeddings approximate the structural information of the graph in the plot.
If these properties are missing you will only see black dots all of the same size.

<br>  

### References
- [jqassistant](https://jqassistant.org)
- [Neo4j Python Driver](https://neo4j.com/docs/api/python-driver/current)
- [Tutorial: Applied Graph Embeddings](https://neo4j.com/developer/graph-data-science/applied-graph-embeddings)
- [Visualizing the embeddings in 2D](https://github.com/openai/openai-cookbook/blob/main/examples/Visualizing_embeddings_in_2D.ipynb)
- [scikit-learn TSNE](https://scikit-learn.org/stable/modules/generated/sklearn.manifold.TSNE.html#sklearn.manifold.TSNE)
- [AttributeError: 'list' object has no attribute 'shape'](https://bobbyhadz.com/blog/python-attributeerror-list-object-has-no-attribute-shape)
- [Fast Random Projection (neo4j)](https://neo4j.com/docs/graph-data-science/current/machine-learning/node-embeddings/fastrp)
- [HashGNN (neo4j)](https://neo4j.com/docs/graph-data-science/2.6/machine-learning/node-embeddings/hashgnn)
- [node2vec (neo4j)](https://neo4j.com/docs/graph-data-science/current/machine-learning/node-embeddings/node2vec) computes a vector representation of a node based on second order random walks in the graph. 
- [Complete guide to understanding Node2Vec algorithm](https://towardsdatascience.com/complete-guide-to-understanding-node2vec-algorithm-4e9a35e5d147)





    The openTSNE version is: 1.0.2
    The pandas version is: 2.2.3


### Dimensionality reduction with t-distributed stochastic neighbor embedding (t-SNE)

The following function takes the original node embeddings with a higher dimensionality, e.g. 64 floating point numbers, and reduces them into a two dimensional array for visualization. 

> It converts similarities between data points to joint probabilities and tries to minimize the Kullback-Leibler divergence between the joint probabilities of the low-dimensional embedding and the high-dimensional data.

(see https://opentsne.readthedocs.io)





## 1. Java Packages

### 1.1 Generate Node Embeddings using Fast Random Projection (Fast RP) for Java Packages

[Fast Random Projection](https://neo4j.com/docs/graph-data-science/current/machine-learning/node-embeddings/fastrp) is used to reduce the dimensionality of the node feature space while preserving most of the distance information. Nodes with similar neighborhood result in node embedding with similar vectors.

**👉Hint:** To skip existing node embeddings and always calculate them based on the parameters below edit `Node_Embeddings_0a_Query_Calculated` so that it won't return any results.

    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownRelationshipTypeWarning} {category: UNRECOGNIZED} {title: The provided relationship type is not in the database.} {description: One of the relationship types in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing relationship type is: HAS_ROOT)} {position: line: 9, column: 44, offset: 696} for query: '// Query already calculated and written node embeddings on nodes with label in parameter $dependencies_projection_node including a communityId and centrality. Variables: dependencies_projection_node, dependencies_projection_write_property. Requires "Add_file_name and_extension.cypher".\n \n  MATCH (codeUnit)\n  WHERE $dependencies_projection_node IN LABELS(codeUnit)\n    AND codeUnit[$dependencies_projection_write_property] IS NOT NULL\n    // AND codeUnit.notExistingToForceRecalculation IS NOT NULL // uncomment this line to force recalculation\n OPTIONAL MATCH (artifact:Java:Artifact)-[:CONTAINS]->(codeUnit)\n    WITH *, artifact.name AS artifactName\n OPTIONAL MATCH (projectRoot:Directory)<-[:HAS_ROOT]-(proj:TS:Project)-[:CONTAINS]->(codeUnit)\n    WITH *, last(split(projectRoot.absoluteFileName, \'/\')) AS projectName   \n  RETURN DISTINCT \n         coalesce(codeUnit.fqn, codeUnit.globalFqn, codeUnit.fileName, codeUnit.signature, codeUnit.name) AS codeUnitName\n        ,codeUnit.name                AS shortCodeUnitName\n        ,coalesce(artifactName, projectName)                                                              AS projectName\n        ,coalesce(codeUnit.communityLeidenId, 0)           AS communityId\n        ,coalesce(codeUnit.centralityPageRank, 0.01)       AS centrality\n        ,codeUnit[$dependencies_projection_write_property] AS embedding\n   ORDER BY communityId'


    The results have been provided by the query filename: ../cypher/Node_Embeddings/Node_Embeddings_0a_Query_Calculated.cypher



<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>codeUnitName</th>
      <th>shortCodeUnitName</th>
      <th>projectName</th>
      <th>communityId</th>
      <th>centrality</th>
      <th>embedding</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.axonframework.axonserver.connector</td>
      <td>connector</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>1.113846</td>
      <td>[-0.44958528876304626, -0.07346808165311813, 0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.axonserver.connector.processor</td>
      <td>processor</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.153313</td>
      <td>[-0.30079174041748047, 0.06917058676481247, 0....</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>util</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.295966</td>
      <td>[-0.4947444796562195, -0.1351310759782791, 0.5...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.axonserver.connector.heartbeat</td>
      <td>heartbeat</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.175500</td>
      <td>[-0.46239173412323, -0.18305456638336182, 0.51...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.heartbe...</td>
      <td>source</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[-0.42939406633377075, -0.23621611297130585, 0...</td>
    </tr>
  </tbody>
</table>
</div>


### 1.2 Dimensionality reduction with t-distributed stochastic neighbor embedding (t-SNE)

This step takes the original node embeddings with a higher dimensionality, e.g. 64 floating point numbers, and reduces them into a two dimensional array for visualization. For more details look up the function declaration for "prepare_node_embeddings_for_2d_visualization".

    --------------------------------------------------------------------------------
    TSNE(early_exaggeration=12, random_state=47, verbose=1)
    --------------------------------------------------------------------------------


    ===> Finding 90 nearest neighbors using exact search using euclidean distance...
       --> Time elapsed: 0.04 seconds
    ===> Calculating affinity matrix...
       --> Time elapsed: 0.00 seconds
    ===> Calculating PCA-based initialization...
       --> Time elapsed: 0.00 seconds
    ===> Running optimization with exaggeration=12.00, lr=10.00 for 250 iterations...
    Iteration   50, KL divergence -0.1125, 50 iterations in 0.0431 sec
    Iteration  100, KL divergence 1.2564, 50 iterations in 0.0116 sec
    Iteration  150, KL divergence 1.2564, 50 iterations in 0.0107 sec
    Iteration  200, KL divergence 1.2564, 50 iterations in 0.0107 sec
    Iteration  250, KL divergence 1.2564, 50 iterations in 0.0108 sec
       --> Time elapsed: 0.09 seconds
    ===> Running optimization with exaggeration=1.00, lr=120.00 for 500 iterations...
    Iteration   50, KL divergence 0.2024, 50 iterations in 0.0407 sec


    Iteration  100, KL divergence 0.1772, 50 iterations in 0.0549 sec
    Iteration  150, KL divergence 0.1647, 50 iterations in 0.0538 sec
    Iteration  200, KL divergence 0.1651, 50 iterations in 0.0531 sec
    Iteration  250, KL divergence 0.1651, 50 iterations in 0.0529 sec


    Iteration  300, KL divergence 0.1653, 50 iterations in 0.0533 sec
    Iteration  350, KL divergence 0.1651, 50 iterations in 0.0531 sec
    Iteration  400, KL divergence 0.1651, 50 iterations in 0.0528 sec
    Iteration  450, KL divergence 0.1647, 50 iterations in 0.0527 sec


    Iteration  500, KL divergence 0.1652, 50 iterations in 0.0525 sec
       --> Time elapsed: 0.52 seconds



    (120, 2)



<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>codeUnit</th>
      <th>artifact</th>
      <th>communityId</th>
      <th>centrality</th>
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.axonframework.axonserver.connector</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>1.113846</td>
      <td>-4.269225</td>
      <td>2.631993</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.axonserver.connector.processor</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.153313</td>
      <td>-4.406635</td>
      <td>1.979918</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.295966</td>
      <td>-3.867899</td>
      <td>3.480273</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.axonserver.connector.heartbeat</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.175500</td>
      <td>-4.364450</td>
      <td>3.781064</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.heartbe...</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-4.813282</td>
      <td>3.569755</td>
    </tr>
  </tbody>
</table>
</div>


### 1.3 Visualization of the node embeddings reduced to two dimensions


    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_21_0.png)
    


### 1.4 Node Embeddings for Java Packages using HashGNN

[HashGNN](https://neo4j.com/docs/graph-data-science/2.6/machine-learning/node-embeddings/hashgnn) resembles Graph Neural Networks (GNN) but does not include a model or require training. It combines ideas of GNNs and fast randomized algorithms. For more details see [HashGNN](https://neo4j.com/docs/graph-data-science/2.6/machine-learning/node-embeddings/hashgnn). Here, the latter 3 steps are combined into one for HashGNN.

    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownRelationshipTypeWarning} {category: UNRECOGNIZED} {title: The provided relationship type is not in the database.} {description: One of the relationship types in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing relationship type is: HAS_ROOT)} {position: line: 9, column: 44, offset: 696} for query: '// Query already calculated and written node embeddings on nodes with label in parameter $dependencies_projection_node including a communityId and centrality. Variables: dependencies_projection_node, dependencies_projection_write_property. Requires "Add_file_name and_extension.cypher".\n \n  MATCH (codeUnit)\n  WHERE $dependencies_projection_node IN LABELS(codeUnit)\n    AND codeUnit[$dependencies_projection_write_property] IS NOT NULL\n    // AND codeUnit.notExistingToForceRecalculation IS NOT NULL // uncomment this line to force recalculation\n OPTIONAL MATCH (artifact:Java:Artifact)-[:CONTAINS]->(codeUnit)\n    WITH *, artifact.name AS artifactName\n OPTIONAL MATCH (projectRoot:Directory)<-[:HAS_ROOT]-(proj:TS:Project)-[:CONTAINS]->(codeUnit)\n    WITH *, last(split(projectRoot.absoluteFileName, \'/\')) AS projectName   \n  RETURN DISTINCT \n         coalesce(codeUnit.fqn, codeUnit.globalFqn, codeUnit.fileName, codeUnit.signature, codeUnit.name) AS codeUnitName\n        ,codeUnit.name                AS shortCodeUnitName\n        ,coalesce(artifactName, projectName)                                                              AS projectName\n        ,coalesce(codeUnit.communityLeidenId, 0)           AS communityId\n        ,coalesce(codeUnit.centralityPageRank, 0.01)       AS centrality\n        ,codeUnit[$dependencies_projection_write_property] AS embedding\n   ORDER BY communityId'


    The results have been provided by the query filename: ../cypher/Node_Embeddings/Node_Embeddings_0a_Query_Calculated.cypher



<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>codeUnitName</th>
      <th>shortCodeUnitName</th>
      <th>projectName</th>
      <th>communityId</th>
      <th>centrality</th>
      <th>embedding</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.axonframework.axonserver.connector</td>
      <td>connector</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>1.113846</td>
      <td>[0.8660253882408142, -0.4330126941204071, -1.5...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.axonserver.connector.processor</td>
      <td>processor</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.153313</td>
      <td>[1.0825317353010178, -0.4330126941204071, -2.1...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>util</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.295966</td>
      <td>[0.0, 1.0825317353010178, -1.5155444294214249,...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.axonserver.connector.heartbeat</td>
      <td>heartbeat</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.175500</td>
      <td>[0.8660253882408142, 0.4330126941204071, -1.51...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.heartbe...</td>
      <td>source</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.0, -1.0825317353010178, -0.2165063470602035...</td>
    </tr>
  </tbody>
</table>
</div>


    --------------------------------------------------------------------------------
    TSNE(early_exaggeration=12, random_state=47, verbose=1)
    --------------------------------------------------------------------------------
    ===> Finding 90 nearest neighbors using exact search using euclidean distance...
       --> Time elapsed: 0.00 seconds
    ===> Calculating affinity matrix...
       --> Time elapsed: 0.01 seconds
    ===> Calculating PCA-based initialization...
       --> Time elapsed: 0.04 seconds
    ===> Running optimization with exaggeration=12.00, lr=10.00 for 250 iterations...
    Iteration   50, KL divergence -0.6396, 50 iterations in 0.0759 sec
    Iteration  100, KL divergence 1.2795, 50 iterations in 0.0182 sec
    Iteration  150, KL divergence 1.2795, 50 iterations in 0.0154 sec
    Iteration  200, KL divergence 1.2795, 50 iterations in 0.0105 sec
    Iteration  250, KL divergence 1.2795, 50 iterations in 0.0104 sec
       --> Time elapsed: 0.13 seconds
    ===> Running optimization with exaggeration=1.00, lr=120.00 for 500 iterations...


    Iteration   50, KL divergence 0.6521, 50 iterations in 0.0410 sec
    Iteration  100, KL divergence 0.6413, 50 iterations in 0.0560 sec
    Iteration  150, KL divergence 0.6381, 50 iterations in 0.0539 sec
    Iteration  200, KL divergence 0.6346, 50 iterations in 0.0552 sec


    Iteration  250, KL divergence 0.6346, 50 iterations in 0.0555 sec
    Iteration  300, KL divergence 0.6344, 50 iterations in 0.0553 sec
    Iteration  350, KL divergence 0.6342, 50 iterations in 0.0554 sec
    Iteration  400, KL divergence 0.6348, 50 iterations in 0.0556 sec


    Iteration  450, KL divergence 0.6347, 50 iterations in 0.0566 sec
    Iteration  500, KL divergence 0.6344, 50 iterations in 0.0564 sec
       --> Time elapsed: 0.54 seconds



    (120, 2)



<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>codeUnit</th>
      <th>artifact</th>
      <th>communityId</th>
      <th>centrality</th>
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.axonframework.axonserver.connector</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>1.113846</td>
      <td>3.943777</td>
      <td>-6.458820</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.axonserver.connector.processor</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.153313</td>
      <td>1.547992</td>
      <td>2.164693</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.295966</td>
      <td>0.952720</td>
      <td>3.665702</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.axonserver.connector.heartbeat</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.175500</td>
      <td>2.113535</td>
      <td>-5.070277</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.heartbe...</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>3.293040</td>
      <td>-5.180042</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_23_9.png)
    


### 2.5 Node Embeddings for Java Packages using node2vec

    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownRelationshipTypeWarning} {category: UNRECOGNIZED} {title: The provided relationship type is not in the database.} {description: One of the relationship types in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing relationship type is: HAS_ROOT)} {position: line: 9, column: 44, offset: 696} for query: '// Query already calculated and written node embeddings on nodes with label in parameter $dependencies_projection_node including a communityId and centrality. Variables: dependencies_projection_node, dependencies_projection_write_property. Requires "Add_file_name and_extension.cypher".\n \n  MATCH (codeUnit)\n  WHERE $dependencies_projection_node IN LABELS(codeUnit)\n    AND codeUnit[$dependencies_projection_write_property] IS NOT NULL\n    // AND codeUnit.notExistingToForceRecalculation IS NOT NULL // uncomment this line to force recalculation\n OPTIONAL MATCH (artifact:Java:Artifact)-[:CONTAINS]->(codeUnit)\n    WITH *, artifact.name AS artifactName\n OPTIONAL MATCH (projectRoot:Directory)<-[:HAS_ROOT]-(proj:TS:Project)-[:CONTAINS]->(codeUnit)\n    WITH *, last(split(projectRoot.absoluteFileName, \'/\')) AS projectName   \n  RETURN DISTINCT \n         coalesce(codeUnit.fqn, codeUnit.globalFqn, codeUnit.fileName, codeUnit.signature, codeUnit.name) AS codeUnitName\n        ,codeUnit.name                AS shortCodeUnitName\n        ,coalesce(artifactName, projectName)                                                              AS projectName\n        ,coalesce(codeUnit.communityLeidenId, 0)           AS communityId\n        ,coalesce(codeUnit.centralityPageRank, 0.01)       AS centrality\n        ,codeUnit[$dependencies_projection_write_property] AS embedding\n   ORDER BY communityId'


    The results have been provided by the query filename: ../cypher/Node_Embeddings/Node_Embeddings_0a_Query_Calculated.cypher



<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>codeUnitName</th>
      <th>shortCodeUnitName</th>
      <th>projectName</th>
      <th>communityId</th>
      <th>centrality</th>
      <th>embedding</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.axonframework.axonserver.connector</td>
      <td>connector</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>1.113846</td>
      <td>[-0.20058690011501312, -0.024909907951951027, ...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.axonserver.connector.processor</td>
      <td>processor</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.153313</td>
      <td>[-0.262472003698349, 0.10399071127176285, 0.21...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>util</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.295966</td>
      <td>[0.01473277062177658, 0.00858526024967432, 0.4...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.axonserver.connector.heartbeat</td>
      <td>heartbeat</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.175500</td>
      <td>[0.034913863986730576, 0.08920011669397354, 0....</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.heartbe...</td>
      <td>source</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[-0.11359481513500214, 0.0066638826392591, 0.2...</td>
    </tr>
  </tbody>
</table>
</div>


    --------------------------------------------------------------------------------
    TSNE(early_exaggeration=12, random_state=47, verbose=1)
    --------------------------------------------------------------------------------
    ===> Finding 90 nearest neighbors using exact search using euclidean distance...
       --> Time elapsed: 0.00 seconds
    ===> Calculating affinity matrix...
       --> Time elapsed: 0.00 seconds
    ===> Calculating PCA-based initialization...
       --> Time elapsed: 0.00 seconds
    ===> Running optimization with exaggeration=12.00, lr=10.00 for 250 iterations...
    Iteration   50, KL divergence -0.2758, 50 iterations in 0.0509 sec
    Iteration  100, KL divergence 1.2165, 50 iterations in 0.0126 sec
    Iteration  150, KL divergence 1.2165, 50 iterations in 0.0110 sec
    Iteration  200, KL divergence 1.2165, 50 iterations in 0.0108 sec
    Iteration  250, KL divergence 1.2165, 50 iterations in 0.0109 sec
       --> Time elapsed: 0.10 seconds
    ===> Running optimization with exaggeration=1.00, lr=120.00 for 500 iterations...
    Iteration   50, KL divergence 0.3369, 50 iterations in 0.0405 sec
    Iteration  100, KL divergence 0.3103, 50 iterations in 0.0530 sec


    Iteration  150, KL divergence 0.3071, 50 iterations in 0.0540 sec
    Iteration  200, KL divergence 0.3072, 50 iterations in 0.0534 sec
    Iteration  250, KL divergence 0.3069, 50 iterations in 0.0523 sec
    Iteration  300, KL divergence 0.3068, 50 iterations in 0.0526 sec


    Iteration  350, KL divergence 0.3069, 50 iterations in 0.0539 sec
    Iteration  400, KL divergence 0.3069, 50 iterations in 0.0536 sec
    Iteration  450, KL divergence 0.3067, 50 iterations in 0.0529 sec
    Iteration  500, KL divergence 0.3067, 50 iterations in 0.0530 sec
       --> Time elapsed: 0.52 seconds



    (120, 2)



<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>codeUnit</th>
      <th>artifact</th>
      <th>communityId</th>
      <th>centrality</th>
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.axonframework.axonserver.connector</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>1.113846</td>
      <td>-4.639834</td>
      <td>-1.733485</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.axonserver.connector.processor</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.153313</td>
      <td>-3.860759</td>
      <td>-0.927612</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.295966</td>
      <td>-3.556561</td>
      <td>-3.127971</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.axonserver.connector.heartbeat</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.175500</td>
      <td>-4.365781</td>
      <td>-2.355176</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.heartbe...</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-2.889790</td>
      <td>-1.092969</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_25_8.png)
    

