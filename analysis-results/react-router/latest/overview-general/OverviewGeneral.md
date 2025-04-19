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
      <td>60310</td>
      <td>52.314739</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change, Create]</td>
      <td>18094</td>
      <td>15.695289</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>11441</td>
      <td>9.924273</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Change, Delete]</td>
      <td>8846</td>
      <td>7.673291</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Git]</td>
      <td>5953</td>
      <td>5.163814</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Rename]</td>
      <td>3403</td>
      <td>2.951866</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Tag]</td>
      <td>1843</td>
      <td>1.598675</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Author, Git, Person]</td>
      <td>1272</td>
      <td>1.103372</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Json, Key]</td>
      <td>668</td>
      <td>0.579444</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Json, Value, Scalar]</td>
      <td>603</td>
      <td>0.523061</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Committer, Git, Person]</td>
      <td>370</td>
      <td>0.320949</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[NPM, Dependency]</td>
      <td>338</td>
      <td>0.293192</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Type, TS, Primitive]</td>
      <td>293</td>
      <td>0.254157</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Type, TS, Declared]</td>
      <td>277</td>
      <td>0.240278</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[TS, ExternalDeclaration]</td>
      <td>215</td>
      <td>0.186498</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Git, Change, Copy]</td>
      <td>156</td>
      <td>0.135319</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Type, TS, Literal]</td>
      <td>136</td>
      <td>0.117971</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Json, Value, Object]</td>
      <td>133</td>
      <td>0.115368</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, TS, Union]</td>
      <td>120</td>
      <td>0.104092</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>103</td>
      <td>0.089345</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[NPM, Script]</td>
      <td>91</td>
      <td>0.078936</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[TS, Property]</td>
      <td>65</td>
      <td>0.056383</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[TS, Function]</td>
      <td>47</td>
      <td>0.040769</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, TS, FunctionParameter]</td>
      <td>40</td>
      <td>0.034697</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, Object, TS]</td>
      <td>39</td>
      <td>0.033830</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Git, Branch]</td>
      <td>37</td>
      <td>0.032095</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[File, Directory]</td>
      <td>34</td>
      <td>0.029493</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Type, TS, Function]</td>
      <td>34</td>
      <td>0.029493</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[TS, Parameter]</td>
      <td>33</td>
      <td>0.028625</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Package, File, Json, NPM]</td>
      <td>29</td>
      <td>0.025155</td>
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
      <td>0.000867</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[NPM, PublishConfig]</td>
      <td>1</td>
      <td>0.000867</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[File, TS, Scan]</td>
      <td>1</td>
      <td>0.000867</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[TS, Method]</td>
      <td>1</td>
      <td>0.000867</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000867</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[TS, Constructor]</td>
      <td>1</td>
      <td>0.000867</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Value, TS, ObjectMember]</td>
      <td>1</td>
      <td>0.000867</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[TS, Class]</td>
      <td>1</td>
      <td>0.000867</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[TS, Enum]</td>
      <td>2</td>
      <td>0.001735</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Value, Object, TS]</td>
      <td>3</td>
      <td>0.002602</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Type, TS, Tuple]</td>
      <td>3</td>
      <td>0.002602</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Value, TS, Function]</td>
      <td>4</td>
      <td>0.003470</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[TS, TypeParameter]</td>
      <td>4</td>
      <td>0.003470</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Value, TS, Complex]</td>
      <td>5</td>
      <td>0.004337</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Repository, NPM]</td>
      <td>5</td>
      <td>0.004337</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[NPM, Engine]</td>
      <td>6</td>
      <td>0.005205</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Project, TS]</td>
      <td>6</td>
      <td>0.005205</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[File, Local]</td>
      <td>6</td>
      <td>0.005205</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, TS, TypeParameterReference]</td>
      <td>6</td>
      <td>0.005205</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Value, TS, Member]</td>
      <td>6</td>
      <td>0.005205</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[File, TS, Local, Module]</td>
      <td>6</td>
      <td>0.005205</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Value, TS, Call]</td>
      <td>6</td>
      <td>0.005205</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[TS, EnumMember]</td>
      <td>8</td>
      <td>0.006939</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, TS, NotIdentified]</td>
      <td>11</td>
      <td>0.009542</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[TS, ExternalModule]</td>
      <td>11</td>
      <td>0.009542</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Json, Value, Array]</td>
      <td>12</td>
      <td>0.010409</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Value, TS, Declared]</td>
      <td>13</td>
      <td>0.011277</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[TS, TypeAlias]</td>
      <td>16</td>
      <td>0.013879</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[File, Directory, Local]</td>
      <td>16</td>
      <td>0.013879</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[TS, Interface]</td>
      <td>17</td>
      <td>0.014746</td>
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
      <td>111726</td>
      <td>96.914549</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>90809</td>
      <td>78.770504</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Update</td>
      <td>60310</td>
      <td>52.314739</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Create</td>
      <td>18094</td>
      <td>15.695289</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Commit</td>
      <td>11441</td>
      <td>9.924273</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Delete</td>
      <td>8846</td>
      <td>7.673291</td>
    </tr>
    <tr>
      <th>6</th>
      <td>File</td>
      <td>6046</td>
      <td>5.244485</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Rename</td>
      <td>3403</td>
      <td>2.951866</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Tag</td>
      <td>1843</td>
      <td>1.598675</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Person</td>
      <td>1642</td>
      <td>1.424321</td>
    </tr>
    <tr>
      <th>10</th>
      <td>TS</td>
      <td>1595</td>
      <td>1.383552</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Json</td>
      <td>1445</td>
      <td>1.253437</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Author</td>
      <td>1272</td>
      <td>1.103372</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Type</td>
      <td>1079</td>
      <td>0.935958</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Value</td>
      <td>806</td>
      <td>0.699149</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Key</td>
      <td>668</td>
      <td>0.579444</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Scalar</td>
      <td>603</td>
      <td>0.523061</td>
    </tr>
    <tr>
      <th>17</th>
      <td>NPM</td>
      <td>470</td>
      <td>0.407692</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Committer</td>
      <td>370</td>
      <td>0.320949</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Dependency</td>
      <td>338</td>
      <td>0.293192</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Primitive</td>
      <td>293</td>
      <td>0.254157</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Declared</td>
      <td>290</td>
      <td>0.251555</td>
    </tr>
    <tr>
      <th>22</th>
      <td>ExternalDeclaration</td>
      <td>215</td>
      <td>0.186498</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Object</td>
      <td>175</td>
      <td>0.151800</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Copy</td>
      <td>156</td>
      <td>0.135319</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Literal</td>
      <td>156</td>
      <td>0.135319</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Union</td>
      <td>120</td>
      <td>0.104092</td>
    </tr>
    <tr>
      <th>27</th>
      <td>ObjectMember</td>
      <td>104</td>
      <td>0.090213</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Script</td>
      <td>91</td>
      <td>0.078936</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Function</td>
      <td>85</td>
      <td>0.073732</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Property</td>
      <td>65</td>
      <td>0.056383</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Directory</td>
      <td>50</td>
      <td>0.043372</td>
    </tr>
    <tr>
      <th>32</th>
      <td>FunctionParameter</td>
      <td>40</td>
      <td>0.034697</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Branch</td>
      <td>37</td>
      <td>0.032095</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Parameter</td>
      <td>33</td>
      <td>0.028625</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Package</td>
      <td>29</td>
      <td>0.025155</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Local</td>
      <td>28</td>
      <td>0.024288</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Variable</td>
      <td>24</td>
      <td>0.020818</td>
    </tr>
    <tr>
      <th>38</th>
      <td>jQAssistant</td>
      <td>20</td>
      <td>0.017349</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Concept</td>
      <td>19</td>
      <td>0.016481</td>
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

    Total number of relationships: 346317





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
      <td>90809</td>
      <td>26.221352</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>90809</td>
      <td>26.221352</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>60310</td>
      <td>17.414681</td>
    </tr>
    <tr>
      <th>3</th>
      <td>COMMITTED</td>
      <td>22882</td>
      <td>6.607241</td>
    </tr>
    <tr>
      <th>4</th>
      <td>CREATES</td>
      <td>21653</td>
      <td>6.252364</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_PARENT</td>
      <td>12540</td>
      <td>3.620960</td>
    </tr>
    <tr>
      <th>6</th>
      <td>DELETES</td>
      <td>12249</td>
      <td>3.536933</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_COMMIT</td>
      <td>11441</td>
      <td>3.303621</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_FILE</td>
      <td>5953</td>
      <td>1.718945</td>
    </tr>
    <tr>
      <th>9</th>
      <td>RENAMES</td>
      <td>3403</td>
      <td>0.982626</td>
    </tr>
    <tr>
      <th>10</th>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>1931</td>
      <td>0.557582</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_TAG</td>
      <td>1843</td>
      <td>0.532171</td>
    </tr>
    <tr>
      <th>12</th>
      <td>ON_COMMIT</td>
      <td>1843</td>
      <td>0.532171</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_NEW_NAME</td>
      <td>1784</td>
      <td>0.515135</td>
    </tr>
    <tr>
      <th>14</th>
      <td>HAS_AUTHOR</td>
      <td>1272</td>
      <td>0.367294</td>
    </tr>
    <tr>
      <th>15</th>
      <td>DEPENDS_ON</td>
      <td>887</td>
      <td>0.256124</td>
    </tr>
    <tr>
      <th>16</th>
      <td>HAS_KEY</td>
      <td>668</td>
      <td>0.192887</td>
    </tr>
    <tr>
      <th>17</th>
      <td>HAS_VALUE</td>
      <td>668</td>
      <td>0.192887</td>
    </tr>
    <tr>
      <th>18</th>
      <td>CONTAINS</td>
      <td>596</td>
      <td>0.172097</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_COMMITTER</td>
      <td>370</td>
      <td>0.106839</td>
    </tr>
    <tr>
      <th>20</th>
      <td>OF_TYPE</td>
      <td>339</td>
      <td>0.097887</td>
    </tr>
    <tr>
      <th>21</th>
      <td>EXPORTS</td>
      <td>309</td>
      <td>0.089225</td>
    </tr>
    <tr>
      <th>22</th>
      <td>REFERENCES</td>
      <td>197</td>
      <td>0.056884</td>
    </tr>
    <tr>
      <th>23</th>
      <td>DECLARES</td>
      <td>186</td>
      <td>0.053708</td>
    </tr>
    <tr>
      <th>24</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>169</td>
      <td>0.048799</td>
    </tr>
    <tr>
      <th>25</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>161</td>
      <td>0.046489</td>
    </tr>
    <tr>
      <th>26</th>
      <td>COPIES</td>
      <td>156</td>
      <td>0.045045</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_MEMBER</td>
      <td>104</td>
      <td>0.030030</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>0.027143</td>
    </tr>
    <tr>
      <th>29</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.026277</td>
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
      <td>0.000289</td>
    </tr>
    <tr>
      <th>1</th>
      <td>CONSTRAINED_BY</td>
      <td>4</td>
      <td>0.001155</td>
    </tr>
    <tr>
      <th>2</th>
      <td>IN_REPOSITORY</td>
      <td>5</td>
      <td>0.001444</td>
    </tr>
    <tr>
      <th>3</th>
      <td>REFERENCED_PROJECTS</td>
      <td>5</td>
      <td>0.001444</td>
    </tr>
    <tr>
      <th>4</th>
      <td>PARENT</td>
      <td>6</td>
      <td>0.001733</td>
    </tr>
    <tr>
      <th>5</th>
      <td>MEMBER</td>
      <td>6</td>
      <td>0.001733</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_ROOT</td>
      <td>6</td>
      <td>0.001733</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_NPM_PACKAGE</td>
      <td>6</td>
      <td>0.001733</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_CONFIG</td>
      <td>6</td>
      <td>0.001733</td>
    </tr>
    <tr>
      <th>9</th>
      <td>HAS_ARGUMENT</td>
      <td>6</td>
      <td>0.001733</td>
    </tr>
    <tr>
      <th>10</th>
      <td>EXTENDS</td>
      <td>6</td>
      <td>0.001733</td>
    </tr>
    <tr>
      <th>11</th>
      <td>DECLARES_ENGINE</td>
      <td>6</td>
      <td>0.001733</td>
    </tr>
    <tr>
      <th>12</th>
      <td>CONTAINS_PROJECT</td>
      <td>6</td>
      <td>0.001733</td>
    </tr>
    <tr>
      <th>13</th>
      <td>CALLS</td>
      <td>6</td>
      <td>0.001733</td>
    </tr>
    <tr>
      <th>14</th>
      <td>DECLARES_PEER_DEPENDENCY</td>
      <td>8</td>
      <td>0.002310</td>
    </tr>
    <tr>
      <th>15</th>
      <td>USES</td>
      <td>11</td>
      <td>0.003176</td>
    </tr>
    <tr>
      <th>16</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.005486</td>
    </tr>
    <tr>
      <th>17</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.008085</td>
    </tr>
    <tr>
      <th>18</th>
      <td>INITIALIZED_WITH</td>
      <td>32</td>
      <td>0.009240</td>
    </tr>
    <tr>
      <th>19</th>
      <td>IS_DESCRIBED_IN_NPM_PACKAGE</td>
      <td>33</td>
      <td>0.009529</td>
    </tr>
    <tr>
      <th>20</th>
      <td>HAS_BRANCH</td>
      <td>37</td>
      <td>0.010684</td>
    </tr>
    <tr>
      <th>21</th>
      <td>HAS_HEAD</td>
      <td>38</td>
      <td>0.010973</td>
    </tr>
    <tr>
      <th>22</th>
      <td>RESOLVES_TO</td>
      <td>41</td>
      <td>0.011839</td>
    </tr>
    <tr>
      <th>23</th>
      <td>CONTAINS_VALUE</td>
      <td>51</td>
      <td>0.014726</td>
    </tr>
    <tr>
      <th>24</th>
      <td>COPY_OF</td>
      <td>72</td>
      <td>0.020790</td>
    </tr>
    <tr>
      <th>25</th>
      <td>HAS_PARAMETER</td>
      <td>73</td>
      <td>0.021079</td>
    </tr>
    <tr>
      <th>26</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>0.023678</td>
    </tr>
    <tr>
      <th>27</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.026277</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>0.027143</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_MEMBER</td>
      <td>104</td>
      <td>0.030030</td>
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
      <td>[Git, Update, Change]</td>
      <td>60310</td>
      <td>11441</td>
      <td>60310</td>
      <td>0.008740</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Update, Change]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>60310</td>
      <td>60310</td>
      <td>5953</td>
      <td>0.016798</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Update, Change]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>60310</td>
      <td>60310</td>
      <td>5953</td>
      <td>0.016798</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>18094</td>
      <td>11441</td>
      <td>18094</td>
      <td>0.008740</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>18094</td>
      <td>18094</td>
      <td>5953</td>
      <td>0.016798</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>18094</td>
      <td>18094</td>
      <td>5953</td>
      <td>0.016798</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>12540</td>
      <td>11441</td>
      <td>11441</td>
      <td>0.009580</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>11441</td>
      <td>1</td>
      <td>11441</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>11441</td>
      <td>1272</td>
      <td>11441</td>
      <td>0.078616</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>11441</td>
      <td>370</td>
      <td>11441</td>
      <td>0.270270</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>8846</td>
      <td>11441</td>
      <td>8846</td>
      <td>0.008740</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>8846</td>
      <td>8846</td>
      <td>5953</td>
      <td>0.016798</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>8846</td>
      <td>8846</td>
      <td>5953</td>
      <td>0.016798</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>5953</td>
      <td>1</td>
      <td>5953</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>3403</td>
      <td>11441</td>
      <td>3403</td>
      <td>0.008740</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>3403</td>
      <td>3403</td>
      <td>5953</td>
      <td>0.016798</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>3403</td>
      <td>3403</td>
      <td>5953</td>
      <td>0.016798</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>3403</td>
      <td>3403</td>
      <td>5953</td>
      <td>0.016798</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>3403</td>
      <td>3403</td>
      <td>5953</td>
      <td>0.016798</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_TAG</td>
      <td>[Git, Tag]</td>
      <td>1843</td>
      <td>1</td>
      <td>1843</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Git, Tag]</td>
      <td>ON_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>1843</td>
      <td>1843</td>
      <td>11441</td>
      <td>0.008740</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>1784</td>
      <td>5953</td>
      <td>5953</td>
      <td>0.005034</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[File, Git]</td>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>[File, Git]</td>
      <td>1676</td>
      <td>5953</td>
      <td>5953</td>
      <td>0.004729</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_AUTHOR</td>
      <td>[Author, Git, Person]</td>
      <td>1272</td>
      <td>1</td>
      <td>1272</td>
      <td>100.000000</td>
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
      <td>370</td>
      <td>1</td>
      <td>370</td>
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
      <td>[Package, File, Json, NPM]</td>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>[Package, File, Json, NPM]</td>
      <td>253</td>
      <td>29</td>
      <td>29</td>
      <td>30.083234</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[File, TS, Local, Module]</td>
      <td>DEPENDS_ON</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>236</td>
      <td>6</td>
      <td>215</td>
      <td>18.294574</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 115283
    total_number_of_relationships (edges): 346317
    -> total directed graph density: 2.6058357550463212e-05
    -> total directed graph density in percent: 0.0026058357550463214

