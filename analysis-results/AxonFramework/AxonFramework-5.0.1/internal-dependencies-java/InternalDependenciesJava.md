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
      <td>axon-messaging-5.0.1.jar</td>
      <td>57</td>
      <td>570</td>
      <td>7</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-common-5.0.1.jar</td>
      <td>13</td>
      <td>150</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-eventsourcing-5.0.1.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-modelling-5.0.1.jar</td>
      <td>7</td>
      <td>93</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-spring-boot-autoconfigure-5.0.1.jar</td>
      <td>7</td>
      <td>70</td>
      <td>0</td>
      <td>7</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-server-connector-5.0.1.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-test-5.0.1.jar</td>
      <td>5</td>
      <td>73</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-update-5.0.1.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-conversion-5.0.1.jar</td>
      <td>4</td>
      <td>30</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.1.jar</td>
      <td>2</td>
      <td>13</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.1.jar</td>
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
      <td>axon-messaging-5.0.1.jar</td>
      <td>57</td>
      <td>570</td>
      <td>7</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-common-5.0.1.jar</td>
      <td>13</td>
      <td>150</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-eventsourcing-5.0.1.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-modelling-5.0.1.jar</td>
      <td>7</td>
      <td>93</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-test-5.0.1.jar</td>
      <td>5</td>
      <td>73</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-server-connector-5.0.1.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-spring-boot-autoconfigure-5.0.1.jar</td>
      <td>7</td>
      <td>70</td>
      <td>0</td>
      <td>7</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-conversion-5.0.1.jar</td>
      <td>4</td>
      <td>30</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-update-5.0.1.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.1.jar</td>
      <td>2</td>
      <td>13</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.1.jar</td>
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
      <td>axon-common-5.0.1.jar</td>
      <td>13</td>
      <td>150</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-messaging-5.0.1.jar</td>
      <td>57</td>
      <td>570</td>
      <td>7</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-conversion-5.0.1.jar</td>
      <td>4</td>
      <td>30</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-eventsourcing-5.0.1.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-modelling-5.0.1.jar</td>
      <td>7</td>
      <td>93</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-server-connector-5.0.1.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-test-5.0.1.jar</td>
      <td>5</td>
      <td>73</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-update-5.0.1.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-metrics-micrometer-5.0.1.jar</td>
      <td>2</td>
      <td>13</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-spring-boot-autoconfigure-5.0.1.jar</td>
      <td>7</td>
      <td>70</td>
      <td>0</td>
      <td>7</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.1.jar</td>
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
      <td>axon-spring-boot-autoconfigure-5.0.1.jar</td>
      <td>7</td>
      <td>70</td>
      <td>0</td>
      <td>7</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-eventsourcing-5.0.1.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-server-connector-5.0.1.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-modelling-5.0.1.jar</td>
      <td>7</td>
      <td>93</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-test-5.0.1.jar</td>
      <td>5</td>
      <td>73</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-messaging-5.0.1.jar</td>
      <td>57</td>
      <td>570</td>
      <td>7</td>
      <td>2</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-metrics-micrometer-5.0.1.jar</td>
      <td>2</td>
      <td>13</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-tracing-opentelemetry-5.0.1.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-conversion-5.0.1.jar</td>
      <td>4</td>
      <td>30</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-update-5.0.1.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-common-5.0.1.jar</td>
      <td>13</td>
      <td>150</td>
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
      <td>axon-tracing-opentelemetry-5.0.1.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-metrics-micrometer-5.0.1.jar</td>
      <td>2</td>
      <td>13</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-conversion-5.0.1.jar</td>
      <td>4</td>
      <td>30</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-server-connector-5.0.1.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-test-5.0.1.jar</td>
      <td>5</td>
      <td>73</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-update-5.0.1.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-eventsourcing-5.0.1.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-modelling-5.0.1.jar</td>
      <td>7</td>
      <td>93</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-spring-boot-autoconfigure-5.0.1.jar</td>
      <td>7</td>
      <td>70</td>
      <td>0</td>
      <td>7</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-common-5.0.1.jar</td>
      <td>13</td>
      <td>150</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-messaging-5.0.1.jar</td>
      <td>57</td>
      <td>570</td>
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
      <td>axon-tracing-opentelemetry-5.0.1.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-metrics-micrometer-5.0.1.jar</td>
      <td>2</td>
      <td>13</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-update-5.0.1.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-conversion-5.0.1.jar</td>
      <td>4</td>
      <td>30</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-spring-boot-autoconfigure-5.0.1.jar</td>
      <td>7</td>
      <td>70</td>
      <td>0</td>
      <td>7</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-server-connector-5.0.1.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-test-5.0.1.jar</td>
      <td>5</td>
      <td>73</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-modelling-5.0.1.jar</td>
      <td>7</td>
      <td>93</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-eventsourcing-5.0.1.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-common-5.0.1.jar</td>
      <td>13</td>
      <td>150</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-messaging-5.0.1.jar</td>
      <td>57</td>
      <td>570</td>
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
      <td>axon-metrics-micrometer-5.0.1.jar</td>
      <td>2</td>
      <td>13</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-spring-boot-autoconfigure-5.0.1.jar</td>
      <td>7</td>
      <td>70</td>
      <td>0</td>
      <td>7</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-tracing-opentelemetry-5.0.1.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-server-connector-5.0.1.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-test-5.0.1.jar</td>
      <td>5</td>
      <td>73</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-update-5.0.1.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-modelling-5.0.1.jar</td>
      <td>7</td>
      <td>93</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-eventsourcing-5.0.1.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-conversion-5.0.1.jar</td>
      <td>4</td>
      <td>30</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-messaging-5.0.1.jar</td>
      <td>57</td>
      <td>570</td>
      <td>7</td>
      <td>2</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-common-5.0.1.jar</td>
      <td>13</td>
      <td>150</td>
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
      <td>axon-common-5.0.1.jar</td>
      <td>13</td>
      <td>150</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-conversion-5.0.1.jar</td>
      <td>4</td>
      <td>30</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-update-5.0.1.jar</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-messaging-5.0.1.jar</td>
      <td>57</td>
      <td>570</td>
      <td>7</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-metrics-micrometer-5.0.1.jar</td>
      <td>2</td>
      <td>13</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-tracing-opentelemetry-5.0.1.jar</td>
      <td>1</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-modelling-5.0.1.jar</td>
      <td>7</td>
      <td>93</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-test-5.0.1.jar</td>
      <td>5</td>
      <td>73</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-eventsourcing-5.0.1.jar</td>
      <td>7</td>
      <td>100</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-server-connector-5.0.1.jar</td>
      <td>5</td>
      <td>72</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-spring-boot-autoconfigure-5.0.1.jar</td>
      <td>7</td>
      <td>70</td>
      <td>0</td>
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
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
      <td>[HandlerDefinition-&gt;MessageStream, InterceptorChainParameterResolverFactory-&gt;Context$ResourceKey, InterceptorChainParameterResolverFactory-&gt;Message, InterceptorChainParameterResolverFactory-&gt;MessageHandlerInterceptorChain, InterceptorChainParameterResolverFactory-&gt;MessageStream, AnnotatedHandler...</td>
      <td>[SimpleHandlerAttributes-&gt;HandlerAttributes]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>0.942857</td>
      <td>34</td>
      <td>1</td>
      <td>[InterceptingEventSink-&gt;MessageDispatchInterceptor, InterceptingEventSink-&gt;MessageStream$Single, InterceptingEventSink-&gt;MessageStream, InterceptingEventSink-&gt;Message, InterceptingEventSink-&gt;MessageStream$Empty, EventHandlingComponent-&gt;QualifiedName, TerminalEventMessage-&gt;MessageType, NoHandlerFo...</td>
      <td>[SubscribableEventSource-&gt;EventMessage]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>0.933333</td>
      <td>29</td>
      <td>1</td>
      <td>[SequenceNumberParameterResolverFactory-&gt;ParameterResolver, SequenceNumberParameterResolverFactory-&gt;AbstractAnnotatedParameterResolverFactory, EventAppenderParameterResolverFactory-&gt;ParameterResolver, EventAppenderParameterResolverFactory-&gt;ParameterResolverFactory, EventAppenderParameterResolver...</td>
      <td>[HandlerTypeResolver-&gt;EventHandler]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.commandhandling.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>0.894737</td>
      <td>18</td>
      <td>1</td>
      <td>[CommandDispatcherParameterResolverFactoryConfigurationEnhancer-&gt;ParameterResolverFactory, MethodCommandHandlerDefinition$MethodCommandHandlingMember-&gt;MessageHandlingMember, MethodCommandHandlerDefinition$MethodCommandHandlingMember-&gt;WrappedMessageHandlingMember, CommandHandler-&gt;MessageHandler, ...</td>
      <td>[HandlerTypeResolver-&gt;CommandHandler]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.queryhandling.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>0.875000</td>
      <td>15</td>
      <td>1</td>
      <td>[QueryResponse-&gt;Message, MethodQueryHandlerDefinition$MethodQueryHandlingMember-&gt;WrappedMessageHandlingMember, MethodQueryHandlerDefinition$MethodQueryHandlingMember-&gt;UnsupportedHandlerException, MethodQueryHandlerDefinition$MethodQueryHandlingMember-&gt;MessageHandlingMember, QueryHandlingMember-&gt;...</td>
      <td>[HandlerTypeResolver-&gt;QueryHandler]</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-modelling-5.0.1</td>
      <td>org.axonframework.modelling.annotation</td>
      <td>axon-modelling-5.0.1</td>
      <td>org.axonframework.modelling</td>
      <td>0.846154</td>
      <td>12</td>
      <td>1</td>
      <td>[EntityIdResolverDefinition-&gt;EntityIdResolver, InjectEntityParameterResolverFactory-&gt;EntityIdResolver, InjectEntityParameterResolverFactory-&gt;PropertyBasedEntityIdResolver, InjectEntity-&gt;EntityIdResolver, InjectEntityParameterResolver-&gt;StateManager, InjectEntityParameterResolver-&gt;EntityIdResolver...</td>
      <td>[PropertyBasedEntityIdResolver-&gt;TargetEntityIdMemberMismatchException]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.pooled</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
      <td>[PooledStreamingEventProcessorModule-&gt;EventProcessorModule$CustomizationPhase, PooledStreamingEventProcessorModule-&gt;EventProcessorCustomization, PooledStreamingEventProcessorModule-&gt;EventProcessorConfiguration, PooledStreamingEventProcessorModule-&gt;EventProcessorModule$EventHandlingPhase, PooledS...</td>
      <td>[EventProcessorModule-&gt;PooledStreamingEventProcessorConfiguration, EventProcessorModule-&gt;PooledStreamingEventProcessorModule, EventProcessingConfigurer-&gt;PooledStreamingEventProcessorsConfigurer]</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.processing.subscribing</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
      <td>[SubscribingEventProcessorsConfigurer-&gt;EventProcessorModule$CustomizationPhase, SubscribingEventProcessorsConfigurer-&gt;EventProcessorModule, SubscribingEventProcessorsConfigurer-&gt;EventProcessingConfigurer, SubscribingEventProcessorsConfigurer-&gt;EventHandlingComponentsConfigurer$RequiredComponentPh...</td>
      <td>[EventProcessorModule-&gt;SubscribingEventProcessorConfiguration, EventProcessorModule-&gt;SubscribingEventProcessorModule, EventProcessingConfigurer-&gt;SubscribingEventProcessorsConfigurer]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.infra</td>
      <td>0.529412</td>
      <td>13</td>
      <td>4</td>
      <td>[DefaultAxonApplication$AxonConfigurationImpl-&gt;ComponentDescriptor, DecoratedComponent-&gt;ComponentDescriptor, LazyInitializedComponentDefinition-&gt;ComponentDescriptor, Component-&gt;DescribableComponent, DefaultComponentRegistry$LocalConfiguration-&gt;ComponentDescriptor, Configuration-&gt;DescribableCompo...</td>
      <td>[FilesystemStyleComponentDescriptor-&gt;Component$Identifier, FilesystemStyleComponentDescriptor-&gt;Component, JacksonComponentDescriptor-&gt;Component, JacksonComponentDescriptor-&gt;Component$Identifier]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>0.500000</td>
      <td>15</td>
      <td>5</td>
      <td>[MessageHandlerInterceptor-&gt;MessageHandler, MessageHandlerInterceptorDefinition$InterceptedMessageHandlingMember-&gt;MessageHandlingMember, MessageHandlerInterceptorDefinition$InterceptedMessageHandlingMember-&gt;WrappedMessageHandlingMember, ResultParameterResolverFactory-&gt;ParameterResolverFactory, R...</td>
      <td>[ChainedMessageHandlerInterceptorMember-&gt;MessageHandlerInterceptorMemberChain, ChainedMessageHandlerInterceptorMember-&gt;NoMoreInterceptors, AnnotatedHandlerInspector-&gt;MessageInterceptingMember, AnnotatedHandlerInspector-&gt;MessageHandlerInterceptorMemberChain, AnnotatedHandlerInspector-&gt;NoMoreInter...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.unitofwork.transaction</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.unitofwork</td>
      <td>0.500000</td>
      <td>6</td>
      <td>2</td>
      <td>[TransactionManager-&gt;ProcessingLifecycleHandlerRegistrar, TransactionManager-&gt;ProcessingLifecycle, TransactionManager-&gt;ProcessingLifecycle$Phase, TransactionManager-&gt;ProcessingLifecycle$ErrorHandler, TransactionManager-&gt;ProcessingContext, NoTransactionManager-&gt;ProcessingLifecycle]</td>
      <td>[TransactionalUnitOfWorkFactory-&gt;TransactionManager, TransactionalUnitOfWorkFactory-&gt;Transaction]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>0.428571</td>
      <td>5</td>
      <td>2</td>
      <td>[EventProcessorControlService-&gt;AxonServerConnectionManager, EventProcessorControlService-&gt;AxonServerConfiguration$Eventhandling$ProcessorSettings, EventProcessorControlService-&gt;AxonServerConfiguration$Eventhandling, AggregateBasedAxonServerEventStorageEngine-&gt;MetadataConverter, AxonServerEventSt...</td>
      <td>[AxonServerConfigurationEnhancer-&gt;AxonServerEventStorageEngineFactory, AxonServerConfigurationEnhancer-&gt;EventProcessorControlService]</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.command</td>
      <td>0.333333</td>
      <td>4</td>
      <td>2</td>
      <td>[AxonServerConfigurationEnhancer-&gt;AxonServerCommandBusConnector, ErrorCode-&gt;AxonServerRemoteCommandHandlingException, ErrorCode-&gt;AxonServerCommandDispatchException, ErrorCode-&gt;AxonServerNonTransientRemoteCommandHandlingException]</td>
      <td>[AxonServerCommandBusConnector-&gt;AxonServerConfiguration, CommandConverter-&gt;MetadataConverter]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.configuration</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>0.333333</td>
      <td>2</td>
      <td>1</td>
      <td>[MessagingConfigurer-&gt;EventBusConfigurationDefaults, MessagingConfigurer-&gt;EventProcessingConfigurer]</td>
      <td>[EventProcessingConfigurer-&gt;MessagingConfigurer]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.sequencing</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling</td>
      <td>0.333333</td>
      <td>8</td>
      <td>4</td>
      <td>[SequencingPolicy-&gt;EventMessage, ExtractionSequencingPolicy-&gt;EventMessage, HierarchicalSequencingPolicy-&gt;EventMessage, SequentialPolicy-&gt;EventMessage, FallbackSequencingPolicy-&gt;EventMessage, FullConcurrencyPolicy-&gt;EventMessage, SequentialPerAggregatePolicy-&gt;EventMessage, MetadataSequencingPolicy...</td>
      <td>[SimpleEventHandlingComponent-&gt;SequencingPolicy, SimpleEventHandlingComponent-&gt;SequentialPolicy, SimpleEventHandlingComponent-&gt;HierarchicalSequencingPolicy, SimpleEventHandlingComponent-&gt;SequentialPerAggregatePolicy]</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>0.200000</td>
      <td>6</td>
      <td>4</td>
      <td>[AxonServerQueryDispatchException-&gt;ErrorCode, FlowControlledResponseSender-&gt;ErrorCode, AxonServerQueryBusConnector-&gt;AxonServerConfiguration, QueryConverter-&gt;ErrorCode, QueryConverter-&gt;MetadataConverter, AxonServerQueryBusConnector$AxonServerUpdateCallback-&gt;ErrorCode]</td>
      <td>[AxonServerConfigurationEnhancer-&gt;AxonServerQueryBusConnector, ErrorCode-&gt;AxonServerNonTransientRemoteQueryHandlingException, ErrorCode-&gt;AxonServerQueryDispatchException, ErrorCode-&gt;AxonServerRemoteQueryHandlingException]</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-modelling-5.0.1</td>
      <td>org.axonframework.modelling.entity.annotation</td>
      <td>axon-modelling-5.0.1</td>
      <td>org.axonframework.modelling.annotation</td>
      <td>0.200000</td>
      <td>3</td>
      <td>2</td>
      <td>[AnnotatedEntityIdResolverDefinition-&gt;EntityIdResolverDefinition, AnnotatedEntityIdResolverDefinition-&gt;AnnotationBasedEntityIdResolver, AnnotatedEntityMetamodel-&gt;AnnotationBasedEntityEvolvingComponent]</td>
      <td>[EntityIdResolverDefinition-&gt;AnnotatedEntityMetamodel, AnnotationBasedEntityIdResolverDefinition-&gt;AnnotatedEntityMetamodel]</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.unitofwork</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>0.157895</td>
      <td>11</td>
      <td>8</td>
      <td>[UnitOfWork-&gt;ApplicationContext, ProcessingContext-&gt;ApplicationContext, ProcessingContext-&gt;Context, ProcessingContext-&gt;Context$ResourceKey, UnitOfWork$UnitOfWorkProcessingContext-&gt;Context$ResourceKey, UnitOfWork$UnitOfWorkProcessingContext-&gt;ApplicationContext, TransactionalUnitOfWorkFactory-&gt;Con...</td>
      <td>[DefaultMessageDispatchInterceptorChain-&gt;ProcessingContext, DefaultMessageDispatchInterceptorChain$InterceptingDispatcher-&gt;ProcessingContext, MessageHandlerInterceptor-&gt;ProcessingContext, MessageHandlerInterceptorChain-&gt;ProcessingContext, Message-&gt;ProcessingContext, SubscribableEventSource-&gt;Proc...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-modelling-5.0.1</td>
      <td>org.axonframework.modelling.entity.child</td>
      <td>axon-modelling-5.0.1</td>
      <td>org.axonframework.modelling.entity</td>
      <td>0.142857</td>
      <td>8</td>
      <td>6</td>
      <td>[ListEntityChildMetamodel-&gt;EntityMetamodel, SingleEntityChildMetamodel-&gt;EntityMetamodel, EntityChildMetamodel-&gt;EntityMetamodel, AbstractEntityChildMetamodel$Builder-&gt;EntityMetamodel, AbstractEntityChildMetamodel-&gt;EntityMetamodel, AbstractEntityChildMetamodel-&gt;ChildEntityNotFoundException, ListEn...</td>
      <td>[PolymorphicEntityMetamodel$Builder-&gt;EntityChildMetamodel, ConcreteEntityMetamodel-&gt;ChildAmbiguityException, ConcreteEntityMetamodel-&gt;EntityChildMetamodel, PolymorphicEntityMetamodelBuilder-&gt;EntityChildMetamodel, ConcreteEntityMetamodel$Builder-&gt;EntityChildMetamodel, EntityMetamodelBuilder-&gt;Enti...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>0.000000</td>
      <td>2</td>
      <td>2</td>
      <td>[GrpcExceptionParser-&gt;ErrorCode, ExceptionConverter-&gt;ErrorCode]</td>
      <td>[AxonServerConnectionManager$Builder-&gt;GrpcMessageSizeInterceptor, ErrorCode-&gt;ExceptionConverter]</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>org.axonframework.eventsourcing.annotation.reflection</td>
      <td>axon-eventsourcing-5.0.1</td>
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
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>DefaultParameterResolverFactory$AnnotatedMetadataParameterResolver-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>AggregateTypeParameterResolverFactory$AggregateTypeParameterResolver-&gt;Context$ResourceKey</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MethodInvokingMessageHandlingMember-&gt;MessageStream$Entry</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>DefaultParameterResolverFactory$MessageParameterResolver-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>DefaultParameterResolverFactory$MetadataParameterResolver-&gt;Metadata</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>AggregateTypeParameterResolverFactory$AggregateTypeParameterResolver-&gt;LegacyResources</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MethodInvokingMessageHandlingMember-&gt;MessageStream$Single</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MethodInvokingMessageHandlingMember-&gt;DelayedMessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotatedMessageHandlingMemberDefinition-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>SourceIdParameterResolverFactory$SourceIdParameterResolver-&gt;Context$ResourceKey</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;FluxUtils</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>DefaultParameterResolverFactory$MetadataParameterResolver-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;MessageTypeResolver</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;MonoUtils</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageHandler-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MethodInvokingMessageHandlingMember-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MethodInvokingMessageHandlingMember-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotationMessageTypeResolver-&gt;ClassBasedMessageTypeResolver</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>ChainedMessageHandlerInterceptorMember-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>ChainedMessageHandlerInterceptorMember-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotatedMessageHandlingMemberDefinition-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>SourceIdParameterResolverFactory$SourceIdParameterResolver-&gt;LegacyResources</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>HandlerAttributes&lt;-SimpleHandlerAttributes</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;MessageStream$Single</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>InterceptorChainParameterResolverFactory-&gt;Context$ResourceKey</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>DefaultParameterResolverFactory$AnnotatedMetadataParameterResolver-&gt;Metadata</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;MessageStream$Empty</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>HandlerDefinition-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;GenericMessage</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MessageStreamResolverUtils-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>30</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>InterceptorChainParameterResolverFactory-&gt;MessageHandlerInterceptorChain</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>31</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>DefaultParameterResolverFactory-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>32</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>InterceptorChainParameterResolverFactory-&gt;Message</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>33</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>MethodInvokingMessageHandlingMember-&gt;MessageStream$Empty</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>34</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>InterceptorChainParameterResolverFactory-&gt;MessageStream</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>35</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotationMessageTypeResolver-&gt;MessageTypeResolver</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>36</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotatedHandlerAttributes-&gt;SimpleHandlerAttributes</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>37</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>AnnotationMessageTypeResolver-&gt;MessageType</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>38</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>DefaultParameterResolverFactory-&gt;Metadata</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>PayloadParameterResolver-&gt;Message</td>
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
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>HandlerAttributes&lt;-SimpleHandlerAttributes</td>
      <td>0.959184</td>
      <td>48</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>EventMessage&lt;-SubscribableEventSource</td>
      <td>0.942857</td>
      <td>34</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>EventHandler&lt;-HandlerTypeResolver</td>
      <td>0.933333</td>
      <td>29</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.commandhandling.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>CommandHandler&lt;-HandlerTypeResolver</td>
      <td>0.894737</td>
      <td>18</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.queryhandling.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>QueryHandler&lt;-HandlerTypeResolver</td>
      <td>0.875000</td>
      <td>15</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-modelling-5.0.1</td>
      <td>org.axonframework.modelling.annotation</td>
      <td>axon-modelling-5.0.1</td>
      <td>org.axonframework.modelling</td>
      <td>TargetEntityIdMemberMismatchException&lt;-PropertyBasedEntityIdResolver</td>
      <td>0.846154</td>
      <td>12</td>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.pooled</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>PooledStreamingEventProcessorsConfigurer&lt;-EventProcessingConfigurer</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.pooled</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>PooledStreamingEventProcessorModule&lt;-EventProcessorModule</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.pooled</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>PooledStreamingEventProcessorConfiguration&lt;-EventProcessorModule</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.processing.subscribing</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>SubscribingEventProcessorConfiguration&lt;-EventProcessorModule</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.processing.subscribing</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>SubscribingEventProcessorModule&lt;-EventProcessorModule</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.processing.subscribing</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>SubscribingEventProcessorsConfigurer&lt;-EventProcessingConfigurer</td>
      <td>0.666667</td>
      <td>15</td>
      <td>3</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.infra</td>
      <td>Component$Identifier&lt;-JacksonComponentDescriptor</td>
      <td>0.529412</td>
      <td>13</td>
      <td>4</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.infra</td>
      <td>Component&lt;-JacksonComponentDescriptor</td>
      <td>0.529412</td>
      <td>13</td>
      <td>4</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.infra</td>
      <td>Component&lt;-FilesystemStyleComponentDescriptor</td>
      <td>0.529412</td>
      <td>13</td>
      <td>4</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.configuration</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.infra</td>
      <td>Component$Identifier&lt;-FilesystemStyleComponentDescriptor</td>
      <td>0.529412</td>
      <td>13</td>
      <td>4</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>MessageHandlerInterceptorMemberChain&lt;-AnnotatedHandlerInspector</td>
      <td>0.500000</td>
      <td>15</td>
      <td>5</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>MessageInterceptingMember&lt;-AnnotatedHandlerInspector</td>
      <td>0.500000</td>
      <td>15</td>
      <td>5</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>NoMoreInterceptors&lt;-ChainedMessageHandlerInterceptorMember</td>
      <td>0.500000</td>
      <td>15</td>
      <td>5</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>MessageHandlerInterceptorMemberChain&lt;-ChainedMessageHandlerInterceptorMember</td>
      <td>0.500000</td>
      <td>15</td>
      <td>5</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>NoMoreInterceptors&lt;-AnnotatedHandlerInspector</td>
      <td>0.500000</td>
      <td>15</td>
      <td>5</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.unitofwork.transaction</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.unitofwork</td>
      <td>TransactionManager&lt;-TransactionalUnitOfWorkFactory</td>
      <td>0.500000</td>
      <td>6</td>
      <td>2</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.unitofwork.transaction</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.unitofwork</td>
      <td>Transaction&lt;-TransactionalUnitOfWorkFactory</td>
      <td>0.500000</td>
      <td>6</td>
      <td>2</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>AxonServerEventStorageEngineFactory&lt;-AxonServerConfigurationEnhancer</td>
      <td>0.428571</td>
      <td>5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>EventProcessorControlService&lt;-AxonServerConfigurationEnhancer</td>
      <td>0.428571</td>
      <td>5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.command</td>
      <td>AxonServerConfiguration&lt;-AxonServerCommandBusConnector</td>
      <td>0.333333</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.command</td>
      <td>MetadataConverter&lt;-CommandConverter</td>
      <td>0.333333</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.configuration</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.configuration</td>
      <td>MessagingConfigurer&lt;-EventProcessingConfigurer</td>
      <td>0.333333</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.sequencing</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling</td>
      <td>SequentialPolicy&lt;-SimpleEventHandlingComponent</td>
      <td>0.333333</td>
      <td>8</td>
      <td>4</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.sequencing</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling</td>
      <td>HierarchicalSequencingPolicy&lt;-SimpleEventHandlingComponent</td>
      <td>0.333333</td>
      <td>8</td>
      <td>4</td>
    </tr>
    <tr>
      <th>30</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.sequencing</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling</td>
      <td>SequentialPerAggregatePolicy&lt;-SimpleEventHandlingComponent</td>
      <td>0.333333</td>
      <td>8</td>
      <td>4</td>
    </tr>
    <tr>
      <th>31</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.sequencing</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling</td>
      <td>SequencingPolicy&lt;-SimpleEventHandlingComponent</td>
      <td>0.333333</td>
      <td>8</td>
      <td>4</td>
    </tr>
    <tr>
      <th>32</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>AxonServerQueryDispatchException&lt;-ErrorCode</td>
      <td>0.200000</td>
      <td>6</td>
      <td>4</td>
    </tr>
    <tr>
      <th>33</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>AxonServerNonTransientRemoteQueryHandlingException&lt;-ErrorCode</td>
      <td>0.200000</td>
      <td>6</td>
      <td>4</td>
    </tr>
    <tr>
      <th>34</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>AxonServerQueryBusConnector&lt;-AxonServerConfigurationEnhancer</td>
      <td>0.200000</td>
      <td>6</td>
      <td>4</td>
    </tr>
    <tr>
      <th>35</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>AxonServerRemoteQueryHandlingException&lt;-ErrorCode</td>
      <td>0.200000</td>
      <td>6</td>
      <td>4</td>
    </tr>
    <tr>
      <th>36</th>
      <td>axon-modelling-5.0.1</td>
      <td>org.axonframework.modelling.entity.annotation</td>
      <td>axon-modelling-5.0.1</td>
      <td>org.axonframework.modelling.annotation</td>
      <td>AnnotatedEntityMetamodel&lt;-EntityIdResolverDefinition</td>
      <td>0.200000</td>
      <td>3</td>
      <td>2</td>
    </tr>
    <tr>
      <th>37</th>
      <td>axon-modelling-5.0.1</td>
      <td>org.axonframework.modelling.entity.annotation</td>
      <td>axon-modelling-5.0.1</td>
      <td>org.axonframework.modelling.annotation</td>
      <td>AnnotatedEntityMetamodel&lt;-AnnotationBasedEntityIdResolverDefinition</td>
      <td>0.200000</td>
      <td>3</td>
      <td>2</td>
    </tr>
    <tr>
      <th>38</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.unitofwork</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>ProcessingContext&lt;-MessageDispatchInterceptorChain</td>
      <td>0.157895</td>
      <td>11</td>
      <td>8</td>
    </tr>
    <tr>
      <th>39</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.unitofwork</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>ProcessingContext&lt;-MessageDispatchInterceptor</td>
      <td>0.157895</td>
      <td>11</td>
      <td>8</td>
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
      <td>org.axonframework.messaging.core.unitofwork.UnitOfWork</td>
      <td>24</td>
      <td>[executeWithResult]</td>
      <td>1</td>
      <td>6</td>
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
      <td>org.axonframework.messaging.commandhandling.CommandBus</td>
      <td>6</td>
      <td>[dispatch]</td>
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
      <td>[timestamp]</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>6</th>
      <td>org.axonframework.messaging.eventhandling.EventMessage</td>
      <td>19</td>
      <td>[identifier, timestamp]</td>
      <td>2</td>
      <td>4</td>
    </tr>
    <tr>
      <th>7</th>
      <td>org.axonframework.messaging.core.MessageStream$Entry</td>
      <td>7</td>
      <td>[message]</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>8</th>
      <td>org.axonframework.messaging.core.MessageStream$Empty</td>
      <td>44</td>
      <td>[cast]</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>9</th>
      <td>org.axonframework.messaging.core.DelayedMessageStream</td>
      <td>42</td>
      <td>[create]</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>10</th>
      <td>org.axonframework.messaging.core.unitofwork.UnitOfWork</td>
      <td>24</td>
      <td>[execute]</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>11</th>
      <td>org.axonframework.messaging.eventhandling.EventMessage</td>
      <td>19</td>
      <td>[identifier]</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>12</th>
      <td>org.axonframework.messaging.core.annotation.WrappedMessageHandlingMember</td>
      <td>13</td>
      <td>[handleSync]</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>13</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>32</td>
      <td>[putResource]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>14</th>
      <td>org.axonframework.messaging.core.unitofwork.UnitOfWork</td>
      <td>25</td>
      <td>[executeWithResult]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>15</th>
      <td>org.axonframework.common.configuration.AbstractComponent</td>
      <td>24</td>
      <td>[describeTo]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>16</th>
      <td>org.axonframework.messaging.commandhandling.CommandMessage</td>
      <td>20</td>
      <td>[routingKey, priority]</td>
      <td>2</td>
      <td>2</td>
    </tr>
    <tr>
      <th>17</th>
      <td>org.axonframework.messaging.commandhandling.CommandMessage</td>
      <td>19</td>
      <td>[withConvertedPayload]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>18</th>
      <td>org.axonframework.messaging.commandhandling.CommandMessage</td>
      <td>19</td>
      <td>[andMetadata]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>19</th>
      <td>org.axonframework.messaging.eventhandling.EventMessage</td>
      <td>19</td>
      <td>[andMetadata]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>20</th>
      <td>org.axonframework.messaging.eventhandling.EventMessage</td>
      <td>19</td>
      <td>[withConvertedPayload]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>21</th>
      <td>org.axonframework.messaging.core.annotation.WrappedMessageHandlingMember</td>
      <td>13</td>
      <td>[canHandle]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>22</th>
      <td>org.axonframework.messaging.eventstreaming.EventCriterion</td>
      <td>12</td>
      <td>[tags]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>23</th>
      <td>org.axonframework.messaging.eventstreaming.OrEventCriteria</td>
      <td>12</td>
      <td>[or]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>24</th>
      <td>org.axonframework.modelling.entity.PolymorphicEntityMetamodel</td>
      <td>11</td>
      <td>[forSuperType]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>25</th>
      <td>org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodel</td>
      <td>11</td>
      <td>[entityType]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>26</th>
      <td>org.axonframework.eventsourcing.eventstore.EventStore</td>
      <td>9</td>
      <td>[transaction]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>27</th>
      <td>org.axonframework.messaging.eventhandling.EventHandlingComponent</td>
      <td>8</td>
      <td>[sequenceIdentifierFor, supports, supportedEvents]</td>
      <td>3</td>
      <td>2</td>
    </tr>
    <tr>
      <th>28</th>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.token.WrappedToken</td>
      <td>8</td>
      <td>[unwrapLowerBound]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>29</th>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.token.store.ConfigToken</td>
      <td>8</td>
      <td>[get]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>30</th>
      <td>org.axonframework.messaging.core.MessageStream$Entry</td>
      <td>7</td>
      <td>[map]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>31</th>
      <td>org.axonframework.messaging.core.EmptyMessageStream</td>
      <td>44</td>
      <td>[instance]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>32</th>
      <td>org.axonframework.eventsourcing.eventstore.inmemory.InMemoryEventStorageEngine$MapBackedMessageStream</td>
      <td>43</td>
      <td>[hasNextAvailable, isCompleted]</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>33</th>
      <td>org.axonframework.eventsourcing.eventstore.inmemory.InMemoryEventStorageEngine$MapBackedMessageStream</td>
      <td>42</td>
      <td>[callback]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>34</th>
      <td>org.axonframework.messaging.core.DelayedMessageStream</td>
      <td>42</td>
      <td>[createSingle]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>35</th>
      <td>org.axonframework.messaging.core.MessageStream$Single</td>
      <td>42</td>
      <td>[cast]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>36</th>
      <td>org.axonframework.messaging.core.MessageStream$Single</td>
      <td>42</td>
      <td>[first]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>37</th>
      <td>org.axonframework.messaging.core.MessageStream$Single</td>
      <td>42</td>
      <td>[asCompletableFuture]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>38</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>37</td>
      <td>[removeResource, updateResource, putResourceIfAbsent, putResource, computeResourceIfAbsent]</td>
      <td>6</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>36</td>
      <td>[updateResource, computeResourceIfAbsent]</td>
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
      <td>57</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Internal</td>
      <td>[Type, File, Java, ByteCode, Annotation, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent...</td>
      <td>47</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.axonframework.messaging.core.Message</td>
      <td>Message</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mar...</td>
      <td>46</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.infra.ComponentDescriptor</td>
      <td>ComponentDescriptor</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0...</td>
      <td>39</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.messaging.eventhandling.EventMessage</td>
      <td>EventMessage</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponen...</td>
      <td>35</td>
    </tr>
    <tr>
      <th>5</th>
      <td>org.axonframework.messaging.core.MessageStream</td>
      <td>MessageStream</td>
      <td>[Type, File, Java, ByteCode, Interface, GenericDeclaration, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWea...</td>
      <td>35</td>
    </tr>
    <tr>
      <th>6</th>
      <td>org.axonframework.messaging.core.MessageType</td>
      <td>MessageType</td>
      <td>[Type, File, Java, ByteCode, Record, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, M...</td>
      <td>29</td>
    </tr>
    <tr>
      <th>7</th>
      <td>org.axonframework.messaging.core.QualifiedName</td>
      <td>QualifiedName</td>
      <td>[Type, File, Java, ByteCode, Record, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4T...</td>
      <td>29</td>
    </tr>
    <tr>
      <th>8</th>
      <td>org.axonframework.common.configuration.Configuration</td>
      <td>Configuration</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation19, Mark4TypeLouvainCommunity0...</td>
      <td>28</td>
    </tr>
    <tr>
      <th>9</th>
      <td>org.axonframework.common.FutureUtils</td>
      <td>FutureUtils</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation15, Mark4TypeLouvainCommunity8, Mark...</td>
      <td>26</td>
    </tr>
    <tr>
      <th>10</th>
      <td>org.axonframework.common.infra.DescribableComponent</td>
      <td>DescribableComponent</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0...</td>
      <td>24</td>
    </tr>
    <tr>
      <th>11</th>
      <td>org.axonframework.messaging.core.MessageStream$Empty</td>
      <td>MessageStream$Empty</td>
      <td>[Type, File, Java, ByteCode, Interface, GenericDeclaration, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation25, Mark4TypeLouvainCommunity14, Mark4TypeLeidenCommunity9, Mark4Type...</td>
      <td>24</td>
    </tr>
    <tr>
      <th>12</th>
      <td>org.axonframework.messaging.core.Context$ResourceKey</td>
      <td>Context$ResourceKey</td>
      <td>[Type, File, Java, Class, ByteCode, GenericDeclaration, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyCon...</td>
      <td>23</td>
    </tr>
    <tr>
      <th>13</th>
      <td>org.axonframework.common.BuilderUtils</td>
      <td>BuilderUtils</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation2, Mark4TypeLouvainCommunity2, Mark4TypeLeidenCommunity2, Mark4TypeKCoreDecomposition8, Mark4TypeMaximumKCut59, Mark4TypeHDBSCAN3, Mark4TopAnomalyHub]</td>
      <td>21</td>
    </tr>
    <tr>
      <th>14</th>
      <td>org.axonframework.common.configuration.ComponentRegistry</td>
      <td>ComponentRegistry</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityBetweenness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation17, Mark4TypeLouvainCommunity0, Mark4TypeLeidenCommunity0, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut35, Mark4TypeHDBSCAN49]</td>
      <td>21</td>
    </tr>
    <tr>
      <th>15</th>
      <td>org.axonframework.common.Assert</td>
      <td>Assert</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity13, Mark4TypeLeidenCommunity12, Mark4TypeKCoreDecomposi...</td>
      <td>20</td>
    </tr>
    <tr>
      <th>16</th>
      <td>org.axonframework.messaging.commandhandling.CommandMessage</td>
      <td>CommandMessage</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityArticleRank, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation13, Mark4TypeLouvainCommunity11, Mark4TypeLeidenCommunity1...</td>
      <td>20</td>
    </tr>
    <tr>
      <th>17</th>
      <td>org.axonframework.messaging.core.MessageStream$Entry</td>
      <td>MessageStream$Entry</td>
      <td>[Type, File, Java, ByteCode, Interface, GenericDeclaration, Mark4TopCentralityArticleRank, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation25, Mark4TypeLouvainCommunity14, Mark4...</td>
      <td>19</td>
    </tr>
    <tr>
      <th>18</th>
      <td>org.axonframework.messaging.core.annotation.ParameterResolverFactory</td>
      <td>ParameterResolverFactory</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation46, Mark4TypeLouvainCommunity16, Mark4TypeLeidenCommunity15, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut0, Mark4TypeHDBSCAN130]</td>
      <td>19</td>
    </tr>
    <tr>
      <th>19</th>
      <td>org.axonframework.messaging.core.MessageStream$Single</td>
      <td>MessageStream$Single</td>
      <td>[Type, File, Java, ByteCode, Interface, GenericDeclaration, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation25, Mar...</td>
      <td>18</td>
    </tr>
    <tr>
      <th>20</th>
      <td>org.axonframework.common.configuration.ConfigurationEnhancer</td>
      <td>ConfigurationEnhancer</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation20, Mark4TypeLouvainCommunity0, Mark4TypeLeidenCommunity0, Mark4TypeKCoreDecomposition8, Mark4TypeMaximumKCut0, Mark4TypeHDBSCAN-1]</td>
      <td>17</td>
    </tr>
    <tr>
      <th>21</th>
      <td>org.axonframework.messaging.core.Metadata</td>
      <td>Metadata</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityPageRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity3, Mark4TypeLeidenCommunity3, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut86, Ma...</td>
      <td>16</td>
    </tr>
    <tr>
      <th>22</th>
      <td>org.axonframework.conversion.Converter</td>
      <td>Converter</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity3, Mark4TypeLeidenCommunity3, Mark4TypeKCoreDecompo...</td>
      <td>15</td>
    </tr>
    <tr>
      <th>23</th>
      <td>org.axonframework.messaging.core.conversion.MessageConverter</td>
      <td>MessageConverter</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation16, Mark4TypeLouvainCommunity3, Mark4TypeLeidenCommunity9, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut0, Mark4TypeLocalClusteringCoefficient0.1225296442687747, Mark4TypeHDBSCAN93]</td>
      <td>15</td>
    </tr>
    <tr>
      <th>24</th>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.token.TrackingToken</td>
      <td>TrackingToken</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityArticleRank, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation24, Mark4TypeLouvainCommunity8, Mark4TypeLeidenCommunity7,...</td>
      <td>15</td>
    </tr>
    <tr>
      <th>25</th>
      <td>org.axonframework.common.AxonConfigurationException</td>
      <td>AxonConfigurationException</td>
      <td>[Type, File, Java, Class, ByteCode, Throwable, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation1, Mark4TypeLouvainCommunity1, Mark4TypeLeidenCommunity1, Mark4TypeKCoreDecomposition8, Mark4TypeMaximumKCut0, Mark4TypeHDBSCAN103]</td>
      <td>14</td>
    </tr>
    <tr>
      <th>26</th>
      <td>org.axonframework.messaging.core.MessageTypeResolver</td>
      <td>MessageTypeResolver</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity3, Mark4TypeLeidenCommunity3, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut0, Mark4TypeHDBSCAN130]</td>
      <td>14</td>
    </tr>
    <tr>
      <th>27</th>
      <td>org.axonframework.common.ObjectUtils</td>
      <td>ObjectUtils</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity3, Mark4TypeLeidenCommunity3, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut83, Mark4TypeHDBSCAN21]</td>
      <td>14</td>
    </tr>
    <tr>
      <th>28</th>
      <td>org.axonframework.messaging.commandhandling.CommandBus</td>
      <td>CommandBus</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation25, Mark4TypeLouvainCommunity11, Mark4TypeLeidenCommunity10, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut1, Mark4TypeHDBSCAN-1]</td>
      <td>13</td>
    </tr>
    <tr>
      <th>29</th>
      <td>org.axonframework.messaging.queryhandling.QueryMessage</td>
      <td>QueryMessage</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation12, Mark4TypeLouvainCommunity10, Mark4TypeLeidenCommunity9, Mark4TypeKCoreDecomposition9,...</td>
      <td>13</td>
    </tr>
    <tr>
      <th>30</th>
      <td>org.axonframework.messaging.commandhandling.CommandResultMessage</td>
      <td>CommandResultMessage</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity3, Mark4TypeLeidenCommunity10, Mark4TypeKCoreDecomposition9, ...</td>
      <td>12</td>
    </tr>
    <tr>
      <th>31</th>
      <td>org.axonframework.common.configuration.ComponentDefinition</td>
      <td>ComponentDefinition</td>
      <td>[Type, File, Java, ByteCode, Interface, GenericDeclaration, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation5, Mark4TypeLouvainCommunity0, Mark4TypeLeidenCommunity0, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut94, Mark4TypeLocalClusteringCoefficient0.2028985507246377, Mark4Typ...</td>
      <td>12</td>
    </tr>
    <tr>
      <th>32</th>
      <td>org.axonframework.common.configuration.ComponentDefinition$IncompleteComponentDefinition</td>
      <td>ComponentDefinition$IncompleteComponentDefinition</td>
      <td>[Type, File, Java, ByteCode, Interface, GenericDeclaration, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation5, Mark4TypeLouvainCommunity0, Mark4TypeLeidenCommunity0, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut34, Mark4TypeHDBSCAN7]</td>
      <td>12</td>
    </tr>
    <tr>
      <th>33</th>
      <td>org.axonframework.messaging.core.Context</td>
      <td>Context</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation25, Mark4TypeLouvainCommunity14, Mark4TypeLeiden...</td>
      <td>12</td>
    </tr>
    <tr>
      <th>34</th>
      <td>org.axonframework.common.ReflectionUtils</td>
      <td>ReflectionUtils</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityBetweenness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation47, Mark4TypeLouvainCommunity11, Mark4TypeLeidenCommunity10, Mark4TypeKCoreDecomposition8, Mark4TypeMaximumKCut78, Mark4TypeHDBSCAN-1, Mark4TopAnomalyBottleneck]</td>
      <td>12</td>
    </tr>
    <tr>
      <th>35</th>
      <td>org.axonframework.common.AxonNonTransientException</td>
      <td>AxonNonTransientException</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation9, Mark4TypeLouvainCommunity9, Mark4TypeLeidenCommunity8, Mark4TypeKCoreDecomposition4, Mark4TypeMaximumKCut43, Mark4TypeLocalClusteringCoef...</td>
      <td>11</td>
    </tr>
    <tr>
      <th>36</th>
      <td>org.axonframework.common.configuration.ComponentBuilder</td>
      <td>ComponentBuilder</td>
      <td>[Type, File, Java, ByteCode, Interface, GenericDeclaration, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation17, Mark4TypeLouvainCommunity0, Mark4TypeLeidenCommunity0, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut15, Mark4TypeHDBSCAN57]</td>
      <td>11</td>
    </tr>
    <tr>
      <th>37</th>
      <td>org.axonframework.messaging.core.MessageHandlerInterceptor</td>
      <td>MessageHandlerInterceptor</td>
      <td>[Type, File, Java, ByteCode, Interface, GenericDeclaration, Mark4TopCentralityBetweenness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation52, Mark4TypeLouvainCommunity0, Mark4T...</td>
      <td>11</td>
    </tr>
    <tr>
      <th>38</th>
      <td>org.axonframework.messaging.core.annotation.ParameterResolver</td>
      <td>ParameterResolver</td>
      <td>[Type, File, Java, ByteCode, Interface, GenericDeclaration, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation15, Mark4TypeLouvainCommunity1, Mark4TypeLeidenCommunity1, Mark4TypeKCoreDecomposition7, Mark4TypeMaximumKCut20, Mark4TypeHDBSCAN140]</td>
      <td>11</td>
    </tr>
    <tr>
      <th>39</th>
      <td>org.axonframework.common.TypeReference</td>
      <td>TypeReference</td>
      <td>[Type, File, Java, Class, ByteCode, GenericDeclaration, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity0, M...</td>
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
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>2</td>
      <td>57</td>
      <td>0.035088</td>
      <td>[org.axonframework.messaging.core, org.axonframework.messaging.tracing]</td>
      <td>[core, tracing]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>1</td>
      <td>13</td>
      <td>0.076923</td>
      <td>[org.axonframework.common]</td>
      <td>[common]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>6</td>
      <td>57</td>
      <td>0.105263</td>
      <td>[org.axonframework.messaging.eventhandling, org.axonframework.messaging.core, org.axonframework.messaging.commandhandling, org.axonframework.messaging.monitoring, org.axonframework.messaging.queryhandling, org.axonframework.messaging.eventhandling.processing]</td>
      <td>[eventhandling, core, commandhandling, monitoring, queryhandling, processing]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-test-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>8</td>
      <td>57</td>
      <td>0.140351</td>
      <td>[org.axonframework.messaging.commandhandling, org.axonframework.messaging.core.unitofwork, org.axonframework.messaging.core, org.axonframework.messaging.monitoring, org.axonframework.messaging.eventhandling.processing.streaming.token, org.axonframework.messaging.eventstreaming, org.axonframework...</td>
      <td>[commandhandling, unitofwork, core, monitoring, token, eventstreaming, eventhandling, annotation]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-test-5.0.1</td>
      <td>axon-eventsourcing-5.0.1</td>
      <td>1</td>
      <td>7</td>
      <td>0.142857</td>
      <td>[org.axonframework.eventsourcing.eventstore]</td>
      <td>[eventstore]</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-server-connector-5.0.1</td>
      <td>axon-eventsourcing-5.0.1</td>
      <td>1</td>
      <td>7</td>
      <td>0.142857</td>
      <td>[org.axonframework.eventsourcing.eventstore]</td>
      <td>[eventstore]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-server-connector-5.0.1</td>
      <td>axon-modelling-5.0.1</td>
      <td>1</td>
      <td>7</td>
      <td>0.142857</td>
      <td>[org.axonframework.modelling]</td>
      <td>[modelling]</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>2</td>
      <td>13</td>
      <td>0.153846</td>
      <td>[org.axonframework.common.configuration, org.axonframework.common]</td>
      <td>[configuration, common]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>axon-server-connector-5.0.1</td>
      <td>1</td>
      <td>5</td>
      <td>0.200000</td>
      <td>[org.axonframework.axonserver.connector]</td>
      <td>[connector]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>axon-test-5.0.1</td>
      <td>1</td>
      <td>5</td>
      <td>0.200000</td>
      <td>[org.axonframework.test.server]</td>
      <td>[server]</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-modelling-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>13</td>
      <td>57</td>
      <td>0.228070</td>
      <td>[org.axonframework.messaging.eventhandling, org.axonframework.messaging.commandhandling, org.axonframework.messaging.core, org.axonframework.messaging.core.unitofwork, org.axonframework.messaging.commandhandling.annotation, org.axonframework.messaging.eventhandling.conversion, org.axonframework....</td>
      <td>[eventhandling, commandhandling, core, unitofwork, annotation, conversion, reflection, configuration]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-update-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>3</td>
      <td>13</td>
      <td>0.230769</td>
      <td>[org.axonframework.common.annotation, org.axonframework.common, org.axonframework.common.configuration]</td>
      <td>[annotation, common, configuration]</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-conversion-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>3</td>
      <td>13</td>
      <td>0.230769</td>
      <td>[org.axonframework.common.infra, org.axonframework.common.annotation, org.axonframework.common]</td>
      <td>[infra, annotation, common]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-conversion-5.0.1</td>
      <td>axon-conversion-5.0.1</td>
      <td>1</td>
      <td>4</td>
      <td>0.250000</td>
      <td>[org.axonframework.conversion]</td>
      <td>[conversion]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-modelling-5.0.1</td>
      <td>axon-conversion-5.0.1</td>
      <td>1</td>
      <td>4</td>
      <td>0.250000</td>
      <td>[org.axonframework.conversion]</td>
      <td>[conversion]</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>axon-conversion-5.0.1</td>
      <td>1</td>
      <td>4</td>
      <td>0.250000</td>
      <td>[org.axonframework.conversion]</td>
      <td>[conversion]</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>15</td>
      <td>57</td>
      <td>0.263158</td>
      <td>[org.axonframework.messaging.core.timeout, org.axonframework.messaging.core.correlation, org.axonframework.messaging.core.unitofwork.transaction, org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa, org.axonframework.messaging.commandhandling, org.axonframework.messagi...</td>
      <td>[timeout, correlation, transaction, jpa, commandhandling, annotation, conversion, distributed, core, interception, store, eventhandling, queryhandling]</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-server-connector-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>16</td>
      <td>57</td>
      <td>0.280702</td>
      <td>[org.axonframework.messaging.queryhandling.distributed, org.axonframework.messaging.queryhandling, org.axonframework.messaging.core, org.axonframework.messaging.core.unitofwork, org.axonframework.messaging.eventstreaming, org.axonframework.messaging.eventhandling.processing.streaming, org.axonfr...</td>
      <td>[distributed, queryhandling, core, unitofwork, eventstreaming, streaming, segmenting, processing, subscribing, store, token, conversion, eventhandling, commandhandling]</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>16</td>
      <td>57</td>
      <td>0.280702</td>
      <td>[org.axonframework.messaging.core.unitofwork, org.axonframework.messaging.core, org.axonframework.messaging.eventstreaming, org.axonframework.messaging.eventhandling.processing.streaming.token, org.axonframework.messaging.eventhandling, org.axonframework.messaging.eventhandling.conversion, org.a...</td>
      <td>[unitofwork, core, eventstreaming, token, eventhandling, conversion, transaction, annotation, configuration, interception, commandhandling]</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>axon-eventsourcing-5.0.1</td>
      <td>2</td>
      <td>7</td>
      <td>0.285714</td>
      <td>[org.axonframework.eventsourcing.eventstore, org.axonframework.eventsourcing.eventstore.jpa]</td>
      <td>[eventstore, jpa]</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-test-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>4</td>
      <td>13</td>
      <td>0.307692</td>
      <td>[org.axonframework.common, org.axonframework.common.infra, org.axonframework.common.annotation, org.axonframework.common.configuration]</td>
      <td>[common, infra, annotation, configuration]</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>4</td>
      <td>13</td>
      <td>0.307692</td>
      <td>[org.axonframework.common.jpa, org.axonframework.common, org.axonframework.common.jdbc, org.axonframework.common.configuration]</td>
      <td>[jpa, common, jdbc, configuration]</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-modelling-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>5</td>
      <td>13</td>
      <td>0.384615</td>
      <td>[org.axonframework.common.infra, org.axonframework.common, org.axonframework.common.configuration, org.axonframework.common.annotation, org.axonframework.common.property]</td>
      <td>[infra, common, configuration, annotation, property]</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-common-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>6</td>
      <td>13</td>
      <td>0.461538</td>
      <td>[org.axonframework.common, org.axonframework.common.annotation, org.axonframework.common.infra, org.axonframework.common.lifecycle, org.axonframework.common.io, org.axonframework.common.configuration]</td>
      <td>[common, annotation, infra, lifecycle, io, configuration]</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-server-connector-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>6</td>
      <td>13</td>
      <td>0.461538</td>
      <td>[org.axonframework.common, org.axonframework.common.util, org.axonframework.common.annotation, org.axonframework.common.lifecycle, org.axonframework.common.infra, org.axonframework.common.configuration]</td>
      <td>[common, util, annotation, lifecycle, infra, configuration]</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-conversion-5.0.1</td>
      <td>2</td>
      <td>4</td>
      <td>0.500000</td>
      <td>[org.axonframework.conversion.json, org.axonframework.conversion]</td>
      <td>[json, conversion]</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>1</td>
      <td>2</td>
      <td>0.500000</td>
      <td>[org.axonframework.extension.metrics.micrometer.reservoir]</td>
      <td>[reservoir]</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>7</td>
      <td>13</td>
      <td>0.538462</td>
      <td>[org.axonframework.common.annotation, org.axonframework.common, org.axonframework.common.infra, org.axonframework.common.jdbc, org.axonframework.common.io, org.axonframework.common.jpa, org.axonframework.common.configuration]</td>
      <td>[annotation, common, infra, jdbc, io, jpa, configuration]</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>axon-update-5.0.1</td>
      <td>3</td>
      <td>5</td>
      <td>0.600000</td>
      <td>[org.axonframework.update.configuration, org.axonframework.update.detection, org.axonframework.update]</td>
      <td>[configuration, detection, update]</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-test-5.0.1</td>
      <td>axon-test-5.0.1</td>
      <td>3</td>
      <td>5</td>
      <td>0.600000</td>
      <td>[org.axonframework.test.util, org.axonframework.test.matchers, org.axonframework.test]</td>
      <td>[util, matchers, test]</td>
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
      <td>axon-test-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.test.matchers</td>
      <td>org.axonframework.messaging.core</td>
      <td>1</td>
      <td>80</td>
      <td>0.012500</td>
      <td>[org.axonframework.messaging.core.Message]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-modelling-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.modelling.repository</td>
      <td>org.axonframework.messaging.core</td>
      <td>1</td>
      <td>80</td>
      <td>0.012500</td>
      <td>[org.axonframework.messaging.core.Context$ResourceKey]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.eventsourcing.configuration</td>
      <td>org.axonframework.messaging.core</td>
      <td>1</td>
      <td>80</td>
      <td>0.012500</td>
      <td>[org.axonframework.messaging.core.MessageTypeResolver]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.eventsourcing.configuration</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>1</td>
      <td>50</td>
      <td>0.020000</td>
      <td>[org.axonframework.messaging.core.annotation.ParameterResolverFactory]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>1</td>
      <td>50</td>
      <td>0.020000</td>
      <td>[org.axonframework.messaging.core.annotation.HandlerEnhancerDefinition]</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-modelling-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.modelling.entity.annotation</td>
      <td>org.axonframework.common.configuration</td>
      <td>1</td>
      <td>46</td>
      <td>0.021739</td>
      <td>[org.axonframework.common.configuration.Configuration]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.eventsourcing.annotation</td>
      <td>org.axonframework.common.configuration</td>
      <td>1</td>
      <td>46</td>
      <td>0.021739</td>
      <td>[org.axonframework.common.configuration.Configuration]</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.core.unitofwork</td>
      <td>org.axonframework.common.configuration</td>
      <td>1</td>
      <td>46</td>
      <td>0.021739</td>
      <td>[org.axonframework.common.configuration.ComponentNotFoundException]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.eventsourcing.annotation.reflection</td>
      <td>org.axonframework.common.configuration</td>
      <td>1</td>
      <td>46</td>
      <td>0.021739</td>
      <td>[org.axonframework.common.configuration.Configuration]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>org.axonframework.common.configuration</td>
      <td>1</td>
      <td>46</td>
      <td>0.021739</td>
      <td>[org.axonframework.common.configuration.Configuration]</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.extension.metrics.micrometer</td>
      <td>org.axonframework.messaging.core</td>
      <td>2</td>
      <td>80</td>
      <td>0.025000</td>
      <td>[org.axonframework.messaging.core.Metadata, org.axonframework.messaging.core.Message]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>org.axonframework.messaging.core</td>
      <td>2</td>
      <td>80</td>
      <td>0.025000</td>
      <td>[org.axonframework.messaging.core.Metadata, org.axonframework.messaging.core.Message]</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.sequencing</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-conversion-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.conversion.avro</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-test-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.test.server</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.Assert]</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.segmenting</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.Assert]</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.core.configuration.reflection</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.Priority]</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-test-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.test.fixture</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.Registration]</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.token.store</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.AxonTransientException]</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.commandhandling.retry</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.FutureUtils]</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.processing</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.AxonException]</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-test-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.test.util</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.ObjectUtils]</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.queryhandling.configuration</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.FutureUtils]</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.tracing</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.commandhandling.tracing</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.commandhandling.configuration</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.FutureUtils]</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.queryhandling.tracing</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.extension.metrics.micrometer</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.BuilderUtils]</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-modelling-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.modelling.repository</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.FutureUtils]</td>
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
      <td>3382</td>
      <td>[org.axonframework.axonserver.connector.MetadataConverter.convertGrpcToMetadataValues(0), org.axonframework.axonserver.connector.MetadataConverter.convertMetadataValuesToGrpc(0), org.axonframework.axonserver.connector.util.PriorityExecutorService.awaitTermination(1), org.axonframework.axonserver...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>jakarta.annotation.Nonnull</td>
      <td>Method</td>
      <td>833</td>
      <td>[org.axonframework.axonserver.connector.MetadataConverter.convertGrpcToMetadataValues, org.axonframework.axonserver.connector.MetadataConverter.convertMetadataValuesToGrpc, org.axonframework.axonserver.connector.util.PriorityExecutorService.shutdownNow, org.axonframework.axonserver.connector.uti...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>jakarta.annotation.Nullable</td>
      <td>Parameter</td>
      <td>399</td>
      <td>[org.axonframework.axonserver.connector.util.ExceptionConverter.convertToErrorMessage(1), org.axonframework.axonserver.connector.query.AxonServerQueryBusConnector.query(1), org.axonframework.axonserver.connector.query.AxonServerQueryBusConnector.subscriptionQuery(1), org.axonframework.axonserver...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>jakarta.annotation.Nullable</td>
      <td>Method</td>
      <td>99</td>
      <td>[org.axonframework.test.fixture.RecordingCommandBus.resultOf, org.axonframework.modelling.annotation.InjectEntityParameterResolverFactory.createInstance, org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodel.getExpectedRepresentation, org.axonframework.modelling.entity.child.Com...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Class</td>
      <td>75</td>
      <td>[org.axonframework.axonserver.connector.MetadataConverter, org.axonframework.axonserver.connector.query.AbstractQueryResponseMessageStream, org.axonframework.axonserver.connector.query.QueryConverter, org.axonframework.axonserver.connector.query.QueryResponseMessageStream, org.axonframework.axon...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>jakarta.annotation.Nonnull</td>
      <td>Field</td>
      <td>70</td>
      <td>[org.axonframework.axonserver.connector.command.AxonServerCommandBusConnector$FutureResultCallback.result, org.axonframework.axonserver.connector.command.AxonServerCommandBusConnector$FutureResultCallback.command, org.axonframework.test.fixture.AxonTestFixture$Customization.fieldFilters, org.axo...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>java.lang.FunctionalInterface</td>
      <td>Interface</td>
      <td>55</td>
      <td>[org.axonframework.axonserver.connector.ErrorCode$ExceptionBuilder, org.axonframework.axonserver.connector.ManagedChannelCustomizer, org.axonframework.axonserver.connector.InstructionAckSource, org.axonframework.axonserver.connector.TargetContextResolver, org.axonframework.axonserver.connector.T...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>java.lang.annotation.Retention</td>
      <td>Annotation</td>
      <td>42</td>
      <td>[org.axonframework.extension.springboot.util.RegisterDefaultEntities, org.axonframework.extension.springboot.util.ConditionalOnQualifiedBean, org.axonframework.extension.springboot.util.ConditionalOnMissingQualifiedBean, org.axonframework.modelling.annotation.TargetEntityId, org.axonframework.mo...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>java.lang.annotation.Target</td>
      <td>Annotation</td>
      <td>42</td>
      <td>[org.axonframework.extension.springboot.util.RegisterDefaultEntities, org.axonframework.extension.springboot.util.ConditionalOnQualifiedBean, org.axonframework.extension.springboot.util.ConditionalOnMissingQualifiedBean, org.axonframework.modelling.annotation.TargetEntityId, org.axonframework.mo...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>org.springframework.context.annotation.Bean</td>
      <td>Method</td>
      <td>36</td>
      <td>[org.axonframework.extension.springboot.autoconfig.AxonTimeoutAutoConfiguration.messageTimeoutHandlerEnhancerDefinition, org.axonframework.extension.springboot.autoconfig.AxonTimeoutAutoConfiguration.axonTimeoutConfigurationEnhancer, org.axonframework.extension.springboot.autoconfig.AvroSchemaSt...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Constructor</td>
      <td>19</td>
      <td>[org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessorConfiguration.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessorsConfigurer.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.su...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>org.springframework.boot.autoconfigure.condition.ConditionalOnMissingBean</td>
      <td>Method</td>
      <td>18</td>
      <td>[org.axonframework.extension.springboot.autoconfig.JpaAutoConfiguration.entityManagerProvider, org.axonframework.extension.springboot.autoconfig.JpaAutoConfiguration.tokenStore, org.axonframework.extension.springboot.autoconfig.JpaAutoConfiguration.persistenceExceptionResolver, org.axonframework...</td>
    </tr>
    <tr>
      <th>12</th>
      <td>org.springframework.boot.autoconfigure.AutoConfiguration</td>
      <td>Class</td>
      <td>18</td>
      <td>[org.axonframework.extension.springboot.autoconfig.AxonTimeoutAutoConfiguration, org.axonframework.extension.springboot.autoconfig.CorrelationDataProviderAutoConfiguration, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration, org.axonframework.extension.springboot....</td>
    </tr>
    <tr>
      <th>13</th>
      <td>java.lang.annotation.Documented</td>
      <td>Annotation</td>
      <td>15</td>
      <td>[org.axonframework.extension.springboot.util.ConditionalOnQualifiedBean, org.axonframework.extension.springboot.util.ConditionalOnMissingQualifiedBean, org.axonframework.modelling.entity.annotation.EntityMember, org.axonframework.messaging.commandhandling.annotation.CommandHandler, org.axonframe...</td>
    </tr>
    <tr>
      <th>14</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Interface</td>
      <td>14</td>
      <td>[org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodelFactory, org.axonframework.messaging.commandhandling.annotation.CommandHandlingMember, org.axonframework.messaging.eventhandling.annotation.EventHandlingMember, org.axonframework.messaging.queryhandling.annotation.QueryHandli...</td>
    </tr>
    <tr>
      <th>15</th>
      <td>com.fasterxml.jackson.annotation.JsonProperty</td>
      <td>Parameter</td>
      <td>12</td>
      <td>[org.axonframework.messaging.eventhandling.processing.streaming.token.GapAwareTrackingToken.&lt;init&gt;(0), org.axonframework.messaging.eventhandling.processing.streaming.token.GapAwareTrackingToken.&lt;init&gt;(1), org.axonframework.messaging.eventhandling.processing.streaming.token.store.ConfigToken.&lt;ini...</td>
    </tr>
    <tr>
      <th>16</th>
      <td>org.axonframework.common.Priority</td>
      <td>Class</td>
      <td>12</td>
      <td>[org.axonframework.test.FixtureResourceParameterResolverFactory, org.axonframework.messaging.eventhandling.annotation.SequenceNumberParameterResolverFactory, org.axonframework.messaging.eventhandling.annotation.TimestampParameterResolverFactory, org.axonframework.messaging.core.annotation.Hierar...</td>
    </tr>
    <tr>
      <th>17</th>
      <td>org.springframework.boot.context.properties.ConfigurationProperties</td>
      <td>Class</td>
      <td>10</td>
      <td>[org.axonframework.axonserver.connector.AxonServerConfiguration, org.axonframework.extension.springboot.DistributedCommandBusProperties, org.axonframework.extension.springboot.TokenStoreProperties, org.axonframework.extension.springboot.TagsConfigurationProperties, org.axonframework.extension.sp...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Method</td>
      <td>10</td>
      <td>[org.axonframework.messaging.eventhandling.conversion.DelegatingEventConverter.delegate, org.axonframework.messaging.eventhandling.processing.streaming.token.store.jdbc.JdbcTokenStore.converter, org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa.JpaTokenStore.converte...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>org.springframework.boot.context.properties.EnableConfigurationProperties</td>
      <td>Class</td>
      <td>9</td>
      <td>[org.axonframework.extension.springboot.autoconfig.AxonTimeoutAutoConfiguration, org.axonframework.extension.springboot.autoconfig.JpaAutoConfiguration, org.axonframework.extension.springboot.autoconfig.AxonServerAutoConfiguration, org.axonframework.extension.springboot.autoconfig.JpaEventStoreA...</td>
    </tr>
    <tr>
      <th>20</th>
      <td>jakarta.persistence.Basic</td>
      <td>Field</td>
      <td>8</td>
      <td>[org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa.TokenEntry.tokenType, org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa.TokenEntry.timestamp, org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa.TokenEntry.own...</td>
    </tr>
    <tr>
      <th>21</th>
      <td>org.springframework.boot.context.properties.NestedConfigurationProperty</td>
      <td>Field</td>
      <td>8</td>
      <td>[org.axonframework.extension.springboot.TimeoutProperties$MessageHandlerTimeoutProperties.events, org.axonframework.extension.springboot.TimeoutProperties$MessageHandlerTimeoutProperties.commands, org.axonframework.extension.springboot.TimeoutProperties$MessageHandlerTimeoutProperties.queries, o...</td>
    </tr>
    <tr>
      <th>22</th>
      <td>org.springframework.boot.autoconfigure.condition.ConditionalOnProperty</td>
      <td>Class</td>
      <td>8</td>
      <td>[org.axonframework.extension.springboot.autoconfig.AxonTimeoutAutoConfiguration, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration$AvroConfiguredCondition$MessagesAvroCondition, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration$Av...</td>
    </tr>
    <tr>
      <th>23</th>
      <td>java.lang.SafeVarargs</td>
      <td>Constructor</td>
      <td>7</td>
      <td>[org.axonframework.test.matchers.SequenceMatcher.&lt;init&gt;, org.axonframework.test.matchers.ListMatcher.&lt;init&gt;, org.axonframework.test.matchers.ExactSequenceMatcher.&lt;init&gt;, org.axonframework.test.matchers.ListWithAllOfMatcher.&lt;init&gt;, org.axonframework.test.matchers.ListWithAnyOfMatcher.&lt;init&gt;, org....</td>
    </tr>
    <tr>
      <th>24</th>
      <td>org.springframework.boot.autoconfigure.condition.ConditionalOnClass</td>
      <td>Class</td>
      <td>7</td>
      <td>[org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration, org.axonframework.extension.springboot.autoconfig.JpaAutoConfiguration, org.axonframework.extension.springboot.autoconfig.AxonServerAutoConfiguration, org.axonframework.extension.springboot.autoconfig.ObjectMapp...</td>
    </tr>
    <tr>
      <th>25</th>
      <td>java.beans.ConstructorProperties</td>
      <td>Constructor</td>
      <td>6</td>
      <td>[org.axonframework.messaging.eventhandling.processing.streaming.token.GapAwareTrackingToken.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.token.store.ConfigToken.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.token.ReplayToken.&lt;init&gt;, org.axonfram...</td>
    </tr>
    <tr>
      <th>26</th>
      <td>org.springframework.boot.context.properties.bind.DefaultValue</td>
      <td>Parameter</td>
      <td>6</td>
      <td>[org.axonframework.extension.springboot.JpaEventStorageEngineConfigurationProperties.&lt;init&gt;(0), org.axonframework.extension.springboot.JpaEventStorageEngineConfigurationProperties.&lt;init&gt;(1), org.axonframework.extension.springboot.JpaEventStorageEngineConfigurationProperties.&lt;init&gt;(2), org.axonfr...</td>
    </tr>
    <tr>
      <th>27</th>
      <td>org.springframework.context.annotation.Conditional</td>
      <td>Method</td>
      <td>6</td>
      <td>[org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration.defaultAxonSchemaStore, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration.collectAvroSchemasFromClassPath, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoCon...</td>
    </tr>
    <tr>
      <th>28</th>
      <td>com.fasterxml.jackson.annotation.JsonCreator</td>
      <td>Constructor</td>
      <td>6</td>
      <td>[org.axonframework.messaging.eventhandling.processing.streaming.token.GapAwareTrackingToken.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.token.store.ConfigToken.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.token.ReplayToken.&lt;init&gt;, org.axonfram...</td>
    </tr>
    <tr>
      <th>29</th>
      <td>org.springframework.boot.autoconfigure.AutoConfigureBefore</td>
      <td>Class</td>
      <td>6</td>
      <td>[org.axonframework.extension.springboot.autoconfig.CorrelationDataProviderAutoConfiguration, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration, org.axonframework.extension.springboot.autoconfig.AxonServerAutoConfiguration, org.axonframework.extension.springboot.a...</td>
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
      <td>2080</td>
      <td>854</td>
      <td>896</td>
      <td>[/axon-spring-boot-autoconfigure-5.0.1.jar uses /axon-server-connector-5.0.1.jar, /org/axonframework/axonserver/connector/command uses /org/axonframework/axonserver/connector/util, /org/axonframework/axonserver/connector/query uses /org/axonframework/axonserver/connector/util, /org/axonframework...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>96</td>
      <td>82</td>
      <td>41</td>
      <td>[/org/axonframework/axonserver/connector/util uses /org/axonframework/axonserver/connector, /org/axonframework/axonserver/connector/command uses /org/axonframework/axonserver/connector, /org/axonframework/axonserver/connector/query uses /org/axonframework/axonserver/connector, /org/axonframework...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>2067</td>
      <td>606</td>
      <td>417</td>
      <td>[/org/axonframework/axonserver/connector/command/CommandConverter.class uses /org/axonframework/axonserver/connector/MetadataConverter.class, /org/axonframework/axonserver/connector/event/AggregateBasedAxonServerEventStorageEngine.class uses /org/axonframework/axonserver/connector/MetadataConver...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2019</td>
      <td>650</td>
      <td>309</td>
      <td>[/org/axonframework/extension/springboot/actuator/axonserver uses /org/axonframework/axonserver/connector, /org/axonframework/extension/springboot/autoconfig uses /org/axonframework/axonserver/connector, /org/axonframework/extension/springboot uses /org/axonframework/axonserver/connector, /org/a...</td>
    </tr>
  </tbody>
</table>
</div>


