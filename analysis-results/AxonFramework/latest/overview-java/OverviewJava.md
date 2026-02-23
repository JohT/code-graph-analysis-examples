# Overview for Java
<br>  

### References
- [jqassistant](https://jqassistant.org)
- [Neo4j Python Driver](https://neo4j.com/docs/api/python-driver/current)





## Overview

### Table 1 - Size




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>nodeCount</th>
      <th>relationshipCount</th>
      <th>artifactCount</th>
      <th>packageCount</th>
      <th>typeCount</th>
      <th>methodCount</th>
      <th>memberCount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>522598</td>
      <td>1621752</td>
      <td>11</td>
      <td>124</td>
      <td>1784</td>
      <td>5603</td>
      <td>7061</td>
    </tr>
  </tbody>
</table>
</div>



## Artifacts

### Table 2a - Largest 30 types per artifact

This table shows the largest (number of types) artifacts and their kind of types (Class, Interface, Enum, Annotation).
The whole table can be found in the CSV report `Number_of_types_per_artifact`.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>numberOfArtifactTypes</th>
      <th>languageElement</th>
      <th>numberOfTypes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-messaging-5.0.2</td>
      <td>570</td>
      <td>Class</td>
      <td>372</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-messaging-5.0.2</td>
      <td>570</td>
      <td>Annotation</td>
      <td>27</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-messaging-5.0.2</td>
      <td>570</td>
      <td>Interface</td>
      <td>137</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-messaging-5.0.2</td>
      <td>570</td>
      <td>Enum</td>
      <td>8</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-common-5.0.2</td>
      <td>156</td>
      <td>Class</td>
      <td>104</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-common-5.0.2</td>
      <td>156</td>
      <td>Interface</td>
      <td>42</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-common-5.0.2</td>
      <td>156</td>
      <td>Enum</td>
      <td>4</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-common-5.0.2</td>
      <td>156</td>
      <td>Annotation</td>
      <td>2</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-eventsourcing-5.0.2</td>
      <td>104</td>
      <td>Class</td>
      <td>65</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-eventsourcing-5.0.2</td>
      <td>104</td>
      <td>Interface</td>
      <td>24</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-eventsourcing-5.0.2</td>
      <td>104</td>
      <td>Annotation</td>
      <td>7</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-modelling-5.0.2</td>
      <td>93</td>
      <td>Class</td>
      <td>61</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-modelling-5.0.2</td>
      <td>93</td>
      <td>Interface</td>
      <td>29</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-modelling-5.0.2</td>
      <td>93</td>
      <td>Annotation</td>
      <td>3</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-test-5.0.2</td>
      <td>73</td>
      <td>Class</td>
      <td>50</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-test-5.0.2</td>
      <td>73</td>
      <td>Interface</td>
      <td>18</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-server-connector-5.0.2</td>
      <td>72</td>
      <td>Class</td>
      <td>56</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-server-connector-5.0.2</td>
      <td>72</td>
      <td>Interface</td>
      <td>10</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-server-connector-5.0.2</td>
      <td>72</td>
      <td>Enum</td>
      <td>2</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-spring-boot-autoconfigure-5.0.2</td>
      <td>72</td>
      <td>Class</td>
      <td>64</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-spring-boot-autoconfigure-5.0.2</td>
      <td>72</td>
      <td>Annotation</td>
      <td>3</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-spring-boot-autoconfigure-5.0.2</td>
      <td>72</td>
      <td>Interface</td>
      <td>1</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-spring-boot-autoconfigure-5.0.2</td>
      <td>72</td>
      <td>Enum</td>
      <td>2</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-conversion-5.0.2</td>
      <td>30</td>
      <td>Class</td>
      <td>23</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-conversion-5.0.2</td>
      <td>30</td>
      <td>Interface</td>
      <td>5</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-update-5.0.2</td>
      <td>23</td>
      <td>Class</td>
      <td>14</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-update-5.0.2</td>
      <td>23</td>
      <td>Enum</td>
      <td>1</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-update-5.0.2</td>
      <td>23</td>
      <td>Interface</td>
      <td>3</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-metrics-micrometer-5.0.2</td>
      <td>13</td>
      <td>Class</td>
      <td>13</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-tracing-opentelemetry-5.0.2</td>
      <td>5</td>
      <td>Class</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>



### Table 2b - Largest 30 types per artifact grouped

This table shows the largest (number of types) artifacts each in one row, their kind of types in columns and the count of them as values.

The source data for this aggregated table can be found in the CSV report `Number_of_types_per_artifact`.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>languageElement</th>
      <th>Class</th>
      <th>Interface</th>
      <th>Annotation</th>
      <th>Enum</th>
    </tr>
    <tr>
      <th>artifactName</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>axon-messaging-5.0.2</th>
      <td>372</td>
      <td>137</td>
      <td>27</td>
      <td>8</td>
    </tr>
    <tr>
      <th>axon-common-5.0.2</th>
      <td>104</td>
      <td>42</td>
      <td>2</td>
      <td>4</td>
    </tr>
    <tr>
      <th>axon-eventsourcing-5.0.2</th>
      <td>65</td>
      <td>24</td>
      <td>7</td>
      <td>0</td>
    </tr>
    <tr>
      <th>axon-modelling-5.0.2</th>
      <td>61</td>
      <td>29</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>axon-spring-boot-autoconfigure-5.0.2</th>
      <td>64</td>
      <td>1</td>
      <td>3</td>
      <td>2</td>
    </tr>
    <tr>
      <th>axon-server-connector-5.0.2</th>
      <td>56</td>
      <td>10</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>axon-test-5.0.2</th>
      <td>50</td>
      <td>18</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>axon-conversion-5.0.2</th>
      <td>23</td>
      <td>5</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>axon-update-5.0.2</th>
      <td>14</td>
      <td>3</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>axon-metrics-micrometer-5.0.2</th>
      <td>13</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>axon-tracing-opentelemetry-5.0.2</th>
      <td>5</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>



### Table 2b Chart 1 - 30 largest artifacts and their types stacked


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewJava_files/OverviewJava_19_1.png)
    


### Table 2c - Largest 30 types per artifact (grouped and normalized in %)




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>languageElement</th>
      <th>Class</th>
      <th>Interface</th>
      <th>Annotation</th>
      <th>Enum</th>
    </tr>
    <tr>
      <th>artifactName</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>axon-messaging-5.0.2</th>
      <td>68.382353</td>
      <td>25.183824</td>
      <td>4.963235</td>
      <td>1.470588</td>
    </tr>
    <tr>
      <th>axon-common-5.0.2</th>
      <td>68.421053</td>
      <td>27.631579</td>
      <td>1.315789</td>
      <td>2.631579</td>
    </tr>
    <tr>
      <th>axon-eventsourcing-5.0.2</th>
      <td>67.708333</td>
      <td>25.000000</td>
      <td>7.291667</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>axon-modelling-5.0.2</th>
      <td>65.591398</td>
      <td>31.182796</td>
      <td>3.225806</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>axon-spring-boot-autoconfigure-5.0.2</th>
      <td>91.428571</td>
      <td>1.428571</td>
      <td>4.285714</td>
      <td>2.857143</td>
    </tr>
    <tr>
      <th>axon-server-connector-5.0.2</th>
      <td>82.352941</td>
      <td>14.705882</td>
      <td>0.000000</td>
      <td>2.941176</td>
    </tr>
    <tr>
      <th>axon-test-5.0.2</th>
      <td>73.529412</td>
      <td>26.470588</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>axon-conversion-5.0.2</th>
      <td>82.142857</td>
      <td>17.857143</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>axon-update-5.0.2</th>
      <td>77.777778</td>
      <td>16.666667</td>
      <td>0.000000</td>
      <td>5.555556</td>
    </tr>
    <tr>
      <th>axon-metrics-micrometer-5.0.2</th>
      <td>100.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>axon-tracing-opentelemetry-5.0.2</th>
      <td>100.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
  </tbody>
</table>
</div>



### Table 2c Chart 1 - Top 30 artifacts with the highest relative amount of classes in %


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewJava_files/OverviewJava_23_1.png)
    


