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
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>opentelemetry</td>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.08114231377840042, -0.11478951573371887, -0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.io</td>
      <td>io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>[-0.05571554973721504, -0.18395081162452698, 0...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.util</td>
      <td>util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>[-0.35514405369758606, -0.04358514025807381, -...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.lifecycle</td>
      <td>lifecycle</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.258173</td>
      <td>[-0.14412306249141693, 0.10078674554824829, -0...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>0</td>
      <td>0.176990</td>
      <td>[-0.20091867446899414, 0.0885273665189743, -0....</td>
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
    Iteration   50, KL divergence -1.2460, 50 iterations in 0.0143 sec
    Iteration  100, KL divergence 1.1815, 50 iterations in 0.0097 sec
    Iteration  150, KL divergence 1.1815, 50 iterations in 0.0095 sec
    Iteration  200, KL divergence 1.1815, 50 iterations in 0.0096 sec
    Iteration  250, KL divergence 1.1815, 50 iterations in 0.0095 sec
       --> Time elapsed: 0.05 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.2561, 50 iterations in 0.0137 sec
    Iteration  100, KL divergence 0.2241, 50 iterations in 0.0153 sec
    Iteration  150, KL divergence 0.2215, 50 iterations in 0.0154 sec
    Iteration  200, KL divergence 0.2206, 50 iterations in 0.0156 sec
    Iteration  250, KL divergence 0.2194, 50 iterations in 0.0155 sec
    Iteration  300, KL divergence 0.2189, 50 iterations in 0.0159 sec
    Iteration  350, KL divergence 0.2187, 50 iterations in 0.0157 sec


    Iteration  400, KL divergence 0.2181, 50 iterations in 0.0160 sec
    Iteration  450, KL divergence 0.2181, 50 iterations in 0.0159 sec
    Iteration  500, KL divergence 0.2169, 50 iterations in 0.0157 sec
       --> Time elapsed: 0.15 seconds



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
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-1.712712</td>
      <td>1.180456</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>3.362760</td>
      <td>-1.655719</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>-7.445026</td>
      <td>3.540704</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.lifecycle</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.258173</td>
      <td>-6.883256</td>
      <td>3.386342</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>0</td>
      <td>0.176990</td>
      <td>-7.070331</td>
      <td>3.421804</td>
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
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>opentelemetry</td>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.4330126941204071, -0.8660253882408142, 0.43...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.io</td>
      <td>io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>[-1.948557123541832, -0.4330126941204071, 1.29...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.util</td>
      <td>util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>[-0.8660253882408142, -0.6495190411806107, 1.0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.lifecycle</td>
      <td>lifecycle</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.258173</td>
      <td>[-0.6495190411806107, -0.6495190411806107, 0.4...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>0</td>
      <td>0.176990</td>
      <td>[-0.4330126941204071, -0.4330126941204071, 1.7...</td>
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
    Iteration   50, KL divergence -0.6554, 50 iterations in 0.0224 sec
    Iteration  100, KL divergence 1.2290, 50 iterations in 0.0147 sec
    Iteration  150, KL divergence 1.2290, 50 iterations in 0.0143 sec
    Iteration  200, KL divergence 1.2290, 50 iterations in 0.0143 sec
    Iteration  250, KL divergence 1.2290, 50 iterations in 0.0144 sec
       --> Time elapsed: 0.08 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.5417, 50 iterations in 0.0208 sec
    Iteration  100, KL divergence 0.5060, 50 iterations in 0.0185 sec
    Iteration  150, KL divergence 0.4871, 50 iterations in 0.0163 sec
    Iteration  200, KL divergence 0.4820, 50 iterations in 0.0158 sec
    Iteration  250, KL divergence 0.4817, 50 iterations in 0.0156 sec
    Iteration  300, KL divergence 0.4815, 50 iterations in 0.0157 sec


    Iteration  350, KL divergence 0.4810, 50 iterations in 0.0164 sec
    Iteration  400, KL divergence 0.4811, 50 iterations in 0.0155 sec
    Iteration  450, KL divergence 0.4816, 50 iterations in 0.0156 sec
    Iteration  500, KL divergence 0.4819, 50 iterations in 0.0157 sec
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
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-4.545804</td>
      <td>5.140264</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>1.290810</td>
      <td>-5.787939</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>1.000236</td>
      <td>-5.514576</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.lifecycle</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.258173</td>
      <td>6.544285</td>
      <td>-0.176546</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>0</td>
      <td>0.176990</td>
      <td>7.410452</td>
      <td>-2.290524</td>
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
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>opentelemetry</td>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.02516273222863674, -0.3453728258609772, -0....</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.io</td>
      <td>io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>[0.3596240282058716, 0.07079111039638519, -0.0...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.util</td>
      <td>util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>[0.28667640686035156, 0.1430722028017044, -0.0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.lifecycle</td>
      <td>lifecycle</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.258173</td>
      <td>[0.05616411939263344, -0.23123116791248322, 0....</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>0</td>
      <td>0.176990</td>
      <td>[0.1784413605928421, 0.015715302899479866, 0.1...</td>
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
    Iteration   50, KL divergence -0.4299, 50 iterations in 0.0153 sec
    Iteration  100, KL divergence 1.1627, 50 iterations in 0.0099 sec
    Iteration  150, KL divergence 1.1627, 50 iterations in 0.0097 sec
    Iteration  200, KL divergence 1.1627, 50 iterations in 0.0096 sec
    Iteration  250, KL divergence 1.1627, 50 iterations in 0.0096 sec
       --> Time elapsed: 0.05 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.3492, 50 iterations in 0.0143 sec
    Iteration  100, KL divergence 0.3175, 50 iterations in 0.0164 sec
    Iteration  150, KL divergence 0.3150, 50 iterations in 0.0164 sec
    Iteration  200, KL divergence 0.3147, 50 iterations in 0.0159 sec
    Iteration  250, KL divergence 0.3140, 50 iterations in 0.0160 sec
    Iteration  300, KL divergence 0.3133, 50 iterations in 0.0158 sec
    Iteration  350, KL divergence 0.3125, 50 iterations in 0.0157 sec
    Iteration  400, KL divergence 0.3129, 50 iterations in 0.0153 sec


    Iteration  450, KL divergence 0.3127, 50 iterations in 0.0162 sec
    Iteration  500, KL divergence 0.3127, 50 iterations in 0.0156 sec
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
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>1.590130</td>
      <td>-6.650060</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>5.141353</td>
      <td>-3.284831</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>5.366038</td>
      <td>-3.213970</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.lifecycle</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.258173</td>
      <td>3.904261</td>
      <td>-3.869121</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>0</td>
      <td>0.176990</td>
      <td>4.912381</td>
      <td>-3.337144</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_25_7.png)
    

