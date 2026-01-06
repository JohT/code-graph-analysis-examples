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
      <td>[MessageHandlingMember-&gt;Message, MessageHandlingMember-&gt;MessageStream, HandlerDefinition-&gt;MessageStream, Message-&gt;Message, ChainedMessageHandlerInterceptorMember-&gt;Message, ChainedMessageHandlerInterceptorMember-&gt;MessageStream, AnnotatedHandlerAttributes-&gt;SimpleHandlerAttributes, SourceIdParamete...</td>
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
      <td>[DelegatingEventHandlingComponent-&gt;Message, DelegatingEventHandlingComponent-&gt;QualifiedName, DelegatingEventHandlingComponent-&gt;MessageStream$Empty, InterceptingEventSink-&gt;MessageStream$Single, InterceptingEventSink-&gt;MessageDispatchInterceptor, InterceptingEventSink-&gt;Message, InterceptingEventSin...</td>
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
      <td>[SequenceNumberParameterResolverFactory$SequenceNumberParameterResolver-&gt;ParameterResolver, MethodEventHandlerDefinition-&gt;MessageHandlingMember, MethodEventHandlerDefinition-&gt;HandlerEnhancerDefinition, EventHandler-&gt;MessageHandler, Event-&gt;Message, TimestampParameterResolverFactory$TimestampParam...</td>
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
      <td>[CommandHandler-&gt;MessageHandler, Command-&gt;Message, CommandDispatcherParameterResolverFactory-&gt;ParameterResolverFactory, CommandDispatcherParameterResolverFactory-&gt;ParameterResolver, MethodCommandHandlerDefinition$MethodCommandHandlingMember-&gt;WrappedMessageHandlingMember, MethodCommandHandlerDefi...</td>
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
      <td>[MethodQueryHandlerDefinition-&gt;HandlerEnhancerDefinition, MethodQueryHandlerDefinition-&gt;MessageHandlingMember, AnnotatedQueryHandlingComponent-&gt;ClasspathHandlerDefinition, AnnotatedQueryHandlingComponent-&gt;ParameterResolverFactory, AnnotatedQueryHandlingComponent-&gt;ClasspathParameterResolverFactor...</td>
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
      <td>[AnnotationBasedEntityEvolvingComponent-&gt;EntityEvolvingComponent, AnnotationBasedEntityEvolvingComponent-&gt;StateEvolvingException, InjectEntityParameterResolver-&gt;EntityIdResolver, InjectEntityParameterResolver-&gt;StateManager, InjectEntityParameterResolver-&gt;EntityIdResolutionException, InjectEntity...</td>
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
      <td>[PooledStreamingEventProcessorConfiguration-&gt;EventProcessorConfiguration, PooledStreamingEventProcessorModule-&gt;EventProcessorModule$EventHandlingPhase, PooledStreamingEventProcessorModule-&gt;EventProcessorModule, PooledStreamingEventProcessorModule-&gt;EventProcessorModule$CustomizationPhase, PooledS...</td>
      <td>[EventProcessingConfigurer-&gt;PooledStreamingEventProcessorsConfigurer, EventProcessorModule-&gt;PooledStreamingEventProcessorConfiguration, EventProcessorModule-&gt;PooledStreamingEventProcessorModule]</td>
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
      <td>[SubscribingEventProcessorConfiguration-&gt;EventProcessorConfiguration, SubscribingEventProcessorModule-&gt;DefaultEventHandlingComponentsConfigurer, SubscribingEventProcessorModule-&gt;EventProcessorModule, SubscribingEventProcessorModule-&gt;EventHandlingComponentsConfigurer$CompletePhase, SubscribingEve...</td>
      <td>[EventProcessingConfigurer-&gt;SubscribingEventProcessorsConfigurer, EventProcessorModule-&gt;SubscribingEventProcessorModule, EventProcessorModule-&gt;SubscribingEventProcessorConfiguration]</td>
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
      <td>[DefaultComponentRegistry-&gt;ComponentDescriptor, Components-&gt;DescribableComponent, Components-&gt;ComponentDescriptor, Component-&gt;DescribableComponent, InstantiatedComponentDefinition-&gt;ComponentDescriptor, LazyInitializedComponentDefinition-&gt;ComponentDescriptor, ComponentRegistry-&gt;DescribableCompone...</td>
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
      <td>[MessageHandlerInterceptorDefinition$ResultHandlingInterceptorMember-&gt;InterceptorChainParameterResolverFactory, MessageHandlerInterceptorDefinition$ResultHandlingInterceptorMember-&gt;WrappedMessageHandlingMember, MessageHandlerInterceptorDefinition$ResultHandlingInterceptorMember-&gt;MessageHandlingM...</td>
      <td>[ChainedMessageHandlerInterceptorMember-&gt;MessageHandlerInterceptorMemberChain, ChainedMessageHandlerInterceptorMember-&gt;NoMoreInterceptors, AnnotatedHandlerInspector-&gt;NoMoreInterceptors, AnnotatedHandlerInspector-&gt;MessageHandlerInterceptorMemberChain, AnnotatedHandlerInspector-&gt;MessageInterceptin...</td>
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
      <td>[TransactionManager-&gt;ProcessingContext, TransactionManager-&gt;ProcessingLifecycle$ErrorHandler, TransactionManager-&gt;ProcessingLifecycle$Phase, TransactionManager-&gt;ProcessingLifecycleHandlerRegistrar, TransactionManager-&gt;ProcessingLifecycle, NoTransactionManager-&gt;ProcessingLifecycle]</td>
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
      <td>[AggregateBasedAxonServerEventStorageEngine-&gt;MetadataConverter, EventProcessorControlService-&gt;AxonServerConnectionManager, EventProcessorControlService-&gt;AxonServerConfiguration$Eventhandling, EventProcessorControlService-&gt;AxonServerConfiguration$Eventhandling$ProcessorSettings, AxonServerEventSt...</td>
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
      <td>[AxonServerConfigurationEnhancer-&gt;AxonServerCommandBusConnector, ErrorCode-&gt;AxonServerNonTransientRemoteCommandHandlingException, ErrorCode-&gt;AxonServerRemoteCommandHandlingException, ErrorCode-&gt;AxonServerCommandDispatchException]</td>
      <td>[CommandConverter-&gt;MetadataConverter, AxonServerCommandBusConnector-&gt;AxonServerConfiguration]</td>
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
      <td>[MessagingConfigurer-&gt;EventProcessingConfigurer, MessagingConfigurer-&gt;EventBusConfigurationDefaults]</td>
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
      <td>[SequentialPolicy-&gt;EventMessage, MetadataSequencingPolicy-&gt;EventMessage, SequentialPerAggregatePolicy-&gt;EventMessage, FullConcurrencyPolicy-&gt;EventMessage, HierarchicalSequencingPolicy-&gt;EventMessage, FallbackSequencingPolicy-&gt;EventMessage, ExtractionSequencingPolicy-&gt;EventMessage, SequencingPolicy...</td>
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
      <td>[QueryConverter-&gt;ErrorCode, QueryConverter-&gt;MetadataConverter, AxonServerQueryDispatchException-&gt;ErrorCode, AxonServerQueryBusConnector$AxonServerUpdateCallback-&gt;ErrorCode, FlowControlledResponseSender-&gt;ErrorCode, AxonServerQueryBusConnector-&gt;AxonServerConfiguration]</td>
      <td>[AxonServerConfigurationEnhancer-&gt;AxonServerQueryBusConnector, ErrorCode-&gt;AxonServerRemoteQueryHandlingException, ErrorCode-&gt;AxonServerNonTransientRemoteQueryHandlingException, ErrorCode-&gt;AxonServerQueryDispatchException]</td>
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
      <td>[AnnotatedEntityMetamodel-&gt;AnnotationBasedEntityEvolvingComponent, AnnotatedEntityIdResolverDefinition-&gt;EntityIdResolverDefinition, AnnotatedEntityIdResolverDefinition-&gt;AnnotationBasedEntityIdResolver]</td>
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
      <td>[LegacyMessageSupportingContext-&gt;Context$ResourceKey, LegacyMessageSupportingContext-&gt;Message, UnitOfWork$UnitOfWorkProcessingContext-&gt;ApplicationContext, UnitOfWork$UnitOfWorkProcessingContext-&gt;Context$ResourceKey, ProcessingContext-&gt;Context$ResourceKey, ProcessingContext-&gt;ApplicationContext, P...</td>
      <td>[SubscribableEventSource-&gt;ProcessingContext, DefaultMessageDispatchInterceptorChain$InterceptingDispatcher-&gt;ProcessingContext, MessageDispatchInterceptor-&gt;ProcessingContext, DefaultMessageDispatchInterceptorChain-&gt;ProcessingContext, MessageHandlerInterceptor-&gt;ProcessingContext, Message-&gt;Processi...</td>
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
      <td>[SingleEntityChildMetamodel-&gt;EntityMetamodel, SingleEntityChildMetamodel$Builder-&gt;EntityMetamodel, ListEntityChildMetamodel$Builder-&gt;EntityMetamodel, AbstractEntityChildMetamodel-&gt;EntityMetamodel, AbstractEntityChildMetamodel-&gt;ChildEntityNotFoundException, ListEntityChildMetamodel-&gt;EntityMetamod...</td>
      <td>[ConcreteEntityMetamodel-&gt;ChildAmbiguityException, ConcreteEntityMetamodel-&gt;EntityChildMetamodel, ConcreteEntityMetamodel$Builder-&gt;EntityChildMetamodel, PolymorphicEntityMetamodelBuilder-&gt;EntityChildMetamodel, EntityMetamodelBuilder-&gt;EntityChildMetamodel, PolymorphicEntityMetamodel$Builder-&gt;Enti...</td>
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
      <td>[ErrorCode-&gt;ExceptionConverter, AxonServerConnectionManager$Builder-&gt;GrpcMessageSizeInterceptor]</td>
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
      <td>MessageStreamResolverUtils-&gt;GenericMessage</td>
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
      <td>AggregateTypeParameterResolverFactory$AggregateTypeParameterResolver-&gt;LegacyResources</td>
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
      <td>AnnotationMessageTypeResolver-&gt;ClassBasedMessageTypeResolver</td>
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
      <td>MessageStreamResolverUtils-&gt;MonoUtils</td>
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
      <td>MessageStreamResolverUtils-&gt;MessageStream$Empty</td>
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
      <td>AggregateTypeParameterResolverFactory$AggregateTypeParameterResolver-&gt;Context$ResourceKey</td>
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
      <td>MethodInvokingMessageHandlingMember-&gt;MessageStream$Entry</td>
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
      <td>MessageHandler-&gt;Message</td>
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
      <td>AnnotatedHandlerInspector-&gt;MessageStream</td>
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
      <td>MessageStreamResolverUtils-&gt;MessageStream$Single</td>
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
      <td>MethodInvokingMessageHandlingMember-&gt;DelayedMessageStream</td>
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
      <td>MessageStreamResolverUtils-&gt;MessageStream</td>
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
      <td>MethodInvokingMessageHandlingMember-&gt;MessageStream$Empty</td>
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
      <td>AnnotatedMessageHandlingMemberDefinition-&gt;Message</td>
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
      <td>DefaultParameterResolverFactory$AnnotatedMetadataParameterResolver-&gt;Message</td>
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
      <td>MethodInvokingMessageHandlingMember-&gt;MessageStream$Single</td>
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
      <td>SourceIdParameterResolverFactory$SourceIdParameterResolver-&gt;LegacyResources</td>
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
      <td>AnnotationMessageTypeResolver-&gt;MessageTypeResolver</td>
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
      <td>AnnotationMessageTypeResolver-&gt;MessageType</td>
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
      <td>AnnotatedHandlerInspector-&gt;Message</td>
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
      <td>MessageStreamResolverUtils-&gt;MessageTypeResolver</td>
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
      <td>MultiHandlerDefinition-&gt;MessageStream</td>
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
      <td>MessageHandlingMember-&gt;MessageStream</td>
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
      <td>MessageStreamResolverUtils-&gt;FluxUtils</td>
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
      <td>WrappedMessageHandlingMember-&gt;MessageStream</td>
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
      <td>MessageHandlingMember-&gt;Message</td>
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
      <td>WrappedMessageHandlingMember-&gt;Message</td>
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
      <td>AnnotatedMessageHandlingMemberDefinition-&gt;MessageStream</td>
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
      <td>Message-&gt;Message</td>
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
      <td>MessageIdentifierParameterResolverFactory$MessageIdentifierParameterResolver-&gt;Message</td>
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
      <td>HandlerDefinition-&gt;MessageStream</td>
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
      <td>MethodInvokingMessageHandlingMember-&gt;Message</td>
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
      <td>ChainedMessageHandlerInterceptorMember-&gt;Message</td>
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
      <td>SourceIdParameterResolverFactory$SourceIdParameterResolver-&gt;Context$ResourceKey</td>
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
      <td>ChainedMessageHandlerInterceptorMember-&gt;MessageStream</td>
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
      <td>AnnotatedHandlerAttributes-&gt;SimpleHandlerAttributes</td>
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
      <td>DefaultParameterResolverFactory$AnnotatedMetadataParameterResolver-&gt;Metadata</td>
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
      <td>InterceptorChainParameterResolverFactory-&gt;MessageStream</td>
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
      <td>PooledStreamingEventProcessorModule&lt;-EventProcessorModule</td>
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
      <td>PooledStreamingEventProcessorConfiguration&lt;-EventProcessorModule</td>
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
      <td>PooledStreamingEventProcessorsConfigurer&lt;-EventProcessingConfigurer</td>
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
      <td>SubscribingEventProcessorsConfigurer&lt;-EventProcessingConfigurer</td>
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
      <td>SubscribingEventProcessorConfiguration&lt;-EventProcessorModule</td>
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
      <td>NoMoreInterceptors&lt;-AnnotatedHandlerInspector</td>
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
      <td>MessageInterceptingMember&lt;-AnnotatedHandlerInspector</td>
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
      <td>MetadataConverter&lt;-CommandConverter</td>
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
      <td>AxonServerConfiguration&lt;-AxonServerCommandBusConnector</td>
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
      <td>AxonServerNonTransientRemoteQueryHandlingException&lt;-ErrorCode</td>
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
      <td>AxonServerRemoteQueryHandlingException&lt;-ErrorCode</td>
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
      <td>AxonServerQueryDispatchException&lt;-ErrorCode</td>
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
      <td>ProcessingContext&lt;-MessageHandlerInterceptorChain</td>
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
      <td>ProcessingContext&lt;-MessageDispatchInterceptorChain</td>
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
      <td>org.axonframework.messaging.commandhandling.CommandBus</td>
      <td>6</td>
      <td>[dispatch]</td>
      <td>1</td>
      <td>6</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.axonframework.common.configuration.ComponentDefinition$ComponentCreator</td>
      <td>17</td>
      <td>[createComponent]</td>
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
      <td>org.axonframework.test.fixture.AxonTestThenMessage</td>
      <td>22</td>
      <td>[exceptionSatisfies, exception]</td>
      <td>3</td>
      <td>2</td>
    </tr>
    <tr>
      <th>17</th>
      <td>org.axonframework.messaging.commandhandling.CommandMessage</td>
      <td>19</td>
      <td>[andMetadata]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>18</th>
      <td>org.axonframework.messaging.eventhandling.EventMessage</td>
      <td>19</td>
      <td>[withConvertedPayload]</td>
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
      <td>org.axonframework.messaging.eventstreaming.EventCriterion</td>
      <td>12</td>
      <td>[tags]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>21</th>
      <td>org.axonframework.messaging.eventstreaming.OrEventCriteria</td>
      <td>12</td>
      <td>[or]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>22</th>
      <td>org.axonframework.modelling.entity.ConcreteEntityMetamodel</td>
      <td>11</td>
      <td>[forEntityClass]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>23</th>
      <td>org.axonframework.modelling.entity.PolymorphicEntityMetamodel</td>
      <td>11</td>
      <td>[forSuperType]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>24</th>
      <td>org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodel</td>
      <td>11</td>
      <td>[entityType]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>25</th>
      <td>org.axonframework.eventsourcing.eventstore.EventStore</td>
      <td>9</td>
      <td>[transaction]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>26</th>
      <td>org.axonframework.messaging.eventhandling.EventHandlingComponent</td>
      <td>8</td>
      <td>[supportedEvents, sequenceIdentifierFor, supports]</td>
      <td>3</td>
      <td>2</td>
    </tr>
    <tr>
      <th>27</th>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.token.WrappedToken</td>
      <td>8</td>
      <td>[unwrapLowerBound]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>28</th>
      <td>org.axonframework.messaging.core.MessageStream$Entry</td>
      <td>7</td>
      <td>[map]</td>
      <td>1</td>
      <td>2</td>
    </tr>
    <tr>
      <th>29</th>
      <td>org.axonframework.messaging.core.unitofwork.UnitOfWork$UnitOfWorkProcessingContext</td>
      <td>45</td>
      <td>[whenComplete, isError, isStarted, on, isCommitted, commit, onError, isCompleted]</td>
      <td>8</td>
      <td>1</td>
    </tr>
    <tr>
      <th>30</th>
      <td>org.axonframework.messaging.core.EmptyMessageStream</td>
      <td>44</td>
      <td>[instance]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>31</th>
      <td>org.axonframework.eventsourcing.eventstore.inmemory.InMemoryEventStorageEngine$MapBackedMessageStream</td>
      <td>43</td>
      <td>[hasNextAvailable, isCompleted]</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>32</th>
      <td>org.axonframework.eventsourcing.eventstore.inmemory.InMemoryEventStorageEngine$MapBackedMessageStream</td>
      <td>42</td>
      <td>[callback]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>33</th>
      <td>org.axonframework.messaging.core.DelayedMessageStream</td>
      <td>42</td>
      <td>[createSingle]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>34</th>
      <td>org.axonframework.messaging.core.MessageStream$Single</td>
      <td>42</td>
      <td>[cast]</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>35</th>
      <td>org.axonframework.messaging.core.MessageStream$Single</td>
      <td>42</td>
      <td>[asCompletableFuture]</td>
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
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>37</td>
      <td>[updateResource, removeResource, putResourceIfAbsent, putResource, computeResourceIfAbsent]</td>
      <td>6</td>
      <td>1</td>
    </tr>
    <tr>
      <th>38</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>36</td>
      <td>[updateResource, computeResourceIfAbsent]</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>39</th>
      <td>org.axonframework.messaging.core.unitofwork.ProcessingContext</td>
      <td>35</td>
      <td>[computeResourceIfAbsent]</td>
      <td>1</td>
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
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWea...</td>
      <td>35</td>
    </tr>
    <tr>
      <th>6</th>
      <td>org.axonframework.messaging.core.MessageType</td>
      <td>MessageType</td>
      <td>[Type, File, Java, ByteCode, Record, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation2, M...</td>
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
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation24, Mark4TypeLouvainCommunity1...</td>
      <td>28</td>
    </tr>
    <tr>
      <th>9</th>
      <td>org.axonframework.common.FutureUtils</td>
      <td>FutureUtils</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation14, Mark4TypeLouvainCommunity2, Mark...</td>
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
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation46, Mark4TypeLouvainCommunity17, Mark4TypeLeidenCommunity16, Mark4Typ...</td>
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
      <td>[Type, File, Java, Class, ByteCode, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation3, Mark4TypeLouvainCommunity1, Mark4TypeLeidenCommunity1, Mark4TypeKCoreDecomposition8, Mark4TypeMaximumKCut9, Mark4TypeHDBSCAN84, Mark4TopAnomalyHub]</td>
      <td>21</td>
    </tr>
    <tr>
      <th>14</th>
      <td>org.axonframework.common.configuration.ComponentRegistry</td>
      <td>ComponentRegistry</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityBetweenness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation33, Mark4TypeLouvainCommunity12, Mark4TypeLeidenCommunity12, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut0, Mark4TypeHDBSCAN70]</td>
      <td>21</td>
    </tr>
    <tr>
      <th>15</th>
      <td>org.axonframework.common.Assert</td>
      <td>Assert</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityCostEffectiveLazyForward, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation7, Mark4TypeLouvainCommunity5, Mark4Typ...</td>
      <td>20</td>
    </tr>
    <tr>
      <th>16</th>
      <td>org.axonframework.messaging.commandhandling.CommandMessage</td>
      <td>CommandMessage</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityArticleRank, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation8, Mark4TypeLouvainCommunity11, Mark4TypeLeidenCommunity4,...</td>
      <td>20</td>
    </tr>
    <tr>
      <th>17</th>
      <td>org.axonframework.messaging.core.MessageStream$Entry</td>
      <td>MessageStream$Entry</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TopCentralityArticleRank, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation46, Mark4TypeLouvainCommunity17, Mark4...</td>
      <td>19</td>
    </tr>
    <tr>
      <th>18</th>
      <td>org.axonframework.messaging.core.annotation.ParameterResolverFactory</td>
      <td>ParameterResolverFactory</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation66, Mark4TypeLouvainCommunity6, Mark4TypeLeidenCommunity10, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut0, Mark4TypeHDBSCAN-1]</td>
      <td>19</td>
    </tr>
    <tr>
      <th>19</th>
      <td>org.axonframework.messaging.core.MessageStream$Single</td>
      <td>MessageStream$Single</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation46, Mar...</td>
      <td>18</td>
    </tr>
    <tr>
      <th>20</th>
      <td>org.axonframework.common.configuration.ConfigurationEnhancer</td>
      <td>ConfigurationEnhancer</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation28, Mark4TypeLouvainCommunity12, Mark4TypeLeidenCommunity12, Mark4TypeKCoreDecomposition8, Mark4TypeMaximumKCut1, Mark4TypeHDBSCAN42]</td>
      <td>17</td>
    </tr>
    <tr>
      <th>21</th>
      <td>org.axonframework.messaging.core.Metadata</td>
      <td>Metadata</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityPageRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation2, Mark4TypeLouvainCommunity0, Mark4TypeLeidenCommunity0, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut95, Ma...</td>
      <td>16</td>
    </tr>
    <tr>
      <th>22</th>
      <td>org.axonframework.conversion.Converter</td>
      <td>Converter</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation2, Mark4TypeLouvainCommunity0, Mark4TypeLeidenCommunity0, Mark4TypeKCoreDecompo...</td>
      <td>15</td>
    </tr>
    <tr>
      <th>23</th>
      <td>org.axonframework.messaging.core.conversion.MessageConverter</td>
      <td>MessageConverter</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation2, Mark4TypeLouvainCommunity4, Mark4TypeLeidenCommunity16, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut96, Mark4TypeLocalClusteringCoefficient0.1225296442687747, Mark4TypeHDBSCAN-1]</td>
      <td>15</td>
    </tr>
    <tr>
      <th>24</th>
      <td>org.axonframework.messaging.eventhandling.processing.streaming.token.TrackingToken</td>
      <td>TrackingToken</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityArticleRank, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation47, Mark4TypeLouvainCommunity2, Mark4TypeLeidenCommunity2,...</td>
      <td>15</td>
    </tr>
    <tr>
      <th>25</th>
      <td>org.axonframework.common.AxonConfigurationException</td>
      <td>AxonConfigurationException</td>
      <td>[Type, File, Java, Class, ByteCode, Throwable, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation10, Mark4TypeLouvainCommunity6, Mark4TypeLeidenCommunity5, Mark4TypeKCoreDecomposition8, Mark4TypeMaximumKCut60, Mark4TypeHDBSCAN-1]</td>
      <td>14</td>
    </tr>
    <tr>
      <th>26</th>
      <td>org.axonframework.messaging.core.MessageTypeResolver</td>
      <td>MessageTypeResolver</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation2, Mark4TypeLouvainCommunity0, Mark4TypeLeidenCommunity0, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut1, Mark4TypeHDBSCAN77]</td>
      <td>14</td>
    </tr>
    <tr>
      <th>27</th>
      <td>org.axonframework.common.ObjectUtils</td>
      <td>ObjectUtils</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation2, Mark4TypeLouvainCommunity0, Mark4TypeLeidenCommunity0, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut0, Mark4TypeHDBSCAN-1]</td>
      <td>14</td>
    </tr>
    <tr>
      <th>28</th>
      <td>org.axonframework.messaging.commandhandling.CommandBus</td>
      <td>CommandBus</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation8, Mark4TypeLouvainCommunity11, Mark4TypeLeidenCommunity4, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut53, Mark4TypeHDBSCAN-1]</td>
      <td>13</td>
    </tr>
    <tr>
      <th>29</th>
      <td>org.axonframework.messaging.queryhandling.QueryMessage</td>
      <td>QueryMessage</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation43, Mark4TypeLouvainCommunity4, Mark4TypeLeidenCommunity16, Mark4TypeKCoreDecomposition9,...</td>
      <td>13</td>
    </tr>
    <tr>
      <th>30</th>
      <td>org.axonframework.messaging.commandhandling.CommandResultMessage</td>
      <td>CommandResultMessage</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation2, Mark4TypeLouvainCommunity0, Mark4TypeLeidenCommunity0, Mark4TypeKCoreDecomposition9, M...</td>
      <td>12</td>
    </tr>
    <tr>
      <th>31</th>
      <td>org.axonframework.common.configuration.ComponentDefinition</td>
      <td>ComponentDefinition</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation37, Mark4TypeLouvainCommunity12, Mark4TypeLeidenCommunity12, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut80, Mark4TypeLocalClusteringCoefficient0.2028985507246377, Mark4...</td>
      <td>12</td>
    </tr>
    <tr>
      <th>32</th>
      <td>org.axonframework.common.configuration.ComponentDefinition$IncompleteComponentDefinition</td>
      <td>ComponentDefinition$IncompleteComponentDefinition</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation37, Mark4TypeLouvainCommunity12, Mark4TypeLeidenCommunity12, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut20, Mark4TypeHDBSCAN128]</td>
      <td>12</td>
    </tr>
    <tr>
      <th>33</th>
      <td>org.axonframework.messaging.core.Context</td>
      <td>Context</td>
      <td>[Type, File, Java, ByteCode, Interface, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation46, Mark4TypeLouvainCommunity17, Mark4TypeLeiden...</td>
      <td>12</td>
    </tr>
    <tr>
      <th>34</th>
      <td>org.axonframework.common.ReflectionUtils</td>
      <td>ReflectionUtils</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityBetweenness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation19, Mark4TypeLouvainCommunity6, Mark4TypeLeidenCommunity5, Mark4TypeKCoreDecomposition8, Mark4TypeMaximumKCut11, Mark4TypeHDBSCAN123, Mark4TopAnomalyBottleneck]</td>
      <td>12</td>
    </tr>
    <tr>
      <th>35</th>
      <td>org.axonframework.common.AxonNonTransientException</td>
      <td>AxonNonTransientException</td>
      <td>[Type, File, Java, Class, ByteCode, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation15, Mark4TypeLouvainCommunity3, Mark4TypeLeidenCommunity3, Mark4TypeKCoreDecomposition4, Mark4TypeMaximumKCut26, Mark4TypeLocalClusteringCoe...</td>
      <td>11</td>
    </tr>
    <tr>
      <th>36</th>
      <td>org.axonframework.common.configuration.ComponentBuilder</td>
      <td>ComponentBuilder</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation33, Mark4TypeLouvainCommunity12, Mark4TypeLeidenCommunity12, Mark4TypeKCoreDecomposition9, Mark4TypeMaximumKCut7, Mark4TypeHDBSCAN69]</td>
      <td>11</td>
    </tr>
    <tr>
      <th>37</th>
      <td>org.axonframework.messaging.core.MessageHandlerInterceptor</td>
      <td>MessageHandlerInterceptor</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TopCentralityBetweenness, Mark4TopCentralityHyperlinkInducedTopicSearchAuthority, Mark4TopCentralityHyperlinkInducedTopicSearchHub, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation85, Mark4TypeLouvainCommunity12, Mark4...</td>
      <td>11</td>
    </tr>
    <tr>
      <th>38</th>
      <td>org.axonframework.messaging.core.annotation.ParameterResolver</td>
      <td>ParameterResolver</td>
      <td>[Type, File, Java, ByteCode, GenericDeclaration, Interface, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation14, Mark4TypeLouvainCommunity6, Mark4TypeLeidenCommunity5, Mark4TypeKCoreDecomposition7, Mark4TypeMaximumKCut47, Mark4TypeHDBSCAN-1]</td>
      <td>11</td>
    </tr>
    <tr>
      <th>39</th>
      <td>org.axonframework.common.TypeReference</td>
      <td>TypeReference</td>
      <td>[Type, File, Java, Class, ByteCode, GenericDeclaration, Mark4TopCentralityPageRank, Mark4TopCentralityArticleRank, Mark4TopCentralityBetweenness, Mark4TopCentralityHarmonic, Mark4TopCentralityCloseness, Mark4TypeWeaklyConnectedComponent0, Mark4TypeLabelPropagation23, Mark4TypeLouvainCommunity12,...</td>
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
      <td>[org.axonframework.messaging.tracing, org.axonframework.messaging.core]</td>
      <td>[tracing, core]</td>
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
      <td>[org.axonframework.messaging.core, org.axonframework.messaging.eventhandling.processing, org.axonframework.messaging.commandhandling, org.axonframework.messaging.eventhandling, org.axonframework.messaging.queryhandling, org.axonframework.messaging.monitoring]</td>
      <td>[core, processing, commandhandling, eventhandling, queryhandling, monitoring]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-test-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>8</td>
      <td>57</td>
      <td>0.140351</td>
      <td>[org.axonframework.messaging.core, org.axonframework.messaging.eventhandling, org.axonframework.messaging.commandhandling, org.axonframework.messaging.monitoring, org.axonframework.messaging.core.unitofwork, org.axonframework.messaging.core.annotation, org.axonframework.messaging.eventhandling.p...</td>
      <td>[core, eventhandling, commandhandling, monitoring, unitofwork, annotation, token, eventstreaming]</td>
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
      <td>[org.axonframework.common, org.axonframework.common.configuration]</td>
      <td>[common, configuration]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>axon-test-5.0.1</td>
      <td>1</td>
      <td>5</td>
      <td>0.200000</td>
      <td>[org.axonframework.test.server]</td>
      <td>[server]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>axon-server-connector-5.0.1</td>
      <td>1</td>
      <td>5</td>
      <td>0.200000</td>
      <td>[org.axonframework.axonserver.connector]</td>
      <td>[connector]</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-modelling-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>13</td>
      <td>57</td>
      <td>0.228070</td>
      <td>[org.axonframework.messaging.core, org.axonframework.messaging.commandhandling, org.axonframework.messaging.core.unitofwork, org.axonframework.messaging.eventhandling, org.axonframework.messaging.core.interception.annotation, org.axonframework.messaging.eventhandling.conversion, org.axonframewor...</td>
      <td>[core, commandhandling, unitofwork, eventhandling, annotation, conversion, reflection, configuration]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-conversion-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>3</td>
      <td>13</td>
      <td>0.230769</td>
      <td>[org.axonframework.common.infra, org.axonframework.common.annotation, org.axonframework.common]</td>
      <td>[infra, annotation, common]</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-update-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>3</td>
      <td>13</td>
      <td>0.230769</td>
      <td>[org.axonframework.common.annotation, org.axonframework.common, org.axonframework.common.configuration]</td>
      <td>[annotation, common, configuration]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-modelling-5.0.1</td>
      <td>axon-conversion-5.0.1</td>
      <td>1</td>
      <td>4</td>
      <td>0.250000</td>
      <td>[org.axonframework.conversion]</td>
      <td>[conversion]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-conversion-5.0.1</td>
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
      <td>[org.axonframework.messaging.core.timeout, org.axonframework.messaging.core.correlation, org.axonframework.messaging.eventhandling.processing.streaming.token.store, org.axonframework.messaging.eventhandling.conversion, org.axonframework.messaging.queryhandling, org.axonframework.messaging.queryh...</td>
      <td>[timeout, correlation, store, conversion, queryhandling, distributed, transaction, annotation, commandhandling, core, eventhandling, interception, jpa]</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>16</td>
      <td>57</td>
      <td>0.280702</td>
      <td>[org.axonframework.messaging.eventhandling.annotation, org.axonframework.messaging.eventstreaming, org.axonframework.messaging.core.unitofwork, org.axonframework.messaging.eventhandling, org.axonframework.messaging.core, org.axonframework.messaging.core.configuration, org.axonframework.messaging...</td>
      <td>[annotation, eventstreaming, unitofwork, eventhandling, core, configuration, commandhandling, conversion, interception, token, transaction]</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-server-connector-5.0.1</td>
      <td>axon-messaging-5.0.1</td>
      <td>16</td>
      <td>57</td>
      <td>0.280702</td>
      <td>[org.axonframework.messaging.core, org.axonframework.messaging.commandhandling.distributed, org.axonframework.messaging.commandhandling, org.axonframework.messaging.core.unitofwork, org.axonframework.messaging.eventhandling.processing.streaming.segmenting, org.axonframework.messaging.eventhandli...</td>
      <td>[core, distributed, commandhandling, unitofwork, segmenting, store, processing, conversion, token, eventstreaming, streaming, eventhandling, subscribing, queryhandling]</td>
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
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>4</td>
      <td>13</td>
      <td>0.307692</td>
      <td>[org.axonframework.common.jpa, org.axonframework.common.configuration, org.axonframework.common, org.axonframework.common.jdbc]</td>
      <td>[jpa, configuration, common, jdbc]</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-test-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>4</td>
      <td>13</td>
      <td>0.307692</td>
      <td>[org.axonframework.common, org.axonframework.common.infra, org.axonframework.common.annotation, org.axonframework.common.configuration]</td>
      <td>[common, infra, annotation, configuration]</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-modelling-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>5</td>
      <td>13</td>
      <td>0.384615</td>
      <td>[org.axonframework.common, org.axonframework.common.infra, org.axonframework.common.property, org.axonframework.common.configuration, org.axonframework.common.annotation]</td>
      <td>[common, infra, property, configuration, annotation]</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-common-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>6</td>
      <td>13</td>
      <td>0.461538</td>
      <td>[org.axonframework.common, org.axonframework.common.annotation, org.axonframework.common.configuration, org.axonframework.common.infra, org.axonframework.common.lifecycle, org.axonframework.common.io]</td>
      <td>[common, annotation, configuration, infra, lifecycle, io]</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-server-connector-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>6</td>
      <td>13</td>
      <td>0.461538</td>
      <td>[org.axonframework.common.lifecycle, org.axonframework.common.annotation, org.axonframework.common.infra, org.axonframework.common, org.axonframework.common.util, org.axonframework.common.configuration]</td>
      <td>[lifecycle, annotation, infra, common, util, configuration]</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>1</td>
      <td>2</td>
      <td>0.500000</td>
      <td>[org.axonframework.extension.metrics.micrometer.reservoir]</td>
      <td>[reservoir]</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-conversion-5.0.1</td>
      <td>2</td>
      <td>4</td>
      <td>0.500000</td>
      <td>[org.axonframework.conversion, org.axonframework.conversion.json]</td>
      <td>[conversion, json]</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>7</td>
      <td>13</td>
      <td>0.538462</td>
      <td>[org.axonframework.common.configuration, org.axonframework.common, org.axonframework.common.infra, org.axonframework.common.annotation, org.axonframework.common.jpa, org.axonframework.common.jdbc, org.axonframework.common.io]</td>
      <td>[configuration, common, infra, annotation, jpa, jdbc, io]</td>
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
      <td>[org.axonframework.test, org.axonframework.test.matchers, org.axonframework.test.util]</td>
      <td>[test, matchers, util]</td>
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
      <th>1</th>
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
      <td>org.axonframework.messaging.eventhandling.processing.streaming.token.store</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.AxonTransientException]</td>
    </tr>
    <tr>
      <th>13</th>
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
      <th>14</th>
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
      <th>15</th>
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
      <th>16</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.eventstreaming</td>
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
      <td>org.axonframework.messaging.core.timeout</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.AxonThreadFactory]</td>
    </tr>
    <tr>
      <th>18</th>
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
      <th>19</th>
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
      <th>20</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.core.unitofwork.annotation</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.Priority]</td>
    </tr>
    <tr>
      <th>21</th>
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
      <th>22</th>
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
      <th>23</th>
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
      <th>24</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.monitoring.configuration</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.TypeReference]</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.queryhandling.annotation</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.ReflectionUtils]</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.core.interception.annotation</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.AxonConfigurationException]</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.AxonConfigurationException]</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.eventsourcing.annotation</td>
      <td>org.axonframework.common</td>
      <td>1</td>
      <td>34</td>
      <td>0.029412</td>
      <td>[org.axonframework.common.ReflectionUtils]</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-messaging-5.0.1</td>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.messaging.queryhandling.configuration</td>
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
      <td>[org.axonframework.extension.tracing.opentelemetry.MetadataContextSetter.set(1), org.axonframework.extension.tracing.opentelemetry.MetadataContextSetter.set(2), org.axonframework.extension.tracing.opentelemetry.MetadataContextGetter.get(1), org.axonframework.extension.tracing.opentelemetry.OpenT...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>jakarta.annotation.Nonnull</td>
      <td>Method</td>
      <td>833</td>
      <td>[org.axonframework.common.util.ExecutorServiceFactory.createExecutorService, org.axonframework.common.ReflectionUtils.ensureAccessible, org.axonframework.common.ReflectionUtils.fieldsOf, org.axonframework.common.ReflectionUtils.methodOf, org.axonframework.common.ReflectionUtils.methodsOf, org.ax...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>jakarta.annotation.Nullable</td>
      <td>Parameter</td>
      <td>399</td>
      <td>[org.axonframework.common.StringUtils.capitalize(0), org.axonframework.common.ReflectionUtils.explicitlyUnequal(0), org.axonframework.common.ReflectionUtils.explicitlyUnequal(1), org.axonframework.common.lifecycle.LifecycleHandlerInvocationException.&lt;init&gt;(1), org.axonframework.common.configurat...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>jakarta.annotation.Nullable</td>
      <td>Method</td>
      <td>99</td>
      <td>[org.axonframework.common.ReflectionUtils.declaringClass, org.axonframework.common.FutureUtils.joinAndUnwrap, org.axonframework.common.configuration.AbstractComponent.name, org.axonframework.common.configuration.ComponentDefinition.name, org.axonframework.common.configuration.Component$Identifie...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Class</td>
      <td>75</td>
      <td>[org.axonframework.common.configuration.LazyInitializedComponentDefinition, org.axonframework.common.configuration.InstantiatedComponentDefinition, org.axonframework.common.configuration.Components, org.axonframework.axonserver.connector.MetadataConverter, org.axonframework.axonserver.connector....</td>
    </tr>
    <tr>
      <th>5</th>
      <td>jakarta.annotation.Nonnull</td>
      <td>Field</td>
      <td>70</td>
      <td>[org.axonframework.common.configuration.AbstractComponent$HandlerRegistration.handler, org.axonframework.common.configuration.Component$Identifier.type, org.axonframework.axonserver.connector.command.AxonServerCommandBusConnector$FutureResultCallback.result, org.axonframework.axonserver.connecto...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>java.lang.FunctionalInterface</td>
      <td>Interface</td>
      <td>55</td>
      <td>[org.axonframework.common.jdbc.JdbcUtils$SqlResultConverter, org.axonframework.common.jdbc.ConnectionProvider, org.axonframework.common.jdbc.JdbcUtils$SqlFunction, org.axonframework.common.util.ExecutorServiceFactory, org.axonframework.common.property.Property, org.axonframework.common.Registrat...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>java.lang.annotation.Retention</td>
      <td>Annotation</td>
      <td>42</td>
      <td>[org.axonframework.common.annotation.Internal, org.axonframework.common.Priority, org.axonframework.modelling.annotation.TargetEntityId, org.axonframework.modelling.annotation.InjectEntity, org.axonframework.modelling.entity.annotation.EntityMember, org.axonframework.eventsourcing.annotation.Eve...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>java.lang.annotation.Target</td>
      <td>Annotation</td>
      <td>42</td>
      <td>[org.axonframework.common.annotation.Internal, org.axonframework.common.Priority, org.axonframework.modelling.annotation.TargetEntityId, org.axonframework.modelling.annotation.InjectEntity, org.axonframework.modelling.entity.annotation.EntityMember, org.axonframework.eventsourcing.annotation.Eve...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>org.springframework.context.annotation.Bean</td>
      <td>Method</td>
      <td>36</td>
      <td>[org.axonframework.extension.springboot.autoconfig.AxonTimeoutAutoConfiguration.messageTimeoutHandlerEnhancerDefinition, org.axonframework.extension.springboot.autoconfig.AxonTimeoutAutoConfiguration.axonTimeoutConfigurationEnhancer, org.axonframework.extension.springboot.autoconfig.CorrelationD...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Constructor</td>
      <td>19</td>
      <td>[org.axonframework.eventsourcing.eventstore.InterceptingEventStore.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessorConfiguration.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessors...</td>
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
      <td>[org.axonframework.common.annotation.Internal, org.axonframework.modelling.entity.annotation.EntityMember, org.axonframework.eventsourcing.annotation.EventSourcingHandler, org.axonframework.extension.springboot.util.ConditionalOnQualifiedBean, org.axonframework.extension.springboot.util.Conditio...</td>
    </tr>
    <tr>
      <th>14</th>
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Interface</td>
      <td>14</td>
      <td>[org.axonframework.common.jdbc.ConnectionProvider, org.axonframework.common.jpa.EntityManagerProvider, org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodelFactory, org.axonframework.eventsourcing.eventstore.EventCoordinator, org.axonframework.eventsourcing.eventstore.EventStora...</td>
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
      <td>org.axonframework.common.annotation.Internal</td>
      <td>Method</td>
      <td>10</td>
      <td>[org.axonframework.messaging.eventhandling.conversion.DelegatingEventConverter.delegate, org.axonframework.messaging.eventhandling.processing.streaming.token.store.jdbc.JdbcTokenStore.converter, org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa.JpaTokenStore.converte...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>org.springframework.boot.context.properties.ConfigurationProperties</td>
      <td>Class</td>
      <td>10</td>
      <td>[org.axonframework.axonserver.connector.AxonServerConfiguration, org.axonframework.extension.springboot.DistributedCommandBusProperties, org.axonframework.extension.springboot.TokenStoreProperties, org.axonframework.extension.springboot.TagsConfigurationProperties, org.axonframework.extension.sp...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>org.springframework.boot.context.properties.EnableConfigurationProperties</td>
      <td>Class</td>
      <td>9</td>
      <td>[org.axonframework.extension.springboot.autoconfig.AxonTimeoutAutoConfiguration, org.axonframework.extension.springboot.autoconfig.JpaAutoConfiguration, org.axonframework.extension.springboot.autoconfig.UpdateCheckerAutoConfiguration, org.axonframework.extension.springboot.autoconfig.ConverterAu...</td>
    </tr>
    <tr>
      <th>20</th>
      <td>org.springframework.boot.autoconfigure.condition.ConditionalOnProperty</td>
      <td>Class</td>
      <td>8</td>
      <td>[org.axonframework.extension.springboot.autoconfig.AxonTimeoutAutoConfiguration, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration$AvroConfiguredCondition$MessagesAvroCondition, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration$Av...</td>
    </tr>
    <tr>
      <th>21</th>
      <td>jakarta.persistence.Basic</td>
      <td>Field</td>
      <td>8</td>
      <td>[org.axonframework.eventsourcing.eventstore.jpa.AggregateEventEntry.type, org.axonframework.eventsourcing.eventstore.jpa.AggregateEventEntry.version, org.axonframework.eventsourcing.eventstore.jpa.AggregateEventEntry.timestamp, org.axonframework.eventsourcing.eventstore.jpa.AggregateEventEntry.p...</td>
    </tr>
    <tr>
      <th>22</th>
      <td>org.springframework.boot.context.properties.NestedConfigurationProperty</td>
      <td>Field</td>
      <td>8</td>
      <td>[org.axonframework.extension.springboot.TimeoutProperties$MessageHandlerTimeoutProperties.commands, org.axonframework.extension.springboot.TimeoutProperties$MessageHandlerTimeoutProperties.queries, org.axonframework.extension.springboot.TimeoutProperties$MessageHandlerTimeoutProperties.deadlines...</td>
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
      <td>org.springframework.context.annotation.Conditional</td>
      <td>Method</td>
      <td>6</td>
      <td>[org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration.defaultAxonSchemaStore, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration.collectAvroSchemasFromClassPath, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoCon...</td>
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
      <td>com.fasterxml.jackson.annotation.JsonCreator</td>
      <td>Constructor</td>
      <td>6</td>
      <td>[org.axonframework.messaging.eventhandling.processing.streaming.token.GapAwareTrackingToken.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.token.store.ConfigToken.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.token.ReplayToken.&lt;init&gt;, org.axonfram...</td>
    </tr>
    <tr>
      <th>28</th>
      <td>org.springframework.boot.autoconfigure.AutoConfigureBefore</td>
      <td>Class</td>
      <td>6</td>
      <td>[org.axonframework.extension.springboot.autoconfig.CorrelationDataProviderAutoConfiguration, org.axonframework.extension.springboot.autoconfig.AvroSchemaStoreAutoConfiguration, org.axonframework.extension.springboot.autoconfig.ConverterAutoConfiguration, org.axonframework.extension.springboot.au...</td>
    </tr>
    <tr>
      <th>29</th>
      <td>java.beans.ConstructorProperties</td>
      <td>Constructor</td>
      <td>6</td>
      <td>[org.axonframework.messaging.eventhandling.processing.streaming.token.GapAwareTrackingToken.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.token.store.ConfigToken.&lt;init&gt;, org.axonframework.messaging.eventhandling.processing.streaming.token.ReplayToken.&lt;init&gt;, org.axonfram...</td>
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
      <td>[/org/axonframework/extension/tracing/opentelemetry/OpenTelemetrySpanFactory$Builder.class uses /org/axonframework/extension/tracing/opentelemetry/OpenTelemetrySpanFactory.class, /org/axonframework/extension/tracing/opentelemetry/OpenTelemetrySpanFactory.class uses /org/axonframework/extension/t...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>96</td>
      <td>82</td>
      <td>41</td>
      <td>[/org/axonframework/common/configuration uses /org/axonframework/common, /org/axonframework/common/lifecycle uses /org/axonframework/common, /org/axonframework/common/jdbc uses /org/axonframework/common, /org/axonframework/common/digest uses /org/axonframework/common]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>2067</td>
      <td>606</td>
      <td>417</td>
      <td>[/org/axonframework/common/caching/WeakReferenceCache.class uses /org/axonframework/common/Assert.class, /org/axonframework/common/configuration/DefaultAxonApplication.class uses /org/axonframework/common/Assert.class, /org/axonframework/common/lock/PessimisticLockFactory$Builder.class uses /org...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>2019</td>
      <td>650</td>
      <td>309</td>
      <td>[/org/axonframework/messaging/eventhandling/processing/streaming/token/store/jdbc/JdbcTokenStore.class uses /org/axonframework/common/jdbc/JdbcUtils.class, /org/axonframework/messaging/eventhandling/processing/EventProcessingException.class uses /org/axonframework/common/AxonException.class, /or...</td>
    </tr>
  </tbody>
</table>
</div>


