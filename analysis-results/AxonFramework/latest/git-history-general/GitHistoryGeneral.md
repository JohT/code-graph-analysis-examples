# git log/history
<br>  

### References
- [Visualizing Code: Polyglot Notebooks Repository (YouTube)](https://youtu.be/ipOpToPS-PY?si=3doePt2cp-LgEUmt)
- [gitstractor (GitHub)](https://github.com/IntegerMan/gitstractor)
- [Neo4j Python Driver](https://neo4j.com/docs/api/python-driver/current)

    Command line execution (CLI mode): Yes






## Git History - Directory Commit Statistics

### Treemap Layout Functions and Constants

### Visualization Data Preparation Functions

### File Data Preparation Functions

### File Data Preparation 

    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.AggregationSkippedNull} {category: UNRECOGNIZED} {title: The query contains an aggregation function that skips null values.} {description: null value eliminated in set function.} {position: None} for query: "// List git files with commit statistics\n \n  MATCH (git_file:File&Git&!Repository)\n  WHERE git_file.deletedAt IS NULL // filter out deleted files\n   WITH percentileDisc(git_file.createdAtEpoch, 0.5)          AS medianCreatedAtEpoch\n       ,percentileDisc(git_file.lastModificationAtEpoch, 0.5) AS medianLastModificationAtEpoch\n       ,collect(git_file)                                     AS git_files\n UNWIND git_files AS git_file\n   WITH *\n       ,datetime.fromepochMillis(coalesce(git_file.createdAtEpoch, medianCreatedAtEpoch))                                            AS fileCreatedAtTimestamp\n       ,datetime.fromepochMillis(coalesce(git_file.lastModificationAtEpoch, git_file.createdAtEpoch, medianLastModificationAtEpoch)) AS fileLastModificationAtTimestamp\n  MATCH (git_repository:Git&Repository)-[:HAS_FILE]->(git_file)\n  MATCH (git_commit:Git&Commit)-[:CONTAINS_CHANGE]->(git_change:Git&Change)-->(old_files_included:Git&File&!Repository)-[:HAS_NEW_NAME*0..3]->(git_file)\n RETURN git_repository.name + '/' + git_file.relativePath AS filePath\n       ,split(git_commit.author, ' <')[0]                 AS author\n       ,count(DISTINCT git_commit.sha)                    AS commitCount\n       ,date(max(git_commit.date))                        AS lastCommitDate\n       ,max(date(fileCreatedAtTimestamp))                 AS lastCreationDate\n       ,max(date(fileLastModificationAtTimestamp))        AS lastModificationDate\n       ,duration.inDays(date(max(git_commit.date)), date()).days               AS daysSinceLastCommit\n       ,duration.inDays(max(fileCreatedAtTimestamp), datetime()).days          AS daysSinceLastCreation\n       ,duration.inDays(max(fileLastModificationAtTimestamp), datetime()).days AS daysSinceLastModification\n       ,max(git_commit.sha)                               AS maxCommitSha\n ORDER BY filePath ASCENDING, commitCount DESCENDING"


### Data Preview




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>fileCount</th>
      <th>authorCount</th>
      <th>commitCount</th>
      <th>daysSinceLastCommit</th>
      <th>daysSinceLastCreation</th>
      <th>daysSinceLastModification</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>305.000000</td>
      <td>305.000000</td>
      <td>305.000000</td>
      <td>305.000000</td>
      <td>305.000000</td>
      <td>305.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>14.062295</td>
      <td>7.636066</td>
      <td>348.750820</td>
      <td>412.901639</td>
      <td>651.790164</td>
      <td>583.085246</td>
    </tr>
    <tr>
      <th>std</th>
      <td>57.455641</td>
      <td>7.093502</td>
      <td>1465.259193</td>
      <td>1048.994357</td>
      <td>1222.531267</td>
      <td>1231.770321</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>1.000000</td>
      <td>3.000000</td>
      <td>24.000000</td>
      <td>18.000000</td>
      <td>55.000000</td>
      <td>17.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>4.000000</td>
      <td>6.000000</td>
      <td>75.000000</td>
      <td>42.000000</td>
      <td>262.000000</td>
      <td>104.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>8.000000</td>
      <td>8.000000</td>
      <td>187.000000</td>
      <td>250.000000</td>
      <td>347.000000</td>
      <td>292.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>904.000000</td>
      <td>71.000000</td>
      <td>22225.000000</td>
      <td>4791.000000</td>
      <td>4879.000000</td>
      <td>4790.000000</td>
    </tr>
  </tbody>
</table>
</div>






<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>directoryPath</th>
      <th>directoryParentPath</th>
      <th>directoryName</th>
      <th>fileCount</th>
      <th>firstFile</th>
      <th>mostFrequentFileExtension</th>
      <th>authorCount</th>
      <th>mainAuthor</th>
      <th>secondAuthor</th>
      <th>commitCount</th>
      <th>daysSinceLastCommit</th>
      <th>daysSinceLastCreation</th>
      <th>daysSinceLastModification</th>
      <th>lastCommitDate</th>
      <th>lastCreationDate</th>
      <th>lastModificationDate</th>
      <th>maxCommitSha</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AxonFramework-4.11.1/.idea/copyright</td>
      <td>AxonFramework-4.11.1/.idea</td>
      <td>copyright</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/.idea/copyright/Axon_Framework_copyright_template.xml</td>
      <td>xml</td>
      <td>2</td>
      <td>Steven van Beelen</td>
      <td>Allard Buijze</td>
      <td>9</td>
      <td>42</td>
      <td>87</td>
      <td>87</td>
      <td>2025-02-24</td>
      <td>2025-01-09</td>
      <td>2025-01-09</td>
      <td>fe926a4970bdf1e538e8e7fb8d147ffdc676e713</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AxonFramework-4.11.1/.idea/inspectionProfiles</td>
      <td>AxonFramework-4.11.1/.idea</td>
      <td>inspectionProfiles</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/.idea/inspectionProfiles/Project_Default.xml</td>
      <td>xml</td>
      <td>3</td>
      <td>Steven van Beelen</td>
      <td>Allard Buijze</td>
      <td>13</td>
      <td>3</td>
      <td>87</td>
      <td>2</td>
      <td>2025-04-04</td>
      <td>2025-01-09</td>
      <td>2025-04-04</td>
      <td>fe926a4970bdf1e538e8e7fb8d147ffdc676e713</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AxonFramework-4.11.1/axon-5-module-structure-suggestion/messaging-core/src/test/java/org/axonframework/messaging</td>
      <td>AxonFramework-4.11.1/axon-5-module-structure-suggestion/messaging-core/src</td>
      <td>test/java/org/axonframework/messaging</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/axon-5-module-structure-suggestion/messaging-core/src/test/java/org/axonframework/messaging/UnitOfWorkTest.java</td>
      <td>java</td>
      <td>2</td>
      <td>Steven van Beelen</td>
      <td>Mitchell Herrijgers</td>
      <td>13</td>
      <td>42</td>
      <td>527</td>
      <td>527</td>
      <td>2025-02-24</td>
      <td>2023-10-27</td>
      <td>2023-10-27</td>
      <td>ea5ee757f6536e2b4f6f5d0cac71a07b94c4c0c4</td>
    </tr>
    <tr>
      <th>3</th>
      <td>AxonFramework-4.11.1/axon-server-connector/src/main/java/org/axonframework/axonserver/connector/command</td>
      <td>AxonFramework-4.11.1/axon-server-connector/src/main/java/org/axonframework/axonserver/connector</td>
      <td>command</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/axon-server-connector/src/main/java/org/axonframework/axonserver/connector/command/AxonServerConnector.java</td>
      <td>java</td>
      <td>4</td>
      <td>Steven van Beelen</td>
      <td>Allard Buijze</td>
      <td>43</td>
      <td>0</td>
      <td>383</td>
      <td>0</td>
      <td>2025-04-07</td>
      <td>2024-03-19</td>
      <td>2025-04-07</td>
      <td>fcedac961db62285c0c224c507284ef1746d5f35</td>
    </tr>
    <tr>
      <th>4</th>
      <td>AxonFramework-4.11.1/core/src/test/java/org/axonframework/commandhandling/disruptor</td>
      <td>AxonFramework-4.11.1/core/src/test/java/org/axonframework</td>
      <td>commandhandling/disruptor</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/core/src/test/java/org/axonframework/commandhandling/disruptor/EventPublisherTest.java</td>
      <td>java</td>
      <td>2</td>
      <td>Allard Buijze</td>
      <td>Rene de Waele</td>
      <td>2</td>
      <td>3469</td>
      <td>3491</td>
      <td>3468</td>
      <td>2015-10-08</td>
      <td>2015-09-15</td>
      <td>2015-10-08</td>
      <td>30d68fd229c59f5aa8f45848de82c91967eebcba</td>
    </tr>
    <tr>
      <th>5</th>
      <td>AxonFramework-4.11.1/core/src/test/java/org/axonframework/contextsupport/spring</td>
      <td>AxonFramework-4.11.1/core/src/test/java/org/axonframework</td>
      <td>contextsupport/spring</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/core/src/test/java/org/axonframework/contextsupport/spring/WiringTest.java</td>
      <td>java</td>
      <td>2</td>
      <td>Sebastian Ganslandt</td>
      <td>lburgazzoli</td>
      <td>2</td>
      <td>4234</td>
      <td>4328</td>
      <td>4328</td>
      <td>2013-09-03</td>
      <td>2013-05-31</td>
      <td>2013-05-31</td>
      <td>f17a45795111f567ca57f97c63a976c1a9a2cce0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>AxonFramework-4.11.1/core/src/test/java/org/axonframework/eventhandling/scheduling/quartz</td>
      <td>AxonFramework-4.11.1/core/src/test/java/org/axonframework</td>
      <td>eventhandling/scheduling/quartz</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/core/src/test/java/org/axonframework/eventhandling/scheduling/quartz/Quartz2EventSchedulerTest.java</td>
      <td>java</td>
      <td>14</td>
      <td>Allard Buijze</td>
      <td>smcvb</td>
      <td>121</td>
      <td>251</td>
      <td>4673</td>
      <td>4673</td>
      <td>2024-07-30</td>
      <td>2012-06-20</td>
      <td>2012-06-20</td>
      <td>fdd51aa788071375721c67bb30bf5709136e974a</td>
    </tr>
    <tr>
      <th>7</th>
      <td>AxonFramework-4.11.1/docs/_playbook/localLinks</td>
      <td>AxonFramework-4.11.1/docs/_playbook</td>
      <td>localLinks</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_playbook/localLinks/axoniq-library-ui</td>
      <td>axoniq-library-ui</td>
      <td>7</td>
      <td>Steven van Beelen</td>
      <td>Allard Buijze</td>
      <td>13</td>
      <td>250</td>
      <td>303</td>
      <td>303</td>
      <td>2024-07-31</td>
      <td>2024-06-07</td>
      <td>2024-06-07</td>
      <td>fcf55fb4f72d050c0949cac6a1818df2cd53d608</td>
    </tr>
    <tr>
      <th>8</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/ROOT/attachments</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/ROOT</td>
      <td>attachments</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/ROOT/attachments/axonframework_overview.gv</td>
      <td>gv</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>22</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>9</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/ROOT/partials</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/ROOT</td>
      <td>partials</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/ROOT/partials/nav.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>22</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>10</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/axon-server-connector/pages</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/axon-server-connector</td>
      <td>pages</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/axon-server-connector/pages/index.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>23</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>11</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/axon-server-connector/partials</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/axon-server-connector</td>
      <td>partials</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/axon-server-connector/partials/nav.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>22</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>12</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/configuration/pages</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/configuration</td>
      <td>pages</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/configuration/pages/index.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>23</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>13</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/configuration/partials</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/configuration</td>
      <td>partials</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/configuration/partials/nav.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>22</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>14</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/disruptor/pages</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/disruptor</td>
      <td>pages</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/disruptor/pages/index.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>23</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>15</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/disruptor/partials</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/disruptor</td>
      <td>partials</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/disruptor/partials/nav.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>22</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>16</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/eventsourcing/pages</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/eventsourcing</td>
      <td>pages</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/eventsourcing/pages/index.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>24</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>17</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/eventsourcing/partials</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/eventsourcing</td>
      <td>partials</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/eventsourcing/partials/nav.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>22</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>18</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/legacy/pages</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/legacy</td>
      <td>pages</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/legacy/pages/index.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>23</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>19</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/legacy/partials</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/legacy</td>
      <td>partials</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/legacy/partials/nav.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>22</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>20</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/metrics/pages</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/metrics</td>
      <td>pages</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/metrics/pages/index.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>23</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>21</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/metrics/partials</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/metrics</td>
      <td>partials</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/metrics/partials/nav.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>22</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>22</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/micrometer/pages</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/micrometer</td>
      <td>pages</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/micrometer/pages/index.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>23</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>23</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/micrometer/partials</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/micrometer</td>
      <td>partials</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/micrometer/partials/nav.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>22</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>24</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/modeling/partials</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/modeling</td>
      <td>partials</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/modeling/partials/nav.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>22</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>25</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/spring/pages</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/spring</td>
      <td>pages</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/spring/pages/index.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>23</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>26</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/spring/partials</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/spring</td>
      <td>partials</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/spring/partials/nav.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>22</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>27</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/springboot-starter/pages</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/springboot-starter</td>
      <td>pages</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/springboot-starter/pages/index.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>24</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>28</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/springboot-starter/partials</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/springboot-starter</td>
      <td>partials</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/springboot-starter/partials/nav.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>22</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
    <tr>
      <th>29</th>
      <td>AxonFramework-4.11.1/docs/_reference/modules/test/pages</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/test</td>
      <td>pages</td>
      <td>1</td>
      <td>AxonFramework-4.11.1/docs/_reference/modules/test/pages/index.adoc</td>
      <td>adoc</td>
      <td>8</td>
      <td>Steven van Beelen</td>
      <td>Milen Dyankov</td>
      <td>23</td>
      <td>250</td>
      <td>292</td>
      <td>292</td>
      <td>2024-07-31</td>
      <td>2024-06-19</td>
      <td>2024-06-19</td>
      <td>f851948ee70e6cc9742c7b1bde5941ed2655e28f</td>
    </tr>
  </tbody>
</table>
</div>



### Number of files per directory


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_26_0.svg)
    


### Most frequent file extension per directory


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_28_0.svg)
    


