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
      <td>263015</td>
      <td>74.164777</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>13529</td>
      <td>3.814898</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>13293</td>
      <td>3.748350</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Commit]</td>
      <td>12966</td>
      <td>3.656143</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Git]</td>
      <td>10911</td>
      <td>3.076676</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Java, ByteCode, ParameterizedType, Bound]</td>
      <td>7279</td>
      <td>2.052527</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Java, ByteCode, Bound]</td>
      <td>7240</td>
      <td>2.041530</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>3604</td>
      <td>1.016253</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Java, ByteCode, Bound, WildcardType]</td>
      <td>2947</td>
      <td>0.830993</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Java, Value, ByteCode, Annotation]</td>
      <td>2931</td>
      <td>0.826481</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Xml, Element]</td>
      <td>2162</td>
      <td>0.609639</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Java, ByteCode, Constructor, Method, Member]</td>
      <td>2128</td>
      <td>0.600052</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Xml, Text]</td>
      <td>1450</td>
      <td>0.408870</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Java, ByteCode, Bound, TypeVariable]</td>
      <td>1111</td>
      <td>0.313279</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Java, ByteCode, Method, Member, Lambda]</td>
      <td>968</td>
      <td>0.272956</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Type, File, Java, ByteCode, ResolvedDuplicate...</td>
      <td>888</td>
      <td>0.250398</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Type, File, Java, Class, ByteCode]</td>
      <td>846</td>
      <td>0.238554</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Json, Key]</td>
      <td>702</td>
      <td>0.197949</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Value, Json, Scalar]</td>
      <td>685</td>
      <td>0.193156</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Java, Value, ByteCode, Primitive]</td>
      <td>672</td>
      <td>0.189490</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>649</td>
      <td>0.183005</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Java, ByteCode, Method, Member, GenericDeclar...</td>
      <td>578</td>
      <td>0.162984</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Type, File, Java, ByteCode, ExternalType]</td>
      <td>411</td>
      <td>0.115893</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Author, Git, Person]</td>
      <td>299</td>
      <td>0.084312</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Value, Array]</td>
      <td>287</td>
      <td>0.080928</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Committer, Git, Person]</td>
      <td>252</td>
      <td>0.071059</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, File, Java, Class, ByteCode, GenericDec...</td>
      <td>237</td>
      <td>0.066829</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Value, Property]</td>
      <td>211</td>
      <td>0.059498</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Type, File, Java, ByteCode, Interface]</td>
      <td>190</td>
      <td>0.053576</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Java, Value, Class, ByteCode]</td>
      <td>189</td>
      <td>0.053294</td>
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
      <td>0.000282</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Package, File, Json, NPM]</td>
      <td>1</td>
      <td>0.000282</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000282</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[File, TS, Scan]</td>
      <td>1</td>
      <td>0.000282</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Json]</td>
      <td>2</td>
      <td>0.000564</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[File]</td>
      <td>3</td>
      <td>0.000846</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Java, ByteCode, Constructor, Method, Member, ...</td>
      <td>4</td>
      <td>0.001128</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Maven, Exclusion]</td>
      <td>5</td>
      <td>0.001410</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Value, Array, Json]</td>
      <td>6</td>
      <td>0.001692</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Dependency, NPM]</td>
      <td>7</td>
      <td>0.001974</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[File, Maven, Xml, Pom, Document]</td>
      <td>9</td>
      <td>0.002538</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Type, File, Java, ByteCode, Void]</td>
      <td>9</td>
      <td>0.002538</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Java, ManifestSection]</td>
      <td>9</td>
      <td>0.002538</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[File, Java, Manifest]</td>
      <td>9</td>
      <td>0.002538</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Artifact, File, Jar, Archive, Zip, Java]</td>
      <td>9</td>
      <td>0.002538</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[File, Java, ServiceLoader]</td>
      <td>10</td>
      <td>0.002820</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[File, Java, Properties]</td>
      <td>12</td>
      <td>0.003384</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Maven, PluginExecution]</td>
      <td>16</td>
      <td>0.004512</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Maven, ExecutionGoal]</td>
      <td>16</td>
      <td>0.004512</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Xml, Attribute]</td>
      <td>18</td>
      <td>0.005076</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[jQAssistant, Rule, Concept]</td>
      <td>19</td>
      <td>0.005358</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Maven, Plugin]</td>
      <td>21</td>
      <td>0.005922</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Type, File, Java, ByteCode, Throwable, Extern...</td>
      <td>21</td>
      <td>0.005922</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Maven, Configuration]</td>
      <td>21</td>
      <td>0.005922</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, File, Java, ByteCode, Throwable, Resolv...</td>
      <td>22</td>
      <td>0.006204</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, File, Java, ByteCode, Enum]</td>
      <td>28</td>
      <td>0.007895</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, File, Java, ByteCode, PrimitiveType]</td>
      <td>30</td>
      <td>0.008459</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Xml, Namespace]</td>
      <td>36</td>
      <td>0.010151</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Type, File, Java, ByteCode, Annotation]</td>
      <td>44</td>
      <td>0.012407</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Git, Branch]</td>
      <td>45</td>
      <td>0.012689</td>
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
      <td>287660</td>
      <td>81.114156</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>263015</td>
      <td>74.164777</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Java</td>
      <td>60697</td>
      <td>17.115296</td>
    </tr>
    <tr>
      <th>3</th>
      <td>ByteCode</td>
      <td>60507</td>
      <td>17.061720</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Member</td>
      <td>20811</td>
      <td>5.868271</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Bound</td>
      <td>18743</td>
      <td>5.285137</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Method</td>
      <td>17207</td>
      <td>4.852017</td>
    </tr>
    <tr>
      <th>7</th>
      <td>File</td>
      <td>14872</td>
      <td>4.193596</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Parameter</td>
      <td>13293</td>
      <td>3.748350</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Commit</td>
      <td>12966</td>
      <td>3.656143</td>
    </tr>
    <tr>
      <th>10</th>
      <td>ParameterizedType</td>
      <td>7279</td>
      <td>2.052527</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Value</td>
      <td>5428</td>
      <td>1.530583</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Type</td>
      <td>3715</td>
      <td>1.047553</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Xml</td>
      <td>3675</td>
      <td>1.036274</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Field</td>
      <td>3604</td>
      <td>1.016253</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Annotation</td>
      <td>2975</td>
      <td>0.838888</td>
    </tr>
    <tr>
      <th>16</th>
      <td>WildcardType</td>
      <td>2947</td>
      <td>0.830993</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Element</td>
      <td>2162</td>
      <td>0.609639</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Constructor</td>
      <td>2132</td>
      <td>0.601180</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Json</td>
      <td>1570</td>
      <td>0.442707</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Text</td>
      <td>1450</td>
      <td>0.408870</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Class</td>
      <td>1327</td>
      <td>0.374186</td>
    </tr>
    <tr>
      <th>22</th>
      <td>TypeVariable</td>
      <td>1111</td>
      <td>0.313279</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Lambda</td>
      <td>968</td>
      <td>0.272956</td>
    </tr>
    <tr>
      <th>24</th>
      <td>ResolvedDuplicateType</td>
      <td>910</td>
      <td>0.256601</td>
    </tr>
    <tr>
      <th>25</th>
      <td>GenericDeclaration</td>
      <td>904</td>
      <td>0.254909</td>
    </tr>
    <tr>
      <th>26</th>
      <td>JavaType</td>
      <td>754</td>
      <td>0.212612</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Key</td>
      <td>702</td>
      <td>0.197949</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Scalar</td>
      <td>685</td>
      <td>0.193156</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Primitive</td>
      <td>672</td>
      <td>0.189490</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Person</td>
      <td>551</td>
      <td>0.155371</td>
    </tr>
    <tr>
      <th>31</th>
      <td>ExternalType</td>
      <td>527</td>
      <td>0.148603</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Maven</td>
      <td>346</td>
      <td>0.097565</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Author</td>
      <td>299</td>
      <td>0.084312</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Array</td>
      <td>293</td>
      <td>0.082620</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Interface</td>
      <td>275</td>
      <td>0.077544</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Committer</td>
      <td>252</td>
      <td>0.071059</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Property</td>
      <td>211</td>
      <td>0.059498</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Throwable</td>
      <td>203</td>
      <td>0.057242</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Directory</td>
      <td>189</td>
      <td>0.053294</td>
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

    Total number of relationships: 1100439





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
      <td>263015</td>
      <td>23.900916</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>263015</td>
      <td>23.900916</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>173566</td>
      <td>15.772433</td>
    </tr>
    <tr>
      <th>3</th>
      <td>CREATES</td>
      <td>61961</td>
      <td>5.630571</td>
    </tr>
    <tr>
      <th>4</th>
      <td>DELETES</td>
      <td>38056</td>
      <td>3.458256</td>
    </tr>
    <tr>
      <th>5</th>
      <td>INVOKES</td>
      <td>36595</td>
      <td>3.325491</td>
    </tr>
    <tr>
      <th>6</th>
      <td>COMMITTED</td>
      <td>25932</td>
      <td>2.356514</td>
    </tr>
    <tr>
      <th>7</th>
      <td>DEPENDS_ON</td>
      <td>22492</td>
      <td>2.043912</td>
    </tr>
    <tr>
      <th>8</th>
      <td>OF_TYPE</td>
      <td>21920</td>
      <td>1.991932</td>
    </tr>
    <tr>
      <th>9</th>
      <td>DECLARES</td>
      <td>21272</td>
      <td>1.933047</td>
    </tr>
    <tr>
      <th>10</th>
      <td>OF_RAW_TYPE</td>
      <td>17353</td>
      <td>1.576916</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_PARENT</td>
      <td>15699</td>
      <td>1.426612</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS</td>
      <td>14429</td>
      <td>1.311204</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_COMMIT</td>
      <td>12966</td>
      <td>1.178257</td>
    </tr>
    <tr>
      <th>14</th>
      <td>RETURNS</td>
      <td>12844</td>
      <td>1.167171</td>
    </tr>
    <tr>
      <th>15</th>
      <td>HAS_FILE</td>
      <td>10911</td>
      <td>0.991513</td>
    </tr>
    <tr>
      <th>16</th>
      <td>RENAMES</td>
      <td>10568</td>
      <td>0.960344</td>
    </tr>
    <tr>
      <th>17</th>
      <td>READS</td>
      <td>9378</td>
      <td>0.852205</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>8407</td>
      <td>0.763968</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_NEW_NAME</td>
      <td>6244</td>
      <td>0.567410</td>
    </tr>
    <tr>
      <th>20</th>
      <td>OF_GENERIC_TYPE</td>
      <td>5996</td>
      <td>0.544873</td>
    </tr>
    <tr>
      <th>21</th>
      <td>RESOLVES_TO</td>
      <td>5279</td>
      <td>0.479718</td>
    </tr>
    <tr>
      <th>22</th>
      <td>SIMILAR</td>
      <td>4078</td>
      <td>0.370579</td>
    </tr>
    <tr>
      <th>23</th>
      <td>WRITES</td>
      <td>3944</td>
      <td>0.358402</td>
    </tr>
    <tr>
      <th>24</th>
      <td>CONTAINS</td>
      <td>3936</td>
      <td>0.357675</td>
    </tr>
    <tr>
      <th>25</th>
      <td>RETURNS_GENERIC</td>
      <td>3593</td>
      <td>0.326506</td>
    </tr>
    <tr>
      <th>26</th>
      <td>ANNOTATED_BY</td>
      <td>2919</td>
      <td>0.265258</td>
    </tr>
    <tr>
      <th>27</th>
      <td>REQUIRES</td>
      <td>2230</td>
      <td>0.202646</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_FIRST_CHILD</td>
      <td>2162</td>
      <td>0.196467</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_LAST_CHILD</td>
      <td>2162</td>
      <td>0.196467</td>
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
      <td>0.000091</td>
    </tr>
    <tr>
      <th>1</th>
      <td>THROWS_GENERIC</td>
      <td>5</td>
      <td>0.000454</td>
    </tr>
    <tr>
      <th>2</th>
      <td>EXCLUDES</td>
      <td>5</td>
      <td>0.000454</td>
    </tr>
    <tr>
      <th>3</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>7</td>
      <td>0.000636</td>
    </tr>
    <tr>
      <th>4</th>
      <td>DESCRIBES</td>
      <td>9</td>
      <td>0.000818</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_ROOT_ELEMENT</td>
      <td>9</td>
      <td>0.000818</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_GOAL</td>
      <td>16</td>
      <td>0.001454</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_EXECUTION</td>
      <td>16</td>
      <td>0.001454</td>
    </tr>
    <tr>
      <th>8</th>
      <td>OF_NAMESPACE</td>
      <td>18</td>
      <td>0.001636</td>
    </tr>
    <tr>
      <th>9</th>
      <td>HAS_ATTRIBUTE</td>
      <td>18</td>
      <td>0.001636</td>
    </tr>
    <tr>
      <th>10</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.001727</td>
    </tr>
    <tr>
      <th>11</th>
      <td>IS_ARTIFACT</td>
      <td>21</td>
      <td>0.001908</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS_CONFIGURATION</td>
      <td>21</td>
      <td>0.001908</td>
    </tr>
    <tr>
      <th>13</th>
      <td>USES_PLUGIN</td>
      <td>21</td>
      <td>0.001908</td>
    </tr>
    <tr>
      <th>14</th>
      <td>REQUIRES_TYPE_PARAMETER</td>
      <td>24</td>
      <td>0.002181</td>
    </tr>
    <tr>
      <th>15</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.002544</td>
    </tr>
    <tr>
      <th>16</th>
      <td>DECLARES_NAMESPACE</td>
      <td>36</td>
      <td>0.003271</td>
    </tr>
    <tr>
      <th>17</th>
      <td>HAS_DEFAULT</td>
      <td>39</td>
      <td>0.003544</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_BRANCH</td>
      <td>45</td>
      <td>0.004089</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_HEAD</td>
      <td>46</td>
      <td>0.004180</td>
    </tr>
    <tr>
      <th>20</th>
      <td>COPY_OF</td>
      <td>126</td>
      <td>0.011450</td>
    </tr>
    <tr>
      <th>21</th>
      <td>CONTAINS_VALUE</td>
      <td>160</td>
      <td>0.014540</td>
    </tr>
    <tr>
      <th>22</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>165</td>
      <td>0.014994</td>
    </tr>
    <tr>
      <th>23</th>
      <td>TO_ARTIFACT</td>
      <td>165</td>
      <td>0.014994</td>
    </tr>
    <tr>
      <th>24</th>
      <td>HAS_COMPONENT_TYPE</td>
      <td>166</td>
      <td>0.015085</td>
    </tr>
    <tr>
      <th>25</th>
      <td>ON_COMMIT</td>
      <td>171</td>
      <td>0.015539</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_TAG</td>
      <td>171</td>
      <td>0.015539</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_COMMITTER</td>
      <td>252</td>
      <td>0.022900</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_AUTHOR</td>
      <td>299</td>
      <td>0.027171</td>
    </tr>
    <tr>
      <th>29</th>
      <td>COPIES</td>
      <td>331</td>
      <td>0.030079</td>
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
      <td>263015</td>
      <td>12966</td>
      <td>263015</td>
      <td>0.007712</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>263015</td>
      <td>263015</td>
      <td>10911</td>
      <td>0.009165</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>173566</td>
      <td>263015</td>
      <td>10911</td>
      <td>0.006048</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Change]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>61961</td>
      <td>263015</td>
      <td>10911</td>
      <td>0.002159</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Change]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>38056</td>
      <td>263015</td>
      <td>10911</td>
      <td>0.001326</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>INVOKES</td>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>22076</td>
      <td>13427</td>
      <td>13427</td>
      <td>0.012245</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>15690</td>
      <td>12966</td>
      <td>12966</td>
      <td>0.009333</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>12966</td>
      <td>1</td>
      <td>12966</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>12966</td>
      <td>299</td>
      <td>12966</td>
      <td>0.334448</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>12966</td>
      <td>252</td>
      <td>12966</td>
      <td>0.396825</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>10911</td>
      <td>1</td>
      <td>10911</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Change]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>10568</td>
      <td>263015</td>
      <td>10911</td>
      <td>0.000368</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>HAS</td>
      <td>[Java, ByteCode, Parameter]</td>
      <td>8476</td>
      <td>13427</td>
      <td>13293</td>
      <td>0.004749</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>READS</td>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>8448</td>
      <td>13427</td>
      <td>3604</td>
      <td>0.017458</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>6244</td>
      <td>10911</td>
      <td>10911</td>
      <td>0.005245</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>OF_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>6156</td>
      <td>13293</td>
      <td>649</td>
      <td>0.071356</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Java, ByteCode, Bound]</td>
      <td>OF_RAW_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>3465</td>
      <td>7240</td>
      <td>649</td>
      <td>0.073743</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Java, ByteCode, ParameterizedType, Bound]</td>
      <td>OF_RAW_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>3110</td>
      <td>7279</td>
      <td>649</td>
      <td>0.065833</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Java, ByteCode, ParameterizedType, Bound]</td>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>[Java, ByteCode, Bound, WildcardType]</td>
      <td>2947</td>
      <td>7279</td>
      <td>2947</td>
      <td>0.013738</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>OF_GENERIC_TYPE</td>
      <td>[Java, ByteCode, ParameterizedType, Bound]</td>
      <td>2695</td>
      <td>13293</td>
      <td>7279</td>
      <td>0.002785</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Java, ByteCode, Constructor, Method, Member]</td>
      <td>WRITES</td>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>2519</td>
      <td>2128</td>
      <td>3604</td>
      <td>0.032845</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Java, ByteCode, ParameterizedType, Bound]</td>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>[Java, ByteCode, Bound, TypeVariable]</td>
      <td>2474</td>
      <td>7279</td>
      <td>1111</td>
      <td>0.030592</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Java, Value, ByteCode, Annotation]</td>
      <td>OF_TYPE</td>
      <td>[Type, File, Java, ByteCode, ExternalType, Ext...</td>
      <td>2445</td>
      <td>2931</td>
      <td>95</td>
      <td>0.878091</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Java, ByteCode, Constructor, Method, Member]</td>
      <td>INVOKES</td>
      <td>[Java, ByteCode, Constructor, Method, Member]</td>
      <td>2195</td>
      <td>2128</td>
      <td>2128</td>
      <td>0.048472</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Xml, Element]</td>
      <td>HAS_ELEMENT</td>
      <td>[Xml, Element]</td>
      <td>2144</td>
      <td>2162</td>
      <td>2162</td>
      <td>0.045868</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>INVOKES</td>
      <td>[Java, ByteCode, Constructor, Method, Member]</td>
      <td>2121</td>
      <td>13427</td>
      <td>2128</td>
      <td>0.007423</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>RETURNS</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>2107</td>
      <td>13427</td>
      <td>649</td>
      <td>0.024179</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Java, ByteCode, Constructor, Method, Member]</td>
      <td>HAS</td>
      <td>[Java, ByteCode, Parameter]</td>
      <td>2075</td>
      <td>2128</td>
      <td>13293</td>
      <td>0.007335</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>OF_GENERIC_TYPE</td>
      <td>[Java, ByteCode, Bound]</td>
      <td>2061</td>
      <td>13293</td>
      <td>7240</td>
      <td>0.002141</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Java, ByteCode, Method, Member, Lambda]</td>
      <td>INVOKES</td>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>1933</td>
      <td>968</td>
      <td>13427</td>
      <td>0.014872</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 354636
    total_number_of_relationships (edges): 1100439
    -> total directed graph density: 8.74986915199027e-06
    -> total directed graph density in percent: 0.000874986915199027

