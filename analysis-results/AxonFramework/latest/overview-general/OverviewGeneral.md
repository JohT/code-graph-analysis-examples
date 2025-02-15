# Overview in General
<br>  

This file contains a general overview of the data in the graph including node labels and relationships types.

### References
- [jqassistant](https://jqassistant.org)
- [Neo4j Python Driver](https://neo4j.com/docs/api/python-driver/current)





## Node Labels

### Table 1a - Highest node count by label combination

Lists the 30 label combinations with the highest number of nodes. The labels with the lowest node count are listed in table 1b.
The total list would sum up to the total number of labels (100%).

The whole table can be found in the CSV report `Node_label_combination_count`.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>nodeLabels</th>
      <th>nodesWithThatLabels</th>
      <th>nodesWithThatLabelsPercent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>[Git, Change]</td>
      <td>261796</td>
      <td>74.462288</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>13197</td>
      <td>3.753605</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>13029</td>
      <td>3.705821</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Commit]</td>
      <td>12886</td>
      <td>3.665148</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Git]</td>
      <td>10887</td>
      <td>3.096575</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
      <td>7176</td>
      <td>2.041060</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Java, ByteCode, Bound]</td>
      <td>7118</td>
      <td>2.024563</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>3502</td>
      <td>0.996069</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Java, ByteCode, Bound, WildcardType]</td>
      <td>2908</td>
      <td>0.827119</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Java, Value, ByteCode, Annotation]</td>
      <td>2822</td>
      <td>0.802658</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Xml, Element]</td>
      <td>2144</td>
      <td>0.609815</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Java, ByteCode, Member, Method, Constructor]</td>
      <td>2039</td>
      <td>0.579950</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Xml, Text]</td>
      <td>1436</td>
      <td>0.408440</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Java, ByteCode, Bound, TypeVariable]</td>
      <td>1096</td>
      <td>0.311734</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Java, ByteCode, Member, Method, Lambda]</td>
      <td>942</td>
      <td>0.267932</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Type, File, Java, ByteCode, ResolvedDuplicate...</td>
      <td>877</td>
      <td>0.249444</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Type, File, Java, ByteCode, Class]</td>
      <td>810</td>
      <td>0.230387</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Java, Value, ByteCode, Primitive]</td>
      <td>652</td>
      <td>0.185447</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>644</td>
      <td>0.183172</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Java, ByteCode, Member, Method, GenericDeclar...</td>
      <td>569</td>
      <td>0.161840</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Json, Key]</td>
      <td>568</td>
      <td>0.161555</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Value, Json, Scalar]</td>
      <td>551</td>
      <td>0.156720</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Type, File, Java, ByteCode, ExternalType]</td>
      <td>380</td>
      <td>0.108083</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Author, Git, Person]</td>
      <td>298</td>
      <td>0.084760</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Value, Array]</td>
      <td>267</td>
      <td>0.075942</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Committer, Git, Person]</td>
      <td>252</td>
      <td>0.071676</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, File, Java, ByteCode, GenericDeclaratio...</td>
      <td>236</td>
      <td>0.067125</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Value, Property]</td>
      <td>202</td>
      <td>0.057455</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Type, File, Java, ByteCode, Interface]</td>
      <td>188</td>
      <td>0.053473</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Java, Value, ByteCode, Class]</td>
      <td>172</td>
      <td>0.048922</td>
    </tr>
  </tbody>
</table>
</div>



### Chart 1a - Highest node count by label combination

Values under 0.5% will be grouped into "others" to get a cleaner plot. The group "others" is then broken down in Chart 1b.


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewGeneral_files/OverviewGeneral_15_1.png)
    


### Table 1b - Lowest node count by label combination

