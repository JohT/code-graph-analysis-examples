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
      <td>axon-eventsourcing-4.11.2</td>
      <td>0</td>
      <td>0.215085</td>
      <td>[-0.16198427975177765, -0.19347916543483734, 0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>conflictresolution</td>
      <td>axon-eventsourcing-4.11.2</td>
      <td>0</td>
      <td>0.154712</td>
      <td>[-0.15265756845474243, -0.22714993357658386, 0...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>commandhandling</td>
      <td>axon-disruptor-4.11.2</td>
      <td>0</td>
      <td>0.152680</td>
      <td>[-0.2465260922908783, -0.2163395881652832, 0.0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command</td>
      <td>command</td>
      <td>axon-modelling-4.11.2</td>
      <td>0</td>
      <td>0.415184</td>
      <td>[-0.323282390832901, -0.16630016267299652, 0.0...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>inspection</td>
      <td>axon-modelling-4.11.2</td>
      <td>0</td>
      <td>0.249377</td>
      <td>[-0.28761762380599976, -0.18274624645709991, 0...</td>
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
    Iteration   50, KL divergence -0.0519, 50 iterations in 0.0402 sec
    Iteration  100, KL divergence 1.2365, 50 iterations in 0.0113 sec
    Iteration  150, KL divergence 1.2365, 50 iterations in 0.0104 sec
    Iteration  200, KL divergence 1.2365, 50 iterations in 0.0104 sec
    Iteration  250, KL divergence 1.2365, 50 iterations in 0.0103 sec
       --> Time elapsed: 0.08 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.1785, 50 iterations in 0.0363 sec


    Iteration  100, KL divergence 0.1543, 50 iterations in 0.0489 sec


    Iteration  150, KL divergence 0.1493, 50 iterations in 0.0498 sec
    Iteration  200, KL divergence 0.1470, 50 iterations in 0.0489 sec
    Iteration  250, KL divergence 0.1471, 50 iterations in 0.0475 sec
    Iteration  300, KL divergence 0.1472, 50 iterations in 0.0474 sec


    Iteration  350, KL divergence 0.1471, 50 iterations in 0.0481 sec


    Iteration  400, KL divergence 0.1471, 50 iterations in 0.0487 sec
    Iteration  450, KL divergence 0.1472, 50 iterations in 0.0479 sec
    Iteration  500, KL divergence 0.1472, 50 iterations in 0.0478 sec
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
      <td>axon-eventsourcing-4.11.2</td>
      <td>0</td>
      <td>0.215085</td>
      <td>3.957771</td>
      <td>-0.932831</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>axon-eventsourcing-4.11.2</td>
      <td>0</td>
      <td>0.154712</td>
      <td>3.686600</td>
      <td>-0.067772</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>axon-disruptor-4.11.2</td>
      <td>0</td>
      <td>0.152680</td>
      <td>4.393888</td>
      <td>-2.150710</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command</td>
      <td>axon-modelling-4.11.2</td>
      <td>0</td>
      <td>0.415184</td>
      <td>4.229732</td>
      <td>-1.776457</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>axon-modelling-4.11.2</td>
      <td>0</td>
      <td>0.249377</td>
      <td>4.530210</td>
      <td>-1.482214</td>
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
      <td>axon-eventsourcing-4.11.2</td>
      <td>0</td>
      <td>0.215085</td>
      <td>[0.0, -0.8660253882408142, -1.2990380823612213...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>conflictresolution</td>
      <td>axon-eventsourcing-4.11.2</td>
      <td>0</td>
      <td>0.154712</td>
      <td>[0.0, -2.1650634706020355, -0.6495190411806107...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>commandhandling</td>
      <td>axon-disruptor-4.11.2</td>
      <td>0</td>
      <td>0.152680</td>
      <td>[-0.8660253882408142, -0.6495190411806107, -1....</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command</td>
      <td>command</td>
      <td>axon-modelling-4.11.2</td>
      <td>0</td>
      <td>0.415184</td>
      <td>[-0.21650634706020355, -0.8660253882408142, -1...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>inspection</td>
      <td>axon-modelling-4.11.2</td>
      <td>0</td>
      <td>0.249377</td>
      <td>[-0.6495190411806107, -1.948557123541832, -1.5...</td>
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
    Iteration   50, KL divergence -1.1026, 50 iterations in 0.0914 sec
    Iteration  100, KL divergence 1.2406, 50 iterations in 0.0178 sec
    Iteration  150, KL divergence 1.2406, 50 iterations in 0.0102 sec
    Iteration  200, KL divergence 1.2406, 50 iterations in 0.0102 sec
    Iteration  250, KL divergence 1.2406, 50 iterations in 0.0103 sec
       --> Time elapsed: 0.14 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.5900, 50 iterations in 0.0395 sec


    Iteration  100, KL divergence 0.5602, 50 iterations in 0.0534 sec
    Iteration  150, KL divergence 0.5583, 50 iterations in 0.0526 sec
    Iteration  200, KL divergence 0.5582, 50 iterations in 0.0534 sec
    Iteration  250, KL divergence 0.5583, 50 iterations in 0.0536 sec


    Iteration  300, KL divergence 0.5575, 50 iterations in 0.0545 sec
    Iteration  350, KL divergence 0.5574, 50 iterations in 0.0546 sec
    Iteration  400, KL divergence 0.5575, 50 iterations in 0.0543 sec
    Iteration  450, KL divergence 0.5576, 50 iterations in 0.0538 sec


    Iteration  500, KL divergence 0.5577, 50 iterations in 0.0540 sec
       --> Time elapsed: 0.52 seconds



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
      <td>axon-eventsourcing-4.11.2</td>
      <td>0</td>
      <td>0.215085</td>
      <td>2.096190</td>
      <td>8.012907</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>axon-eventsourcing-4.11.2</td>
      <td>0</td>
      <td>0.154712</td>
      <td>2.625525</td>
      <td>0.559214</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>axon-disruptor-4.11.2</td>
      <td>0</td>
      <td>0.152680</td>
      <td>4.666791</td>
      <td>8.429115</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command</td>
      <td>axon-modelling-4.11.2</td>
      <td>0</td>
      <td>0.415184</td>
      <td>3.328025</td>
      <td>8.118217</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>axon-modelling-4.11.2</td>
      <td>0</td>
      <td>0.249377</td>
      <td>3.304516</td>
      <td>8.112345</td>
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
      <td>axon-eventsourcing-4.11.2</td>
      <td>0</td>
      <td>0.215085</td>
      <td>[0.4915933907032013, 0.45673155784606934, -0.4...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>conflictresolution</td>
      <td>axon-eventsourcing-4.11.2</td>
      <td>0</td>
      <td>0.154712</td>
      <td>[0.2977370023727417, 0.3300282657146454, -0.30...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>commandhandling</td>
      <td>axon-disruptor-4.11.2</td>
      <td>0</td>
      <td>0.152680</td>
      <td>[0.45150187611579895, 0.40339359641075134, -0....</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command</td>
      <td>command</td>
      <td>axon-modelling-4.11.2</td>
      <td>0</td>
      <td>0.415184</td>
      <td>[0.43193694949150085, 0.4029911160469055, -0.1...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>inspection</td>
      <td>axon-modelling-4.11.2</td>
      <td>0</td>
      <td>0.249377</td>
      <td>[0.40448322892189026, 0.33430758118629456, -0....</td>
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
    Iteration   50, KL divergence -0.4527, 50 iterations in 0.0465 sec
    Iteration  100, KL divergence 1.1897, 50 iterations in 0.0119 sec
    Iteration  150, KL divergence 1.1897, 50 iterations in 0.0119 sec
    Iteration  200, KL divergence 1.1897, 50 iterations in 0.0107 sec
    Iteration  250, KL divergence 1.1897, 50 iterations in 0.0105 sec
       --> Time elapsed: 0.09 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.3791, 50 iterations in 0.0395 sec
    Iteration  100, KL divergence 0.3449, 50 iterations in 0.0516 sec


    Iteration  150, KL divergence 0.3230, 50 iterations in 0.0529 sec
    Iteration  200, KL divergence 0.3223, 50 iterations in 0.0517 sec
    Iteration  250, KL divergence 0.3227, 50 iterations in 0.0510 sec
    Iteration  300, KL divergence 0.3222, 50 iterations in 0.0510 sec


    Iteration  350, KL divergence 0.3223, 50 iterations in 0.0516 sec
    Iteration  400, KL divergence 0.3218, 50 iterations in 0.0512 sec
    Iteration  450, KL divergence 0.3217, 50 iterations in 0.0507 sec
    Iteration  500, KL divergence 0.3220, 50 iterations in 0.0512 sec
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
      <td>axon-eventsourcing-4.11.2</td>
      <td>0</td>
      <td>0.215085</td>
      <td>-4.760902</td>
      <td>0.127959</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>axon-eventsourcing-4.11.2</td>
      <td>0</td>
      <td>0.154712</td>
      <td>-4.257110</td>
      <td>-0.343938</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>axon-disruptor-4.11.2</td>
      <td>0</td>
      <td>0.152680</td>
      <td>-4.984525</td>
      <td>-0.074274</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command</td>
      <td>axon-modelling-4.11.2</td>
      <td>0</td>
      <td>0.415184</td>
      <td>-6.273546</td>
      <td>0.281226</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>axon-modelling-4.11.2</td>
      <td>0</td>
      <td>0.249377</td>
      <td>-4.596063</td>
      <td>0.732510</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_23_8.png)
    

