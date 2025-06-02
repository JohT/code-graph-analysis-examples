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
      <td>26416</td>
      <td>48.641084</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Commit]</td>
      <td>6744</td>
      <td>12.418060</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change, Create]</td>
      <td>5847</td>
      <td>10.766370</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Change, Delete]</td>
      <td>4190</td>
      <td>7.715254</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Git]</td>
      <td>3576</td>
      <td>6.584665</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Rename]</td>
      <td>1699</td>
      <td>3.128453</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Author, Git, Person]</td>
      <td>1000</td>
      <td>1.841349</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Tag]</td>
      <td>906</td>
      <td>1.668263</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Json, Key]</td>
      <td>668</td>
      <td>1.230021</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Json, Value, Scalar]</td>
      <td>603</td>
      <td>1.110334</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Committer, Git, Person]</td>
      <td>356</td>
      <td>0.655520</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[NPM, Dependency]</td>
      <td>338</td>
      <td>0.622376</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Type, TS, Primitive]</td>
      <td>293</td>
      <td>0.539515</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Type, TS, Declared]</td>
      <td>277</td>
      <td>0.510054</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[TS, ExternalDeclaration]</td>
      <td>215</td>
      <td>0.395890</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Type, TS, Literal]</td>
      <td>136</td>
      <td>0.250424</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Json, Value, Object]</td>
      <td>133</td>
      <td>0.244899</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Type, TS, Union]</td>
      <td>120</td>
      <td>0.220962</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>103</td>
      <td>0.189659</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[NPM, Script]</td>
      <td>91</td>
      <td>0.167563</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[TS, Property]</td>
      <td>65</td>
      <td>0.119688</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[TS, Function]</td>
      <td>47</td>
      <td>0.086543</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Type, TS, FunctionParameter]</td>
      <td>40</td>
      <td>0.073654</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, Object, TS]</td>
      <td>39</td>
      <td>0.071813</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[File, Directory]</td>
      <td>34</td>
      <td>0.062606</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, TS, Function]</td>
      <td>34</td>
      <td>0.062606</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[TS, Parameter]</td>
      <td>33</td>
      <td>0.060765</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Package, File, Json, NPM]</td>
      <td>29</td>
      <td>0.053399</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[TS, Variable]</td>
      <td>24</td>
      <td>0.044192</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Value, TS, Literal]</td>
      <td>20</td>
      <td>0.036827</td>
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
      <td>0.001841</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[NPM, PublishConfig]</td>
      <td>1</td>
      <td>0.001841</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[File, TS, Scan]</td>
      <td>1</td>
      <td>0.001841</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[TS, Method]</td>
      <td>1</td>
      <td>0.001841</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Branch]</td>
      <td>1</td>
      <td>0.001841</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[TS, Constructor]</td>
      <td>1</td>
      <td>0.001841</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Value, TS, ObjectMember]</td>
      <td>1</td>
      <td>0.001841</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.001841</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[TS, Class]</td>
      <td>1</td>
      <td>0.001841</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[TS, Enum]</td>
      <td>2</td>
      <td>0.003683</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Value, Object, TS]</td>
      <td>3</td>
      <td>0.005524</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Type, TS, Tuple]</td>
      <td>3</td>
      <td>0.005524</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Value, TS, Function]</td>
      <td>4</td>
      <td>0.007365</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[TS, TypeParameter]</td>
      <td>4</td>
      <td>0.007365</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Value, TS, Complex]</td>
      <td>5</td>
      <td>0.009207</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Repository, NPM]</td>
      <td>5</td>
      <td>0.009207</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[NPM, Engine]</td>
      <td>6</td>
      <td>0.011048</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Project, TS]</td>
      <td>6</td>
      <td>0.011048</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[File, Local]</td>
      <td>6</td>
      <td>0.011048</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[File, TS, Local, Module]</td>
      <td>6</td>
      <td>0.011048</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Value, TS, Call]</td>
      <td>6</td>
      <td>0.011048</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Type, TS, TypeParameterReference]</td>
      <td>6</td>
      <td>0.011048</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Value, TS, Member]</td>
      <td>6</td>
      <td>0.011048</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[TS, EnumMember]</td>
      <td>8</td>
      <td>0.014731</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, TS, NotIdentified]</td>
      <td>11</td>
      <td>0.020255</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[TS, ExternalModule]</td>
      <td>11</td>
      <td>0.020255</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Json, Value, Array]</td>
      <td>12</td>
      <td>0.022096</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Value, TS, Declared]</td>
      <td>13</td>
      <td>0.023938</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Git, Change, Copy]</td>
      <td>15</td>
      <td>0.027620</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[TS, TypeAlias]</td>
      <td>16</td>
      <td>0.029462</td>
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
      <td>50751</td>
      <td>93.450320</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>38167</td>
      <td>70.278780</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Update</td>
      <td>26416</td>
      <td>48.641084</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Commit</td>
      <td>6744</td>
      <td>12.418060</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Create</td>
      <td>5847</td>
      <td>10.766370</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Delete</td>
      <td>4190</td>
      <td>7.715254</td>
    </tr>
    <tr>
      <th>6</th>
      <td>File</td>
      <td>3669</td>
      <td>6.755911</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Rename</td>
      <td>1699</td>
      <td>3.128453</td>
    </tr>
    <tr>
      <th>8</th>
      <td>TS</td>
      <td>1595</td>
      <td>2.936952</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Json</td>
      <td>1445</td>
      <td>2.660750</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Person</td>
      <td>1356</td>
      <td>2.496870</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Type</td>
      <td>1079</td>
      <td>1.986816</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Author</td>
      <td>1000</td>
      <td>1.841349</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Tag</td>
      <td>906</td>
      <td>1.668263</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Value</td>
      <td>806</td>
      <td>1.484128</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Key</td>
      <td>668</td>
      <td>1.230021</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Scalar</td>
      <td>603</td>
      <td>1.110334</td>
    </tr>
    <tr>
      <th>17</th>
      <td>NPM</td>
      <td>470</td>
      <td>0.865434</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Committer</td>
      <td>356</td>
      <td>0.655520</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Dependency</td>
      <td>338</td>
      <td>0.622376</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Primitive</td>
      <td>293</td>
      <td>0.539515</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Declared</td>
      <td>290</td>
      <td>0.533991</td>
    </tr>
    <tr>
      <th>22</th>
      <td>ExternalDeclaration</td>
      <td>215</td>
      <td>0.395890</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Object</td>
      <td>175</td>
      <td>0.322236</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Literal</td>
      <td>156</td>
      <td>0.287250</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Union</td>
      <td>120</td>
      <td>0.220962</td>
    </tr>
    <tr>
      <th>26</th>
      <td>ObjectMember</td>
      <td>104</td>
      <td>0.191500</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Script</td>
      <td>91</td>
      <td>0.167563</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Function</td>
      <td>85</td>
      <td>0.156515</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Property</td>
      <td>65</td>
      <td>0.119688</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Directory</td>
      <td>50</td>
      <td>0.092067</td>
    </tr>
    <tr>
      <th>31</th>
      <td>FunctionParameter</td>
      <td>40</td>
      <td>0.073654</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Parameter</td>
      <td>33</td>
      <td>0.060765</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Package</td>
      <td>29</td>
      <td>0.053399</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Local</td>
      <td>28</td>
      <td>0.051558</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Variable</td>
      <td>24</td>
      <td>0.044192</td>
    </tr>
    <tr>
      <th>36</th>
      <td>jQAssistant</td>
      <td>20</td>
      <td>0.036827</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Concept</td>
      <td>19</td>
      <td>0.034986</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Rule</td>
      <td>19</td>
      <td>0.034986</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Interface</td>
      <td>17</td>
      <td>0.031303</td>
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

    Total number of relationships: 160177





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
      <td>38167</td>
      <td>23.828015</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>38167</td>
      <td>23.828015</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>26416</td>
      <td>16.491756</td>
    </tr>
    <tr>
      <th>3</th>
      <td>COMMITTED</td>
      <td>13488</td>
      <td>8.420685</td>
    </tr>
    <tr>
      <th>4</th>
      <td>CREATES</td>
      <td>7561</td>
      <td>4.720403</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_PARENT</td>
      <td>7517</td>
      <td>4.692933</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_COMMIT</td>
      <td>6744</td>
      <td>4.210342</td>
    </tr>
    <tr>
      <th>7</th>
      <td>DELETES</td>
      <td>5889</td>
      <td>3.676558</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_FILE</td>
      <td>3576</td>
      <td>2.232530</td>
    </tr>
    <tr>
      <th>9</th>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>1801</td>
      <td>1.124381</td>
    </tr>
    <tr>
      <th>10</th>
      <td>RENAMES</td>
      <td>1699</td>
      <td>1.060702</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_NEW_NAME</td>
      <td>1032</td>
      <td>0.644287</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS_AUTHOR</td>
      <td>1000</td>
      <td>0.624309</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_TAG</td>
      <td>906</td>
      <td>0.565624</td>
    </tr>
    <tr>
      <th>14</th>
      <td>ON_COMMIT</td>
      <td>906</td>
      <td>0.565624</td>
    </tr>
    <tr>
      <th>15</th>
      <td>DEPENDS_ON</td>
      <td>887</td>
      <td>0.553762</td>
    </tr>
    <tr>
      <th>16</th>
      <td>HAS_KEY</td>
      <td>668</td>
      <td>0.417039</td>
    </tr>
    <tr>
      <th>17</th>
      <td>HAS_VALUE</td>
      <td>668</td>
      <td>0.417039</td>
    </tr>
    <tr>
      <th>18</th>
      <td>CONTAINS</td>
      <td>596</td>
      <td>0.372088</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_COMMITTER</td>
      <td>356</td>
      <td>0.222254</td>
    </tr>
    <tr>
      <th>20</th>
      <td>OF_TYPE</td>
      <td>339</td>
      <td>0.211641</td>
    </tr>
    <tr>
      <th>21</th>
      <td>EXPORTS</td>
      <td>309</td>
      <td>0.192912</td>
    </tr>
    <tr>
      <th>22</th>
      <td>REFERENCES</td>
      <td>197</td>
      <td>0.122989</td>
    </tr>
    <tr>
      <th>23</th>
      <td>DECLARES</td>
      <td>186</td>
      <td>0.116122</td>
    </tr>
    <tr>
      <th>24</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>169</td>
      <td>0.105508</td>
    </tr>
    <tr>
      <th>25</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>161</td>
      <td>0.100514</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_MEMBER</td>
      <td>104</td>
      <td>0.064928</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>0.058685</td>
    </tr>
    <tr>
      <th>28</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.056812</td>
    </tr>
    <tr>
      <th>29</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>0.051193</td>
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
      <td>HAS_BRANCH</td>
      <td>1</td>
      <td>0.000624</td>
    </tr>
    <tr>
      <th>1</th>
      <td>DECLARES_PUBLISH_CONFIG</td>
      <td>1</td>
      <td>0.000624</td>
    </tr>
    <tr>
      <th>2</th>
      <td>HAS_HEAD</td>
      <td>2</td>
      <td>0.001249</td>
    </tr>
    <tr>
      <th>3</th>
      <td>CONSTRAINED_BY</td>
      <td>4</td>
      <td>0.002497</td>
    </tr>
    <tr>
      <th>4</th>
      <td>REFERENCED_PROJECTS</td>
      <td>5</td>
      <td>0.003122</td>
    </tr>
    <tr>
      <th>5</th>
      <td>IN_REPOSITORY</td>
      <td>5</td>
      <td>0.003122</td>
    </tr>
    <tr>
      <th>6</th>
      <td>DECLARES_ENGINE</td>
      <td>6</td>
      <td>0.003746</td>
    </tr>
    <tr>
      <th>7</th>
      <td>EXTENDS</td>
      <td>6</td>
      <td>0.003746</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_ARGUMENT</td>
      <td>6</td>
      <td>0.003746</td>
    </tr>
    <tr>
      <th>9</th>
      <td>CALLS</td>
      <td>6</td>
      <td>0.003746</td>
    </tr>
    <tr>
      <th>10</th>
      <td>HAS_NPM_PACKAGE</td>
      <td>6</td>
      <td>0.003746</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_CONFIG</td>
      <td>6</td>
      <td>0.003746</td>
    </tr>
    <tr>
      <th>12</th>
      <td>PARENT</td>
      <td>6</td>
      <td>0.003746</td>
    </tr>
    <tr>
      <th>13</th>
      <td>CONTAINS_PROJECT</td>
      <td>6</td>
      <td>0.003746</td>
    </tr>
    <tr>
      <th>14</th>
      <td>MEMBER</td>
      <td>6</td>
      <td>0.003746</td>
    </tr>
    <tr>
      <th>15</th>
      <td>HAS_ROOT</td>
      <td>6</td>
      <td>0.003746</td>
    </tr>
    <tr>
      <th>16</th>
      <td>DECLARES_PEER_DEPENDENCY</td>
      <td>8</td>
      <td>0.004994</td>
    </tr>
    <tr>
      <th>17</th>
      <td>USES</td>
      <td>11</td>
      <td>0.006867</td>
    </tr>
    <tr>
      <th>18</th>
      <td>COPY_OF</td>
      <td>12</td>
      <td>0.007492</td>
    </tr>
    <tr>
      <th>19</th>
      <td>COPIES</td>
      <td>15</td>
      <td>0.009365</td>
    </tr>
    <tr>
      <th>20</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.011862</td>
    </tr>
    <tr>
      <th>21</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.017481</td>
    </tr>
    <tr>
      <th>22</th>
      <td>INITIALIZED_WITH</td>
      <td>32</td>
      <td>0.019978</td>
    </tr>
    <tr>
      <th>23</th>
      <td>IS_DESCRIBED_IN_NPM_PACKAGE</td>
      <td>33</td>
      <td>0.020602</td>
    </tr>
    <tr>
      <th>24</th>
      <td>RESOLVES_TO</td>
      <td>41</td>
      <td>0.025597</td>
    </tr>
    <tr>
      <th>25</th>
      <td>CONTAINS_VALUE</td>
      <td>51</td>
      <td>0.031840</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_PARAMETER</td>
      <td>73</td>
      <td>0.045575</td>
    </tr>
    <tr>
      <th>27</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>0.051193</td>
    </tr>
    <tr>
      <th>28</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.056812</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>0.058685</td>
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
      <td>26416</td>
      <td>26416</td>
      <td>3576</td>
      <td>0.027964</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Update, Change]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>26416</td>
      <td>26416</td>
      <td>3576</td>
      <td>0.027964</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Update, Change]</td>
      <td>26416</td>
      <td>6744</td>
      <td>26416</td>
      <td>0.014828</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>7517</td>
      <td>6744</td>
      <td>6744</td>
      <td>0.016528</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>6744</td>
      <td>1</td>
      <td>6744</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>6744</td>
      <td>1000</td>
      <td>6744</td>
      <td>0.100000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>6744</td>
      <td>356</td>
      <td>6744</td>
      <td>0.280899</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>5847</td>
      <td>6744</td>
      <td>5847</td>
      <td>0.014828</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>5847</td>
      <td>5847</td>
      <td>3576</td>
      <td>0.027964</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>5847</td>
      <td>5847</td>
      <td>3576</td>
      <td>0.027964</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>4190</td>
      <td>6744</td>
      <td>4190</td>
      <td>0.014828</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>4190</td>
      <td>4190</td>
      <td>3576</td>
      <td>0.027964</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>4190</td>
      <td>4190</td>
      <td>3576</td>
      <td>0.027964</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>3576</td>
      <td>1</td>
      <td>3576</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>1699</td>
      <td>6744</td>
      <td>1699</td>
      <td>0.014828</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>1699</td>
      <td>1699</td>
      <td>3576</td>
      <td>0.027964</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>1699</td>
      <td>1699</td>
      <td>3576</td>
      <td>0.027964</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>1699</td>
      <td>1699</td>
      <td>3576</td>
      <td>0.027964</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>1699</td>
      <td>1699</td>
      <td>3576</td>
      <td>0.027964</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[File, Git]</td>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>[File, Git]</td>
      <td>1648</td>
      <td>3576</td>
      <td>3576</td>
      <td>0.012887</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>1032</td>
      <td>3576</td>
      <td>3576</td>
      <td>0.008070</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_AUTHOR</td>
      <td>[Author, Git, Person]</td>
      <td>1000</td>
      <td>1</td>
      <td>1000</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_TAG</td>
      <td>[Git, Tag]</td>
      <td>906</td>
      <td>1</td>
      <td>906</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Git, Tag]</td>
      <td>ON_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>906</td>
      <td>906</td>
      <td>6744</td>
      <td>0.014828</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Json, Value, Object]</td>
      <td>HAS_KEY</td>
      <td>[Json, Key]</td>
      <td>668</td>
      <td>133</td>
      <td>668</td>
      <td>0.751880</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Json, Key]</td>
      <td>HAS_VALUE</td>
      <td>[Json, Value, Scalar]</td>
      <td>552</td>
      <td>668</td>
      <td>603</td>
      <td>0.137039</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMITTER</td>
      <td>[Committer, Git, Person]</td>
      <td>356</td>
      <td>1</td>
      <td>356</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[TS, Function]</td>
      <td>DEPENDS_ON</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>293</td>
      <td>47</td>
      <td>215</td>
      <td>2.899555</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[File, TS, Local, Module]</td>
      <td>DEPENDS_ON</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>236</td>
      <td>6</td>
      <td>215</td>
      <td>18.294574</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[TS, ExternalModule]</td>
      <td>EXPORTS</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>215</td>
      <td>11</td>
      <td>215</td>
      <td>9.090909</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 54308
    total_number_of_relationships (edges): 160177
    -> total directed graph density: 5.431009139905184e-05
    -> total directed graph density in percent: 0.005431009139905184