### Number of commits per directory


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_30_0.svg)
    


### Number of distinct authors per directory


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_32_0.svg)
    


### Main author per directory


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_34_0.svg)
    


### Second author per directory


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_36_0.svg)
    


### Days since last commit per directory


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_38_0.svg)
    


### Days since last commit per directory (ranked)


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_40_0.svg)
    


### Days since last file creation per directory


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_42_0.svg)
    


### Days since last file creation per directory (ranked)


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_44_0.svg)
    


### Days since last file modification per directory


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_46_0.svg)
    


### Days since last file modification per directory (ranked)


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_48_0.svg)
    


## Filecount per commit

Shows how many commits had changed one file, how many had changed two files, and so on.
The chart is limited to 30 lines for improved readability.
The data preview also includes overall statistics including the number of commits that are filtered out in the chart.

### Preview data

    Sum of commits that changed more than 30 files (each) = 1181
    Max changed files with one commit = 4041



<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>filesPerCommit</th>
      <th>commitCount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>377.000000</td>
      <td>377.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>398.572944</td>
      <td>35.607427</td>
    </tr>
    <tr>
      <th>std</th>
      <td>559.546155</td>
      <td>302.200493</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>95.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>204.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>429.000000</td>
      <td>5.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>4041.000000</td>
      <td>5249.000000</td>
    </tr>
  </tbody>
