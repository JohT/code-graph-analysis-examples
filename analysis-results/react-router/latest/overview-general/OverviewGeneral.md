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
      <td>[Git, Change, Update]</td>
      <td>56742</td>
      <td>27.692398</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Type, TS, NotIdentified]</td>
      <td>54205</td>
      <td>26.454239</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change, Create]</td>
      <td>16953</td>
      <td>8.273752</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Type, TS, Declared]</td>
      <td>11269</td>
      <td>5.499729</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Commit]</td>
      <td>10676</td>
      <td>5.210321</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Type, TS, Primitive]</td>
      <td>9113</td>
      <td>4.447514</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Change, Delete]</td>
      <td>8922</td>
      <td>4.354298</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[File, Git]</td>
      <td>6191</td>
      <td>3.021459</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Type, TS, Union]</td>
      <td>5600</td>
      <td>2.733027</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Type, TS, Literal]</td>
      <td>3393</td>
      <td>1.655922</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Change, Rename]</td>
      <td>2850</td>
      <td>1.390916</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>1930</td>
      <td>0.941918</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Json, Key]</td>
      <td>1928</td>
      <td>0.940942</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Json, Value, Scalar]</td>
      <td>1670</td>
      <td>0.815028</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Type, Object, TS]</td>
      <td>1534</td>
      <td>0.748654</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Author, Git, Person]</td>
      <td>1290</td>
      <td>0.629572</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Git, Tag]</td>
      <td>1213</td>
      <td>0.591993</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[TS, Parameter]</td>
      <td>1168</td>
      <td>0.570031</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[TS, ExternalDeclaration]</td>
      <td>1012</td>
      <td>0.493897</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[NPM, Dependency]</td>
      <td>881</td>
      <td>0.429964</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[TS, Property]</td>
      <td>614</td>
      <td>0.299657</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[TS, Function]</td>
      <td>568</td>
      <td>0.277207</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Type, TS, FunctionParameter]</td>
      <td>479</td>
      <td>0.233771</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Json, Value, Object]</td>
      <td>410</td>
      <td>0.200097</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, TS, Function]</td>
      <td>408</td>
      <td>0.199121</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Committer, Git, Person]</td>
      <td>361</td>
      <td>0.176183</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[TS, TypeAlias]</td>
      <td>335</td>
      <td>0.163494</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[TS, Variable]</td>
      <td>265</td>
      <td>0.129331</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Value, TS, Declared]</td>
      <td>242</td>
      <td>0.118106</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[TS, TypeParameter]</td>
      <td>233</td>
      <td>0.113713</td>
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
      <td>0.000488</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[TS, Setter]</td>
      <td>1</td>
      <td>0.000488</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Branch]</td>
      <td>1</td>
      <td>0.000488</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000488</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, TS, Local, Module, TestRelated, TestEnv...</td>
      <td>2</td>
      <td>0.000976</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[NPM, Overrides]</td>
      <td>2</td>
      <td>0.000976</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[TS, Enum]</td>
      <td>3</td>
      <td>0.001464</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[NPM, Binary]</td>
      <td>3</td>
      <td>0.001464</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[File, NPM, Export]</td>
      <td>5</td>
      <td>0.002440</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[TS, EnumMember]</td>
      <td>9</td>
      <td>0.004392</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[NPM, BugTracker]</td>
      <td>9</td>
      <td>0.004392</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[TS, Getter]</td>
      <td>11</td>
      <td>0.005368</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[TS, AccessorProperty]</td>
      <td>11</td>
      <td>0.005368</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[TS, Constructor]</td>
      <td>11</td>
      <td>0.005368</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[File, Local]</td>
      <td>11</td>
      <td>0.005368</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Project, TS]</td>
      <td>11</td>
      <td>0.005368</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Repository, NPM]</td>
      <td>11</td>
      <td>0.005368</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[TS, Class]</td>
      <td>12</td>
      <td>0.005856</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[File, TS, Scan]</td>
      <td>13</td>
      <td>0.006345</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Value, Object, TS]</td>
      <td>17</td>
      <td>0.008297</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[jQAssistant, Rule, Concept]</td>
      <td>19</td>
      <td>0.009273</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Value, TS, Null]</td>
      <td>23</td>
      <td>0.011225</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Value, Array, TS]</td>
      <td>29</td>
      <td>0.014153</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[NPM, Engine]</td>
      <td>31</td>
      <td>0.015129</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Json, Value, Array]</td>
      <td>37</td>
      <td>0.018058</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[File, Directory, Local]</td>
      <td>43</td>
      <td>0.020986</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, TS, Tuple]</td>
      <td>48</td>
      <td>0.023426</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Package, File, Json, NPM]</td>
      <td>62</td>
      <td>0.030259</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Git, Change, Copy]</td>
      <td>72</td>
      <td>0.035139</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[File, Directory]</td>
      <td>74</td>
      <td>0.036115</td>
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
      <td>105272</td>
      <td>51.377006</td>
    </tr>
    <tr>
      <th>1</th>
      <td>TS</td>
      <td>94208</td>
      <td>45.977326</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Type</td>
      <td>88325</td>
      <td>43.106183</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Change</td>
      <td>85539</td>
      <td>41.746502</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Update</td>
      <td>56742</td>
      <td>27.692398</td>
    </tr>
    <tr>
      <th>5</th>
      <td>NotIdentified</td>
      <td>54205</td>
      <td>26.454239</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Create</td>
      <td>16953</td>
      <td>8.273752</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Declared</td>
      <td>11511</td>
      <td>5.617835</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Commit</td>
      <td>10676</td>
      <td>5.210321</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Primitive</td>
      <td>9113</td>
      <td>4.447514</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Delete</td>
      <td>8922</td>
      <td>4.354298</td>
    </tr>
    <tr>
      <th>11</th>
      <td>File</td>
      <td>6558</td>
      <td>3.200570</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Union</td>
      <td>5600</td>
      <td>2.733027</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Json</td>
      <td>4107</td>
      <td>2.004383</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Literal</td>
      <td>3619</td>
      <td>1.766219</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Value</td>
      <td>3121</td>
      <td>1.523175</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Rename</td>
      <td>2850</td>
      <td>1.390916</td>
    </tr>
    <tr>
      <th>17</th>
      <td>ObjectMember</td>
      <td>2025</td>
      <td>0.988282</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Object</td>
      <td>1961</td>
      <td>0.957048</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Key</td>
      <td>1928</td>
      <td>0.940942</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Scalar</td>
      <td>1670</td>
      <td>0.815028</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Person</td>
      <td>1651</td>
      <td>0.805755</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Author</td>
      <td>1290</td>
      <td>0.629572</td>
    </tr>
    <tr>
      <th>23</th>
      <td>NPM</td>
      <td>1228</td>
      <td>0.599314</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Tag</td>
      <td>1213</td>
      <td>0.591993</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Parameter</td>
      <td>1168</td>
      <td>0.570031</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Function</td>
      <td>1065</td>
      <td>0.519763</td>
    </tr>
    <tr>
      <th>27</th>
      <td>ExternalDeclaration</td>
      <td>1012</td>
      <td>0.493897</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Dependency</td>
      <td>881</td>
      <td>0.429964</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Property</td>
      <td>614</td>
      <td>0.299657</td>
    </tr>
    <tr>
      <th>30</th>
      <td>FunctionParameter</td>
      <td>479</td>
      <td>0.233771</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Committer</td>
      <td>361</td>
      <td>0.176183</td>
    </tr>
    <tr>
      <th>32</th>
      <td>TypeAlias</td>
      <td>335</td>
      <td>0.163494</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Variable</td>
      <td>265</td>
      <td>0.129331</td>
    </tr>
    <tr>
      <th>34</th>
      <td>TypeParameter</td>
      <td>233</td>
      <td>0.113713</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Script</td>
      <td>224</td>
      <td>0.109321</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Local</td>
      <td>212</td>
      <td>0.103465</td>
    </tr>
    <tr>
      <th>37</th>
      <td>ExternalModule</td>
      <td>178</td>
      <td>0.086871</td>
    </tr>
    <tr>
      <th>38</th>
      <td>TypeParameterReference</td>
      <td>177</td>
      <td>0.086383</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Intersection</td>
      <td>169</td>
      <td>0.082479</td>
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

    Total number of relationships: 436769





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
      <td>85539</td>
      <td>19.584494</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>85539</td>
      <td>19.584494</td>
    </tr>
    <tr>
      <th>2</th>
      <td>CONTAINS</td>
      <td>74181</td>
      <td>16.984035</td>
    </tr>
    <tr>
      <th>3</th>
      <td>UPDATES</td>
      <td>56742</td>
      <td>12.991307</td>
    </tr>
    <tr>
      <th>4</th>
      <td>COMMITTED</td>
      <td>21352</td>
      <td>4.888625</td>
    </tr>
    <tr>
      <th>5</th>
      <td>CREATES</td>
      <td>19875</td>
      <td>4.550460</td>
    </tr>
    <tr>
      <th>6</th>
      <td>DELETES</td>
      <td>11772</td>
      <td>2.695246</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_PARENT</td>
      <td>11742</td>
      <td>2.688378</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_COMMIT</td>
      <td>10676</td>
      <td>2.444313</td>
    </tr>
    <tr>
      <th>9</th>
      <td>DEPENDS_ON</td>
      <td>9942</td>
      <td>2.276260</td>
    </tr>
    <tr>
      <th>10</th>
      <td>HAS_FILE</td>
      <td>6191</td>
      <td>1.417454</td>
    </tr>
    <tr>
      <th>11</th>
      <td>OF_TYPE</td>
      <td>5795</td>
      <td>1.326788</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>5506</td>
      <td>1.260621</td>
    </tr>
    <tr>
      <th>13</th>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>3722</td>
      <td>0.852167</td>
    </tr>
    <tr>
      <th>14</th>
      <td>REFERENCES</td>
      <td>3383</td>
      <td>0.774551</td>
    </tr>
    <tr>
      <th>15</th>
      <td>RENAMES</td>
      <td>2850</td>
      <td>0.652519</td>
    </tr>
    <tr>
      <th>16</th>
      <td>DECLARES</td>
      <td>2327</td>
      <td>0.532776</td>
    </tr>
    <tr>
      <th>17</th>
      <td>HAS_MEMBER</td>
      <td>2025</td>
      <td>0.463632</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_KEY</td>
      <td>1928</td>
      <td>0.441423</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_VALUE</td>
      <td>1928</td>
      <td>0.441423</td>
    </tr>
    <tr>
      <th>20</th>
      <td>EXPORTS</td>
      <td>1898</td>
      <td>0.434555</td>
    </tr>
    <tr>
      <th>21</th>
      <td>HAS_NEW_NAME</td>
      <td>1688</td>
      <td>0.386474</td>
    </tr>
    <tr>
      <th>22</th>
      <td>HAS_PARAMETER</td>
      <td>1535</td>
      <td>0.351444</td>
    </tr>
    <tr>
      <th>23</th>
      <td>HAS_AUTHOR</td>
      <td>1290</td>
      <td>0.295351</td>
    </tr>
    <tr>
      <th>24</th>
      <td>HAS_TAG</td>
      <td>1213</td>
      <td>0.277721</td>
    </tr>
    <tr>
      <th>25</th>
      <td>ON_COMMIT</td>
      <td>1213</td>
      <td>0.277721</td>
    </tr>
    <tr>
      <th>26</th>
      <td>RETURNS</td>
      <td>1108</td>
      <td>0.253681</td>
    </tr>
    <tr>
      <th>27</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>454</td>
      <td>0.103945</td>
    </tr>
    <tr>
      <th>28</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>400</td>
      <td>0.091582</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_COMMITTER</td>
      <td>361</td>
      <td>0.082652</td>
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
      <td>IMPLEMENTS</td>
      <td>1</td>
      <td>0.000229</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HAS_BRANCH</td>
      <td>1</td>
      <td>0.000229</td>
    </tr>
    <tr>
      <th>2</th>
      <td>DESCRIBED_BY_SETTER</td>
      <td>1</td>
      <td>0.000229</td>
    </tr>
    <tr>
      <th>3</th>
      <td>HAS_OVERRIDES</td>
      <td>2</td>
      <td>0.000458</td>
    </tr>
    <tr>
      <th>4</th>
      <td>HAS_HEAD</td>
      <td>2</td>
      <td>0.000458</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_BINARY</td>
      <td>3</td>
      <td>0.000687</td>
    </tr>
    <tr>
      <th>6</th>
      <td>REQUIRES</td>
      <td>5</td>
      <td>0.001145</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_BUG_TRACKER</td>
      <td>9</td>
      <td>0.002061</td>
    </tr>
    <tr>
      <th>8</th>
      <td>IN_REPOSITORY</td>
      <td>11</td>
      <td>0.002518</td>
    </tr>
    <tr>
      <th>9</th>
      <td>HAS_ROOT</td>
      <td>11</td>
      <td>0.002518</td>
    </tr>
    <tr>
      <th>10</th>
      <td>HAS_NPM_PACKAGE</td>
      <td>11</td>
      <td>0.002518</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_CONFIG</td>
      <td>11</td>
      <td>0.002518</td>
    </tr>
    <tr>
      <th>12</th>
      <td>DESCRIBED_BY_GETTER</td>
      <td>11</td>
      <td>0.002518</td>
    </tr>
    <tr>
      <th>13</th>
      <td>CONTAINS_PROJECT</td>
      <td>11</td>
      <td>0.002518</td>
    </tr>
    <tr>
      <th>14</th>
      <td>HAS_EXPORT</td>
      <td>15</td>
      <td>0.003434</td>
    </tr>
    <tr>
      <th>15</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.004350</td>
    </tr>
    <tr>
      <th>16</th>
      <td>DECLARES_PEER_DEPENDENCY</td>
      <td>27</td>
      <td>0.006182</td>
    </tr>
    <tr>
      <th>17</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.006411</td>
    </tr>
    <tr>
      <th>18</th>
      <td>DECLARES_ENGINE</td>
      <td>31</td>
      <td>0.007098</td>
    </tr>
    <tr>
      <th>19</th>
      <td>EXTENDS</td>
      <td>38</td>
      <td>0.008700</td>
    </tr>
    <tr>
      <th>20</th>
      <td>COPY_OF</td>
      <td>42</td>
      <td>0.009616</td>
    </tr>
    <tr>
      <th>21</th>
      <td>COPIES</td>
      <td>72</td>
      <td>0.016485</td>
    </tr>
    <tr>
      <th>22</th>
      <td>PARENT</td>
      <td>95</td>
      <td>0.021751</td>
    </tr>
    <tr>
      <th>23</th>
      <td>MEMBER</td>
      <td>95</td>
      <td>0.021751</td>
    </tr>
    <tr>
      <th>24</th>
      <td>CALLS</td>
      <td>100</td>
      <td>0.022895</td>
    </tr>
    <tr>
      <th>25</th>
      <td>HAS_ARGUMENT</td>
      <td>104</td>
      <td>0.023811</td>
    </tr>
    <tr>
      <th>26</th>
      <td>PROVIDED_BY_NPM_DEPENDENCY</td>
      <td>106</td>
      <td>0.024269</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS</td>
      <td>112</td>
      <td>0.025643</td>
    </tr>
    <tr>
      <th>28</th>
      <td>CONTAINS_VALUE</td>
      <td>127</td>
      <td>0.029077</td>
    </tr>
    <tr>
      <th>29</th>
      <td>IS_DESCRIBED_IN_NPM_PACKAGE</td>
      <td>146</td>
      <td>0.033427</td>
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
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Update]</td>
      <td>56742</td>
      <td>10676</td>
      <td>56742</td>
      <td>0.009367</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change, Update]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>56742</td>
      <td>56742</td>
      <td>6191</td>
      <td>0.016152</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change, Update]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>56742</td>
      <td>56742</td>
      <td>6191</td>
      <td>0.016152</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, NotIdentified]</td>
      <td>53911</td>
      <td>5600</td>
      <td>54205</td>
      <td>0.017760</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>16953</td>
      <td>10676</td>
      <td>16953</td>
      <td>0.009367</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>16953</td>
      <td>16953</td>
      <td>6191</td>
      <td>0.016152</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>16953</td>
      <td>16953</td>
      <td>6191</td>
      <td>0.016152</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>11742</td>
      <td>10676</td>
      <td>10676</td>
      <td>0.010302</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>10676</td>
      <td>1</td>
      <td>10676</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>10676</td>
      <td>1290</td>
      <td>10676</td>
      <td>0.077519</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>10676</td>
      <td>361</td>
      <td>10676</td>
      <td>0.277008</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>8922</td>
      <td>10676</td>
      <td>8922</td>
      <td>0.009367</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>8922</td>
      <td>8922</td>
      <td>6191</td>
      <td>0.016152</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>8922</td>
      <td>8922</td>
      <td>6191</td>
      <td>0.016152</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Declared]</td>
      <td>8240</td>
      <td>5600</td>
      <td>11269</td>
      <td>0.013057</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Primitive]</td>
      <td>6419</td>
      <td>5600</td>
      <td>9113</td>
      <td>0.012578</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>6191</td>
      <td>1</td>
      <td>6191</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Type, TS, Declared]</td>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>[Type, TS, Union]</td>
      <td>4157</td>
      <td>11269</td>
      <td>5600</td>
      <td>0.006587</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[File, Git]</td>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>[File, Git]</td>
      <td>3240</td>
      <td>6191</td>
      <td>6191</td>
      <td>0.008453</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Literal]</td>
      <td>3130</td>
      <td>5600</td>
      <td>3393</td>
      <td>0.016473</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>2850</td>
      <td>10676</td>
      <td>2850</td>
      <td>0.009367</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>2850</td>
      <td>2850</td>
      <td>6191</td>
      <td>0.016152</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>2850</td>
      <td>2850</td>
      <td>6191</td>
      <td>0.016152</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>2850</td>
      <td>2850</td>
      <td>6191</td>
      <td>0.016152</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>2850</td>
      <td>2850</td>
      <td>6191</td>
      <td>0.016152</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, Object, TS]</td>
      <td>HAS_MEMBER</td>
      <td>[Type, TS, ObjectMember]</td>
      <td>1930</td>
      <td>1534</td>
      <td>1930</td>
      <td>0.065189</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Json, Value, Object]</td>
      <td>HAS_KEY</td>
      <td>[Json, Key]</td>
      <td>1928</td>
      <td>410</td>
      <td>1928</td>
      <td>0.243902</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>1688</td>
      <td>6191</td>
      <td>6191</td>
      <td>0.004404</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Json, Key]</td>
      <td>HAS_VALUE</td>
      <td>[Json, Value, Scalar]</td>
      <td>1543</td>
      <td>1928</td>
      <td>1670</td>
      <td>0.047923</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Type, TS, Declared]</td>
      <td>REFERENCES</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>1497</td>
      <td>11269</td>
      <td>1012</td>
      <td>0.013127</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 204901
    total_number_of_relationships (edges): 436769
    -> total directed graph density: 1.0403171788261783e-05
    -> total directed graph density in percent: 0.0010403171788261783

