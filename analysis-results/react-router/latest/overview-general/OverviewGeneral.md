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
      <td>26453</td>
      <td>48.605395</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Commit]</td>
      <td>6754</td>
      <td>12.409966</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change, Create]</td>
      <td>5851</td>
      <td>10.750772</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Change, Delete]</td>
      <td>4197</td>
      <td>7.711671</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Git]</td>
      <td>3579</td>
      <td>6.576143</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Rename]</td>
      <td>1699</td>
      <td>3.121785</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Author, Git, Person]</td>
      <td>1000</td>
      <td>1.837425</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Tag]</td>
      <td>916</td>
      <td>1.683081</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Json, Key]</td>
      <td>668</td>
      <td>1.227400</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Json, Value, Scalar]</td>
      <td>603</td>
      <td>1.107967</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Committer, Git, Person]</td>
      <td>356</td>
      <td>0.654123</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[NPM, Dependency]</td>
      <td>338</td>
      <td>0.621050</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Type, TS, Primitive]</td>
      <td>294</td>
      <td>0.540203</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Type, TS, Declared]</td>
      <td>294</td>
      <td>0.540203</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[TS, ExternalDeclaration]</td>
      <td>215</td>
      <td>0.395046</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Type, TS, Literal]</td>
      <td>138</td>
      <td>0.253565</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Json, Value, Object]</td>
      <td>133</td>
      <td>0.244377</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Type, TS, Union]</td>
      <td>121</td>
      <td>0.222328</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>111</td>
      <td>0.203954</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[NPM, Script]</td>
      <td>91</td>
      <td>0.167206</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[TS, Property]</td>
      <td>65</td>
      <td>0.119433</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[TS, Function]</td>
      <td>47</td>
      <td>0.086359</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[TS, Parameter]</td>
      <td>44</td>
      <td>0.080847</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, Object, TS]</td>
      <td>42</td>
      <td>0.077172</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, TS, FunctionParameter]</td>
      <td>40</td>
      <td>0.073497</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[File, Directory]</td>
      <td>34</td>
      <td>0.062472</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, TS, Function]</td>
      <td>34</td>
      <td>0.062472</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Package, File, Json, NPM]</td>
      <td>29</td>
      <td>0.053285</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[TS, Variable]</td>
      <td>24</td>
      <td>0.044098</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Value, TS, Literal]</td>
      <td>20</td>
      <td>0.036748</td>
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
      <td>0.001837</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[NPM, PublishConfig]</td>
      <td>1</td>
      <td>0.001837</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[TS, Class]</td>
      <td>1</td>
      <td>0.001837</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[TS, Constructor]</td>
      <td>1</td>
      <td>0.001837</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Branch]</td>
      <td>1</td>
      <td>0.001837</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Value, TS, ObjectMember]</td>
      <td>1</td>
      <td>0.001837</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.001837</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[TS, Method]</td>
      <td>1</td>
      <td>0.001837</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[TS, Enum]</td>
      <td>2</td>
      <td>0.003675</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Value, Object, TS]</td>
      <td>3</td>
      <td>0.005512</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Type, TS, Tuple]</td>
      <td>3</td>
      <td>0.005512</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Value, TS, Function]</td>
      <td>4</td>
      <td>0.007350</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[TS, TypeParameter]</td>
      <td>4</td>
      <td>0.007350</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Repository, NPM]</td>
      <td>5</td>
      <td>0.009187</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[File, TS, Scan]</td>
      <td>5</td>
      <td>0.009187</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[File, Local]</td>
      <td>5</td>
      <td>0.009187</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Value, TS, Complex]</td>
      <td>5</td>
      <td>0.009187</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Project, TS]</td>
      <td>5</td>
      <td>0.009187</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Value, TS, Call]</td>
      <td>6</td>
      <td>0.011025</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Value, TS, Member]</td>
      <td>6</td>
      <td>0.011025</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Type, TS, TypeParameterReference]</td>
      <td>6</td>
      <td>0.011025</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[File, TS, Local, Module]</td>
      <td>6</td>
      <td>0.011025</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[NPM, Engine]</td>
      <td>6</td>
      <td>0.011025</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[TS, EnumMember]</td>
      <td>8</td>
      <td>0.014699</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, TS, NotIdentified]</td>
      <td>11</td>
      <td>0.020212</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[TS, ExternalModule]</td>
      <td>11</td>
      <td>0.020212</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Json, Value, Array]</td>
      <td>12</td>
      <td>0.022049</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Value, TS, Declared]</td>
      <td>13</td>
      <td>0.023887</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Git, Change, Copy]</td>
      <td>15</td>
      <td>0.027561</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[TS, TypeAlias]</td>
      <td>16</td>
      <td>0.029399</td>
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
      <td>50822</td>
      <td>93.381596</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>38215</td>
      <td>70.217184</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Update</td>
      <td>26453</td>
      <td>48.605395</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Commit</td>
      <td>6754</td>
      <td>12.409966</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Create</td>
      <td>5851</td>
      <td>10.750772</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Delete</td>
      <td>4197</td>
      <td>7.711671</td>
    </tr>
    <tr>
      <th>6</th>
      <td>File</td>
      <td>3675</td>
      <td>6.752536</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Rename</td>
      <td>1699</td>
      <td>3.121785</td>
    </tr>
    <tr>
      <th>8</th>
      <td>TS</td>
      <td>1641</td>
      <td>3.015214</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Json</td>
      <td>1445</td>
      <td>2.655079</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Person</td>
      <td>1356</td>
      <td>2.491548</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Type</td>
      <td>1111</td>
      <td>2.041379</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Author</td>
      <td>1000</td>
      <td>1.837425</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Tag</td>
      <td>916</td>
      <td>1.683081</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Value</td>
      <td>806</td>
      <td>1.480964</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Key</td>
      <td>668</td>
      <td>1.227400</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Scalar</td>
      <td>603</td>
      <td>1.107967</td>
    </tr>
    <tr>
      <th>17</th>
      <td>NPM</td>
      <td>470</td>
      <td>0.863590</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Committer</td>
      <td>356</td>
      <td>0.654123</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Dependency</td>
      <td>338</td>
      <td>0.621050</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Declared</td>
      <td>307</td>
      <td>0.564089</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Primitive</td>
      <td>294</td>
      <td>0.540203</td>
    </tr>
    <tr>
      <th>22</th>
      <td>ExternalDeclaration</td>
      <td>215</td>
      <td>0.395046</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Object</td>
      <td>178</td>
      <td>0.327062</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Literal</td>
      <td>158</td>
      <td>0.290313</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Union</td>
      <td>121</td>
      <td>0.222328</td>
    </tr>
    <tr>
      <th>26</th>
      <td>ObjectMember</td>
      <td>112</td>
      <td>0.205792</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Script</td>
      <td>91</td>
      <td>0.167206</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Function</td>
      <td>85</td>
      <td>0.156181</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Property</td>
      <td>65</td>
      <td>0.119433</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Directory</td>
      <td>50</td>
      <td>0.091871</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Parameter</td>
      <td>44</td>
      <td>0.080847</td>
    </tr>
    <tr>
      <th>32</th>
      <td>FunctionParameter</td>
      <td>40</td>
      <td>0.073497</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Package</td>
      <td>29</td>
      <td>0.053285</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Local</td>
      <td>27</td>
      <td>0.049610</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Variable</td>
      <td>24</td>
      <td>0.044098</td>
    </tr>
    <tr>
      <th>36</th>
      <td>jQAssistant</td>
      <td>20</td>
      <td>0.036748</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Concept</td>
      <td>19</td>
      <td>0.034911</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Rule</td>
      <td>19</td>
      <td>0.034911</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Interface</td>
      <td>17</td>
      <td>0.031236</td>
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

    Total number of relationships: 160357





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
      <td>38215</td>
      <td>23.831202</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>38215</td>
      <td>23.831202</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>26453</td>
      <td>16.496318</td>
    </tr>
    <tr>
      <th>3</th>
      <td>COMMITTED</td>
      <td>13508</td>
      <td>8.423705</td>
    </tr>
    <tr>
      <th>4</th>
      <td>CREATES</td>
      <td>7565</td>
      <td>4.717599</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_PARENT</td>
      <td>7528</td>
      <td>4.694525</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_COMMIT</td>
      <td>6754</td>
      <td>4.211852</td>
    </tr>
    <tr>
      <th>7</th>
      <td>DELETES</td>
      <td>5896</td>
      <td>3.676796</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_FILE</td>
      <td>3579</td>
      <td>2.231895</td>
    </tr>
    <tr>
      <th>9</th>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>1725</td>
      <td>1.075725</td>
    </tr>
    <tr>
      <th>10</th>
      <td>RENAMES</td>
      <td>1699</td>
      <td>1.059511</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_NEW_NAME</td>
      <td>1032</td>
      <td>0.643564</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS_AUTHOR</td>
      <td>1000</td>
      <td>0.623609</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_TAG</td>
      <td>916</td>
      <td>0.571225</td>
    </tr>
    <tr>
      <th>14</th>
      <td>ON_COMMIT</td>
      <td>916</td>
      <td>0.571225</td>
    </tr>
    <tr>
      <th>15</th>
      <td>DEPENDS_ON</td>
      <td>888</td>
      <td>0.553764</td>
    </tr>
    <tr>
      <th>16</th>
      <td>HAS_KEY</td>
      <td>668</td>
      <td>0.416571</td>
    </tr>
    <tr>
      <th>17</th>
      <td>HAS_VALUE</td>
      <td>668</td>
      <td>0.416571</td>
    </tr>
    <tr>
      <th>18</th>
      <td>CONTAINS</td>
      <td>598</td>
      <td>0.372918</td>
    </tr>
    <tr>
      <th>19</th>
      <td>OF_TYPE</td>
      <td>358</td>
      <td>0.223252</td>
    </tr>
    <tr>
      <th>20</th>
      <td>HAS_COMMITTER</td>
      <td>356</td>
      <td>0.222005</td>
    </tr>
    <tr>
      <th>21</th>
      <td>EXPORTS</td>
      <td>309</td>
      <td>0.192695</td>
    </tr>
    <tr>
      <th>22</th>
      <td>REFERENCES</td>
      <td>212</td>
      <td>0.132205</td>
    </tr>
    <tr>
      <th>23</th>
      <td>DECLARES</td>
      <td>186</td>
      <td>0.115991</td>
    </tr>
    <tr>
      <th>24</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>169</td>
      <td>0.105390</td>
    </tr>
    <tr>
      <th>25</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>161</td>
      <td>0.100401</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_MEMBER</td>
      <td>112</td>
      <td>0.069844</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>96</td>
      <td>0.059866</td>
    </tr>
    <tr>
      <th>28</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.056748</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_PARAMETER</td>
      <td>84</td>
      <td>0.052383</td>
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
      <td>0.001247</td>
    </tr>
    <tr>
      <th>3</th>
      <td>CONSTRAINED_BY</td>
      <td>4</td>
      <td>0.002494</td>
    </tr>
    <tr>
      <th>4</th>
      <td>IN_REPOSITORY</td>
      <td>5</td>
      <td>0.003118</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_ROOT</td>
      <td>5</td>
      <td>0.003118</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_NPM_PACKAGE</td>
      <td>5</td>
      <td>0.003118</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_CONFIG</td>
      <td>5</td>
      <td>0.003118</td>
    </tr>
    <tr>
      <th>8</th>
      <td>CONTAINS_PROJECT</td>
      <td>5</td>
      <td>0.003118</td>
    </tr>
    <tr>
      <th>9</th>
      <td>DECLARES_ENGINE</td>
      <td>6</td>
      <td>0.003742</td>
    </tr>
    <tr>
      <th>10</th>
      <td>EXTENDS</td>
      <td>6</td>
      <td>0.003742</td>
    </tr>
    <tr>
      <th>11</th>
      <td>CALLS</td>
      <td>6</td>
      <td>0.003742</td>
    </tr>
    <tr>
      <th>12</th>
      <td>MEMBER</td>
      <td>6</td>
      <td>0.003742</td>
    </tr>
    <tr>
      <th>13</th>
      <td>PARENT</td>
      <td>6</td>
      <td>0.003742</td>
    </tr>
    <tr>
      <th>14</th>
      <td>HAS_ARGUMENT</td>
      <td>6</td>
      <td>0.003742</td>
    </tr>
    <tr>
      <th>15</th>
      <td>DECLARES_PEER_DEPENDENCY</td>
      <td>8</td>
      <td>0.004989</td>
    </tr>
    <tr>
      <th>16</th>
      <td>USES</td>
      <td>11</td>
      <td>0.006860</td>
    </tr>
    <tr>
      <th>17</th>
      <td>COPY_OF</td>
      <td>12</td>
      <td>0.007483</td>
    </tr>
    <tr>
      <th>18</th>
      <td>COPIES</td>
      <td>15</td>
      <td>0.009354</td>
    </tr>
    <tr>
      <th>19</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.011849</td>
    </tr>
    <tr>
      <th>20</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.017461</td>
    </tr>
    <tr>
      <th>21</th>
      <td>INITIALIZED_WITH</td>
      <td>32</td>
      <td>0.019955</td>
    </tr>
    <tr>
      <th>22</th>
      <td>IS_DESCRIBED_IN_NPM_PACKAGE</td>
      <td>33</td>
      <td>0.020579</td>
    </tr>
    <tr>
      <th>23</th>
      <td>RESOLVES_TO</td>
      <td>40</td>
      <td>0.024944</td>
    </tr>
    <tr>
      <th>24</th>
      <td>CONTAINS_VALUE</td>
      <td>51</td>
      <td>0.031804</td>
    </tr>
    <tr>
      <th>25</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>0.051136</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_PARAMETER</td>
      <td>84</td>
      <td>0.052383</td>
    </tr>
    <tr>
      <th>27</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.056748</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>96</td>
      <td>0.059866</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_MEMBER</td>
      <td>112</td>
      <td>0.069844</td>
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
      <td>26453</td>
      <td>26453</td>
      <td>3579</td>
      <td>0.027941</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Update, Change]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>26453</td>
      <td>26453</td>
      <td>3579</td>
      <td>0.027941</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Update, Change]</td>
      <td>26453</td>
      <td>6754</td>
      <td>26453</td>
      <td>0.014806</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>7528</td>
      <td>6754</td>
      <td>6754</td>
      <td>0.016503</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>6754</td>
      <td>1</td>
      <td>6754</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>6754</td>
      <td>1000</td>
      <td>6754</td>
      <td>0.100000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>6754</td>
      <td>356</td>
      <td>6754</td>
      <td>0.280899</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>5851</td>
      <td>5851</td>
      <td>3579</td>
      <td>0.027941</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>5851</td>
      <td>5851</td>
      <td>3579</td>
      <td>0.027941</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>5851</td>
      <td>6754</td>
      <td>5851</td>
      <td>0.014806</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>4197</td>
      <td>6754</td>
      <td>4197</td>
      <td>0.014806</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>4197</td>
      <td>4197</td>
      <td>3579</td>
      <td>0.027941</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>4197</td>
      <td>4197</td>
      <td>3579</td>
      <td>0.027941</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>3579</td>
      <td>1</td>
      <td>3579</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>1699</td>
      <td>6754</td>
      <td>1699</td>
      <td>0.014806</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>1699</td>
      <td>1699</td>
      <td>3579</td>
      <td>0.027941</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>1699</td>
      <td>1699</td>
      <td>3579</td>
      <td>0.027941</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>1699</td>
      <td>1699</td>
      <td>3579</td>
      <td>0.027941</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>1699</td>
      <td>1699</td>
      <td>3579</td>
      <td>0.027941</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[File, Git]</td>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>[File, Git]</td>
      <td>1578</td>
      <td>3579</td>
      <td>3579</td>
      <td>0.012319</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>1032</td>
      <td>3579</td>
      <td>3579</td>
      <td>0.008057</td>
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
      <td>916</td>
      <td>1</td>
      <td>916</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Git, Tag]</td>
      <td>ON_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>916</td>
      <td>916</td>
      <td>6754</td>
      <td>0.014806</td>
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

    total_number_of_nodes (vertices): 54424
    total_number_of_relationships (edges): 160357
    -> total directed graph density: 5.413959302129778e-05
    -> total directed graph density in percent: 0.005413959302129778