</table>
</div>



<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>filesPerCommit</th>
      <th>commitCount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>5249</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>2251</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1059</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>664</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>449</td>
    </tr>
    <tr>
      <th>5</th>
      <td>6</td>
      <td>329</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7</td>
      <td>267</td>
    </tr>
    <tr>
      <th>7</th>
      <td>8</td>
      <td>218</td>
    </tr>
    <tr>
      <th>8</th>
      <td>9</td>
      <td>163</td>
    </tr>
    <tr>
      <th>9</th>
      <td>10</td>
      <td>147</td>
    </tr>
    <tr>
      <th>10</th>
      <td>11</td>
      <td>110</td>
    </tr>
    <tr>
      <th>11</th>
      <td>12</td>
      <td>105</td>
    </tr>
    <tr>
      <th>12</th>
      <td>13</td>
      <td>127</td>
    </tr>
    <tr>
      <th>13</th>
      <td>14</td>
      <td>170</td>
    </tr>
    <tr>
      <th>14</th>
      <td>15</td>
      <td>189</td>
    </tr>
    <tr>
      <th>15</th>
      <td>16</td>
      <td>78</td>
    </tr>
    <tr>
      <th>16</th>
      <td>17</td>
      <td>71</td>
    </tr>
    <tr>
      <th>17</th>
      <td>18</td>
      <td>61</td>
    </tr>
    <tr>
      <th>18</th>
      <td>19</td>
      <td>83</td>
    </tr>
    <tr>
      <th>19</th>
      <td>20</td>
      <td>74</td>
    </tr>
    <tr>
      <th>20</th>
      <td>21</td>
      <td>46</td>
    </tr>
    <tr>
      <th>21</th>
      <td>22</td>
      <td>68</td>
    </tr>
    <tr>
      <th>22</th>
      <td>23</td>
      <td>34</td>
    </tr>
    <tr>
      <th>23</th>
      <td>24</td>
      <td>38</td>
    </tr>
    <tr>
      <th>24</th>
      <td>25</td>
      <td>43</td>
    </tr>
    <tr>
      <th>25</th>
      <td>26</td>
      <td>33</td>
    </tr>
    <tr>
      <th>26</th>
      <td>27</td>
      <td>34</td>
    </tr>
    <tr>
      <th>27</th>
      <td>28</td>
      <td>30</td>
    </tr>
    <tr>
      <th>28</th>
      <td>29</td>
      <td>29</td>
    </tr>
    <tr>
      <th>29</th>
      <td>30</td>
      <td>24</td>
    </tr>
  </tbody>
</table>
</div>


### Bar chart with the number of files per commit distribution


    
![svg](GitHistoryGeneral_files/GitHistoryGeneral_53_0.svg)
    


## WordCloud of git authors




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>word</th>
      <th>frequency</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Steven van Beelen</td>
      <td>4357</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Allard Buijze</td>
      <td>3156</td>
    </tr>
    <tr>
      <th>2</th>
      <td>smcvb</td>
      <td>822</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Mateusz Nowak</td>
      <td>506</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Milan Savic</td>
      <td>449</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Mitchell Herrijgers</td>
      <td>438</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Gerard Klijs</td>
      <td>247</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Marc Gathier</td>
      <td>231</td>
    </tr>
    <tr>
      <th>8</th>
      <td>sara pellegrini</td>
      <td>163</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Rene de Waele</td>
      <td>129</td>
    </tr>
  </tbody>
</table>
</div>




    
![png](GitHistoryGeneral_files/GitHistoryGeneral_56_0.png)
    

