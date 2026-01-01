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
      <td>[0.1337575763463974, 0.1442030668258667, 0.205...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.io</td>
      <td>io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>[0.20984505116939545, 0.08760502934455872, -0....</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.util</td>
      <td>util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>[-0.10188078135251999, 0.11513500660657883, 0....</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.lifecycle</td>
      <td>lifecycle</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.258173</td>
      <td>[0.0944896712899208, 0.22446702420711517, 0.14...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>0</td>
      <td>0.176990</td>
      <td>[0.0869443267583847, 0.268654465675354, 0.1593...</td>
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
    Iteration   50, KL divergence -1.3678, 50 iterations in 0.0147 sec
    Iteration  100, KL divergence 1.1643, 50 iterations in 0.0098 sec
    Iteration  150, KL divergence 1.1643, 50 iterations in 0.0096 sec
    Iteration  200, KL divergence 1.1643, 50 iterations in 0.0096 sec
    Iteration  250, KL divergence 1.1643, 50 iterations in 0.0096 sec
       --> Time elapsed: 0.05 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.2173, 50 iterations in 0.0141 sec
    Iteration  100, KL divergence 0.1824, 50 iterations in 0.0153 sec
    Iteration  150, KL divergence 0.1705, 50 iterations in 0.0155 sec
    Iteration  200, KL divergence 0.1693, 50 iterations in 0.0155 sec
    Iteration  250, KL divergence 0.1697, 50 iterations in 0.0157 sec
    Iteration  300, KL divergence 0.1695, 50 iterations in 0.0157 sec
    Iteration  350, KL divergence 0.1721, 50 iterations in 0.0156 sec


    Iteration  400, KL divergence 0.1719, 50 iterations in 0.0161 sec
    Iteration  450, KL divergence 0.1721, 50 iterations in 0.0157 sec
    Iteration  500, KL divergence 0.1721, 50 iterations in 0.0154 sec
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
      <td>-2.161232</td>
      <td>1.999413</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>2.729018</td>
      <td>7.252400</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>-5.682568</td>
      <td>3.985398</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.lifecycle</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.258173</td>
      <td>-5.148649</td>
      <td>3.635585</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>0</td>
      <td>0.176990</td>
      <td>-5.306196</td>
      <td>3.749065</td>
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
      <td>[-0.6495190411806107, 0.8660253882408142, -1.0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.io</td>
      <td>io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>[-0.6495190411806107, 0.4330126941204071, 0.43...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.util</td>
      <td>util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>[0.21650634706020355, 0.21650634706020355, 0.4...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.lifecycle</td>
      <td>lifecycle</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.258173</td>
      <td>[-0.8660253882408142, 0.4330126941204071, -0.2...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>0</td>
      <td>0.176990</td>
      <td>[0.4330126941204071, -0.21650634706020355, 0.2...</td>
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
    Iteration   50, KL divergence -0.4010, 50 iterations in 0.0231 sec
    Iteration  100, KL divergence -2.8021, 50 iterations in 0.0150 sec
    Iteration  150, KL divergence 1.2366, 50 iterations in 0.0143 sec
    Iteration  200, KL divergence 1.2366, 50 iterations in 0.0142 sec
    Iteration  250, KL divergence 1.2366, 50 iterations in 0.0141 sec
       --> Time elapsed: 0.08 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.6061, 50 iterations in 0.0206 sec
    Iteration  100, KL divergence 0.5392, 50 iterations in 0.0186 sec
    Iteration  150, KL divergence 0.5337, 50 iterations in 0.0157 sec
    Iteration  200, KL divergence 0.5340, 50 iterations in 0.0155 sec
    Iteration  250, KL divergence 0.5300, 50 iterations in 0.0157 sec
    Iteration  300, KL divergence 0.5302, 50 iterations in 0.0159 sec


    Iteration  350, KL divergence 0.5276, 50 iterations in 0.0165 sec
    Iteration  400, KL divergence 0.5268, 50 iterations in 0.0159 sec
    Iteration  450, KL divergence 0.5272, 50 iterations in 0.0158 sec
    Iteration  500, KL divergence 0.5275, 50 iterations in 0.0158 sec
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
      <td>-5.144702</td>
      <td>4.578728</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>-7.816902</td>
      <td>2.696225</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>-2.760308</td>
      <td>-3.193230</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.lifecycle</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.258173</td>
      <td>-3.869910</td>
      <td>-4.290168</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>0</td>
      <td>0.176990</td>
      <td>-3.402879</td>
      <td>-3.936032</td>
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
      <td>[-0.11319497972726822, -0.20911745727062225, -...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.io</td>
      <td>io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>[0.3755985200405121, -0.4150378704071045, -0.2...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.util</td>
      <td>util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>[0.26531553268432617, -0.41420435905456543, -0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.lifecycle</td>
      <td>lifecycle</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.258173</td>
      <td>[0.22852371633052826, -0.5454846024513245, -0....</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>0</td>
      <td>0.176990</td>
      <td>[0.3232279419898987, -0.386302649974823, -0.27...</td>
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
    Iteration   50, KL divergence -0.5288, 50 iterations in 0.0160 sec
    Iteration  100, KL divergence 1.1554, 50 iterations in 0.0101 sec
    Iteration  150, KL divergence 1.1554, 50 iterations in 0.0096 sec
    Iteration  200, KL divergence 1.1554, 50 iterations in 0.0096 sec
    Iteration  250, KL divergence 1.1554, 50 iterations in 0.0096 sec
       --> Time elapsed: 0.06 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.3313, 50 iterations in 0.0145 sec
    Iteration  100, KL divergence 0.3109, 50 iterations in 0.0162 sec
    Iteration  150, KL divergence 0.3076, 50 iterations in 0.0167 sec
    Iteration  200, KL divergence 0.3048, 50 iterations in 0.0174 sec
    Iteration  250, KL divergence 0.3050, 50 iterations in 0.0157 sec
    Iteration  300, KL divergence 0.3051, 50 iterations in 0.0154 sec
    Iteration  350, KL divergence 0.3049, 50 iterations in 0.0153 sec
    Iteration  400, KL divergence 0.3049, 50 iterations in 0.0155 sec


    Iteration  450, KL divergence 0.3050, 50 iterations in 0.0163 sec
    Iteration  500, KL divergence 0.3050, 50 iterations in 0.0156 sec
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
      <td>-4.907336</td>
      <td>-3.676782</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>1.971036</td>
      <td>6.036171</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>2.019244</td>
      <td>6.208951</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.lifecycle</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.258173</td>
      <td>2.822232</td>
      <td>4.860547</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>0</td>
      <td>0.176990</td>
      <td>2.067661</td>
      <td>5.984243</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_25_7.png)
    