Lists the 30 label combinations with the lowest number of nodes until they reach 0.5% of the total node count, which are shown above.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>nodeLabels</th>
      <th>nodesWithThatLabels</th>
      <th>nodesWithThatLabelsPercent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>[Analyze, Task, jQAssistant]</td>
      <td>1</td>
      <td>0.000284</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Package, File, Json, NPM]</td>
      <td>1</td>
      <td>0.000284</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000284</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[File, TS, Scan]</td>
      <td>1</td>
      <td>0.000284</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Json]</td>
      <td>2</td>
      <td>0.000569</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[File]</td>
      <td>3</td>
      <td>0.000853</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Java, ByteCode, Member, Method, GenericDeclar...</td>
      <td>4</td>
      <td>0.001138</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Maven, Exclusion]</td>
      <td>5</td>
      <td>0.001422</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Value, Array, Json]</td>
      <td>6</td>
      <td>0.001707</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Dependency, NPM]</td>
      <td>7</td>
      <td>0.001991</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Type, File, Java, ByteCode, Void]</td>
      <td>9</td>
      <td>0.002560</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[File, Maven, Xml, Pom, Document]</td>
      <td>9</td>
      <td>0.002560</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Java, ManifestSection]</td>
      <td>9</td>
      <td>0.002560</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[File, Java, Manifest]</td>
      <td>9</td>
      <td>0.002560</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Artifact, File, Jar, Archive, Zip, Java]</td>
      <td>9</td>
      <td>0.002560</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[File, Java, ServiceLoader]</td>
      <td>10</td>
      <td>0.002844</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[File, Java, Properties]</td>
      <td>12</td>
      <td>0.003413</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Maven, PluginExecution]</td>
      <td>16</td>
      <td>0.004551</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Maven, ExecutionGoal]</td>
      <td>16</td>
      <td>0.004551</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Type, File, Java, ByteCode, Throwable, Extern...</td>
      <td>16</td>
      <td>0.004551</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Xml, Attribute]</td>
      <td>18</td>
      <td>0.005120</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[jQAssistant, Rule, Concept]</td>
      <td>19</td>
      <td>0.005404</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Maven, Configuration]</td>
      <td>21</td>
      <td>0.005973</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Maven, Plugin]</td>
      <td>21</td>
      <td>0.005973</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, File, Java, ByteCode, Throwable, Resolv...</td>
      <td>22</td>
      <td>0.006257</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, File, Java, ByteCode, Enum]</td>
      <td>28</td>
      <td>0.007964</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, File, Java, ByteCode, PrimitiveType]</td>
      <td>29</td>
      <td>0.008248</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Xml, Namespace]</td>
      <td>36</td>
      <td>0.010239</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Type, File, Java, ByteCode, Annotation]</td>
      <td>43</td>
      <td>0.012230</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Git, Branch]</td>
      <td>44</td>
      <td>0.012515</td>
    </tr>
  </tbody>
</table>
</div>



### Chart 1b - Lowest node count by label combination

Shows the lowest (less than 0.5% overall) node count label combinations. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.01% will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewGeneral_files/OverviewGeneral_19_1.png)
    


### Table 1c - Highest node count by single label

