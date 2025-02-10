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
      <td>[Git, Change]</td>
      <td>83882</td>
      <td>78.271499</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Commit]</td>
      <td>10932</td>
      <td>10.200806</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[File, Git]</td>
      <td>5619</td>
      <td>5.243170</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Tag]</td>
      <td>1536</td>
      <td>1.433264</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Author, Git, Person]</td>
      <td>1244</td>
      <td>1.160794</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Json, Key]</td>
      <td>668</td>
      <td>0.623320</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Json, Value, Scalar]</td>
      <td>603</td>
      <td>0.562668</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Committer, Git, Person]</td>
      <td>370</td>
      <td>0.345252</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[NPM, Dependency]</td>
      <td>338</td>
      <td>0.315393</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Type, TS, Primitive]</td>
      <td>291</td>
      <td>0.271536</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Type, TS, Declared]</td>
      <td>276</td>
      <td>0.257540</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[TS, ExternalDeclaration]</td>
      <td>215</td>
      <td>0.200620</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Type, TS, Literal]</td>
      <td>136</td>
      <td>0.126904</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Json, Value, Object]</td>
      <td>133</td>
      <td>0.124104</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Type, TS, Union]</td>
      <td>119</td>
      <td>0.111041</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>101</td>
      <td>0.094245</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[NPM, Script]</td>
      <td>91</td>
      <td>0.084913</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[TS, Property]</td>
      <td>65</td>
      <td>0.060652</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[TS, Function]</td>
      <td>47</td>
      <td>0.043856</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Type, TS, FunctionParameter]</td>
      <td>40</td>
      <td>0.037325</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Type, Object, TS]</td>
      <td>39</td>
      <td>0.036391</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Git, Branch]</td>
      <td>39</td>
      <td>0.036391</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[File, Directory]</td>
      <td>34</td>
      <td>0.031726</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, TS, Function]</td>
      <td>34</td>
      <td>0.031726</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[TS, Parameter]</td>
      <td>33</td>
      <td>0.030793</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Package, File, Json, NPM]</td>
      <td>29</td>
      <td>0.027060</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[TS, Variable]</td>
      <td>24</td>
      <td>0.022395</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Value, TS, Literal]</td>
      <td>20</td>
      <td>0.018662</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[jQAssistant, Rule, Concept]</td>
      <td>19</td>
      <td>0.017729</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Type, TS, Intersection]</td>
      <td>17</td>
      <td>0.015863</td>
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
      <td>0.000933</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[File, TS, Scan]</td>
      <td>1</td>
      <td>0.000933</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[TS, Method]</td>
      <td>1</td>
      <td>0.000933</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.000933</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[TS, Constructor]</td>
      <td>1</td>
      <td>0.000933</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Value, TS, ObjectMember]</td>
      <td>1</td>
      <td>0.000933</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[TS, Class]</td>
      <td>1</td>
      <td>0.000933</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[TS, Enum]</td>
      <td>2</td>
      <td>0.001866</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Value, Object, TS]</td>
      <td>3</td>
      <td>0.002799</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Type, TS, Tuple]</td>
      <td>3</td>
      <td>0.002799</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Value, TS, Function]</td>
      <td>4</td>
      <td>0.003732</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[TS, TypeParameter]</td>
      <td>4</td>
      <td>0.003732</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Value, TS, Complex]</td>
      <td>5</td>
      <td>0.004666</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[NPM, Engine]</td>
      <td>6</td>
      <td>0.005599</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Project, TS]</td>
      <td>6</td>
      <td>0.005599</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[File, Local]</td>
      <td>6</td>
      <td>0.005599</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Value, TS, Call]</td>
      <td>6</td>
      <td>0.005599</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Value, TS, Member]</td>
      <td>6</td>
      <td>0.005599</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[File, TS, Local, Module]</td>
      <td>6</td>
      <td>0.005599</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Type, TS, TypeParameterReference]</td>
      <td>6</td>
      <td>0.005599</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[TS, EnumMember]</td>
      <td>8</td>
      <td>0.007465</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Type, TS, NotIdentified]</td>
      <td>11</td>
      <td>0.010264</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[TS, ExternalModule]</td>
      <td>11</td>
      <td>0.010264</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Json, Value, Array]</td>
      <td>12</td>
      <td>0.011197</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Value, TS, Declared]</td>
      <td>13</td>
      <td>0.012130</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[TS, TypeAlias]</td>
      <td>16</td>
      <td>0.014930</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[File, Directory, Local]</td>
      <td>16</td>
      <td>0.014930</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Type, TS, Intersection]</td>
      <td>17</td>
      <td>0.015863</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[TS, Interface]</td>
      <td>17</td>
      <td>0.015863</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[jQAssistant, Rule, Concept]</td>
      <td>19</td>
      <td>0.017729</td>
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
      <td>103623</td>
      <td>96.692110</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Change</td>
      <td>83882</td>
      <td>78.271499</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Commit</td>
      <td>10932</td>
      <td>10.200806</td>
    </tr>
    <tr>
      <th>3</th>
      <td>File</td>
      <td>5712</td>
      <td>5.329949</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Person</td>
      <td>1614</td>
      <td>1.506047</td>
    </tr>
    <tr>
      <th>5</th>
      <td>TS</td>
      <td>1589</td>
      <td>1.482719</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Tag</td>
      <td>1536</td>
      <td>1.433264</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Json</td>
      <td>1445</td>
      <td>1.348350</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Author</td>
      <td>1244</td>
      <td>1.160794</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Type</td>
      <td>1073</td>
      <td>1.001232</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Value</td>
      <td>806</td>
      <td>0.752090</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Key</td>
      <td>668</td>
      <td>0.623320</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Scalar</td>
      <td>603</td>
      <td>0.562668</td>
    </tr>
    <tr>
      <th>13</th>
      <td>NPM</td>
      <td>464</td>
      <td>0.432965</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Committer</td>
      <td>370</td>
      <td>0.345252</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Dependency</td>
      <td>338</td>
      <td>0.315393</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Primitive</td>
      <td>291</td>
      <td>0.271536</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Declared</td>
      <td>289</td>
      <td>0.269670</td>
    </tr>
    <tr>
      <th>18</th>
      <td>ExternalDeclaration</td>
      <td>215</td>
      <td>0.200620</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Object</td>
      <td>175</td>
      <td>0.163295</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Literal</td>
      <td>156</td>
      <td>0.145566</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Union</td>
      <td>119</td>
      <td>0.111041</td>
    </tr>
    <tr>
      <th>22</th>
      <td>ObjectMember</td>
      <td>102</td>
      <td>0.095178</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Script</td>
      <td>91</td>
      <td>0.084913</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Function</td>
      <td>85</td>
      <td>0.079315</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Property</td>
      <td>65</td>
      <td>0.060652</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Directory</td>
      <td>50</td>
      <td>0.046656</td>
    </tr>
    <tr>
      <th>27</th>
      <td>FunctionParameter</td>
      <td>40</td>
      <td>0.037325</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Branch</td>
      <td>39</td>
      <td>0.036391</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Parameter</td>
      <td>33</td>
      <td>0.030793</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Package</td>
      <td>29</td>
      <td>0.027060</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Local</td>
      <td>28</td>
      <td>0.026127</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Variable</td>
      <td>24</td>
      <td>0.022395</td>
    </tr>
    <tr>
      <th>33</th>
      <td>jQAssistant</td>
      <td>20</td>
      <td>0.018662</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Concept</td>
      <td>19</td>
      <td>0.017729</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Rule</td>
      <td>19</td>
      <td>0.017729</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Interface</td>
      <td>17</td>
      <td>0.015863</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Intersection</td>
      <td>17</td>
      <td>0.015863</td>
    </tr>
    <tr>
      <th>38</th>
      <td>TypeAlias</td>
      <td>16</td>
      <td>0.014930</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Array</td>
      <td>12</td>
      <td>0.011197</td>
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

    Total number of relationships: 320138





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
      <td>83882</td>
      <td>26.201825</td>
    </tr>
    <tr>
      <th>1</th>
      <td>MODIFIES</td>
      <td>83882</td>
      <td>26.201825</td>
    </tr>
    <tr>
      <th>2</th>
      <td>UPDATES</td>
      <td>55685</td>
      <td>17.394061</td>
    </tr>
    <tr>
      <th>3</th>
      <td>COMMITTED</td>
      <td>21864</td>
      <td>6.829555</td>
    </tr>
    <tr>
      <th>4</th>
      <td>CREATES</td>
      <td>19620</td>
      <td>6.128607</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_PARENT</td>
      <td>11995</td>
      <td>3.746822</td>
    </tr>
    <tr>
      <th>6</th>
      <td>DELETES</td>
      <td>11844</td>
      <td>3.699655</td>
    </tr>
    <tr>
      <th>7</th>
      <td>HAS_COMMIT</td>
      <td>10932</td>
      <td>3.414777</td>
    </tr>
    <tr>
      <th>8</th>
      <td>HAS_FILE</td>
      <td>5619</td>
      <td>1.755181</td>
    </tr>
    <tr>
      <th>9</th>
      <td>RENAMES</td>
      <td>3267</td>
      <td>1.020497</td>
    </tr>
    <tr>
      <th>10</th>
      <td>HAS_NEW_NAME</td>
      <td>1751</td>
      <td>0.546952</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_TAG</td>
      <td>1536</td>
      <td>0.479793</td>
    </tr>
    <tr>
      <th>12</th>
      <td>ON_COMMIT</td>
      <td>1536</td>
      <td>0.479793</td>
    </tr>
    <tr>
      <th>13</th>
      <td>HAS_AUTHOR</td>
      <td>1244</td>
      <td>0.388582</td>
    </tr>
    <tr>
      <th>14</th>
      <td>DEPENDS_ON</td>
      <td>887</td>
      <td>0.277068</td>
    </tr>
    <tr>
      <th>15</th>
      <td>HAS_KEY</td>
      <td>668</td>
      <td>0.208660</td>
    </tr>
    <tr>
      <th>16</th>
      <td>HAS_VALUE</td>
      <td>668</td>
      <td>0.208660</td>
    </tr>
    <tr>
      <th>17</th>
      <td>CONTAINS</td>
      <td>594</td>
      <td>0.185545</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_COMMITTER</td>
      <td>370</td>
      <td>0.115575</td>
    </tr>
    <tr>
      <th>19</th>
      <td>OF_TYPE</td>
      <td>337</td>
      <td>0.105267</td>
    </tr>
    <tr>
      <th>20</th>
      <td>EXPORTS</td>
      <td>309</td>
      <td>0.096521</td>
    </tr>
    <tr>
      <th>21</th>
      <td>REFERENCES</td>
      <td>197</td>
      <td>0.061536</td>
    </tr>
    <tr>
      <th>22</th>
      <td>DECLARES</td>
      <td>186</td>
      <td>0.058100</td>
    </tr>
    <tr>
      <th>23</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>169</td>
      <td>0.052790</td>
    </tr>
    <tr>
      <th>24</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>161</td>
      <td>0.050291</td>
    </tr>
    <tr>
      <th>25</th>
      <td>HAS_MEMBER</td>
      <td>102</td>
      <td>0.031861</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>0.029362</td>
    </tr>
    <tr>
      <th>27</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.028425</td>
    </tr>
    <tr>
      <th>28</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>0.025614</td>
    </tr>
    <tr>
      <th>29</th>
      <td>COPIES</td>
      <td>79</td>
      <td>0.024677</td>
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
      <td>CONSTRAINED_BY</td>
      <td>4</td>
      <td>0.001249</td>
    </tr>
    <tr>
      <th>1</th>
      <td>REFERENCED_PROJECTS</td>
      <td>5</td>
      <td>0.001562</td>
    </tr>
    <tr>
      <th>2</th>
      <td>MEMBER</td>
      <td>6</td>
      <td>0.001874</td>
    </tr>
    <tr>
      <th>3</th>
      <td>HAS_ROOT</td>
      <td>6</td>
      <td>0.001874</td>
    </tr>
    <tr>
      <th>4</th>
      <td>HAS_NPM_PACKAGE</td>
      <td>6</td>
      <td>0.001874</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_CONFIG</td>
      <td>6</td>
      <td>0.001874</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_ARGUMENT</td>
      <td>6</td>
      <td>0.001874</td>
    </tr>
    <tr>
      <th>7</th>
      <td>EXTENDS</td>
      <td>6</td>
      <td>0.001874</td>
    </tr>
    <tr>
      <th>8</th>
      <td>DECLARES_ENGINE</td>
      <td>6</td>
      <td>0.001874</td>
    </tr>
    <tr>
      <th>9</th>
      <td>CONTAINS_PROJECT</td>
      <td>6</td>
      <td>0.001874</td>
    </tr>
    <tr>
      <th>10</th>
      <td>CALLS</td>
      <td>6</td>
      <td>0.001874</td>
    </tr>
    <tr>
      <th>11</th>
      <td>PARENT</td>
      <td>6</td>
      <td>0.001874</td>
    </tr>
    <tr>
      <th>12</th>
      <td>DECLARES_PEER_DEPENDENCY</td>
      <td>8</td>
      <td>0.002499</td>
    </tr>
    <tr>
      <th>13</th>
      <td>USES</td>
      <td>11</td>
      <td>0.003436</td>
    </tr>
    <tr>
      <th>14</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.005935</td>
    </tr>
    <tr>
      <th>15</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.008746</td>
    </tr>
    <tr>
      <th>16</th>
      <td>INITIALIZED_WITH</td>
      <td>32</td>
      <td>0.009996</td>
    </tr>
    <tr>
      <th>17</th>
      <td>IS_DESCRIBED_IN_NPM_PACKAGE</td>
      <td>33</td>
      <td>0.010308</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_BRANCH</td>
      <td>39</td>
      <td>0.012182</td>
    </tr>
    <tr>
      <th>19</th>
      <td>HAS_HEAD</td>
      <td>40</td>
      <td>0.012495</td>
    </tr>
    <tr>
      <th>20</th>
      <td>RESOLVES_TO</td>
      <td>41</td>
      <td>0.012807</td>
    </tr>
    <tr>
      <th>21</th>
      <td>COPY_OF</td>
      <td>43</td>
      <td>0.013432</td>
    </tr>
    <tr>
      <th>22</th>
      <td>CONTAINS_VALUE</td>
      <td>51</td>
      <td>0.015931</td>
    </tr>
    <tr>
      <th>23</th>
      <td>HAS_PARAMETER</td>
      <td>73</td>
      <td>0.022803</td>
    </tr>
    <tr>
      <th>24</th>
      <td>COPIES</td>
      <td>79</td>
      <td>0.024677</td>
    </tr>
    <tr>
      <th>25</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>0.025614</td>
    </tr>
    <tr>
      <th>26</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>0.028425</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>0.029362</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_MEMBER</td>
      <td>102</td>
      <td>0.031861</td>
    </tr>
    <tr>
      <th>29</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>161</td>
      <td>0.050291</td>
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
      <td>[Git, Change]</td>
      <td>MODIFIES</td>
      <td>[File, Git]</td>
      <td>83882</td>
      <td>83882</td>
      <td>5619</td>
      <td>0.017797</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Git, Commit]</td>
      <td>CONTAINS_CHANGE</td>
      <td>[Git, Change]</td>
      <td>83882</td>
      <td>10932</td>
      <td>83882</td>
      <td>0.009147</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[Git, Change]</td>
      <td>UPDATES</td>
      <td>[File, Git]</td>
      <td>55685</td>
      <td>83882</td>
      <td>5619</td>
      <td>0.011814</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Git, Change]</td>
      <td>CREATES</td>
      <td>[File, Git]</td>
      <td>19620</td>
      <td>83882</td>
      <td>5619</td>
      <td>0.004163</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Git, Commit]</td>
      <td>HAS_PARENT</td>
      <td>[Git, Commit]</td>
      <td>11995</td>
      <td>10932</td>
      <td>10932</td>
      <td>0.010037</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Change]</td>
      <td>DELETES</td>
      <td>[File, Git]</td>
      <td>11844</td>
      <td>83882</td>
      <td>5619</td>
      <td>0.002513</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>10932</td>
      <td>1</td>
      <td>10932</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Author, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>10932</td>
      <td>1244</td>
      <td>10932</td>
      <td>0.080386</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Committer, Git, Person]</td>
      <td>COMMITTED</td>
      <td>[Git, Commit]</td>
      <td>10932</td>
      <td>370</td>
      <td>10932</td>
      <td>0.270270</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_FILE</td>
      <td>[File, Git]</td>
      <td>5619</td>
      <td>1</td>
      <td>5619</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Change]</td>
      <td>RENAMES</td>
      <td>[File, Git]</td>
      <td>3267</td>
      <td>83882</td>
      <td>5619</td>
      <td>0.000693</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[File, Git]</td>
      <td>HAS_NEW_NAME</td>
      <td>[File, Git]</td>
      <td>1751</td>
      <td>5619</td>
      <td>5619</td>
      <td>0.005546</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_TAG</td>
      <td>[Git, Tag]</td>
      <td>1536</td>
      <td>1</td>
      <td>1536</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Git, Tag]</td>
      <td>ON_COMMIT</td>
      <td>[Git, Commit]</td>
      <td>1536</td>
      <td>1536</td>
      <td>10932</td>
      <td>0.009147</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_AUTHOR</td>
      <td>[Author, Git, Person]</td>
      <td>1244</td>
      <td>1</td>
      <td>1244</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Json, Value, Object]</td>
      <td>HAS_KEY</td>
      <td>[Json, Key]</td>
      <td>668</td>
      <td>133</td>
      <td>668</td>
      <td>0.751880</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Json, Key]</td>
      <td>HAS_VALUE</td>
      <td>[Json, Value, Scalar]</td>
      <td>552</td>
      <td>668</td>
      <td>603</td>
      <td>0.137039</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Repository, File, Git]</td>
      <td>HAS_COMMITTER</td>
      <td>[Committer, Git, Person]</td>
      <td>370</td>
      <td>1</td>
      <td>370</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[TS, Function]</td>
      <td>DEPENDS_ON</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>293</td>
      <td>47</td>
      <td>215</td>
      <td>2.899555</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[File, TS, Local, Module]</td>
      <td>DEPENDS_ON</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>236</td>
      <td>6</td>
      <td>215</td>
      <td>18.294574</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[TS, ExternalModule]</td>
      <td>EXPORTS</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>215</td>
      <td>11</td>
      <td>215</td>
      <td>9.090909</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[Package, File, Json, NPM]</td>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>[NPM, Dependency]</td>
      <td>169</td>
      <td>29</td>
      <td>338</td>
      <td>1.724138</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Package, File, Json, NPM]</td>
      <td>DECLARES_DEPENDENCY</td>
      <td>[NPM, Dependency]</td>
      <td>161</td>
      <td>29</td>
      <td>338</td>
      <td>1.642522</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Primitive]</td>
      <td>147</td>
      <td>119</td>
      <td>291</td>
      <td>0.424500</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, TS, Declared]</td>
      <td>REFERENCES</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>143</td>
      <td>276</td>
      <td>215</td>
      <td>0.240984</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Literal]</td>
      <td>119</td>
      <td>119</td>
      <td>136</td>
      <td>0.735294</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Json, Key]</td>
      <td>HAS_VALUE</td>
      <td>[Json, Value, Object]</td>
      <td>104</td>
      <td>668</td>
      <td>133</td>
      <td>0.117059</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Type, Object, TS]</td>
      <td>HAS_MEMBER</td>
      <td>[Type, TS, ObjectMember]</td>
      <td>101</td>
      <td>39</td>
      <td>101</td>
      <td>2.564103</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Package, File, Json, NPM]</td>
      <td>DECLARES_SCRIPT</td>
      <td>[NPM, Script]</td>
      <td>91</td>
      <td>29</td>
      <td>91</td>
      <td>3.448276</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Git, Change]</td>
      <td>COPIES</td>
      <td>[File, Git]</td>
      <td>79</td>
      <td>83882</td>
      <td>5619</td>
      <td>0.000017</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 107168
    total_number_of_relationships (edges): 320138
    -> total directed graph density: 2.7874753028528382e-05
    -> total directed graph density in percent: 0.002787475302852838

