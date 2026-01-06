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
      <td>55754</td>
      <td>27.464348</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Type, TS, NotIdentified]</td>
      <td>54204</td>
      <td>26.700820</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change, Create]</td>
      <td>16816</td>
      <td>8.283540</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Type, TS, Declared]</td>
      <td>11182</td>
      <td>5.508239</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Commit]</td>
      <td>10586</td>
      <td>5.214650</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Type, TS, Primitive]</td>
      <td>9016</td>
      <td>4.441270</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Change, Delete]</td>
      <td>8830</td>
      <td>4.349647</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[File, Git]</td>
      <td>6135</td>
      <td>3.022093</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Type, TS, Union]</td>
      <td>5549</td>
      <td>2.733430</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Type, TS, Literal]</td>
      <td>3382</td>
      <td>1.665969</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Change, Rename]</td>
      <td>2850</td>
      <td>1.403906</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>1902</td>
      <td>0.936923</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Json, Key]</td>
      <td>1894</td>
      <td>0.932982</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Json, Value, Scalar]</td>
      <td>1642</td>
      <td>0.808847</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Type, Object, TS]</td>
      <td>1527</td>
      <td>0.752198</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Author, Git, Person]</td>
      <td>1279</td>
      <td>0.630034</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Git, Tag]</td>
      <td>1180</td>
      <td>0.581266</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[TS, Parameter]</td>
      <td>1135</td>
      <td>0.559100</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[TS, ExternalDeclaration]</td>
      <td>1010</td>
      <td>0.497525</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[NPM, Dependency]</td>
      <td>865</td>
      <td>0.426098</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[TS, Property]</td>
      <td>593</td>
      <td>0.292111</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[TS, Function]</td>
      <td>550</td>
      <td>0.270929</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Type, TS, FunctionParameter]</td>
      <td>470</td>
      <td>0.231521</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Json, Value, Object]</td>
      <td>402</td>
      <td>0.198025</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, TS, Function]</td>
      <td>400</td>
      <td>0.197039</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Committer, Git, Person]</td>
      <td>361</td>
      <td>0.177828</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[TS, TypeAlias]</td>
      <td>332</td>
      <td>0.163543</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[TS, Variable]</td>
      <td>264</td>
      <td>0.130046</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Value, TS, Declared]</td>
      <td>242</td>
      <td>0.119209</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[TS, TypeParameter]</td>
      <td>227</td>
      <td>0.111820</td>
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
      <td>0.000493</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[TS, Setter]</td>
      <td>1</td>
      <td>0.000493</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Branch]</td>
      <td>1</td>
      <td>0.000493</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000493</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[File, TS, Local, Module, TestRelated, TestEnv...</td>
      <td>2</td>
      <td>0.000985</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[NPM, Overrides]</td>
      <td>2</td>
      <td>0.000985</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[NPM, Binary]</td>
      <td>3</td>
      <td>0.001478</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[TS, Enum]</td>
      <td>3</td>
      <td>0.001478</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[File, NPM, Export]</td>
      <td>5</td>
      <td>0.002463</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[NPM, BugTracker]</td>
      <td>9</td>
      <td>0.004433</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[TS, EnumMember]</td>
      <td>9</td>
      <td>0.004433</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Project, TS]</td>
      <td>11</td>
      <td>0.005419</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[TS, AccessorProperty]</td>
      <td>11</td>
      <td>0.005419</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[File, Local]</td>
      <td>11</td>
      <td>0.005419</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[TS, Constructor]</td>
      <td>11</td>
      <td>0.005419</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Repository, NPM]</td>
      <td>11</td>
      <td>0.005419</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[TS, Getter]</td>
      <td>11</td>
      <td>0.005419</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[TS, Class]</td>
      <td>12</td>
      <td>0.005911</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[File, TS, Scan]</td>
      <td>13</td>
      <td>0.006404</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Value, Object, TS]</td>
      <td>17</td>
      <td>0.008374</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[jQAssistant, Rule, Concept]</td>
      <td>19</td>
      <td>0.009359</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Value, TS, Null]</td>
      <td>23</td>
      <td>0.011330</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Value, Array, TS]</td>
      <td>29</td>
      <td>0.014285</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[NPM, Engine]</td>
      <td>31</td>
      <td>0.015271</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Json, Value, Array]</td>
      <td>37</td>
      <td>0.018226</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[File, Directory, Local]</td>
      <td>43</td>
      <td>0.021182</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, TS, Tuple]</td>
      <td>48</td>
      <td>0.023645</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Package, File, Json, NPM]</td>
      <td>60</td>
      <td>0.029556</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[File, Directory]</td>
      <td>72</td>
      <td>0.035467</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Git, Change, Copy]</td>
      <td>72</td>
      <td>0.035467</td>
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
      <td>103865</td>
      <td>51.163764</td>
    </tr>
    <tr>
      <th>1</th>
      <td>TS</td>
      <td>93815</td>
      <td>46.213147</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Type</td>
      <td>88020</td>
      <td>43.358538</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Change</td>
      <td>84322</td>
      <td>41.536908</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Update</td>
      <td>55754</td>
      <td>27.464348</td>
    </tr>
    <tr>
      <th>5</th>
      <td>NotIdentified</td>
      <td>54204</td>
      <td>26.700820</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Create</td>
      <td>16816</td>
      <td>8.283540</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Declared</td>
      <td>11424</td>
      <td>5.627448</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Commit</td>
      <td>10586</td>
      <td>5.214650</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Primitive</td>
      <td>9016</td>
      <td>4.441270</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Delete</td>
      <td>8830</td>
      <td>4.349647</td>
    </tr>
    <tr>
      <th>11</th>
      <td>File</td>
      <td>6496</td>
      <td>3.199921</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Union</td>
      <td>5549</td>
      <td>2.733430</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Json</td>
      <td>4035</td>
      <td>1.987636</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Literal</td>
      <td>3608</td>
      <td>1.777296</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Value</td>
      <td>3085</td>
      <td>1.519667</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Rename</td>
      <td>2850</td>
      <td>1.403906</td>
    </tr>
    <tr>
      <th>17</th>
      <td>ObjectMember</td>
      <td>1997</td>
      <td>0.983720</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Object</td>
      <td>1946</td>
      <td>0.958597</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Key</td>
      <td>1894</td>
      <td>0.932982</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Scalar</td>
      <td>1642</td>
      <td>0.808847</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Person</td>
      <td>1640</td>
      <td>0.807862</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Author</td>
      <td>1279</td>
      <td>0.630034</td>
    </tr>
    <tr>
      <th>23</th>
      <td>NPM</td>
      <td>1204</td>
      <td>0.593089</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Tag</td>
      <td>1180</td>
      <td>0.581266</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Parameter</td>
      <td>1135</td>
      <td>0.559100</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Function</td>
      <td>1039</td>
      <td>0.511810</td>
    </tr>
    <tr>
      <th>27</th>
      <td>ExternalDeclaration</td>
      <td>1010</td>
      <td>0.497525</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Dependency</td>
      <td>865</td>
      <td>0.426098</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Property</td>
      <td>593</td>
      <td>0.292111</td>
    </tr>
    <tr>
      <th>30</th>
      <td>FunctionParameter</td>
      <td>470</td>
      <td>0.231521</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Committer</td>
      <td>361</td>
      <td>0.177828</td>
    </tr>
    <tr>
      <th>32</th>
      <td>TypeAlias</td>
      <td>332</td>
      <td>0.163543</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Variable</td>
      <td>264</td>
      <td>0.130046</td>
    </tr>
    <tr>
      <th>34</th>
      <td>TypeParameter</td>
      <td>227</td>
      <td>0.111820</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Script</td>
      <td>218</td>
      <td>0.107387</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Local</td>
      <td>210</td>
      <td>0.103446</td>
    </tr>
    <tr>
      <th>37</th>
      <td>ExternalModule</td>
      <td>179</td>
      <td>0.088175</td>
    </tr>
    <tr>
      <th>38</th>
      <td>TypeParameterReference</td>
      <td>171</td>
      <td>0.084234</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Intersection</td>
      <td>169</td>
      <td>0.083249</td>
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

    Total number of relationships: 431601





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
      <td>84322</td>
      <td>19.537026</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>84322</td>
      <td>19.537026</td>
    </tr>
    <tr>
      <th>2</th>
      <td>CONTAINS</td>
      <td>74051</td>
      <td>17.157282</td>
    </tr>
    <tr>
      <th>3</th>
      <td>UPDATES</td>
      <td>55754</td>
      <td>12.917950</td>
    </tr>
    <tr>
      <th>4</th>
      <td>COMMITTED</td>
      <td>21172</td>
      <td>4.905457</td>
    </tr>
    <tr>
      <th>5</th>
      <td>CREATES</td>
      <td>19738</td>
      <td>4.573205</td>
    </tr>
    <tr>
      <th>6</th>
      <td>DELETES</td>
      <td>11680</td>
      <td>2.706203</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_PARENT</td>
      <td>11643</td>
      <td>2.697630</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_COMMIT</td>
      <td>10586</td>
      <td>2.452728</td>
    </tr>
    <tr>
      <th>9</th>
      <td>DEPENDS_ON</td>
      <td>9786</td>
      <td>2.267372</td>
    </tr>
    <tr>
      <th>10</th>
      <td>HAS_FILE</td>
      <td>6135</td>
      <td>1.421452</td>
    </tr>
    <tr>
      <th>11</th>
      <td>OF_TYPE</td>
      <td>5700</td>
      <td>1.320664</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>5481</td>
      <td>1.269923</td>
    </tr>
    <tr>
      <th>13</th>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>3408</td>
      <td>0.789618</td>
    </tr>
    <tr>
      <th>14</th>
      <td>REFERENCES</td>
      <td>3350</td>
      <td>0.776180</td>
    </tr>
    <tr>
      <th>15</th>
      <td>RENAMES</td>
      <td>2850</td>
      <td>0.660332</td>
    </tr>
    <tr>
      <th>16</th>
      <td>DECLARES</td>
      <td>2275</td>
      <td>0.527107</td>
    </tr>
    <tr>
      <th>17</th>
      <td>HAS_MEMBER</td>
      <td>1997</td>
      <td>0.462696</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_KEY</td>
      <td>1894</td>
      <td>0.438831</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_VALUE</td>
      <td>1894</td>
      <td>0.438831</td>
    </tr>
    <tr>
      <th>20</th>
      <td>EXPORTS</td>
      <td>1884</td>
      <td>0.436514</td>
    </tr>
    <tr>
      <th>21</th>
      <td>HAS_NEW_NAME</td>
      <td>1688</td>
      <td>0.391102</td>
    </tr>
    <tr>
      <th>22</th>
      <td>HAS_PARAMETER</td>
      <td>1493</td>
      <td>0.345921</td>
    </tr>
    <tr>
      <th>23</th>
      <td>HAS_AUTHOR</td>
      <td>1279</td>
      <td>0.296339</td>
    </tr>
    <tr>
      <th>24</th>
      <td>HAS_TAG</td>
      <td>1180</td>
      <td>0.273401</td>
    </tr>
    <tr>
      <th>25</th>
      <td>ON_COMMIT</td>
      <td>1180</td>
      <td>0.273401</td>
    </tr>
    <tr>
      <th>26</th>
      <td>RETURNS</td>
      <td>1082</td>
      <td>0.250695</td>
    </tr>
    <tr>
      <th>27</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>444</td>
      <td>0.102873</td>
    </tr>
    <tr>
      <th>28</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>394</td>
      <td>0.091288</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_COMMITTER</td>
      <td>361</td>
      <td>0.083642</td>
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
      <td>0.000232</td>
    </tr>
    <tr>
      <th>1</th>
      <td>DESCRIBED_BY_SETTER</td>
      <td>1</td>
      <td>0.000232</td>
    </tr>
    <tr>
      <th>2</th>
      <td>HAS_BRANCH</td>
      <td>1</td>
      <td>0.000232</td>
    </tr>
    <tr>
      <th>3</th>
      <td>HAS_HEAD</td>
      <td>2</td>
      <td>0.000463</td>
    </tr>
    <tr>
      <th>4</th>
      <td>HAS_OVERRIDES</td>
      <td>2</td>
      <td>0.000463</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_BINARY</td>
      <td>3</td>
      <td>0.000695</td>
    </tr>
    <tr>
      <th>6</th>
      <td>REQUIRES</td>
      <td>5</td>
      <td>0.001158</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_BUG_TRACKER</td>
      <td>9</td>
      <td>0.002085</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_NPM_PACKAGE</td>
      <td>11</td>
      <td>0.002549</td>
    </tr>
    <tr>
      <th>9</th>
      <td>IN_REPOSITORY</td>
      <td>11</td>
      <td>0.002549</td>
    </tr>
    <tr>
      <th>10</th>
      <td>DESCRIBED_BY_GETTER</td>
      <td>11</td>
      <td>0.002549</td>
    </tr>
    <tr>
      <th>11</th>
      <td>CONTAINS_PROJECT</td>
      <td>11</td>
      <td>0.002549</td>
    </tr>
    <tr>
      <th>12</th>
      <td>HAS_ROOT</td>
      <td>11</td>
      <td>0.002549</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_CONFIG</td>
      <td>11</td>
      <td>0.002549</td>
    </tr>
    <tr>
      <th>14</th>
      <td>HAS_EXPORT</td>
      <td>15</td>
      <td>0.003475</td>
    </tr>
    <tr>
      <th>15</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.004402</td>
    </tr>
    <tr>
      <th>16</th>
      <td>DECLARES_PEER_DEPENDENCY</td>
      <td>27</td>
      <td>0.006256</td>
    </tr>
    <tr>
      <th>17</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.006487</td>
    </tr>
    <tr>
      <th>18</th>
      <td>DECLARES_ENGINE</td>
      <td>31</td>
      <td>0.007183</td>
    </tr>
    <tr>
      <th>19</th>
      <td>EXTENDS</td>
      <td>38</td>
      <td>0.008804</td>
    </tr>
    <tr>
      <th>20</th>
      <td>COPY_OF</td>
      <td>42</td>
      <td>0.009731</td>
    </tr>
    <tr>
      <th>21</th>
      <td>COPIES</td>
      <td>72</td>
      <td>0.016682</td>
    </tr>
    <tr>
      <th>22</th>
      <td>PARENT</td>
      <td>95</td>
      <td>0.022011</td>
    </tr>
    <tr>
      <th>23</th>
      <td>MEMBER</td>
      <td>95</td>
      <td>0.022011</td>
    </tr>
    <tr>
      <th>24</th>
      <td>CALLS</td>
      <td>100</td>
      <td>0.023170</td>
    </tr>
    <tr>
      <th>25</th>
      <td>HAS_ARGUMENT</td>
      <td>104</td>
      <td>0.024096</td>
    </tr>
    <tr>
      <th>26</th>
      <td>PROVIDED_BY_NPM_DEPENDENCY</td>
      <td>107</td>
      <td>0.024791</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS</td>
      <td>112</td>
      <td>0.025950</td>
    </tr>
    <tr>
      <th>28</th>
      <td>CONTAINS_VALUE</td>
      <td>127</td>
      <td>0.029425</td>
    </tr>
    <tr>
      <th>29</th>
      <td>IS_DESCRIBED_IN_NPM_PACKAGE</td>
      <td>144</td>
      <td>0.033364</td>
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
      <td>55754</td>
      <td>10586</td>
      <td>55754</td>
      <td>0.009446</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Change, Update]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>55754</td>
      <td>55754</td>
      <td>6135</td>
      <td>0.016300</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change, Update]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>55754</td>
      <td>55754</td>
      <td>6135</td>
      <td>0.016300</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, NotIdentified]</td>
      <td>53911</td>
      <td>5549</td>
      <td>54204</td>
      <td>0.017924</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Create]</td>
      <td>16816</td>
      <td>10586</td>
      <td>16816</td>
      <td>0.009446</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change, Create]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>16816</td>
      <td>16816</td>
      <td>6135</td>
      <td>0.016300</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Git, Change, Create]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>16816</td>
      <td>16816</td>
      <td>6135</td>
      <td>0.016300</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>11643</td>
      <td>10586</td>
      <td>10586</td>
      <td>0.010390</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>10586</td>
      <td>1</td>
      <td>10586</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>10586</td>
      <td>1279</td>
      <td>10586</td>
      <td>0.078186</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>10586</td>
      <td>361</td>
      <td>10586</td>
      <td>0.277008</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Delete]</td>
      <td>8830</td>
      <td>10586</td>
      <td>8830</td>
      <td>0.009446</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Git, Change, Delete]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>8830</td>
      <td>8830</td>
      <td>6135</td>
      <td>0.016300</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Git, Change, Delete]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>8830</td>
      <td>8830</td>
      <td>6135</td>
      <td>0.016300</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Declared]</td>
      <td>8209</td>
      <td>5549</td>
      <td>11182</td>
      <td>0.013230</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Primitive]</td>
      <td>6360</td>
      <td>5549</td>
      <td>9016</td>
      <td>0.012712</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>6135</td>
      <td>1</td>
      <td>6135</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Type, TS, Declared]</td>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>[Type, TS, Union]</td>
      <td>4157</td>
      <td>11182</td>
      <td>5549</td>
      <td>0.006700</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Literal]</td>
      <td>3119</td>
      <td>5549</td>
      <td>3382</td>
      <td>0.016620</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[File, Git]</td>
      <td>CHANGED_TOGETHER_WITH</td>
      <td>[File, Git]</td>
      <td>2959</td>
      <td>6135</td>
      <td>6135</td>
      <td>0.007862</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change, Rename]</td>
      <td>2850</td>
      <td>10586</td>
      <td>2850</td>
      <td>0.009446</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Git, Change, Rename]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>2850</td>
      <td>2850</td>
      <td>6135</td>
      <td>0.016300</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Git, Change, Rename]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>2850</td>
      <td>2850</td>
      <td>6135</td>
      <td>0.016300</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Git, Change, Rename]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>2850</td>
      <td>2850</td>
      <td>6135</td>
      <td>0.016300</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Git, Change, Rename]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>2850</td>
      <td>2850</td>
      <td>6135</td>
      <td>0.016300</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, Object, TS]</td>
      <td>HAS_MEMBER</td>
      <td>[Type, TS, ObjectMember]</td>
      <td>1902</td>
      <td>1527</td>
      <td>1902</td>
      <td>0.065488</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Json, Value, Object]</td>
      <td>HAS_KEY</td>
      <td>[Json, Key]</td>
      <td>1894</td>
      <td>402</td>
      <td>1894</td>
      <td>0.248756</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>1688</td>
      <td>6135</td>
      <td>6135</td>
      <td>0.004485</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Json, Key]</td>
      <td>HAS_VALUE</td>
      <td>[Json, Value, Scalar]</td>
      <td>1515</td>
      <td>1894</td>
      <td>1642</td>
      <td>0.048715</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Type, TS, Declared]</td>
      <td>REFERENCES</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>1495</td>
      <td>11182</td>
      <td>1010</td>
      <td>0.013237</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 203005
    total_number_of_relationships (edges): 431601
    -> total directed graph density: 1.0473000209157171e-05
    -> total directed graph density in percent: 0.001047300020915717

