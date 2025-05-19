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
      <td>org.axonframework.actuator</td>
      <td>actuator</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.016033</td>
      <td>[0.479514479637146, 0.26002901792526245, 0.430...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.actuator.axonserver</td>
      <td>axonserver</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.012032</td>
      <td>[0.40798240900039673, 0.26484453678131104, 0.6...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.springboot</td>
      <td>springboot</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.025122</td>
      <td>[0.27516859769821167, 0.1610458791255951, 0.52...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.springboot.service.connection</td>
      <td>connection</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.011993</td>
      <td>[0.34944629669189453, 0.19861848652362823, 0.4...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.springboot.autoconfig</td>
      <td>autoconfig</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.013011</td>
      <td>[0.295519083738327, 0.21225126087665558, 0.549...</td>
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
    Iteration   50, KL divergence 0.1359, 50 iterations in 0.0407 sec
    Iteration  100, KL divergence 1.2526, 50 iterations in 0.0108 sec
    Iteration  150, KL divergence 1.2526, 50 iterations in 0.0102 sec
    Iteration  200, KL divergence 1.2526, 50 iterations in 0.0101 sec
    Iteration  250, KL divergence 1.2526, 50 iterations in 0.0123 sec
       --> Time elapsed: 0.08 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.1741, 50 iterations in 0.0373 sec


    Iteration  100, KL divergence 0.1489, 50 iterations in 0.0483 sec


    Iteration  150, KL divergence 0.1435, 50 iterations in 0.0481 sec
    Iteration  200, KL divergence 0.1437, 50 iterations in 0.0469 sec
    Iteration  250, KL divergence 0.1435, 50 iterations in 0.0462 sec
    Iteration  300, KL divergence 0.1436, 50 iterations in 0.0458 sec


    Iteration  350, KL divergence 0.1439, 50 iterations in 0.0471 sec


    Iteration  400, KL divergence 0.1436, 50 iterations in 0.0473 sec
    Iteration  450, KL divergence 0.1438, 50 iterations in 0.0469 sec
    Iteration  500, KL divergence 0.1440, 50 iterations in 0.0461 sec
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
      <td>org.axonframework.actuator</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.016033</td>
      <td>-3.231173</td>
      <td>6.659988</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.actuator.axonserver</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.012032</td>
      <td>-3.005815</td>
      <td>6.546643</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.springboot</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.025122</td>
      <td>-2.897114</td>
      <td>7.199815</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.springboot.service.connection</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.011993</td>
      <td>-2.602932</td>
      <td>5.600352</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.springboot.autoconfig</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.013011</td>
      <td>-2.475842</td>
      <td>6.959947</td>
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
      <td>org.axonframework.actuator</td>
      <td>actuator</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.016033</td>
      <td>[0.4330126941204071, -1.5155444294214249, 0.64...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.actuator.axonserver</td>
      <td>axonserver</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.012032</td>
      <td>[0.0, -1.948557123541832, 0.4330126941204071, ...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.springboot</td>
      <td>springboot</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.025122</td>
      <td>[1.0825317353010178, -1.2990380823612213, 1.08...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.springboot.service.connection</td>
      <td>connection</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.011993</td>
      <td>[0.0, -1.2990380823612213, 0.21650634706020355...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.springboot.autoconfig</td>
      <td>autoconfig</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.013011</td>
      <td>[0.6495190411806107, -0.8660253882408142, 0.0,...</td>
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
    Iteration   50, KL divergence -0.5647, 50 iterations in 0.0712 sec
    Iteration  100, KL divergence 1.2318, 50 iterations in 0.0177 sec
    Iteration  150, KL divergence 1.2318, 50 iterations in 0.0151 sec
    Iteration  200, KL divergence 1.2318, 50 iterations in 0.0119 sec
    Iteration  250, KL divergence 1.2318, 50 iterations in 0.0102 sec
       --> Time elapsed: 0.13 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.6268, 50 iterations in 0.0400 sec


    Iteration  100, KL divergence 0.6017, 50 iterations in 0.0520 sec
    Iteration  150, KL divergence 0.5948, 50 iterations in 0.0511 sec
    Iteration  200, KL divergence 0.5909, 50 iterations in 0.0500 sec
    Iteration  250, KL divergence 0.5904, 50 iterations in 0.0563 sec


    Iteration  300, KL divergence 0.5906, 50 iterations in 0.0521 sec
    Iteration  350, KL divergence 0.5905, 50 iterations in 0.0511 sec
    Iteration  400, KL divergence 0.5903, 50 iterations in 0.0502 sec
    Iteration  450, KL divergence 0.5902, 50 iterations in 0.0502 sec


    Iteration  500, KL divergence 0.5902, 50 iterations in 0.0507 sec
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
      <td>org.axonframework.actuator</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.016033</td>
      <td>2.986049</td>
      <td>-4.888799</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.actuator.axonserver</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.012032</td>
      <td>2.593384</td>
      <td>-5.292505</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.springboot</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.025122</td>
      <td>0.084289</td>
      <td>-3.216256</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.springboot.service.connection</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.011993</td>
      <td>2.013935</td>
      <td>-5.454373</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.springboot.autoconfig</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.013011</td>
      <td>-6.980086</td>
      <td>3.749383</td>
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
      <td>org.axonframework.actuator</td>
      <td>actuator</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.016033</td>
      <td>[0.8700096011161804, 0.6186504364013672, -0.07...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.actuator.axonserver</td>
      <td>axonserver</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.012032</td>
      <td>[0.8898075222969055, 0.5169278979301453, -0.09...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.springboot</td>
      <td>springboot</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.025122</td>
      <td>[0.5271784067153931, -0.009853689931333065, -0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.springboot.service.connection</td>
      <td>connection</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.011993</td>
      <td>[0.23302528262138367, 0.40895938873291016, -0....</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.springboot.autoconfig</td>
      <td>autoconfig</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.013011</td>
      <td>[0.4879651367664337, 0.12227421998977661, -0.0...</td>
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
    Iteration   50, KL divergence -0.8682, 50 iterations in 0.0475 sec
    Iteration  100, KL divergence -2.8971, 50 iterations in 0.0132 sec
    Iteration  150, KL divergence -2.8971, 50 iterations in 0.0119 sec
    Iteration  200, KL divergence -2.8971, 50 iterations in 0.0121 sec
    Iteration  250, KL divergence 1.1676, 50 iterations in 0.0107 sec
       --> Time elapsed: 0.10 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.3396, 50 iterations in 0.0449 sec


    Iteration  100, KL divergence 0.3011, 50 iterations in 0.0535 sec


    Iteration  150, KL divergence 0.2986, 50 iterations in 0.0522 sec
    Iteration  200, KL divergence 0.2982, 50 iterations in 0.0516 sec
    Iteration  250, KL divergence 0.2985, 50 iterations in 0.0495 sec


    Iteration  300, KL divergence 0.2981, 50 iterations in 0.0505 sec


    Iteration  350, KL divergence 0.2983, 50 iterations in 0.0511 sec
    Iteration  400, KL divergence 0.2983, 50 iterations in 0.0503 sec
    Iteration  450, KL divergence 0.2983, 50 iterations in 0.0494 sec
    Iteration  500, KL divergence 0.2981, 50 iterations in 0.0494 sec
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
      <td>org.axonframework.actuator</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.016033</td>
      <td>4.902034</td>
      <td>6.721263</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.actuator.axonserver</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.012032</td>
      <td>4.900662</td>
      <td>6.718804</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.springboot</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.025122</td>
      <td>7.001533</td>
      <td>2.379719</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.springboot.service.connection</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.011993</td>
      <td>7.910060</td>
      <td>6.071901</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.springboot.autoconfig</td>
      <td>axon-spring-boot-autoconfigure-4.11.2</td>
      <td>0</td>
      <td>0.013011</td>
      <td>6.208342</td>
      <td>2.030549</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_23_10.png)
    

