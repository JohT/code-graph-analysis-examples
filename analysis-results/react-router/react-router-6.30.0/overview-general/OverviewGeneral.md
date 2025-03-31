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
      <td>58793</td>
      <td>52.230731</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change, Create]</td>
      <td>17294</td>
      <td>15.363704</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>11298</td>
      <td>10.036957</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Change, Delete]</td>
      <td>8782</td>
      <td>7.801784</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Git]</td>
      <td>5905</td>
      <td>5.245905</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Rename]</td>
      <td>3355</td>
      <td>2.980527</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Tag]</td>
      <td>1758</td>
      <td>1.561778</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Author, Git, Person]</td>
      <td>1267</td>
      <td>1.125582</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Json, Key]</td>
      <td>668</td>
      <td>0.593440</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Json, Value, Scalar]</td>
      <td>603</td>
      <td>0.535695</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Committer, Git, Person]</td>
      <td>370</td>
      <td>0.328702</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[NPM, Dependency]</td>
      <td>338</td>
      <td>0.300274</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Type, TS, Primitive]</td>
      <td>293</td>
      <td>0.260296</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Type, TS, Declared]</td>
      <td>277</td>
      <td>0.246082</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[TS, ExternalDeclaration]</td>
      <td>215</td>
      <td>0.191002</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Git, Change, Copy]</td>
      <td>138</td>
      <td>0.122597</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Type, TS, Literal]</td>
      <td>136</td>
      <td>0.120820</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Json, Value, Object]</td>
      <td>133</td>
      <td>0.118155</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, TS, Union]</td>
      <td>120</td>
      <td>0.106606</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>103</td>
      <td>0.091504</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[NPM, Script]</td>
      <td>91</td>
      <td>0.080843</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[TS, Property]</td>
      <td>65</td>
      <td>0.057745</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[TS, Function]</td>
      <td>47</td>
      <td>0.041754</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Git, Branch]</td>
      <td>46</td>
      <td>0.040866</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, TS, FunctionParameter]</td>
      <td>40</td>
      <td>0.035535</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, Object, TS]</td>
      <td>39</td>
      <td>0.034647</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[File, Directory]</td>
      <td>34</td>
      <td>0.030205</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Type, TS, Function]</td>
      <td>34</td>
      <td>0.030205</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[TS, Parameter]</td>
      <td>33</td>
      <td>0.029317</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Package, File, Json, NPM]</td>
      <td>29</td>
      <td>0.025763</td>
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
      <td>0.000888</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[NPM, PublishConfig]</td>
      <td>1</td>
      <td>0.000888</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[File, TS, Scan]</td>
      <td>1</td>
      <td>0.000888</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[TS, Method]</td>
      <td>1</td>
      <td>0.000888</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000888</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[TS, Constructor]</td>
      <td>1</td>
      <td>0.000888</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Value, TS, ObjectMember]</td>
      <td>1</td>
      <td>0.000888</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[TS, Class]</td>
      <td>1</td>
      <td>0.000888</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[TS, Enum]</td>
      <td>2</td>
      <td>0.001777</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Value, Object, TS]</td>
      <td>3</td>
      <td>0.002665</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Type, TS, Tuple]</td>
      <td>3</td>
      <td>0.002665</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Value, TS, Function]</td>
      <td>4</td>
      <td>0.003554</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[TS, TypeParameter]</td>
      <td>4</td>
      <td>0.003554</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Value, TS, Complex]</td>
      <td>5</td>
      <td>0.004442</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Repository, NPM]</td>
      <td>5</td>
      <td>0.004442</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[NPM, Engine]</td>
      <td>6</td>
      <td>0.005330</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Project, TS]</td>
      <td>6</td>
      <td>0.005330</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[File, Local]</td>
      <td>6</td>
      <td>0.005330</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, TS, TypeParameterReference]</td>
      <td>6</td>
      <td>0.005330</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Value, TS, Member]</td>
      <td>6</td>
      <td>0.005330</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[File, TS, Local, Module]</td>
      <td>6</td>
      <td>0.005330</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Value, TS, Call]</td>
      <td>6</td>
      <td>0.005330</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[TS, EnumMember]</td>
      <td>8</td>
      <td>0.007107</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, TS, NotIdentified]</td>
      <td>11</td>
      <td>0.009772</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[TS, ExternalModule]</td>
      <td>11</td>
      <td>0.009772</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Json, Value, Array]</td>
      <td>12</td>
      <td>0.010661</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Value, TS, Declared]</td>
      <td>13</td>
      <td>0.011549</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[TS, TypeAlias]</td>
      <td>16</td>
      <td>0.014214</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[File, Directory, Local]</td>
      <td>16</td>
      <td>0.014214</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[TS, Interface]</td>
      <td>17</td>
      <td>0.015103</td>
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
      <td>109007</td>
      <td>96.840020</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>88362</td>
      <td>78.499343</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Update</td>
      <td>58793</td>
      <td>52.230731</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Create</td>
      <td>17294</td>
      <td>15.363704</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Commit</td>
      <td>11298</td>
      <td>10.036957</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Delete</td>
      <td>8782</td>
      <td>7.801784</td>
    </tr>
    <tr>
      <th>6</th>
      <td>File</td>
      <td>5998</td>
      <td>5.328524</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Rename</td>
      <td>3355</td>
      <td>2.980527</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Tag</td>
      <td>1758</td>
      <td>1.561778</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Person</td>
      <td>1637</td>
      <td>1.454284</td>
    </tr>
    <tr>
      <th>10</th>
      <td>TS</td>
      <td>1595</td>
      <td>1.416972</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Json</td>
      <td>1445</td>
      <td>1.283714</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Author</td>
      <td>1267</td>
      <td>1.125582</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Type</td>
      <td>1079</td>
      <td>0.958566</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Value</td>
      <td>806</td>
      <td>0.716037</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Key</td>
      <td>668</td>
      <td>0.593440</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Scalar</td>
      <td>603</td>
      <td>0.535695</td>
    </tr>
    <tr>
      <th>17</th>
      <td>NPM</td>
      <td>470</td>
      <td>0.417540</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Committer</td>
      <td>370</td>
      <td>0.328702</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Dependency</td>
      <td>338</td>
      <td>0.300274</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Primitive</td>
      <td>293</td>
      <td>0.260296</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Declared</td>
      <td>290</td>
      <td>0.257631</td>
    </tr>
    <tr>
      <th>22</th>
      <td>ExternalDeclaration</td>
      <td>215</td>
      <td>0.191002</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Object</td>
      <td>175</td>
      <td>0.155467</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Literal</td>
      <td>156</td>
      <td>0.138588</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Copy</td>
      <td>138</td>
      <td>0.122597</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Union</td>
      <td>120</td>
      <td>0.106606</td>
    </tr>
    <tr>
      <th>27</th>
      <td>ObjectMember</td>
      <td>104</td>
      <td>0.092392</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Script</td>
      <td>91</td>
      <td>0.080843</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Function</td>
      <td>85</td>
      <td>0.075513</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Property</td>
      <td>65</td>
      <td>0.057745</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Directory</td>
      <td>50</td>
      <td>0.044419</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Branch</td>
      <td>46</td>
      <td>0.040866</td>
    </tr>
    <tr>
      <th>33</th>
      <td>FunctionParameter</td>
      <td>40</td>
      <td>0.035535</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Parameter</td>
      <td>33</td>
      <td>0.029317</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Package</td>
      <td>29</td>
      <td>0.025763</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Local</td>
      <td>28</td>
      <td>0.024875</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Variable</td>
      <td>24</td>
      <td>0.021321</td>
    </tr>
    <tr>
      <th>38</th>
      <td>jQAssistant</td>
      <td>20</td>
      <td>0.017768</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Concept</td>
      <td>19</td>
      <td>0.016879</td>
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

    Total number of relationships: 336124





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
      <td>88362</td>
      <td>26.288513</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>88362</td>
      <td>26.288513</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>58793</td>
      <td>17.491461</td>
    </tr>
    <tr>
      <th>3</th>
      <td>COMMITTED</td>
      <td>22596</td>
      <td>6.722519</td>
    </tr>
    <tr>
      <th>4</th>
      <td>CREATES</td>
      <td>20787</td>
      <td>6.184325</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_PARENT</td>
      <td>12383</td>
      <td>3.684057</td>
    </tr>
    <tr>
      <th>6</th>
      <td>DELETES</td>
      <td>12137</td>
      <td>3.610870</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_COMMIT</td>
      <td>11298</td>
      <td>3.361260</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_FILE</td>
      <td>5905</td>
      <td>1.756792</td>
    </tr>
    <tr>
      <th>9</th>
      <td>RENAMES</td>
      <td>3355</td>
      <td>0.998144</td>
    </tr>
    <tr>
      <th>10</th>
      <td>HAS_NEW_NAME</td>
      <td>1771</td>
      <td>0.526889</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_TAG</td>
      <td>1758</td>
      <td>0.523021</td>
    </tr>
    <tr>
      <th>12</th>
      <td>ON_COMMIT</td>
      <td>1758</td>
      <td>0.523021</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_AUTHOR</td>
      <td>1267</td>
      <td>0.376944</td>
    </tr>
    <tr>
      <th>14</th>
      <td>DEPENDS_ON</td>
      <td>887</td>
      <td>0.263891</td>
    </tr>
    <tr>
      <th>15</th>
      <td>HAS_KEY</td>
      <td>668</td>
      <td>0.198736</td>
    </tr>
    <tr>
      <th>16</th>
      <td>HAS_VALUE</td>
      <td>668</td>
      <td>0.198736</td>
    </tr>
    <tr>
      <th>17</th>
      <td>CONTAINS</td>
      <td>596</td>
      <td>0.177316</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_COMMITTER</td>
      <td>370</td>
      <td>0.110078</td>
    </tr>
    <tr>
      <th>19</th>
      <td>OF_TYPE</td>
      <td>339</td>
      <td>0.100856</td>
    </tr>
    <tr>
      <th>20</th>
      <td>EXPORTS</td>
      <td>309</td>
      <td>0.091930</td>
    </tr>
    <tr>
      <th>21</th>
      <td>REFERENCES</td>
      <td>197</td>
      <td>0.058609</td>
    </tr>
    <tr>
      <th>22</th>
      <td>DECLARES</td>
      <td>186</td>
      <td>0.055337</td>
    </tr>
    <tr>
      <th>23</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>169</td>
      <td>0.050279</td>
    </tr>
    <tr>
      <th>24</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>161</td>
      <td>0.047899</td>
    </tr>
    <tr>
      <th>25</th>
      <td>COPIES</td>
      <td>138</td>
      <td>0.041056</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_MEMBER</td>
      <td>104</td>
      <td>0.030941</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>0.027966</td>
    </tr>
    <tr>
      <th>28</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.027073</td>
    </tr>
    <tr>
      <th>29</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>0.024396</td>
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
      <td>0.000298</td>
    </tr>
    <tr>
      <th>1</th>
      <td>CONSTRAINED_BY</td>
      <td>4</td>
      <td>0.001190</td>
    </tr>
    <tr>
      <th>2</th>
      <td>IN_REPOSITORY</td>
      <td>5</td>
      <td>0.001488</td>
    </tr>
    <tr>
      <th>3</th>
      <td>REFERENCED_PROJECTS</td>
      <td>5</td>
      <td>0.001488</td>
    </tr>
    <tr>
      <th>4</th>
      <td>PARENT</td>
      <td>6</td>
      <td>0.001785</td>
    </tr>
    <tr>
      <th>5</th>
      <td>MEMBER</td>
      <td>6</td>
      <td>0.001785</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_ROOT</td>
      <td>6</td>
      <td>0.001785</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_NPM_PACKAGE</td>
      <td>6</td>
      <td>0.001785</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_CONFIG</td>
      <td>6</td>
      <td>0.001785</td>
    </tr>
    <tr>
      <th>9</th>
      <td>HAS_ARGUMENT</td>
      <td>6</td>
      <td>0.001785</td>
    </tr>
    <tr>
      <th>10</th>
      <td>EXTENDS</td>
      <td>6</td>
      <td>0.001785</td>
    </tr>
    <tr>
      <th>11</th>
      <td>DECLARES_ENGINE</td>
      <td>6</td>
      <td>0.001785</td>
    </tr>
    <tr>
      <th>12</th>
      <td>CONTAINS_PROJECT</td>
      <td>6</td>
      <td>0.001785</td>
    </tr>
    <tr>
      <th>13</th>
      <td>CALLS</td>
      <td>6</td>
      <td>0.001785</td>
    </tr>
    <tr>
      <th>14</th>
      <td>DECLARES_PEER_DEPENDENCY</td>
      <td>8</td>
      <td>0.002380</td>
    </tr>
    <tr>
      <th>15</th>
      <td>USES</td>
      <td>11</td>
      <td>0.003273</td>
    </tr>
    <tr>
      <th>16</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.005653</td>
    </tr>
    <tr>
      <th>17</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.008330</td>
    </tr>
    <tr>
      <th>18</th>
      <td>INITIALIZED_WITH</td>
      <td>32</td>
      <td>0.009520</td>
    </tr>
    <tr>
      <th>19</th>
      <td>IS_DESCRIBED_IN_NPM_PACKAGE</td>
      <td>33</td>
      <td>0.009818</td>
    </tr>
    <tr>
      <th>20</th>
      <td>RESOLVES_TO</td>
      <td>41</td>
      <td>0.012198</td>
    </tr>
    <tr>
      <th>21</th>
      <td>HAS_BRANCH</td>
      <td>46</td>
      <td>0.013685</td>
    </tr>
    <tr>
      <th>22</th>
      <td>HAS_HEAD</td>
      <td>47</td>
      <td>0.013983</td>
    </tr>
    <tr>
      <th>23</th>
      <td>CONTAINS_VALUE</td>
      <td>51</td>
      <td>0.015173</td>
    </tr>
    <tr>
      <th>24</th>
      <td>COPY_OF</td>
      <td>69</td>
      <td>0.020528</td>
    </tr>
    <tr>
      <th>25</th>
      <td>HAS_PARAMETER</td>
      <td>73</td>
      <td>0.021718</td>
    </tr>
    <tr>
      <th>26</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>0.024396</td>
    </tr>
    <tr>
      <th>27</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.027073</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>0.027966</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_MEMBER</td>
      <td>104</td>
      <td>0.030941</td>
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
      <td>58793</td>
      <td>58793</td>
      <td>5905</td>
      <td>0.016935</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Update, Change]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>58793</td>
      <td>58793</td>
      <td>5905</td>
      <td>0.016935</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Update, Change]</td>
      <td>58793</td>
      <td>11298</td>
      <td>58793</td>
      <td>0.008851</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>17294</td>
      <td>11298</td>
      <td>17294</td>
      <td>0.008851</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>17294</td>
      <td>17294</td>
      <td>5905</td>
      <td>0.016935</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>17294</td>
      <td>17294</td>
      <td>5905</td>
      <td>0.016935</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>12383</td>
      <td>11298</td>
      <td>11298</td>
      <td>0.009701</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>11298</td>
      <td>1</td>
      <td>11298</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>11298</td>
      <td>1267</td>
      <td>11298</td>
      <td>0.078927</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>11298</td>
      <td>370</td>
      <td>11298</td>
      <td>0.270270</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>8782</td>
      <td>11298</td>
      <td>8782</td>
      <td>0.008851</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>8782</td>
      <td>8782</td>
      <td>5905</td>
      <td>0.016935</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>8782</td>
      <td>8782</td>
      <td>5905</td>
      <td>0.016935</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>5905</td>
      <td>1</td>
      <td>5905</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>3355</td>
      <td>11298</td>
      <td>3355</td>
      <td>0.008851</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>3355</td>
      <td>3355</td>
      <td>5905</td>
      <td>0.016935</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>3355</td>
      <td>3355</td>
      <td>5905</td>
      <td>0.016935</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>3355</td>
      <td>3355</td>
      <td>5905</td>
      <td>0.016935</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>3355</td>
      <td>3355</td>
      <td>5905</td>
      <td>0.016935</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>1771</td>
      <td>5905</td>
      <td>5905</td>
      <td>0.005079</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_TAG</td>
      <td>[Git, Tag]</td>
      <td>1758</td>
      <td>1</td>
      <td>1758</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Git, Tag]</td>
      <td>ON_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>1758</td>
      <td>1758</td>
      <td>11298</td>
      <td>0.008851</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_AUTHOR</td>
      <td>[Author, Git, Person]</td>
      <td>1267</td>
      <td>1</td>
      <td>1267</td>
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

    total_number_of_nodes (vertices): 112564
    total_number_of_relationships (edges): 336124
    -> total directed graph density: 2.652799007454451e-05
    -> total directed graph density in percent: 0.002652799007454451

