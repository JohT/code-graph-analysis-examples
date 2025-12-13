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
      <td>[Git, Update, Change]</td>
      <td>257375</td>
      <td>53.226470</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change, Create]</td>
      <td>74452</td>
      <td>15.397056</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change, Delete]</td>
      <td>44503</td>
      <td>9.203449</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Change, Rename]</td>
      <td>23284</td>
      <td>4.815251</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Git]</td>
      <td>15911</td>
      <td>3.290476</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Commit]</td>
      <td>15582</td>
      <td>3.222438</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>9227</td>
      <td>1.908191</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>8876</td>
      <td>1.835602</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Java, ByteCode, Bound]</td>
      <td>6300</td>
      <td>1.302872</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Java, Value, ByteCode, Annotation]</td>
      <td>5334</td>
      <td>1.103099</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
      <td>4849</td>
      <td>1.002798</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Xml, Element]</td>
      <td>2384</td>
      <td>0.493023</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>2187</td>
      <td>0.452283</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Xml, Text]</td>
      <td>1596</td>
      <td>0.330061</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Java, ByteCode, Member, Constructor, Method]</td>
      <td>1582</td>
      <td>0.327166</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Java, ByteCode, Bound, WildcardType]</td>
      <td>968</td>
      <td>0.200187</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Java, ByteCode, Member, Method, Lambda]</td>
      <td>851</td>
      <td>0.175991</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Java, ByteCode, Bound, TypeVariable]</td>
      <td>830</td>
      <td>0.171648</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>689</td>
      <td>0.142489</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Type, File, Java, Class, ByteCode]</td>
      <td>647</td>
      <td>0.133803</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Json, Key]</td>
      <td>533</td>
      <td>0.110227</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Value, Json, Scalar]</td>
      <td>523</td>
      <td>0.108159</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Git, Change, Copy]</td>
      <td>470</td>
      <td>0.097198</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, File, Java, ByteCode, ResolvedDuplicate...</td>
      <td>459</td>
      <td>0.094924</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Java, ByteCode, GenericDeclaration, Member, M...</td>
      <td>455</td>
      <td>0.094096</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Java, Value, ByteCode, Primitive]</td>
      <td>322</td>
      <td>0.066591</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Author, Git, Person]</td>
      <td>302</td>
      <td>0.062455</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Type, File, Java, ByteCode, ExternalType]</td>
      <td>301</td>
      <td>0.062248</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Committer, Git, Person]</td>
      <td>246</td>
      <td>0.050874</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Maven, Dependency]</td>
      <td>192</td>
      <td>0.039707</td>
    </tr>
  </tbody>
</table>
</div>



### Chart 1a - Highest node count by label combination

Values under 0.5% will be grouped into "others" to get a cleaner plot. The group "others" is then broken down in Chart 1b.


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewGeneral_files/OverviewGeneral_14_1.png)
    


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
      <td>0.000207</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Branch]</td>
      <td>1</td>
      <td>0.000207</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000207</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[File, Json]</td>
      <td>2</td>
      <td>0.000414</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File]</td>
      <td>3</td>
      <td>0.000620</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Maven, Exclusion]</td>
      <td>4</td>
      <td>0.000827</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Type, File, Java, ByteCode, GenericDeclaratio...</td>
      <td>4</td>
      <td>0.000827</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Value, Array, Json]</td>
      <td>8</td>
      <td>0.001654</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Type, File, Java, ByteCode, Throwable, Extern...</td>
      <td>8</td>
      <td>0.001654</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Java, ByteCode, GenericDeclaration, Member, C...</td>
      <td>9</td>
      <td>0.001861</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Maven, Scm]</td>
      <td>11</td>
      <td>0.002275</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[File, Maven, Xml, Pom, Document]</td>
      <td>11</td>
      <td>0.002275</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Type, File, Java, ByteCode, Throwable, Resolv...</td>
      <td>11</td>
      <td>0.002275</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Type, File, Java, ByteCode, Void]</td>
      <td>11</td>
      <td>0.002275</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Java, ManifestSection]</td>
      <td>11</td>
      <td>0.002275</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[File, Java, Manifest]</td>
      <td>11</td>
      <td>0.002275</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[File, Artifact, Jar, Archive, Zip, Java]</td>
      <td>11</td>
      <td>0.002275</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[File, Java, ServiceLoader]</td>
      <td>12</td>
      <td>0.002482</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Maven, PluginExecution]</td>
      <td>13</td>
      <td>0.002688</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[File, Java, Properties]</td>
      <td>13</td>
      <td>0.002688</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Maven, ExecutionGoal]</td>
      <td>13</td>
      <td>0.002688</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Type, File, Java, ByteCode, Enum]</td>
      <td>17</td>
      <td>0.003516</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[jQAssistant, Rule, Concept]</td>
      <td>19</td>
      <td>0.003929</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Maven, Configuration]</td>
      <td>20</td>
      <td>0.004136</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Maven, Plugin]</td>
      <td>20</td>
      <td>0.004136</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Xml, Attribute]</td>
      <td>22</td>
      <td>0.004550</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, File, Java, ByteCode, PrimitiveType]</td>
      <td>39</td>
      <td>0.008065</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Type, File, Java, ByteCode, Annotation]</td>
      <td>42</td>
      <td>0.008686</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Type, File, Java, Class, ByteCode, Throwable]</td>
      <td>42</td>
      <td>0.008686</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Xml, Namespace]</td>
      <td>44</td>
      <td>0.009099</td>
    </tr>
  </tbody>
