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
      <td>178996</td>
      <td>49.272594</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change, Create]</td>
      <td>53059</td>
      <td>14.605659</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change, Delete]</td>
      <td>28004</td>
      <td>7.708718</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>13451</td>
      <td>3.702684</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>13293</td>
      <td>3.659191</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Commit]</td>
      <td>13149</td>
      <td>3.619552</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[File, Git]</td>
      <td>11241</td>
      <td>3.094333</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Change, Rename]</td>
      <td>10854</td>
      <td>2.987803</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Java, ByteCode, ParameterizedType, Bound]</td>
      <td>7279</td>
      <td>2.003705</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Java, ByteCode, Bound]</td>
      <td>7240</td>
      <td>1.992970</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>3604</td>
      <td>0.992080</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Java, ByteCode, Bound, WildcardType]</td>
      <td>2947</td>
      <td>0.811227</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Value, Java, ByteCode, Annotation]</td>
      <td>2931</td>
      <td>0.806822</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Xml, Element]</td>
      <td>2162</td>
      <td>0.595138</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Java, ByteCode, Member, Method, Constructor]</td>
      <td>2109</td>
      <td>0.580549</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Xml, Text]</td>
      <td>1450</td>
      <td>0.399144</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Java, ByteCode, Bound, TypeVariable]</td>
      <td>1111</td>
      <td>0.305827</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Java, ByteCode, Member, Method, Lambda]</td>
      <td>968</td>
      <td>0.266463</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, File, Java, ByteCode, ResolvedDuplicate...</td>
      <td>888</td>
      <td>0.244442</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Type, File, Java, ByteCode, Class]</td>
      <td>846</td>
      <td>0.232880</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Json, Key]</td>
      <td>702</td>
      <td>0.193241</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Json, Value, Scalar]</td>
      <td>685</td>
      <td>0.188561</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Value, Java, ByteCode, Primitive]</td>
      <td>672</td>
      <td>0.184983</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>649</td>
      <td>0.178652</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Java, ByteCode, Member, Method, GenericDeclar...</td>
      <td>578</td>
      <td>0.159107</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, File, Java, ByteCode, ExternalType]</td>
      <td>411</td>
      <td>0.113137</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Git, Change, Copy]</td>
      <td>342</td>
      <td>0.094143</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Author, Git, Person]</td>
      <td>299</td>
      <td>0.082306</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Value, Array]</td>
      <td>287</td>
      <td>0.079003</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Committer, Git, Person]</td>
      <td>252</td>
      <td>0.069369</td>
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
      <td>0.000275</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Package, File, Json, NPM]</td>
      <td>1</td>
      <td>0.000275</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000275</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[File, TS, Scan]</td>
      <td>1</td>
      <td>0.000275</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Json]</td>
      <td>2</td>
      <td>0.000551</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[File]</td>
      <td>3</td>
      <td>0.000826</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Java, ByteCode, Member, Method, GenericDeclar...</td>
      <td>4</td>
      <td>0.001101</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Maven, Exclusion]</td>
      <td>5</td>
      <td>0.001376</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Json, Value, Array]</td>
      <td>6</td>
      <td>0.001652</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[NPM, Dependency]</td>
      <td>7</td>
      <td>0.001927</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Type, File, Java, ByteCode, Void]</td>
      <td>9</td>
      <td>0.002477</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[File, Maven, Xml, Pom, Document]</td>
      <td>9</td>
      <td>0.002477</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Java, ManifestSection]</td>
      <td>9</td>
      <td>0.002477</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[File, Java, Manifest]</td>
      <td>9</td>
      <td>0.002477</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[File, Artifact, Jar, Archive, Zip, Java]</td>
      <td>9</td>
      <td>0.002477</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[File, Java, ServiceLoader]</td>
      <td>10</td>
      <td>0.002753</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[File, Java, Properties]</td>
      <td>12</td>
      <td>0.003303</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Maven, ExecutionGoal]</td>
      <td>16</td>
      <td>0.004404</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Maven, PluginExecution]</td>
      <td>16</td>
      <td>0.004404</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Xml, Attribute]</td>
      <td>18</td>
      <td>0.004955</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[jQAssistant, Rule, Concept]</td>
      <td>19</td>
      <td>0.005230</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Type, File, Java, ByteCode, Throwable, Extern...</td>
      <td>21</td>
      <td>0.005781</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Maven, Configuration]</td>
      <td>21</td>
      <td>0.005781</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Maven, Plugin]</td>
      <td>21</td>
      <td>0.005781</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, File, Java, ByteCode, Throwable, Resolv...</td>
      <td>22</td>
      <td>0.006056</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, File, Java, ByteCode, Enum]</td>
      <td>28</td>
      <td>0.007708</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Git, Branch]</td>
      <td>30</td>
      <td>0.008258</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Type, File, Java, ByteCode, PrimitiveType]</td>
      <td>30</td>
      <td>0.008258</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Xml, Namespace]</td>
      <td>36</td>
      <td>0.009910</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Type, File, Java, ByteCode, Annotation]</td>
      <td>44</td>
      <td>0.012112</td>
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
      <td>296398</td>
      <td>81.590081</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>271255</td>
      <td>74.668917</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Update</td>
      <td>178996</td>
      <td>49.272594</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Java</td>
      <td>60600</td>
      <td>16.681485</td>
    </tr>
    <tr>
      <th>4</th>
      <td>ByteCode</td>
      <td>60410</td>
      <td>16.629184</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Create</td>
      <td>53059</td>
      <td>14.605659</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Delete</td>
      <td>28004</td>
      <td>7.708718</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Member</td>
      <td>20714</td>
      <td>5.701985</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Bound</td>
      <td>18743</td>
      <td>5.159424</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Method</td>
      <td>17110</td>
      <td>4.709905</td>
    </tr>
    <tr>
      <th>10</th>
      <td>File</td>
      <td>15202</td>
      <td>4.184686</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Parameter</td>
      <td>13293</td>
      <td>3.659191</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Commit</td>
      <td>13149</td>
      <td>3.619552</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Rename</td>
      <td>10854</td>
      <td>2.987803</td>
    </tr>
    <tr>
      <th>14</th>
      <td>ParameterizedType</td>
      <td>7279</td>
      <td>2.003705</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Value</td>
      <td>5428</td>
      <td>1.494177</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Type</td>
      <td>3715</td>
      <td>1.022636</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Xml</td>
      <td>3675</td>
      <td>1.011625</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Field</td>
      <td>3604</td>
      <td>0.992080</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Annotation</td>
      <td>2975</td>
      <td>0.818934</td>
    </tr>
    <tr>
      <th>20</th>
      <td>WildcardType</td>
      <td>2947</td>
      <td>0.811227</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Element</td>
      <td>2162</td>
      <td>0.595138</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Constructor</td>
      <td>2113</td>
      <td>0.581650</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Json</td>
      <td>1570</td>
      <td>0.432177</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Text</td>
      <td>1450</td>
      <td>0.399144</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Class</td>
      <td>1327</td>
      <td>0.365286</td>
    </tr>
    <tr>
      <th>26</th>
      <td>TypeVariable</td>
      <td>1111</td>
      <td>0.305827</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Lambda</td>
      <td>968</td>
      <td>0.266463</td>
    </tr>
    <tr>
      <th>28</th>
      <td>ResolvedDuplicateType</td>
      <td>910</td>
      <td>0.250498</td>
    </tr>
    <tr>
      <th>29</th>
      <td>GenericDeclaration</td>
      <td>904</td>
      <td>0.248846</td>
    </tr>
    <tr>
      <th>30</th>
      <td>JavaType</td>
      <td>754</td>
      <td>0.207555</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Key</td>
      <td>702</td>
      <td>0.193241</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Scalar</td>
      <td>685</td>
      <td>0.188561</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Primitive</td>
      <td>672</td>
      <td>0.184983</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Person</td>
      <td>551</td>
      <td>0.151675</td>
    </tr>
    <tr>
      <th>35</th>
      <td>ExternalType</td>
      <td>527</td>
      <td>0.145068</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Maven</td>
      <td>346</td>
      <td>0.095244</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Copy</td>
      <td>342</td>
      <td>0.094143</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Author</td>
      <td>299</td>
      <td>0.082306</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Array</td>
      <td>293</td>
      <td>0.080655</td>
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

    Total number of relationships: 1127591





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
      <td>271255</td>
      <td>24.056152</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>271255</td>
      <td>24.056152</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>178996</td>
      <td>15.874196</td>
    </tr>
    <tr>
      <th>3</th>
      <td>CREATES</td>
      <td>64255</td>
      <td>5.698431</td>
    </tr>
    <tr>
      <th>4</th>
      <td>DELETES</td>
      <td>38858</td>
      <td>3.446108</td>
    </tr>
    <tr>
      <th>5</th>
      <td>INVOKES</td>
      <td>36425</td>
      <td>3.230338</td>
    </tr>
    <tr>
      <th>6</th>
      <td>COMMITTED</td>
      <td>26298</td>
      <td>2.332229</td>
    </tr>
    <tr>
      <th>7</th>
      <td>DEPENDS_ON</td>
      <td>22492</td>
      <td>1.994695</td>
    </tr>
    <tr>
      <th>8</th>
      <td>OF_TYPE</td>
      <td>21920</td>
      <td>1.943967</td>
    </tr>
    <tr>
      <th>9</th>
      <td>DECLARES</td>
      <td>21175</td>
      <td>1.877897</td>
    </tr>
    <tr>
      <th>10</th>
      <td>OF_RAW_TYPE</td>
      <td>17353</td>
      <td>1.538945</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_PARENT</td>
      <td>15955</td>
      <td>1.414963</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS</td>
      <td>14429</td>
      <td>1.279631</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_COMMIT</td>
      <td>13149</td>
      <td>1.166114</td>
    </tr>
    <tr>
      <th>14</th>
      <td>RETURNS</td>
      <td>12844</td>
      <td>1.139065</td>
    </tr>
    <tr>
      <th>15</th>
      <td>HAS_FILE</td>
      <td>11241</td>
      <td>0.996904</td>
    </tr>
    <tr>
      <th>16</th>
      <td>RENAMES</td>
      <td>10854</td>
      <td>0.962583</td>
    </tr>
    <tr>
      <th>17</th>
      <td>READS</td>
      <td>9379</td>
      <td>0.831773</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>8407</td>
      <td>0.745572</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_NEW_NAME</td>
      <td>6344</td>
      <td>0.562615</td>
    </tr>
    <tr>
      <th>20</th>
      <td>OF_GENERIC_TYPE</td>
      <td>5996</td>
      <td>0.531753</td>
    </tr>
    <tr>
      <th>21</th>
      <td>RESOLVES_TO</td>
      <td>5235</td>
      <td>0.464264</td>
    </tr>
    <tr>
      <th>22</th>
      <td>SIMILAR</td>
      <td>4078</td>
      <td>0.361656</td>
    </tr>
    <tr>
      <th>23</th>
      <td>WRITES</td>
      <td>3944</td>
      <td>0.349772</td>
    </tr>
    <tr>
      <th>24</th>
      <td>CONTAINS</td>
      <td>3936</td>
      <td>0.349063</td>
    </tr>
    <tr>
      <th>25</th>
      <td>RETURNS_GENERIC</td>
      <td>3593</td>
      <td>0.318644</td>
    </tr>
    <tr>
      <th>26</th>
      <td>ANNOTATED_BY</td>
      <td>2919</td>
      <td>0.258870</td>
    </tr>
    <tr>
      <th>27</th>
      <td>REQUIRES</td>
      <td>2230</td>
      <td>0.197767</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_FIRST_CHILD</td>
      <td>2162</td>
      <td>0.191736</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_LAST_CHILD</td>
      <td>2162</td>
      <td>0.191736</td>
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
      <td>0.000089</td>
    </tr>
    <tr>
      <th>1</th>
      <td>THROWS_GENERIC</td>
      <td>5</td>
      <td>0.000443</td>
    </tr>
    <tr>
      <th>2</th>
      <td>EXCLUDES</td>
      <td>5</td>
      <td>0.000443</td>
    </tr>
    <tr>
      <th>3</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>7</td>
      <td>0.000621</td>
    </tr>
    <tr>
      <th>4</th>
      <td>DESCRIBES</td>
      <td>9</td>
      <td>0.000798</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_ROOT_ELEMENT</td>
      <td>11</td>
      <td>0.000976</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_GOAL</td>
      <td>16</td>
      <td>0.001419</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_EXECUTION</td>
      <td>16</td>
      <td>0.001419</td>
    </tr>
    <tr>
      <th>8</th>
      <td>OF_NAMESPACE</td>
      <td>18</td>
      <td>0.001596</td>
    </tr>
    <tr>
      <th>9</th>
      <td>HAS_ATTRIBUTE</td>
      <td>18</td>
      <td>0.001596</td>
    </tr>
    <tr>
      <th>10</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.001685</td>
    </tr>
    <tr>
      <th>11</th>
      <td>IS_ARTIFACT</td>
      <td>21</td>
      <td>0.001862</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS_CONFIGURATION</td>
      <td>21</td>
      <td>0.001862</td>
    </tr>
    <tr>
      <th>13</th>
      <td>USES_PLUGIN</td>
      <td>21</td>
      <td>0.001862</td>
    </tr>
    <tr>
      <th>14</th>
      <td>REQUIRES_TYPE_PARAMETER</td>
      <td>24</td>
      <td>0.002128</td>
    </tr>
    <tr>
      <th>15</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.002483</td>
    </tr>
    <tr>
      <th>16</th>
      <td>HAS_BRANCH</td>
      <td>30</td>
      <td>0.002661</td>
    </tr>
    <tr>
      <th>17</th>
      <td>HAS_HEAD</td>
      <td>31</td>
      <td>0.002749</td>
    </tr>
    <tr>
      <th>18</th>
      <td>DECLARES_NAMESPACE</td>
      <td>36</td>
      <td>0.003193</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_DEFAULT</td>
      <td>39</td>
      <td>0.003459</td>
    </tr>
    <tr>
      <th>20</th>
      <td>COPY_OF</td>
      <td>132</td>
      <td>0.011706</td>
    </tr>
    <tr>
      <th>21</th>
      <td>CONTAINS_VALUE</td>
      <td>160</td>
      <td>0.014190</td>
    </tr>
    <tr>
      <th>22</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>165</td>
      <td>0.014633</td>
    </tr>
    <tr>
      <th>23</th>
      <td>TO_ARTIFACT</td>
      <td>165</td>
      <td>0.014633</td>
    </tr>
    <tr>
      <th>24</th>
      <td>HAS_COMPONENT_TYPE</td>
      <td>166</td>
      <td>0.014722</td>
    </tr>
    <tr>
      <th>25</th>
      <td>ON_COMMIT</td>
      <td>171</td>
      <td>0.015165</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_TAG</td>
      <td>171</td>
      <td>0.015165</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_COMMITTER</td>
      <td>252</td>
      <td>0.022349</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_AUTHOR</td>
      <td>299</td>
      <td>0.026517</td>
    </tr>
    <tr>
      <th>29</th>
      <td>COPIES</td>
      <td>342</td>
      <td>0.030330</td>
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
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>178996</td>
      <td>178996</td>
      <td>11241</td>
      <td>0.008896</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Update, Change]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>178996</td>
      <td>178996</td>
      <td>11241</td>
      <td>0.008896</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Update, Change]</td>
      <td>178996</td>
      <td>13149</td>
      <td>178996</td>
      <td>0.007605</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>53059</td>
      <td>13149</td>
      <td>53059</td>
      <td>0.007605</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>53059</td>
      <td>53059</td>
      <td>11241</td>
      <td>0.008896</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>53059</td>
      <td>53059</td>
      <td>11241</td>
      <td>0.008896</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>28004</td>
      <td>13149</td>
      <td>28004</td>
      <td>0.007605</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>28004</td>
      <td>28004</td>
      <td>11241</td>
      <td>0.008896</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>28004</td>
      <td>28004</td>
      <td>11241</td>
      <td>0.008896</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>INVOKES</td>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>22175</td>
      <td>13349</td>
      <td>13349</td>
      <td>0.012444</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>15946</td>
      <td>13149</td>
      <td>13149</td>
      <td>0.009223</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>13149</td>
      <td>1</td>
      <td>13149</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>13149</td>
      <td>252</td>
      <td>13149</td>
      <td>0.396825</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>13149</td>
      <td>299</td>
      <td>13149</td>
      <td>0.334448</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>11241</td>
      <td>1</td>
      <td>11241</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>10854</td>
      <td>13149</td>
      <td>10854</td>
      <td>0.007605</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>10854</td>
      <td>10854</td>
      <td>11241</td>
      <td>0.008896</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>10854</td>
      <td>10854</td>
      <td>11241</td>
      <td>0.008896</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>10854</td>
      <td>10854</td>
      <td>11241</td>
      <td>0.008896</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>10854</td>
      <td>10854</td>
      <td>11241</td>
      <td>0.008896</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>HAS</td>
      <td>[Java, ByteCode, Parameter]</td>
      <td>8500</td>
      <td>13349</td>
      <td>13293</td>
      <td>0.004790</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>READS</td>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>8444</td>
      <td>13349</td>
      <td>3604</td>
      <td>0.017552</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>6344</td>
      <td>11241</td>
      <td>11241</td>
      <td>0.005021</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>OF_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>6156</td>
      <td>13293</td>
      <td>649</td>
      <td>0.071356</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Java, ByteCode, Bound]</td>
      <td>OF_RAW_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>3465</td>
      <td>7240</td>
      <td>649</td>
      <td>0.073743</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Java, ByteCode, ParameterizedType, Bound]</td>
      <td>OF_RAW_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>3110</td>
      <td>7279</td>
      <td>649</td>
      <td>0.065833</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Java, ByteCode, ParameterizedType, Bound]</td>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>[Java, ByteCode, Bound, WildcardType]</td>
      <td>2947</td>
      <td>7279</td>
      <td>2947</td>
      <td>0.013738</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>OF_GENERIC_TYPE</td>
      <td>[Java, ByteCode, ParameterizedType, Bound]</td>
      <td>2695</td>
      <td>13293</td>
      <td>7279</td>
      <td>0.002785</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Java, ByteCode, Member, Method, Constructor]</td>
      <td>WRITES</td>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>2519</td>
      <td>2109</td>
      <td>3604</td>
      <td>0.033141</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Java, ByteCode, ParameterizedType, Bound]</td>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>[Java, ByteCode, Bound, TypeVariable]</td>
      <td>2474</td>
      <td>7279</td>
      <td>1111</td>
      <td>0.030592</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 363277
    total_number_of_relationships (edges): 1127591
    -> total directed graph density: 8.544309894940536e-06
    -> total directed graph density in percent: 0.0008544309894940536