### Table 2c Chart 2 - Top 30 artifacts with the highest relative amount of interfaces in %


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewJava_files/OverviewJava_25_1.png)
    


### Table 2c Chart 3 - Top 30 artifacts with the highest relative amount of enums in %


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewJava_files/OverviewJava_27_1.png)
    


### Table 2c Chart 4 - Top 30 artifacts with the highest relative amount of annotations in %


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewJava_files/OverviewJava_29_1.png)
    


### Table 3 - Top 30 artifacts with the highest package count

The whole table can be found in the CSV report `Number_of_packages_per_artifact`.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>numberOfPackages</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-messaging-5.0.2</td>
      <td>57</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-common-5.0.2</td>
      <td>15</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-eventsourcing-5.0.2</td>
      <td>8</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-spring-boot-autoconfigure-5.0.2</td>
      <td>7</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-modelling-5.0.2</td>
      <td>7</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-test-5.0.2</td>
      <td>5</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-update-5.0.2</td>
      <td>5</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-server-connector-5.0.2</td>
      <td>5</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-conversion-5.0.2</td>
      <td>4</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.2</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>



### Table 3 Chart 1 - Number of packages per artifact

The following chat shows artifacts with the largest package count in percentage. Artifacts with less than 0.7% package count are grouped into "others" to focus on the most significant artifacts regarding their package count.


    <Figure size 640x480 with 0 Axes>



    
![png](OverviewJava_files/OverviewJava_33_1.png)
    