</table>
</div>



### Chart 1b - Lowest node count by label combination

Shows the lowest (less than 0.5% overall) node count label combinations. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.01% will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewGeneral_files/OverviewGeneral_18_1.png)
    


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
      <td>432268</td>
      <td>89.395240</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>400084</td>
      <td>82.739423</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Update</td>
      <td>257375</td>
      <td>53.226470</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Create</td>
      <td>74452</td>
      <td>15.397056</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Java</td>
      <td>45189</td>
      <td>9.345317</td>
    </tr>
    <tr>
      <th>5</th>
      <td>ByteCode</td>
      <td>44988</td>
      <td>9.303749</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Delete</td>
      <td>44503</td>
      <td>9.203449</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Rename</td>
      <td>23284</td>
      <td>4.815251</td>
    </tr>
    <tr>
      <th>8</th>
      <td>File</td>
      <td>19047</td>
      <td>3.939017</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Commit</td>
      <td>15582</td>
      <td>3.222438</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Member</td>
      <td>13960</td>
      <td>2.887000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Bound</td>
      <td>13052</td>
      <td>2.699221</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Method</td>
      <td>11773</td>
      <td>2.434717</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Parameter</td>
      <td>9227</td>
      <td>1.908191</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Value</td>
      <td>6927</td>
      <td>1.432539</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Annotation</td>
      <td>5376</td>
      <td>1.111784</td>
    </tr>
    <tr>
      <th>16</th>
      <td>ParameterizedType</td>
      <td>4849</td>
      <td>1.002798</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Xml</td>
      <td>4057</td>
      <td>0.839008</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Type</td>
      <td>2874</td>
      <td>0.594358</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Element</td>
      <td>2384</td>
      <td>0.493023</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Field</td>
      <td>2187</td>
      <td>0.452283</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Text</td>
      <td>1596</td>
      <td>0.330061</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Constructor</td>
      <td>1591</td>
      <td>0.329027</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Json</td>
      <td>1198</td>
      <td>0.247753</td>
    </tr>
    <tr>
      <th>24</th>
      <td>WildcardType</td>
      <td>968</td>
      <td>0.200187</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Class</td>
      <td>893</td>
      <td>0.184677</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Lambda</td>
      <td>851</td>
      <td>0.175991</td>
    </tr>
    <tr>
      <th>27</th>
      <td>TypeVariable</td>
      <td>830</td>
      <td>0.171648</td>
    </tr>
    <tr>
      <th>28</th>
      <td>JavaType</td>
      <td>788</td>
      <td>0.162962</td>
    </tr>
    <tr>
      <th>29</th>
      <td>GenericDeclaration</td>
      <td>671</td>
      <td>0.138766</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Person</td>
      <td>548</td>
      <td>0.113329</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Key</td>
      <td>533</td>
      <td>0.110227</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Scalar</td>
      <td>523</td>
      <td>0.108159</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Copy</td>
      <td>470</td>
      <td>0.097198</td>
    </tr>
    <tr>
      <th>34</th>
      <td>ResolvedDuplicateType</td>
      <td>470</td>
      <td>0.097198</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Maven</td>
      <td>379</td>
      <td>0.078379</td>
    </tr>
    <tr>
      <th>36</th>
      <td>ExternalType</td>
      <td>371</td>
      <td>0.076725</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Primitive</td>
      <td>322</td>
      <td>0.066591</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Author</td>
      <td>302</td>
      <td>0.062455</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Interface</td>
      <td>266</td>
      <td>0.055010</td>
    </tr>
  </tbody>
