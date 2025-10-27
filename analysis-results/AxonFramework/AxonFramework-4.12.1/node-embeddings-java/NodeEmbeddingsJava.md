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
       --> Time elapsed: 0.03 seconds
    ===> Calculating affinity matrix...
       --> Time elapsed: 0.00 seconds
    ===> Calculating PCA-based initialization...
       --> Time elapsed: 0.00 seconds
    ===> Running optimization with exaggeration=12.00, lr=10.00 for 250 iterations...
    Iteration   50, KL divergence -0.8950, 50 iterations in 0.0427 sec
    Iteration  100, KL divergence 1.2564, 50 iterations in 0.0114 sec
    Iteration  150, KL divergence 1.2564, 50 iterations in 0.0107 sec
    Iteration  200, KL divergence 1.2564, 50 iterations in 0.0107 sec
    Iteration  250, KL divergence 1.2564, 50 iterations in 0.0108 sec
       --> Time elapsed: 0.09 seconds
    ===> Running optimization with exaggeration=1.00, lr=120.00 for 500 iterations...
    Iteration   50, KL divergence 0.1718, 50 iterations in 0.0382 sec


    Iteration  100, KL divergence 0.1566, 50 iterations in 0.0492 sec
    Iteration  150, KL divergence 0.1523, 50 iterations in 0.0493 sec
    Iteration  200, KL divergence 0.1521, 50 iterations in 0.0491 sec
    Iteration  250, KL divergence 0.1514, 50 iterations in 0.0487 sec
    Iteration  300, KL divergence 0.1514, 50 iterations in 0.0484 sec


    Iteration  350, KL divergence 0.1515, 50 iterations in 0.0496 sec
    Iteration  400, KL divergence 0.1514, 50 iterations in 0.0501 sec
    Iteration  450, KL divergence 0.1514, 50 iterations in 0.0487 sec
    Iteration  500, KL divergence 0.1513, 50 iterations in 0.0489 sec
       --> Time elapsed: 0.48 seconds



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
      <td>5.115739</td>
      <td>0.692804</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.axonserver.connector.processor</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.153313</td>
      <td>3.775631</td>
      <td>2.255179</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.295966</td>
      <td>5.350155</td>
      <td>1.284793</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.axonserver.connector.heartbeat</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.175500</td>
      <td>5.472376</td>
      <td>2.094333</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.heartbe...</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>5.889619</td>
      <td>1.969229</td>
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
       --> Time elapsed: 0.00 seconds
    ===> Calculating PCA-based initialization...
       --> Time elapsed: 0.00 seconds
    ===> Running optimization with exaggeration=12.00, lr=10.00 for 250 iterations...
    Iteration   50, KL divergence 0.0698, 50 iterations in 0.0733 sec
    Iteration  100, KL divergence 1.2795, 50 iterations in 0.0184 sec
    Iteration  150, KL divergence 1.2795, 50 iterations in 0.0158 sec
    Iteration  200, KL divergence 1.2795, 50 iterations in 0.0110 sec
    Iteration  250, KL divergence 1.2795, 50 iterations in 0.0105 sec
       --> Time elapsed: 0.13 seconds
    ===> Running optimization with exaggeration=1.00, lr=120.00 for 500 iterations...
    Iteration   50, KL divergence 0.6614, 50 iterations in 0.0420 sec


    Iteration  100, KL divergence 0.6427, 50 iterations in 0.0554 sec
    Iteration  150, KL divergence 0.6404, 50 iterations in 0.0532 sec
    Iteration  200, KL divergence 0.6354, 50 iterations in 0.0513 sec
    Iteration  250, KL divergence 0.6356, 50 iterations in 0.0507 sec


    Iteration  300, KL divergence 0.6319, 50 iterations in 0.0512 sec
    Iteration  350, KL divergence 0.6227, 50 iterations in 0.0497 sec
    Iteration  400, KL divergence 0.6218, 50 iterations in 0.0492 sec
    Iteration  450, KL divergence 0.6215, 50 iterations in 0.0499 sec
    Iteration  500, KL divergence 0.6211, 50 iterations in 0.0496 sec
       --> Time elapsed: 0.50 seconds



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
      <td>5.705563</td>
      <td>-6.138522</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.axonserver.connector.processor</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.153313</td>
      <td>1.112172</td>
      <td>0.022125</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.295966</td>
      <td>-3.603105</td>
      <td>-5.253422</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.axonserver.connector.heartbeat</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.175500</td>
      <td>3.353314</td>
      <td>-5.273928</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.heartbe...</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>4.632759</td>
      <td>-5.047015</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_23_8.png)
    


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
      <td>[0.08994719386100769, -0.03396010398864746, 0....</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.axonserver.connector.processor</td>
      <td>processor</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.153313</td>
      <td>[-0.27921679615974426, -0.04437103867530823, 0...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>util</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.295966</td>
      <td>[0.012659032829105854, 0.10450753569602966, 0....</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.axonserver.connector.heartbeat</td>
      <td>heartbeat</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.175500</td>
      <td>[-0.08161035180091858, 0.07520858943462372, 0....</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.heartbe...</td>
      <td>source</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.026473751291632652, -0.12043460458517075, 0...</td>
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
    Iteration   50, KL divergence -0.3682, 50 iterations in 0.0516 sec
    Iteration  100, KL divergence 1.2061, 50 iterations in 0.0127 sec
    Iteration  150, KL divergence 1.2061, 50 iterations in 0.0108 sec
    Iteration  200, KL divergence 1.2061, 50 iterations in 0.0108 sec
    Iteration  250, KL divergence 1.2061, 50 iterations in 0.0108 sec
       --> Time elapsed: 0.10 seconds
    ===> Running optimization with exaggeration=1.00, lr=120.00 for 500 iterations...
    Iteration   50, KL divergence 0.2975, 50 iterations in 0.0399 sec
    Iteration  100, KL divergence 0.2737, 50 iterations in 0.0490 sec


    Iteration  150, KL divergence 0.2670, 50 iterations in 0.0522 sec
    Iteration  200, KL divergence 0.2671, 50 iterations in 0.0516 sec
    Iteration  250, KL divergence 0.2672, 50 iterations in 0.0509 sec
    Iteration  300, KL divergence 0.2673, 50 iterations in 0.0506 sec


    Iteration  350, KL divergence 0.2673, 50 iterations in 0.0517 sec
    Iteration  400, KL divergence 0.2673, 50 iterations in 0.0516 sec
    Iteration  450, KL divergence 0.2673, 50 iterations in 0.0508 sec
    Iteration  500, KL divergence 0.2673, 50 iterations in 0.0508 sec
       --> Time elapsed: 0.50 seconds



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
      <td>-2.137376</td>
      <td>4.336285</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.axonserver.connector.processor</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.153313</td>
      <td>-0.742711</td>
      <td>3.667236</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.295966</td>
      <td>-3.170842</td>
      <td>4.567190</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.axonserver.connector.heartbeat</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.175500</td>
      <td>-2.739121</td>
      <td>5.266777</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.heartbe...</td>
      <td>axon-server-connector-4.12.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-0.493634</td>
      <td>2.375022</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_25_8.png)
    

