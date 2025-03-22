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
      <td>58384</td>
      <td>52.135088</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change, Create]</td>
      <td>17242</td>
      <td>15.396567</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>11255</td>
      <td>10.050363</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Change, Delete]</td>
      <td>8758</td>
      <td>7.820620</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Git]</td>
      <td>5891</td>
      <td>5.260479</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Rename]</td>
      <td>3354</td>
      <td>2.995017</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Tag]</td>
      <td>1732</td>
      <td>1.546622</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Author, Git, Person]</td>
      <td>1265</td>
      <td>1.129605</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Json, Key]</td>
      <td>668</td>
      <td>0.596503</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Json, Value, Scalar]</td>
      <td>603</td>
      <td>0.538460</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Committer, Git, Person]</td>
      <td>370</td>
      <td>0.330398</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[NPM, Dependency]</td>
      <td>338</td>
      <td>0.301823</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Type, TS, Primitive]</td>
      <td>291</td>
      <td>0.259854</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Type, TS, Declared]</td>
      <td>277</td>
      <td>0.247352</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[TS, ExternalDeclaration]</td>
      <td>215</td>
      <td>0.191988</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Git, Change, Copy]</td>
      <td>138</td>
      <td>0.123230</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Type, TS, Literal]</td>
      <td>136</td>
      <td>0.121444</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Json, Value, Object]</td>
      <td>133</td>
      <td>0.118765</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, TS, Union]</td>
      <td>119</td>
      <td>0.106263</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>102</td>
      <td>0.091083</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[NPM, Script]</td>
      <td>91</td>
      <td>0.081260</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[TS, Property]</td>
      <td>65</td>
      <td>0.058043</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[TS, Function]</td>
      <td>47</td>
      <td>0.041970</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Git, Branch]</td>
      <td>43</td>
      <td>0.038398</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, TS, FunctionParameter]</td>
      <td>40</td>
      <td>0.035719</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, Object, TS]</td>
      <td>39</td>
      <td>0.034826</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[File, Directory]</td>
      <td>34</td>
      <td>0.030361</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Type, TS, Function]</td>
      <td>34</td>
      <td>0.030361</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[TS, Parameter]</td>
      <td>33</td>
      <td>0.029468</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Package, File, Json, NPM]</td>
      <td>29</td>
      <td>0.025896</td>
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
      <td>0.000893</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[NPM, PublishConfig]</td>
      <td>1</td>
      <td>0.000893</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[File, TS, Scan]</td>
      <td>1</td>
      <td>0.000893</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[TS, Method]</td>
      <td>1</td>
      <td>0.000893</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000893</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[TS, Constructor]</td>
      <td>1</td>
      <td>0.000893</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Value, TS, ObjectMember]</td>
      <td>1</td>
      <td>0.000893</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[TS, Class]</td>
      <td>1</td>
      <td>0.000893</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[TS, Enum]</td>
      <td>2</td>
      <td>0.001786</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Value, Object, TS]</td>
      <td>3</td>
      <td>0.002679</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Type, TS, Tuple]</td>
      <td>3</td>
      <td>0.002679</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Value, TS, Function]</td>
      <td>4</td>
      <td>0.003572</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[TS, TypeParameter]</td>
      <td>4</td>
      <td>0.003572</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Value, TS, Complex]</td>
      <td>5</td>
      <td>0.004465</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Repository, NPM]</td>
      <td>5</td>
      <td>0.004465</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[NPM, Engine]</td>
      <td>6</td>
      <td>0.005358</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Project, TS]</td>
      <td>6</td>
      <td>0.005358</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[File, Local]</td>
      <td>6</td>
      <td>0.005358</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, TS, TypeParameterReference]</td>
      <td>6</td>
      <td>0.005358</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Value, TS, Member]</td>
      <td>6</td>
      <td>0.005358</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[File, TS, Local, Module]</td>
      <td>6</td>
      <td>0.005358</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Value, TS, Call]</td>
      <td>6</td>
      <td>0.005358</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[TS, EnumMember]</td>
      <td>8</td>
      <td>0.007144</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, TS, NotIdentified]</td>
      <td>11</td>
      <td>0.009823</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[TS, ExternalModule]</td>
      <td>11</td>
      <td>0.009823</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Json, Value, Array]</td>
      <td>12</td>
      <td>0.010716</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Value, TS, Declared]</td>
      <td>13</td>
      <td>0.011609</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[TS, TypeAlias]</td>
      <td>16</td>
      <td>0.014288</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[File, Directory, Local]</td>
      <td>16</td>
      <td>0.014288</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[TS, Interface]</td>
      <td>17</td>
      <td>0.015180</td>
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
      <td>108433</td>
      <td>96.827282</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>87876</td>
      <td>78.470523</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Update</td>
      <td>58384</td>
      <td>52.135088</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Create</td>
      <td>17242</td>
      <td>15.396567</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Commit</td>
      <td>11255</td>
      <td>10.050363</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Delete</td>
      <td>8758</td>
      <td>7.820620</td>
    </tr>
    <tr>
      <th>6</th>
      <td>File</td>
      <td>5984</td>
      <td>5.343525</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Rename</td>
      <td>3354</td>
      <td>2.995017</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Tag</td>
      <td>1732</td>
      <td>1.546622</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Person</td>
      <td>1635</td>
      <td>1.460004</td>
    </tr>
    <tr>
      <th>10</th>
      <td>TS</td>
      <td>1591</td>
      <td>1.420713</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Json</td>
      <td>1445</td>
      <td>1.290340</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Author</td>
      <td>1265</td>
      <td>1.129605</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Type</td>
      <td>1075</td>
      <td>0.959941</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Value</td>
      <td>806</td>
      <td>0.719733</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Key</td>
      <td>668</td>
      <td>0.596503</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Scalar</td>
      <td>603</td>
      <td>0.538460</td>
    </tr>
    <tr>
      <th>17</th>
      <td>NPM</td>
      <td>470</td>
      <td>0.419695</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Committer</td>
      <td>370</td>
      <td>0.330398</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Dependency</td>
      <td>338</td>
      <td>0.301823</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Primitive</td>
      <td>291</td>
      <td>0.259854</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Declared</td>
      <td>290</td>
      <td>0.258961</td>
    </tr>
    <tr>
      <th>22</th>
      <td>ExternalDeclaration</td>
      <td>215</td>
      <td>0.191988</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Object</td>
      <td>175</td>
      <td>0.156270</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Literal</td>
      <td>156</td>
      <td>0.139303</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Copy</td>
      <td>138</td>
      <td>0.123230</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Union</td>
      <td>119</td>
      <td>0.106263</td>
    </tr>
    <tr>
      <th>27</th>
      <td>ObjectMember</td>
      <td>103</td>
      <td>0.091976</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Script</td>
      <td>91</td>
      <td>0.081260</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Function</td>
      <td>85</td>
      <td>0.075902</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Property</td>
      <td>65</td>
      <td>0.058043</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Directory</td>
      <td>50</td>
      <td>0.044648</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Branch</td>
      <td>43</td>
      <td>0.038398</td>
    </tr>
    <tr>
      <th>33</th>
      <td>FunctionParameter</td>
      <td>40</td>
      <td>0.035719</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Parameter</td>
      <td>33</td>
      <td>0.029468</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Package</td>
      <td>29</td>
      <td>0.025896</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Local</td>
      <td>28</td>
      <td>0.025003</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Variable</td>
      <td>24</td>
      <td>0.021431</td>
    </tr>
    <tr>
      <th>38</th>
      <td>jQAssistant</td>
      <td>20</td>
      <td>0.017859</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Concept</td>
      <td>19</td>
      <td>0.016966</td>
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

    Total number of relationships: 334408





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
      <td>87876</td>
      <td>26.278079</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>87876</td>
      <td>26.278079</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>58384</td>
      <td>17.458912</td>
    </tr>
    <tr>
      <th>3</th>
      <td>COMMITTED</td>
      <td>22510</td>
      <td>6.731298</td>
    </tr>
    <tr>
      <th>4</th>
      <td>CREATES</td>
      <td>20734</td>
      <td>6.200211</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_PARENT</td>
      <td>12335</td>
      <td>3.688608</td>
    </tr>
    <tr>
      <th>6</th>
      <td>DELETES</td>
      <td>12112</td>
      <td>3.621923</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_COMMIT</td>
      <td>11255</td>
      <td>3.365649</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_FILE</td>
      <td>5891</td>
      <td>1.761621</td>
    </tr>
    <tr>
      <th>9</th>
      <td>RENAMES</td>
      <td>3354</td>
      <td>1.002966</td>
    </tr>
    <tr>
      <th>10</th>
      <td>HAS_NEW_NAME</td>
      <td>1770</td>
      <td>0.529294</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_TAG</td>
      <td>1732</td>
      <td>0.517930</td>
    </tr>
    <tr>
      <th>12</th>
      <td>ON_COMMIT</td>
      <td>1732</td>
      <td>0.517930</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_AUTHOR</td>
      <td>1265</td>
      <td>0.378280</td>
    </tr>
    <tr>
      <th>14</th>
      <td>DEPENDS_ON</td>
      <td>887</td>
      <td>0.265245</td>
    </tr>
    <tr>
      <th>15</th>
      <td>HAS_KEY</td>
      <td>668</td>
      <td>0.199756</td>
    </tr>
    <tr>
      <th>16</th>
      <td>HAS_VALUE</td>
      <td>668</td>
      <td>0.199756</td>
    </tr>
    <tr>
      <th>17</th>
      <td>CONTAINS</td>
      <td>594</td>
      <td>0.177627</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_COMMITTER</td>
      <td>370</td>
      <td>0.110643</td>
    </tr>
    <tr>
      <th>19</th>
      <td>OF_TYPE</td>
      <td>338</td>
      <td>0.101074</td>
    </tr>
    <tr>
      <th>20</th>
      <td>EXPORTS</td>
      <td>309</td>
      <td>0.092402</td>
    </tr>
    <tr>
      <th>21</th>
      <td>REFERENCES</td>
      <td>197</td>
      <td>0.058910</td>
    </tr>
    <tr>
      <th>22</th>
      <td>DECLARES</td>
      <td>186</td>
      <td>0.055621</td>
    </tr>
    <tr>
      <th>23</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>169</td>
      <td>0.050537</td>
    </tr>
    <tr>
      <th>24</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>161</td>
      <td>0.048145</td>
    </tr>
    <tr>
      <th>25</th>
      <td>COPIES</td>
      <td>138</td>
      <td>0.041267</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_MEMBER</td>
      <td>103</td>
      <td>0.030801</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>0.028109</td>
    </tr>
    <tr>
      <th>28</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.027212</td>
    </tr>
    <tr>
      <th>29</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>0.024521</td>
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
      <td>DECLARES_PUBLISH_CONFIG</td>
      <td>1</td>
      <td>0.000299</td>
    </tr>
    <tr>
      <th>1</th>
      <td>CONSTRAINED_BY</td>
      <td>4</td>
      <td>0.001196</td>
    </tr>
    <tr>
      <th>2</th>
      <td>IN_REPOSITORY</td>
      <td>5</td>
      <td>0.001495</td>
    </tr>
    <tr>
      <th>3</th>
      <td>REFERENCED_PROJECTS</td>
      <td>5</td>
      <td>0.001495</td>
    </tr>
    <tr>
      <th>4</th>
      <td>PARENT</td>
      <td>6</td>
      <td>0.001794</td>
    </tr>
    <tr>
      <th>5</th>
      <td>MEMBER</td>
      <td>6</td>
      <td>0.001794</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_ROOT</td>
      <td>6</td>
      <td>0.001794</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_NPM_PACKAGE</td>
      <td>6</td>
      <td>0.001794</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_CONFIG</td>
      <td>6</td>
      <td>0.001794</td>
    </tr>
    <tr>
      <th>9</th>
      <td>HAS_ARGUMENT</td>
      <td>6</td>
      <td>0.001794</td>
    </tr>
    <tr>
      <th>10</th>
      <td>EXTENDS</td>
      <td>6</td>
      <td>0.001794</td>
    </tr>
    <tr>
      <th>11</th>
      <td>DECLARES_ENGINE</td>
      <td>6</td>
      <td>0.001794</td>
    </tr>
    <tr>
      <th>12</th>
      <td>CONTAINS_PROJECT</td>
      <td>6</td>
      <td>0.001794</td>
    </tr>
    <tr>
      <th>13</th>
      <td>CALLS</td>
      <td>6</td>
      <td>0.001794</td>
    </tr>
    <tr>
      <th>14</th>
      <td>DECLARES_PEER_DEPENDENCY</td>
      <td>8</td>
      <td>0.002392</td>
    </tr>
    <tr>
      <th>15</th>
      <td>USES</td>
      <td>11</td>
      <td>0.003289</td>
    </tr>
    <tr>
      <th>16</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.005682</td>
    </tr>
    <tr>
      <th>17</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.008373</td>
    </tr>
    <tr>
      <th>18</th>
      <td>INITIALIZED_WITH</td>
      <td>32</td>
      <td>0.009569</td>
    </tr>
    <tr>
      <th>19</th>
      <td>IS_DESCRIBED_IN_NPM_PACKAGE</td>
      <td>33</td>
      <td>0.009868</td>
    </tr>
    <tr>
      <th>20</th>
      <td>RESOLVES_TO</td>
      <td>41</td>
      <td>0.012260</td>
    </tr>
    <tr>
      <th>21</th>
      <td>HAS_BRANCH</td>
      <td>43</td>
      <td>0.012859</td>
    </tr>
    <tr>
      <th>22</th>
      <td>HAS_HEAD</td>
      <td>44</td>
      <td>0.013158</td>
    </tr>
    <tr>
      <th>23</th>
      <td>CONTAINS_VALUE</td>
      <td>51</td>
      <td>0.015251</td>
    </tr>
    <tr>
      <th>24</th>
      <td>COPY_OF</td>
      <td>69</td>
      <td>0.020633</td>
    </tr>
    <tr>
      <th>25</th>
      <td>HAS_PARAMETER</td>
      <td>73</td>
      <td>0.021830</td>
    </tr>
    <tr>
      <th>26</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>0.024521</td>
    </tr>
    <tr>
      <th>27</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.027212</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>0.028109</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_MEMBER</td>
      <td>103</td>
      <td>0.030801</td>
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
      <td>[Git, Change, Update]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>58384</td>
      <td>58384</td>
      <td>5891</td>
      <td>0.016975</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change, Update]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>58384</td>
      <td>58384</td>
      <td>5891</td>
      <td>0.016975</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Update]</td>
      <td>58384</td>
      <td>11255</td>
      <td>58384</td>
      <td>0.008885</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>17242</td>
      <td>17242</td>
      <td>5891</td>
      <td>0.016975</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>17242</td>
      <td>17242</td>
      <td>5891</td>
      <td>0.016975</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>17242</td>
      <td>11255</td>
      <td>17242</td>
      <td>0.008885</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>12335</td>
      <td>11255</td>
      <td>11255</td>
      <td>0.009738</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>11255</td>
      <td>1</td>
      <td>11255</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>11255</td>
      <td>1265</td>
      <td>11255</td>
      <td>0.079051</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>11255</td>
      <td>370</td>
      <td>11255</td>
      <td>0.270270</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>8758</td>
      <td>8758</td>
      <td>5891</td>
      <td>0.016975</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>8758</td>
      <td>8758</td>
      <td>5891</td>
      <td>0.016975</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>8758</td>
      <td>11255</td>
      <td>8758</td>
      <td>0.008885</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>5891</td>
      <td>1</td>
      <td>5891</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>3354</td>
      <td>3354</td>
      <td>5891</td>
      <td>0.016975</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>3354</td>
      <td>3354</td>
      <td>5891</td>
      <td>0.016975</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>3354</td>
      <td>3354</td>
      <td>5891</td>
      <td>0.016975</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>3354</td>
      <td>3354</td>
      <td>5891</td>
      <td>0.016975</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>3354</td>
      <td>11255</td>
      <td>3354</td>
      <td>0.008885</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>1770</td>
      <td>5891</td>
      <td>5891</td>
      <td>0.005100</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_TAG</td>
      <td>[Git, Tag]</td>
      <td>1732</td>
      <td>1</td>
      <td>1732</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Git, Tag]</td>
      <td>ON_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>1732</td>
      <td>1732</td>
      <td>11255</td>
      <td>0.008885</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_AUTHOR</td>
      <td>[Author, Git, Person]</td>
      <td>1265</td>
      <td>1</td>
      <td>1265</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Json, Value, Object]</td>
      <td>HAS_KEY</td>
      <td>[Json, Key]</td>
      <td>668</td>
      <td>133</td>
      <td>668</td>
      <td>0.751880</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Json, Key]</td>
      <td>HAS_VALUE</td>
      <td>[Json, Value, Scalar]</td>
      <td>552</td>
      <td>668</td>
      <td>603</td>
      <td>0.137039</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMITTER</td>
      <td>[Committer, Git, Person]</td>
      <td>370</td>
      <td>1</td>
      <td>370</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[TS, Function]</td>
      <td>DEPENDS_ON</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>293</td>
      <td>47</td>
      <td>215</td>
      <td>2.899555</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[File, TS, Local, Module]</td>
      <td>DEPENDS_ON</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>236</td>
      <td>6</td>
      <td>215</td>
      <td>18.294574</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[TS, ExternalModule]</td>
      <td>EXPORTS</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>215</td>
      <td>11</td>
      <td>215</td>
      <td>9.090909</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Package, File, Json, NPM]</td>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>[NPM, Dependency]</td>
      <td>169</td>
      <td>29</td>
      <td>338</td>
      <td>1.724138</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 111986
    total_number_of_relationships (edges): 334408
    -> total directed graph density: 2.666570508691998e-05
    -> total directed graph density in percent: 0.0026665705086919983

