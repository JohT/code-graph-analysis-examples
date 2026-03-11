# Internal Dependencies
<br>  

### References
- [Analyze java package metrics in a graph database](https://joht.github.io/johtizen/data/2023/04/21/java-package-metrics-analysis.html)
- [Calculate metrics](https://101.jqassistant.org/calculate-metrics/index.html)
- [Neo4j Python Driver](https://neo4j.com/docs/api/python-driver/current)





## Artifacts

List the artifacts this notebook is based on. Different sorting variations help finding artifacts by their features and support larger code bases where the list of all artifacts gets too long.

Only the top 30 entries are shown. The whole table can be found in the following CSV report:  
`List_all_Java_artifacts`

### Table 1a - Top 30 artifacts with the highest package count




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>packages</th>
      <th>types</th>
      <th>incomingDependencies</th>
      <th>outgoingDependencies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-messaging-5.0.3.jar</td>
      <td>59</td>
      <td>579</td>
      <td>7</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-common-5.0.3.jar</td>
      <td>15</td>
      <td>156</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-eventsourcing-5.0.3.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-modelling-5.0.3.jar</td>
      <td>7</td>
      <td>92</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-spring-boot-autoconfigure-5.0.3.jar</td>
      <td>7</td>
      <td>75</td>
      <td>1</td>
      <td>7</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-test-5.0.3.jar</td>
      <td>6</td>
      <td>78</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-conversion-5.0.3.jar</td>
      <td>5</td>
      <td>35</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-server-connector-5.0.3.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-update-5.0.3.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.3.jar</td>
      <td>3</td>
      <td>16</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.3.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
</div>



### Table 1b - Top 30 artifacts with the highest type count




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>packages</th>
      <th>types</th>
      <th>incomingDependencies</th>
      <th>outgoingDependencies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-messaging-5.0.3.jar</td>
      <td>59</td>
      <td>579</td>
      <td>7</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-common-5.0.3.jar</td>
      <td>15</td>
      <td>156</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-eventsourcing-5.0.3.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-modelling-5.0.3.jar</td>
      <td>7</td>
      <td>92</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-test-5.0.3.jar</td>
      <td>6</td>
      <td>78</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-spring-boot-autoconfigure-5.0.3.jar</td>
      <td>7</td>
      <td>75</td>
      <td>1</td>
      <td>7</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-server-connector-5.0.3.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-conversion-5.0.3.jar</td>
      <td>5</td>
      <td>35</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-update-5.0.3.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.3.jar</td>
      <td>3</td>
      <td>16</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.3.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
</div>



### Table 1c - Top 30 artifacts with the highest number of incoming dependencies

The following table lists the top 30 artifacts that are used the most by other artifacts (highest count of incoming dependencies, highest in-degree).




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>packages</th>
      <th>types</th>
      <th>incomingDependencies</th>
      <th>outgoingDependencies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-common-5.0.3.jar</td>
      <td>15</td>
      <td>156</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-messaging-5.0.3.jar</td>
      <td>59</td>
      <td>579</td>
      <td>7</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-conversion-5.0.3.jar</td>
      <td>5</td>
      <td>35</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-eventsourcing-5.0.3.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-modelling-5.0.3.jar</td>
      <td>7</td>
      <td>92</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-server-connector-5.0.3.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-spring-boot-autoconfigure-5.0.3.jar</td>
      <td>7</td>
      <td>75</td>
      <td>1</td>
      <td>7</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-test-5.0.3.jar</td>
      <td>6</td>
      <td>78</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-update-5.0.3.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.3.jar</td>
      <td>3</td>
      <td>16</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.3.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
</div>



### Table 1d - Top 30 artifacts with the highest number of outgoing dependencies

The following table lists the top 30 artifacts that are depending on the highest number of other artifacts (highest count of outgoing dependencies, highest out-degree).




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>packages</th>
      <th>types</th>
      <th>incomingDependencies</th>
      <th>outgoingDependencies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-spring-boot-autoconfigure-5.0.3.jar</td>
      <td>7</td>
      <td>75</td>
      <td>1</td>
      <td>7</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-eventsourcing-5.0.3.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-server-connector-5.0.3.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-metrics-micrometer-5.0.3.jar</td>
      <td>3</td>
      <td>16</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-modelling-5.0.3.jar</td>
      <td>7</td>
      <td>92</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-test-5.0.3.jar</td>
      <td>6</td>
      <td>78</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-messaging-5.0.3.jar</td>
      <td>59</td>
      <td>579</td>
      <td>7</td>
      <td>2</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-tracing-opentelemetry-5.0.3.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-conversion-5.0.3.jar</td>
      <td>5</td>
      <td>35</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-update-5.0.3.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-common-5.0.3.jar</td>
      <td>15</td>
      <td>156</td>
      <td>10</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>



### Table 1e - Top 30 artifacts with the lowest package count




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>packages</th>
      <th>types</th>
      <th>incomingDependencies</th>
      <th>outgoingDependencies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-tracing-opentelemetry-5.0.3.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-metrics-micrometer-5.0.3.jar</td>
      <td>3</td>
      <td>16</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-conversion-5.0.3.jar</td>
      <td>5</td>
      <td>35</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-server-connector-5.0.3.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-update-5.0.3.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-test-5.0.3.jar</td>
      <td>6</td>
      <td>78</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-eventsourcing-5.0.3.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-modelling-5.0.3.jar</td>
      <td>7</td>
      <td>92</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-spring-boot-autoconfigure-5.0.3.jar</td>
      <td>7</td>
      <td>75</td>
      <td>1</td>
      <td>7</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-common-5.0.3.jar</td>
      <td>15</td>
      <td>156</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-messaging-5.0.3.jar</td>
      <td>59</td>
      <td>579</td>
      <td>7</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
</div>



### Table 1f - Top 30 artifacts with the lowest type count




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>packages</th>
      <th>types</th>
      <th>incomingDependencies</th>
      <th>outgoingDependencies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-tracing-opentelemetry-5.0.3.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-metrics-micrometer-5.0.3.jar</td>
      <td>3</td>
      <td>16</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-update-5.0.3.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-conversion-5.0.3.jar</td>
      <td>5</td>
      <td>35</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-server-connector-5.0.3.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-spring-boot-autoconfigure-5.0.3.jar</td>
      <td>7</td>
      <td>75</td>
      <td>1</td>
      <td>7</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-test-5.0.3.jar</td>
      <td>6</td>
      <td>78</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-modelling-5.0.3.jar</td>
      <td>7</td>
      <td>92</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-eventsourcing-5.0.3.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-common-5.0.3.jar</td>
      <td>15</td>
      <td>156</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-messaging-5.0.3.jar</td>
      <td>59</td>
      <td>579</td>
      <td>7</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
</div>



### Table 1g - Top 30 artifacts with the lowest number of incoming dependencies

The following table lists the top 30 artifacts that are used the least by other artifacts (lowest count of incoming dependencies, lowest in-degree).




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>packages</th>
      <th>types</th>
      <th>incomingDependencies</th>
      <th>outgoingDependencies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-metrics-micrometer-5.0.3.jar</td>
      <td>3</td>
      <td>16</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-tracing-opentelemetry-5.0.3.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-server-connector-5.0.3.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-spring-boot-autoconfigure-5.0.3.jar</td>
      <td>7</td>
      <td>75</td>
      <td>1</td>
      <td>7</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-test-5.0.3.jar</td>
      <td>6</td>
      <td>78</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-update-5.0.3.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-modelling-5.0.3.jar</td>
      <td>7</td>
      <td>92</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-eventsourcing-5.0.3.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-conversion-5.0.3.jar</td>
      <td>5</td>
      <td>35</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-messaging-5.0.3.jar</td>
      <td>59</td>
      <td>579</td>
      <td>7</td>
      <td>2</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-common-5.0.3.jar</td>
      <td>15</td>
      <td>156</td>
      <td>10</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>



### Table 1h - Top 30 artifacts with the lowest number of outgoing dependencies

The following table lists the top 30 artifacts that are depending on the lowest number of other artifacts (lowest count of outgoing dependencies, lowest out-degree).




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>packages</th>
      <th>types</th>
      <th>incomingDependencies</th>
      <th>outgoingDependencies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-common-5.0.3.jar</td>
      <td>15</td>
      <td>156</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-conversion-5.0.3.jar</td>
      <td>5</td>
      <td>35</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-update-5.0.3.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-messaging-5.0.3.jar</td>
      <td>59</td>
      <td>579</td>
      <td>7</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-tracing-opentelemetry-5.0.3.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-metrics-micrometer-5.0.3.jar</td>
      <td>3</td>
      <td>16</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-modelling-5.0.3.jar</td>
      <td>7</td>
      <td>92</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-test-5.0.3.jar</td>
      <td>6</td>
      <td>78</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-eventsourcing-5.0.3.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-server-connector-5.0.3.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-spring-boot-autoconfigure-5.0.3.jar</td>
      <td>7</td>
      <td>75</td>
      <td>1</td>
      <td>7</td>
    </tr>
  </tbody>
</table>
</div>



## Cyclic Dependencies

Cyclic dependencies occur when one package uses a class of another package and vice versa. 
These dependencies can lead to problems when one of these packages needs to be changed.

## Table 2a - Cyclic Dependencies Overview

Show the top 40 cyclic dependencies sorted by the most promising to resolve first. This is done by calculating the number of forward dependencies (first cycle participant to second cycle participant) in relation to backward dependencies (second cycle participant back to first cycle participant). The higher this rate (approaching 1), the easier it should be to resolve the cycle by focussing on the few backward dependencies.

Only the top 40 entries are shown. The whole table can be found in the following CSV report:  
`Cyclic_Dependencies`

**Columns:**
- *artifactName* identifies the artifact of the first participant of the cycle
- *packageName* identifies the package of the first participant of the cycle
- *dependentArtifactName* identifies the artifact of the second participant of the cycle
- *dependentPackageName* identifies the package of the second participant of the cycle
- *forwardToBackwardBalance* is between 0 and 1. High for many forward and few backward dependencies.
- *numberForward* contains the number of dependencies from the first participant of the cycle to the second one
- *numberBackward* contains the number of dependencies from the second participant of the cycle back to the first one
- *someForwardDependencies* lists some forward dependencies in the text format "type1 -> type2"
- *backwardDependencies* lists the backward dependencies in the format "type1 <- type2" that are recommended to get resolved




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>packageName</th>
      <th>dependentArtifactName</th>
      <th>dependentPackageName</th>
      <th>forwardToBackwardBalance</th>
      <th>numberForward</th>
      <th>numberBackward</th>
      <th>someForwardDependencies</th>
      <th>backwardDependencies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
      <td>[DefaultParameterResolverFactory$AnnotatedMetadataParameterResolver-&gt;Message, DefaultParameterResolverFactory$AnnotatedMetadataParameterResolver-&gt;Metadata, MessageHandler-&gt;Message, MultiHandlerDefinition-&gt;MessageStream, MessageStreamResolverUtils-&gt;MessageStream$Empty, MessageStreamResolverUtils-...</td>
      <td>[SimpleHandlerAttributes-&gt;HandlerAttributes]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>0.942857</td>
      <td>34</td>
      <td>1</td>
      <td>[SimpleEventHandlingComponent-&gt;Message, SimpleEventHandlingComponent-&gt;MessageType, SimpleEventHandlingComponent-&gt;MessageStream, SimpleEventHandlingComponent-&gt;QualifiedName, SimpleEventHandlingComponent-&gt;MessageStream$Empty, TerminalEventMessage-&gt;MessageType, EventMessage-&gt;Message, SimpleEventBus...</td>
      <td>[SubscribableEventSource-&gt;EventMessage]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>0.931034</td>
      <td>28</td>
      <td>1</td>
      <td>[EventAppenderParameterResolverFactoryConfigurationEnhancer-&gt;ParameterResolverFactory, TimestampParameterResolverFactory-&gt;ParameterResolver, TimestampParameterResolverFactory-&gt;AbstractAnnotatedParameterResolverFactory, MethodSequencingPolicyEventHandlerDefinition-&gt;HandlerEnhancerDefinition, Meth...</td>
      <td>[HandlerTypeResolver-&gt;EventHandler]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.commandhandling.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>0.875000</td>
      <td>15</td>
      <td>1</td>
      <td>[CommandDispatcherParameterResolverFactory-&gt;ParameterResolverFactory, CommandDispatcherParameterResolverFactory-&gt;ParameterResolver, CommandDispatcherParameterResolverFactoryConfigurationEnhancer-&gt;ParameterResolverFactory, AnnotatedCommandHandlingComponent-&gt;MessageHandlingMember, AnnotatedCommand...</td>
      <td>[HandlerTypeResolver-&gt;CommandHandler]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.queryhandling.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>0.857143</td>
      <td>13</td>
      <td>1</td>
      <td>[MethodQueryHandlerDefinition$MethodQueryHandlingMember-&gt;WrappedMessageHandlingMember, MethodQueryHandlerDefinition$MethodQueryHandlingMember-&gt;UnsupportedHandlerException, MethodQueryHandlerDefinition$MethodQueryHandlingMember-&gt;MessageHandlingMember, AnnotatedQueryHandlingComponent-&gt;HandlerDefin...</td>
      <td>[HandlerTypeResolver-&gt;QueryHandler]</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.annotation</td>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling</td>
      <td>0.846154</td>
      <td>12</td>
      <td>1</td>
      <td>[AnnotationBasedEntityIdResolver-&gt;EntityIdResolutionException, AnnotationBasedEntityIdResolver-&gt;EntityIdResolver, InjectEntityParameterResolverFactory-&gt;EntityIdResolver, InjectEntityParameterResolverFactory-&gt;PropertyBasedEntityIdResolver, InjectEntityParameterResolver-&gt;EntityIdResolutionExceptio...</td>
      <td>[PropertyBasedEntityIdResolver-&gt;TargetEntityIdMemberMismatchException]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.unitofwork.transaction</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.unitofwork</td>
      <td>0.666667</td>
      <td>5</td>
      <td>1</td>
      <td>[TransactionalExecutorProvider-&gt;ProcessingContext, TransactionManager-&gt;ProcessingContext, TransactionManager-&gt;ProcessingLifecycle$Phase, TransactionManager-&gt;ProcessingLifecycle$ErrorHandler, TransactionManager-&gt;ProcessingLifecycle]</td>
      <td>[TransactionalUnitOfWorkFactory-&gt;TransactionManager]</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.pooled</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
      <td>[PooledStreamingEventProcessorModule-&gt;EventHandlingComponentsConfigurer$CompletePhase, PooledStreamingEventProcessorModule-&gt;EventHandlingComponentsConfigurer$RequiredComponentPhase, PooledStreamingEventProcessorModule-&gt;DefaultEventHandlingComponentsConfigurer, PooledStreamingEventProcessorModule...</td>
      <td>[EventProcessorModule-&gt;PooledStreamingEventProcessorModule, EventProcessorModule-&gt;PooledStreamingEventProcessorConfiguration, EventProcessingConfigurer-&gt;PooledStreamingEventProcessorsConfigurer]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.processing.subscribing</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
      <td>[SubscribingEventProcessorsConfigurer-&gt;EventProcessorModule$EventHandlingPhase, SubscribingEventProcessorsConfigurer-&gt;EventHandlingComponentsConfigurer$RequiredComponentPhase, SubscribingEventProcessorsConfigurer-&gt;EventHandlingComponentsConfigurer$CompletePhase, SubscribingEventProcessorsConfigu...</td>
      <td>[EventProcessorModule-&gt;SubscribingEventProcessorConfiguration, EventProcessorModule-&gt;SubscribingEventProcessorModule, EventProcessingConfigurer-&gt;SubscribingEventProcessorsConfigurer]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.infra</td>
      <td>0.529412</td>
      <td>13</td>
      <td>4</td>
      <td>[Component-&gt;DescribableComponent, DefaultComponentRegistry$LocalConfiguration-&gt;ComponentDescriptor, LazyInitializedComponentDefinition-&gt;ComponentDescriptor, Configuration-&gt;DescribableComponent, DefaultAxonApplication$AxonConfigurationImpl-&gt;ComponentDescriptor, DecoratedComponent-&gt;ComponentDescri...</td>
      <td>[FilesystemStyleComponentDescriptor-&gt;Component$Identifier, FilesystemStyleComponentDescriptor-&gt;Component, JacksonComponentDescriptor-&gt;Component, JacksonComponentDescriptor-&gt;Component$Identifier]</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>0.500000</td>
      <td>15</td>
      <td>5</td>
      <td>[NoMoreInterceptors-&gt;MessageHandlingMember, MessageHandlerInterceptorDefinition$InterceptedMessageHandlingMember-&gt;MessageHandlingMember, MessageHandlerInterceptorDefinition$InterceptedMessageHandlingMember-&gt;WrappedMessageHandlingMember, MessageHandlerInterceptorMemberChain-&gt;MessageHandlingMember...</td>
      <td>[AnnotatedHandlerInspector-&gt;MessageInterceptingMember, AnnotatedHandlerInspector-&gt;MessageHandlerInterceptorMemberChain, AnnotatedHandlerInspector-&gt;NoMoreInterceptors, ChainedMessageHandlerInterceptorMember-&gt;NoMoreInterceptors, ChainedMessageHandlerInterceptorMember-&gt;MessageHandlerInterceptorMemb...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>0.428571</td>
      <td>5</td>
      <td>2</td>
      <td>[EventProcessorControlService-&gt;AxonServerConfiguration$Eventhandling$ProcessorSettings, EventProcessorControlService-&gt;AxonServerConnectionManager, EventProcessorControlService-&gt;AxonServerConfiguration$Eventhandling, AggregateBasedAxonServerEventStorageEngine-&gt;MetadataConverter, AxonServerEventSt...</td>
      <td>[AxonServerConfigurationEnhancer-&gt;EventProcessorControlService, AxonServerConfigurationEnhancer-&gt;AxonServerEventStorageEngineFactory]</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.command</td>
      <td>0.333333</td>
      <td>4</td>
      <td>2</td>
      <td>[ErrorCode-&gt;AxonServerRemoteCommandHandlingException, ErrorCode-&gt;AxonServerNonTransientRemoteCommandHandlingException, ErrorCode-&gt;AxonServerCommandDispatchException, AxonServerConfigurationEnhancer-&gt;AxonServerCommandBusConnector]</td>
      <td>[CommandConverter-&gt;MetadataConverter, AxonServerCommandBusConnector-&gt;AxonServerConfiguration]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.configuration</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>0.333333</td>
      <td>2</td>
      <td>1</td>
      <td>[MessagingConfigurer-&gt;EventBusConfigurationDefaults, MessagingConfigurer-&gt;EventProcessingConfigurer]</td>
      <td>[EventProcessingConfigurer-&gt;MessagingConfigurer]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.sequencing</td>
      <td>0.333333</td>
      <td>4</td>
      <td>2</td>
      <td>[SimpleEventHandlingComponent-&gt;SequentialPolicy, SimpleEventHandlingComponent-&gt;SequentialPerAggregatePolicy, SimpleEventHandlingComponent-&gt;HierarchicalSequencingPolicy, SimpleEventHandlingComponent-&gt;SequencingPolicy]</td>
      <td>[SequentialPerAggregatePolicy-&gt;EventMessage, ExtractionSequencingPolicy-&gt;EventMessage]</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>0.200000</td>
      <td>6</td>
      <td>4</td>
      <td>[QueryConverter-&gt;ErrorCode, QueryConverter-&gt;MetadataConverter, FlowControlledResponseSender-&gt;ErrorCode, AxonServerQueryDispatchException-&gt;ErrorCode, AxonServerQueryBusConnector-&gt;AxonServerConfiguration, AxonServerQueryBusConnector$AxonServerUpdateCallback-&gt;ErrorCode]</td>
      <td>[ErrorCode-&gt;AxonServerNonTransientRemoteQueryHandlingException, ErrorCode-&gt;AxonServerQueryDispatchException, ErrorCode-&gt;AxonServerRemoteQueryHandlingException, AxonServerConfigurationEnhancer-&gt;AxonServerQueryBusConnector]</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity.annotation</td>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.annotation</td>
      <td>0.200000</td>
      <td>3</td>
      <td>2</td>
      <td>[AnnotatedEntityMetamodel-&gt;AnnotationBasedEntityEvolvingComponent, AnnotatedEntityIdResolverDefinition-&gt;AnnotationBasedEntityIdResolver, AnnotatedEntityIdResolverDefinition-&gt;EntityIdResolverDefinition]</td>
      <td>[AnnotationBasedEntityIdResolverDefinition-&gt;AnnotatedEntityMetamodel, EntityIdResolverDefinition-&gt;AnnotatedEntityMetamodel]</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity.child</td>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity</td>
      <td>0.142857</td>
      <td>8</td>
      <td>6</td>
      <td>[SingleEntityChildMetamodel-&gt;EntityMetamodel, AbstractEntityChildMetamodel-&gt;ChildEntityNotFoundException, AbstractEntityChildMetamodel-&gt;EntityMetamodel, ListEntityChildMetamodel-&gt;EntityMetamodel, SingleEntityChildMetamodel$Builder-&gt;EntityMetamodel, EntityChildMetamodel-&gt;EntityMetamodel, Abstract...</td>
      <td>[PolymorphicEntityMetamodel$Builder-&gt;EntityChildMetamodel, EntityMetamodelBuilder-&gt;EntityChildMetamodel, PolymorphicEntityMetamodelBuilder-&gt;EntityChildMetamodel, ConcreteEntityMetamodel-&gt;EntityChildMetamodel, ConcreteEntityMetamodel-&gt;ChildAmbiguityException, ConcreteEntityMetamodel$Builder-&gt;Enti...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.unitofwork</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>0.111111</td>
      <td>10</td>
      <td>8</td>
      <td>[UnitOfWork-&gt;ApplicationContext, LegacyMessageSupportingContext-&gt;Context$ResourceKey, LegacyMessageSupportingContext-&gt;Message, ResourceOverridingProcessingContext-&gt;Context$ResourceKey, ProcessingContext-&gt;Context, ProcessingContext-&gt;ApplicationContext, ProcessingContext-&gt;Context$ResourceKey, Unit...</td>
      <td>[DefaultMessageDispatchInterceptorChain-&gt;ProcessingContext, MessageHandlerInterceptor-&gt;ProcessingContext, DefaultMessageDispatchInterceptorChain$InterceptingDispatcher-&gt;ProcessingContext, MessageDispatchInterceptorChain-&gt;ProcessingContext, Message-&gt;ProcessingContext, MessageDispatchInterceptor-&gt;...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>0.000000</td>
      <td>2</td>
      <td>2</td>
      <td>[ExceptionConverter-&gt;ErrorCode, GrpcExceptionParser-&gt;ErrorCode]</td>
      <td>[AxonServerConnectionManager$Builder-&gt;GrpcMessageSizeInterceptor, ErrorCode-&gt;ExceptionConverter]</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>org.axonframework.eventsourcing.annotation.reflection</td>
      <td>axon-eventsourcing-5.0.3</td>
      <td>org.axonframework.eventsourcing.annotation</td>
      <td>0.000000</td>
      <td>1</td>
      <td>1</td>
      <td>[AnnotationBasedEventSourcedEntityFactoryDefinition-&gt;EventSourcedEntityFactoryDefinition]</td>
      <td>[EventSourcedEntity-&gt;AnnotationBasedEventSourcedEntityFactoryDefinition]</td>
    </tr>
  </tbody>
</table>
</div>



### Table 2b - Cyclic Dependencies Break Down

Lists packages with cyclic dependencies with every dependency in a separate row sorted by the most promising  dependency first.

Only the top 40 entries are shown. The whole table can be found in the following CSV report:  
`Cyclic_Dependencies_Breakdown`

**Columns in addition to Table 2a:**
- *dependency* shows the cycle dependency in the text format "type1 -> type2" (forward) or "type2<-type1" (backward)




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>packageName</th>
      <th>dependentArtifactName</th>
      <th>dependentPackageName</th>
      <th>dependency</th>
      <th>forwardToBackwardBalance</th>
      <th>numberForward</th>
      <th>numberBackward</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>ChainedMessageHandlerInterceptorMember-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MethodInvokingMessageHandlingMember-&gt;MessageStream$Single</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageHandlingMember-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>ChainedMessageHandlerInterceptorMember-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotatedMessageHandlingMemberDefinition-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotatedMessageHandlingMemberDefinition-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotationMessageTypeResolver-&gt;MessageTypeResolver</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>PayloadParameterResolver-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>DefaultParameterResolverFactory-&gt;Metadata</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>DefaultParameterResolverFactory$MessageParameterResolver-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>InterceptorChainParameterResolverFactory-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>AggregateTypeParameterResolverFactory$AggregateTypeParameterResolver-&gt;Context$ResourceKey</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>InterceptorChainParameterResolverFactory-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>InterceptorChainParameterResolverFactory-&gt;Context$ResourceKey</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>WrappedMessageHandlingMember-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotationMessageTypeResolver-&gt;MessageType</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotationMessageTypeResolver-&gt;ClassBasedMessageTypeResolver</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;GenericMessage</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>WrappedMessageHandlingMember-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageHandlingMember-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>HandlerAttributes&lt;-SimpleHandlerAttributes</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>DefaultParameterResolverFactory-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageHandler-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageIdentifierParameterResolverFactory$MessageIdentifierParameterResolver-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;MessageStream$Empty</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>AggregateTypeParameterResolverFactory$AggregateTypeParameterResolver-&gt;LegacyResources</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotatedHandlerInspector-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MultiHandlerDefinition-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotatedHandlerInspector-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>InterceptorChainParameterResolverFactory-&gt;MessageHandlerInterceptorChain</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>30</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;MessageStream$Single</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>31</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>SourceIdParameterResolverFactory$SourceIdParameterResolver-&gt;LegacyResources</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>32</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;MessageTypeResolver</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>33</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>DefaultParameterResolverFactory$AnnotatedMetadataParameterResolver-&gt;Metadata</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>34</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;FluxUtils</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>35</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>SourceIdParameterResolverFactory$SourceIdParameterResolver-&gt;Context$ResourceKey</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>36</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;MonoUtils</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>37</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>38</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>DefaultParameterResolverFactory$AnnotatedMetadataParameterResolver-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>MethodInvokingMessageHandlingMember-&gt;MessageStream$Entry</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>



### Table 2c - Cyclic Dependencies Break Down - Backward Dependencies Only

Lists packages with cyclic dependencies with every dependency in a separate row sorted by the most promising  dependency first. This table only contains the backward dependencies from the second participant of the cycle back to the first one that are the most promising to resolve.

Only the top 40 entries are shown. The whole table can be found in the following CSV report:  
`Cyclic_Dependencies_Breakdown_BackwardOnly`




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>packageName</th>
      <th>dependentArtifactName</th>
      <th>dependentPackageName</th>
      <th>dependency</th>
      <th>forwardToBackwardBalance</th>
      <th>numberForward</th>
      <th>numberBackward</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>HandlerAttributes&lt;-SimpleHandlerAttributes</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>EventMessage&lt;-SubscribableEventSource</td>
      <td>0.942857</td>
      <td>34</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>EventHandler&lt;-HandlerTypeResolver</td>
      <td>0.931034</td>
      <td>28</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.commandhandling.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>CommandHandler&lt;-HandlerTypeResolver</td>
      <td>0.875000</td>
      <td>15</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.queryhandling.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>QueryHandler&lt;-HandlerTypeResolver</td>
      <td>0.857143</td>
      <td>13</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.annotation</td>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling</td>
      <td>TargetEntityIdMemberMismatchException&lt;-PropertyBasedEntityIdResolver</td>
      <td>0.846154</td>
      <td>12</td>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.unitofwork.transaction</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.unitofwork</td>
      <td>TransactionManager&lt;-TransactionalUnitOfWorkFactory</td>
      <td>0.666667</td>
      <td>5</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.pooled</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>PooledStreamingEventProcessorsConfigurer&lt;-EventProcessingConfigurer</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.pooled</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>PooledStreamingEventProcessorConfiguration&lt;-EventProcessorModule</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.pooled</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>PooledStreamingEventProcessorModule&lt;-EventProcessorModule</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.processing.subscribing</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>SubscribingEventProcessorConfiguration&lt;-EventProcessorModule</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.processing.subscribing</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>SubscribingEventProcessorsConfigurer&lt;-EventProcessingConfigurer</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.processing.subscribing</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>SubscribingEventProcessorModule&lt;-EventProcessorModule</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.infra</td>
      <td>Component$Identifier&lt;-JacksonComponentDescriptor</td>
      <td>0.529412</td>
      <td>13</td>
      <td>4</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.infra</td>
      <td>Component&lt;-JacksonComponentDescriptor</td>
      <td>0.529412</td>
      <td>13</td>
      <td>4</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.infra</td>
      <td>Component&lt;-FilesystemStyleComponentDescriptor</td>
      <td>0.529412</td>
      <td>13</td>
      <td>4</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.common.infra</td>
      <td>Component$Identifier&lt;-FilesystemStyleComponentDescriptor</td>
      <td>0.529412</td>
      <td>13</td>
      <td>4</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>NoMoreInterceptors&lt;-ChainedMessageHandlerInterceptorMember</td>
      <td>0.500000</td>
      <td>15</td>
      <td>5</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>NoMoreInterceptors&lt;-AnnotatedHandlerInspector</td>
      <td>0.500000</td>
      <td>15</td>
      <td>5</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>MessageHandlerInterceptorMemberChain&lt;-AnnotatedHandlerInspector</td>
      <td>0.500000</td>
      <td>15</td>
      <td>5</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>MessageInterceptingMember&lt;-AnnotatedHandlerInspector</td>
      <td>0.500000</td>
      <td>15</td>
      <td>5</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>MessageHandlerInterceptorMemberChain&lt;-ChainedMessageHandlerInterceptorMember</td>
      <td>0.500000</td>
      <td>15</td>
      <td>5</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>EventProcessorControlService&lt;-AxonServerConfigurationEnhancer</td>
      <td>0.428571</td>
      <td>5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>AxonServerEventStorageEngineFactory&lt;-AxonServerConfigurationEnhancer</td>
      <td>0.428571</td>
      <td>5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.command</td>
      <td>MetadataConverter&lt;-CommandConverter</td>
      <td>0.333333</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.command</td>
      <td>AxonServerConfiguration&lt;-AxonServerCommandBusConnector</td>
      <td>0.333333</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.configuration</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>MessagingConfigurer&lt;-EventProcessingConfigurer</td>
      <td>0.333333</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.sequencing</td>
      <td>EventMessage&lt;-ExtractionSequencingPolicy</td>
      <td>0.333333</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.messaging.core.sequencing</td>
      <td>EventMessage&lt;-SequentialPerAggregatePolicy</td>
      <td>0.333333</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>AxonServerRemoteQueryHandlingException&lt;-ErrorCode</td>
      <td>0.200000</td>
      <td>6</td>
      <td>4</td>
    </tr>
    <tr>
      <th>30</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>AxonServerQueryDispatchException&lt;-ErrorCode</td>
      <td>0.200000</td>
      <td>6</td>
      <td>4</td>
    </tr>
    <tr>
      <th>31</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>AxonServerNonTransientRemoteQueryHandlingException&lt;-ErrorCode</td>
      <td>0.200000</td>
      <td>6</td>
      <td>4</td>
    </tr>
    <tr>
      <th>32</th>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>axon-server-connector-5.0.3</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>AxonServerQueryBusConnector&lt;-AxonServerConfigurationEnhancer</td>
      <td>0.200000</td>
      <td>6</td>
      <td>4</td>
    </tr>
    <tr>
      <th>33</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity.annotation</td>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.annotation</td>
      <td>AnnotatedEntityMetamodel&lt;-EntityIdResolverDefinition</td>
      <td>0.200000</td>
      <td>3</td>
      <td>2</td>
    </tr>
    <tr>
      <th>34</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity.annotation</td>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.annotation</td>
      <td>AnnotatedEntityMetamodel&lt;-AnnotationBasedEntityIdResolverDefinition</td>
      <td>0.200000</td>
      <td>3</td>
      <td>2</td>
    </tr>
    <tr>
      <th>35</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity.child</td>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity</td>
      <td>EntityChildMetamodel&lt;-PolymorphicEntityMetamodel$Builder</td>
      <td>0.142857</td>
      <td>8</td>
      <td>6</td>
    </tr>
    <tr>
      <th>36</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity.child</td>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity</td>
      <td>EntityChildMetamodel&lt;-EntityMetamodelBuilder</td>
      <td>0.142857</td>
      <td>8</td>
      <td>6</td>
    </tr>
    <tr>
      <th>37</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity.child</td>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity</td>
      <td>EntityChildMetamodel&lt;-PolymorphicEntityMetamodelBuilder</td>
      <td>0.142857</td>
      <td>8</td>
      <td>6</td>
    </tr>
    <tr>
      <th>38</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity.child</td>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity</td>
      <td>EntityChildMetamodel&lt;-ConcreteEntityMetamodel</td>
      <td>0.142857</td>
      <td>8</td>
      <td>6</td>
    </tr>
    <tr>
      <th>39</th>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity.child</td>
      <td>axon-modelling-5.0.3</td>
      <td>org.axonframework.modelling.entity</td>
      <td>ChildAmbiguityException&lt;-ConcreteEntityMetamodel</td>
      <td>0.142857</td>
      <td>8</td>
      <td>6</td>
    </tr>
  </tbody>
</table>
</div>



## Interface Segregation Candidates

Well known from [Design Principles and Design Patterns by Robert C. Martin](http://staff.cs.utu.fi/~jounsmed/doos_06/material/DesignPrinciplesAndPatterns.pdf), the *Interface Segregation Principle* suggests that software components should have narrow, focused interfaces rather than large, general-purpose ones. The goal is to minimize the dependencies between components and increase modularity, flexibility, and maintainability.

Smaller, focused and purpose-driven interfaces

- make it easier to modify individual components without affecting the rest of the system.
- make it clearer which client is affected by which change.
- don’t force their clients to depend on methods they don’t need.
- reduce the scope of changes since a change to one component doesn’t affect others.
- lead to a more loosely coupled architecture that is easier to understand and maintain.

Reference: [Analyze java package metrics in a graph database](https://joht.github.io/johtizen/data/2023/04/21/java-package-metrics-analysis.html#interface-segregation)

### How to apply the results

If just one method of a type is used, especially in many places, then the result of this method can be used to call e.g. a method or constuct an object instead of using the whole object and then just calling that single method.

If there are a couple of methods that are used for a distinct purpose, those could be factored out into a separate interface. The original type can extended/implement the new interface so that there are no breaking changes. Then all the callers, that use only this group of methods, can be changed to the new interface.


### Table 4 - Top 40 most used combinations of methods

The following table shows the top 40 most used combinations of methods of larger types that might benefit from applying the *Interface Segregation Principle*. The whole table can be found in the CSV report `Candidates_for_Interface_Segregation`.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>fullDependentTypeName</th>
      <th>declaredMethods</th>
      <th>calledMethodNames</th>
      <th>calledMethods</th>
      <th>callerTypes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>32</td>
      <td>[computeResourceIfAbsent]</td>
      <td>1</td>
      <td>7</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.messaging.commandhandling.CommandBus</td>
      <td>6</td>
      <td>[dispatch]</td>
      <td>1</td>
      <td>7</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.common.configuration.ComponentDefinition$ComponentCreator</td>
      <td>17</td>
      <td>[createComponent]</td>
      <td>1</td>
      <td>5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.messaging.core.MessageStream$Entry</td>
      <td>7</td>
      <td>[message]</td>
      <td>1</td>
      <td>5</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>32</td>
      <td>[withResource]</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>org.axonframework.messaging.eventhandling.EventMessage</td>
      <td>19</td>
      <td>[identifier, timestamp]</td>
      <td>2</td>
      <td>4</td>
    </tr>
    <tr>
      <th>6</th>
      <td>org.axonframework.messaging.eventhandling.EventMessage</td>
      <td>19</td>
      <td>[timestamp]</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>7</th>
      <td>org.axonframework.messaging.core.MessageStream$Empty</td>
      <td>44</td>
      <td>[cast]</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>8</th>
      <td>org.axonframework.messaging.core.DelayedMessageStream</td>
      <td>42</td>
      <td>[create]</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>9</th>
      <td>org.axonframework.messaging.eventhandling.EventMessage</td>
      <td>19</td>
      <td>[andMetadata]</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>10</th>
      <td>org.axonframework.messaging.core.annotation.WrappedMessageHandlingMember</td>
      <td>13</td>
      <td>[handleSync]</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>11</th>
      <td>org.axonframework.common.configuration.AbstractComponent</td>
      <td>24</td>
      <td>[describeTo]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>12</th>
      <td>org.axonframework.messaging.core.unitofwork.UnitOfWork</td>
      <td>24</td>
      <td>[execute]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>13</th>
      <td>org.axonframework.test.fixture.AxonTestThenMessage</td>
      <td>22</td>
      <td>[exception, exceptionSatisfies]</td>
      <td>3</td>
      <td>2</td>
    </tr>
    <tr>
      <th>14</th>
      <td>org.axonframework.messaging.commandhandling.CommandMessage</td>
      <td>20</td>
      <td>[priority, routingKey]</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>15</th>
      <td>org.axonframework.messaging.commandhandling.CommandMessage</td>
      <td>19</td>
      <td>[withConvertedPayload]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>16</th>
      <td>org.axonframework.messaging.commandhandling.CommandMessage</td>
      <td>19</td>
      <td>[andMetadata]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>17</th>
      <td>org.axonframework.messaging.eventhandling.EventMessage</td>
      <td>19</td>
      <td>[withConvertedPayload]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>18</th>
      <td>org.axonframework.messaging.eventhandling.EventMessage</td>
      <td>19</td>
      <td>[identifier]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>19</th>
      <td>org.axonframework.messaging.eventstreaming.EventCriterion</td>
      <td>12</td>
      <td>[tags]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>20</th>
      <td>org.axonframework.messaging.eventstreaming.OrEventCriteria</td>
      <td>12</td>
      <td>[or]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>21</th>
      <td>org.axonframework.modelling.entity.ConcreteEntityMetamodel</td>
      <td>11</td>
      <td>[forEntityClass]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>22</th>
      <td>org.axonframework.modelling.entity.PolymorphicEntityMetamodel</td>
      <td>11</td>
      <td>[forSuperType]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>23</th>
      <td>org.axonframework.eventsourcing.eventstore.EventStore</td>
      <td>9</td>
      <td>[transaction]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>24</th>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.token.store.ConfigToken</td>
      <td>9</td>
      <td>[get]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>25</th>
      <td>org.axonframework.messaging.core.MessageStream$Entry</td>
      <td>7</td>
      <td>[map]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>26</th>
      <td>org.axonframework.conversion.ChainingContentTypeConverter</td>
      <td>5</td>
      <td>[registerConverter, canConvert]</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>27</th>
      <td>org.axonframework.messaging.core.unitofwork.UnitOfWork$UnitOfWorkProcessingContext</td>
      <td>45</td>
      <td>[on, commit, whenComplete, isCommitted, isCompleted, isStarted, isError, onError]</td>
      <td>8</td>
      <td>1</td>
    </tr>
    <tr>
      <th>28</th>
      <td>org.axonframework.messaging.core.EmptyMessageStream</td>
      <td>44</td>
      <td>[instance]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>29</th>
      <td>org.axonframework.eventsourcing.eventstore.inmemory.InMemoryEventStorageEngine$MapBackedMessageStream</td>
      <td>43</td>
      <td>[hasNextAvailable, isCompleted]</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>30</th>
      <td>org.axonframework.eventsourcing.eventstore.inmemory.InMemoryEventStorageEngine$MapBackedMessageStream</td>
      <td>42</td>
      <td>[callback]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>31</th>
      <td>org.axonframework.messaging.core.DelayedMessageStream</td>
      <td>42</td>
      <td>[createSingle]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>32</th>
      <td>org.axonframework.messaging.core.MessageStream$Single</td>
      <td>42</td>
      <td>[asCompletableFuture]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>33</th>
      <td>org.axonframework.messaging.core.MessageStream$Single</td>
      <td>42</td>
      <td>[cast]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>34</th>
      <td>org.axonframework.messaging.core.MessageStream$Single</td>
      <td>42</td>
      <td>[first]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>35</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>37</td>
      <td>[updateResource, removeResource, putResourceIfAbsent, putResource, computeResourceIfAbsent]</td>
      <td>6</td>
      <td>1</td>
    </tr>
    <tr>
      <th>36</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>36</td>
      <td>[updateResource, computeResourceIfAbsent]</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>37</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>35</td>
      <td>[computeResourceIfAbsent]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>38</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>34</td>
      <td>[computeResourceIfAbsent]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>33</td>
      <td>[putResourceIfAbsent, computeResourceIfAbsent]</td>
      <td>2</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>



## Package Usage

### Table 5 - Types that are used by multiple packages

This table shows the top 40 packages that are used by the highest number of different packages. The whole table can be found in the CSV report `List_types_that_are_used_by_many_different_packages`.





<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>fullQualifiedDependentTypeName</th>
      <th>dependentTypeName</th>
      <th>dependentTypeLabels</th>
      <th>numberOfUsingPackages</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>ProcessingContext</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mar...</td>
      <td>59</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Internal</td>
      <td>[Type, File, Java, ByteCode, Annotation, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent...</td>
      <td>55</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.messaging.core.Message</td>
      <td>Message</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mar...</td>
      <td>47</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.infra.ComponentDescriptor</td>
      <td>ComponentDescriptor</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0...</td>
      <td>46</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.messaging.core.MessageStream</td>
      <td>MessageStream</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWea...</td>
      <td>36</td>
    </tr>
    <tr>
      <th>5</th>
      <td>org.axonframework.messaging.eventhandling.EventMessage</td>
      <td>EventMessage</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponen...</td>
      <td>35</td>
    </tr>
    <tr>
      <th>6</th>
      <td>org.axonframework.messaging.core.MessageType</td>
      <td>MessageType</td>
      <td>[Type, File, Java, ByteCode, Record, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0...</td>
      <td>31</td>
    </tr>
    <tr>
      <th>7</th>
      <td>org.axonframework.messaging.core.QualifiedName</td>
      <td>QualifiedName</td>
      <td>[Type, File, Java, ByteCode, Record, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4T...</td>
      <td>30</td>
    </tr>
    <tr>
      <th>8</th>
      <td>org.axonframework.common.configuration.Configuration</td>
      <td>Configuration</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation14, Mark4TypeLouvainCommunity6...</td>
      <td>29</td>
    </tr>
    <tr>
      <th>9</th>
      <td>org.axonframework.common.FutureUtils</td>
      <td>FutureUtils</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation7, Mark4TypeLouvainCommunity13, Mark...</td>
      <td>28</td>
    </tr>
    <tr>
      <th>10</th>
      <td>org.axonframework.messaging.core.Context$ResourceKey</td>
      <td>Context$ResourceKey</td>
      <td>[Type, File, Java, Class, ByteCode, GenericDeclaration, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyCon...</td>
      <td>25</td>
    </tr>
    <tr>
      <th>11</th>
      <td>org.axonframework.messaging.core.MessageStream$Empty</td>
      <td>MessageStream$Empty</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity8, Mark4TypeLeidenCommunity9, Mark4TypeKC...</td>
      <td>25</td>
    </tr>
    <tr>
      <th>12</th>
      <td>org.axonframework.common.infra.DescribableComponent</td>
      <td>DescribableComponent</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0...</td>
      <td>24</td>
    </tr>
    <tr>
      <th>13</th>
      <td>org.axonframework.common.Assert</td>
      <td>Assert</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation1, Mark4TypeLouvainCommunity1, Mark4TypeLeidenCommunity1, Mark4TypeKCoreDecompositi...</td>
      <td>22</td>
    </tr>
    <tr>
      <th>14</th>
      <td>org.axonframework.common.configuration.ComponentRegistry</td>
      <td>ComponentRegistry</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityBetweenness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation13, Mark4TypeLouvainCommunity6, Mark4TypeLeidenCommunity7, Mark4TypeKCoreDecomposition10, Mark4TypeMaximumKCut17, Mark4TypeHDBSCAN-1]</td>
      <td>22</td>
    </tr>
    <tr>
      <th>15</th>
      <td>org.axonframework.common.BuilderUtils</td>
      <td>BuilderUtils</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation5, Mark4TypeLouvainCommunity3, Mark4TypeLeidenCommunity6, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut16, Mark4TypeHDBSCAN51, Mark4TopAnomalyHub]</td>
      <td>21</td>
    </tr>
    <tr>
      <th>16</th>
      <td>org.axonframework.messaging.commandhandling.CommandMessage</td>
      <td>CommandMessage</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityArticleRank, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation1, Mark4TypeLouvainCommunity9, Mark4TypeLeidenCommunity10,...</td>
      <td>20</td>
    </tr>
    <tr>
      <th>17</th>
      <td>org.axonframework.messaging.core.annotation.ParameterResolverFactory</td>
      <td>ParameterResolverFactory</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation22, Mark4TypeLouvainCommunity14, Mark4TypeLeidenCommunity1, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut10, Mark4TypeHDBSCAN-1]</td>
      <td>20</td>
    </tr>
    <tr>
      <th>18</th>
      <td>org.axonframework.messaging.core.MessageStream$Entry</td>
      <td>MessageStream$Entry</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TopCentralityArticleRank, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity8, Mark4Ty...</td>
      <td>19</td>
    </tr>
    <tr>
      <th>19</th>
      <td>org.axonframework.common.configuration.ConfigurationEnhancer</td>
      <td>ConfigurationEnhancer</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation17, Mark4TypeLouvainCommunity6, Mark4TypeLeidenCommunity7, Mark4TypeKCoreDecomposition8, Mark4TypeMaximumKCut86, Mark4TypeHDBSCAN-1]</td>
      <td>18</td>
    </tr>
    <tr>
      <th>20</th>
      <td>org.axonframework.conversion.Converter</td>
      <td>Converter</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity4, Mark4TypeLeidenCommunity4, Mark4TypeKCoreDecompo...</td>
      <td>18</td>
    </tr>
    <tr>
      <th>21</th>
      <td>org.axonframework.messaging.core.MessageStream$Single</td>
      <td>MessageStream$Single</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark...</td>
      <td>18</td>
    </tr>
    <tr>
      <th>22</th>
      <td>org.axonframework.messaging.core.MessageTypeResolver</td>
      <td>MessageTypeResolver</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity4, Mark4TypeLeidenCommunity4, Mark4TypeKCoreDecomposition10, ...</td>
      <td>18</td>
    </tr>
    <tr>
      <th>23</th>
      <td>org.axonframework.messaging.core.conversion.MessageConverter</td>
      <td>MessageConverter</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity6, Mark4TypeLeidenCommunity7, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut0, Mark4TypeLocalClusteringCoefficient0.11333333333333333, Mark4TypeHDBSCAN-1]</td>
      <td>17</td>
    </tr>
    <tr>
      <th>24</th>
      <td>org.axonframework.messaging.core.Metadata</td>
      <td>Metadata</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityPageRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity4, Mark4TypeLeidenCommunity4, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut66, Ma...</td>
      <td>16</td>
    </tr>
    <tr>
      <th>25</th>
      <td>org.axonframework.common.ObjectUtils</td>
      <td>ObjectUtils</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity4, Mark4TypeLeidenCommunity4, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut44, Mark4TypeHDBSCAN63]</td>
      <td>16</td>
    </tr>
    <tr>
      <th>26</th>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.token.TrackingToken</td>
      <td>TrackingToken</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation39, Mark4TypeLouvainCommunity1...</td>
      <td>15</td>
    </tr>
    <tr>
      <th>27</th>
      <td>org.axonframework.common.AxonConfigurationException</td>
      <td>AxonConfigurationException</td>
      <td>[Type, File, Java, Class, ByteCode, Throwable, Mark4TopCentralityBetweenness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation27, Mark4TypeLouvainCommunity7, Mark4TypeLeidenCommunity1, Mark4TypeKCoreDecomposition8, Mark4TypeMaximumKCut0, Mark4TypeHDBSCAN-1]</td>
      <td>14</td>
    </tr>
    <tr>
      <th>28</th>
      <td>org.axonframework.messaging.commandhandling.CommandBus</td>
      <td>CommandBus</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation1, Mark4TypeLouvainCommunity9, Mark4TypeLeidenCommunity10, Mark4TypeKCoreDecomposition10, Mark4TypeMaximumKCut22, Mark4TypeHDBSCAN-1]</td>
      <td>13</td>
    </tr>
    <tr>
      <th>29</th>
      <td>org.axonframework.common.ReflectionUtils</td>
      <td>ReflectionUtils</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityBetweenness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation19, Mark4TypeLouvainCommunity1, Mark4TypeLeidenCommunity1, Mark4TypeKCoreDecomposition8, Mark4TypeMaximumKCut38, Mark4TypeHDBSCAN53, Mark4TopAnomalyBottleneck, Mark4Top...</td>
      <td>13</td>
    </tr>
    <tr>
      <th>30</th>
      <td>org.axonframework.messaging.commandhandling.CommandResultMessage</td>
      <td>CommandResultMessage</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation1, Mark4TypeLouvainCommunity9, Mark4TypeLeidenCommunity10, Mark4TypeKCoreDecomposition10,...</td>
      <td>12</td>
    </tr>
    <tr>
      <th>31</th>
      <td>org.axonframework.common.configuration.ComponentDefinition</td>
      <td>ComponentDefinition</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation11, Mark4TypeLouvainCommunity6, Mark4TypeLeidenCommunity7, Mark4TypeKCoreDecomposition10, Mark4TypeMaximumKCut1, Mark4TypeHDBSCAN-1]</td>
      <td>12</td>
    </tr>
    <tr>
      <th>32</th>
      <td>org.axonframework.common.configuration.ComponentDefinition$IncompleteComponentDefinition</td>
      <td>ComponentDefinition$IncompleteComponentDefinition</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation11, Mark4TypeLouvainCommunity6, Mark4TypeLeidenCommunity7, Mark4TypeKCoreDecomposition10, Mark4TypeMaximumKCut15, Mark4TypeHDBSCAN17]</td>
      <td>12</td>
    </tr>
    <tr>
      <th>33</th>
      <td>org.axonframework.messaging.core.Context</td>
      <td>Context</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity8, Mark4TypeLeidenCo...</td>
      <td>12</td>
    </tr>
    <tr>
      <th>34</th>
      <td>org.axonframework.messaging.queryhandling.QueryMessage</td>
      <td>QueryMessage</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation9, Mark4TypeLouvainCommunity11, Mark4TypeLeidenCommunity3, Mark4TypeKCoreDecomposition10,...</td>
      <td>12</td>
    </tr>
    <tr>
      <th>35</th>
      <td>org.axonframework.common.AxonNonTransientException</td>
      <td>AxonNonTransientException</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation2, Mark4TypeLouvainCommunity5, Mark4TypeLeidenCommunity5, Mark4TypeKCoreDecomposition4, Mark4TypeMaximumKCut34, Mark4TypeLocalClusteringCoef...</td>
      <td>11</td>
    </tr>
    <tr>
      <th>36</th>
      <td>org.axonframework.common.configuration.ComponentBuilder</td>
      <td>ComponentBuilder</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation13, Mark4TypeLouvainCommunity6, Mark4TypeLeidenCommunity7, Mark4TypeKCoreDecomposition10, Mark4TypeMaximumKCut95, Mark4TypeHDBSCAN81]</td>
      <td>11</td>
    </tr>
    <tr>
      <th>37</th>
      <td>org.axonframework.messaging.eventhandling.conversion.EventConverter</td>
      <td>EventConverter</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity10, Mark4TypeLeidenCommunity7, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut0, Mark4TypeHDBSCAN-1]</td>
      <td>11</td>
    </tr>
    <tr>
      <th>38</th>
      <td>org.axonframework.messaging.core.MessageHandlerInterceptor</td>
      <td>MessageHandlerInterceptor</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation8, Mark4TypeLouvainCommunity6, Mark4TypeLeidenCommunity7, Mark4TypeKC...</td>
      <td>11</td>
    </tr>
    <tr>
      <th>39</th>
      <td>org.axonframework.messaging.core.annotation.ParameterResolver</td>
      <td>ParameterResolver</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity7, Mark4TypeLeidenCommunity1, Mark4TypeKCoreDecomposition7, Mark4TypeMaximumKCut29, Mark4TypeHDBSCAN27]</td>
      <td>11</td>
    </tr>
  </tbody>
</table>
</div>



### Table 6 - Packages that are used by multiple artifacts

This table shows the top 30 artifacts that only use a few (compared to all existing) packages of another artifact.
The whole table can be found in the CSV report `ArtifactPackageUsage`.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>dependentArtifactName</th>
      <th>dependentPackages</th>
      <th>dependentArtifactPackages</th>
      <th>packageUsagePercentage</th>
      <th>dependentFullQualifiedPackageNames</th>
      <th>dependentPackageNames</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-tracing-opentelemetry-5.0.3</td>
      <td>axon-messaging-5.0.3</td>
      <td>2</td>
      <td>59</td>
      <td>0.033898</td>
      <td>[org.axonframework.messaging.core, org.axonframework.messaging.tracing]</td>
      <td>[core, tracing]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-tracing-opentelemetry-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>1</td>
      <td>15</td>
      <td>0.066667</td>
      <td>[org.axonframework.common]</td>
      <td>[common]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-metrics-micrometer-5.0.3</td>
      <td>axon-messaging-5.0.3</td>
      <td>7</td>
      <td>59</td>
      <td>0.118644</td>
      <td>[org.axonframework.messaging.commandhandling, org.axonframework.messaging.core, org.axonframework.messaging.eventhandling, org.axonframework.messaging.queryhandling, org.axonframework.messaging.monitoring, org.axonframework.messaging.eventhandling.processing, org.axonframework.messaging.monitori...</td>
      <td>[commandhandling, core, eventhandling, queryhandling, monitoring, processing, configuration]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-metrics-micrometer-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>2</td>
      <td>15</td>
      <td>0.133333</td>
      <td>[org.axonframework.common.configuration, org.axonframework.common]</td>
      <td>[configuration, common]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-test-5.0.3</td>
      <td>axon-eventsourcing-5.0.3</td>
      <td>1</td>
      <td>7</td>
      <td>0.142857</td>
      <td>[org.axonframework.eventsourcing.eventstore]</td>
      <td>[eventstore]</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-server-connector-5.0.3</td>
      <td>axon-modelling-5.0.3</td>
      <td>1</td>
      <td>7</td>
      <td>0.142857</td>
      <td>[org.axonframework.modelling]</td>
      <td>[modelling]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-server-connector-5.0.3</td>
      <td>axon-eventsourcing-5.0.3</td>
      <td>1</td>
      <td>7</td>
      <td>0.142857</td>
      <td>[org.axonframework.eventsourcing.eventstore]</td>
      <td>[eventstore]</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-metrics-micrometer-5.0.3</td>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>1</td>
      <td>7</td>
      <td>0.142857</td>
      <td>[org.axonframework.extension.springboot.autoconfig]</td>
      <td>[autoconfig]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-test-5.0.3</td>
      <td>axon-messaging-5.0.3</td>
      <td>9</td>
      <td>59</td>
      <td>0.152542</td>
      <td>[org.axonframework.messaging.core.unitofwork, org.axonframework.messaging.core, org.axonframework.messaging.monitoring, org.axonframework.messaging.commandhandling, org.axonframework.messaging.core.annotation, org.axonframework.messaging.eventhandling, org.axonframework.messaging.eventhandling.p...</td>
      <td>[unitofwork, core, monitoring, commandhandling, annotation, eventhandling, token, conversion, eventstreaming]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>axon-test-5.0.3</td>
      <td>1</td>
      <td>6</td>
      <td>0.166667</td>
      <td>[org.axonframework.test.server]</td>
      <td>[server]</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>axon-conversion-5.0.3</td>
      <td>1</td>
      <td>5</td>
      <td>0.200000</td>
      <td>[org.axonframework.conversion]</td>
      <td>[conversion]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-conversion-5.0.3</td>
      <td>axon-conversion-5.0.3</td>
      <td>1</td>
      <td>5</td>
      <td>0.200000</td>
      <td>[org.axonframework.conversion]</td>
      <td>[conversion]</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-modelling-5.0.3</td>
      <td>axon-conversion-5.0.3</td>
      <td>1</td>
      <td>5</td>
      <td>0.200000</td>
      <td>[org.axonframework.conversion]</td>
      <td>[conversion]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-conversion-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>3</td>
      <td>15</td>
      <td>0.200000</td>
      <td>[org.axonframework.common, org.axonframework.common.infra, org.axonframework.common.annotation]</td>
      <td>[common, infra, annotation]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>axon-server-connector-5.0.3</td>
      <td>1</td>
      <td>5</td>
      <td>0.200000</td>
      <td>[org.axonframework.axonserver.connector]</td>
      <td>[connector]</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-update-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>3</td>
      <td>15</td>
      <td>0.200000</td>
      <td>[org.axonframework.common.annotation, org.axonframework.common, org.axonframework.common.configuration]</td>
      <td>[annotation, common, configuration]</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-modelling-5.0.3</td>
      <td>axon-messaging-5.0.3</td>
      <td>13</td>
      <td>59</td>
      <td>0.220339</td>
      <td>[org.axonframework.messaging.queryhandling.configuration, org.axonframework.messaging.core.configuration, org.axonframework.messaging.commandhandling.configuration, org.axonframework.messaging.commandhandling, org.axonframework.messaging.eventhandling, org.axonframework.messaging.core, org.axonf...</td>
      <td>[configuration, commandhandling, eventhandling, core, unitofwork, annotation, conversion, reflection]</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-test-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>4</td>
      <td>15</td>
      <td>0.266667</td>
      <td>[org.axonframework.common, org.axonframework.common.infra, org.axonframework.common.annotation, org.axonframework.common.configuration]</td>
      <td>[common, infra, annotation, configuration]</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-server-connector-5.0.3</td>
      <td>axon-messaging-5.0.3</td>
      <td>16</td>
      <td>59</td>
      <td>0.271186</td>
      <td>[org.axonframework.messaging.core.unitofwork, org.axonframework.messaging.eventhandling.processing.streaming.token, org.axonframework.messaging.eventhandling.processing, org.axonframework.messaging.eventhandling.conversion, org.axonframework.messaging.eventstreaming, org.axonframework.messaging....</td>
      <td>[unitofwork, token, processing, conversion, eventstreaming, streaming, subscribing, store, segmenting, core, eventhandling, distributed, queryhandling, commandhandling]</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>axon-messaging-5.0.3</td>
      <td>16</td>
      <td>59</td>
      <td>0.271186</td>
      <td>[org.axonframework.messaging.core.configuration, org.axonframework.messaging.eventhandling, org.axonframework.messaging.core.interception, org.axonframework.messaging.commandhandling, org.axonframework.messaging.core.annotation, org.axonframework.messaging.eventhandling.conversion, org.axonframe...</td>
      <td>[configuration, eventhandling, interception, commandhandling, annotation, conversion, core, token, eventstreaming, unitofwork, transaction]</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>axon-messaging-5.0.3</td>
      <td>16</td>
      <td>59</td>
      <td>0.271186</td>
      <td>[org.axonframework.messaging.core.annotation, org.axonframework.messaging.commandhandling.distributed, org.axonframework.messaging.core.interception, org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa, org.axonframework.messaging.queryhandling.distributed, org.axonfra...</td>
      <td>[annotation, distributed, interception, jpa, conversion, timeout, store, core, eventhandling, transaction, correlation, queryhandling, commandhandling]</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>axon-eventsourcing-5.0.3</td>
      <td>2</td>
      <td>7</td>
      <td>0.285714</td>
      <td>[org.axonframework.eventsourcing.eventstore.jpa, org.axonframework.eventsourcing.eventstore]</td>
      <td>[jpa, eventstore]</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>5</td>
      <td>15</td>
      <td>0.333333</td>
      <td>[org.axonframework.common, org.axonframework.common.jdbc, org.axonframework.common.jpa, org.axonframework.common.configuration, org.axonframework.common.annotation]</td>
      <td>[common, jdbc, jpa, configuration, annotation]</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-modelling-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>5</td>
      <td>15</td>
      <td>0.333333</td>
      <td>[org.axonframework.common, org.axonframework.common.configuration, org.axonframework.common.infra, org.axonframework.common.annotation, org.axonframework.common.property]</td>
      <td>[common, configuration, infra, annotation, property]</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-server-connector-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>6</td>
      <td>15</td>
      <td>0.400000</td>
      <td>[org.axonframework.common.configuration, org.axonframework.common.infra, org.axonframework.common.annotation, org.axonframework.common, org.axonframework.common.lifecycle, org.axonframework.common.util]</td>
      <td>[configuration, infra, annotation, common, lifecycle, util]</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-conversion-5.0.3</td>
      <td>2</td>
      <td>5</td>
      <td>0.400000</td>
      <td>[org.axonframework.conversion, org.axonframework.conversion.jackson]</td>
      <td>[conversion, jackson]</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>8</td>
      <td>15</td>
      <td>0.533333</td>
      <td>[org.axonframework.common, org.axonframework.common.annotation, org.axonframework.common.configuration, org.axonframework.common.infra, org.axonframework.common.tx, org.axonframework.common.jpa, org.axonframework.common.jdbc, org.axonframework.common.io]</td>
      <td>[common, annotation, configuration, infra, tx, jpa, jdbc, io]</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-common-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>8</td>
      <td>15</td>
      <td>0.533333</td>
      <td>[org.axonframework.common.infra, org.axonframework.common.lifecycle, org.axonframework.common.annotation, org.axonframework.common, org.axonframework.common.configuration, org.axonframework.common.tx, org.axonframework.common.function, org.axonframework.common.io]</td>
      <td>[infra, lifecycle, annotation, common, configuration, tx, function, io]</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>axon-update-5.0.3</td>
      <td>3</td>
      <td>5</td>
      <td>0.600000</td>
      <td>[org.axonframework.update.detection, org.axonframework.update.configuration, org.axonframework.update]</td>
      <td>[detection, configuration, update]</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-metrics-micrometer-5.0.3</td>
      <td>axon-metrics-micrometer-5.0.3</td>
      <td>2</td>
      <td>3</td>
      <td>0.666667</td>
      <td>[org.axonframework.extension.metrics.micrometer, org.axonframework.extension.metrics.micrometer.reservoir]</td>
      <td>[micrometer, reservoir]</td>
    </tr>
  </tbody>
</table>
</div>



### Table 7 - Types that are used by multiple artifacts

This table shows the top 30 types that only use a few (compared to all existing) types of another artifact. The whole table can be found in the CSV report `ClassesPerPackageUsageAcrossArtifacts`.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>dependentArtifactName</th>
      <th>packageName</th>
      <th>dependentPackage.fqn</th>
      <th>dependentTypes</th>
      <th>dependentPackageTypes</th>
      <th>typeUsagePercentage</th>
      <th>dependentTypeNames</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.eventsourcing.configuration</td>
      <td>org.axonframework.messaging.core</td>
      <td>1</td>
      <td>80</td>
      <td>0.012500</td>
      <td>[org.axonframework.messaging.core.MessageTypeResolver]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-test-5.0.3</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.test.matchers</td>
      <td>org.axonframework.messaging.core</td>
      <td>1</td>
      <td>80</td>
      <td>0.012500</td>
      <td>[org.axonframework.messaging.core.Message]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-modelling-5.0.3</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.modelling.repository</td>
      <td>org.axonframework.messaging.core</td>
      <td>1</td>
      <td>80</td>
      <td>0.012500</td>
      <td>[org.axonframework.messaging.core.Context$ResourceKey]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.eventsourcing.configuration</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>1</td>
      <td>51</td>
      <td>0.019608</td>
      <td>[org.axonframework.messaging.core.annotation.ParameterResolverFactory]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.eventsourcing.annotation</td>
      <td>org.axonframework.common.configuration</td>
      <td>1</td>
      <td>46</td>
      <td>0.021739</td>
      <td>[org.axonframework.common.configuration.Configuration]</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.core</td>
      <td>org.axonframework.common.configuration</td>
      <td>1</td>
      <td>46</td>
      <td>0.021739</td>
      <td>[org.axonframework.common.configuration.Configuration]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.core.unitofwork</td>
      <td>org.axonframework.common.configuration</td>
      <td>1</td>
      <td>46</td>
      <td>0.021739</td>
      <td>[org.axonframework.common.configuration.ComponentNotFoundException]</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-modelling-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.modelling.entity.annotation</td>
      <td>org.axonframework.common.configuration</td>
      <td>1</td>
      <td>46</td>
      <td>0.021739</td>
      <td>[org.axonframework.common.configuration.Configuration]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-eventsourcing-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.eventsourcing.annotation.reflection</td>
      <td>org.axonframework.common.configuration</td>
      <td>1</td>
      <td>46</td>
      <td>0.021739</td>
      <td>[org.axonframework.common.configuration.Configuration]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.3</td>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>org.axonframework.extension.metrics.micrometer.springboot</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>1</td>
      <td>41</td>
      <td>0.024390</td>
      <td>[org.axonframework.extension.springboot.autoconfig.AxonAutoConfiguration]</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.3</td>
      <td>axon-messaging-5.0.3</td>
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>org.axonframework.messaging.core</td>
      <td>2</td>
      <td>80</td>
      <td>0.025000</td>
      <td>[org.axonframework.messaging.core.Metadata, org.axonframework.messaging.core.Message]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-spring-boot-autoconfigure-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.AxonConfigurationException]</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-update-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.update</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.ObjectUtils]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.monitoring</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.Assert]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.AxonConfigurationException]</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-conversion-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.conversion.avro</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.core.unitofwork.annotation</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.Priority]</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-test-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.test.util</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.ObjectUtils]</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.queryhandling.tracing</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.core.configuration.reflection</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.Priority]</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.eventstreaming</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.Assert]</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.processing</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.AxonException]</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-test-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.test.extension</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.ReflectionUtils]</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.eventhandling.tracing</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.commandhandling.tracing</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.core.sequencing</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.core.timeout</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.AxonThreadFactory]</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-test-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.test.server</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.Assert]</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-messaging-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.messaging.monitoring.configuration</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.TypeReference]</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-tracing-opentelemetry-5.0.3</td>
      <td>axon-common-5.0.3</td>
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
  </tbody>
</table>
</div>



### Table 8 - Duplicate package names across artifacts

This table shows the top 30 duplicate package names across artifacts. They are ordered by the number of duplicates descending.

This might lead to confusion, makes importing more error prone and might even lead to duplicate classes where only one of them will be loaded by the class loader. If a package is named the same way in two or more artifacts this even allows another artifact to access package protected classes, methods or members which might not be intended. 

The whole table can be found in the CSV report `DuplicatePackageNamesAcrossArtifacts`.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>packageName</th>
      <th>duplicates</th>
      <th>artifactNames</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>



### Table 9 - Annotated elements

This table shows 30 most used Java Annotations including some examples where they are used.





<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>annotationName</th>
      <th>languageElement</th>
      <th>numberOfAnnotatedElements</th>
      <th>examples</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>jakarta.annotation.Nonnull</td>
      <td>Parameter</td>
      <td>3497</td>
      <td>[org.axonframework.conversion.ChainedConverter.calculateChain(0), org.axonframework.conversion.ChainedConverter.calculateChain(1), org.axonframework.conversion.ChainedConverter.calculateChain(2), org.axonframework.conversion.ChainedConverter.canConvert(0), org.axonframework.conversion.ChainedCon...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>jakarta.annotation.Nonnull</td>
      <td>Method</td>
      <td>865</td>
      <td>[org.axonframework.conversion.ContentTypeConverter.expectedSourceType, org.axonframework.conversion.ContentTypeConverter.targetType, org.axonframework.conversion.ChainedConverter.expectedSourceType, org.axonframework.conversion.ChainedConverter.targetType, org.axonframework.conversion.jackson.Js...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>jakarta.annotation.Nullable</td>
      <td>Parameter</td>
      <td>395</td>
      <td>[org.axonframework.conversion.ChainedConverter.convert(0), org.axonframework.conversion.Converter.convert(0), org.axonframework.conversion.jackson.JsonNodeToByteArrayConverter.convert(0), org.axonframework.conversion.jackson.ObjectNodeToJsonNodeConverter.convert(0), org.axonframework.conversion....</td>
    </tr>
    <tr>
      <th>3</th>
      <td>jakarta.annotation.Nullable</td>
      <td>Method</td>
      <td>112</td>
      <td>[org.axonframework.conversion.ChainedConverter.convert, org.axonframework.conversion.ContentTypeConverter.convert, org.axonframework.conversion.Converter.convert, org.axonframework.conversion.jackson.JsonNodeToByteArrayConverter.convert, org.axonframework.conversion.jackson.ObjectNodeToJsonNodeC...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Class</td>
      <td>83</td>
      <td>[org.axonframework.messaging.monitoring.configuration.DefaultMessageMonitorRegistry, org.axonframework.messaging.commandhandling.distributed.DistributedCommandBusConfigurationEnhancer, org.axonframework.messaging.commandhandling.annotation.CommandDispatcherParameterResolverFactory, org.axonframe...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>jakarta.annotation.Nonnull</td>
      <td>Field</td>
      <td>72</td>
      <td>[org.axonframework.conversion.avro.AvroConverterConfiguration.strategies, org.axonframework.conversion.avro.AvroConverterConfiguration.schemaStore, org.axonframework.conversion.avro.AvroConverterConfiguration.schemaIncompatibilityChecker, org.axonframework.conversion.avro.AvroConverterConfigurat...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>java.lang.FunctionalInterface</td>
      <td>Interface</td>
      <td>59</td>
      <td>[org.axonframework.messaging.monitoring.configuration.MessageMonitorFactory, org.axonframework.messaging.commandhandling.distributed.CommandBusConnector$Handler, org.axonframework.messaging.commandhandling.CommandHandler, org.axonframework.messaging.commandhandling.CommandPriorityCalculator, org...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>org.springframework.context.annotation.Bean</td>
      <td>Method</td>
      <td>45</td>
      <td>[org.axonframework.extension.springboot.autoconfig.UpdateCheckerAutoConfiguration.springUpdateCheckerConfigEnhancer, org.axonframework.extension.springboot.autoconfig.JdbcTransactionAutoConfiguration.axonTransactionManager, org.axonframework.extension.springboot.autoconfig.AxonTimeoutAutoConfigu...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>java.lang.annotation.Retention</td>
      <td>Annotation</td>
      <td>42</td>
      <td>[org.axonframework.messaging.commandhandling.annotation.CommandHandler, org.axonframework.messaging.commandhandling.annotation.Command, org.axonframework.messaging.eventhandling.annotation.EventHandler, org.axonframework.messaging.eventhandling.annotation.SequenceNumber, org.axonframework.messag...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>java.lang.annotation.Target</td>
      <td>Annotation</td>
      <td>42</td>
      <td>[org.axonframework.messaging.commandhandling.annotation.CommandHandler, org.axonframework.messaging.commandhandling.annotation.Command, org.axonframework.messaging.eventhandling.annotation.EventHandler, org.axonframework.messaging.eventhandling.annotation.SequenceNumber, org.axonframework.messag...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>org.springframework.boot.autoconfigure.condition.ConditionalOnMissingBean</td>
      <td>Method</td>
      <td>23</td>
      <td>[org.axonframework.extension.springboot.autoconfig.JdbcTransactionAutoConfiguration.axonTransactionManager, org.axonframework.extension.springboot.autoconfig.Jackson2MapperAutoConfiguration.defaultAxonJackson2Mapper, org.axonframework.extension.springboot.autoconfig.JpaAutoConfiguration.entityMa...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>org.springframework.boot.autoconfigure.AutoConfiguration</td>
      <td>Class</td>
      <td>21</td>
      <td>[org.axonframework.extension.springboot.autoconfig.UpdateCheckerAutoConfiguration, org.axonframework.extension.springboot.autoconfig.JdbcTransactionAutoConfiguration, org.axonframework.extension.springboot.autoconfig.AxonTimeoutAutoConfiguration, org.axonframework.extension.springboot.autoconfig...</td>
    </tr>
    <tr>
      <th>12</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Interface</td>
      <td>18</td>
      <td>[org.axonframework.messaging.monitoring.configuration.MessageMonitorRegistry, org.axonframework.messaging.commandhandling.annotation.CommandHandlingMember, org.axonframework.messaging.eventhandling.annotation.EventHandlingMember, org.axonframework.messaging.queryhandling.annotation.QueryHandling...</td>
    </tr>
    <tr>
      <th>13</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Constructor</td>
      <td>17</td>
      <td>[org.axonframework.conversion.jackson.JacksonConverter.&lt;init&gt;, org.axonframework.conversion.jackson2.Jackson2Converter.&lt;init&gt;, org.axonframework.conversion.avro.AvroConverter.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessorConfiguration....</td>
    </tr>
    <tr>
      <th>14</th>
      <td>java.lang.annotation.Documented</td>
      <td>Annotation</td>
      <td>15</td>
      <td>[org.axonframework.messaging.commandhandling.annotation.CommandHandler, org.axonframework.messaging.eventhandling.annotation.EventHandler, org.axonframework.messaging.eventhandling.replay.annotation.AllowReplay, org.axonframework.messaging.eventhandling.replay.annotation.DisallowReplay, org.axon...</td>
    </tr>
    <tr>
      <th>15</th>
      <td>com.fasterxml.jackson.annotation.JsonProperty</td>
      <td>Parameter</td>
      <td>12</td>
      <td>[org.axonframework.messaging.eventhandling.processing.streaming.token.GapAwareTrackingToken.&lt;init&gt;(0), org.axonframework.messaging.eventhandling.processing.streaming.token.GapAwareTrackingToken.&lt;init&gt;(1), org.axonframework.messaging.eventhandling.processing.streaming.token.ReplayToken.&lt;init&gt;(0),...</td>
    </tr>
    <tr>
      <th>16</th>
      <td>org.springframework.boot.autoconfigure.condition.ConditionalOnProperty</td>
      <td>Class</td>
      <td>12</td>
      <td>[org.axonframework.extension.springboot.autoconfig.Jackson2MapperAutoConfiguration$JacksonConfiguredCondition$EventsJacksonCondition, org.axonframework.extension.springboot.autoconfig.Jackson2MapperAutoConfiguration$JacksonConfiguredCondition$GeneralDefaultCondition, org.axonframework.extension....</td>
    </tr>
    <tr>
      <th>17</th>
      <td>org.axonframework.common.Priority</td>
      <td>Class</td>
      <td>12</td>
      <td>[org.axonframework.messaging.eventhandling.annotation.SequenceNumberParameterResolverFactory, org.axonframework.messaging.eventhandling.annotation.TimestampParameterResolverFactory, org.axonframework.messaging.core.annotation.SimpleResourceParameterResolverFactory, org.axonframework.messaging.co...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>org.springframework.boot.context.properties.EnableConfigurationProperties</td>
      <td>Class</td>
      <td>11</td>
      <td>[org.axonframework.extension.springboot.autoconfig.UpdateCheckerAutoConfiguration, org.axonframework.extension.springboot.autoconfig.AxonTimeoutAutoConfiguration, org.axonframework.extension.springboot.autoconfig.Jackson2MapperAutoConfiguration, org.axonframework.extension.springboot.autoconfig....</td>
    </tr>
    <tr>
      <th>19</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Method</td>
      <td>11</td>
      <td>[org.axonframework.messaging.eventhandling.conversion.DelegatingEventConverter.delegate, org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa.JpaTokenStore.converter, org.axonframework.messaging.eventhandling.processing.streaming.token.store.jdbc.JdbcTokenStore.converte...</td>
    </tr>
    <tr>
      <th>20</th>
      <td>org.springframework.boot.context.properties.ConfigurationProperties</td>
      <td>Class</td>
      <td>10</td>
      <td>[org.axonframework.extension.springboot.DistributedCommandBusProperties, org.axonframework.extension.springboot.TokenStoreProperties, org.axonframework.extension.springboot.TagsConfigurationProperties, org.axonframework.extension.springboot.TimeoutProperties, org.axonframework.extension.springbo...</td>
    </tr>
    <tr>
      <th>21</th>
      <td>org.springframework.boot.autoconfigure.condition.ConditionalOnClass</td>
      <td>Class</td>
      <td>9</td>
      <td>[org.axonframework.extension.springboot.autoconfig.Jackson2MapperAutoConfiguration, org.axonframework.extension.springboot.autoconfig.CBORMapperAutoConfiguration, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration, org.axonframework.extension.springboot.autoconfig...</td>
    </tr>
    <tr>
      <th>22</th>
      <td>org.springframework.boot.autoconfigure.condition.ConditionalOnProperty</td>
      <td>Method</td>
      <td>8</td>
      <td>[org.axonframework.extension.springboot.autoconfig.AxonServerAutoConfiguration.disableAxonServerConfigurationEnhancer, org.axonframework.extension.springboot.autoconfig.AxonServerAutoConfiguration.axonServerConfigurationEnhancer, org.axonframework.extension.springboot.autoconfig.AxonServerAutoCo...</td>
    </tr>
    <tr>
      <th>23</th>
      <td>jakarta.persistence.Basic</td>
      <td>Field</td>
      <td>8</td>
      <td>[org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa.TokenEntry.tokenType, org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa.TokenEntry.timestamp, org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa.TokenEntry.own...</td>
    </tr>
    <tr>
      <th>24</th>
      <td>org.springframework.boot.autoconfigure.AutoConfigureBefore</td>
      <td>Class</td>
      <td>8</td>
      <td>[org.axonframework.extension.springboot.autoconfig.CorrelationDataProviderAutoConfiguration, org.axonframework.extension.springboot.autoconfig.Jackson2MapperAutoConfiguration, org.axonframework.extension.springboot.autoconfig.CBORMapperAutoConfiguration, org.axonframework.extension.springboot.au...</td>
    </tr>
    <tr>
      <th>25</th>
      <td>org.springframework.boot.context.properties.NestedConfigurationProperty</td>
      <td>Field</td>
      <td>8</td>
      <td>[org.axonframework.extension.springboot.TimeoutProperties$MessageHandlerTimeoutProperties.events, org.axonframework.extension.springboot.TimeoutProperties$MessageHandlerTimeoutProperties.commands, org.axonframework.extension.springboot.TimeoutProperties$MessageHandlerTimeoutProperties.queries, o...</td>
    </tr>
    <tr>
      <th>26</th>
      <td>java.lang.SafeVarargs</td>
      <td>Constructor</td>
      <td>7</td>
      <td>[org.axonframework.messaging.monitoring.MultiMessageMonitor.&lt;init&gt;, org.axonframework.messaging.core.retry.NonTransientExceptionClassesPredicate.&lt;init&gt;, org.axonframework.test.matchers.SequenceMatcher.&lt;init&gt;, org.axonframework.test.matchers.ListMatcher.&lt;init&gt;, org.axonframework.test.matchers.Exa...</td>
    </tr>
    <tr>
      <th>27</th>
      <td>org.springframework.context.annotation.Conditional</td>
      <td>Method</td>
      <td>7</td>
      <td>[org.axonframework.extension.springboot.autoconfig.UpdateCheckerAutoConfiguration.springUpdateCheckerConfigEnhancer, org.axonframework.extension.springboot.autoconfig.Jackson2MapperAutoConfiguration.defaultAxonJackson2Mapper, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoC...</td>
    </tr>
    <tr>
      <th>28</th>
      <td>java.lang.Deprecated</td>
      <td>Method</td>
      <td>7</td>
      <td>[org.axonframework.messaging.core.GenericResultMessage.asResultMessage, org.axonframework.messaging.core.annotation.MessageHandlingMember.handleSync, org.axonframework.messaging.core.interception.annotation.MessageHandlerInterceptorMemberChain.handleSync, org.axonframework.messaging.core.interce...</td>
    </tr>
    <tr>
      <th>29</th>
      <td>java.beans.ConstructorProperties</td>
      <td>Constructor</td>
      <td>6</td>
      <td>[org.axonframework.messaging.eventhandling.processing.streaming.token.GapAwareTrackingToken.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.token.ReplayToken.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.token.store.ConfigToken.&lt;init&gt;, org.axonfram...</td>
    </tr>
  </tbody>
</table>
</div>



### Table 10 - Distance distribution between dependent files

This table shows the file directory distance distribution between dependent files. Intuitively, the distance is given by the fewest number of change directory commands needed to navigate between a file and a dependency it uses. Those are aggregate to see how many dependent files are in the same directory, how many are just one change directory command apart, and so on.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>dependency.fileDistanceAsFewestChangeDirectoryCommands</th>
      <th>numberOfDependencies</th>
      <th>numberOfDependencyUsers</th>
      <th>numberOfDependencyProviders</th>
      <th>examples</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>2125</td>
      <td>881</td>
      <td>921</td>
      <td>[/axon-eventsourcing-5.0.3.jar uses /axon-conversion-5.0.3.jar, /axon-spring-boot-autoconfigure-5.0.3.jar uses /axon-conversion-5.0.3.jar, /axon-messaging-5.0.3.jar uses /axon-conversion-5.0.3.jar, /axon-modelling-5.0.3.jar uses /axon-conversion-5.0.3.jar]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>100</td>
      <td>86</td>
      <td>41</td>
      <td>[/org/axonframework/conversion/jackson2 uses /org/axonframework/conversion, /org/axonframework/conversion/avro uses /org/axonframework/conversion, /org/axonframework/conversion/jackson uses /org/axonframework/conversion, /org/axonframework/conversion/converter uses /org/axonframework/conversion]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>2138</td>
      <td>631</td>
      <td>420</td>
      <td>[/org/axonframework/conversion/avro/AvroConverter.class uses /org/axonframework/conversion/ChainingContentTypeConverter.class, /org/axonframework/conversion/jackson/JacksonConverter.class uses /org/axonframework/conversion/ChainingContentTypeConverter.class, /org/axonframework/conversion/jackson...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2104</td>
      <td>679</td>
      <td>322</td>
      <td>[/org/axonframework/messaging/eventhandling/conversion uses /org/axonframework/conversion, /org/axonframework/messaging/core/configuration uses /org/axonframework/conversion, /org/axonframework/messaging/commandhandling/gateway uses /org/axonframework/conversion, /org/axonframework/messaging/eve...</td>
    </tr>
  </tbody>
</table>
</div>


