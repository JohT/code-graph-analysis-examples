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
      <td>[-0.11377386748790741, -0.0631684958934784, -0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>conflictresolution</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012317</td>
      <td>[-0.17257723212242126, 0.014088433235883713, -...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>commandhandling</td>
      <td>axon-disruptor-4.11.1</td>
      <td>0</td>
      <td>0.012155</td>
      <td>[-0.20612820982933044, -0.07834579050540924, -...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command</td>
      <td>command</td>
      <td>axon-modelling-4.11.1</td>
      <td>0</td>
      <td>0.033006</td>
      <td>[-0.18261972069740295, -0.09530505537986755, -...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>inspection</td>
      <td>axon-modelling-4.11.1</td>
      <td>0</td>
      <td>0.019848</td>
      <td>[-0.19546182453632355, 0.02368229627609253, -0...</td>
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
    Iteration   50, KL divergence -0.3782, 50 iterations in 0.0456 sec
    Iteration  100, KL divergence 1.2505, 50 iterations in 0.0116 sec
    Iteration  150, KL divergence 1.2505, 50 iterations in 0.0103 sec
    Iteration  200, KL divergence 1.2505, 50 iterations in 0.0108 sec
    Iteration  250, KL divergence 1.2505, 50 iterations in 0.0104 sec
       --> Time elapsed: 0.09 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.2110, 50 iterations in 0.0372 sec


    Iteration  100, KL divergence 0.1878, 50 iterations in 0.0499 sec
    Iteration  150, KL divergence 0.1754, 50 iterations in 0.0474 sec
    Iteration  200, KL divergence 0.1752, 50 iterations in 0.0461 sec
    Iteration  250, KL divergence 0.1753, 50 iterations in 0.0460 sec
    Iteration  300, KL divergence 0.1752, 50 iterations in 0.0461 sec


    Iteration  350, KL divergence 0.1755, 50 iterations in 0.0470 sec
    Iteration  400, KL divergence 0.1754, 50 iterations in 0.0464 sec
    Iteration  450, KL divergence 0.1754, 50 iterations in 0.0461 sec
    Iteration  500, KL divergence 0.1754, 50 iterations in 0.0454 sec
       --> Time elapsed: 0.46 seconds



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
      <td>-3.902253</td>
      <td>-0.633782</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012317</td>
      <td>-3.333950</td>
      <td>0.415560</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>axon-disruptor-4.11.1</td>
      <td>0</td>
      <td>0.012155</td>
      <td>-4.399996</td>
      <td>-2.101618</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command</td>
      <td>axon-modelling-4.11.1</td>
      <td>0</td>
      <td>0.033006</td>
      <td>-4.159437</td>
      <td>-1.528784</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>axon-modelling-4.11.1</td>
      <td>0</td>
      <td>0.019848</td>
      <td>-3.898559</td>
      <td>-0.994458</td>
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
      <td>[0.0, -0.8660253882408142, -0.2165063470602035...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>conflictresolution</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012317</td>
      <td>[0.6495190411806107, -1.2990380823612213, -0.2...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>commandhandling</td>
      <td>axon-disruptor-4.11.1</td>
      <td>0</td>
      <td>0.012155</td>
      <td>[0.6495190411806107, -0.6495190411806107, -0.4...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command</td>
      <td>command</td>
      <td>axon-modelling-4.11.1</td>
      <td>0</td>
      <td>0.033006</td>
      <td>[0.6495190411806107, -0.8660253882408142, -0.8...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>inspection</td>
      <td>axon-modelling-4.11.1</td>
      <td>0</td>
      <td>0.019848</td>
      <td>[1.0825317353010178, -0.6495190411806107, -0.8...</td>
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
    Iteration   50, KL divergence -0.2450, 50 iterations in 0.0696 sec
    Iteration  100, KL divergence 1.2364, 50 iterations in 0.0187 sec
    Iteration  150, KL divergence 1.2364, 50 iterations in 0.0153 sec
    Iteration  200, KL divergence 1.2364, 50 iterations in 0.0120 sec
    Iteration  250, KL divergence 1.2364, 50 iterations in 0.0104 sec
       --> Time elapsed: 0.13 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.5984, 50 iterations in 0.0391 sec


    Iteration  100, KL divergence 0.5914, 50 iterations in 0.0519 sec
    Iteration  150, KL divergence 0.5900, 50 iterations in 0.0506 sec
    Iteration  200, KL divergence 0.5899, 50 iterations in 0.0505 sec
    Iteration  250, KL divergence 0.5896, 50 iterations in 0.0499 sec


    Iteration  300, KL divergence 0.5902, 50 iterations in 0.0507 sec
    Iteration  350, KL divergence 0.5899, 50 iterations in 0.0499 sec
    Iteration  400, KL divergence 0.5901, 50 iterations in 0.0496 sec
    Iteration  450, KL divergence 0.5902, 50 iterations in 0.0494 sec
    Iteration  500, KL divergence 0.5903, 50 iterations in 0.0496 sec
       --> Time elapsed: 0.49 seconds



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
      <td>3.128942</td>
      <td>-2.385446</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012317</td>
      <td>3.360119</td>
      <td>-0.723023</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>axon-disruptor-4.11.1</td>
      <td>0</td>
      <td>0.012155</td>
      <td>4.751606</td>
      <td>-2.043786</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command</td>
      <td>axon-modelling-4.11.1</td>
      <td>0</td>
      <td>0.033006</td>
      <td>3.639634</td>
      <td>-1.195082</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>axon-modelling-4.11.1</td>
      <td>0</td>
      <td>0.019848</td>
      <td>4.616553</td>
      <td>-1.270090</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_21_8.png)
    


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
      <td>[-0.5916745066642761, 0.25714316964149475, 0.2...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>conflictresolution</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012317</td>
      <td>[-0.5582274794578552, 0.17233936488628387, 0.2...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>commandhandling</td>
      <td>axon-disruptor-4.11.1</td>
      <td>0</td>
      <td>0.012155</td>
      <td>[-0.46858924627304077, 0.2973204553127289, 0.1...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command</td>
      <td>command</td>
      <td>axon-modelling-4.11.1</td>
      <td>0</td>
      <td>0.033006</td>
      <td>[-0.5826924443244934, 0.06509067863225937, 0.1...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>inspection</td>
      <td>axon-modelling-4.11.1</td>
      <td>0</td>
      <td>0.019848</td>
      <td>[-0.492026150226593, -0.07846558094024658, 0.1...</td>
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
    Iteration   50, KL divergence -0.5815, 50 iterations in 0.0468 sec
    Iteration  100, KL divergence -2.8758, 50 iterations in 0.0131 sec
    Iteration  150, KL divergence 1.1933, 50 iterations in 0.0107 sec
    Iteration  200, KL divergence 1.1933, 50 iterations in 0.0113 sec
    Iteration  250, KL divergence 1.1933, 50 iterations in 0.0106 sec
       --> Time elapsed: 0.09 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.2895, 50 iterations in 0.0396 sec
    Iteration  100, KL divergence 0.2433, 50 iterations in 0.0493 sec


    Iteration  150, KL divergence 0.2343, 50 iterations in 0.0497 sec
    Iteration  200, KL divergence 0.2342, 50 iterations in 0.0500 sec
    Iteration  250, KL divergence 0.2340, 50 iterations in 0.0499 sec
    Iteration  300, KL divergence 0.2345, 50 iterations in 0.0500 sec
    Iteration  350, KL divergence 0.2344, 50 iterations in 0.0495 sec


    Iteration  400, KL divergence 0.2345, 50 iterations in 0.0505 sec
    Iteration  450, KL divergence 0.2342, 50 iterations in 0.0507 sec
    Iteration  500, KL divergence 0.2346, 50 iterations in 0.0497 sec
       --> Time elapsed: 0.49 seconds



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
      <td>0.702522</td>
      <td>1.382881</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.eventsourcing.conflictresolu...</td>
      <td>axon-eventsourcing-4.11.1</td>
      <td>0</td>
      <td>0.012317</td>
      <td>0.414085</td>
      <td>0.840785</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>axon-disruptor-4.11.1</td>
      <td>0</td>
      <td>0.012155</td>
      <td>2.118847</td>
      <td>1.110407</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command</td>
      <td>axon-modelling-4.11.1</td>
      <td>0</td>
      <td>0.033006</td>
      <td>0.715752</td>
      <td>2.199322</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>axon-modelling-4.11.1</td>
      <td>0</td>
      <td>0.019848</td>
      <td>1.570136</td>
      <td>2.643903</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_23_8.png)
    

