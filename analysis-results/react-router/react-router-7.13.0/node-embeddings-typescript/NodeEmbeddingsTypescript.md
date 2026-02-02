# Node Embeddings for TypeScript

This notebook demonstrates different methods for node embeddings and how to further reduce their dimensionality to be able to visualize them in a 2D plot. 

Node embeddings are essentially an array of floating point numbers (length = embedding dimension) that can be used as "features" in machine learning. These numbers approximate the relationship and similarity information of each node and can also be seen as a way to encode the topology of the graph.

## Considerations

Due to dimensionality reduction some information gets lost, especially when visualizing node embeddings in two dimensions. Nevertheless, it helps to get an intuition on what node embeddings are and how much of the similarity and neighborhood information is retained. The latter can be observed by how well nodes of the same color and therefore same community are placed together and how much bigger nodes with a high centrality score influence them. 

If the visualization doesn't show a somehow clear separation between the communities (colors) here are some ideas for tuning: 
- Clean the data, e.g. filter out very few nodes with extremely high degree that aren't actually that important
- Try directed vs. undirected projections
- Tune the embedding algorithm, e.g. use a higher dimensionality
- Tune UMAP that is used to reduce the node embeddings dimension to two dimensions for visualization. 

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
- [UMAP](https://umap-learn.readthedocs.io/en/latest)
- [AttributeError: 'list' object has no attribute 'shape'](https://bobbyhadz.com/blog/python-attributeerror-list-object-has-no-attribute-shape)
- [Fast Random Projection (neo4j)](https://neo4j.com/docs/graph-data-science/current/machine-learning/node-embeddings/fastrp)
- [HashGNN (neo4j)](https://neo4j.com/docs/graph-data-science/2.6/machine-learning/node-embeddings/hashgnn)
- [node2vec (neo4j)](https://neo4j.com/docs/graph-data-science/current/machine-learning/node-embeddings/node2vec) computes a vector representation of a node based on second order random walks in the graph. 
- [Complete guide to understanding Node2Vec algorithm](https://towardsdatascience.com/complete-guide-to-understanding-node2vec-algorithm-4e9a35e5d147)





    The numpy version is: 1.26.4
    The pandas version is: 2.2.3
    The matplotlib version is: 3.10.8
    The sklearn version is: 1.6.1
    The UMAP version is: 0.5.9.post2






## 1. Typescript Modules

### 1.1 Create Dependency Graph Projection for TypeScript Modules

The projection and related common parameters are shared across all embedding algorithms below.


<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>nodeCount</th>
      <th>relationshipCount</th>
      <th>density</th>
      <th>sizeInBytes</th>
      <th>degreeDistribution.min</th>
      <th>degreeDistribution.mean</th>
      <th>degreeDistribution.max</th>
      <th>degreeDistribution.p50</th>
      <th>degreeDistribution.p75</th>
      <th>degreeDistribution.p90</th>
      <th>degreeDistribution.p95</th>
      <th>degreeDistribution.p99</th>
      <th>degreeDistribution.p999</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>129</td>
      <td>680</td>
      <td>0.041182</td>
      <td>2597818</td>
      <td>0</td>
      <td>5.271318</td>
      <td>60</td>
      <td>3</td>
      <td>6</td>
      <td>11</td>
      <td>15</td>
      <td>27</td>
      <td>60</td>
    </tr>
  </tbody>
</table>
</div>


### 1.2 Generate Node Embeddings for Typescript Modules using Fast Random Projection (Fast RP)

[Fast Random Projection](https://neo4j.com/docs/graph-data-science/current/machine-learning/node-embeddings/fastrp) is used to reduce the dimensionality of the node feature space while preserving most of the distance information. Nodes with similar neighborhood result in node embedding with similar vectors.

**👉 Hint:** To skip existing node embeddings and always calculate them based on the parameters below edit `Node_Embeddings_0a_Query_Calculated` so that it won't return any results.

    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownLabelWarning} {category: UNRECOGNIZED} {title: The provided label is not in the database.} {description: One of the labels in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing label name is: Java)} {position: line: 7, column: 27, offset: 572} for query: '// Query already calculated and written node embeddings on nodes with label in parameter $dependencies_projection_node including a communityId and centrality. Variables: dependencies_projection_node, dependencies_projection_write_property. Requires "Add_file_name and_extension.cypher".\n \n  MATCH (codeUnit)\n  WHERE $dependencies_projection_node IN LABELS(codeUnit)\n    AND codeUnit[$dependencies_projection_write_property] IS NOT NULL\n    // AND codeUnit.notExistingToForceRecalculation IS NOT NULL // uncomment this line to force recalculation\n OPTIONAL MATCH (artifact:Java:Artifact)-[:CONTAINS]->(codeUnit)\n    WITH *, artifact.name AS artifactName\n OPTIONAL MATCH (projectRoot:Directory)<-[:HAS_ROOT]-(proj:TS:Project)-[:CONTAINS]->(codeUnit)\n    WITH *, last(split(projectRoot.absoluteFileName, \'/\')) AS projectName   \n  RETURN DISTINCT \n         coalesce(codeUnit.fqn, codeUnit.globalFqn, codeUnit.fileName, codeUnit.signature, codeUnit.name) AS codeUnitName\n        ,codeUnit.name                AS shortCodeUnitName\n        ,coalesce(artifactName, projectName)                                                              AS projectName\n        ,coalesce(codeUnit.communityLeidenId, 0)           AS communityId\n        ,coalesce(codeUnit.centralityPageRank, 0.01)       AS centrality\n        ,codeUnit[$dependencies_projection_write_property] AS embedding\n   ORDER BY communityId'


    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownPropertyKeyWarning} {category: UNRECOGNIZED} {title: The provided property key is not in the database} {description: One of the property names in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing property name is: signature)} {position: line: 12, column: 81, offset: 924} for query: '// Query already calculated and written node embeddings on nodes with label in parameter $dependencies_projection_node including a communityId and centrality. Variables: dependencies_projection_node, dependencies_projection_write_property. Requires "Add_file_name and_extension.cypher".\n \n  MATCH (codeUnit)\n  WHERE $dependencies_projection_node IN LABELS(codeUnit)\n    AND codeUnit[$dependencies_projection_write_property] IS NOT NULL\n    // AND codeUnit.notExistingToForceRecalculation IS NOT NULL // uncomment this line to force recalculation\n OPTIONAL MATCH (artifact:Java:Artifact)-[:CONTAINS]->(codeUnit)\n    WITH *, artifact.name AS artifactName\n OPTIONAL MATCH (projectRoot:Directory)<-[:HAS_ROOT]-(proj:TS:Project)-[:CONTAINS]->(codeUnit)\n    WITH *, last(split(projectRoot.absoluteFileName, \'/\')) AS projectName   \n  RETURN DISTINCT \n         coalesce(codeUnit.fqn, codeUnit.globalFqn, codeUnit.fileName, codeUnit.signature, codeUnit.name) AS codeUnitName\n        ,codeUnit.name                AS shortCodeUnitName\n        ,coalesce(artifactName, projectName)                                                              AS projectName\n        ,coalesce(codeUnit.communityLeidenId, 0)           AS communityId\n        ,coalesce(codeUnit.centralityPageRank, 0.01)       AS centrality\n        ,codeUnit[$dependencies_projection_write_property] AS embedding\n   ORDER BY communityId'


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
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>config</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>1.705838</td>
      <td>[-0.5952500700950623, -0.3340594470500946, 0.1...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>detectPackageManager</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>0.188886</td>
      <td>[-0.6000653505325317, -0.32334285974502563, 0....</td>
    </tr>
    <tr>
      <th>2</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>config</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>2.129389</td>
      <td>[-0.5498749613761902, -0.38851770758628845, 0....</td>
    </tr>
    <tr>
      <th>3</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>context</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>0.180345</td>
      <td>[-0.3691451847553253, -0.6460049152374268, 0.3...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>generate</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>0.277201</td>
      <td>[-0.10859015583992004, -0.2827555537223816, -0...</td>
    </tr>
  </tbody>
</table>
</div>


### 1.3 Dimensionality reduction with Uniform Manifold Approximation and Projection (UMAP)

This step takes the original node embeddings in their high dimensionality, e.g. 32 floating point numbers, and reduces them into a two dimensional array for visualization. For more details look up the function  "prepare_node_embeddings_for_2d_visualization".

**About UMAP:**

> The embedding is found by searching for a low dimensional projection of the data that has the closest possible equivalent fuzzy topological structure.

(see https://umap-learn.readthedocs.io)

### 1.4 Plot the node embeddings reduced to two dimensions for Typescript


    
![png](NodeEmbeddingsTypescript_files/NodeEmbeddingsTypescript_30_0.png)
    


### 1.5 Node Embeddings for Typescript Modules using HashGNN

[HashGNN](https://neo4j.com/docs/graph-data-science/2.6/machine-learning/node-embeddings/hashgnn) resembles Graph Neural Networks (GNN) but does not include a model or require training. It combines ideas of GNNs and fast randomized algorithms. For more details see [HashGNN](https://neo4j.com/docs/graph-data-science/2.6/machine-learning/node-embeddings/hashgnn). Here, the latter 3 steps are combined into one for HashGNN.

    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownLabelWarning} {category: UNRECOGNIZED} {title: The provided label is not in the database.} {description: One of the labels in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing label name is: Java)} {position: line: 7, column: 27, offset: 572} for query: '// Query already calculated and written node embeddings on nodes with label in parameter $dependencies_projection_node including a communityId and centrality. Variables: dependencies_projection_node, dependencies_projection_write_property. Requires "Add_file_name and_extension.cypher".\n \n  MATCH (codeUnit)\n  WHERE $dependencies_projection_node IN LABELS(codeUnit)\n    AND codeUnit[$dependencies_projection_write_property] IS NOT NULL\n    // AND codeUnit.notExistingToForceRecalculation IS NOT NULL // uncomment this line to force recalculation\n OPTIONAL MATCH (artifact:Java:Artifact)-[:CONTAINS]->(codeUnit)\n    WITH *, artifact.name AS artifactName\n OPTIONAL MATCH (projectRoot:Directory)<-[:HAS_ROOT]-(proj:TS:Project)-[:CONTAINS]->(codeUnit)\n    WITH *, last(split(projectRoot.absoluteFileName, \'/\')) AS projectName   \n  RETURN DISTINCT \n         coalesce(codeUnit.fqn, codeUnit.globalFqn, codeUnit.fileName, codeUnit.signature, codeUnit.name) AS codeUnitName\n        ,codeUnit.name                AS shortCodeUnitName\n        ,coalesce(artifactName, projectName)                                                              AS projectName\n        ,coalesce(codeUnit.communityLeidenId, 0)           AS communityId\n        ,coalesce(codeUnit.centralityPageRank, 0.01)       AS centrality\n        ,codeUnit[$dependencies_projection_write_property] AS embedding\n   ORDER BY communityId'


    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownPropertyKeyWarning} {category: UNRECOGNIZED} {title: The provided property key is not in the database} {description: One of the property names in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing property name is: signature)} {position: line: 12, column: 81, offset: 924} for query: '// Query already calculated and written node embeddings on nodes with label in parameter $dependencies_projection_node including a communityId and centrality. Variables: dependencies_projection_node, dependencies_projection_write_property. Requires "Add_file_name and_extension.cypher".\n \n  MATCH (codeUnit)\n  WHERE $dependencies_projection_node IN LABELS(codeUnit)\n    AND codeUnit[$dependencies_projection_write_property] IS NOT NULL\n    // AND codeUnit.notExistingToForceRecalculation IS NOT NULL // uncomment this line to force recalculation\n OPTIONAL MATCH (artifact:Java:Artifact)-[:CONTAINS]->(codeUnit)\n    WITH *, artifact.name AS artifactName\n OPTIONAL MATCH (projectRoot:Directory)<-[:HAS_ROOT]-(proj:TS:Project)-[:CONTAINS]->(codeUnit)\n    WITH *, last(split(projectRoot.absoluteFileName, \'/\')) AS projectName   \n  RETURN DISTINCT \n         coalesce(codeUnit.fqn, codeUnit.globalFqn, codeUnit.fileName, codeUnit.signature, codeUnit.name) AS codeUnitName\n        ,codeUnit.name                AS shortCodeUnitName\n        ,coalesce(artifactName, projectName)                                                              AS projectName\n        ,coalesce(codeUnit.communityLeidenId, 0)           AS communityId\n        ,coalesce(codeUnit.centralityPageRank, 0.01)       AS centrality\n        ,codeUnit[$dependencies_projection_write_property] AS embedding\n   ORDER BY communityId'


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
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>config</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>1.705838</td>
      <td>[1.8371173739433289, 1.530931144952774, 0.6123...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>detectPackageManager</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>0.188886</td>
      <td>[1.530931144952774, 0.3061862289905548, 0.6123...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>config</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>2.129389</td>
      <td>[2.1433036029338837, 1.2247449159622192, 0.612...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>context</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>0.180345</td>
      <td>[1.2247449159622192, 0.6123724579811096, 1.224...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>generate</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>0.277201</td>
      <td>[1.2247449159622192, 0.3061862289905548, 0.918...</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsTypescript_files/NodeEmbeddingsTypescript_32_4.png)
    


### 1.6 Node Embeddings for Typescript Modules using node2vec

[node2vec](https://neo4j.com/docs/graph-data-science/current/machine-learning/node-embeddings/node2vec) computes a vector representation of a node based on second order random walks in the graph. 
The [node2vec](https://towardsdatascience.com/complete-guide-to-understanding-node2vec-algorithm-4e9a35e5d147) algorithm is a transductive node embedding algorithm, meaning that it needs the whole graph to be available to learn the node embeddings.

    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownLabelWarning} {category: UNRECOGNIZED} {title: The provided label is not in the database.} {description: One of the labels in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing label name is: Java)} {position: line: 7, column: 27, offset: 572} for query: '// Query already calculated and written node embeddings on nodes with label in parameter $dependencies_projection_node including a communityId and centrality. Variables: dependencies_projection_node, dependencies_projection_write_property. Requires "Add_file_name and_extension.cypher".\n \n  MATCH (codeUnit)\n  WHERE $dependencies_projection_node IN LABELS(codeUnit)\n    AND codeUnit[$dependencies_projection_write_property] IS NOT NULL\n    // AND codeUnit.notExistingToForceRecalculation IS NOT NULL // uncomment this line to force recalculation\n OPTIONAL MATCH (artifact:Java:Artifact)-[:CONTAINS]->(codeUnit)\n    WITH *, artifact.name AS artifactName\n OPTIONAL MATCH (projectRoot:Directory)<-[:HAS_ROOT]-(proj:TS:Project)-[:CONTAINS]->(codeUnit)\n    WITH *, last(split(projectRoot.absoluteFileName, \'/\')) AS projectName   \n  RETURN DISTINCT \n         coalesce(codeUnit.fqn, codeUnit.globalFqn, codeUnit.fileName, codeUnit.signature, codeUnit.name) AS codeUnitName\n        ,codeUnit.name                AS shortCodeUnitName\n        ,coalesce(artifactName, projectName)                                                              AS projectName\n        ,coalesce(codeUnit.communityLeidenId, 0)           AS communityId\n        ,coalesce(codeUnit.centralityPageRank, 0.01)       AS centrality\n        ,codeUnit[$dependencies_projection_write_property] AS embedding\n   ORDER BY communityId'


    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownPropertyKeyWarning} {category: UNRECOGNIZED} {title: The provided property key is not in the database} {description: One of the property names in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing property name is: signature)} {position: line: 12, column: 81, offset: 924} for query: '// Query already calculated and written node embeddings on nodes with label in parameter $dependencies_projection_node including a communityId and centrality. Variables: dependencies_projection_node, dependencies_projection_write_property. Requires "Add_file_name and_extension.cypher".\n \n  MATCH (codeUnit)\n  WHERE $dependencies_projection_node IN LABELS(codeUnit)\n    AND codeUnit[$dependencies_projection_write_property] IS NOT NULL\n    // AND codeUnit.notExistingToForceRecalculation IS NOT NULL // uncomment this line to force recalculation\n OPTIONAL MATCH (artifact:Java:Artifact)-[:CONTAINS]->(codeUnit)\n    WITH *, artifact.name AS artifactName\n OPTIONAL MATCH (projectRoot:Directory)<-[:HAS_ROOT]-(proj:TS:Project)-[:CONTAINS]->(codeUnit)\n    WITH *, last(split(projectRoot.absoluteFileName, \'/\')) AS projectName   \n  RETURN DISTINCT \n         coalesce(codeUnit.fqn, codeUnit.globalFqn, codeUnit.fileName, codeUnit.signature, codeUnit.name) AS codeUnitName\n        ,codeUnit.name                AS shortCodeUnitName\n        ,coalesce(artifactName, projectName)                                                              AS projectName\n        ,coalesce(codeUnit.communityLeidenId, 0)           AS communityId\n        ,coalesce(codeUnit.centralityPageRank, 0.01)       AS centrality\n        ,codeUnit[$dependencies_projection_write_property] AS embedding\n   ORDER BY communityId'


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
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>config</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>1.705838</td>
      <td>[-1.718456745147705, 0.20641838014125824, -0.4...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>detectPackageManager</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>0.188886</td>
      <td>[-1.2130721807479858, 0.12161558866500854, -0....</td>
    </tr>
    <tr>
      <th>2</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>config</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>2.129389</td>
      <td>[-1.6842386722564697, 0.1261667013168335, -0.3...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>context</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>0.180345</td>
      <td>[-1.7159409523010254, 0.20308297872543335, -0....</td>
    </tr>
    <tr>
      <th>4</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>generate</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>0.277201</td>
      <td>[-1.8294841051101685, 0.06012331694364548, -0....</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsTypescript_files/NodeEmbeddingsTypescript_34_4.png)
    


### 1.7 Node Embeddings for Java Packages using GraphSAGE


<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>modelName</th>
      <th>didConverge</th>
      <th>ranEpochs</th>
      <th>epochLosses</th>
      <th>trainingTimeMilliseconds</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>typescript-module-embeddings-notebook-graphSAGE</td>
      <td>False</td>
      <td>1</td>
      <td>[33.89941588827657]</td>
      <td>456</td>
    </tr>
  </tbody>
</table>
</div>


    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownLabelWarning} {category: UNRECOGNIZED} {title: The provided label is not in the database.} {description: One of the labels in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing label name is: Java)} {position: line: 11, column: 27, offset: 349} for query: '// Node Embeddings 4d using GraphSAGE: Stream. Requires "Add_file_name and_extension.cypher".\n \n CALL gds.beta.graphSage.stream(\n  $dependencies_projection + \'-cleaned\', {\n       modelName: $dependencies_projection + \'-graphSAGE\'\n   }\n )\n YIELD nodeId, embedding\n  WITH gds.util.asNode(nodeId) AS codeUnit\n      ,embedding\n OPTIONAL MATCH (artifact:Java:Artifact)-[:CONTAINS]->(codeUnit)\n    WITH *, artifact.name AS artifactName\n OPTIONAL MATCH (projectRoot:Directory)<-[:HAS_ROOT]-(proj:TS:Project)-[:CONTAINS]->(codeUnit)\n    WITH *, last(split(projectRoot.absoluteFileName, \'/\')) AS projectName   \n  RETURN DISTINCT \n         coalesce(codeUnit.fqn, codeUnit.globalFqn, codeUnit.fileName, codeUnit.signature, codeUnit.name) AS codeUnitName\n        ,codeUnit.name                               AS shortCodeUnitName\n        ,elementId(codeUnit)                         AS nodeElementId\n        ,coalesce(artifactName, projectName)         AS projectName\n        ,coalesce(codeUnit.communityLeidenId, 0)     AS communityId\n        ,coalesce(codeUnit.centralityPageRank, 0.01) AS centrality\n        ,embedding'


    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownPropertyKeyWarning} {category: UNRECOGNIZED} {title: The provided property key is not in the database} {description: One of the property names in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing property name is: signature)} {position: line: 16, column: 81, offset: 701} for query: '// Node Embeddings 4d using GraphSAGE: Stream. Requires "Add_file_name and_extension.cypher".\n \n CALL gds.beta.graphSage.stream(\n  $dependencies_projection + \'-cleaned\', {\n       modelName: $dependencies_projection + \'-graphSAGE\'\n   }\n )\n YIELD nodeId, embedding\n  WITH gds.util.asNode(nodeId) AS codeUnit\n      ,embedding\n OPTIONAL MATCH (artifact:Java:Artifact)-[:CONTAINS]->(codeUnit)\n    WITH *, artifact.name AS artifactName\n OPTIONAL MATCH (projectRoot:Directory)<-[:HAS_ROOT]-(proj:TS:Project)-[:CONTAINS]->(codeUnit)\n    WITH *, last(split(projectRoot.absoluteFileName, \'/\')) AS projectName   \n  RETURN DISTINCT \n         coalesce(codeUnit.fqn, codeUnit.globalFqn, codeUnit.fileName, codeUnit.signature, codeUnit.name) AS codeUnitName\n        ,codeUnit.name                               AS shortCodeUnitName\n        ,elementId(codeUnit)                         AS nodeElementId\n        ,coalesce(artifactName, projectName)         AS projectName\n        ,coalesce(codeUnit.communityLeidenId, 0)     AS communityId\n        ,coalesce(codeUnit.centralityPageRank, 0.01) AS centrality\n        ,embedding'



<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>codeUnitName</th>
      <th>shortCodeUnitName</th>
      <th>nodeElementId</th>
      <th>projectName</th>
      <th>communityId</th>
      <th>centrality</th>
      <th>embedding</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>config</td>
      <td>4:917ae344-1160-45dc-bb24-6210e2366804:10877</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>1.705838</td>
      <td>[-0.004854696200530722, 0.0380514686146112, 0....</td>
    </tr>
    <tr>
      <th>1</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>manifest</td>
      <td>4:917ae344-1160-45dc-bb24-6210e2366804:10879</td>
      <td>react-router-dev</td>
      <td>1</td>
      <td>0.150390</td>
      <td>[-0.0048546962005307235, 0.03805146861461116, ...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>routes</td>
      <td>4:917ae344-1160-45dc-bb24-6210e2366804:10880</td>
      <td>react-router-dev</td>
      <td>1</td>
      <td>4.035645</td>
      <td>[-0.004854696200530722, 0.038051468614611214, ...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>commands</td>
      <td>4:917ae344-1160-45dc-bb24-6210e2366804:10884</td>
      <td>react-router-dev</td>
      <td>2</td>
      <td>0.277500</td>
      <td>[-0.004854696200530722, 0.03805146861461115, 0...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>detectPackageManager</td>
      <td>4:917ae344-1160-45dc-bb24-6210e2366804:10886</td>
      <td>react-router-dev</td>
      <td>0</td>
      <td>0.188886</td>
      <td>[-0.0048546962005307235, 0.03805146861461118, ...</td>
    </tr>
  </tbody>
</table>
</div>



    
![png](NodeEmbeddingsTypescript_files/NodeEmbeddingsTypescript_36_4.png)
    


### 2. Compare Node Embeddings

In this section we will compare all node embedding methods from above in a grid plot. This helps to see how well the different algorithms were able to capture the structure of the graph and how well the communities are separated.


    
![png](NodeEmbeddingsTypescript_files/NodeEmbeddingsTypescript_38_0.png)
    


#### Interpreting Node Embedding Results

##### Summary of Observations

- **FastRP** and **node2vec** show clear, well-separated clusters
- **HashGNN** and **GraphSAGE** produce more diffuse embeddings
- Silhouette scores are high for FastRP / node2vec and low for HashGNN / GraphSAGE

These differences are expected and stem from the **fundamentally different objectives** of the algorithms.

##### Key Takeaways

- **FastRP and node2vec** are well-suited for **community discovery and visualization**
- **HashGNN** is best viewed as a **fast structural fingerprint**, not a clustering embedding
- **GraphSAGE** requires meaningful node features or labels and performs poorly in dense, feature-poor settings
- Poor silhouette scores for HashGNN and GraphSAGE are **expected and theoretically consistent**