</table>
</div>



### Chart 1c - Highest node count by label

Shows the 40 labels with the highest number of nodes.


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewGeneral_files/OverviewGeneral_22_1.png)
    


## Relationship Types

### Table 2a - Highest relationship count by type

Lists the 30 relationship types with the highest number of occurrences.
The whole table can be found in the CSV report `Relationship_type_count`.

    Total number of relationships: 1501837





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
      <td>400084</td>
      <td>26.639642</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>400084</td>
      <td>26.639642</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>257375</td>
      <td>17.137346</td>
    </tr>
    <tr>
      <th>3</th>
      <td>CREATES</td>
      <td>98206</td>
      <td>6.539058</td>
    </tr>
    <tr>
      <th>4</th>
      <td>DELETES</td>
      <td>67787</td>
      <td>4.513606</td>
    </tr>
    <tr>
      <th>5</th>
      <td>COMMITTED</td>
      <td>31164</td>
      <td>2.075059</td>
    </tr>
    <tr>
      <th>6</th>
      <td>RENAMES</td>
      <td>23284</td>
      <td>1.550368</td>
    </tr>
    <tr>
      <th>7</th>
      <td>INVOKES</td>
      <td>22195</td>
      <td>1.477857</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_PARENT</td>
      <td>18926</td>
      <td>1.260190</td>
    </tr>
    <tr>
      <th>9</th>
      <td>OF_TYPE</td>
      <td>18495</td>
      <td>1.231492</td>
    </tr>
    <tr>
      <th>10</th>
      <td>DEPENDS_ON</td>
      <td>17561</td>
      <td>1.169301</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_FILE</td>
      <td>15911</td>
      <td>1.059436</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS_COMMIT</td>
      <td>15582</td>
      <td>1.037529</td>
    </tr>
    <tr>
      <th>13</th>
      <td>DECLARES</td>
      <td>14299</td>
      <td>0.952101</td>
    </tr>
    <tr>
      <th>14</th>
      <td>OF_RAW_TYPE</td>
      <td>13122</td>
      <td>0.873730</td>
    </tr>
    <tr>
      <th>15</th>
      <td>HAS</td>
      <td>9843</td>
      <td>0.655397</td>
    </tr>
    <tr>
      <th>16</th>
      <td>HAS_NEW_NAME</td>
      <td>9378</td>
      <td>0.624435</td>
    </tr>
    <tr>
      <th>17</th>
      <td>RETURNS</td>
      <td>8100</td>
      <td>0.539339</td>
    </tr>
    <tr>
      <th>18</th>
      <td>READS</td>
      <td>5929</td>
      <td>0.394783</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>5753</td>
      <td>0.383064</td>
    </tr>
    <tr>
      <th>20</th>
      <td>ANNOTATED_BY</td>
      <td>5333</td>
      <td>0.355098</td>
    </tr>
    <tr>
      <th>21</th>
      <td>OF_GENERIC_TYPE</td>
      <td>4392</td>
      <td>0.292442</td>
    </tr>
    <tr>
      <th>22</th>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>3686</td>
      <td>0.245433</td>
    </tr>
    <tr>
      <th>23</th>
      <td>SIMILAR</td>
      <td>3370</td>
      <td>0.224392</td>
    </tr>
    <tr>
      <th>24</th>
      <td>CONTAINS</td>
      <td>3183</td>
      <td>0.211940</td>
    </tr>
    <tr>
      <th>25</th>
      <td>RETURNS_GENERIC</td>
      <td>2586</td>
      <td>0.172189</td>
    </tr>
    <tr>
      <th>26</th>
      <td>RESOLVES_TO</td>
      <td>2568</td>
      <td>0.170991</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_FIRST_CHILD</td>
      <td>2384</td>
      <td>0.158739</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_LAST_CHILD</td>
      <td>2384</td>
      <td>0.158739</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_ELEMENT</td>
      <td>2362</td>
      <td>0.157274</td>
    </tr>
  </tbody>
