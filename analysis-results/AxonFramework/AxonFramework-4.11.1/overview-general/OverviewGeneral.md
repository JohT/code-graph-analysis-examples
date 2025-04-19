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
      <td>138637</td>
      <td>46.084372</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change, Create]</td>
      <td>44924</td>
      <td>14.933202</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change, Delete]</td>
      <td>22780</td>
      <td>7.572308</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>13482</td>
      <td>4.481556</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>13293</td>
      <td>4.418731</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Commit]</td>
      <td>11339</td>
      <td>3.769201</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[File, Git]</td>
      <td>8285</td>
      <td>2.754020</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
      <td>7279</td>
      <td>2.419615</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Java, ByteCode, Bound]</td>
      <td>7240</td>
      <td>2.406651</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Git, Change, Rename]</td>
      <td>7018</td>
      <td>2.332856</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>3605</td>
      <td>1.198339</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Java, ByteCode, Bound, WildcardType]</td>
      <td>2947</td>
      <td>0.979613</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Java, Value, ByteCode, Annotation]</td>
      <td>2931</td>
      <td>0.974295</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Xml, Element]</td>
      <td>2162</td>
      <td>0.718671</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Java, ByteCode, Constructor, Method, Member]</td>
      <td>2113</td>
      <td>0.702383</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Xml, Text]</td>
      <td>1450</td>
      <td>0.481995</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Java, ByteCode, TypeVariable, Bound]</td>
      <td>1111</td>
      <td>0.369308</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Java, ByteCode, Method, Member, Lambda]</td>
      <td>968</td>
      <td>0.321773</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, File, Java, ByteCode, ResolvedDuplicate...</td>
      <td>888</td>
      <td>0.295180</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Type, File, Java, ByteCode, Class]</td>
      <td>846</td>
      <td>0.281219</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Json, Key]</td>
      <td>694</td>
      <td>0.230693</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Value, Json, Scalar]</td>
      <td>678</td>
      <td>0.225374</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Java, Value, ByteCode, Primitive]</td>
      <td>672</td>
      <td>0.223380</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>649</td>
      <td>0.215734</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Java, ByteCode, Method, Member, GenericDeclar...</td>
      <td>578</td>
      <td>0.192133</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, File, Java, ByteCode, ExternalType]</td>
      <td>411</td>
      <td>0.136621</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Git, Change, Copy]</td>
      <td>298</td>
      <td>0.099058</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Author, Git, Person]</td>
      <td>295</td>
      <td>0.098061</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Value, Array]</td>
      <td>287</td>
      <td>0.095402</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Committer, Git, Person]</td>
      <td>242</td>
      <td>0.080443</td>
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
      <td>0.000332</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Branch]</td>
      <td>1</td>
      <td>0.000332</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000332</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[File, Json]</td>
      <td>2</td>
      <td>0.000665</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File]</td>
      <td>3</td>
      <td>0.000997</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Java, ByteCode, Constructor, Method, Member, ...</td>
      <td>4</td>
      <td>0.001330</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Maven, Exclusion]</td>
      <td>5</td>
      <td>0.001662</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Value, Array, Json]</td>
      <td>6</td>
      <td>0.001994</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Type, File, Java, ByteCode, Void]</td>
      <td>9</td>
      <td>0.002992</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[File, Maven, Xml, Pom, Document]</td>
      <td>9</td>
      <td>0.002992</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Java, ManifestSection]</td>
      <td>9</td>
      <td>0.002992</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[File, Artifact, Jar, Archive, Zip, Java]</td>
      <td>9</td>
      <td>0.002992</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[File, Java, Manifest]</td>
      <td>9</td>
      <td>0.002992</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[File, Java, ServiceLoader]</td>
      <td>10</td>
      <td>0.003324</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[File, Java, Properties]</td>
      <td>12</td>
      <td>0.003989</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Maven, ExecutionGoal]</td>
      <td>16</td>
      <td>0.005319</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Maven, PluginExecution]</td>
      <td>16</td>
      <td>0.005319</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Xml, Attribute]</td>
      <td>18</td>
      <td>0.005983</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[jQAssistant, Rule, Concept]</td>
      <td>19</td>
      <td>0.006316</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Maven, Plugin]</td>
      <td>21</td>
      <td>0.006981</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Maven, Configuration]</td>
      <td>21</td>
      <td>0.006981</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Type, File, Java, ByteCode, Throwable, Extern...</td>
      <td>21</td>
      <td>0.006981</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Type, File, Java, ByteCode, Throwable, Resolv...</td>
      <td>22</td>
      <td>0.007313</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, File, Java, ByteCode, Enum]</td>
      <td>28</td>
      <td>0.009307</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, File, Java, ByteCode, PrimitiveType]</td>
      <td>30</td>
      <td>0.009972</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Xml, Namespace]</td>
      <td>36</td>
      <td>0.011967</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, File, Java, ByteCode, Annotation]</td>
      <td>44</td>
      <td>0.014626</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[File, Directory]</td>
      <td>44</td>
      <td>0.014626</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Type, File, Java, ByteCode, Class, Throwable]</td>
      <td>55</td>
      <td>0.018283</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Type, File, Java, ByteCode, GenericDeclaratio...</td>
      <td>85</td>
      <td>0.028255</td>
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
      <td>233948</td>
      <td>77.766734</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>213657</td>
      <td>71.021796</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Update</td>
      <td>138637</td>
      <td>46.084372</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Java</td>
      <td>60636</td>
      <td>20.156033</td>
    </tr>
    <tr>
      <th>4</th>
      <td>ByteCode</td>
      <td>60446</td>
      <td>20.092875</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Create</td>
      <td>44924</td>
      <td>14.933202</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Delete</td>
      <td>22780</td>
      <td>7.572308</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Member</td>
      <td>20750</td>
      <td>6.897515</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Bound</td>
      <td>18743</td>
      <td>6.230367</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Method</td>
      <td>17145</td>
      <td>5.699175</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Parameter</td>
      <td>13293</td>
      <td>4.418731</td>
    </tr>
    <tr>
      <th>11</th>
      <td>File</td>
      <td>12240</td>
      <td>4.068703</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Commit</td>
      <td>11339</td>
      <td>3.769201</td>
    </tr>
    <tr>
      <th>13</th>
      <td>ParameterizedType</td>
      <td>7279</td>
      <td>2.419615</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Rename</td>
      <td>7018</td>
      <td>2.332856</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Value</td>
      <td>5419</td>
      <td>1.801332</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Type</td>
      <td>3715</td>
      <td>1.234904</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Xml</td>
      <td>3675</td>
      <td>1.221608</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Field</td>
      <td>3605</td>
      <td>1.198339</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Annotation</td>
      <td>2975</td>
      <td>0.988921</td>
    </tr>
    <tr>
      <th>20</th>
      <td>WildcardType</td>
      <td>2947</td>
      <td>0.979613</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Element</td>
      <td>2162</td>
      <td>0.718671</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Constructor</td>
      <td>2117</td>
      <td>0.703713</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Json</td>
      <td>1552</td>
      <td>0.515901</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Text</td>
      <td>1450</td>
      <td>0.481995</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Class</td>
      <td>1327</td>
      <td>0.441109</td>
    </tr>
    <tr>
      <th>26</th>
      <td>TypeVariable</td>
      <td>1111</td>
      <td>0.369308</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Lambda</td>
      <td>968</td>
      <td>0.321773</td>
    </tr>
    <tr>
      <th>28</th>
      <td>ResolvedDuplicateType</td>
      <td>910</td>
      <td>0.302493</td>
    </tr>
    <tr>
      <th>29</th>
      <td>GenericDeclaration</td>
      <td>904</td>
      <td>0.300499</td>
    </tr>
    <tr>
      <th>30</th>
      <td>JavaType</td>
      <td>754</td>
      <td>0.250637</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Key</td>
      <td>694</td>
      <td>0.230693</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Scalar</td>
      <td>678</td>
      <td>0.225374</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Primitive</td>
      <td>672</td>
      <td>0.223380</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Person</td>
      <td>537</td>
      <td>0.178504</td>
    </tr>
    <tr>
      <th>35</th>
      <td>ExternalType</td>
      <td>527</td>
      <td>0.175180</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Maven</td>
      <td>346</td>
      <td>0.115014</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Copy</td>
      <td>298</td>
      <td>0.099058</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Author</td>
      <td>295</td>
      <td>0.098061</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Array</td>
      <td>293</td>
      <td>0.097396</td>
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

    Total number of relationships: 935189





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
      <td>213657</td>
      <td>22.846398</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>213657</td>
      <td>22.846398</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>138637</td>
      <td>14.824490</td>
    </tr>
    <tr>
      <th>3</th>
      <td>CREATES</td>
      <td>52240</td>
      <td>5.586037</td>
    </tr>
    <tr>
      <th>4</th>
      <td>INVOKES</td>
      <td>36786</td>
      <td>3.933536</td>
    </tr>
    <tr>
      <th>5</th>
      <td>DELETES</td>
      <td>29798</td>
      <td>3.186308</td>
    </tr>
    <tr>
      <th>6</th>
      <td>COMMITTED</td>
      <td>22678</td>
      <td>2.424964</td>
    </tr>
    <tr>
      <th>7</th>
      <td>DEPENDS_ON</td>
      <td>22492</td>
      <td>2.405075</td>
    </tr>
    <tr>
      <th>8</th>
      <td>OF_TYPE</td>
      <td>21920</td>
      <td>2.343911</td>
    </tr>
    <tr>
      <th>9</th>
      <td>DECLARES</td>
      <td>21211</td>
      <td>2.268098</td>
    </tr>
    <tr>
      <th>10</th>
      <td>OF_RAW_TYPE</td>
      <td>17353</td>
      <td>1.855561</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS</td>
      <td>14429</td>
      <td>1.542897</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS_PARENT</td>
      <td>13858</td>
      <td>1.481839</td>
    </tr>
    <tr>
      <th>13</th>
      <td>RETURNS</td>
      <td>12844</td>
      <td>1.373412</td>
    </tr>
    <tr>
      <th>14</th>
      <td>HAS_COMMIT</td>
      <td>11339</td>
      <td>1.212482</td>
    </tr>
    <tr>
      <th>15</th>
      <td>READS</td>
      <td>9379</td>
      <td>1.002899</td>
    </tr>
    <tr>
      <th>16</th>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>8407</td>
      <td>0.898963</td>
    </tr>
    <tr>
      <th>17</th>
      <td>HAS_FILE</td>
      <td>8285</td>
      <td>0.885917</td>
    </tr>
    <tr>
      <th>18</th>
      <td>RENAMES</td>
      <td>7018</td>
      <td>0.750437</td>
    </tr>
    <tr>
      <th>19</th>
      <td>OF_GENERIC_TYPE</td>
      <td>5996</td>
      <td>0.641154</td>
    </tr>
    <tr>
      <th>20</th>
      <td>RESOLVES_TO</td>
      <td>4234</td>
      <td>0.452743</td>
    </tr>
    <tr>
      <th>21</th>
      <td>SIMILAR</td>
      <td>4078</td>
      <td>0.436062</td>
    </tr>
    <tr>
      <th>22</th>
      <td>WRITES</td>
      <td>3944</td>
      <td>0.421733</td>
    </tr>
    <tr>
      <th>23</th>
      <td>CONTAINS</td>
      <td>3926</td>
      <td>0.419808</td>
    </tr>
    <tr>
      <th>24</th>
      <td>HAS_NEW_NAME</td>
      <td>3662</td>
      <td>0.391579</td>
    </tr>
    <tr>
      <th>25</th>
      <td>RETURNS_GENERIC</td>
      <td>3593</td>
      <td>0.384200</td>
    </tr>
    <tr>
      <th>26</th>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>3027</td>
      <td>0.323678</td>
    </tr>
    <tr>
      <th>27</th>
      <td>ANNOTATED_BY</td>
      <td>2919</td>
      <td>0.312129</td>
    </tr>
    <tr>
      <th>28</th>
      <td>REQUIRES</td>
      <td>2230</td>
      <td>0.238454</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_FIRST_CHILD</td>
      <td>2162</td>
      <td>0.231183</td>
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
      <td>0.000107</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HAS_BRANCH</td>
      <td>1</td>
      <td>0.000107</td>
    </tr>
    <tr>
      <th>2</th>
      <td>HAS_HEAD</td>
      <td>2</td>
      <td>0.000214</td>
    </tr>
    <tr>
      <th>3</th>
      <td>THROWS_GENERIC</td>
      <td>5</td>
      <td>0.000535</td>
    </tr>
    <tr>
      <th>4</th>
      <td>EXCLUDES</td>
      <td>5</td>
      <td>0.000535</td>
    </tr>
    <tr>
      <th>5</th>
      <td>DESCRIBES</td>
      <td>9</td>
      <td>0.000962</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_ROOT_ELEMENT</td>
      <td>11</td>
      <td>0.001176</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_GOAL</td>
      <td>16</td>
      <td>0.001711</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_EXECUTION</td>
      <td>16</td>
      <td>0.001711</td>
    </tr>
    <tr>
      <th>9</th>
      <td>OF_NAMESPACE</td>
      <td>18</td>
      <td>0.001925</td>
    </tr>
    <tr>
      <th>10</th>
      <td>HAS_ATTRIBUTE</td>
      <td>18</td>
      <td>0.001925</td>
    </tr>
    <tr>
      <th>11</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.002032</td>
    </tr>
    <tr>
      <th>12</th>
      <td>USES_PLUGIN</td>
      <td>21</td>
      <td>0.002246</td>
    </tr>
    <tr>
      <th>13</th>
      <td>IS_ARTIFACT</td>
      <td>21</td>
      <td>0.002246</td>
    </tr>
    <tr>
      <th>14</th>
      <td>HAS_CONFIGURATION</td>
      <td>21</td>
      <td>0.002246</td>
    </tr>
    <tr>
      <th>15</th>
      <td>REQUIRES_TYPE_PARAMETER</td>
      <td>24</td>
      <td>0.002566</td>
    </tr>
    <tr>
      <th>16</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.002994</td>
    </tr>
    <tr>
      <th>17</th>
      <td>DECLARES_NAMESPACE</td>
      <td>36</td>
      <td>0.003849</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_DEFAULT</td>
      <td>39</td>
      <td>0.004170</td>
    </tr>
    <tr>
      <th>19</th>
      <td>COPY_OF</td>
      <td>119</td>
      <td>0.012725</td>
    </tr>
    <tr>
      <th>20</th>
      <td>HAS_TAG</td>
      <td>128</td>
      <td>0.013687</td>
    </tr>
    <tr>
      <th>21</th>
      <td>ON_COMMIT</td>
      <td>128</td>
      <td>0.013687</td>
    </tr>
    <tr>
      <th>22</th>
      <td>CONTAINS_VALUE</td>
      <td>160</td>
      <td>0.017109</td>
    </tr>
    <tr>
      <th>23</th>
      <td>TO_ARTIFACT</td>
      <td>165</td>
      <td>0.017643</td>
    </tr>
    <tr>
      <th>24</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>165</td>
      <td>0.017643</td>
    </tr>
    <tr>
      <th>25</th>
      <td>HAS_COMPONENT_TYPE</td>
      <td>166</td>
      <td>0.017750</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_COMMITTER</td>
      <td>242</td>
      <td>0.025877</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_AUTHOR</td>
      <td>295</td>
      <td>0.031544</td>
    </tr>
    <tr>
      <th>28</th>
      <td>COPIES</td>
      <td>298</td>
      <td>0.031865</td>
    </tr>
    <tr>
      <th>29</th>
      <td>IMPLEMENTS_GENERIC</td>
      <td>378</td>
      <td>0.040420</td>
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
      <td>138637</td>
      <td>138637</td>
      <td>8285</td>
      <td>0.012070</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Update, Change]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>138637</td>
      <td>138637</td>
      <td>8285</td>
      <td>0.012070</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Update, Change]</td>
      <td>138637</td>
      <td>11339</td>
      <td>138637</td>
      <td>0.008819</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>44924</td>
      <td>44924</td>
      <td>8285</td>
      <td>0.012070</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>44924</td>
      <td>44924</td>
      <td>8285</td>
      <td>0.012070</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>44924</td>
      <td>11339</td>
      <td>44924</td>
      <td>0.008819</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>22780</td>
      <td>11339</td>
      <td>22780</td>
      <td>0.008819</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>22780</td>
      <td>22780</td>
      <td>8285</td>
      <td>0.012070</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>22780</td>
      <td>22780</td>
      <td>8285</td>
      <td>0.012070</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>INVOKES</td>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>22484</td>
      <td>13382</td>
      <td>13382</td>
      <td>0.012555</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>13849</td>
      <td>11339</td>
      <td>11339</td>
      <td>0.010771</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>11339</td>
      <td>1</td>
      <td>11339</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>11339</td>
      <td>295</td>
      <td>11339</td>
      <td>0.338983</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>11339</td>
      <td>242</td>
      <td>11339</td>
      <td>0.413223</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>HAS</td>
      <td>[Java, ByteCode, Parameter]</td>
      <td>8506</td>
      <td>13382</td>
      <td>13293</td>
      <td>0.004782</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Java, ByteCode, Method, Member]</td>
      <td>READS</td>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>8444</td>
      <td>13382</td>
      <td>3605</td>
      <td>0.017503</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>8285</td>
      <td>1</td>
      <td>8285</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>7018</td>
      <td>11339</td>
      <td>7018</td>
      <td>0.008819</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>7018</td>
      <td>7018</td>
      <td>8285</td>
      <td>0.012070</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>7018</td>
      <td>7018</td>
      <td>8285</td>
      <td>0.012070</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>7018</td>
      <td>7018</td>
      <td>8285</td>
      <td>0.012070</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>7018</td>
      <td>7018</td>
      <td>8285</td>
      <td>0.012070</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>OF_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>6156</td>
      <td>13293</td>
      <td>649</td>
      <td>0.071356</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>3662</td>
      <td>8285</td>
      <td>8285</td>
      <td>0.005335</td>
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
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
      <td>OF_RAW_TYPE</td>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>3110</td>
      <td>7279</td>
      <td>649</td>
      <td>0.065833</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
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
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
      <td>2695</td>
      <td>13293</td>
      <td>7279</td>
      <td>0.002785</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Java, ByteCode, Constructor, Method, Member]</td>
      <td>WRITES</td>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>2519</td>
      <td>2113</td>
      <td>3605</td>
      <td>0.033069</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>[Java, ByteCode, TypeVariable, Bound]</td>
      <td>2474</td>
      <td>7279</td>
      <td>1111</td>
      <td>0.030592</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 300833
    total_number_of_relationships (edges): 935189
    -> total directed graph density: 1.0333558066791313e-05
    -> total directed graph density in percent: 0.0010333558066791314

