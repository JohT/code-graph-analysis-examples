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
      <td>57173</td>
      <td>27.839564</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Type, TS, NotIdentified]</td>
      <td>54186</td>
      <td>26.385088</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change, Create]</td>
      <td>17009</td>
      <td>8.282286</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Commit]</td>
      <td>10711</td>
      <td>5.215566</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Type, TS, Declared]</td>
      <td>10639</td>
      <td>5.180507</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Type, TS, Primitive]</td>
      <td>9616</td>
      <td>4.682372</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Change, Delete]</td>
      <td>8942</td>
      <td>4.354177</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[File, Git]</td>
      <td>6207</td>
      <td>3.022409</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Type, TS, Union]</td>
      <td>5440</td>
      <td>2.648929</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Type, TS, Literal]</td>
      <td>3421</td>
      <td>1.665806</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Change, Rename]</td>
      <td>2850</td>
      <td>1.387766</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Json, Key]</td>
      <td>1927</td>
      <td>0.938325</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>1705</td>
      <td>0.830225</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Json, Value, Scalar]</td>
      <td>1669</td>
      <td>0.812695</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Type, Object, TS]</td>
      <td>1507</td>
      <td>0.733812</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Author, Git, Person]</td>
      <td>1295</td>
      <td>0.630581</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Git, Tag]</td>
      <td>1224</td>
      <td>0.596009</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[TS, Parameter]</td>
      <td>1182</td>
      <td>0.575558</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[TS, ExternalDeclaration]</td>
      <td>1012</td>
      <td>0.492779</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[NPM, Dependency]</td>
      <td>880</td>
      <td>0.428503</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Type, TS, FunctionParameter]</td>
      <td>719</td>
      <td>0.350107</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Type, TS, Function]</td>
      <td>645</td>
      <td>0.314073</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[TS, Property]</td>
      <td>582</td>
      <td>0.283396</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[TS, Function]</td>
      <td>574</td>
      <td>0.279501</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Json, Value, Object]</td>
      <td>410</td>
      <td>0.199644</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Committer, Git, Person]</td>
      <td>361</td>
      <td>0.175784</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[TS, TypeAlias]</td>
      <td>332</td>
      <td>0.161663</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[TS, Variable]</td>
      <td>268</td>
      <td>0.130499</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Value, TS, Declared]</td>
      <td>244</td>
      <td>0.118812</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Value, TS, Literal]</td>
      <td>237</td>
      <td>0.115404</td>
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
      <td>0.000487</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[TS, Setter]</td>
      <td>1</td>
      <td>0.000487</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Branch]</td>
      <td>1</td>
      <td>0.000487</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000487</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, TS, Local, Module, TestRelated, TestEnv...</td>
      <td>2</td>
      <td>0.000974</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[NPM, Overrides]</td>
      <td>2</td>
      <td>0.000974</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[TS, Enum]</td>
      <td>3</td>
      <td>0.001461</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[NPM, Binary]</td>
      <td>3</td>
      <td>0.001461</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[File, NPM, Export]</td>
      <td>5</td>
      <td>0.002435</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[TS, EnumMember]</td>
      <td>9</td>
      <td>0.004382</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[NPM, BugTracker]</td>
      <td>9</td>
      <td>0.004382</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[TS, Getter]</td>
      <td>11</td>
      <td>0.005356</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[TS, AccessorProperty]</td>
      <td>11</td>
      <td>0.005356</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[TS, Constructor]</td>
      <td>11</td>
      <td>0.005356</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[File, Local]</td>
      <td>11</td>
      <td>0.005356</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Project, TS]</td>
      <td>11</td>
      <td>0.005356</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Repository, NPM]</td>
      <td>11</td>
      <td>0.005356</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[TS, Class]</td>
      <td>12</td>
      <td>0.005843</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[File, TS, Scan]</td>
      <td>13</td>
      <td>0.006330</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Value, Object, TS]</td>
      <td>18</td>
      <td>0.008765</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[jQAssistant, Rule, Concept]</td>
      <td>19</td>
      <td>0.009252</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Value, TS, Null]</td>
      <td>23</td>
      <td>0.011200</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Value, Array, TS]</td>
      <td>30</td>
      <td>0.014608</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[NPM, Engine]</td>
      <td>31</td>
      <td>0.015095</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Json, Value, Array]</td>
      <td>37</td>
      <td>0.018017</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[File, Directory, Local]</td>
      <td>43</td>
      <td>0.020938</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, TS, Tuple]</td>
      <td>48</td>
      <td>0.023373</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Package, File, Json, NPM]</td>
      <td>62</td>
      <td>0.030190</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Git, Change, Copy]</td>
      <td>72</td>
      <td>0.035059</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[File, Directory]</td>
      <td>74</td>
      <td>0.036033</td>
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
      <td>105846</td>
      <td>51.540177</td>
    </tr>
    <tr>
      <th>1</th>
      <td>TS</td>
      <td>94102</td>
      <td>45.821606</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Type</td>
      <td>88226</td>
      <td>42.960373</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Change</td>
      <td>86046</td>
      <td>41.898854</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Update</td>
      <td>57173</td>
      <td>27.839564</td>
    </tr>
    <tr>
      <th>5</th>
      <td>NotIdentified</td>
      <td>54186</td>
      <td>26.385088</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Create</td>
      <td>17009</td>
      <td>8.282286</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Declared</td>
      <td>10883</td>
      <td>5.299319</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Commit</td>
      <td>10711</td>
      <td>5.215566</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Primitive</td>
      <td>9616</td>
      <td>4.682372</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Delete</td>
      <td>8942</td>
      <td>4.354177</td>
    </tr>
    <tr>
      <th>11</th>
      <td>File</td>
      <td>6575</td>
      <td>3.201601</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Union</td>
      <td>5440</td>
      <td>2.648929</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Json</td>
      <td>4105</td>
      <td>1.998870</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Literal</td>
      <td>3658</td>
      <td>1.781210</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Value</td>
      <td>3135</td>
      <td>1.526543</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Rename</td>
      <td>2850</td>
      <td>1.387766</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Object</td>
      <td>1935</td>
      <td>0.942220</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Key</td>
      <td>1927</td>
      <td>0.938325</td>
    </tr>
    <tr>
      <th>19</th>
      <td>ObjectMember</td>
      <td>1800</td>
      <td>0.876484</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Scalar</td>
      <td>1669</td>
      <td>0.812695</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Person</td>
      <td>1656</td>
      <td>0.806365</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Function</td>
      <td>1308</td>
      <td>0.636912</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Author</td>
      <td>1295</td>
      <td>0.630581</td>
    </tr>
    <tr>
      <th>24</th>
      <td>NPM</td>
      <td>1227</td>
      <td>0.597470</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Tag</td>
      <td>1224</td>
      <td>0.596009</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Parameter</td>
      <td>1182</td>
      <td>0.575558</td>
    </tr>
    <tr>
      <th>27</th>
      <td>ExternalDeclaration</td>
      <td>1012</td>
      <td>0.492779</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Dependency</td>
      <td>880</td>
      <td>0.428503</td>
    </tr>
    <tr>
      <th>29</th>
      <td>FunctionParameter</td>
      <td>719</td>
      <td>0.350107</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Property</td>
      <td>582</td>
      <td>0.283396</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Committer</td>
      <td>361</td>
      <td>0.175784</td>
    </tr>
    <tr>
      <th>32</th>
      <td>TypeAlias</td>
      <td>332</td>
      <td>0.161663</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Variable</td>
      <td>268</td>
      <td>0.130499</td>
    </tr>
    <tr>
      <th>34</th>
      <td>TypeParameter</td>
      <td>225</td>
      <td>0.109560</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Script</td>
      <td>224</td>
      <td>0.109074</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Local</td>
      <td>213</td>
      <td>0.103717</td>
    </tr>
    <tr>
      <th>37</th>
      <td>ExternalModule</td>
      <td>179</td>
      <td>0.087161</td>
    </tr>
    <tr>
      <th>38</th>
      <td>TypeParameterReference</td>
      <td>169</td>
      <td>0.082292</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Module</td>
      <td>159</td>
      <td>0.077423</td>
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

    Total number of relationships: 438080





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
      <td>86046</td>
      <td>19.641618</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>86046</td>
      <td>19.641618</td>
    </tr>
    <tr>
      <th>2</th>
      <td>CONTAINS</td>
      <td>73828</td>
      <td>16.852630</td>
    </tr>
    <tr>
      <th>3</th>
      <td>UPDATES</td>
      <td>57173</td>
      <td>13.050813</td>
    </tr>
    <tr>
      <th>4</th>
      <td>COMMITTED</td>
      <td>21422</td>
      <td>4.889974</td>
    </tr>
    <tr>
      <th>5</th>
      <td>CREATES</td>
      <td>19931</td>
      <td>4.549626</td>
    </tr>
    <tr>
      <th>6</th>
      <td>DELETES</td>
      <td>11792</td>
      <td>2.691746</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_PARENT</td>
      <td>11780</td>
      <td>2.689007</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_COMMIT</td>
      <td>10711</td>
      <td>2.444987</td>
    </tr>
    <tr>
      <th>9</th>
      <td>DEPENDS_ON</td>
      <td>10002</td>
      <td>2.283145</td>
    </tr>
    <tr>
      <th>10</th>
      <td>HAS_FILE</td>
      <td>6207</td>
      <td>1.416864</td>
    </tr>
    <tr>
      <th>11</th>
      <td>OF_TYPE</td>
      <td>5807</td>
      <td>1.325557</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>5512</td>
      <td>1.258218</td>
    </tr>
    <tr>
      <th>13</th>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>3781</td>
      <td>0.863084</td>
    </tr>
    <tr>
      <th>14</th>
      <td>REFERENCES</td>
      <td>2974</td>
      <td>0.678871</td>
    </tr>
    <tr>
      <th>15</th>
      <td>RENAMES</td>
      <td>2850</td>
      <td>0.650566</td>
    </tr>
    <tr>
      <th>16</th>
      <td>DECLARES</td>
      <td>2289</td>
      <td>0.522507</td>
    </tr>
    <tr>
      <th>17</th>
      <td>HAS_KEY</td>
      <td>1927</td>
      <td>0.439874</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_VALUE</td>
      <td>1927</td>
      <td>0.439874</td>
    </tr>
    <tr>
      <th>19</th>
      <td>EXPORTS</td>
      <td>1895</td>
      <td>0.432569</td>
    </tr>
    <tr>
      <th>20</th>
      <td>HAS_MEMBER</td>
      <td>1800</td>
      <td>0.410884</td>
    </tr>
    <tr>
      <th>21</th>
      <td>HAS_PARAMETER</td>
      <td>1789</td>
      <td>0.408373</td>
    </tr>
    <tr>
      <th>22</th>
      <td>HAS_NEW_NAME</td>
      <td>1688</td>
      <td>0.385318</td>
    </tr>
    <tr>
      <th>23</th>
      <td>RETURNS</td>
      <td>1351</td>
      <td>0.308391</td>
    </tr>
    <tr>
      <th>24</th>
      <td>HAS_AUTHOR</td>
      <td>1295</td>
      <td>0.295608</td>
    </tr>
    <tr>
      <th>25</th>
      <td>HAS_TAG</td>
      <td>1224</td>
      <td>0.279401</td>
    </tr>
    <tr>
      <th>26</th>
      <td>ON_COMMIT</td>
      <td>1224</td>
      <td>0.279401</td>
    </tr>
    <tr>
      <th>27</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>454</td>
      <td>0.103634</td>
    </tr>
    <tr>
      <th>28</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>399</td>
      <td>0.091079</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_COMMITTER</td>
      <td>361</td>
      <td>0.082405</td>
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
      <td>0.000228</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HAS_BRANCH</td>
      <td>1</td>
      <td>0.000228</td>
    </tr>
    <tr>
      <th>2</th>
      <td>DESCRIBED_BY_SETTER</td>
      <td>1</td>
      <td>0.000228</td>
    </tr>
    <tr>
      <th>3</th>
      <td>HAS_OVERRIDES</td>
      <td>2</td>
      <td>0.000457</td>
    </tr>
    <tr>
      <th>4</th>
      <td>HAS_HEAD</td>
      <td>2</td>
      <td>0.000457</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_BINARY</td>
      <td>3</td>
      <td>0.000685</td>
    </tr>
    <tr>
      <th>6</th>
      <td>REQUIRES</td>
      <td>5</td>
      <td>0.001141</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_BUG_TRACKER</td>
      <td>9</td>
      <td>0.002054</td>
    </tr>
    <tr>
      <th>8</th>
      <td>IN_REPOSITORY</td>
      <td>11</td>
      <td>0.002511</td>
    </tr>
    <tr>
      <th>9</th>
      <td>HAS_ROOT</td>
      <td>11</td>
      <td>0.002511</td>
    </tr>
    <tr>
      <th>10</th>
      <td>HAS_NPM_PACKAGE</td>
      <td>11</td>
      <td>0.002511</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_CONFIG</td>
      <td>11</td>
      <td>0.002511</td>
    </tr>
    <tr>
      <th>12</th>
      <td>DESCRIBED_BY_GETTER</td>
      <td>11</td>
      <td>0.002511</td>
    </tr>
    <tr>
      <th>13</th>
      <td>CONTAINS_PROJECT</td>
      <td>11</td>
      <td>0.002511</td>
    </tr>
    <tr>
      <th>14</th>
      <td>HAS_EXPORT</td>
      <td>15</td>
      <td>0.003424</td>
    </tr>
    <tr>
      <th>15</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.004337</td>
    </tr>
    <tr>
      <th>16</th>
      <td>DECLARES_PEER_DEPENDENCY</td>
      <td>27</td>
      <td>0.006163</td>
    </tr>
    <tr>
      <th>17</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.006392</td>
    </tr>
    <tr>
      <th>18</th>
      <td>DECLARES_ENGINE</td>
      <td>31</td>
      <td>0.007076</td>
    </tr>
    <tr>
      <th>19</th>
      <td>EXTENDS</td>
      <td>36</td>
      <td>0.008218</td>
    </tr>
    <tr>
      <th>20</th>
      <td>COPY_OF</td>
      <td>42</td>
      <td>0.009587</td>
    </tr>
    <tr>
      <th>21</th>
      <td>COPIES</td>
      <td>72</td>
      <td>0.016435</td>
    </tr>
    <tr>
      <th>22</th>
      <td>PARENT</td>
      <td>96</td>
      <td>0.021914</td>
    </tr>
    <tr>
      <th>23</th>
      <td>MEMBER</td>
      <td>96</td>
      <td>0.021914</td>
    </tr>
    <tr>
      <th>24</th>
      <td>CALLS</td>
      <td>100</td>
      <td>0.022827</td>
    </tr>
    <tr>
      <th>25</th>
      <td>HAS_ARGUMENT</td>
      <td>104</td>
      <td>0.023740</td>
    </tr>
    <tr>
      <th>26</th>
      <td>PROVIDED_BY_NPM_DEPENDENCY</td>
      <td>107</td>
      <td>0.024425</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS</td>
      <td>112</td>
      <td>0.025566</td>
    </tr>
    <tr>
      <th>28</th>
      <td>CONTAINS_VALUE</td>
      <td>127</td>
      <td>0.028990</td>
    </tr>
    <tr>
      <th>29</th>
      <td>IS_DESCRIBED_IN_NPM_PACKAGE</td>
      <td>146</td>
      <td>0.033327</td>
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
      <td>57173</td>
      <td>10711</td>
      <td>57173</td>
      <td>0.009336</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change, Update]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>57173</td>
      <td>57173</td>
      <td>6207</td>
      <td>0.016111</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change, Update]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>57173</td>
      <td>57173</td>
      <td>6207</td>
      <td>0.016111</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, NotIdentified]</td>
      <td>53911</td>
      <td>5440</td>
      <td>54186</td>
      <td>0.018289</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>17009</td>
      <td>10711</td>
      <td>17009</td>
      <td>0.009336</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>17009</td>
      <td>17009</td>
      <td>6207</td>
      <td>0.016111</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>17009</td>
      <td>17009</td>
      <td>6207</td>
      <td>0.016111</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>11780</td>
      <td>10711</td>
      <td>10711</td>
      <td>0.010268</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>10711</td>
      <td>1</td>
      <td>10711</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>10711</td>
      <td>1295</td>
      <td>10711</td>
      <td>0.077220</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>10711</td>
      <td>361</td>
      <td>10711</td>
      <td>0.277008</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>8942</td>
      <td>10711</td>
      <td>8942</td>
      <td>0.009336</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>8942</td>
      <td>8942</td>
      <td>6207</td>
      <td>0.016111</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>8942</td>
      <td>8942</td>
      <td>6207</td>
      <td>0.016111</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Declared]</td>
      <td>7874</td>
      <td>5440</td>
      <td>10639</td>
      <td>0.013605</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Primitive]</td>
      <td>6498</td>
      <td>5440</td>
      <td>9616</td>
      <td>0.012422</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>6207</td>
      <td>1</td>
      <td>6207</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Type, TS, Declared]</td>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>[Type, TS, Union]</td>
      <td>4161</td>
      <td>10639</td>
      <td>5440</td>
      <td>0.007189</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[File, Git]</td>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>[File, Git]</td>
      <td>3292</td>
      <td>6207</td>
      <td>6207</td>
      <td>0.008545</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Literal]</td>
      <td>3158</td>
      <td>5440</td>
      <td>3421</td>
      <td>0.016969</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>2850</td>
      <td>10711</td>
      <td>2850</td>
      <td>0.009336</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>2850</td>
      <td>2850</td>
      <td>6207</td>
      <td>0.016111</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>2850</td>
      <td>2850</td>
      <td>6207</td>
      <td>0.016111</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>2850</td>
      <td>2850</td>
      <td>6207</td>
      <td>0.016111</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>2850</td>
      <td>2850</td>
      <td>6207</td>
      <td>0.016111</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Json, Value, Object]</td>
      <td>HAS_KEY</td>
      <td>[Json, Key]</td>
      <td>1927</td>
      <td>410</td>
      <td>1927</td>
      <td>0.243902</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, Object, TS]</td>
      <td>HAS_MEMBER</td>
      <td>[Type, TS, ObjectMember]</td>
      <td>1705</td>
      <td>1507</td>
      <td>1705</td>
      <td>0.066357</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>1688</td>
      <td>6207</td>
      <td>6207</td>
      <td>0.004381</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Json, Key]</td>
      <td>HAS_VALUE</td>
      <td>[Json, Value, Scalar]</td>
      <td>1542</td>
      <td>1927</td>
      <td>1669</td>
      <td>0.047945</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_AUTHOR</td>
      <td>[Author, Git, Person]</td>
      <td>1295</td>
      <td>1</td>
      <td>1295</td>
      <td>100.000000</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 205366
    total_number_of_relationships (edges): 438080
    -> total directed graph density: 1.0387199016430132e-05
    -> total directed graph density in percent: 0.001038719901643013