Lists the 40 labels with the highest number of nodes.
Doesn't sum up to the total number of nodes or 100% because one node can have multiple labels.
Helps to identify commonly used labels.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>nodeLabel</th>
      <th>nodesWithThatLabel</th>
      <th>nodesWithThatLabelPercent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Git</td>
      <td>286334</td>
      <td>81.441598</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>261796</td>
      <td>74.462288</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Java</td>
      <td>59340</td>
      <td>16.877997</td>
    </tr>
    <tr>
      <th>3</th>
      <td>ByteCode</td>
      <td>59152</td>
      <td>16.824525</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Member</td>
      <td>20253</td>
      <td>5.760534</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Bound</td>
      <td>18456</td>
      <td>5.249415</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Method</td>
      <td>16751</td>
      <td>4.764465</td>
    </tr>
    <tr>
      <th>7</th>
      <td>File</td>
      <td>14749</td>
      <td>4.195038</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Parameter</td>
      <td>13029</td>
      <td>3.705821</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Commit</td>
      <td>12886</td>
      <td>3.665148</td>
    </tr>
    <tr>
      <th>10</th>
      <td>ParameterizedType</td>
      <td>7176</td>
      <td>2.041060</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Value</td>
      <td>5077</td>
      <td>1.444044</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Xml</td>
      <td>3643</td>
      <td>1.036174</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Type</td>
      <td>3618</td>
      <td>1.029063</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Field</td>
      <td>3502</td>
      <td>0.996069</td>
    </tr>
    <tr>
      <th>15</th>
      <td>WildcardType</td>
      <td>2908</td>
      <td>0.827119</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Annotation</td>
      <td>2865</td>
      <td>0.814888</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Element</td>
      <td>2144</td>
      <td>0.609815</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Constructor</td>
      <td>2043</td>
      <td>0.581088</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Text</td>
      <td>1436</td>
      <td>0.408440</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Class</td>
      <td>1272</td>
      <td>0.361793</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Json</td>
      <td>1263</td>
      <td>0.359233</td>
    </tr>
    <tr>
      <th>22</th>
      <td>TypeVariable</td>
      <td>1096</td>
      <td>0.311734</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Lambda</td>
      <td>942</td>
      <td>0.267932</td>
    </tr>
    <tr>
      <th>24</th>
      <td>ResolvedDuplicateType</td>
      <td>899</td>
      <td>0.255701</td>
    </tr>
    <tr>
      <th>25</th>
      <td>GenericDeclaration</td>
      <td>894</td>
      <td>0.254279</td>
    </tr>
    <tr>
      <th>26</th>
      <td>JavaType</td>
      <td>748</td>
      <td>0.212753</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Primitive</td>
      <td>652</td>
      <td>0.185447</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Key</td>
      <td>568</td>
      <td>0.161555</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Scalar</td>
      <td>551</td>
      <td>0.156720</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Person</td>
      <td>550</td>
      <td>0.156436</td>
    </tr>
    <tr>
      <th>31</th>
      <td>ExternalType</td>
      <td>489</td>
      <td>0.139086</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Maven</td>
      <td>343</td>
      <td>0.097559</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Author</td>
      <td>298</td>
      <td>0.084760</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Array</td>
      <td>273</td>
      <td>0.077649</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Interface</td>
      <td>273</td>
      <td>0.077649</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Committer</td>
      <td>252</td>
      <td>0.071676</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Property</td>
      <td>202</td>
      <td>0.057455</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Throwable</td>
      <td>196</td>
      <td>0.055748</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Directory</td>
      <td>187</td>
      <td>0.053188</td>
    </tr>
  </tbody>
</table>
</div>



### Chart 1c - Highest node count by label

Shows the 40 labels with the highest number of nodes.


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewGeneral_files/OverviewGeneral_23_1.png)
    


## Relationship Types

### Table 2a - Highest relationship count by type

Lists the 30 relationship types with the highest number of occurrences.
The whole table can be found in the CSV report `Relationship_type_count`.

    Total number of relationships: 1091605





