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
      <td>[0.14914719760417938, 0.5048106908798218, -0.0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>[0.13395258784294128, 0.5042384266853333, -0.0...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.3626928925514221, 0.4858619272708893, -0.00...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>[0.1529412567615509, 0.6055339574813843, -0.02...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>[0.1485750675201416, 0.5554510951042175, -0.11...</td>
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
    Iteration   50, KL divergence -0.1950, 50 iterations in 0.0159 sec
    Iteration  100, KL divergence 1.2513, 50 iterations in 0.0104 sec
    Iteration  150, KL divergence 1.2513, 50 iterations in 0.0103 sec
    Iteration  200, KL divergence 1.2513, 50 iterations in 0.0102 sec
    Iteration  250, KL divergence 1.2513, 50 iterations in 0.0102 sec
       --> Time elapsed: 0.06 seconds
    ===> Running optimization with exaggeration=1.00, lr=121.00 for 500 iterations...
    Iteration   50, KL divergence 0.2264, 50 iterations in 0.0151 sec
    Iteration  100, KL divergence 0.1783, 50 iterations in 0.0166 sec
    Iteration  150, KL divergence 0.1677, 50 iterations in 0.0169 sec
    Iteration  200, KL divergence 0.1682, 50 iterations in 0.0166 sec
    Iteration  250, KL divergence 0.1680, 50 iterations in 0.0165 sec
    Iteration  300, KL divergence 0.1679, 50 iterations in 0.0168 sec
    Iteration  350, KL divergence 0.1681, 50 iterations in 0.0168 sec


    Iteration  400, KL divergence 0.1681, 50 iterations in 0.0176 sec
    Iteration  450, KL divergence 0.1681, 50 iterations in 0.0168 sec
    Iteration  500, KL divergence 0.1682, 50 iterations in 0.0167 sec
       --> Time elapsed: 0.17 seconds



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
      <td>-5.199181</td>
      <td>6.856988</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>-5.193027</td>
      <td>6.744990</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-4.829437</td>
      <td>6.568939</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>-5.521690</td>
      <td>6.875663</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>-5.348737</td>
      <td>5.704686</td>
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
      <td>[0.0, -1.7320507764816284, -0.4330126941204071...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>[0.6495190411806107, -2.1650634706020355, -1.0...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.6495190411806107, -1.948557123541832, 0.433...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>[0.0, -2.1650634706020355, 0.0, -1.08253173530...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>[0.8660253882408142, -1.5155444294214249, 0.86...</td>
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
    Iteration   50, KL divergence -0.2624, 50 iterations in 0.0246 sec
    Iteration  100, KL divergence 1.2949, 50 iterations in 0.0155 sec
    Iteration  150, KL divergence 1.2949, 50 iterations in 0.0151 sec
    Iteration  200, KL divergence 1.2949, 50 iterations in 0.0151 sec
    Iteration  250, KL divergence 1.2949, 50 iterations in 0.0196 sec
       --> Time elapsed: 0.09 seconds
    ===> Running optimization with exaggeration=1.00, lr=121.00 for 500 iterations...
    Iteration   50, KL divergence 0.6610, 50 iterations in 0.0212 sec
    Iteration  100, KL divergence 0.6382, 50 iterations in 0.0171 sec
    Iteration  150, KL divergence 0.6353, 50 iterations in 0.0165 sec
    Iteration  200, KL divergence 0.6317, 50 iterations in 0.0168 sec
    Iteration  250, KL divergence 0.6287, 50 iterations in 0.0170 sec


    Iteration  300, KL divergence 0.6282, 50 iterations in 0.0170 sec
    Iteration  350, KL divergence 0.6259, 50 iterations in 0.0170 sec
    Iteration  400, KL divergence 0.6229, 50 iterations in 0.0167 sec
    Iteration  450, KL divergence 0.6224, 50 iterations in 0.0163 sec
    Iteration  500, KL divergence 0.6226, 50 iterations in 0.0163 sec
       --> Time elapsed: 0.17 seconds



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
      <td>-6.597028</td>
      <td>3.530629</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>-7.376830</td>
      <td>3.527225</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-6.598839</td>
      <td>2.476355</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>-6.878499</td>
      <td>3.281628</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>-6.784871</td>
      <td>5.106137</td>
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
      <td>org.axonframework.test</td>
      <td>test</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.329631</td>
      <td>[0.023808220401406288, -0.178813174366951, -0....</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>[-0.11378388851881027, -0.1553647369146347, 0....</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[-0.21312229335308075, -0.1673550009727478, -0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>[-0.09809263050556183, -0.08952255547046661, -...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>[0.008563043549656868, -0.0011804066598415375,...</td>
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
    Iteration   50, KL divergence -0.7753, 50 iterations in 0.0166 sec
    Iteration  100, KL divergence 1.2279, 50 iterations in 0.0104 sec
    Iteration  150, KL divergence 1.2279, 50 iterations in 0.0103 sec
    Iteration  200, KL divergence 1.2279, 50 iterations in 0.0105 sec
    Iteration  250, KL divergence 1.2279, 50 iterations in 0.0103 sec
       --> Time elapsed: 0.06 seconds
    ===> Running optimization with exaggeration=1.00, lr=121.00 for 500 iterations...
    Iteration   50, KL divergence 0.3536, 50 iterations in 0.0154 sec
    Iteration  100, KL divergence 0.3213, 50 iterations in 0.0172 sec
    Iteration  150, KL divergence 0.3171, 50 iterations in 0.0171 sec
    Iteration  200, KL divergence 0.3148, 50 iterations in 0.0171 sec
    Iteration  250, KL divergence 0.3145, 50 iterations in 0.0169 sec
    Iteration  300, KL divergence 0.3144, 50 iterations in 0.0169 sec
    Iteration  350, KL divergence 0.3143, 50 iterations in 0.0168 sec


    Iteration  400, KL divergence 0.3017, 50 iterations in 0.0176 sec


    Iteration  450, KL divergence 0.3004, 50 iterations in 0.0175 sec
    Iteration  500, KL divergence 0.3003, 50 iterations in 0.0170 sec
       --> Time elapsed: 0.17 seconds



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
      <td>9.360025</td>
      <td>1.885303</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>9.359876</td>
      <td>1.486573</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>8.434526</td>
      <td>1.385806</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>9.125416</td>
      <td>2.097738</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>8.373916</td>
      <td>2.815701</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_25_8.png)
    

