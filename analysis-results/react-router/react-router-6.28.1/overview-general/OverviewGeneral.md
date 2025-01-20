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
      <td>[Json, Key]</td>
      <td>668</td>
      <td>18.816901</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Json, Value, Scalar]</td>
      <td>603</td>
      <td>16.985915</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[NPM, Dependency]</td>
      <td>338</td>
      <td>9.521127</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[Type, TS, Primitive]</td>
      <td>291</td>
      <td>8.197183</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[Type, TS, Declared]</td>
      <td>276</td>
      <td>7.774648</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[TS, ExternalDeclaration]</td>
      <td>212</td>
      <td>5.971831</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Type, TS, Literal]</td>
      <td>136</td>
      <td>3.830986</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Json, Value, Object]</td>
      <td>133</td>
      <td>3.746479</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Type, TS, Union]</td>
      <td>119</td>
      <td>3.352113</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>101</td>
      <td>2.845070</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[NPM, Script]</td>
      <td>91</td>
      <td>2.563380</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[TS, Property]</td>
      <td>65</td>
      <td>1.830986</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[TS, Function]</td>
      <td>47</td>
      <td>1.323944</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Type, TS, FunctionParameter]</td>
      <td>40</td>
      <td>1.126761</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Type, Object, TS]</td>
      <td>39</td>
      <td>1.098592</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[File, Directory]</td>
      <td>34</td>
      <td>0.957746</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[Type, TS, Function]</td>
      <td>34</td>
      <td>0.957746</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[TS, Parameter]</td>
      <td>33</td>
      <td>0.929577</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Package, File, Json, NPM]</td>
      <td>29</td>
      <td>0.816901</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[TS, Variable]</td>
      <td>24</td>
      <td>0.676056</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Value, TS, Literal]</td>
      <td>20</td>
      <td>0.563380</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[jQAssistant, Rule, Concept]</td>
      <td>19</td>
      <td>0.535211</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Type, TS, Intersection]</td>
      <td>17</td>
      <td>0.478873</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[TS, Interface]</td>
      <td>17</td>
      <td>0.478873</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[File, Directory, Local]</td>
      <td>16</td>
      <td>0.450704</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[TS, TypeAlias]</td>
      <td>16</td>
      <td>0.450704</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Value, TS, Declared]</td>
      <td>13</td>
      <td>0.366197</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[Json, Value, Array]</td>
      <td>12</td>
      <td>0.338028</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[TS, ExternalModule]</td>
      <td>11</td>
      <td>0.309859</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Type, TS, NotIdentified]</td>
      <td>11</td>
      <td>0.309859</td>
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
      <td>0.028169</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[File, TS, Scan]</td>
      <td>1</td>
      <td>0.028169</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[TS, Method]</td>
      <td>1</td>
      <td>0.028169</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[TS, Class]</td>
      <td>1</td>
      <td>0.028169</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[TS, Constructor]</td>
      <td>1</td>
      <td>0.028169</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Git, Branch]</td>
      <td>1</td>
      <td>0.028169</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Repository, File, Git]</td>
      <td>1</td>
      <td>0.028169</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Author, Git, Person]</td>
      <td>1</td>
      <td>0.028169</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Committer, Git, Person]</td>
      <td>1</td>
      <td>0.028169</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Value, TS, ObjectMember]</td>
      <td>1</td>
      <td>0.028169</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Git, Tag]</td>
      <td>2</td>
      <td>0.056338</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Git, Commit]</td>
      <td>2</td>
      <td>0.056338</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[TS, Enum]</td>
      <td>2</td>
      <td>0.056338</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[Type, TS, Tuple]</td>
      <td>3</td>
      <td>0.084507</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Value, Object, TS]</td>
      <td>3</td>
      <td>0.084507</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[Value, TS, Function]</td>
      <td>4</td>
      <td>0.112676</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[TS, TypeParameter]</td>
      <td>4</td>
      <td>0.112676</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[Value, TS, Complex]</td>
      <td>5</td>
      <td>0.140845</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Value, TS, Member]</td>
      <td>6</td>
      <td>0.169014</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[Value, TS, Call]</td>
      <td>6</td>
      <td>0.169014</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[Type, TS, TypeParameterReference]</td>
      <td>6</td>
      <td>0.169014</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[File, TS, Local, Module]</td>
      <td>6</td>
      <td>0.169014</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[File, Local]</td>
      <td>6</td>
      <td>0.169014</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Project, TS]</td>
      <td>6</td>
      <td>0.169014</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[NPM, Engine]</td>
      <td>6</td>
      <td>0.169014</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[TS, EnumMember]</td>
      <td>8</td>
      <td>0.225352</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[Type, TS, NotIdentified]</td>
      <td>11</td>
      <td>0.309859</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[TS, ExternalModule]</td>
      <td>11</td>
      <td>0.309859</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Json, Value, Array]</td>
      <td>12</td>
      <td>0.338028</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[Value, TS, Declared]</td>
      <td>13</td>
      <td>0.366197</td>
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
      <td>TS</td>
      <td>1586</td>
      <td>44.676056</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Json</td>
      <td>1445</td>
      <td>40.704225</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Type</td>
      <td>1073</td>
      <td>30.225352</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Value</td>
      <td>806</td>
      <td>22.704225</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Key</td>
      <td>668</td>
      <td>18.816901</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Scalar</td>
      <td>603</td>
      <td>16.985915</td>
    </tr>
    <tr>
      <th>6</th>
      <td>NPM</td>
      <td>464</td>
      <td>13.070423</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Dependency</td>
      <td>338</td>
      <td>9.521127</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Primitive</td>
      <td>291</td>
      <td>8.197183</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Declared</td>
      <td>289</td>
      <td>8.140845</td>
    </tr>
    <tr>
      <th>10</th>
      <td>ExternalDeclaration</td>
      <td>212</td>
      <td>5.971831</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Object</td>
      <td>175</td>
      <td>4.929577</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Literal</td>
      <td>156</td>
      <td>4.394366</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Union</td>
      <td>119</td>
      <td>3.352113</td>
    </tr>
    <tr>
      <th>14</th>
      <td>ObjectMember</td>
      <td>102</td>
      <td>2.873239</td>
    </tr>
    <tr>
      <th>15</th>
      <td>File</td>
      <td>93</td>
      <td>2.619718</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Script</td>
      <td>91</td>
      <td>2.563380</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Function</td>
      <td>85</td>
      <td>2.394366</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Property</td>
      <td>65</td>
      <td>1.830986</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Directory</td>
      <td>50</td>
      <td>1.408451</td>
    </tr>
    <tr>
      <th>20</th>
      <td>FunctionParameter</td>
      <td>40</td>
      <td>1.126761</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Parameter</td>
      <td>33</td>
      <td>0.929577</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Package</td>
      <td>29</td>
      <td>0.816901</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Local</td>
      <td>28</td>
      <td>0.788732</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Variable</td>
      <td>24</td>
      <td>0.676056</td>
    </tr>
    <tr>
      <th>25</th>
      <td>jQAssistant</td>
      <td>20</td>
      <td>0.563380</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Concept</td>
      <td>19</td>
      <td>0.535211</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Rule</td>
      <td>19</td>
      <td>0.535211</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Interface</td>
      <td>17</td>
      <td>0.478873</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Intersection</td>
      <td>17</td>
      <td>0.478873</td>
    </tr>
    <tr>
      <th>30</th>
      <td>TypeAlias</td>
      <td>16</td>
      <td>0.450704</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Array</td>
      <td>12</td>
      <td>0.338028</td>
    </tr>
    <tr>
      <th>32</th>
      <td>ExternalModule</td>
      <td>11</td>
      <td>0.309859</td>
    </tr>
    <tr>
      <th>33</th>
      <td>NotIdentified</td>
      <td>11</td>
      <td>0.309859</td>
    </tr>
    <tr>
      <th>34</th>
      <td>EnumMember</td>
      <td>8</td>
      <td>0.225352</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Git</td>
      <td>8</td>
      <td>0.225352</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Call</td>
      <td>6</td>
      <td>0.169014</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Engine</td>
      <td>6</td>
      <td>0.169014</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Member</td>
      <td>6</td>
      <td>0.169014</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Module</td>
      <td>6</td>
      <td>0.169014</td>
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

    Total number of relationships: 4869





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
      <td>DEPENDS_ON</td>
      <td>876</td>
      <td>17.991374</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HAS_KEY</td>
      <td>668</td>
      <td>13.719450</td>
    </tr>
    <tr>
      <th>2</th>
      <td>HAS_VALUE</td>
      <td>668</td>
      <td>13.719450</td>
    </tr>
    <tr>
      <th>3</th>
      <td>CONTAINS</td>
      <td>594</td>
      <td>12.199630</td>
    </tr>
    <tr>
      <th>4</th>
      <td>OF_TYPE</td>
      <td>337</td>
      <td>6.921339</td>
    </tr>
    <tr>
      <th>5</th>
      <td>EXPORTS</td>
      <td>305</td>
      <td>6.264120</td>
    </tr>
    <tr>
      <th>6</th>
      <td>REFERENCES</td>
      <td>197</td>
      <td>4.046005</td>
    </tr>
    <tr>
      <th>7</th>
      <td>DECLARES</td>
      <td>186</td>
      <td>3.820086</td>
    </tr>
    <tr>
      <th>8</th>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>169</td>
      <td>3.470939</td>
    </tr>
    <tr>
      <th>9</th>
      <td>DECLARES_DEPENDENCY</td>
      <td>161</td>
      <td>3.306634</td>
    </tr>
    <tr>
      <th>10</th>
      <td>HAS_MEMBER</td>
      <td>102</td>
      <td>2.094886</td>
    </tr>
    <tr>
      <th>11</th>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>94</td>
      <td>1.930581</td>
    </tr>
    <tr>
      <th>12</th>
      <td>DECLARES_SCRIPT</td>
      <td>91</td>
      <td>1.868967</td>
    </tr>
    <tr>
      <th>13</th>
      <td>RETURNS</td>
      <td>82</td>
      <td>1.684124</td>
    </tr>
    <tr>
      <th>14</th>
      <td>HAS_PARAMETER</td>
      <td>73</td>
      <td>1.499281</td>
    </tr>
    <tr>
      <th>15</th>
      <td>CONTAINS_VALUE</td>
      <td>51</td>
      <td>1.047443</td>
    </tr>
    <tr>
      <th>16</th>
      <td>IS_DESCRIBED_IN_NPM_PACKAGE</td>
      <td>33</td>
      <td>0.677757</td>
    </tr>
    <tr>
      <th>17</th>
      <td>INITIALIZED_WITH</td>
      <td>32</td>
      <td>0.657219</td>
    </tr>
    <tr>
      <th>18</th>
      <td>REQUIRES_CONCEPT</td>
      <td>28</td>
      <td>0.575067</td>
    </tr>
    <tr>
      <th>19</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.390224</td>
    </tr>
    <tr>
      <th>20</th>
      <td>USES</td>
      <td>11</td>
      <td>0.225919</td>
    </tr>
    <tr>
      <th>21</th>
      <td>DECLARES_PEER_DEPENDENCY</td>
      <td>8</td>
      <td>0.164305</td>
    </tr>
    <tr>
      <th>22</th>
      <td>CALLS</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>23</th>
      <td>CONTAINS_PROJECT</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>24</th>
      <td>DECLARES_ENGINE</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>25</th>
      <td>EXTENDS</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>26</th>
      <td>HAS_ARGUMENT</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>27</th>
      <td>HAS_CONFIG</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>28</th>
      <td>HAS_NPM_PACKAGE</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>29</th>
      <td>HAS_ROOT</td>
      <td>6</td>
      <td>0.123229</td>
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
      <td>HAS_COMMITTER</td>
      <td>1</td>
      <td>0.020538</td>
    </tr>
    <tr>
      <th>1</th>
      <td>HAS_BRANCH</td>
      <td>1</td>
      <td>0.020538</td>
    </tr>
    <tr>
      <th>2</th>
      <td>HAS_AUTHOR</td>
      <td>1</td>
      <td>0.020538</td>
    </tr>
    <tr>
      <th>3</th>
      <td>ON_COMMIT</td>
      <td>2</td>
      <td>0.041076</td>
    </tr>
    <tr>
      <th>4</th>
      <td>HAS_TAG</td>
      <td>2</td>
      <td>0.041076</td>
    </tr>
    <tr>
      <th>5</th>
      <td>HAS_HEAD</td>
      <td>2</td>
      <td>0.041076</td>
    </tr>
    <tr>
      <th>6</th>
      <td>HAS_COMMIT</td>
      <td>2</td>
      <td>0.041076</td>
    </tr>
    <tr>
      <th>7</th>
      <td>CONSTRAINED_BY</td>
      <td>4</td>
      <td>0.082152</td>
    </tr>
    <tr>
      <th>8</th>
      <td>COMMITTED</td>
      <td>4</td>
      <td>0.082152</td>
    </tr>
    <tr>
      <th>9</th>
      <td>REFERENCED_PROJECTS</td>
      <td>5</td>
      <td>0.102690</td>
    </tr>
    <tr>
      <th>10</th>
      <td>CALLS</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>11</th>
      <td>CONTAINS_PROJECT</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>12</th>
      <td>DECLARES_ENGINE</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>13</th>
      <td>EXTENDS</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>14</th>
      <td>HAS_ROOT</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>15</th>
      <td>HAS_CONFIG</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>16</th>
      <td>HAS_NPM_PACKAGE</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>17</th>
      <td>PARENT</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>18</th>
      <td>HAS_ARGUMENT</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>19</th>
      <td>MEMBER</td>
      <td>6</td>
      <td>0.123229</td>
    </tr>
    <tr>
      <th>20</th>
      <td>DECLARES_PEER_DEPENDENCY</td>
      <td>8</td>
      <td>0.164305</td>
    </tr>
    <tr>
      <th>21</th>
      <td>USES</td>
      <td>11</td>
      <td>0.225919</td>
    </tr>
    <tr>
      <th>22</th>
      <td>INCLUDES_CONCEPT</td>
      <td>19</td>
      <td>0.390224</td>
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
      <td>[Json, Value, Object]</td>
      <td>HAS_KEY</td>
      <td>[Json, Key]</td>
      <td>668</td>
      <td>133</td>
      <td>668</td>
      <td>0.751880</td>
    </tr>
    <tr>
      <th>1</th>
      <td>[Json, Key]</td>
      <td>HAS_VALUE</td>
      <td>[Json, Value, Scalar]</td>
      <td>552</td>
      <td>668</td>
      <td>603</td>
      <td>0.137039</td>
    </tr>
    <tr>
      <th>2</th>
      <td>[TS, Function]</td>
      <td>DEPENDS_ON</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>289</td>
      <td>47</td>
      <td>212</td>
      <td>2.900442</td>
    </tr>
    <tr>
      <th>3</th>
      <td>[File, TS, Local, Module]</td>
      <td>DEPENDS_ON</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>233</td>
      <td>6</td>
      <td>212</td>
      <td>18.317610</td>
    </tr>
    <tr>
      <th>4</th>
      <td>[TS, ExternalModule]</td>
      <td>EXPORTS</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>212</td>
      <td>11</td>
      <td>212</td>
      <td>9.090909</td>
    </tr>
    <tr>
      <th>5</th>
      <td>[Package, File, Json, NPM]</td>
      <td>DECLARES_DEV_DEPENDENCY</td>
      <td>[NPM, Dependency]</td>
      <td>169</td>
      <td>29</td>
      <td>338</td>
      <td>1.724138</td>
    </tr>
    <tr>
      <th>6</th>
      <td>[Package, File, Json, NPM]</td>
      <td>DECLARES_DEPENDENCY</td>
      <td>[NPM, Dependency]</td>
      <td>161</td>
      <td>29</td>
      <td>338</td>
      <td>1.642522</td>
    </tr>
    <tr>
      <th>7</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Primitive]</td>
      <td>147</td>
      <td>119</td>
      <td>291</td>
      <td>0.424500</td>
    </tr>
    <tr>
      <th>8</th>
      <td>[Type, TS, Declared]</td>
      <td>REFERENCES</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>143</td>
      <td>276</td>
      <td>212</td>
      <td>0.244394</td>
    </tr>
    <tr>
      <th>9</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Literal]</td>
      <td>119</td>
      <td>119</td>
      <td>136</td>
      <td>0.735294</td>
    </tr>
    <tr>
      <th>10</th>
      <td>[Json, Key]</td>
      <td>HAS_VALUE</td>
      <td>[Json, Value, Object]</td>
      <td>104</td>
      <td>668</td>
      <td>133</td>
      <td>0.117059</td>
    </tr>
    <tr>
      <th>11</th>
      <td>[Type, Object, TS]</td>
      <td>HAS_MEMBER</td>
      <td>[Type, TS, ObjectMember]</td>
      <td>101</td>
      <td>39</td>
      <td>101</td>
      <td>2.564103</td>
    </tr>
    <tr>
      <th>12</th>
      <td>[Package, File, Json, NPM]</td>
      <td>DECLARES_SCRIPT</td>
      <td>[NPM, Script]</td>
      <td>91</td>
      <td>29</td>
      <td>91</td>
      <td>3.448276</td>
    </tr>
    <tr>
      <th>13</th>
      <td>[TS, Function]</td>
      <td>DEPENDS_ON</td>
      <td>[TS, ExternalModule]</td>
      <td>76</td>
      <td>47</td>
      <td>11</td>
      <td>14.700193</td>
    </tr>
    <tr>
      <th>14</th>
      <td>[Type, TS, Union]</td>
      <td>CONTAINS</td>
      <td>[Type, TS, Declared]</td>
      <td>70</td>
      <td>119</td>
      <td>276</td>
      <td>0.213129</td>
    </tr>
    <tr>
      <th>15</th>
      <td>[File, Directory]</td>
      <td>CONTAINS</td>
      <td>[File, Directory]</td>
      <td>63</td>
      <td>34</td>
      <td>34</td>
      <td>5.449827</td>
    </tr>
    <tr>
      <th>16</th>
      <td>[TS, Interface]</td>
      <td>DECLARES</td>
      <td>[TS, Property]</td>
      <td>61</td>
      <td>17</td>
      <td>65</td>
      <td>5.520362</td>
    </tr>
    <tr>
      <th>17</th>
      <td>[File, Directory]</td>
      <td>CONTAINS</td>
      <td>[Package, File, Json, NPM]</td>
      <td>58</td>
      <td>34</td>
      <td>29</td>
      <td>5.882353</td>
    </tr>
    <tr>
      <th>18</th>
      <td>[Json, Value, Array]</td>
      <td>CONTAINS_VALUE</td>
      <td>[Json, Value, Scalar]</td>
      <td>51</td>
      <td>12</td>
      <td>603</td>
      <td>0.704809</td>
    </tr>
    <tr>
      <th>19</th>
      <td>[File, TS, Local, Module]</td>
      <td>DECLARES</td>
      <td>[TS, Function]</td>
      <td>47</td>
      <td>6</td>
      <td>47</td>
      <td>16.666667</td>
    </tr>
    <tr>
      <th>20</th>
      <td>[TS, Property]</td>
      <td>OF_TYPE</td>
      <td>[Type, TS, Union]</td>
      <td>46</td>
      <td>65</td>
      <td>119</td>
      <td>0.594699</td>
    </tr>
    <tr>
      <th>21</th>
      <td>[TS, Variable]</td>
      <td>DEPENDS_ON</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>44</td>
      <td>24</td>
      <td>212</td>
      <td>0.864780</td>
    </tr>
    <tr>
      <th>22</th>
      <td>[Type, TS, Declared]</td>
      <td>HAS_TYPE_ARGUMENT</td>
      <td>[Type, TS, Declared]</td>
      <td>41</td>
      <td>276</td>
      <td>276</td>
      <td>0.053823</td>
    </tr>
    <tr>
      <th>23</th>
      <td>[Type, TS, Function]</td>
      <td>HAS_PARAMETER</td>
      <td>[Type, TS, FunctionParameter]</td>
      <td>40</td>
      <td>34</td>
      <td>40</td>
      <td>2.941176</td>
    </tr>
    <tr>
      <th>24</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>OF_TYPE</td>
      <td>[Type, TS, Union]</td>
      <td>35</td>
      <td>101</td>
      <td>119</td>
      <td>0.291206</td>
    </tr>
    <tr>
      <th>25</th>
      <td>[NPM, Dependency]</td>
      <td>IS_DESCRIBED_IN_NPM_PACKAGE</td>
      <td>[Package, File, Json, NPM]</td>
      <td>33</td>
      <td>338</td>
      <td>29</td>
      <td>0.336666</td>
    </tr>
    <tr>
      <th>26</th>
      <td>[TS, Function]</td>
      <td>HAS_PARAMETER</td>
      <td>[TS, Parameter]</td>
      <td>33</td>
      <td>47</td>
      <td>33</td>
      <td>2.127660</td>
    </tr>
    <tr>
      <th>27</th>
      <td>[File, TS, Local, Module]</td>
      <td>EXPORTS</td>
      <td>[TS, ExternalDeclaration]</td>
      <td>32</td>
      <td>6</td>
      <td>212</td>
      <td>2.515723</td>
    </tr>
    <tr>
      <th>28</th>
      <td>[Type, TS, ObjectMember]</td>
      <td>OF_TYPE</td>
      <td>[Type, TS, Primitive]</td>
      <td>32</td>
      <td>101</td>
      <td>291</td>
      <td>0.108877</td>
    </tr>
    <tr>
      <th>29</th>
      <td>[File, TS, Local, Module]</td>
      <td>EXPORTS</td>
      <td>[TS, Function]</td>
      <td>31</td>
      <td>6</td>
      <td>47</td>
      <td>10.992908</td>
    </tr>
  </tbody>
</table>
</div>



## Graph Density

    total_number_of_nodes (vertices): 3550
    total_number_of_relationships (edges): 4869
    -> total directed graph density: 0.0003864607764932792
    -> total directed graph density in percent: 0.03864607764932792