</table>
</div>



### Chart 2a - Highest relationship count by type

Values under 0.5% will be grouped into "others" to get a cleaner plot. The group "others" is then broken down in the second chart.


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewGeneral_files/OverviewGeneral_27_1.png)
    


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
      <td>0.000067</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HAS_BRANCH</td>
      <td>1</td>
      <td>0.000067</td>
    </tr>
    <tr>
      <th>2</th>
      <td>HAS_HEAD</td>
      <td>2</td>
      <td>0.000133</td>
    </tr>
    <tr>
      <th>3</th>
      <td>THROWS_GENERIC</td>
      <td>3</td>
      <td>0.000200</td>
    </tr>
    <tr>
      <th>4</th>
      <td>EXCLUDES</td>
      <td>4</td>
      <td>0.000266</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_SCM</td>
      <td>11</td>
      <td>0.000732</td>
    </tr>
    <tr>
      <th>6</th>
      <td>DESCRIBES</td>
      <td>11</td>
      <td>0.000732</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_ROOT_ELEMENT</td>
      <td>12</td>
      <td>0.000799</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_GOAL</td>
      <td>13</td>
      <td>0.000866</td>
    </tr>
    <tr>
      <th>9</th>
      <td>HAS_EXECUTION</td>
      <td>13</td>
      <td>0.000866</td>
    </tr>
    <tr>
      <th>10</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.001265</td>
    </tr>
    <tr>
      <th>11</th>
      <td>IS_ARTIFACT</td>
      <td>20</td>
      <td>0.001332</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS_CONFIGURATION</td>
      <td>20</td>
      <td>0.001332</td>
    </tr>
    <tr>
      <th>13</th>
      <td>USES_PLUGIN</td>
      <td>20</td>
      <td>0.001332</td>
    </tr>
    <tr>
      <th>14</th>
      <td>OF_NAMESPACE</td>
      <td>22</td>
      <td>0.001465</td>
    </tr>
    <tr>
      <th>15</th>
      <td>HAS_ATTRIBUTE</td>
      <td>22</td>
      <td>0.001465</td>
    </tr>
    <tr>
      <th>16</th>
      <td>REQUIRES_TYPE_PARAMETER</td>
      <td>26</td>
      <td>0.001731</td>
    </tr>
    <tr>
      <th>17</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.001864</td>
    </tr>
    <tr>
      <th>18</th>
      <td>DECLARES_NAMESPACE</td>
      <td>44</td>
      <td>0.002930</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_DEFAULT</td>
      <td>53</td>
      <td>0.003529</td>
    </tr>
    <tr>
      <th>20</th>
      <td>HAS_COMPONENT_TYPE</td>
      <td>105</td>
      <td>0.006991</td>
    </tr>
    <tr>
      <th>21</th>
      <td>CONTAINS_VALUE</td>
      <td>128</td>
      <td>0.008523</td>
    </tr>
    <tr>
      <th>22</th>
      <td>HAS_TAG</td>
      <td>141</td>
      <td>0.009389</td>
    </tr>
    <tr>
      <th>23</th>
      <td>ON_COMMIT</td>
      <td>141</td>
      <td>0.009389</td>
    </tr>
    <tr>
      <th>24</th>
      <td>COPY_OF</td>
      <td>181</td>
      <td>0.012052</td>
    </tr>
    <tr>
      <th>25</th>
      <td>TO_ARTIFACT</td>
      <td>192</td>
      <td>0.012784</td>
    </tr>
    <tr>
      <th>26</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>192</td>
      <td>0.012784</td>
    </tr>
    <tr>
      <th>27</th>
      <td>IS</td>
      <td>228</td>
      <td>0.015181</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_COMMITTER</td>
      <td>246</td>
      <td>0.016380</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_LOWER_BOUND</td>
      <td>248</td>
      <td>0.016513</td>
    </tr>
  </tbody>
