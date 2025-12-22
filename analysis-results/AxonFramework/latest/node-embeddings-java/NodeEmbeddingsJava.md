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





    The openTSNE version is: 1.0.4
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
      <td>org.axonframework.extension.metrics.micrometer</td>
      <td>micrometer</td>
      <td>axon-metrics-micrometer-5.0.0</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.06471307575702667, -0.2933361530303955, 0.6...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.extension.metrics.micrometer...</td>
      <td>reservoir</td>
      <td>axon-metrics-micrometer-5.0.0</td>
      <td>0</td>
      <td>0.173182</td>
      <td>[0.045119013637304306, -0.38521111011505127, 0...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.infra</td>
      <td>infra</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>0.822416</td>
      <td>[0.13393719494342804, -0.3714454770088196, 0.2...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.configuration</td>
      <td>configuration</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>1.374842</td>
      <td>[0.07136408984661102, -0.29010772705078125, 0....</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.messaging.monitoring</td>
      <td>monitoring</td>
      <td>axon-messaging-5.0.0</td>
      <td>0</td>
      <td>0.281048</td>
      <td>[0.09050509333610535, -0.4365323781967163, 0.5...</td>
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
    ===> Running optimization with exaggeration=12.00, lr=9.42 for 250 iterations...
    Iteration   50, KL divergence -0.7165, 50 iterations in 0.0147 sec
    Iteration  100, KL divergence 1.1787, 50 iterations in 0.0098 sec
    Iteration  150, KL divergence 1.1787, 50 iterations in 0.0098 sec
    Iteration  200, KL divergence 1.1787, 50 iterations in 0.0097 sec
    Iteration  250, KL divergence 1.1787, 50 iterations in 0.0097 sec
       --> Time elapsed: 0.05 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.2424, 50 iterations in 0.0143 sec
    Iteration  100, KL divergence 0.2257, 50 iterations in 0.0159 sec
    Iteration  150, KL divergence 0.2241, 50 iterations in 0.0166 sec
    Iteration  200, KL divergence 0.2242, 50 iterations in 0.0162 sec
    Iteration  250, KL divergence 0.2240, 50 iterations in 0.0161 sec
    Iteration  300, KL divergence 0.2242, 50 iterations in 0.0163 sec
    Iteration  350, KL divergence 0.2243, 50 iterations in 0.0161 sec


    Iteration  400, KL divergence 0.2243, 50 iterations in 0.0171 sec
    Iteration  450, KL divergence 0.2264, 50 iterations in 0.0164 sec
    Iteration  500, KL divergence 0.2269, 50 iterations in 0.0161 sec
       --> Time elapsed: 0.16 seconds



    (113, 2)



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
      <td>org.axonframework.extension.metrics.micrometer</td>
      <td>axon-metrics-micrometer-5.0.0</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-4.239730</td>
      <td>6.861290</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.extension.metrics.micrometer...</td>
      <td>axon-metrics-micrometer-5.0.0</td>
      <td>0</td>
      <td>0.173182</td>
      <td>-4.290205</td>
      <td>6.928121</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.infra</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>0.822416</td>
      <td>2.539156</td>
      <td>0.622459</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>1.374842</td>
      <td>-3.003625</td>
      <td>3.899563</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.messaging.monitoring</td>
      <td>axon-messaging-5.0.0</td>
      <td>0</td>
      <td>0.281048</td>
      <td>-4.147937</td>
      <td>6.729405</td>
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
      <td>org.axonframework.extension.metrics.micrometer</td>
      <td>micrometer</td>
      <td>axon-metrics-micrometer-5.0.0</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[-0.21650634706020355, -0.6495190411806107, 0....</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.extension.metrics.micrometer...</td>
      <td>reservoir</td>
      <td>axon-metrics-micrometer-5.0.0</td>
      <td>0</td>
      <td>0.173182</td>
      <td>[0.0, -1.2990380823612213, 0.0, -0.43301269412...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.infra</td>
      <td>infra</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>0.822416</td>
      <td>[0.21650634706020355, -0.6495190411806107, -1....</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.configuration</td>
      <td>configuration</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>1.374842</td>
      <td>[0.6495190411806107, -1.0825317353010178, 0.43...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.messaging.monitoring</td>
      <td>monitoring</td>
      <td>axon-messaging-5.0.0</td>
      <td>0</td>
      <td>0.281048</td>
      <td>[0.8660253882408142, -1.0825317353010178, 0.43...</td>
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
    ===> Running optimization with exaggeration=12.00, lr=9.42 for 250 iterations...
    Iteration   50, KL divergence -1.1974, 50 iterations in 0.0226 sec
    Iteration  100, KL divergence 1.2309, 50 iterations in 0.0146 sec
    Iteration  150, KL divergence 1.2309, 50 iterations in 0.0142 sec
    Iteration  200, KL divergence 1.2309, 50 iterations in 0.0142 sec
    Iteration  250, KL divergence 1.2309, 50 iterations in 0.0142 sec
       --> Time elapsed: 0.08 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.5444, 50 iterations in 0.0206 sec
    Iteration  100, KL divergence 0.5251, 50 iterations in 0.0188 sec
    Iteration  150, KL divergence 0.5232, 50 iterations in 0.0159 sec
    Iteration  200, KL divergence 0.5234, 50 iterations in 0.0158 sec
    Iteration  250, KL divergence 0.5235, 50 iterations in 0.0158 sec
    Iteration  300, KL divergence 0.5234, 50 iterations in 0.0158 sec


    Iteration  350, KL divergence 0.5237, 50 iterations in 0.0166 sec
    Iteration  400, KL divergence 0.5236, 50 iterations in 0.0162 sec
    Iteration  450, KL divergence 0.5236, 50 iterations in 0.0158 sec
    Iteration  500, KL divergence 0.5236, 50 iterations in 0.0159 sec
       --> Time elapsed: 0.17 seconds



    (113, 2)



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
      <td>org.axonframework.extension.metrics.micrometer</td>
      <td>axon-metrics-micrometer-5.0.0</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-0.663008</td>
      <td>3.067239</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.extension.metrics.micrometer...</td>
      <td>axon-metrics-micrometer-5.0.0</td>
      <td>0</td>
      <td>0.173182</td>
      <td>5.196152</td>
      <td>4.278796</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.infra</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>0.822416</td>
      <td>-10.057174</td>
      <td>-0.258686</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>1.374842</td>
      <td>-6.772098</td>
      <td>-0.562087</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.messaging.monitoring</td>
      <td>axon-messaging-5.0.0</td>
      <td>0</td>
      <td>0.281048</td>
      <td>0.773923</td>
      <td>3.775277</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_23_7.png)
    


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
      <td>org.axonframework.extension.metrics.micrometer</td>
      <td>micrometer</td>
      <td>axon-metrics-micrometer-5.0.0</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[-0.6167477369308472, 0.6386266350746155, 0.77...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.extension.metrics.micrometer...</td>
      <td>reservoir</td>
      <td>axon-metrics-micrometer-5.0.0</td>
      <td>0</td>
      <td>0.173182</td>
      <td>[-0.6470420956611633, 0.8579778075218201, 0.74...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.infra</td>
      <td>infra</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>0.822416</td>
      <td>[-0.3565714657306671, 0.3427692949771881, 0.21...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.configuration</td>
      <td>configuration</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>1.374842</td>
      <td>[-0.30609458684921265, 0.5671186447143555, 0.1...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.messaging.monitoring</td>
      <td>monitoring</td>
      <td>axon-messaging-5.0.0</td>
      <td>0</td>
      <td>0.281048</td>
      <td>[-0.5385095477104187, 0.7670970559120178, 0.61...</td>
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
    ===> Running optimization with exaggeration=12.00, lr=9.42 for 250 iterations...
    Iteration   50, KL divergence -0.4632, 50 iterations in 0.0153 sec
    Iteration  100, KL divergence 1.1699, 50 iterations in 0.0100 sec
    Iteration  150, KL divergence 1.1699, 50 iterations in 0.0099 sec
    Iteration  200, KL divergence 1.1699, 50 iterations in 0.0098 sec
    Iteration  250, KL divergence 1.1699, 50 iterations in 0.0098 sec
       --> Time elapsed: 0.05 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.3125, 50 iterations in 0.0146 sec
    Iteration  100, KL divergence 0.2830, 50 iterations in 0.0166 sec
    Iteration  150, KL divergence 0.2786, 50 iterations in 0.0165 sec
    Iteration  200, KL divergence 0.2724, 50 iterations in 0.0162 sec
    Iteration  250, KL divergence 0.2723, 50 iterations in 0.0161 sec
    Iteration  300, KL divergence 0.2708, 50 iterations in 0.0162 sec
    Iteration  350, KL divergence 0.2698, 50 iterations in 0.0159 sec
    Iteration  400, KL divergence 0.2698, 50 iterations in 0.0160 sec


    Iteration  450, KL divergence 0.2695, 50 iterations in 0.0169 sec
    Iteration  500, KL divergence 0.2696, 50 iterations in 0.0163 sec
       --> Time elapsed: 0.16 seconds



    (113, 2)



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
      <td>org.axonframework.extension.metrics.micrometer</td>
      <td>axon-metrics-micrometer-5.0.0</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-6.844645</td>
      <td>-4.090009</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.extension.metrics.micrometer...</td>
      <td>axon-metrics-micrometer-5.0.0</td>
      <td>0</td>
      <td>0.173182</td>
      <td>-6.941323</td>
      <td>-4.265116</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.infra</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>0.822416</td>
      <td>0.974028</td>
      <td>1.416065</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>1.374842</td>
      <td>-3.210026</td>
      <td>2.546618</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.messaging.monitoring</td>
      <td>axon-messaging-5.0.0</td>
      <td>0</td>
      <td>0.281048</td>
      <td>-6.609096</td>
      <td>-3.714524</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_25_7.png)
    

