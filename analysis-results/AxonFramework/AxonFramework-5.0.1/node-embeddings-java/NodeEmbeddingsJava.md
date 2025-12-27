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
      <td>[0.14061221480369568, -0.08217788487672806, -0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common</td>
      <td>common</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>10.756631</td>
      <td>[0.15428410470485687, -0.08416125923395157, 0....</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.io</td>
      <td>io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>[0.16760286688804626, -0.16856589913368225, 0....</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.util</td>
      <td>util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>[-0.32020461559295654, -0.037977006286382675, ...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.caching</td>
      <td>caching</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.0853026807308197, -0.1533559262752533, -0.0...</td>
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
    Iteration   50, KL divergence -0.6912, 50 iterations in 0.0130 sec
    Iteration  100, KL divergence 1.1968, 50 iterations in 0.0085 sec
    Iteration  150, KL divergence 1.1968, 50 iterations in 0.0084 sec
    Iteration  200, KL divergence 1.1968, 50 iterations in 0.0085 sec
    Iteration  250, KL divergence 1.1968, 50 iterations in 0.0085 sec
       --> Time elapsed: 0.05 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.2199, 50 iterations in 0.0126 sec
    Iteration  100, KL divergence 0.1997, 50 iterations in 0.0137 sec
    Iteration  150, KL divergence 0.1958, 50 iterations in 0.0138 sec
    Iteration  200, KL divergence 0.1958, 50 iterations in 0.0135 sec
    Iteration  250, KL divergence 0.1958, 50 iterations in 0.0138 sec
    Iteration  300, KL divergence 0.1958, 50 iterations in 0.0136 sec
    Iteration  350, KL divergence 0.1958, 50 iterations in 0.0137 sec
    Iteration  400, KL divergence 0.1925, 50 iterations in 0.0136 sec
    Iteration  450, KL divergence 0.1928, 50 iterations in 0.0138 sec


    Iteration  500, KL divergence 0.1927, 50 iterations in 0.0145 sec
       --> Time elapsed: 0.14 seconds



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
      <td>-2.552235</td>
      <td>2.110738</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>10.756631</td>
      <td>1.198247</td>
      <td>1.318933</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>4.308250</td>
      <td>0.081449</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>-4.454872</td>
      <td>5.834210</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.caching</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>0.724442</td>
      <td>-0.325138</td>
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
      <td>[0.6495190411806107, 0.0, 0.21650634706020355,...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common</td>
      <td>common</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>10.756631</td>
      <td>[0.8660253882408142, -1.7320507764816284, -1.9...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.io</td>
      <td>io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>[-1.948557123541832, -0.4330126941204071, 1.29...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.util</td>
      <td>util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>[-1.948557123541832, -0.4330126941204071, 1.08...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.caching</td>
      <td>caching</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.6495190411806107, -0.21650634706020355, -0....</td>
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
    Iteration   50, KL divergence -0.7298, 50 iterations in 0.0220 sec
    Iteration  100, KL divergence 1.2289, 50 iterations in 0.0140 sec
    Iteration  150, KL divergence 1.2289, 50 iterations in 0.0136 sec
    Iteration  200, KL divergence 1.2289, 50 iterations in 0.0138 sec
    Iteration  250, KL divergence 1.2289, 50 iterations in 0.0136 sec
       --> Time elapsed: 0.08 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.4866, 50 iterations in 0.0192 sec
    Iteration  100, KL divergence 0.4807, 50 iterations in 0.0140 sec
    Iteration  150, KL divergence 0.4802, 50 iterations in 0.0137 sec
    Iteration  200, KL divergence 0.4806, 50 iterations in 0.0137 sec
    Iteration  250, KL divergence 0.4808, 50 iterations in 0.0136 sec
    Iteration  300, KL divergence 0.4806, 50 iterations in 0.0139 sec
    Iteration  350, KL divergence 0.4807, 50 iterations in 0.0137 sec


    Iteration  400, KL divergence 0.4809, 50 iterations in 0.0144 sec
    Iteration  450, KL divergence 0.4806, 50 iterations in 0.0141 sec
    Iteration  500, KL divergence 0.4808, 50 iterations in 0.0138 sec
       --> Time elapsed: 0.14 seconds



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
      <td>-0.628384</td>
      <td>5.866121</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>10.756631</td>
      <td>5.831044</td>
      <td>4.302659</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>-5.646677</td>
      <td>-1.045768</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>-5.944378</td>
      <td>-2.160707</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.caching</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-3.880894</td>
      <td>0.340884</td>
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
      <td>[-0.21053963899612427, -0.3726460933685303, -0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common</td>
      <td>common</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>10.756631</td>
      <td>[-0.051502522081136703, -0.15689386427402496, ...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.io</td>
      <td>io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>[0.0003798155812546611, 0.14913347363471985, 0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.util</td>
      <td>util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>[-0.14913545548915863, 0.130649596452713, 0.21...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.caching</td>
      <td>caching</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[-0.018165074288845062, 0.08975622057914734, 0...</td>
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
    Iteration   50, KL divergence -0.6342, 50 iterations in 0.0140 sec
    Iteration  100, KL divergence 1.1496, 50 iterations in 0.0088 sec
    Iteration  150, KL divergence 1.1496, 50 iterations in 0.0086 sec
    Iteration  200, KL divergence 1.1496, 50 iterations in 0.0085 sec
    Iteration  250, KL divergence 1.1496, 50 iterations in 0.0085 sec
       --> Time elapsed: 0.05 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.3526, 50 iterations in 0.0132 sec
    Iteration  100, KL divergence 0.3160, 50 iterations in 0.0147 sec
    Iteration  150, KL divergence 0.3092, 50 iterations in 0.0149 sec
    Iteration  200, KL divergence 0.3076, 50 iterations in 0.0147 sec
    Iteration  250, KL divergence 0.3060, 50 iterations in 0.0147 sec
    Iteration  300, KL divergence 0.3056, 50 iterations in 0.0143 sec
    Iteration  350, KL divergence 0.2935, 50 iterations in 0.0144 sec
    Iteration  400, KL divergence 0.2750, 50 iterations in 0.0149 sec
    Iteration  450, KL divergence 0.2750, 50 iterations in 0.0141 sec


    Iteration  500, KL divergence 0.2751, 50 iterations in 0.0145 sec
       --> Time elapsed: 0.14 seconds



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
      <td>5.837092</td>
      <td>3.592862</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>10.756631</td>
      <td>-0.495545</td>
      <td>1.158554</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.io</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.377311</td>
      <td>-0.991850</td>
      <td>-6.674177</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.util</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.265252</td>
      <td>-0.994116</td>
      <td>-6.748003</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.caching</td>
      <td>axon-common-5.0.1</td>
      <td>0</td>
      <td>0.150000</td>
      <td>0.087059</td>
      <td>1.676555</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_25_7.png)
    

