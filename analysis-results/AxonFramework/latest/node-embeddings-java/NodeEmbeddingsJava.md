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
      <td>org.axonframework.test</td>
      <td>test</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.329631</td>
      <td>[-0.015897266566753387, 0.5035235285758972, -0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>[-0.0310148224234581, 0.5041637420654297, -0.0...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.18910135328769684, 0.498261421918869, -0.01...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>[-0.035025108605623245, 0.599344789981842, -0....</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>[-0.06809912621974945, 0.5486534833908081, -0....</td>
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
    ===> Running optimization with exaggeration=12.00, lr=10.08 for 250 iterations...
    Iteration   50, KL divergence -0.2928, 50 iterations in 0.0144 sec
    Iteration  100, KL divergence 1.2612, 50 iterations in 0.0090 sec
    Iteration  150, KL divergence 1.2612, 50 iterations in 0.0089 sec
    Iteration  200, KL divergence 1.2612, 50 iterations in 0.0091 sec
    Iteration  250, KL divergence 1.2612, 50 iterations in 0.0089 sec
       --> Time elapsed: 0.05 seconds
    ===> Running optimization with exaggeration=1.00, lr=121.00 for 500 iterations...
    Iteration   50, KL divergence 0.1747, 50 iterations in 0.0135 sec
    Iteration  100, KL divergence 0.1603, 50 iterations in 0.0149 sec
    Iteration  150, KL divergence 0.1533, 50 iterations in 0.0147 sec
    Iteration  200, KL divergence 0.1533, 50 iterations in 0.0146 sec
    Iteration  250, KL divergence 0.1529, 50 iterations in 0.0145 sec
    Iteration  300, KL divergence 0.1529, 50 iterations in 0.0146 sec
    Iteration  350, KL divergence 0.1528, 50 iterations in 0.0144 sec
    Iteration  400, KL divergence 0.1529, 50 iterations in 0.0147 sec


    Iteration  450, KL divergence 0.1552, 50 iterations in 0.0155 sec
    Iteration  500, KL divergence 0.1552, 50 iterations in 0.0143 sec
       --> Time elapsed: 0.15 seconds



    (121, 2)



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
      <td>org.axonframework.test</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.329631</td>
      <td>-9.151298</td>
      <td>-1.302200</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>-9.060952</td>
      <td>-1.358357</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-8.741168</td>
      <td>-1.112722</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>-9.318148</td>
      <td>-1.529091</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>-8.171855</td>
      <td>-1.945886</td>
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
      <td>org.axonframework.test</td>
      <td>test</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.329631</td>
      <td>[0.4330126941204071, -1.2990380823612213, -0.8...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>[0.21650634706020355, -1.5155444294214249, -0....</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[-0.6495190411806107, -1.5155444294214249, 0.2...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>[0.4330126941204071, -1.2990380823612213, -0.4...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>[0.21650634706020355, 0.4330126941204071, 0.86...</td>
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
       --> Time elapsed: 0.03 seconds
    ===> Running optimization with exaggeration=12.00, lr=10.08 for 250 iterations...
    Iteration   50, KL divergence -0.3502, 50 iterations in 0.0244 sec
    Iteration  100, KL divergence -2.8526, 50 iterations in 0.0151 sec
    Iteration  150, KL divergence 1.2542, 50 iterations in 0.0145 sec
    Iteration  200, KL divergence 1.2542, 50 iterations in 0.0147 sec
    Iteration  250, KL divergence 1.2542, 50 iterations in 0.0150 sec
       --> Time elapsed: 0.08 seconds
    ===> Running optimization with exaggeration=1.00, lr=121.00 for 500 iterations...
    Iteration   50, KL divergence 0.6783, 50 iterations in 0.0179 sec
    Iteration  100, KL divergence 0.6668, 50 iterations in 0.0157 sec
    Iteration  150, KL divergence 0.6642, 50 iterations in 0.0153 sec
    Iteration  200, KL divergence 0.6615, 50 iterations in 0.0149 sec


    Iteration  250, KL divergence 0.6623, 50 iterations in 0.0157 sec


    Iteration  300, KL divergence 0.6623, 50 iterations in 0.0156 sec
    Iteration  350, KL divergence 0.6624, 50 iterations in 0.0148 sec
    Iteration  400, KL divergence 0.6619, 50 iterations in 0.0146 sec
    Iteration  450, KL divergence 0.6624, 50 iterations in 0.0147 sec
    Iteration  500, KL divergence 0.6625, 50 iterations in 0.0148 sec
       --> Time elapsed: 0.15 seconds



    (121, 2)



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
      <td>org.axonframework.test</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.329631</td>
      <td>3.128144</td>
      <td>6.364717</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>2.643808</td>
      <td>6.849747</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>1.972707</td>
      <td>6.920237</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>3.072437</td>
      <td>6.540251</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>4.922498</td>
      <td>6.800743</td>
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
      <td>org.axonframework.test</td>
      <td>test</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.329631</td>
      <td>[0.4655553698539734, -0.3768097162246704, -0.2...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>[0.3335535526275635, -0.415880411863327, -0.14...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.22560736536979675, -0.3210165798664093, -0....</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>[0.4712684154510498, -0.392704039812088, -0.12...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>[0.5616535544395447, -0.1142037883400917, 0.01...</td>
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
    ===> Running optimization with exaggeration=12.00, lr=10.08 for 250 iterations...
    Iteration   50, KL divergence -1.0052, 50 iterations in 0.0149 sec
    Iteration  100, KL divergence 1.2244, 50 iterations in 0.0094 sec
    Iteration  150, KL divergence 1.2244, 50 iterations in 0.0091 sec
    Iteration  200, KL divergence 1.2244, 50 iterations in 0.0090 sec
    Iteration  250, KL divergence 1.2244, 50 iterations in 0.0090 sec
       --> Time elapsed: 0.05 seconds
    ===> Running optimization with exaggeration=1.00, lr=121.00 for 500 iterations...
    Iteration   50, KL divergence 0.3722, 50 iterations in 0.0144 sec
    Iteration  100, KL divergence 0.3087, 50 iterations in 0.0160 sec
    Iteration  150, KL divergence 0.2996, 50 iterations in 0.0156 sec
    Iteration  200, KL divergence 0.2993, 50 iterations in 0.0153 sec
    Iteration  250, KL divergence 0.2992, 50 iterations in 0.0147 sec
    Iteration  300, KL divergence 0.2994, 50 iterations in 0.0148 sec
    Iteration  350, KL divergence 0.2994, 50 iterations in 0.0149 sec
    Iteration  400, KL divergence 0.2992, 50 iterations in 0.0147 sec
    Iteration  450, KL divergence 0.2994, 50 iterations in 0.0150 sec


    Iteration  500, KL divergence 0.2993, 50 iterations in 0.0160 sec
       --> Time elapsed: 0.15 seconds



    (121, 2)



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
      <td>org.axonframework.test</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.329631</td>
      <td>-9.649423</td>
      <td>-1.885672</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>-9.472886</td>
      <td>-2.176231</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-9.167516</td>
      <td>-2.575255</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>-9.020881</td>
      <td>-2.011688</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>-8.478227</td>
      <td>-1.206023</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_25_7.png)
    

