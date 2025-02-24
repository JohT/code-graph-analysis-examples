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
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.016032</td>
      <td>[0.22182150185108185, 0.13067832589149475, 0.2...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.actuator.axonserver</td>
      <td>axonserver</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.012033</td>
      <td>[0.1773374378681183, 0.13082271814346313, 0.29...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.springboot</td>
      <td>springboot</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.025172</td>
      <td>[0.2952502369880676, 0.04961102083325386, 0.32...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.springboot.service.connection</td>
      <td>connection</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.011994</td>
      <td>[0.25010088086128235, 0.14678312838077545, 0.2...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.springboot.autoconfig</td>
      <td>autoconfig</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.013010</td>
      <td>[0.31862837076187134, 0.17515161633491516, 0.2...</td>
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
    ===> Running optimization with exaggeration=12.00, lr=9.67 for 250 iterations...
    Iteration   50, KL divergence -0.8168, 50 iterations in 0.0409 sec
    Iteration  100, KL divergence 1.2321, 50 iterations in 0.0111 sec
    Iteration  150, KL divergence 1.2321, 50 iterations in 0.0101 sec
    Iteration  200, KL divergence 1.2321, 50 iterations in 0.0102 sec
    Iteration  250, KL divergence 1.2321, 50 iterations in 0.0101 sec
       --> Time elapsed: 0.08 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.1764, 50 iterations in 0.0373 sec


    Iteration  100, KL divergence 0.1624, 50 iterations in 0.0501 sec
    Iteration  150, KL divergence 0.1596, 50 iterations in 0.0506 sec
    Iteration  200, KL divergence 0.1598, 50 iterations in 0.0499 sec
    Iteration  250, KL divergence 0.1600, 50 iterations in 0.0480 sec
    Iteration  300, KL divergence 0.1598, 50 iterations in 0.0477 sec


    Iteration  350, KL divergence 0.1599, 50 iterations in 0.0485 sec
    Iteration  400, KL divergence 0.1601, 50 iterations in 0.0483 sec
    Iteration  450, KL divergence 0.1599, 50 iterations in 0.0478 sec
    Iteration  500, KL divergence 0.1598, 50 iterations in 0.0479 sec
       --> Time elapsed: 0.48 seconds



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
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.016032</td>
      <td>-8.078439</td>
      <td>-1.256757</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.actuator.axonserver</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.012033</td>
      <td>-7.483996</td>
      <td>-1.049281</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.springboot</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.025172</td>
      <td>-8.228343</td>
      <td>-0.501003</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.springboot.service.connection</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.011994</td>
      <td>-6.526374</td>
      <td>0.700237</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.springboot.autoconfig</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.013010</td>
      <td>-7.796610</td>
      <td>-0.154023</td>
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
      <td>org.axonframework.actuator</td>
      <td>actuator</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.016032</td>
      <td>[0.6495190411806107, -0.6495190411806107, -0.2...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.actuator.axonserver</td>
      <td>axonserver</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.012033</td>
      <td>[1.2990380823612213, -0.6495190411806107, 0.0,...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.springboot</td>
      <td>springboot</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.025172</td>
      <td>[1.0825317353010178, 0.0, 0.4330126941204071, ...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.springboot.service.connection</td>
      <td>connection</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.011994</td>
      <td>[1.2990380823612213, -0.4330126941204071, -0.2...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.springboot.autoconfig</td>
      <td>autoconfig</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.013010</td>
      <td>[1.2990380823612213, -0.6495190411806107, -0.6...</td>
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
    Iteration   50, KL divergence -0.5673, 50 iterations in 0.0694 sec
    Iteration  100, KL divergence 1.2337, 50 iterations in 0.0174 sec
    Iteration  150, KL divergence 1.2337, 50 iterations in 0.0150 sec
    Iteration  200, KL divergence 1.2337, 50 iterations in 0.0123 sec
    Iteration  250, KL divergence 1.2337, 50 iterations in 0.0100 sec
       --> Time elapsed: 0.12 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.4974, 50 iterations in 0.0367 sec


    Iteration  100, KL divergence 0.4877, 50 iterations in 0.0498 sec
    Iteration  150, KL divergence 0.4877, 50 iterations in 0.0477 sec
    Iteration  200, KL divergence 0.4867, 50 iterations in 0.0468 sec
    Iteration  250, KL divergence 0.4871, 50 iterations in 0.0471 sec
    Iteration  300, KL divergence 0.4872, 50 iterations in 0.0474 sec


    Iteration  350, KL divergence 0.4869, 50 iterations in 0.0490 sec
    Iteration  400, KL divergence 0.4871, 50 iterations in 0.0499 sec
    Iteration  450, KL divergence 0.4870, 50 iterations in 0.0495 sec
    Iteration  500, KL divergence 0.4874, 50 iterations in 0.0498 sec
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
      <td>org.axonframework.actuator</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.016032</td>
      <td>-1.159282</td>
      <td>-8.234627</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.actuator.axonserver</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.012033</td>
      <td>-1.264158</td>
      <td>-8.160727</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.springboot</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.025172</td>
      <td>2.416177</td>
      <td>3.300589</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.springboot.service.connection</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.011994</td>
      <td>-1.944578</td>
      <td>-7.050764</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.springboot.autoconfig</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.013010</td>
      <td>4.364447</td>
      <td>5.546456</td>
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
      <td>org.axonframework.actuator</td>
      <td>actuator</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.016032</td>
      <td>[-0.04189976677298546, 0.3221112787723541, -0....</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.actuator.axonserver</td>
      <td>axonserver</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.012033</td>
      <td>[0.04894734546542168, 0.33538857102394104, -0....</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.springboot</td>
      <td>springboot</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.025172</td>
      <td>[0.17724694311618805, 0.440067321062088, -0.34...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.springboot.service.connection</td>
      <td>connection</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.011994</td>
      <td>[0.5365509986877441, 0.562873125076294, -0.435...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.springboot.autoconfig</td>
      <td>autoconfig</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.013010</td>
      <td>[-0.010833886452019215, 0.09680607169866562, -...</td>
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
    Iteration   50, KL divergence -0.6737, 50 iterations in 0.0480 sec
    Iteration  100, KL divergence -2.8743, 50 iterations in 0.0129 sec
    Iteration  150, KL divergence -2.8743, 50 iterations in 0.0114 sec
    Iteration  200, KL divergence 1.1905, 50 iterations in 0.0103 sec
    Iteration  250, KL divergence 1.1905, 50 iterations in 0.0100 sec
       --> Time elapsed: 0.09 seconds
    ===> Running optimization with exaggeration=1.00, lr=116.00 for 500 iterations...
    Iteration   50, KL divergence 0.3472, 50 iterations in 0.0455 sec


    Iteration  100, KL divergence 0.3274, 50 iterations in 0.0543 sec


    Iteration  150, KL divergence 0.3245, 50 iterations in 0.0536 sec
    Iteration  200, KL divergence 0.3239, 50 iterations in 0.0535 sec
    Iteration  250, KL divergence 0.3185, 50 iterations in 0.0581 sec


    Iteration  300, KL divergence 0.3179, 50 iterations in 0.0522 sec


    Iteration  350, KL divergence 0.3180, 50 iterations in 0.0527 sec
    Iteration  400, KL divergence 0.3180, 50 iterations in 0.0528 sec
    Iteration  450, KL divergence 0.3181, 50 iterations in 0.0521 sec


    Iteration  500, KL divergence 0.3180, 50 iterations in 0.0528 sec
       --> Time elapsed: 0.53 seconds



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
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.016032</td>
      <td>-7.606611</td>
      <td>1.454607</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.actuator.axonserver</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.012033</td>
      <td>-7.663040</td>
      <td>1.463091</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.springboot</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.025172</td>
      <td>-5.991554</td>
      <td>2.929857</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.springboot.service.connection</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.011994</td>
      <td>-8.580361</td>
      <td>3.092644</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.springboot.autoconfig</td>
      <td>axon-spring-boot-autoconfigure-4.11.1</td>
      <td>0</td>
      <td>0.013010</td>
      <td>-5.099886</td>
      <td>2.208683</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_25_11.png)
    

