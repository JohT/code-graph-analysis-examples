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
    Iteration   50, KL divergence -0.3668, 50 iterations in 0.0157 sec
    Iteration  100, KL divergence 1.2513, 50 iterations in 0.0102 sec
    Iteration  150, KL divergence 1.2513, 50 iterations in 0.0100 sec
    Iteration  200, KL divergence 1.2513, 50 iterations in 0.0102 sec
    Iteration  250, KL divergence 1.2513, 50 iterations in 0.0101 sec
       --> Time elapsed: 0.06 seconds
    ===> Running optimization with exaggeration=1.00, lr=121.00 for 500 iterations...
    Iteration   50, KL divergence 0.1920, 50 iterations in 0.0147 sec
    Iteration  100, KL divergence 0.1611, 50 iterations in 0.0165 sec
    Iteration  150, KL divergence 0.1521, 50 iterations in 0.0167 sec
    Iteration  200, KL divergence 0.1515, 50 iterations in 0.0162 sec
    Iteration  250, KL divergence 0.1516, 50 iterations in 0.0162 sec
    Iteration  300, KL divergence 0.1514, 50 iterations in 0.0161 sec
    Iteration  350, KL divergence 0.1514, 50 iterations in 0.0163 sec


    Iteration  400, KL divergence 0.1538, 50 iterations in 0.0172 sec
    Iteration  450, KL divergence 0.1538, 50 iterations in 0.0161 sec
    Iteration  500, KL divergence 0.1538, 50 iterations in 0.0160 sec
       --> Time elapsed: 0.16 seconds



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
      <td>-6.790619</td>
      <td>-6.390369</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>-6.796062</td>
      <td>-6.280772</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-6.423352</td>
      <td>-6.099405</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>-7.085774</td>
      <td>-6.435797</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>-7.021885</td>
      <td>-5.268923</td>
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
    Iteration   50, KL divergence -0.2211, 50 iterations in 0.0246 sec
    Iteration  100, KL divergence 1.2949, 50 iterations in 0.0154 sec
    Iteration  150, KL divergence 1.2949, 50 iterations in 0.0149 sec
    Iteration  200, KL divergence 1.2949, 50 iterations in 0.0150 sec
    Iteration  250, KL divergence 1.2949, 50 iterations in 0.0154 sec
       --> Time elapsed: 0.09 seconds
    ===> Running optimization with exaggeration=1.00, lr=121.00 for 500 iterations...
    Iteration   50, KL divergence 0.6447, 50 iterations in 0.0223 sec
    Iteration  100, KL divergence 0.6170, 50 iterations in 0.0172 sec
    Iteration  150, KL divergence 0.6148, 50 iterations in 0.0166 sec
    Iteration  200, KL divergence 0.6143, 50 iterations in 0.0164 sec
    Iteration  250, KL divergence 0.6136, 50 iterations in 0.0163 sec


    Iteration  300, KL divergence 0.6136, 50 iterations in 0.0172 sec
    Iteration  350, KL divergence 0.6132, 50 iterations in 0.0163 sec
    Iteration  400, KL divergence 0.6120, 50 iterations in 0.0165 sec
    Iteration  450, KL divergence 0.6118, 50 iterations in 0.0162 sec
    Iteration  500, KL divergence 0.6110, 50 iterations in 0.0163 sec
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
      <td>-7.551160</td>
      <td>-0.068745</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>-8.297125</td>
      <td>-0.017871</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-6.757870</td>
      <td>0.691759</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>-7.640882</td>
      <td>-0.030277</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>-8.614611</td>
      <td>1.452427</td>
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
      <td>[0.37680864334106445, -0.30120500922203064, -0...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>[0.4226599931716919, -0.28219074010849, 0.0128...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>[0.1193510890007019, -0.2583690285682678, 0.01...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>[0.3798343241214752, -0.2737148106098175, 0.03...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>[0.42955830693244934, -0.08157213032245636, 0....</td>
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
    Iteration   50, KL divergence -0.5309, 50 iterations in 0.0172 sec
    Iteration  100, KL divergence 1.2216, 50 iterations in 0.0105 sec
    Iteration  150, KL divergence 1.2216, 50 iterations in 0.0102 sec
    Iteration  200, KL divergence 1.2216, 50 iterations in 0.0102 sec
    Iteration  250, KL divergence 1.2216, 50 iterations in 0.0102 sec
       --> Time elapsed: 0.06 seconds
    ===> Running optimization with exaggeration=1.00, lr=121.00 for 500 iterations...
    Iteration   50, KL divergence 0.3432, 50 iterations in 0.0158 sec
    Iteration  100, KL divergence 0.3138, 50 iterations in 0.0172 sec
    Iteration  150, KL divergence 0.3025, 50 iterations in 0.0179 sec
    Iteration  200, KL divergence 0.2988, 50 iterations in 0.0175 sec
    Iteration  250, KL divergence 0.2964, 50 iterations in 0.0173 sec
    Iteration  300, KL divergence 0.2958, 50 iterations in 0.0171 sec
    Iteration  350, KL divergence 0.2884, 50 iterations in 0.0172 sec


    Iteration  400, KL divergence 0.2823, 50 iterations in 0.0177 sec
    Iteration  450, KL divergence 0.2810, 50 iterations in 0.0171 sec
    Iteration  500, KL divergence 0.2812, 50 iterations in 0.0166 sec
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
      <td>-4.583256</td>
      <td>9.271016</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.test.matchers</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.220506</td>
      <td>-4.467828</td>
      <td>8.794377</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.test.aggregate</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.150000</td>
      <td>-4.433488</td>
      <td>7.860415</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.test.deadline</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.170496</td>
      <td>-4.200623</td>
      <td>8.607220</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.test.utils</td>
      <td>axon-test-4.12.2</td>
      <td>0</td>
      <td>0.156071</td>
      <td>-3.188521</td>
      <td>8.567573</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_25_7.png)
    

