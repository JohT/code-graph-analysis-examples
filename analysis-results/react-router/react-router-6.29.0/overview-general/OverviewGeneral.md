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
      <td>57800</td>
      <td>52.208473</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change, Create]</td>
      <td>16910</td>
      <td>15.274140</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>11176</td>
      <td>10.094842</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Change, Delete]</td>
      <td>8703</td>
      <td>7.861078</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, Git]</td>
      <td>5776</td>
      <td>5.217234</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Rename]</td>
      <td>3315</td>
      <td>2.994309</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Tag]</td>
      <td>1703</td>
      <td>1.538253</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Author, Git, Person]</td>
      <td>1261</td>
      <td>1.139012</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Json, Key]</td>
      <td>668</td>
      <td>0.603378</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Json, Value, Scalar]</td>
      <td>603</td>
      <td>0.544666</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Committer, Git, Person]</td>
      <td>370</td>
      <td>0.334206</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[NPM, Dependency]</td>
      <td>338</td>
      <td>0.305302</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Type, TS, Primitive]</td>
      <td>291</td>
      <td>0.262849</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Type, TS, Declared]</td>
      <td>277</td>
      <td>0.250203</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[TS, ExternalDeclaration]</td>
      <td>215</td>
      <td>0.194201</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Type, TS, Literal]</td>
      <td>136</td>
      <td>0.122843</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Json, Value, Object]</td>
      <td>133</td>
      <td>0.120134</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Type, TS, Union]</td>
      <td>119</td>
      <td>0.107488</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>102</td>
      <td>0.092133</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Git, Change, Copy]</td>
      <td>102</td>
      <td>0.092133</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[NPM, Script]</td>
      <td>91</td>
      <td>0.082197</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[TS, Property]</td>
      <td>65</td>
      <td>0.058712</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[TS, Function]</td>
      <td>47</td>
      <td>0.042453</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, TS, FunctionParameter]</td>
      <td>40</td>
      <td>0.036130</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Git, Branch]</td>
      <td>40</td>
      <td>0.036130</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, Object, TS]</td>
      <td>39</td>
      <td>0.035227</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[File, Directory]</td>
      <td>34</td>
      <td>0.030711</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Type, TS, Function]</td>
      <td>34</td>
      <td>0.030711</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[TS, Parameter]</td>
      <td>33</td>
      <td>0.029808</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Package, File, Json, NPM]</td>
      <td>29</td>
      <td>0.026195</td>
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
      <td>0.000903</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[NPM, PublishConfig]</td>
      <td>1</td>
      <td>0.000903</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[File, TS, Scan]</td>
      <td>1</td>
      <td>0.000903</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[TS, Method]</td>
      <td>1</td>
      <td>0.000903</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000903</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[TS, Constructor]</td>
      <td>1</td>
      <td>0.000903</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Value, TS, ObjectMember]</td>
      <td>1</td>
      <td>0.000903</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[TS, Class]</td>
      <td>1</td>
      <td>0.000903</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[TS, Enum]</td>
      <td>2</td>
      <td>0.001807</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Value, Object, TS]</td>
      <td>3</td>
      <td>0.002710</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Type, TS, Tuple]</td>
      <td>3</td>
      <td>0.002710</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Value, TS, Function]</td>
      <td>4</td>
      <td>0.003613</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[TS, TypeParameter]</td>
      <td>4</td>
      <td>0.003613</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Value, TS, Complex]</td>
      <td>5</td>
      <td>0.004516</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Repository, NPM]</td>
      <td>5</td>
      <td>0.004516</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[NPM, Engine]</td>
      <td>6</td>
      <td>0.005420</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Project, TS]</td>
      <td>6</td>
      <td>0.005420</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[File, Local]</td>
      <td>6</td>
      <td>0.005420</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, TS, TypeParameterReference]</td>
      <td>6</td>
      <td>0.005420</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Value, TS, Member]</td>
      <td>6</td>
      <td>0.005420</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[File, TS, Local, Module]</td>
      <td>6</td>
      <td>0.005420</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Value, TS, Call]</td>
      <td>6</td>
      <td>0.005420</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[TS, EnumMember]</td>
      <td>8</td>
      <td>0.007226</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, TS, NotIdentified]</td>
      <td>11</td>
      <td>0.009936</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[TS, ExternalModule]</td>
      <td>11</td>
      <td>0.009936</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Json, Value, Array]</td>
      <td>12</td>
      <td>0.010839</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Value, TS, Declared]</td>
      <td>13</td>
      <td>0.011742</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[TS, TypeAlias]</td>
      <td>16</td>
      <td>0.014452</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[File, Directory, Local]</td>
      <td>16</td>
      <td>0.014452</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[TS, Interface]</td>
      <td>17</td>
      <td>0.015355</td>
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
      <td>107157</td>
      <td>96.790714</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>86830</td>
      <td>78.430133</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Update</td>
      <td>57800</td>
      <td>52.208473</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Create</td>
      <td>16910</td>
      <td>15.274140</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Commit</td>
      <td>11176</td>
      <td>10.094842</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Delete</td>
      <td>8703</td>
      <td>7.861078</td>
    </tr>
    <tr>
      <th>6</th>
      <td>File</td>
      <td>5869</td>
      <td>5.301237</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Rename</td>
      <td>3315</td>
      <td>2.994309</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Tag</td>
      <td>1703</td>
      <td>1.538253</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Person</td>
      <td>1631</td>
      <td>1.473218</td>
    </tr>
    <tr>
      <th>10</th>
      <td>TS</td>
      <td>1591</td>
      <td>1.437088</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Json</td>
      <td>1445</td>
      <td>1.305212</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Author</td>
      <td>1261</td>
      <td>1.139012</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Type</td>
      <td>1075</td>
      <td>0.971005</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Value</td>
      <td>806</td>
      <td>0.728028</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Key</td>
      <td>668</td>
      <td>0.603378</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Scalar</td>
      <td>603</td>
      <td>0.544666</td>
    </tr>
    <tr>
      <th>17</th>
      <td>NPM</td>
      <td>470</td>
      <td>0.424533</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Committer</td>
      <td>370</td>
      <td>0.334206</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Dependency</td>
      <td>338</td>
      <td>0.305302</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Primitive</td>
      <td>291</td>
      <td>0.262849</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Declared</td>
      <td>290</td>
      <td>0.261946</td>
    </tr>
    <tr>
      <th>22</th>
      <td>ExternalDeclaration</td>
      <td>215</td>
      <td>0.194201</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Object</td>
      <td>175</td>
      <td>0.158071</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Literal</td>
      <td>156</td>
      <td>0.140909</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Union</td>
      <td>119</td>
      <td>0.107488</td>
    </tr>
    <tr>
      <th>26</th>
      <td>ObjectMember</td>
      <td>103</td>
      <td>0.093036</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Copy</td>
      <td>102</td>
      <td>0.092133</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Script</td>
      <td>91</td>
      <td>0.082197</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Function</td>
      <td>85</td>
      <td>0.076777</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Property</td>
      <td>65</td>
      <td>0.058712</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Directory</td>
      <td>50</td>
      <td>0.045163</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Branch</td>
      <td>40</td>
      <td>0.036130</td>
    </tr>
    <tr>
      <th>33</th>
      <td>FunctionParameter</td>
      <td>40</td>
      <td>0.036130</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Parameter</td>
      <td>33</td>
      <td>0.029808</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Package</td>
      <td>29</td>
      <td>0.026195</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Local</td>
      <td>28</td>
      <td>0.025291</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Variable</td>
      <td>24</td>
      <td>0.021678</td>
    </tr>
    <tr>
      <th>38</th>
      <td>jQAssistant</td>
      <td>20</td>
      <td>0.018065</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Concept</td>
      <td>19</td>
      <td>0.017162</td>
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

    Total number of relationships: 330628





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
      <td>86830</td>
      <td>26.262144</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>86830</td>
      <td>26.262144</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>57800</td>
      <td>17.481883</td>
    </tr>
    <tr>
      <th>3</th>
      <td>COMMITTED</td>
      <td>22352</td>
      <td>6.760468</td>
    </tr>
    <tr>
      <th>4</th>
      <td>CREATES</td>
      <td>20327</td>
      <td>6.147997</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_PARENT</td>
      <td>12251</td>
      <td>3.705373</td>
    </tr>
    <tr>
      <th>6</th>
      <td>DELETES</td>
      <td>12018</td>
      <td>3.634901</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_COMMIT</td>
      <td>11176</td>
      <td>3.380234</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_FILE</td>
      <td>5776</td>
      <td>1.746978</td>
    </tr>
    <tr>
      <th>9</th>
      <td>RENAMES</td>
      <td>3315</td>
      <td>1.002637</td>
    </tr>
    <tr>
      <th>10</th>
      <td>HAS_NEW_NAME</td>
      <td>1763</td>
      <td>0.533228</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_TAG</td>
      <td>1703</td>
      <td>0.515080</td>
    </tr>
    <tr>
      <th>12</th>
      <td>ON_COMMIT</td>
      <td>1703</td>
      <td>0.515080</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_AUTHOR</td>
      <td>1261</td>
      <td>0.381395</td>
    </tr>
    <tr>
      <th>14</th>
      <td>DEPENDS_ON</td>
      <td>887</td>
      <td>0.268277</td>
    </tr>
    <tr>
      <th>15</th>
      <td>HAS_KEY</td>
      <td>668</td>
      <td>0.202040</td>
    </tr>
    <tr>
      <th>16</th>
      <td>HAS_VALUE</td>
      <td>668</td>
      <td>0.202040</td>
    </tr>
    <tr>
      <th>17</th>
      <td>CONTAINS</td>
      <td>594</td>
      <td>0.179658</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_COMMITTER</td>
      <td>370</td>
      <td>0.111908</td>
    </tr>
    <tr>
      <th>19</th>
      <td>OF_TYPE</td>
      <td>338</td>
      <td>0.102230</td>
    </tr>
    <tr>
      <th>20</th>
      <td>EXPORTS</td>
      <td>309</td>
      <td>0.093459</td>
    </tr>
    <tr>
      <th>21</th>
      <td>REFERENCES</td>
      <td>197</td>
      <td>0.059584</td>
    </tr>
    <tr>
      <th>22</th>
      <td>DECLARES</td>
      <td>186</td>
      <td>0.056257</td>
    </tr>
    <tr>
      <th>23</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>169</td>
      <td>0.051115</td>
    </tr>
    <tr>
      <th>24</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>161</td>
      <td>0.048695</td>
    </tr>
    <tr>
      <th>25</th>
      <td>HAS_MEMBER</td>
      <td>103</td>
      <td>0.031153</td>
    </tr>
    <tr>
      <th>26</th>
      <td>COPIES</td>
      <td>102</td>
      <td>0.030850</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>0.028431</td>
    </tr>
    <tr>
      <th>28</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.027523</td>
    </tr>
    <tr>
      <th>29</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>0.024801</td>
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
      <td>DECLARES_PUBLISH_CONFIG</td>
      <td>1</td>
      <td>0.000302</td>
    </tr>
    <tr>
      <th>1</th>
      <td>CONSTRAINED_BY</td>
      <td>4</td>
      <td>0.001210</td>
    </tr>
    <tr>
      <th>2</th>
      <td>IN_REPOSITORY</td>
      <td>5</td>
      <td>0.001512</td>
    </tr>
    <tr>
      <th>3</th>
      <td>REFERENCED_PROJECTS</td>
      <td>5</td>
      <td>0.001512</td>
    </tr>
    <tr>
      <th>4</th>
      <td>PARENT</td>
      <td>6</td>
      <td>0.001815</td>
    </tr>
    <tr>
      <th>5</th>
      <td>MEMBER</td>
      <td>6</td>
      <td>0.001815</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_ROOT</td>
      <td>6</td>
      <td>0.001815</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_NPM_PACKAGE</td>
      <td>6</td>
      <td>0.001815</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_CONFIG</td>
      <td>6</td>
      <td>0.001815</td>
    </tr>
    <tr>
      <th>9</th>
      <td>HAS_ARGUMENT</td>
      <td>6</td>
      <td>0.001815</td>
    </tr>
    <tr>
      <th>10</th>
      <td>EXTENDS</td>
      <td>6</td>
      <td>0.001815</td>
    </tr>
    <tr>
      <th>11</th>
      <td>DECLARES_ENGINE</td>
      <td>6</td>
      <td>0.001815</td>
    </tr>
    <tr>
      <th>12</th>
      <td>CONTAINS_PROJECT</td>
      <td>6</td>
      <td>0.001815</td>
    </tr>
    <tr>
      <th>13</th>
      <td>CALLS</td>
      <td>6</td>
      <td>0.001815</td>
    </tr>
    <tr>
      <th>14</th>
      <td>DECLARES_PEER_DEPENDENCY</td>
      <td>8</td>
      <td>0.002420</td>
    </tr>
    <tr>
      <th>15</th>
      <td>USES</td>
      <td>11</td>
      <td>0.003327</td>
    </tr>
    <tr>
      <th>16</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.005747</td>
    </tr>
    <tr>
      <th>17</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.008469</td>
    </tr>
    <tr>
      <th>18</th>
      <td>INITIALIZED_WITH</td>
      <td>32</td>
      <td>0.009679</td>
    </tr>
    <tr>
      <th>19</th>
      <td>IS_DESCRIBED_IN_NPM_PACKAGE</td>
      <td>33</td>
      <td>0.009981</td>
    </tr>
    <tr>
      <th>20</th>
      <td>HAS_BRANCH</td>
      <td>40</td>
      <td>0.012098</td>
    </tr>
    <tr>
      <th>21</th>
      <td>RESOLVES_TO</td>
      <td>41</td>
      <td>0.012401</td>
    </tr>
    <tr>
      <th>22</th>
      <td>HAS_HEAD</td>
      <td>41</td>
      <td>0.012401</td>
    </tr>
    <tr>
      <th>23</th>
      <td>CONTAINS_VALUE</td>
      <td>51</td>
      <td>0.015425</td>
    </tr>
    <tr>
      <th>24</th>
      <td>COPY_OF</td>
      <td>52</td>
      <td>0.015728</td>
    </tr>
    <tr>
      <th>25</th>
      <td>HAS_PARAMETER</td>
      <td>73</td>
      <td>0.022079</td>
    </tr>
    <tr>
      <th>26</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>0.024801</td>
    </tr>
    <tr>
      <th>27</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.027523</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>0.028431</td>
    </tr>
    <tr>
      <th>29</th>
      <td>COPIES</td>
      <td>102</td>
      <td>0.030850</td>
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
      <td>57800</td>
      <td>57800</td>
      <td>5776</td>
      <td>0.017313</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Update, Change]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>57800</td>
      <td>57800</td>
      <td>5776</td>
      <td>0.017313</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Update, Change]</td>
      <td>57800</td>
      <td>11176</td>
      <td>57800</td>
      <td>0.008948</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>16910</td>
      <td>11176</td>
      <td>16910</td>
      <td>0.008948</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>16910</td>
      <td>16910</td>
      <td>5776</td>
      <td>0.017313</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>16910</td>
      <td>16910</td>
      <td>5776</td>
      <td>0.017313</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>12251</td>
      <td>11176</td>
      <td>11176</td>
      <td>0.009808</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>11176</td>
      <td>1</td>
      <td>11176</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>11176</td>
      <td>1261</td>
      <td>11176</td>
      <td>0.079302</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>11176</td>
      <td>370</td>
      <td>11176</td>
      <td>0.270270</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>8703</td>
      <td>11176</td>
      <td>8703</td>
      <td>0.008948</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>8703</td>
      <td>8703</td>
      <td>5776</td>
      <td>0.017313</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>8703</td>
      <td>8703</td>
      <td>5776</td>
      <td>0.017313</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>5776</td>
      <td>1</td>
      <td>5776</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>3315</td>
      <td>11176</td>
      <td>3315</td>
      <td>0.008948</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>3315</td>
      <td>3315</td>
      <td>5776</td>
      <td>0.017313</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>3315</td>
      <td>3315</td>
      <td>5776</td>
      <td>0.017313</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>3315</td>
      <td>3315</td>
      <td>5776</td>
      <td>0.017313</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>3315</td>
      <td>3315</td>
      <td>5776</td>
      <td>0.017313</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>1763</td>
      <td>5776</td>
      <td>5776</td>
      <td>0.005284</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_TAG</td>
      <td>[Git, Tag]</td>
      <td>1703</td>
      <td>1</td>
      <td>1703</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Git, Tag]</td>
      <td>ON_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>1703</td>
      <td>1703</td>
      <td>11176</td>
      <td>0.008948</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_AUTHOR</td>
      <td>[Author, Git, Person]</td>
      <td>1261</td>
      <td>1</td>
      <td>1261</td>
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

    total_number_of_nodes (vertices): 110710
    total_number_of_relationships (edges): 330628
    -> total directed graph density: 2.6975521621673052e-05
    -> total directed graph density in percent: 0.0026975521621673054