</table>
</div>



### Chart 2b - Lowest relationship count by type

Shows the lowest (less than 0.5% overall) relationship types. This plot breaks down the "others" slice of the pie chart above. Values under 0.01% will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewGeneral_files/OverviewGeneral_31_1.png)
    


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
      <td>[Git, Update, Change]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>257375</td>
      <td>257375</td>
      <td>15911</td>
      <td>0.006285</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Update, Change]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>257375</td>
      <td>257375</td>
      <td>15911</td>
      <td>0.006285</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Update, Change]</td>
      <td>257375</td>
      <td>15582</td>
      <td>257375</td>
      <td>0.006418</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>74452</td>
      <td>15582</td>
      <td>74452</td>
      <td>0.006418</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>74452</td>
      <td>74452</td>
      <td>15911</td>
      <td>0.006285</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>74452</td>
      <td>74452</td>
      <td>15911</td>
      <td>0.006285</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>44503</td>
      <td>15582</td>
      <td>44503</td>
      <td>0.006418</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>44503</td>
      <td>44503</td>
      <td>15911</td>
      <td>0.006285</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>44503</td>
      <td>44503</td>
      <td>15911</td>
      <td>0.006285</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>23284</td>
      <td>15582</td>
      <td>23284</td>
      <td>0.006418</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>23284</td>
      <td>23284</td>
      <td>15911</td>
      <td>0.006285</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>23284</td>
      <td>23284</td>
      <td>15911</td>
      <td>0.006285</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>23284</td>
      <td>23284</td>
      <td>15911</td>
      <td>0.006285</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>23284</td>
      <td>23284</td>
      <td>15911</td>
      <td>0.006285</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>18915</td>
      <td>15582</td>
      <td>15582</td>
      <td>0.007790</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>15911</td>
      <td>1</td>
      <td>15911</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>15582</td>
      <td>1</td>
      <td>15582</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>15582</td>
      <td>246</td>
      <td>15582</td>
      <td>0.406504</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>15582</td>
      <td>302</td>
      <td>15582</td>
      <td>0.331126</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>INVOKES</td>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>13220</td>
      <td>8848</td>
      <td>8848</td>
      <td>0.016887</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>9378</td>
      <td>15911</td>
      <td>15911</td>
      <td>0.003704</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>HAS</td>
      <td>[Java, ByteCode, Parameter]</td>
      <td>5323</td>
      <td>8848</td>
      <td>9227</td>
      <td>0.006520</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>READS</td>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>5322</td>
      <td>8848</td>
      <td>2187</td>
      <td>0.027503</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Java, Value, ByteCode, Annotation]</td>
      <td>OF_TYPE</td>
      <td>[Type, File, Java, ByteCode, ExternalAnnotatio...</td>
      <td>4990</td>
      <td>5334</td>
      <td>62</td>
      <td>1.508884</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>OF_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>4105</td>
      <td>9227</td>
      <td>689</td>
      <td>0.064570</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>ANNOTATED_BY</td>
      <td>[Java, Value, ByteCode, Annotation]</td>
      <td>3797</td>
      <td>9227</td>
      <td>5334</td>
      <td>0.007715</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[File, Git]</td>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>[File, Git]</td>
      <td>3068</td>
      <td>15911</td>
      <td>15911</td>
      <td>0.001212</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
      <td>OF_RAW_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>2799</td>
      <td>4849</td>
      <td>689</td>
      <td>0.083778</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Xml, Element]</td>
      <td>HAS_ELEMENT</td>
      <td>[Xml, Element]</td>
      <td>2362</td>
      <td>2384</td>
      <td>2384</td>
      <td>0.041559</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Java, ByteCode, Bound]</td>
      <td>OF_RAW_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>2256</td>
      <td>6300</td>
      <td>689</td>
      <td>0.051973</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 483547
    total_number_of_relationships (edges): 1501837
    -> total directed graph density: 6.423124075366494e-06
    -> total directed graph density in percent: 0.0006423124075366494

