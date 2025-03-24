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
      <td>org.axonframework.config</td>
      <td>config</td>
      <td>axon-configuration-4.11.1</td>
      <td>0</td>
      <td>0.026304</td>
      <td>[-0.28918302059173584, -0.2171250581741333, -0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.eventstore</td>
      <td>eventstore</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.035726</td>
      <td>[-0.5323679447174072, -0.23136034607887268, -0...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.eventsourcing.eventstore.inm...</td>
      <td>inmemory</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.011941</td>
      <td>[-0.2160782814025879, -0.08594624698162079, -0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.eventsourcing.eventstore.jdbc</td>
      <td>jdbc</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.022978</td>
      <td>[-0.5992332696914673, -0.16151545941829681, -0...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.eventsourcing.eventstore.jpa</td>
      <td>jpa</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012970</td>
      <td>[-0.2872907817363739, -0.09887191653251648, 0....</td>
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
       --> Time elapsed: 0.02 seconds
    ===> Calculating affinity matrix...
       --> Time elapsed: 0.00 seconds
    ===> Calculating PCA-based initialization...
       --> Time elapsed: 0.00 seconds
    ===> Running optimization with exaggeration=12.00, lr=9.67 for 250 iterations...
    Iteration   50, KL divergence -1.1276, 50 iterations in 0.0443 sec
    Iteration  100, KL divergence 1.2289, 50 iterations in 0.0114 sec
    Iteration  150, KL divergence 1.2289, 50 iterations in 0.0102 sec
    Iteration  200, KL divergence 1.2289, 50 iterations in 0.0101 sec
    Iteration  250, KL divergence 1.2289, 50 iterations in 0.0101 sec
       --> Time elapsed: 0.09 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.1936, 50 iterations in 0.0385 sec


    Iteration  100, KL divergence 0.1786, 50 iterations in 0.0525 sec
    Iteration  150, KL divergence 0.1740, 50 iterations in 0.0519 sec
    Iteration  200, KL divergence 0.1737, 50 iterations in 0.0508 sec
    Iteration  250, KL divergence 0.1733, 50 iterations in 0.0505 sec


    Iteration  300, KL divergence 0.1733, 50 iterations in 0.0514 sec
    Iteration  350, KL divergence 0.1731, 50 iterations in 0.0505 sec
    Iteration  400, KL divergence 0.1734, 50 iterations in 0.0511 sec
    Iteration  450, KL divergence 0.1736, 50 iterations in 0.0501 sec


    Iteration  500, KL divergence 0.1731, 50 iterations in 0.0496 sec
       --> Time elapsed: 0.50 seconds



    (116, 2)



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
      <td>org.axonframework.config</td>
      <td>axon-configuration-4.11.1</td>
      <td>0</td>
      <td>0.026304</td>
      <td>-1.759446</td>
      <td>-0.470833</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.eventstore</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.035726</td>
      <td>1.015544</td>
      <td>-4.407028</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.eventsourcing.eventstore.inm...</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.011941</td>
      <td>-0.964234</td>
      <td>-4.060937</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.eventsourcing.eventstore.jdbc</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.022978</td>
      <td>-2.016357</td>
      <td>-6.790448</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.eventsourcing.eventstore.jpa</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012970</td>
      <td>0.323770</td>
      <td>-3.947835</td>
    </tr>
  </tbody>
</table>
</div>


### 1.3 Visualization of the node embeddings reduced to two dimensions


    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_19_0.png)
    


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
      <td>org.axonframework.config</td>
      <td>config</td>
      <td>axon-configuration-4.11.1</td>
      <td>0</td>
      <td>0.026304</td>
      <td>[0.21650634706020355, 0.21650634706020355, -1....</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.eventstore</td>
      <td>eventstore</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.035726</td>
      <td>[0.8660253882408142, -2.1650634706020355, -1.2...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.eventsourcing.eventstore.inm...</td>
      <td>inmemory</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.011941</td>
      <td>[-0.4330126941204071, -0.6495190411806107, 0.0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.eventsourcing.eventstore.jdbc</td>
      <td>jdbc</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.022978</td>
      <td>[-0.21650634706020355, -0.8660253882408142, -1...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.eventsourcing.eventstore.jpa</td>
      <td>jpa</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012970</td>
      <td>[-1.2990380823612213, -1.0825317353010178, -0....</td>
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
       --> Time elapsed: 0.01 seconds
    ===> Running optimization with exaggeration=12.00, lr=9.67 for 250 iterations...
    Iteration   50, KL divergence -0.7383, 50 iterations in 0.0673 sec
    Iteration  100, KL divergence 1.2422, 50 iterations in 0.0170 sec
    Iteration  150, KL divergence 1.2422, 50 iterations in 0.0150 sec
    Iteration  200, KL divergence 1.2422, 50 iterations in 0.0133 sec
    Iteration  250, KL divergence 1.2422, 50 iterations in 0.0099 sec
       --> Time elapsed: 0.12 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.6090, 50 iterations in 0.0374 sec


    Iteration  100, KL divergence 0.6004, 50 iterations in 0.0552 sec
    Iteration  150, KL divergence 0.5973, 50 iterations in 0.0518 sec
    Iteration  200, KL divergence 0.5972, 50 iterations in 0.0517 sec
    Iteration  250, KL divergence 0.5972, 50 iterations in 0.0516 sec


    Iteration  300, KL divergence 0.5975, 50 iterations in 0.0520 sec
    Iteration  350, KL divergence 0.5975, 50 iterations in 0.0528 sec
    Iteration  400, KL divergence 0.5972, 50 iterations in 0.0535 sec
    Iteration  450, KL divergence 0.5975, 50 iterations in 0.0539 sec


    Iteration  500, KL divergence 0.5974, 50 iterations in 0.0541 sec
       --> Time elapsed: 0.51 seconds



    (116, 2)



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
      <td>org.axonframework.config</td>
      <td>axon-configuration-4.11.1</td>
      <td>0</td>
      <td>0.026304</td>
      <td>-5.819005</td>
      <td>0.500981</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.eventstore</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.035726</td>
      <td>-8.379437</td>
      <td>-1.292311</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.eventsourcing.eventstore.inm...</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.011941</td>
      <td>0.436887</td>
      <td>6.942537</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.eventsourcing.eventstore.jdbc</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.022978</td>
      <td>-4.793485</td>
      <td>4.995128</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.eventsourcing.eventstore.jpa</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012970</td>
      <td>-4.753637</td>
      <td>3.309032</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_21_9.png)
    


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
      <td>org.axonframework.config</td>
      <td>config</td>
      <td>axon-configuration-4.11.1</td>
      <td>0</td>
      <td>0.026304</td>
      <td>[0.25365686416625977, -0.44706737995147705, 0....</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.eventstore</td>
      <td>eventstore</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.035726</td>
      <td>[0.4675859808921814, -0.6033666729927063, 0.22...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.eventsourcing.eventstore.inm...</td>
      <td>inmemory</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.011941</td>
      <td>[0.36969777941703796, -0.5103996396064758, 0.1...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.eventsourcing.eventstore.jdbc</td>
      <td>jdbc</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.022978</td>
      <td>[0.3120621144771576, -0.42582106590270996, 0.4...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.eventsourcing.eventstore.jpa</td>
      <td>jpa</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012970</td>
      <td>[0.3966706693172455, -0.47492745518684387, 0.1...</td>
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
    ===> Running optimization with exaggeration=12.00, lr=9.67 for 250 iterations...
    Iteration   50, KL divergence -0.4850, 50 iterations in 0.0480 sec
    Iteration  100, KL divergence -2.8916, 50 iterations in 0.0142 sec
    Iteration  150, KL divergence 1.1732, 50 iterations in 0.0106 sec
    Iteration  200, KL divergence 1.1732, 50 iterations in 0.0101 sec
    Iteration  250, KL divergence 1.1732, 50 iterations in 0.0102 sec
       --> Time elapsed: 0.09 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.3187, 50 iterations in 0.0421 sec
    Iteration  100, KL divergence 0.2982, 50 iterations in 0.0501 sec


    Iteration  150, KL divergence 0.2983, 50 iterations in 0.0511 sec
    Iteration  200, KL divergence 0.2988, 50 iterations in 0.0510 sec
    Iteration  250, KL divergence 0.2989, 50 iterations in 0.0506 sec
    Iteration  300, KL divergence 0.2988, 50 iterations in 0.0508 sec


    Iteration  350, KL divergence 0.2992, 50 iterations in 0.0548 sec
    Iteration  400, KL divergence 0.2991, 50 iterations in 0.0523 sec
    Iteration  450, KL divergence 0.2989, 50 iterations in 0.0506 sec
    Iteration  500, KL divergence 0.2988, 50 iterations in 0.0505 sec
       --> Time elapsed: 0.50 seconds



    (116, 2)



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
      <td>org.axonframework.config</td>
      <td>axon-configuration-4.11.1</td>
      <td>0</td>
      <td>0.026304</td>
      <td>0.510999</td>
      <td>-0.994986</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.eventstore</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.035726</td>
      <td>4.545241</td>
      <td>0.293533</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.eventsourcing.eventstore.inm...</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.011941</td>
      <td>3.041052</td>
      <td>-0.083640</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.eventsourcing.eventstore.jdbc</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.022978</td>
      <td>6.644166</td>
      <td>0.398179</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.eventsourcing.eventstore.jpa</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012970</td>
      <td>3.754827</td>
      <td>-0.354880</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_23_8.png)
    