<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>relationshipType</th>
      <th>nodesWithThatRelationshipType</th>
      <th>nodesWithThatRelationshipTypePercent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>CONTAINS_CHANGE</td>
      <td>261796</td>
      <td>23.982668</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>261796</td>
      <td>23.982668</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>172614</td>
      <td>15.812863</td>
    </tr>
    <tr>
      <th>3</th>
      <td>CREATES</td>
      <td>61715</td>
      <td>5.653602</td>
    </tr>
    <tr>
      <th>4</th>
      <td>DELETES</td>
      <td>38029</td>
      <td>3.483769</td>
    </tr>
    <tr>
      <th>5</th>
      <td>INVOKES</td>
      <td>35947</td>
      <td>3.293041</td>
    </tr>
    <tr>
      <th>6</th>
      <td>COMMITTED</td>
      <td>25772</td>
      <td>2.360927</td>
    </tr>
    <tr>
      <th>7</th>
      <td>DEPENDS_ON</td>
      <td>21931</td>
      <td>2.009060</td>
    </tr>
    <tr>
      <th>8</th>
      <td>OF_TYPE</td>
      <td>21394</td>
      <td>1.959866</td>
    </tr>
    <tr>
      <th>9</th>
      <td>DECLARES</td>
      <td>20698</td>
      <td>1.896107</td>
    </tr>
    <tr>
      <th>10</th>
      <td>OF_RAW_TYPE</td>
      <td>17093</td>
      <td>1.565859</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_PARENT</td>
      <td>15598</td>
      <td>1.428905</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS</td>
      <td>14125</td>
      <td>1.293966</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_COMMIT</td>
      <td>12886</td>
      <td>1.180464</td>
    </tr>
    <tr>
      <th>14</th>
      <td>RETURNS</td>
      <td>12578</td>
      <td>1.152248</td>
    </tr>
    <tr>
      <th>15</th>
      <td>HAS_FILE</td>
      <td>10887</td>
      <td>0.997339</td>
    </tr>
    <tr>
      <th>16</th>
      <td>RENAMES</td>
      <td>10562</td>
      <td>0.967566</td>
    </tr>
    <tr>
      <th>17</th>
      <td>READS</td>
      <td>9161</td>
      <td>0.839223</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>8288</td>
      <td>0.759249</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_NEW_NAME</td>
      <td>6240</td>
      <td>0.571635</td>
    </tr>
    <tr>
      <th>20</th>
      <td>OF_GENERIC_TYPE</td>
      <td>5906</td>
      <td>0.541038</td>
    </tr>
    <tr>
      <th>21</th>
      <td>RESOLVES_TO</td>
      <td>5216</td>
      <td>0.477829</td>
    </tr>
    <tr>
      <th>22</th>
      <td>SIMILAR</td>
      <td>3977</td>
      <td>0.364326</td>
    </tr>
    <tr>
      <th>23</th>
      <td>CONTAINS</td>
      <td>3824</td>
      <td>0.350310</td>
    </tr>
    <tr>
      <th>24</th>
      <td>WRITES</td>
      <td>3818</td>
      <td>0.349760</td>
    </tr>
    <tr>
      <th>25</th>
      <td>RETURNS_GENERIC</td>
      <td>3545</td>
      <td>0.324751</td>
    </tr>
    <tr>
      <th>26</th>
      <td>ANNOTATED_BY</td>
      <td>2810</td>
      <td>0.257419</td>
    </tr>
    <tr>
      <th>27</th>
      <td>REQUIRES</td>
      <td>2174</td>
      <td>0.199156</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_FIRST_CHILD</td>
      <td>2144</td>
      <td>0.196408</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_LAST_CHILD</td>
      <td>2144</td>
      <td>0.196408</td>
    </tr>
  </tbody>
</table>
</div>



### Chart 2a - Highest relationship count by type

Values under 0.5% will be grouped into "others" to get a cleaner plot. The group "others" is then broken down in the second chart.


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewGeneral_files/OverviewGeneral_28_1.png)
    


### Table 2b - Lowest relationship count by type

