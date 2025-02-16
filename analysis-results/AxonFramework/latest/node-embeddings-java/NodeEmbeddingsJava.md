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
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>commandhandling</td>
      <td>axon-disruptor-4.11.0</td>
      <td>0</td>
      <td>0.012156</td>
      <td>[0.07319182902574539, -0.11561159789562225, 0....</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.modelling.command</td>
      <td>command</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.033013</td>
      <td>[0.0698334202170372, -0.16919010877609253, 0.2...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>inspection</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.019850</td>
      <td>[0.04140711575746536, -0.1820932924747467, 0.2...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command.legacyjpa</td>
      <td>legacyjpa</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.011941</td>
      <td>[-0.06166009232401848, -0.15027368068695068, 0...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.eventsourcing</td>
      <td>eventsourcing</td>
      <td>axon-eventsourcing-4.11.0</td>
      <td>0</td>
      <td>0.017131</td>
      <td>[0.07438604533672333, -0.14707809686660767, 0....</td>
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
       --> Time elapsed: 0.09 seconds
    ===> Calculating affinity matrix...
       --> Time elapsed: 0.00 seconds
    ===> Calculating PCA-based initialization...
       --> Time elapsed: 0.00 seconds
    ===> Running optimization with exaggeration=12.00, lr=9.67 for 250 iterations...
    Iteration   50, KL divergence -1.0225, 50 iterations in 0.0429 sec
    Iteration  100, KL divergence 1.2483, 50 iterations in 0.0108 sec
    Iteration  150, KL divergence 1.2483, 50 iterations in 0.0100 sec
    Iteration  200, KL divergence 1.2483, 50 iterations in 0.0100 sec
    Iteration  250, KL divergence 1.2483, 50 iterations in 0.0099 sec
       --> Time elapsed: 0.08 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...


    Iteration   50, KL divergence 0.2085, 50 iterations in 0.0391 sec
    Iteration  100, KL divergence 0.1648, 50 iterations in 0.0466 sec
    Iteration  150, KL divergence 0.1603, 50 iterations in 0.0466 sec
    Iteration  200, KL divergence 0.1602, 50 iterations in 0.0452 sec
    Iteration  250, KL divergence 0.1603, 50 iterations in 0.0534 sec


    Iteration  300, KL divergence 0.1601, 50 iterations in 0.0451 sec
    Iteration  350, KL divergence 0.1602, 50 iterations in 0.0443 sec
    Iteration  400, KL divergence 0.1600, 50 iterations in 0.0441 sec
    Iteration  450, KL divergence 0.1601, 50 iterations in 0.0440 sec
    Iteration  500, KL divergence 0.1601, 50 iterations in 0.0442 sec
       --> Time elapsed: 0.45 seconds



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
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>axon-disruptor-4.11.0</td>
      <td>0</td>
      <td>0.012156</td>
      <td>-5.092271</td>
      <td>-3.171525</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.modelling.command</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.033013</td>
      <td>-4.451940</td>
      <td>-3.038192</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.019850</td>
      <td>-4.692068</td>
      <td>-2.670332</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command.legacyjpa</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.011941</td>
      <td>-5.843010</td>
      <td>-2.820116</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.eventsourcing</td>
      <td>axon-eventsourcing-4.11.0</td>
      <td>0</td>
      <td>0.017131</td>
      <td>-4.312332</td>
      <td>-2.358277</td>
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
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>commandhandling</td>
      <td>axon-disruptor-4.11.0</td>
      <td>0</td>
      <td>0.012156</td>
      <td>[-0.6495190411806107, -0.6495190411806107, -1....</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.modelling.command</td>
      <td>command</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.033013</td>
      <td>[0.4330126941204071, -1.5155444294214249, 0.21...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>inspection</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.019850</td>
      <td>[-0.8660253882408142, -1.5155444294214249, 0.2...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command.legacyjpa</td>
      <td>legacyjpa</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.011941</td>
      <td>[-0.6495190411806107, -1.5155444294214249, 0.4...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.eventsourcing</td>
      <td>eventsourcing</td>
      <td>axon-eventsourcing-4.11.0</td>
      <td>0</td>
      <td>0.017131</td>
      <td>[-1.0825317353010178, -1.948557123541832, -1.0...</td>
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
       --> Time elapsed: 0.10 seconds
    ===> Running optimization with exaggeration=12.00, lr=9.67 for 250 iterations...
    Iteration   50, KL divergence -0.3986, 50 iterations in 0.0695 sec


    Iteration  100, KL divergence -2.8594, 50 iterations in 0.0278 sec
    Iteration  150, KL divergence 1.2054, 50 iterations in 0.0110 sec
    Iteration  200, KL divergence 1.2054, 50 iterations in 0.0098 sec
    Iteration  250, KL divergence 1.2054, 50 iterations in 0.0097 sec
       --> Time elapsed: 0.13 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.6376, 50 iterations in 0.0415 sec
    Iteration  100, KL divergence 0.6275, 50 iterations in 0.0501 sec
    Iteration  150, KL divergence 0.6263, 50 iterations in 0.0491 sec


    Iteration  200, KL divergence 0.6259, 50 iterations in 0.0502 sec
    Iteration  250, KL divergence 0.6261, 50 iterations in 0.0508 sec
    Iteration  300, KL divergence 0.6262, 50 iterations in 0.0501 sec
    Iteration  350, KL divergence 0.6261, 50 iterations in 0.0500 sec


    Iteration  400, KL divergence 0.6262, 50 iterations in 0.0505 sec
    Iteration  450, KL divergence 0.6261, 50 iterations in 0.0505 sec
    Iteration  500, KL divergence 0.6262, 50 iterations in 0.0508 sec
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
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>axon-disruptor-4.11.0</td>
      <td>0</td>
      <td>0.012156</td>
      <td>1.881062</td>
      <td>1.245779</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.modelling.command</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.033013</td>
      <td>5.195499</td>
      <td>-1.040133</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.019850</td>
      <td>4.268606</td>
      <td>-1.296892</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command.legacyjpa</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.011941</td>
      <td>5.885445</td>
      <td>1.768883</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.eventsourcing</td>
      <td>axon-eventsourcing-4.11.0</td>
      <td>0</td>
      <td>0.017131</td>
      <td>2.820696</td>
      <td>3.477451</td>
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
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>commandhandling</td>
      <td>axon-disruptor-4.11.0</td>
      <td>0</td>
      <td>0.012156</td>
      <td>[0.24934718012809753, 0.05292239785194397, 0.3...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.modelling.command</td>
      <td>command</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.033013</td>
      <td>[0.1892593801021576, 0.075283944606781, 0.2512...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>inspection</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.019850</td>
      <td>[0.4492984116077423, -0.08181710541248322, 0.1...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command.legacyjpa</td>
      <td>legacyjpa</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.011941</td>
      <td>[0.3352530002593994, -0.054873015731573105, 0....</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.eventsourcing</td>
      <td>eventsourcing</td>
      <td>axon-eventsourcing-4.11.0</td>
      <td>0</td>
      <td>0.017131</td>
      <td>[0.18305234611034393, -0.053913407027721405, 0...</td>
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
    Iteration   50, KL divergence -0.4867, 50 iterations in 0.0471 sec
    Iteration  100, KL divergence 1.1778, 50 iterations in 0.0120 sec
    Iteration  150, KL divergence 1.1778, 50 iterations in 0.0101 sec
    Iteration  200, KL divergence 1.1778, 50 iterations in 0.0101 sec
    Iteration  250, KL divergence 1.1778, 50 iterations in 0.0100 sec
       --> Time elapsed: 0.09 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.3508, 50 iterations in 0.0400 sec
    Iteration  100, KL divergence 0.3409, 50 iterations in 0.0516 sec


    Iteration  150, KL divergence 0.3390, 50 iterations in 0.0514 sec
    Iteration  200, KL divergence 0.3375, 50 iterations in 0.0511 sec
    Iteration  250, KL divergence 0.3357, 50 iterations in 0.0510 sec
    Iteration  300, KL divergence 0.3357, 50 iterations in 0.0508 sec


    Iteration  350, KL divergence 0.3356, 50 iterations in 0.0511 sec
    Iteration  400, KL divergence 0.3356, 50 iterations in 0.0505 sec
    Iteration  450, KL divergence 0.3354, 50 iterations in 0.0502 sec
    Iteration  500, KL divergence 0.3354, 50 iterations in 0.0503 sec
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
      <td>org.axonframework.disruptor.commandhandling</td>
      <td>axon-disruptor-4.11.0</td>
      <td>0</td>
      <td>0.012156</td>
      <td>2.167051</td>
      <td>0.360958</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.modelling.command</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.033013</td>
      <td>2.885397</td>
      <td>-0.596777</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.modelling.command.inspection</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.019850</td>
      <td>3.875641</td>
      <td>-0.630526</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.command.legacyjpa</td>
      <td>axon-modelling-4.11.0</td>
      <td>0</td>
      <td>0.011941</td>
      <td>4.538305</td>
      <td>1.458984</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.eventsourcing</td>
      <td>axon-eventsourcing-4.11.0</td>
      <td>0</td>
      <td>0.017131</td>
      <td>2.335855</td>
      <td>-0.509846</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_25_8.png)
    

