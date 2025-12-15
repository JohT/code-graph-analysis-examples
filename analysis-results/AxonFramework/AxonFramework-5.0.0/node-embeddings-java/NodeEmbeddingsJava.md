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
      <td>org.axonframework.modelling</td>
      <td>modelling</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.225594</td>
      <td>[-0.18517041206359863, -0.19453135132789612, -...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.modelling.annotation</td>
      <td>annotation</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.167480</td>
      <td>[-0.25651735067367554, -0.3252694606781006, -0...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.modelling.configuration</td>
      <td>configuration</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.171795</td>
      <td>[-0.28743916749954224, -0.10028918087482452, -...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.repository</td>
      <td>repository</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.277381</td>
      <td>[-0.25944310426712036, -0.27486568689346313, -...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.infra</td>
      <td>infra</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>0.822416</td>
      <td>[-0.14152909815311432, -0.22061559557914734, -...</td>
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
    Iteration   50, KL divergence -0.0873, 50 iterations in 0.0145 sec
    Iteration  100, KL divergence 1.1747, 50 iterations in 0.0097 sec
    Iteration  150, KL divergence 1.1747, 50 iterations in 0.0097 sec
    Iteration  200, KL divergence 1.1747, 50 iterations in 0.0096 sec
    Iteration  250, KL divergence 1.1747, 50 iterations in 0.0095 sec
       --> Time elapsed: 0.05 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.2143, 50 iterations in 0.0141 sec
    Iteration  100, KL divergence 0.1896, 50 iterations in 0.0155 sec
    Iteration  150, KL divergence 0.1879, 50 iterations in 0.0157 sec
    Iteration  200, KL divergence 0.1843, 50 iterations in 0.0156 sec
    Iteration  250, KL divergence 0.1867, 50 iterations in 0.0157 sec
    Iteration  300, KL divergence 0.1871, 50 iterations in 0.0154 sec
    Iteration  350, KL divergence 0.1875, 50 iterations in 0.0154 sec


    Iteration  400, KL divergence 0.1869, 50 iterations in 0.0163 sec
    Iteration  450, KL divergence 0.1871, 50 iterations in 0.0157 sec
    Iteration  500, KL divergence 0.1868, 50 iterations in 0.0157 sec
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
      <td>org.axonframework.modelling</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.225594</td>
      <td>-2.994593</td>
      <td>-4.164392</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.modelling.annotation</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.167480</td>
      <td>-3.043135</td>
      <td>-3.055810</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.modelling.configuration</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.171795</td>
      <td>1.332320</td>
      <td>-3.367482</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.repository</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.277381</td>
      <td>-1.932583</td>
      <td>-3.743586</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.infra</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>0.822416</td>
      <td>-0.845201</td>
      <td>-1.291120</td>
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
      <td>org.axonframework.modelling</td>
      <td>modelling</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.225594</td>
      <td>[0.4330126941204071, -1.5155444294214249, 0.21...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.modelling.annotation</td>
      <td>annotation</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.167480</td>
      <td>[0.6495190411806107, -0.6495190411806107, -0.6...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.modelling.configuration</td>
      <td>configuration</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.171795</td>
      <td>[-0.21650634706020355, -0.4330126941204071, -0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.repository</td>
      <td>repository</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.277381</td>
      <td>[0.0, -2.5980761647224426, -0.6495190411806107...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.infra</td>
      <td>infra</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>0.822416</td>
      <td>[-0.21650634706020355, -1.948557123541832, -2....</td>
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
    Iteration   50, KL divergence -0.2482, 50 iterations in 0.0229 sec
    Iteration  100, KL divergence 1.1999, 50 iterations in 0.0151 sec
    Iteration  150, KL divergence 1.1999, 50 iterations in 0.0144 sec
    Iteration  200, KL divergence 1.1999, 50 iterations in 0.0145 sec
    Iteration  250, KL divergence 1.1999, 50 iterations in 0.0144 sec
       --> Time elapsed: 0.08 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.5786, 50 iterations in 0.0221 sec
    Iteration  100, KL divergence 0.5447, 50 iterations in 0.0180 sec
    Iteration  150, KL divergence 0.5370, 50 iterations in 0.0159 sec
    Iteration  200, KL divergence 0.5193, 50 iterations in 0.0159 sec
    Iteration  250, KL divergence 0.5032, 50 iterations in 0.0157 sec
    Iteration  300, KL divergence 0.5021, 50 iterations in 0.0157 sec


    Iteration  350, KL divergence 0.5020, 50 iterations in 0.0161 sec
    Iteration  400, KL divergence 0.5021, 50 iterations in 0.0156 sec
    Iteration  450, KL divergence 0.5018, 50 iterations in 0.0156 sec
    Iteration  500, KL divergence 0.4929, 50 iterations in 0.0160 sec
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
      <td>org.axonframework.modelling</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.225594</td>
      <td>-1.984251</td>
      <td>-3.540982</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.modelling.annotation</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.167480</td>
      <td>-1.442872</td>
      <td>-2.399408</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.modelling.configuration</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.171795</td>
      <td>-5.314712</td>
      <td>4.591742</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.repository</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.277381</td>
      <td>-0.213674</td>
      <td>-3.971510</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.infra</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>0.822416</td>
      <td>-5.799531</td>
      <td>-5.083165</td>
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
      <td>org.axonframework.modelling</td>
      <td>modelling</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.225594</td>
      <td>[0.340716689825058, -0.7679421901702881, -0.11...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.modelling.annotation</td>
      <td>annotation</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.167480</td>
      <td>[0.3664795458316803, -0.7054729461669922, -0.1...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.modelling.configuration</td>
      <td>configuration</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.171795</td>
      <td>[0.09089288860559464, -0.8119312524795532, 0.0...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.repository</td>
      <td>repository</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.277381</td>
      <td>[0.2791661024093628, -0.6690201163291931, -0.1...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.infra</td>
      <td>infra</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>0.822416</td>
      <td>[-0.018120750784873962, -0.4988015294075012, 0...</td>
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
    Iteration   50, KL divergence -0.9456, 50 iterations in 0.0153 sec
    Iteration  100, KL divergence -2.4894, 50 iterations in 0.0101 sec
    Iteration  150, KL divergence -2.4894, 50 iterations in 0.0099 sec
    Iteration  200, KL divergence -2.4894, 50 iterations in 0.0099 sec
    Iteration  250, KL divergence -2.8934, 50 iterations in 0.0098 sec
       --> Time elapsed: 0.06 seconds
    ===> Running optimization with exaggeration=1.00, lr=113.00 for 500 iterations...
    Iteration   50, KL divergence 0.3246, 50 iterations in 0.0155 sec
    Iteration  100, KL divergence 0.2678, 50 iterations in 0.0167 sec
    Iteration  150, KL divergence 0.2569, 50 iterations in 0.0163 sec
    Iteration  200, KL divergence 0.2561, 50 iterations in 0.0157 sec
    Iteration  250, KL divergence 0.2565, 50 iterations in 0.0157 sec
    Iteration  300, KL divergence 0.2565, 50 iterations in 0.0157 sec
    Iteration  350, KL divergence 0.2565, 50 iterations in 0.0157 sec
    Iteration  400, KL divergence 0.2565, 50 iterations in 0.0160 sec


    Iteration  450, KL divergence 0.2565, 50 iterations in 0.0166 sec
    Iteration  500, KL divergence 0.2564, 50 iterations in 0.0164 sec
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
      <td>org.axonframework.modelling</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.225594</td>
      <td>-4.168436</td>
      <td>-3.421235</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.modelling.annotation</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.167480</td>
      <td>-3.911342</td>
      <td>-3.566050</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.modelling.configuration</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.171795</td>
      <td>-4.070087</td>
      <td>-0.916247</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.modelling.repository</td>
      <td>axon-modelling-5.0.0</td>
      <td>0</td>
      <td>0.277381</td>
      <td>-4.276452</td>
      <td>-2.831575</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.infra</td>
      <td>axon-common-5.0.0</td>
      <td>0</td>
      <td>0.822416</td>
      <td>0.205060</td>
      <td>-1.736481</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsJava_files/NodeEmbeddingsJava_25_7.png)
    