Lists the 30 relationships type with the lowest number of occurrences up to 0.5% of the total node count. This is essentially breaking down the "others" slice from the chart above.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>relationshipType</th>
      <th>nodesWithThatRelationshipType</th>
      <th>nodesWithThatRelationshipTypePercent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>HAS_PROPERTY</td>
      <td>1</td>
      <td>0.000092</td>
    </tr>
    <tr>
      <th>1</th>
      <td>THROWS_GENERIC</td>
      <td>5</td>
      <td>0.000458</td>
    </tr>
    <tr>
      <th>2</th>
      <td>EXCLUDES</td>
      <td>5</td>
      <td>0.000458</td>
    </tr>
    <tr>
      <th>3</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>7</td>
      <td>0.000641</td>
    </tr>
    <tr>
      <th>4</th>
      <td>DESCRIBES</td>
      <td>9</td>
      <td>0.000824</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_ROOT_ELEMENT</td>
      <td>10</td>
      <td>0.000916</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_GOAL</td>
      <td>16</td>
      <td>0.001466</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_EXECUTION</td>
      <td>16</td>
      <td>0.001466</td>
    </tr>
    <tr>
      <th>8</th>
      <td>OF_NAMESPACE</td>
      <td>18</td>
      <td>0.001649</td>
    </tr>
    <tr>
      <th>9</th>
      <td>HAS_ATTRIBUTE</td>
      <td>18</td>
      <td>0.001649</td>
    </tr>
    <tr>
      <th>10</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.001741</td>
    </tr>
    <tr>
      <th>11</th>
      <td>REQUIRES_TYPE_PARAMETER</td>
      <td>21</td>
      <td>0.001924</td>
    </tr>
    <tr>
      <th>12</th>
      <td>IS_ARTIFACT</td>
      <td>21</td>
      <td>0.001924</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_CONFIGURATION</td>
      <td>21</td>
      <td>0.001924</td>
    </tr>
    <tr>
      <th>14</th>
      <td>USES_PLUGIN</td>
      <td>21</td>
      <td>0.001924</td>
    </tr>
    <tr>
      <th>15</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.002565</td>
    </tr>
    <tr>
      <th>16</th>
      <td>HAS_DEFAULT</td>
      <td>36</td>
      <td>0.003298</td>
    </tr>
    <tr>
      <th>17</th>
      <td>DECLARES_NAMESPACE</td>
      <td>36</td>
      <td>0.003298</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_BRANCH</td>
      <td>44</td>
      <td>0.004031</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_HEAD</td>
      <td>45</td>
      <td>0.004122</td>
    </tr>
    <tr>
      <th>20</th>
      <td>CONTAINS_VALUE</td>
      <td>121</td>
      <td>0.011085</td>
    </tr>
    <tr>
      <th>21</th>
      <td>COPY_OF</td>
      <td>126</td>
      <td>0.011543</td>
    </tr>
    <tr>
      <th>22</th>
      <td>HAS_COMPONENT_TYPE</td>
      <td>158</td>
      <td>0.014474</td>
    </tr>
    <tr>
      <th>23</th>
      <td>TO_ARTIFACT</td>
      <td>163</td>
      <td>0.014932</td>
    </tr>
    <tr>
      <th>24</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>163</td>
      <td>0.014932</td>
    </tr>
    <tr>
      <th>25</th>
      <td>ON_COMMIT</td>
      <td>170</td>
      <td>0.015573</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_TAG</td>
      <td>170</td>
      <td>0.015573</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_COMMITTER</td>
      <td>252</td>
      <td>0.023085</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_AUTHOR</td>
      <td>298</td>
      <td>0.027299</td>
    </tr>
    <tr>
      <th>29</th>
      <td>COPIES</td>
      <td>331</td>
      <td>0.030322</td>
    </tr>
  </tbody>
</table>
</div>



### Chart 2b - Lowest relationship count by type

Shows the lowest (less than 0.5% overall) relationship types. This plot breaks down the "others" slice of the pie chart above. Values under 0.01% will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewGeneral_files/OverviewGeneral_32_1.png)
    


## Node labels with their relationships

### Table 3a - Highest relationship count by node labels and relationship type

