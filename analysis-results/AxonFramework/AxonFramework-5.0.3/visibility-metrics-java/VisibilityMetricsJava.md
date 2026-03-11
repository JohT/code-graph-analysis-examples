# Visibility Metrics for Java
<br>  

### References
- [Visibility Metrics and the Importance of Hiding Things](https://dzone.com/articles/visibility-metrics-and-the-importance-of-hiding-th)
- [Calculate metrics](https://101.jqassistant.org/calculate-metrics/index.html)
- [Controlling Access to Members of a Class](https://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html)
- [Neo4j Python Driver](https://neo4j.com/docs/api/python-driver/current)









## Relative Visibility Of Types

A Java class or interface may be declared with the modifier public, in which case it is visible to all classes everywhere. If a class or interface has no modifier (the default, also known as package-private), it is visible only within its own package.

The relative visibility is the number of inner components that are visible outside (public) divided by the number of all types:

$$ relative visibility = \frac{public\:types}{all\:types} $$

Using package protected types is one of many ways to improve encapsulation and implementation detail hiding.

### How to apply the results

The relative visibility is between zero (all types are package protected) and one (all types are public). A value lower than one means that there are types that are declared package protected. The lower the value is, the better implementation details are hidden. 

Non public classes can't be accessed from another package so they can be changed without affecting code in other packages. They clearly indicate functionality that only belongs to one package. This also motivates to use more classes and to split up code into smaller pieces with a single responsibility and reason to change.

### Table 1a - Top 40 artifacts with lowest median of package protection encapsulation

This table shows the relative visibility statistics aggregated for all packages per artifact and focusses on artifacts with many packages and hardly any package protected types (lowest median, high visibility). Package protected types would help to  improve encapsulation.

Only the top 40 entries are shown. The whole table can be found in the following CSV report:  
`Global_relative_visibility_statistics_for_types`




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifact</th>
      <th>all</th>
      <th>public</th>
      <th>min</th>
      <th>max</th>
      <th>average</th>
      <th>percentile25</th>
      <th>percentile50</th>
      <th>percentile75</th>
      <th>percentile90</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-common-5.0.3</td>
      <td>156</td>
      <td>129</td>
      <td>0.615385</td>
      <td>1.000000</td>
      <td>0.893102</td>
      <td>0.791304</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>75</td>
      <td>53</td>
      <td>0.512195</td>
      <td>1.000000</td>
      <td>0.887081</td>
      <td>0.848684</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-conversion-5.0.3</td>
      <td>35</td>
      <td>32</td>
      <td>0.700000</td>
      <td>1.000000</td>
      <td>0.940000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-update-5.0.3</td>
      <td>23</td>
      <td>23</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-tracing-opentelemetry-5.0.3</td>
      <td>5</td>
      <td>5</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-modelling-5.0.3</td>
      <td>92</td>
      <td>84</td>
      <td>0.692308</td>
      <td>1.000000</td>
      <td>0.901923</td>
      <td>0.860577</td>
      <td>0.900000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-messaging-5.0.3</td>
      <td>579</td>
      <td>439</td>
      <td>0.250000</td>
      <td>1.000000</td>
      <td>0.802085</td>
      <td>0.727273</td>
      <td>0.842105</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-server-connector-5.0.3</td>
      <td>72</td>
      <td>58</td>
      <td>0.642857</td>
      <td>0.892857</td>
      <td>0.788495</td>
      <td>0.727273</td>
      <td>0.833333</td>
      <td>0.846154</td>
      <td>0.874176</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-test-5.0.3</td>
      <td>78</td>
      <td>63</td>
      <td>0.600000</td>
      <td>1.000000</td>
      <td>0.809768</td>
      <td>0.726562</td>
      <td>0.791667</td>
      <td>0.925725</td>
      <td>0.978261</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.3</td>
      <td>16</td>
      <td>12</td>
      <td>0.727273</td>
      <td>1.000000</td>
      <td>0.825758</td>
      <td>0.738636</td>
      <td>0.750000</td>
      <td>0.875000</td>
      <td>0.950000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>100</td>
      <td>66</td>
      <td>0.200000</td>
      <td>0.900000</td>
      <td>0.599721</td>
      <td>0.480769</td>
      <td>0.666667</td>
      <td>0.734921</td>
      <td>0.813333</td>
    </tr>
  </tbody>
</table>
</div>



### Table 1b - Top 40 artifacts with highest median of package protection encapsulation

This table shows the relative visibility statistics aggregated for all packages per artifact and focusses on artifacts with many packages and the highest median of package protected types (low visibility). Package protected types help to improve encapsulation.

Only the top 40 entries are shown. The whole table can be found in the following CSV report:  
`Global_relative_visibility_statistics_for_types`




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifact</th>
      <th>all</th>
      <th>public</th>
      <th>min</th>
      <th>max</th>
      <th>average</th>
      <th>percentile25</th>
      <th>percentile50</th>
      <th>percentile75</th>
      <th>percentile90</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>100</td>
      <td>66</td>
      <td>0.200000</td>
      <td>0.900000</td>
      <td>0.599721</td>
      <td>0.480769</td>
      <td>0.666667</td>
      <td>0.734921</td>
      <td>0.813333</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-metrics-micrometer-5.0.3</td>
      <td>16</td>
      <td>12</td>
      <td>0.727273</td>
      <td>1.000000</td>
      <td>0.825758</td>
      <td>0.738636</td>
      <td>0.750000</td>
      <td>0.875000</td>
      <td>0.950000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-test-5.0.3</td>
      <td>78</td>
      <td>63</td>
      <td>0.600000</td>
      <td>1.000000</td>
      <td>0.809768</td>
      <td>0.726562</td>
      <td>0.791667</td>
      <td>0.925725</td>
      <td>0.978261</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-server-connector-5.0.3</td>
      <td>72</td>
      <td>58</td>
      <td>0.642857</td>
      <td>0.892857</td>
      <td>0.788495</td>
      <td>0.727273</td>
      <td>0.833333</td>
      <td>0.846154</td>
      <td>0.874176</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-messaging-5.0.3</td>
      <td>579</td>
      <td>439</td>
      <td>0.250000</td>
      <td>1.000000</td>
      <td>0.802085</td>
      <td>0.727273</td>
      <td>0.842105</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-modelling-5.0.3</td>
      <td>92</td>
      <td>84</td>
      <td>0.692308</td>
      <td>1.000000</td>
      <td>0.901923</td>
      <td>0.860577</td>
      <td>0.900000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-common-5.0.3</td>
      <td>156</td>
      <td>129</td>
      <td>0.615385</td>
      <td>1.000000</td>
      <td>0.893102</td>
      <td>0.791304</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>75</td>
      <td>53</td>
      <td>0.512195</td>
      <td>1.000000</td>
      <td>0.887081</td>
      <td>0.848684</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-conversion-5.0.3</td>
      <td>35</td>
      <td>32</td>
      <td>0.700000</td>
      <td>1.000000</td>
      <td>0.940000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-update-5.0.3</td>
      <td>23</td>
      <td>23</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.3</td>
      <td>5</td>
      <td>5</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>



### Table 1 Chart 1 - Relative visibility in artifacts

    /home/runner/miniconda3/envs/codegraph/lib/python3.12/site-packages/pandas/plotting/_matplotlib/core.py:1351: UserWarning: No data for colormapping provided via 'c'. Parameters 'cmap' will be ignored
      scatter = ax.scatter(
    /home/runner/miniconda3/envs/codegraph/lib/python3.12/site-packages/pandas/plotting/_matplotlib/core.py:1351: UserWarning: No data for colormapping provided via 'c'. Parameters 'cmap' will be ignored
      scatter = ax.scatter(
    /home/runner/miniconda3/envs/codegraph/lib/python3.12/site-packages/pandas/plotting/_matplotlib/core.py:1351: UserWarning: No data for colormapping provided via 'c'. Parameters 'cmap' will be ignored
      scatter = ax.scatter(



    <Figure size 640x480 with 0 Axes>



    
![png](VisibilityMetricsJava_files/VisibilityMetricsJava_16_2.png)
    


### Table 2a - Top 40 packages with the highest visibility and lowest encapsulation

This table shows the relative visibility statistics per packages and artifact and focusses on packages with many types, hardly any package protected ones and therefore the highest relative visibility (lowest encapsulation). Package protected types would help to improve encapsulation.

Only the top 40 entries are shown. The whole table can be found in the following CSV report:  
`Relative_visibility_public_types_to_all_types_per_package`




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>fullQualifiedPackageName</th>
      <th>packageName</th>
      <th>publicTypes</th>
      <th>allTypes</th>
      <th>relativeVisibility</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity.annotation</td>
      <td>annotation</td>
      <td>18</td>
      <td>18</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling</td>
      <td>modelling</td>
      <td>16</td>
      <td>16</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.conf...</td>
      <td>configuration</td>
      <td>14</td>
      <td>14</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity.child</td>
      <td>child</td>
      <td>14</td>
      <td>14</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.jdbc</td>
      <td>jdbc</td>
      <td>12</td>
      <td>12</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.sequencing</td>
      <td>sequencing</td>
      <td>11</td>
      <td>11</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-conversion-5.0.3</td>
      <td>org.axonframework.conversion.avro</td>
      <td>avro</td>
      <td>10</td>
      <td>10</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.property</td>
      <td>property</td>
      <td>9</td>
      <td>9</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.proc...</td>
      <td>jdbc</td>
      <td>9</td>
      <td>9</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.tracing</td>
      <td>tracing</td>
      <td>7</td>
      <td>7</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.queryhandling.tracing</td>
      <td>tracing</td>
      <td>7</td>
      <td>7</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>org.axonframework.extension.springboot.util</td>
      <td>util</td>
      <td>7</td>
      <td>7</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-update-5.0.3</td>
      <td>org.axonframework.update.configuration</td>
      <td>configuration</td>
      <td>7</td>
      <td>7</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.util</td>
      <td>util</td>
      <td>6</td>
      <td>6</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.tracing.attributes</td>
      <td>attributes</td>
      <td>6</td>
      <td>6</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.correlation</td>
      <td>correlation</td>
      <td>6</td>
      <td>6</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-update-5.0.3</td>
      <td>org.axonframework.update.api</td>
      <td>api</td>
      <td>6</td>
      <td>6</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.lifecycle</td>
      <td>lifecycle</td>
      <td>5</td>
      <td>5</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-conversion-5.0.3</td>
      <td>org.axonframework.conversion.converter</td>
      <td>converter</td>
      <td>5</td>
      <td>5</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-conversion-5.0.3</td>
      <td>org.axonframework.conversion.jackson</td>
      <td>jackson</td>
      <td>5</td>
      <td>5</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-conversion-5.0.3</td>
      <td>org.axonframework.conversion.jackson2</td>
      <td>jackson2</td>
      <td>5</td>
      <td>5</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.monitoring.interce...</td>
      <td>interception</td>
      <td>5</td>
      <td>5</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.proc...</td>
      <td>store</td>
      <td>5</td>
      <td>5</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.proc...</td>
      <td>subscribing</td>
      <td>5</td>
      <td>5</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-tracing-opentelemetry-5.0.3</td>
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>opentelemetry</td>
      <td>5</td>
      <td>5</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-update-5.0.3</td>
      <td>org.axonframework.update</td>
      <td>update</td>
      <td>5</td>
      <td>5</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.jpa</td>
      <td>jpa</td>
      <td>4</td>
      <td>4</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.proc...</td>
      <td>jpa</td>
      <td>4</td>
      <td>4</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.replay</td>
      <td>replay</td>
      <td>4</td>
      <td>4</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-update-5.0.3</td>
      <td>org.axonframework.update.detection</td>
      <td>detection</td>
      <td>4</td>
      <td>4</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>30</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.proc...</td>
      <td>errorhandling</td>
      <td>3</td>
      <td>3</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>31</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.proc...</td>
      <td>processing</td>
      <td>3</td>
      <td>3</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>32</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.configuration...</td>
      <td>reflection</td>
      <td>3</td>
      <td>3</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>33</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.function</td>
      <td>function</td>
      <td>2</td>
      <td>2</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>34</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.configuration</td>
      <td>configuration</td>
      <td>2</td>
      <td>2</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>35</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.conv...</td>
      <td>conversion</td>
      <td>2</td>
      <td>2</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>36</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.conversion</td>
      <td>conversion</td>
      <td>2</td>
      <td>2</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>37</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.queryhandling.gateway</td>
      <td>gateway</td>
      <td>2</td>
      <td>2</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>38</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.reflection</td>
      <td>reflection</td>
      <td>2</td>
      <td>2</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>39</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>org.axonframework.extension.springboot.actuato...</td>
      <td>axonserver</td>
      <td>2</td>
      <td>2</td>
      <td>1.0</td>
    </tr>
  </tbody>
</table>
</div>



### Table 2b - Top 40 packages with the lowest visibility and highest encapsulation

This table shows the relative visibility statistics per packages and artifact and focusses on packages with many types, many package protected ones and therefore the lowest relative visibility (highest encapsulation). Package protected types help to improve encapsulation. Zero percent visibility and therefore packages with no public visible type are suspicious to be dead code.

Only the top 40 entries are shown. The whole table can be found in the following CSV report:  
`Relative_visibility_public_types_to_all_types_per_package`




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>fullQualifiedPackageName</th>
      <th>packageName</th>
      <th>publicTypes</th>
      <th>allTypes</th>
      <th>relativeVisibility</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>org.axonframework.eventsourcing.eventstore.inm...</td>
      <td>inmemory</td>
      <td>1</td>
      <td>5</td>
      <td>0.200000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.proc...</td>
      <td>pooled</td>
      <td>6</td>
      <td>24</td>
      <td>0.250000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.queryhandling.inte...</td>
      <td>interception</td>
      <td>2</td>
      <td>8</td>
      <td>0.250000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.monitoring.configu...</td>
      <td>configuration</td>
      <td>3</td>
      <td>9</td>
      <td>0.333333</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.proc...</td>
      <td>inmemory</td>
      <td>1</td>
      <td>3</td>
      <td>0.333333</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>org.axonframework.eventsourcing.eventstore.jpa</td>
      <td>jpa</td>
      <td>6</td>
      <td>13</td>
      <td>0.461538</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.interception</td>
      <td>interception</td>
      <td>10</td>
      <td>21</td>
      <td>0.476190</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>org.axonframework.eventsourcing.configuration</td>
      <td>configuration</td>
      <td>7</td>
      <td>14</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.commandhandling.in...</td>
      <td>interception</td>
      <td>3</td>
      <td>6</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.proc...</td>
      <td>annotation</td>
      <td>1</td>
      <td>2</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.unitofwork.an...</td>
      <td>annotation</td>
      <td>1</td>
      <td>2</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.unitofwork.tr...</td>
      <td>jdbc</td>
      <td>1</td>
      <td>2</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.unitofwork.tr...</td>
      <td>jpa</td>
      <td>1</td>
      <td>2</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>autoconfig</td>
      <td>21</td>
      <td>41</td>
      <td>0.512195</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventstreaming</td>
      <td>eventstreaming</td>
      <td>9</td>
      <td>16</td>
      <td>0.562500</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-test-5.0.3</td>
      <td>org.axonframework.test</td>
      <td>test</td>
      <td>3</td>
      <td>5</td>
      <td>0.600000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.caching</td>
      <td>caching</td>
      <td>8</td>
      <td>13</td>
      <td>0.615385</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>core</td>
      <td>50</td>
      <td>80</td>
      <td>0.625000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.infra</td>
      <td>infra</td>
      <td>5</td>
      <td>8</td>
      <td>0.625000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>event</td>
      <td>9</td>
      <td>14</td>
      <td>0.642857</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>org.axonframework.eventsourcing.annotation.ref...</td>
      <td>reflection</td>
      <td>4</td>
      <td>6</td>
      <td>0.666667</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.inte...</td>
      <td>interception</td>
      <td>2</td>
      <td>3</td>
      <td>0.666667</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.configuration</td>
      <td>configuration</td>
      <td>9</td>
      <td>13</td>
      <td>0.692308</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-conversion-5.0.3</td>
      <td>org.axonframework.conversion</td>
      <td>conversion</td>
      <td>7</td>
      <td>10</td>
      <td>0.700000</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.repl...</td>
      <td>annotation</td>
      <td>7</td>
      <td>10</td>
      <td>0.700000</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>org.axonframework.eventsourcing</td>
      <td>eventsourcing</td>
      <td>5</td>
      <td>7</td>
      <td>0.714286</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-test-5.0.3</td>
      <td>org.axonframework.test.fixture</td>
      <td>fixture</td>
      <td>23</td>
      <td>32</td>
      <td>0.718750</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.commandhandling.an...</td>
      <td>annotation</td>
      <td>8</td>
      <td>11</td>
      <td>0.727273</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.interception....</td>
      <td>annotation</td>
      <td>8</td>
      <td>11</td>
      <td>0.727273</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.queryhandling.dist...</td>
      <td>distributed</td>
      <td>8</td>
      <td>11</td>
      <td>0.727273</td>
    </tr>
    <tr>
      <th>30</th>
      <td>axon-metrics-micrometer-5.0.3</td>
      <td>org.axonframework.extension.metrics.micrometer</td>
      <td>micrometer</td>
      <td>8</td>
      <td>11</td>
      <td>0.727273</td>
    </tr>
    <tr>
      <th>31</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>query</td>
      <td>8</td>
      <td>11</td>
      <td>0.727273</td>
    </tr>
    <tr>
      <th>32</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.timeout</td>
      <td>timeout</td>
      <td>6</td>
      <td>8</td>
      <td>0.750000</td>
    </tr>
    <tr>
      <th>33</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.proc...</td>
      <td>token</td>
      <td>6</td>
      <td>8</td>
      <td>0.750000</td>
    </tr>
    <tr>
      <th>34</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.annotation</td>
      <td>annotation</td>
      <td>3</td>
      <td>4</td>
      <td>0.750000</td>
    </tr>
    <tr>
      <th>35</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.commandhandling.co...</td>
      <td>configuration</td>
      <td>3</td>
      <td>4</td>
      <td>0.750000</td>
    </tr>
    <tr>
      <th>36</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.queryhandling.conf...</td>
      <td>configuration</td>
      <td>3</td>
      <td>4</td>
      <td>0.750000</td>
    </tr>
    <tr>
      <th>37</th>
      <td>axon-metrics-micrometer-5.0.3</td>
      <td>org.axonframework.extension.metrics.micrometer...</td>
      <td>springboot</td>
      <td>3</td>
      <td>4</td>
      <td>0.750000</td>
    </tr>
    <tr>
      <th>38</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>org.axonframework.extension.springboot.service...</td>
      <td>connection</td>
      <td>3</td>
      <td>4</td>
      <td>0.750000</td>
    </tr>
    <tr>
      <th>39</th>
      <td>axon-test-5.0.3</td>
      <td>org.axonframework.test.extension</td>
      <td>extension</td>
      <td>3</td>
      <td>4</td>
      <td>0.750000</td>
    </tr>
  </tbody>
</table>
</div>



### Table 2 Chart 1 - Relative visibility of packages

    /home/runner/miniconda3/envs/codegraph/lib/python3.12/site-packages/pandas/plotting/_matplotlib/core.py:1351: UserWarning: No data for colormapping provided via 'c'. Parameters 'cmap' will be ignored
      scatter = ax.scatter(



    <Figure size 640x480 with 0 Axes>



    
![png](VisibilityMetricsJava_files/VisibilityMetricsJava_23_2.png)
    

