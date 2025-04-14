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
      <td>org.axonframework.eventsourcing</td>
      <td>eventsourcing</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.017126</td>
      <td>[-0.10686580836772919, -0.585504412651062, 0.3...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>conflictresolution</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012317</td>
      <td>[-0.08751511573791504, -0.6243192553520203, 0....</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.commandhandling</td>
      <td>commandhandling</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.070973</td>
      <td>[-0.09599084407091141, -0.5183320045471191, 0....</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.commandhandling.callbacks</td>
      <td>callbacks</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.015328</td>
      <td>[-0.08961674571037292, -0.4049396514892578, -0...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.commandhandling.distributed</td>
      <td>distributed</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.022596</td>
      <td>[0.067047119140625, -0.48849308490753174, -0.1...</td>
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
    Iteration   50, KL divergence -0.5712, 50 iterations in 0.0424 sec
    Iteration  100, KL divergence 1.2393, 50 iterations in 0.0113 sec
    Iteration  150, KL divergence 1.2393, 50 iterations in 0.0102 sec
    Iteration  200, KL divergence 1.2393, 50 iterations in 0.0102 sec
    Iteration  250, KL divergence 1.2393, 50 iterations in 0.0102 sec
       --> Time elapsed: 0.08 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.1686, 50 iterations in 0.0367 sec


    Iteration  100, KL divergence 0.1532, 50 iterations in 0.0494 sec


    Iteration  150, KL divergence 0.1468, 50 iterations in 0.0487 sec
    Iteration  200, KL divergence 0.1470, 50 iterations in 0.0487 sec
    Iteration  250, KL divergence 0.1468, 50 iterations in 0.0480 sec
    Iteration  300, KL divergence 0.1468, 50 iterations in 0.0479 sec


    Iteration  350, KL divergence 0.1464, 50 iterations in 0.0480 sec


    Iteration  400, KL divergence 0.1466, 50 iterations in 0.0485 sec
    Iteration  450, KL divergence 0.1467, 50 iterations in 0.0473 sec
    Iteration  500, KL divergence 0.1464, 50 iterations in 0.0467 sec
       --> Time elapsed: 0.47 seconds



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
      <td>org.axonframework.eventsourcing</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.017126</td>
      <td>-0.895126</td>
      <td>3.816135</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012317</td>
      <td>-2.043176</td>
      <td>2.513820</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.commandhandling</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.070973</td>
      <td>2.246597</td>
      <td>4.215214</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.commandhandling.callbacks</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.015328</td>
      <td>3.498408</td>
      <td>4.631354</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.commandhandling.distributed</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.022596</td>
      <td>3.066986</td>
      <td>4.041368</td>
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
      <td>org.axonframework.eventsourcing</td>
      <td>eventsourcing</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.017126</td>
      <td>[-0.8660253882408142, -0.4330126941204071, 0.2...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>conflictresolution</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012317</td>
      <td>[-0.4330126941204071, -0.4330126941204071, -0....</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.commandhandling</td>
      <td>commandhandling</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.070973</td>
      <td>[-0.6495190411806107, -0.21650634706020355, -1...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.commandhandling.callbacks</td>
      <td>callbacks</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.015328</td>
      <td>[0.0, -1.0825317353010178, -0.6495190411806107...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.commandhandling.distributed</td>
      <td>distributed</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.022596</td>
      <td>[-2.1650634706020355, -0.21650634706020355, -0...</td>
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
    Iteration   50, KL divergence -0.5083, 50 iterations in 0.0698 sec
    Iteration  100, KL divergence 1.2419, 50 iterations in 0.0176 sec
    Iteration  150, KL divergence 1.2419, 50 iterations in 0.0152 sec
    Iteration  200, KL divergence 1.2419, 50 iterations in 0.0124 sec
    Iteration  250, KL divergence 1.2419, 50 iterations in 0.0104 sec
       --> Time elapsed: 0.13 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.5700, 50 iterations in 0.0395 sec


    Iteration  100, KL divergence 0.5534, 50 iterations in 0.0530 sec
    Iteration  150, KL divergence 0.5525, 50 iterations in 0.0525 sec
    Iteration  200, KL divergence 0.5499, 50 iterations in 0.0525 sec
    Iteration  250, KL divergence 0.5497, 50 iterations in 0.0526 sec


    Iteration  300, KL divergence 0.5495, 50 iterations in 0.0532 sec
    Iteration  350, KL divergence 0.5495, 50 iterations in 0.0526 sec
    Iteration  400, KL divergence 0.5498, 50 iterations in 0.0519 sec
    Iteration  450, KL divergence 0.5497, 50 iterations in 0.0523 sec


    Iteration  500, KL divergence 0.5496, 50 iterations in 0.0530 sec
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
      <td>org.axonframework.eventsourcing</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.017126</td>
      <td>-0.614392</td>
      <td>-2.137867</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012317</td>
      <td>2.397422</td>
      <td>-0.039932</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.commandhandling</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.070973</td>
      <td>-3.322770</td>
      <td>-2.162414</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.commandhandling.callbacks</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.015328</td>
      <td>-6.251502</td>
      <td>-2.406126</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.commandhandling.distributed</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.022596</td>
      <td>-4.444918</td>
      <td>-2.161663</td>
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
      <td>org.axonframework.eventsourcing</td>
      <td>eventsourcing</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.017126</td>
      <td>[0.15337468683719635, -0.46430152654647827, -0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>conflictresolution</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012317</td>
      <td>[0.17244575917720795, -0.2731046974658966, -0....</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.commandhandling</td>
      <td>commandhandling</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.070973</td>
      <td>[0.24176724255084991, -0.2852061688899994, -0....</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.commandhandling.callbacks</td>
      <td>callbacks</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.015328</td>
      <td>[-0.12481729686260223, -0.11538942903280258, -...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.commandhandling.distributed</td>
      <td>distributed</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.022596</td>
      <td>[0.16083534061908722, -0.13185352087020874, -0...</td>
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
    Iteration   50, KL divergence -1.1806, 50 iterations in 0.0473 sec
    Iteration  100, KL divergence 1.1689, 50 iterations in 0.0123 sec
    Iteration  150, KL divergence 1.1689, 50 iterations in 0.0103 sec
    Iteration  200, KL divergence 1.1689, 50 iterations in 0.0103 sec
    Iteration  250, KL divergence 1.1689, 50 iterations in 0.0102 sec
       --> Time elapsed: 0.09 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.4324, 50 iterations in 0.0447 sec
    Iteration  100, KL divergence 0.4144, 50 iterations in 0.0510 sec


    Iteration  150, KL divergence 0.4018, 50 iterations in 0.0524 sec
    Iteration  200, KL divergence 0.3922, 50 iterations in 0.0503 sec
    Iteration  250, KL divergence 0.3827, 50 iterations in 0.0485 sec
    Iteration  300, KL divergence 0.3827, 50 iterations in 0.0495 sec
    Iteration  350, KL divergence 0.3817, 50 iterations in 0.0492 sec


    Iteration  400, KL divergence 0.3817, 50 iterations in 0.0504 sec
    Iteration  450, KL divergence 0.3816, 50 iterations in 0.0509 sec
    Iteration  500, KL divergence 0.3818, 50 iterations in 0.0509 sec
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
      <td>org.axonframework.eventsourcing</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.017126</td>
      <td>-2.519250</td>
      <td>1.597505</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012317</td>
      <td>-0.825288</td>
      <td>1.675254</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.commandhandling</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.070973</td>
      <td>-6.519362</td>
      <td>4.394452</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.commandhandling.callbacks</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.015328</td>
      <td>-6.887415</td>
      <td>4.582360</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.commandhandling.distributed</td>
      <td>axon-messaging-4.11.1</td>
      <td>0</td>
      <td>0.022596</td>
      <td>-5.467332</td>
      <td>5.531416</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_23_8.png)
    