Lists the 30 node labels and their relationship types with the highest number of occurrences.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sourceLabels</th>
      <th>relationType</th>
      <th>targetLabels</th>
      <th>numberOfRelationships</th>
      <th>numberOfNodesWithSameLabelsAsSource</th>
      <th>numberOfNodesWithSameLabelsAsTarget</th>
      <th>densityInPercent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change]</td>
      <td>261796</td>
      <td>12886</td>
      <td>261796</td>
      <td>0.007760</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>261796</td>
      <td>261796</td>
      <td>10887</td>
      <td>0.009185</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>172614</td>
      <td>261796</td>
      <td>10887</td>
      <td>0.006056</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Change]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>61715</td>
      <td>261796</td>
      <td>10887</td>
      <td>0.002165</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Change]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>38029</td>
      <td>261796</td>
      <td>10887</td>
      <td>0.001334</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>INVOKES</td>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>21999</td>
      <td>13102</td>
      <td>13102</td>
      <td>0.012815</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>15589</td>
      <td>12886</td>
      <td>12886</td>
      <td>0.009388</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>12886</td>
      <td>1</td>
      <td>12886</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>12886</td>
      <td>252</td>
      <td>12886</td>
      <td>0.396825</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>12886</td>
      <td>298</td>
      <td>12886</td>
      <td>0.335570</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>10887</td>
      <td>1</td>
      <td>10887</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Change]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>10562</td>
      <td>261796</td>
      <td>10887</td>
      <td>0.000371</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>HAS</td>
      <td>[Java, ByteCode, Parameter]</td>
      <td>8363</td>
      <td>13102</td>
      <td>13029</td>
      <td>0.004899</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>READS</td>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>8221</td>
      <td>13102</td>
      <td>3502</td>
      <td>0.017917</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>6240</td>
      <td>10887</td>
      <td>10887</td>
      <td>0.005265</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>OF_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>6079</td>
      <td>13029</td>
      <td>644</td>
      <td>0.072449</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Java, ByteCode, Bound]</td>
      <td>OF_RAW_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>3427</td>
      <td>7118</td>
      <td>644</td>
      <td>0.074760</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
      <td>OF_RAW_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>3053</td>
      <td>7176</td>
      <td>644</td>
      <td>0.066063</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>[Java, ByteCode, Bound, WildcardType]</td>
      <td>2908</td>
      <td>7176</td>
      <td>2908</td>
      <td>0.013935</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>OF_GENERIC_TYPE</td>
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
      <td>2657</td>
      <td>13029</td>
      <td>7176</td>
      <td>0.002842</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>[Java, ByteCode, Bound, TypeVariable]</td>
      <td>2454</td>
      <td>7176</td>
      <td>1096</td>
      <td>0.031202</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Java, ByteCode, Member, Method, Constructor]</td>
      <td>WRITES</td>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>2438</td>
      <td>2039</td>
      <td>3502</td>
      <td>0.034143</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Java, Value, ByteCode, Annotation]</td>
      <td>OF_TYPE</td>
      <td>[Type, File, Java, ByteCode, ExternalType, Ext...</td>
      <td>2341</td>
      <td>2822</td>
      <td>93</td>
      <td>0.891993</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Xml, Element]</td>
      <td>HAS_ELEMENT</td>
      <td>[Xml, Element]</td>
      <td>2126</td>
      <td>2144</td>
      <td>2144</td>
      <td>0.046250</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Java, ByteCode, Member, Method, Constructor]</td>
      <td>INVOKES</td>
      <td>[Java, ByteCode, Member, Method, Constructor]</td>
      <td>2119</td>
      <td>2039</td>
      <td>2039</td>
      <td>0.050968</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>RETURNS</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>2080</td>
      <td>13102</td>
      <td>644</td>
      <td>0.024651</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>INVOKES</td>
      <td>[Java, ByteCode, Member, Method, Constructor]</td>
      <td>2028</td>
      <td>13102</td>
      <td>2039</td>
      <td>0.007591</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Java, ByteCode, Member, Method, Constructor]</td>
      <td>HAS</td>
      <td>[Java, ByteCode, Parameter]</td>
      <td>2027</td>
      <td>2039</td>
      <td>13029</td>
      <td>0.007630</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>OF_GENERIC_TYPE</td>
      <td>[Java, ByteCode, Bound]</td>
      <td>2022</td>
      <td>13029</td>
      <td>7118</td>
      <td>0.002180</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Java, ByteCode, Member, Method, Lambda]</td>
      <td>INVOKES</td>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>1892</td>
      <td>942</td>
      <td>13102</td>
      <td>0.015330</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 351582
    total_number_of_relationships (edges): 1091605
    -> total directed graph density: 8.831073245674903e-06
    -> total directed graph density in percent: 0.0008831073245674903

