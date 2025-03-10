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
      <td>176097</td>
      <td>49.092977</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change, Create]</td>
      <td>51952</td>
      <td>14.483372</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change, Delete]</td>
      <td>27797</td>
      <td>7.749351</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>13494</td>
      <td>3.761908</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Java, ByteCode, Parameter]</td>
      <td>13293</td>
      <td>3.705872</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Commit]</td>
      <td>13137</td>
      <td>3.662382</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[File, Git]</td>
      <td>11022</td>
      <td>3.072754</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Change, Rename]</td>
      <td>10655</td>
      <td>2.970441</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
      <td>7279</td>
      <td>2.029267</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Java, ByteCode, Bound]</td>
      <td>7240</td>
      <td>2.018394</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>3609</td>
      <td>1.006130</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Java, ByteCode, Bound, WildcardType]</td>
      <td>2947</td>
      <td>0.821576</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Java, Value, ByteCode, Annotation]</td>
      <td>2931</td>
      <td>0.817115</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Xml, Element]</td>
      <td>2162</td>
      <td>0.602730</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Java, ByteCode, Member, Method, Constructor]</td>
      <td>2120</td>
      <td>0.591021</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Xml, Text]</td>
      <td>1450</td>
      <td>0.404236</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Java, ByteCode, Bound, TypeVariable]</td>
      <td>1111</td>
      <td>0.309729</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Java, ByteCode, Member, Method, Lambda]</td>
      <td>968</td>
      <td>0.269863</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, File, Java, ByteCode, ResolvedDuplicate...</td>
      <td>888</td>
      <td>0.247560</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Type, File, Java, ByteCode, Class]</td>
      <td>846</td>
      <td>0.235851</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Json, Key]</td>
      <td>702</td>
      <td>0.195706</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Value, Json, Scalar]</td>
      <td>685</td>
      <td>0.190967</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Java, Value, ByteCode, Primitive]</td>
      <td>672</td>
      <td>0.187343</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, File, Java, ByteCode, JavaType]</td>
      <td>649</td>
      <td>0.180931</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Java, ByteCode, Member, Method, GenericDeclar...</td>
      <td>578</td>
      <td>0.161137</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, File, Java, ByteCode, ExternalType]</td>
      <td>411</td>
      <td>0.114580</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Git, Change, Copy]</td>
      <td>334</td>
      <td>0.093114</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Author, Git, Person]</td>
      <td>299</td>
      <td>0.083356</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Value, Array]</td>
      <td>287</td>
      <td>0.080011</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Committer, Git, Person]</td>
      <td>252</td>
      <td>0.070253</td>
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
      <td>0.000279</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Package, File, Json, NPM]</td>
      <td>1</td>
      <td>0.000279</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000279</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[File, TS, Scan]</td>
      <td>1</td>
      <td>0.000279</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Json]</td>
      <td>2</td>
      <td>0.000558</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[File]</td>
      <td>3</td>
      <td>0.000836</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Java, ByteCode, Member, Method, GenericDeclar...</td>
      <td>4</td>
      <td>0.001115</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Maven, Exclusion]</td>
      <td>5</td>
      <td>0.001394</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Value, Array, Json]</td>
      <td>6</td>
      <td>0.001673</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Dependency, NPM]</td>
      <td>7</td>
      <td>0.001951</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Type, File, Java, ByteCode, Void]</td>
      <td>9</td>
      <td>0.002509</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[File, Maven, Xml, Pom, Document]</td>
      <td>9</td>
      <td>0.002509</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Java, ManifestSection]</td>
      <td>9</td>
      <td>0.002509</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[File, Java, Manifest]</td>
      <td>9</td>
      <td>0.002509</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Artifact, File, Jar, Archive, Zip, Java]</td>
      <td>9</td>
      <td>0.002509</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[File, Java, ServiceLoader]</td>
      <td>10</td>
      <td>0.002788</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[File, Java, Properties]</td>
      <td>12</td>
      <td>0.003345</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Maven, ExecutionGoal]</td>
      <td>16</td>
      <td>0.004461</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Maven, PluginExecution]</td>
      <td>16</td>
      <td>0.004461</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Xml, Attribute]</td>
      <td>18</td>
      <td>0.005018</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[jQAssistant, Rule, Concept]</td>
      <td>19</td>
      <td>0.005297</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Type, File, Java, ByteCode, Throwable, Extern...</td>
      <td>21</td>
      <td>0.005854</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Maven, Configuration]</td>
      <td>21</td>
      <td>0.005854</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Maven, Plugin]</td>
      <td>21</td>
      <td>0.005854</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, File, Java, ByteCode, Throwable, Resolv...</td>
      <td>22</td>
      <td>0.006133</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, File, Java, ByteCode, Enum]</td>
      <td>28</td>
      <td>0.007806</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, File, Java, ByteCode, PrimitiveType]</td>
      <td>30</td>
      <td>0.008364</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Xml, Namespace]</td>
      <td>36</td>
      <td>0.010036</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Type, File, Java, ByteCode, Annotation]</td>
      <td>44</td>
      <td>0.012266</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Git, Branch]</td>
      <td>46</td>
      <td>0.012824</td>
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
      <td>291763</td>
      <td>81.338775</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>266835</td>
      <td>74.389255</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Update</td>
      <td>176097</td>
      <td>49.092977</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Java</td>
      <td>60659</td>
      <td>16.910742</td>
    </tr>
    <tr>
      <th>4</th>
      <td>ByteCode</td>
      <td>60469</td>
      <td>16.857773</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Create</td>
      <td>51952</td>
      <td>14.483372</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Delete</td>
      <td>27797</td>
      <td>7.749351</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Member</td>
      <td>20773</td>
      <td>5.791174</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Bound</td>
      <td>18743</td>
      <td>5.225243</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Method</td>
      <td>17164</td>
      <td>4.785044</td>
    </tr>
    <tr>
      <th>10</th>
      <td>File</td>
      <td>14983</td>
      <td>4.177017</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Parameter</td>
      <td>13293</td>
      <td>3.705872</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Commit</td>
      <td>13137</td>
      <td>3.662382</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Rename</td>
      <td>10655</td>
      <td>2.970441</td>
    </tr>
    <tr>
      <th>14</th>
      <td>ParameterizedType</td>
      <td>7279</td>
      <td>2.029267</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Value</td>
      <td>5428</td>
      <td>1.513238</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Type</td>
      <td>3715</td>
      <td>1.035682</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Xml</td>
      <td>3675</td>
      <td>1.024530</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Field</td>
      <td>3609</td>
      <td>1.006130</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Annotation</td>
      <td>2975</td>
      <td>0.829382</td>
    </tr>
    <tr>
      <th>20</th>
      <td>WildcardType</td>
      <td>2947</td>
      <td>0.821576</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Element</td>
      <td>2162</td>
      <td>0.602730</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Constructor</td>
      <td>2124</td>
      <td>0.592137</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Json</td>
      <td>1570</td>
      <td>0.437690</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Text</td>
      <td>1450</td>
      <td>0.404236</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Class</td>
      <td>1327</td>
      <td>0.369946</td>
    </tr>
    <tr>
      <th>26</th>
      <td>TypeVariable</td>
      <td>1111</td>
      <td>0.309729</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Lambda</td>
      <td>968</td>
      <td>0.269863</td>
    </tr>
    <tr>
      <th>28</th>
      <td>ResolvedDuplicateType</td>
      <td>910</td>
      <td>0.253693</td>
    </tr>
    <tr>
      <th>29</th>
      <td>GenericDeclaration</td>
      <td>904</td>
      <td>0.252020</td>
    </tr>
    <tr>
      <th>30</th>
      <td>JavaType</td>
      <td>754</td>
      <td>0.210203</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Key</td>
      <td>702</td>
      <td>0.195706</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Scalar</td>
      <td>685</td>
      <td>0.190967</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Primitive</td>
      <td>672</td>
      <td>0.187343</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Person</td>
      <td>551</td>
      <td>0.153610</td>
    </tr>
    <tr>
      <th>35</th>
      <td>ExternalType</td>
      <td>527</td>
      <td>0.146919</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Maven</td>
      <td>346</td>
      <td>0.096459</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Copy</td>
      <td>334</td>
      <td>0.093114</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Author</td>
      <td>299</td>
      <td>0.083356</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Array</td>
      <td>293</td>
      <td>0.081684</td>
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

    Total number of relationships: 1113059





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
      <td>266835</td>
      <td>23.973123</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>266835</td>
      <td>23.973123</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>176097</td>
      <td>15.820994</td>
    </tr>
    <tr>
      <th>3</th>
      <td>CREATES</td>
      <td>62941</td>
      <td>5.654777</td>
    </tr>
    <tr>
      <th>4</th>
      <td>DELETES</td>
      <td>38452</td>
      <td>3.454624</td>
    </tr>
    <tr>
      <th>5</th>
      <td>INVOKES</td>
      <td>36776</td>
      <td>3.304048</td>
    </tr>
    <tr>
      <th>6</th>
      <td>COMMITTED</td>
      <td>26274</td>
      <td>2.360522</td>
    </tr>
    <tr>
      <th>7</th>
      <td>DEPENDS_ON</td>
      <td>22492</td>
      <td>2.020737</td>
    </tr>
    <tr>
      <th>8</th>
      <td>OF_TYPE</td>
      <td>21920</td>
      <td>1.969348</td>
    </tr>
    <tr>
      <th>9</th>
      <td>DECLARES</td>
      <td>21234</td>
      <td>1.907716</td>
    </tr>
    <tr>
      <th>10</th>
      <td>OF_RAW_TYPE</td>
      <td>17353</td>
      <td>1.559037</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_PARENT</td>
      <td>15893</td>
      <td>1.427867</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS</td>
      <td>14429</td>
      <td>1.296337</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_COMMIT</td>
      <td>13137</td>
      <td>1.180261</td>
    </tr>
    <tr>
      <th>14</th>
      <td>RETURNS</td>
      <td>12844</td>
      <td>1.153937</td>
    </tr>
    <tr>
      <th>15</th>
      <td>HAS_FILE</td>
      <td>11022</td>
      <td>0.990244</td>
    </tr>
    <tr>
      <th>16</th>
      <td>RENAMES</td>
      <td>10655</td>
      <td>0.957272</td>
    </tr>
    <tr>
      <th>17</th>
      <td>READS</td>
      <td>9378</td>
      <td>0.842543</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_ACTUAL_TYPE_ARGUMENT</td>
      <td>8407</td>
      <td>0.755306</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_NEW_NAME</td>
      <td>6270</td>
      <td>0.563312</td>
    </tr>
    <tr>
      <th>20</th>
      <td>OF_GENERIC_TYPE</td>
      <td>5996</td>
      <td>0.538696</td>
    </tr>
    <tr>
      <th>21</th>
      <td>RESOLVES_TO</td>
      <td>5270</td>
      <td>0.473470</td>
    </tr>
    <tr>
      <th>22</th>
      <td>SIMILAR</td>
      <td>4078</td>
      <td>0.366378</td>
    </tr>
    <tr>
      <th>23</th>
      <td>WRITES</td>
      <td>3944</td>
      <td>0.354339</td>
    </tr>
    <tr>
      <th>24</th>
      <td>CONTAINS</td>
      <td>3936</td>
      <td>0.353620</td>
    </tr>
    <tr>
      <th>25</th>
      <td>RETURNS_GENERIC</td>
      <td>3593</td>
      <td>0.322804</td>
    </tr>
    <tr>
      <th>26</th>
      <td>ANNOTATED_BY</td>
      <td>2919</td>
      <td>0.262250</td>
    </tr>
    <tr>
      <th>27</th>
      <td>REQUIRES</td>
      <td>2230</td>
      <td>0.200349</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_FIRST_CHILD</td>
      <td>2162</td>
      <td>0.194239</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_LAST_CHILD</td>
      <td>2162</td>
      <td>0.194239</td>
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
      <td>0.000090</td>
    </tr>
    <tr>
      <th>1</th>
      <td>THROWS_GENERIC</td>
      <td>5</td>
      <td>0.000449</td>
    </tr>
    <tr>
      <th>2</th>
      <td>EXCLUDES</td>
      <td>5</td>
      <td>0.000449</td>
    </tr>
    <tr>
      <th>3</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>7</td>
      <td>0.000629</td>
    </tr>
    <tr>
      <th>4</th>
      <td>DESCRIBES</td>
      <td>9</td>
      <td>0.000809</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_ROOT_ELEMENT</td>
      <td>11</td>
      <td>0.000988</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_GOAL</td>
      <td>16</td>
      <td>0.001437</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_EXECUTION</td>
      <td>16</td>
      <td>0.001437</td>
    </tr>
    <tr>
      <th>8</th>
      <td>OF_NAMESPACE</td>
      <td>18</td>
      <td>0.001617</td>
    </tr>
    <tr>
      <th>9</th>
      <td>HAS_ATTRIBUTE</td>
      <td>18</td>
      <td>0.001617</td>
    </tr>
    <tr>
      <th>10</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.001707</td>
    </tr>
    <tr>
      <th>11</th>
      <td>IS_ARTIFACT</td>
      <td>21</td>
      <td>0.001887</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS_CONFIGURATION</td>
      <td>21</td>
      <td>0.001887</td>
    </tr>
    <tr>
      <th>13</th>
      <td>USES_PLUGIN</td>
      <td>21</td>
      <td>0.001887</td>
    </tr>
    <tr>
      <th>14</th>
      <td>REQUIRES_TYPE_PARAMETER</td>
      <td>24</td>
      <td>0.002156</td>
    </tr>
    <tr>
      <th>15</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.002516</td>
    </tr>
    <tr>
      <th>16</th>
      <td>DECLARES_NAMESPACE</td>
      <td>36</td>
      <td>0.003234</td>
    </tr>
    <tr>
      <th>17</th>
      <td>HAS_DEFAULT</td>
      <td>39</td>
      <td>0.003504</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_BRANCH</td>
      <td>46</td>
      <td>0.004133</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_HEAD</td>
      <td>47</td>
      <td>0.004223</td>
    </tr>
    <tr>
      <th>20</th>
      <td>COPY_OF</td>
      <td>127</td>
      <td>0.011410</td>
    </tr>
    <tr>
      <th>21</th>
      <td>CONTAINS_VALUE</td>
      <td>160</td>
      <td>0.014375</td>
    </tr>
    <tr>
      <th>22</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>165</td>
      <td>0.014824</td>
    </tr>
    <tr>
      <th>23</th>
      <td>TO_ARTIFACT</td>
      <td>165</td>
      <td>0.014824</td>
    </tr>
    <tr>
      <th>24</th>
      <td>HAS_COMPONENT_TYPE</td>
      <td>166</td>
      <td>0.014914</td>
    </tr>
    <tr>
      <th>25</th>
      <td>ON_COMMIT</td>
      <td>171</td>
      <td>0.015363</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_TAG</td>
      <td>171</td>
      <td>0.015363</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_COMMITTER</td>
      <td>252</td>
      <td>0.022640</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_AUTHOR</td>
      <td>299</td>
      <td>0.026863</td>
    </tr>
    <tr>
      <th>29</th>
      <td>COPIES</td>
      <td>334</td>
      <td>0.030007</td>
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
      <td>[Git, Update, Change]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>176097</td>
      <td>176097</td>
      <td>11022</td>
      <td>0.009073</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Update, Change]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>176097</td>
      <td>176097</td>
      <td>11022</td>
      <td>0.009073</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Update, Change]</td>
      <td>176097</td>
      <td>13137</td>
      <td>176097</td>
      <td>0.007612</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>51952</td>
      <td>13137</td>
      <td>51952</td>
      <td>0.007612</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>51952</td>
      <td>51952</td>
      <td>11022</td>
      <td>0.009073</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>51952</td>
      <td>51952</td>
      <td>11022</td>
      <td>0.009073</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>27797</td>
      <td>13137</td>
      <td>27797</td>
      <td>0.007612</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>27797</td>
      <td>27797</td>
      <td>11022</td>
      <td>0.009073</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>27797</td>
      <td>27797</td>
      <td>11022</td>
      <td>0.009073</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>INVOKES</td>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>22590</td>
      <td>13404</td>
      <td>13404</td>
      <td>0.012573</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>15884</td>
      <td>13137</td>
      <td>13137</td>
      <td>0.009204</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>13137</td>
      <td>1</td>
      <td>13137</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>13137</td>
      <td>252</td>
      <td>13137</td>
      <td>0.396825</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>13137</td>
      <td>299</td>
      <td>13137</td>
      <td>0.334448</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>11022</td>
      <td>1</td>
      <td>11022</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>10655</td>
      <td>13137</td>
      <td>10655</td>
      <td>0.007612</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>10655</td>
      <td>10655</td>
      <td>11022</td>
      <td>0.009073</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>10655</td>
      <td>10655</td>
      <td>11022</td>
      <td>0.009073</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>10655</td>
      <td>10655</td>
      <td>11022</td>
      <td>0.009073</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>10655</td>
      <td>10655</td>
      <td>11022</td>
      <td>0.009073</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>HAS</td>
      <td>[Java, ByteCode, Parameter]</td>
      <td>8517</td>
      <td>13404</td>
      <td>13293</td>
      <td>0.004780</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Java, ByteCode, Member, Method]</td>
      <td>READS</td>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>8446</td>
      <td>13404</td>
      <td>3609</td>
      <td>0.017459</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>6270</td>
      <td>11022</td>
      <td>11022</td>
      <td>0.005161</td>
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
      <td>[Java, ByteCode, Member, Method, Constructor]</td>
      <td>WRITES</td>
      <td>[Java, ByteCode, Member, Field]</td>
      <td>2519</td>
      <td>2120</td>
      <td>3609</td>
      <td>0.032923</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Java, ByteCode, Bound, ParameterizedType]</td>
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

    total_number_of_nodes (vertices): 358701
    total_number_of_relationships (edges): 1113059
    -> total directed graph density: 8.650759164876725e-06
    -> total directed graph density in percent: 0.0008650759164876725

