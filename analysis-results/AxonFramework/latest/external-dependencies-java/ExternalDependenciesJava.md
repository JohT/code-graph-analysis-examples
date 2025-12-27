# External Dependencies for Java
<br>  

### References
- [jqassistant](https://jqassistant.org)
- [Neo4j Python Driver](https://neo4j.com/docs/api/python-driver/current)





## External Package Usage

### External Package

An external type has no `byteCodeVersion` since it only occurs as a dependency but wasn't analyzed itself (missing bytecode). Core Java types like `java.lang.Integer` and primitives like `int` are considered "build-in" and therefore aren't interpreted as "external" even though their byte code is also missing. A package is categorized as "external" if the types it contains are classified as external.

### External annotation dependency

The aforementioned classification encompasses external annotation dependencies as well. These dependencies introduce significantly less coupling and are not indispensable for compiling code. Without the external annotation the code would most probably behave differently. Hence, they are included in the first more overall and general tables and then left out in the later more specific ones.

### Table 1 - Top 20 most used external packages overall

This table shows the external packages that are used by the most different internal types overall.
Additionally, it shows which types of the external package are actually used. External annotations are also listed.

Only the top 20 entries are shown. The whole table can be found in the following CSV report:
`External_package_usage_overall`

**Columns:**
- *externalPackageName* identifies the external package as described above
- *numberOfExternalCallerPackages* refers to the distinct packages that make use of the external package
- *numberOfExternalCallerTypes* refers to the distinct types that make use of the external package
- *numberOfExternalTypeCalls* includes every dependency to the types in the external package
- *numberOfExternalTypeCallsWeighted* includes every invocation or reference (sum of weights) to the types in the external package
- *allPackages* contains the total count of all analyzed packages in general
- *allTypes* contains the total count of all analyzed types in general
- *externalTypeNames* contains a list of actually utilized types of the external package




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalPackageName</th>
      <th>numberOfExternalCallerPackages</th>
      <th>numberOfExternalCallerTypes</th>
      <th>numberOfExternalTypeCalls</th>
      <th>numberOfExternalTypeCallsWeighted</th>
      <th>allPackages</th>
      <th>allTypes</th>
      <th>tenExternalTypeNames</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>jakarta.annotation</td>
      <td>98</td>
      <td>672</td>
      <td>859</td>
      <td>4788</td>
      <td>113</td>
      <td>1199</td>
      <td>[Nonnull, Nullable]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.slf4j</td>
      <td>38</td>
      <td>74</td>
      <td>133</td>
      <td>456</td>
      <td>113</td>
      <td>1199</td>
      <td>[Logger, LoggerFactory]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>io.axoniq.axonserver.connector</td>
      <td>5</td>
      <td>16</td>
      <td>23</td>
      <td>124</td>
      <td>113</td>
      <td>1199</td>
      <td>[AxonServerConnection, AxonServerConnectionFac...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>io.axoniq.axonserver.grpc</td>
      <td>5</td>
      <td>18</td>
      <td>40</td>
      <td>271</td>
      <td>113</td>
      <td>1199</td>
      <td>[ErrorMessage, ErrorMessage$Builder, Instructi...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>jakarta.persistence</td>
      <td>5</td>
      <td>13</td>
      <td>33</td>
      <td>129</td>
      <td>113</td>
      <td>1199</td>
      <td>[EntityManager, Lob, Index, SequenceGenerator,...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>reactor.core.publisher</td>
      <td>5</td>
      <td>8</td>
      <td>14</td>
      <td>49</td>
      <td>113</td>
      <td>1199</td>
      <td>[MonoSink, Flux, Mono, FluxSink]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>com.fasterxml.jackson.annotation</td>
      <td>3</td>
      <td>6</td>
      <td>18</td>
      <td>34</td>
      <td>113</td>
      <td>1199</td>
      <td>[JsonProperty, JsonCreator, JsonGetter, JsonIg...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>com.fasterxml.jackson.databind</td>
      <td>3</td>
      <td>9</td>
      <td>14</td>
      <td>67</td>
      <td>113</td>
      <td>1199</td>
      <td>[JsonNode, SerializationFeature, ObjectMapper,...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>io.grpc</td>
      <td>3</td>
      <td>7</td>
      <td>23</td>
      <td>51</td>
      <td>113</td>
      <td>1199</td>
      <td>[ManagedChannelBuilder, ClientInterceptor, Cli...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>org.hamcrest</td>
      <td>3</td>
      <td>22</td>
      <td>44</td>
      <td>194</td>
      <td>113</td>
      <td>1199</td>
      <td>[Matcher, StringDescription, Description, Core...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>org.reactivestreams</td>
      <td>3</td>
      <td>6</td>
      <td>8</td>
      <td>27</td>
      <td>113</td>
      <td>1199</td>
      <td>[Publisher, Subscription, Subscriber]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>org.springframework.boot.actuate.health</td>
      <td>3</td>
      <td>4</td>
      <td>7</td>
      <td>24</td>
      <td>113</td>
      <td>1199</td>
      <td>[Status, Health$Builder, AbstractHealthIndicat...</td>
    </tr>
    <tr>
      <th>12</th>
      <td>com.fasterxml.jackson.databind.node</td>
      <td>2</td>
      <td>3</td>
      <td>5</td>
      <td>28</td>
      <td>113</td>
      <td>1199</td>
      <td>[ArrayNode, ObjectNode, JsonNodeType]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>io.axoniq.axonserver.grpc.control</td>
      <td>2</td>
      <td>6</td>
      <td>13</td>
      <td>86</td>
      <td>113</td>
      <td>1199</td>
      <td>[TopologyChange, QuerySubscription, CommandSub...</td>
    </tr>
    <tr>
      <th>14</th>
      <td>io.grpc.stub</td>
      <td>2</td>
      <td>3</td>
      <td>4</td>
      <td>11</td>
      <td>113</td>
      <td>1199</td>
      <td>[StreamObserver, ClientCallStreamObserver, Cli...</td>
    </tr>
    <tr>
      <th>15</th>
      <td>io.micrometer.core.instrument</td>
      <td>2</td>
      <td>12</td>
      <td>38</td>
      <td>140</td>
      <td>113</td>
      <td>1199</td>
      <td>[MeterRegistry, Tags, Clock, Tag, Timer$Builde...</td>
    </tr>
    <tr>
      <th>16</th>
      <td>org.apache.avro</td>
      <td>2</td>
      <td>5</td>
      <td>17</td>
      <td>56</td>
      <td>113</td>
      <td>1199</td>
      <td>[Schema, AvroRuntimeException, SchemaCompatibi...</td>
    </tr>
    <tr>
      <th>17</th>
      <td>org.apache.avro.message</td>
      <td>2</td>
      <td>9</td>
      <td>12</td>
      <td>38</td>
      <td>113</td>
      <td>1199</td>
      <td>[SchemaStore$Cache, SchemaStore, BinaryMessage...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>org.axonframework.extension.spring.config</td>
      <td>2</td>
      <td>4</td>
      <td>9</td>
      <td>35</td>
      <td>113</td>
      <td>1199</td>
      <td>[EventProcessorSettings$SubscribingEventProces...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>org.springframework.boot.autoconfigure</td>
      <td>2</td>
      <td>19</td>
      <td>29</td>
      <td>30</td>
      <td>113</td>
      <td>1199</td>
      <td>[AutoConfiguration, AutoConfigureBefore, AutoC...</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 1 Chart 1a - Most called external packages in % by types (more than 0.7% overall)

External packages that are used less than 0.7% are grouped into the name "others" to get a cleaner chart
with the most significant external packages and how ofter they are called in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_15_1.png)
    


#### Table 1 Chart 1b - Most called external packages in % by types (less than 0.7% overall "others" drill-down)

Shows the lowest (less than 0.7% overall) most called external package. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_17_1.png)
    


#### Table 1 Chart 2a - Most called external packages in % by packages (more than 0.7% overall)

External packages that are used less than 0.7% are grouped into the name "others" to get a cleaner chart
with the most significant external packages and how ofter they are called in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_19_1.png)
    


#### Table 1 Chart 2b - Most called external packages in % by packages (less than 0.7% overall "others" drill-down)

Shows the lowest (less than 0.7% overall) most called external package. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_21_1.png)
    


### Table 2 - Top 20 most used external packages grouped by their first 2 layers

This table shows external packages grouped by their first 2 layers that are used by the most different internal types overall including external annotations. For example, "javax.xml.stream" and "javax.xml.parsers" are grouped together to "javax.xml".

Additionally, it shows which types of the external packages are actually used.

Only the top 20 entries are shown. The whole table can be found in the following CSV report:
`External_second_level_package_usage_overall`

**Columns:**
- *externalSecondLevelPackageName* identifies the first 2 levels of the external package as described above
- *numberOfExternalCallerPackages* refers to the distinct packages that make use of the external package
- *numberOfExternalCallerTypes* refers to the distinct types that make use of the external package
- *numberOfExternalTypeCalls* includes every dependency to the types in the external package
- *numberOfExternalTypeCallsWeighted* includes every invocation or reference (sum of weights) to the types in the external package
- *allPackages* contains the total count of all analyzed packages in general
- *allTypes* contains the total count of all analyzed types in general
- *externalTypeNames* contains a list of actually utilized types of the external package




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalSecondLevelPackageName</th>
      <th>numberOfExternalCallerPackages</th>
      <th>numberOfExternalCallerTypes</th>
      <th>numberOfExternalTypeCalls</th>
      <th>numberOfExternalTypeCallsWeighted</th>
      <th>allPackages</th>
      <th>allTypes</th>
      <th>tenExternalTypeNames</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>jakarta.annotation</td>
      <td>98</td>
      <td>672</td>
      <td>859</td>
      <td>4788</td>
      <td>113</td>
      <td>1199</td>
      <td>[Nonnull, Nullable]</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.slf4j</td>
      <td>38</td>
      <td>74</td>
      <td>133</td>
      <td>456</td>
      <td>113</td>
      <td>1199</td>
      <td>[Logger, LoggerFactory]</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.springframework</td>
      <td>7</td>
      <td>55</td>
      <td>173</td>
      <td>293</td>
      <td>113</td>
      <td>1199</td>
      <td>[ConfigurationProperties, NestedConfigurationP...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>com.fasterxml</td>
      <td>6</td>
      <td>16</td>
      <td>40</td>
      <td>138</td>
      <td>113</td>
      <td>1199</td>
      <td>[JsonNode, SerializationFeature, ArrayNode, Ob...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>io.axoniq</td>
      <td>6</td>
      <td>45</td>
      <td>153</td>
      <td>849</td>
      <td>113</td>
      <td>1199</td>
      <td>[TopologyChange, QuerySubscription, CommandSub...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>reactor.core</td>
      <td>6</td>
      <td>9</td>
      <td>16</td>
      <td>51</td>
      <td>113</td>
      <td>1199</td>
      <td>[Scheduler, Schedulers, MonoSink, Flux, Mono, ...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>com.google</td>
      <td>5</td>
      <td>9</td>
      <td>12</td>
      <td>36</td>
      <td>113</td>
      <td>1199</td>
      <td>[MessageLite, ByteString, JsonElement, JsonPar...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>jakarta.persistence</td>
      <td>5</td>
      <td>13</td>
      <td>33</td>
      <td>129</td>
      <td>113</td>
      <td>1199</td>
      <td>[EntityManager, Lob, Index, SequenceGenerator,...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>io.grpc</td>
      <td>3</td>
      <td>10</td>
      <td>29</td>
      <td>65</td>
      <td>113</td>
      <td>1199</td>
      <td>[ManagedChannelBuilder, GrpcSslContexts, SslCo...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>org.axonframework</td>
      <td>3</td>
      <td>8</td>
      <td>15</td>
      <td>48</td>
      <td>113</td>
      <td>1199</td>
      <td>[EventProcessorSettings$SubscribingEventProces...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>org.hamcrest</td>
      <td>3</td>
      <td>22</td>
      <td>44</td>
      <td>194</td>
      <td>113</td>
      <td>1199</td>
      <td>[Matcher, StringDescription, Description, Core...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>org.reactivestreams</td>
      <td>3</td>
      <td>6</td>
      <td>8</td>
      <td>27</td>
      <td>113</td>
      <td>1199</td>
      <td>[Publisher, Subscription, Subscriber]</td>
    </tr>
    <tr>
      <th>12</th>
      <td>io.micrometer</td>
      <td>2</td>
      <td>12</td>
      <td>39</td>
      <td>142</td>
      <td>113</td>
      <td>1199</td>
      <td>[MeterRegistry, Tags, Clock, Tag, Timer$Builde...</td>
    </tr>
    <tr>
      <th>13</th>
      <td>org.apache</td>
      <td>2</td>
      <td>12</td>
      <td>42</td>
      <td>145</td>
      <td>113</td>
      <td>1199</td>
      <td>[Schema, SchemaStore$Cache, SchemaStore, Gener...</td>
    </tr>
    <tr>
      <th>14</th>
      <td>io.opentelemetry</td>
      <td>1</td>
      <td>5</td>
      <td>21</td>
      <td>70</td>
      <td>113</td>
      <td>1199</td>
      <td>[TextMapSetter, Span, Scope, StatusCode, SpanC...</td>
    </tr>
    <tr>
      <th>15</th>
      <td>jakarta.validation</td>
      <td>1</td>
      <td>2</td>
      <td>5</td>
      <td>16</td>
      <td>113</td>
      <td>1199</td>
      <td>[ConstraintViolation, ValidatorFactory, Valida...</td>
    </tr>
    <tr>
      <th>16</th>
      <td>javax.cache</td>
      <td>1</td>
      <td>2</td>
      <td>12</td>
      <td>48</td>
      <td>113</td>
      <td>1199</td>
      <td>[Cache, CacheEntryListenerConfiguration, Cache...</td>
    </tr>
    <tr>
      <th>17</th>
      <td>org.awaitility</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>113</td>
      <td>1199</td>
      <td>[Awaitility, ConditionFactory]</td>
    </tr>
    <tr>
      <th>18</th>
      <td>org.ehcache</td>
      <td>1</td>
      <td>3</td>
      <td>10</td>
      <td>45</td>
      <td>113</td>
      <td>1199</td>
      <td>[EventType, Ehcache, EventOrdering, CacheRunti...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>org.testcontainers</td>
      <td>1</td>
      <td>1</td>
      <td>6</td>
      <td>19</td>
      <td>113</td>
      <td>1199</td>
      <td>[GenericContainer, MountableFile, HttpWaitStra...</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 2 Chart 1a - Most called second level external packages in % by type

External package groups that are used less than 0.7% are grouped into the name "others" to get a cleaner chart
with the most significant external packages and how ofter they are called in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_25_1.png)
    


#### Table 2 Chart 1b - Most called second level external packages in % by type (less than 0.7% overall "others" drill-down)

Shows the lowest (less than 0.7% overall) most called external package. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_27_1.png)
    


#### Table 2 Chart 2a - Most called second level external packages in % by package (more than 0.7% overall)

External package groups that are used less than 0.7% are grouped into the name "others" to get a cleaner chart
with the most significant external packages and how ofter they are called in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_29_1.png)
    


#### Table 2 Chart 2b - Most called second level external packages in % by package (less than 0.7% overall "others" drill-down)

Shows the lowest (less than 0.7% overall) most called external package. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_31_1.png)
    


### Table 3 - Top 20 most widely spread external packages

The following tables shows external packages that are used by many different artifacts with the highest number of artifacts first. External annotations are filtered out to only get those external packages that significantly add to coupling.

Statistics like minimum, maximum, average, median and standard deviation are provided for the number of packages and number of types in every artifact that uses the listed external package. 

The intuition behind that is to find external package dependencies that are used in a widely spread manner. This should uncover libraries and frameworks and make it easier to distinguish them from external dependencies that are used for specific tasks. It can also be used to find external dependencies that are used sparsely regarding artifacts but are used in many different packages there. This could then be improved by applying a [Hexagonal architecture](https://alistair.cockburn.us/hexagonal-architecture).

Only the top 20 entries are shown. The whole table can be found in the following CSV report:
`External_package_usage_spread`

**Columns:**
- *externalPackageName* identifies the external package as defined above. All other columns contain aggregated data for this external package.
- *numberOfArtifacts* contains the number of artifacts that use the external package
- *sumNumberOfPackages* contains the sum of all packages that use the external package
- *min/max/med/avg/stdNumberOfPackages* provide statistics based on the number of packages of each artifact that uses the external package
- *min/max/med/avg/stdNumberOfPackagesPercentage* provide statistics in percent (%) based on the number of packages of each artifact that uses the external package
- *min/max/med/avg/stdNumberOfTypes* provide statistics based on the number of types of each artifact that uses the external package
- *min/max/med/avg/stdNumberOfPackagesPercentage* provide statistics in percent (%) based on the number of types of each artifact that uses the external package
- *someArtifactNames* contain some of the artifacts that contain the external package for reference




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalPackageName</th>
      <th>numberOfArtifacts</th>
      <th>sumNumberOfPackages</th>
      <th>minNumberOfPackages</th>
      <th>maxNumberOfPackages</th>
      <th>medNumberOfPackages</th>
      <th>avgNumberOfPackages</th>
      <th>stdNumberOfPackages</th>
      <th>minNumberOfPackagesPercentage</th>
      <th>maxNumberOfPackagesPercentage</th>
      <th>...</th>
      <th>maxNumberOfTypes</th>
      <th>medNumberOfTypes</th>
      <th>avgNumberOfTypes</th>
      <th>stdNumberOfTypes</th>
      <th>minNumberOfTypesPercentage</th>
      <th>maxNumberOfTypesPercentage</th>
      <th>medNumberOfTypesPercentage</th>
      <th>avgNumberOfTypesPercentage</th>
      <th>stdNumberOfTypesPercentage</th>
      <th>someArtifactNames</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.slf4j</td>
      <td>11</td>
      <td>38</td>
      <td>1</td>
      <td>14</td>
      <td>3.0</td>
      <td>3.454545</td>
      <td>3.670521</td>
      <td>20.000000</td>
      <td>100.000000</td>
      <td>...</td>
      <td>30</td>
      <td>3.0</td>
      <td>6.727273</td>
      <td>8.486353</td>
      <td>1.369863</td>
      <td>30.434783</td>
      <td>6.000000</td>
      <td>9.894824</td>
      <td>8.937748</td>
      <td>[axon-tracing-opentelemetry-5.0.1, axon-common...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>jakarta.persistence</td>
      <td>4</td>
      <td>5</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.250000</td>
      <td>0.500000</td>
      <td>1.754386</td>
      <td>28.571429</td>
      <td>...</td>
      <td>4</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>1.154701</td>
      <td>0.350877</td>
      <td>5.714286</td>
      <td>2.666667</td>
      <td>2.849624</td>
      <td>2.454419</td>
      <td>[axon-common-5.0.1, axon-eventsourcing-5.0.1, ...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>com.fasterxml.jackson.databind</td>
      <td>3</td>
      <td>3</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>7.692308</td>
      <td>25.000000</td>
      <td>...</td>
      <td>5</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>2.000000</td>
      <td>0.666667</td>
      <td>16.666667</td>
      <td>4.285714</td>
      <td>7.206349</td>
      <td>8.390327</td>
      <td>[axon-common-5.0.1, axon-spring-boot-autoconfi...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>com.fasterxml.jackson.databind.node</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>7.692308</td>
      <td>25.000000</td>
      <td>...</td>
      <td>2</td>
      <td>1.5</td>
      <td>1.500000</td>
      <td>0.707107</td>
      <td>0.666667</td>
      <td>6.666667</td>
      <td>3.666667</td>
      <td>3.666667</td>
      <td>4.242641</td>
      <td>[axon-common-5.0.1, axon-conversion-5.0.1]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>io.axoniq.axonserver.connector</td>
      <td>2</td>
      <td>5</td>
      <td>1</td>
      <td>4</td>
      <td>2.5</td>
      <td>2.500000</td>
      <td>2.121320</td>
      <td>14.285714</td>
      <td>80.000000</td>
      <td>...</td>
      <td>15</td>
      <td>8.0</td>
      <td>8.000000</td>
      <td>9.899495</td>
      <td>1.428571</td>
      <td>20.833333</td>
      <td>11.130952</td>
      <td>11.130952</td>
      <td>13.721239</td>
      <td>[axon-server-connector-5.0.1, axon-spring-boot...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>io.axoniq.axonserver.connector.control</td>
      <td>2</td>
      <td>3</td>
      <td>1</td>
      <td>2</td>
      <td>1.5</td>
      <td>1.500000</td>
      <td>0.707107</td>
      <td>14.285714</td>
      <td>40.000000</td>
      <td>...</td>
      <td>4</td>
      <td>2.5</td>
      <td>2.500000</td>
      <td>2.121320</td>
      <td>1.428571</td>
      <td>5.555556</td>
      <td>3.492063</td>
      <td>3.492063</td>
      <td>2.918218</td>
      <td>[axon-server-connector-5.0.1, axon-spring-boot...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>org.apache.avro</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>14.285714</td>
      <td>25.000000</td>
      <td>...</td>
      <td>4</td>
      <td>2.5</td>
      <td>2.500000</td>
      <td>2.121320</td>
      <td>1.428571</td>
      <td>13.333333</td>
      <td>7.380952</td>
      <td>7.380952</td>
      <td>8.417938</td>
      <td>[axon-spring-boot-autoconfigure-5.0.1, axon-co...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>org.apache.avro.message</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>14.285714</td>
      <td>25.000000</td>
      <td>...</td>
      <td>6</td>
      <td>4.5</td>
      <td>4.500000</td>
      <td>2.121320</td>
      <td>4.285714</td>
      <td>20.000000</td>
      <td>12.142857</td>
      <td>12.142857</td>
      <td>11.111678</td>
      <td>[axon-spring-boot-autoconfigure-5.0.1, axon-co...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>IdTypeParameterResolver</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>...</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>[axon-eventsourcing-5.0.1]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ScannedEntityCreator</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>...</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>[axon-eventsourcing-5.0.1]</td>
    </tr>
  </tbody>
</table>
<p>10 rows × 25 columns</p>
</div>



### Table 3a - Top 20 most widely spread external packages - number of internal packages

This table shows the top 20 most widely spread external packages focussing on the spread across the number of internal packages.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalPackageName</th>
      <th>numberOfArtifacts</th>
      <th>minNumberOfPackages</th>
      <th>maxNumberOfPackages</th>
      <th>medNumberOfPackages</th>
      <th>avgNumberOfPackages</th>
      <th>stdNumberOfPackages</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.slf4j</td>
      <td>11</td>
      <td>1</td>
      <td>14</td>
      <td>3.0</td>
      <td>3.454545</td>
      <td>3.670521</td>
    </tr>
    <tr>
      <th>1</th>
      <td>jakarta.persistence</td>
      <td>4</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.250000</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>com.fasterxml.jackson.databind</td>
      <td>3</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>com.fasterxml.jackson.databind.node</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>io.axoniq.axonserver.connector</td>
      <td>2</td>
      <td>1</td>
      <td>4</td>
      <td>2.5</td>
      <td>2.500000</td>
      <td>2.121320</td>
    </tr>
    <tr>
      <th>5</th>
      <td>io.axoniq.axonserver.connector.control</td>
      <td>2</td>
      <td>1</td>
      <td>2</td>
      <td>1.5</td>
      <td>1.500000</td>
      <td>0.707107</td>
    </tr>
    <tr>
      <th>6</th>
      <td>org.apache.avro</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>org.apache.avro.message</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>IdTypeParameterResolver</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ScannedEntityCreator</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>WrappedEventCriteriaBuilderMethod</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>com.fasterxml.jackson.annotation</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>com.fasterxml.jackson.core</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>com.fasterxml.jackson.dataformat.cbor.databind</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>com.google.gson</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>com.google.protobuf</td>
      <td>1</td>
      <td>4</td>
      <td>4</td>
      <td>4.0</td>
      <td>4.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>io.axoniq.axonserver.connector.admin</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>io.axoniq.axonserver.connector.command</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>io.axoniq.axonserver.connector.event</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>io.axoniq.axonserver.connector.impl</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
  </tbody>
</table>
</div>



### Table 3b - Top 20 most widely spread external packages - percentage of internal packages

This table shows the top 20 most widely spread external packages focussing on the spread across the percentage of internal packages.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalPackageName</th>
      <th>numberOfArtifacts</th>
      <th>minNumberOfPackagesPercentage</th>
      <th>maxNumberOfPackagesPercentage</th>
      <th>medNumberOfPackagesPercentage</th>
      <th>avgNumberOfPackagesPercentage</th>
      <th>stdNumberOfPackagesPercentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.slf4j</td>
      <td>11</td>
      <td>20.000000</td>
      <td>100.000000</td>
      <td>42.857143</td>
      <td>49.120967</td>
      <td>26.462866</td>
    </tr>
    <tr>
      <th>1</th>
      <td>jakarta.persistence</td>
      <td>4</td>
      <td>1.754386</td>
      <td>28.571429</td>
      <td>10.989011</td>
      <td>13.075959</td>
      <td>11.528729</td>
    </tr>
    <tr>
      <th>2</th>
      <td>com.fasterxml.jackson.databind</td>
      <td>3</td>
      <td>7.692308</td>
      <td>25.000000</td>
      <td>14.285714</td>
      <td>15.659341</td>
      <td>8.735227</td>
    </tr>
    <tr>
      <th>3</th>
      <td>com.fasterxml.jackson.databind.node</td>
      <td>2</td>
      <td>7.692308</td>
      <td>25.000000</td>
      <td>16.346154</td>
      <td>16.346154</td>
      <td>12.238387</td>
    </tr>
    <tr>
      <th>4</th>
      <td>io.axoniq.axonserver.connector</td>
      <td>2</td>
      <td>14.285714</td>
      <td>80.000000</td>
      <td>47.142857</td>
      <td>47.142857</td>
      <td>46.467017</td>
    </tr>
    <tr>
      <th>5</th>
      <td>io.axoniq.axonserver.connector.control</td>
      <td>2</td>
      <td>14.285714</td>
      <td>40.000000</td>
      <td>27.142857</td>
      <td>27.142857</td>
      <td>18.182746</td>
    </tr>
    <tr>
      <th>6</th>
      <td>org.apache.avro</td>
      <td>2</td>
      <td>14.285714</td>
      <td>25.000000</td>
      <td>19.642857</td>
      <td>19.642857</td>
      <td>7.576144</td>
    </tr>
    <tr>
      <th>7</th>
      <td>org.apache.avro.message</td>
      <td>2</td>
      <td>14.285714</td>
      <td>25.000000</td>
      <td>19.642857</td>
      <td>19.642857</td>
      <td>7.576144</td>
    </tr>
    <tr>
      <th>8</th>
      <td>IdTypeParameterResolver</td>
      <td>1</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ScannedEntityCreator</td>
      <td>1</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>WrappedEventCriteriaBuilderMethod</td>
      <td>1</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>com.fasterxml.jackson.annotation</td>
      <td>1</td>
      <td>1.754386</td>
      <td>1.754386</td>
      <td>1.754386</td>
      <td>1.754386</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>com.fasterxml.jackson.core</td>
      <td>1</td>
      <td>25.000000</td>
      <td>25.000000</td>
      <td>25.000000</td>
      <td>25.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>com.fasterxml.jackson.dataformat.cbor.databind</td>
      <td>1</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>com.google.gson</td>
      <td>1</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>com.google.protobuf</td>
      <td>1</td>
      <td>80.000000</td>
      <td>80.000000</td>
      <td>80.000000</td>
      <td>80.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>io.axoniq.axonserver.connector.admin</td>
      <td>1</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>io.axoniq.axonserver.connector.command</td>
      <td>1</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>io.axoniq.axonserver.connector.event</td>
      <td>1</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>io.axoniq.axonserver.connector.impl</td>
      <td>1</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>0.000000</td>
    </tr>
  </tbody>
</table>
</div>



### Table 3c - Top 20 most widely spread external packages - number of internal types

This table shows the top 20 most widely spread external packages focussing on the spread across the number of internal types.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalPackageName</th>
      <th>numberOfArtifacts</th>
      <th>minNumberOfTypes</th>
      <th>maxNumberOfTypes</th>
      <th>medNumberOfTypes</th>
      <th>avgNumberOfTypes</th>
      <th>stdNumberOfTypes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.slf4j</td>
      <td>11</td>
      <td>1</td>
      <td>30</td>
      <td>3.0</td>
      <td>6.727273</td>
      <td>8.486353</td>
    </tr>
    <tr>
      <th>1</th>
      <td>jakarta.persistence</td>
      <td>4</td>
      <td>2</td>
      <td>4</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>1.154701</td>
    </tr>
    <tr>
      <th>2</th>
      <td>com.fasterxml.jackson.databind</td>
      <td>3</td>
      <td>1</td>
      <td>5</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>com.fasterxml.jackson.databind.node</td>
      <td>2</td>
      <td>1</td>
      <td>2</td>
      <td>1.5</td>
      <td>1.500000</td>
      <td>0.707107</td>
    </tr>
    <tr>
      <th>4</th>
      <td>io.axoniq.axonserver.connector</td>
      <td>2</td>
      <td>1</td>
      <td>15</td>
      <td>8.0</td>
      <td>8.000000</td>
      <td>9.899495</td>
    </tr>
    <tr>
      <th>5</th>
      <td>io.axoniq.axonserver.connector.control</td>
      <td>2</td>
      <td>1</td>
      <td>4</td>
      <td>2.5</td>
      <td>2.500000</td>
      <td>2.121320</td>
    </tr>
    <tr>
      <th>6</th>
      <td>org.apache.avro</td>
      <td>2</td>
      <td>1</td>
      <td>4</td>
      <td>2.5</td>
      <td>2.500000</td>
      <td>2.121320</td>
    </tr>
    <tr>
      <th>7</th>
      <td>org.apache.avro.message</td>
      <td>2</td>
      <td>3</td>
      <td>6</td>
      <td>4.5</td>
      <td>4.500000</td>
      <td>2.121320</td>
    </tr>
    <tr>
      <th>8</th>
      <td>IdTypeParameterResolver</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ScannedEntityCreator</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>WrappedEventCriteriaBuilderMethod</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>com.fasterxml.jackson.annotation</td>
      <td>1</td>
      <td>2</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>com.fasterxml.jackson.core</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>com.fasterxml.jackson.dataformat.cbor.databind</td>
      <td>1</td>
      <td>2</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>com.google.gson</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>com.google.protobuf</td>
      <td>1</td>
      <td>8</td>
      <td>8</td>
      <td>8.0</td>
      <td>8.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>io.axoniq.axonserver.connector.admin</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>io.axoniq.axonserver.connector.command</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>io.axoniq.axonserver.connector.event</td>
      <td>1</td>
      <td>5</td>
      <td>5</td>
      <td>5.0</td>
      <td>5.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>io.axoniq.axonserver.connector.impl</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
  </tbody>
</table>
</div>



### Table 3d - Top 20 most widely spread external packages - percentage of internal types

This table shows the top 20 most widely spread external packages focussing on the spread across the percentage of internal types.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalPackageName</th>
      <th>numberOfArtifacts</th>
      <th>minNumberOfTypesPercentage</th>
      <th>maxNumberOfTypesPercentage</th>
      <th>medNumberOfTypesPercentage</th>
      <th>avgNumberOfTypesPercentage</th>
      <th>stdNumberOfTypesPercentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.slf4j</td>
      <td>11</td>
      <td>1.369863</td>
      <td>30.434783</td>
      <td>6.000000</td>
      <td>9.894824</td>
      <td>8.937748</td>
    </tr>
    <tr>
      <th>1</th>
      <td>jakarta.persistence</td>
      <td>4</td>
      <td>0.350877</td>
      <td>5.714286</td>
      <td>2.666667</td>
      <td>2.849624</td>
      <td>2.454419</td>
    </tr>
    <tr>
      <th>2</th>
      <td>com.fasterxml.jackson.databind</td>
      <td>3</td>
      <td>0.666667</td>
      <td>16.666667</td>
      <td>4.285714</td>
      <td>7.206349</td>
      <td>8.390327</td>
    </tr>
    <tr>
      <th>3</th>
      <td>com.fasterxml.jackson.databind.node</td>
      <td>2</td>
      <td>0.666667</td>
      <td>6.666667</td>
      <td>3.666667</td>
      <td>3.666667</td>
      <td>4.242641</td>
    </tr>
    <tr>
      <th>4</th>
      <td>io.axoniq.axonserver.connector</td>
      <td>2</td>
      <td>1.428571</td>
      <td>20.833333</td>
      <td>11.130952</td>
      <td>11.130952</td>
      <td>13.721239</td>
    </tr>
    <tr>
      <th>5</th>
      <td>io.axoniq.axonserver.connector.control</td>
      <td>2</td>
      <td>1.428571</td>
      <td>5.555556</td>
      <td>3.492063</td>
      <td>3.492063</td>
      <td>2.918218</td>
    </tr>
    <tr>
      <th>6</th>
      <td>org.apache.avro</td>
      <td>2</td>
      <td>1.428571</td>
      <td>13.333333</td>
      <td>7.380952</td>
      <td>7.380952</td>
      <td>8.417938</td>
    </tr>
    <tr>
      <th>7</th>
      <td>org.apache.avro.message</td>
      <td>2</td>
      <td>4.285714</td>
      <td>20.000000</td>
      <td>12.142857</td>
      <td>12.142857</td>
      <td>11.111678</td>
    </tr>
    <tr>
      <th>8</th>
      <td>IdTypeParameterResolver</td>
      <td>1</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ScannedEntityCreator</td>
      <td>1</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>WrappedEventCriteriaBuilderMethod</td>
      <td>1</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>com.fasterxml.jackson.annotation</td>
      <td>1</td>
      <td>0.350877</td>
      <td>0.350877</td>
      <td>0.350877</td>
      <td>0.350877</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>com.fasterxml.jackson.core</td>
      <td>1</td>
      <td>3.333333</td>
      <td>3.333333</td>
      <td>3.333333</td>
      <td>3.333333</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>com.fasterxml.jackson.dataformat.cbor.databind</td>
      <td>1</td>
      <td>2.857143</td>
      <td>2.857143</td>
      <td>2.857143</td>
      <td>2.857143</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>com.google.gson</td>
      <td>1</td>
      <td>1.369863</td>
      <td>1.369863</td>
      <td>1.369863</td>
      <td>1.369863</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>com.google.protobuf</td>
      <td>1</td>
      <td>11.111111</td>
      <td>11.111111</td>
      <td>11.111111</td>
      <td>11.111111</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>io.axoniq.axonserver.connector.admin</td>
      <td>1</td>
      <td>1.388889</td>
      <td>1.388889</td>
      <td>1.388889</td>
      <td>1.388889</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>io.axoniq.axonserver.connector.command</td>
      <td>1</td>
      <td>1.388889</td>
      <td>1.388889</td>
      <td>1.388889</td>
      <td>1.388889</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>io.axoniq.axonserver.connector.event</td>
      <td>1</td>
      <td>6.944444</td>
      <td>6.944444</td>
      <td>6.944444</td>
      <td>6.944444</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>io.axoniq.axonserver.connector.impl</td>
      <td>1</td>
      <td>1.388889</td>
      <td>1.388889</td>
      <td>1.388889</td>
      <td>1.388889</td>
      <td>0.000000</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 3 Chart 1a - Most widely spread external packages in % by types (more than 0.5% overall)

External packages that are used less than 0.5% are grouped into the name "others" to get a cleaner chart with the most significant external packages.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_43_1.png)
    


#### Table 3 Chart 1b - Most widely spread external packages in % by types (less than 0.5% overall "others" drill-down)

Shows the lowest (less than 0.5% overall) most spread external packages. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_45_1.png)
    


#### Table 3 Chart 2a - Most widely spread external packages in % by packages (more than 0.5% overall)

External packages that are used less than 0.5% are grouped into the name "others" to get a cleaner chart with the most significant external packages.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_47_1.png)
    


#### Table 3 Chart 2b - Most widely spread external packages in % by packages (less than 0.5% overall "others" drill-down)

Shows the lowest (less than 0.5% overall) most spread external packages. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.

    No data to plot for title 'Top external package usage spread [%] by type (less than 0.7% overall "others" drill-down)'.


### Table 4 - Top 20 most widely spread external packages grouped by their first 2 layers

This table shows external packages grouped by their first 2 layers that are used by many different artifacts with the highest number of artifacts first. External annotations are filtered out to only get those external packages that significantly add to coupling.

Statistics like minimum, maximum, average, median and standard deviation are provided for the number of packages and number of types in every artifact that uses the listed external package. 

The intuition behind that is to find external package dependencies that are used in a widely spread manner. This should uncover libraries and frameworks and make it easier to distinguish them from external dependencies that are used for specific tasks. It can also be used to find external dependencies that are used sparsely regarding artifacts but are used in many different packages there. This could then be improved by applying a [Hexagonal architecture](https://alistair.cockburn.us/hexagonal-architecture).

Only the top 20 entries are shown. The whole table can be found in the following CSV report:
`External_package_usage_spread`

**Columns:**
- *externalPackageName* identifies the external package as defined above. All other columns contain aggregated data for this external package.
- *numberOfArtifacts* contains the number of artifacts that use the external package
- *sumNumberOfPackages* contains the sum of all packages that use the external package
- *min/max/med/avg/stdNumberOfPackages* provide statistics based on the number of packages of each artifact that uses the external package
- *min/max/med/avg/stdNumberOfPackagesPercentage* provide statistics in percent (%) based on the number of packages of each artifact that uses the external package
- *min/max/med/avg/stdNumberOfTypes* provide statistics based on the number of types of each artifact that uses the external package
- *min/max/med/avg/stdNumberOfPackagesPercentage* provide statistics in percent (%) based on the number of types of each artifact that uses the external package
- *someArtifactNames* contain some of the artifacts that contain the external package for reference




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalSecondLevelPackageName</th>
      <th>numberOfArtifacts</th>
      <th>sumNumberOfPackages</th>
      <th>minNumberOfPackages</th>
      <th>maxNumberOfPackages</th>
      <th>medNumberOfPackages</th>
      <th>avgNumberOfPackages</th>
      <th>stdNumberOfPackages</th>
      <th>minNumberOfPackagesPercentage</th>
      <th>maxNumberOfPackagesPercentage</th>
      <th>...</th>
      <th>maxNumberOfTypes</th>
      <th>medNumberOfTypes</th>
      <th>avgNumberOfTypes</th>
      <th>stdNumberOfTypes</th>
      <th>minNumberOfTypesPercentage</th>
      <th>maxNumberOfTypesPercentage</th>
      <th>medNumberOfTypesPercentage</th>
      <th>avgNumberOfTypesPercentage</th>
      <th>stdNumberOfTypesPercentage</th>
      <th>someArtifactNames</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>org.slf4j</td>
      <td>11</td>
      <td>38</td>
      <td>1</td>
      <td>14</td>
      <td>3.0</td>
      <td>3.454545</td>
      <td>3.670521</td>
      <td>20.000000</td>
      <td>100.000000</td>
      <td>...</td>
      <td>30</td>
      <td>3.0</td>
      <td>6.727273</td>
      <td>8.486353</td>
      <td>1.369863</td>
      <td>30.434783</td>
      <td>6.000000</td>
      <td>9.894824</td>
      <td>8.937748</td>
      <td>[axon-tracing-opentelemetry-5.0.1, axon-common...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>com.fasterxml</td>
      <td>4</td>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.754386</td>
      <td>25.000000</td>
      <td>...</td>
      <td>5</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>1.825742</td>
      <td>0.350877</td>
      <td>16.666667</td>
      <td>3.190476</td>
      <td>5.849624</td>
      <td>7.618530</td>
      <td>[axon-common-5.0.1, axon-spring-boot-autoconfi...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>jakarta.persistence</td>
      <td>4</td>
      <td>5</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.250000</td>
      <td>0.500000</td>
      <td>1.754386</td>
      <td>28.571429</td>
      <td>...</td>
      <td>4</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>1.154701</td>
      <td>0.350877</td>
      <td>5.714286</td>
      <td>2.666667</td>
      <td>2.849624</td>
      <td>2.454419</td>
      <td>[axon-common-5.0.1, axon-eventsourcing-5.0.1, ...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>com.google</td>
      <td>2</td>
      <td>5</td>
      <td>1</td>
      <td>4</td>
      <td>2.5</td>
      <td>2.500000</td>
      <td>2.121320</td>
      <td>20.000000</td>
      <td>80.000000</td>
      <td>...</td>
      <td>8</td>
      <td>4.5</td>
      <td>4.500000</td>
      <td>4.949747</td>
      <td>1.369863</td>
      <td>11.111111</td>
      <td>6.240487</td>
      <td>6.240487</td>
      <td>6.888103</td>
      <td>[axon-server-connector-5.0.1, axon-test-5.0.1]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>io.axoniq</td>
      <td>2</td>
      <td>6</td>
      <td>1</td>
      <td>5</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>2.828427</td>
      <td>14.285714</td>
      <td>100.000000</td>
      <td>...</td>
      <td>44</td>
      <td>22.5</td>
      <td>22.500000</td>
      <td>30.405592</td>
      <td>1.428571</td>
      <td>61.111111</td>
      <td>31.269841</td>
      <td>31.269841</td>
      <td>42.201929</td>
      <td>[axon-server-connector-5.0.1, axon-spring-boot...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>org.apache</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>14.285714</td>
      <td>25.000000</td>
      <td>...</td>
      <td>9</td>
      <td>6.0</td>
      <td>6.000000</td>
      <td>4.242641</td>
      <td>4.285714</td>
      <td>30.000000</td>
      <td>17.142857</td>
      <td>17.142857</td>
      <td>18.182746</td>
      <td>[axon-spring-boot-autoconfigure-5.0.1, axon-co...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>reactor.core</td>
      <td>2</td>
      <td>6</td>
      <td>1</td>
      <td>5</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>2.828427</td>
      <td>8.771930</td>
      <td>20.000000</td>
      <td>...</td>
      <td>8</td>
      <td>4.5</td>
      <td>4.500000</td>
      <td>4.949747</td>
      <td>1.388889</td>
      <td>1.403509</td>
      <td>1.396199</td>
      <td>1.396199</td>
      <td>0.010338</td>
      <td>[axon-server-connector-5.0.1, axon-messaging-5...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>IdTypeParameterResolver</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>...</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>[axon-eventsourcing-5.0.1]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>ScannedEntityCreator</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>...</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>[axon-eventsourcing-5.0.1]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>WrappedEventCriteriaBuilderMethod</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>...</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>[axon-eventsourcing-5.0.1]</td>
    </tr>
    <tr>
      <th>10</th>
      <td>io.grpc</td>
      <td>1</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>0.000000</td>
      <td>60.000000</td>
      <td>60.000000</td>
      <td>...</td>
      <td>10</td>
      <td>10.0</td>
      <td>10.000000</td>
      <td>0.000000</td>
      <td>13.888889</td>
      <td>13.888889</td>
      <td>13.888889</td>
      <td>13.888889</td>
      <td>0.000000</td>
      <td>[axon-server-connector-5.0.1]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>io.micrometer</td>
      <td>1</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>0.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>...</td>
      <td>12</td>
      <td>12.0</td>
      <td>12.000000</td>
      <td>0.000000</td>
      <td>92.307692</td>
      <td>92.307692</td>
      <td>92.307692</td>
      <td>92.307692</td>
      <td>0.000000</td>
      <td>[axon-metrics-micrometer-5.0.1]</td>
    </tr>
    <tr>
      <th>12</th>
      <td>io.opentelemetry</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>...</td>
      <td>5</td>
      <td>5.0</td>
      <td>5.000000</td>
      <td>0.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>0.000000</td>
      <td>[axon-tracing-opentelemetry-5.0.1]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>jakarta.validation</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.754386</td>
      <td>1.754386</td>
      <td>...</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>0.000000</td>
      <td>0.350877</td>
      <td>0.350877</td>
      <td>0.350877</td>
      <td>0.350877</td>
      <td>0.000000</td>
      <td>[axon-messaging-5.0.1]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>javax.cache</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>7.692308</td>
      <td>7.692308</td>
      <td>...</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>0.000000</td>
      <td>1.333333</td>
      <td>1.333333</td>
      <td>1.333333</td>
      <td>1.333333</td>
      <td>0.000000</td>
      <td>[axon-common-5.0.1]</td>
    </tr>
    <tr>
      <th>15</th>
      <td>org.awaitility</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>...</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.369863</td>
      <td>1.369863</td>
      <td>1.369863</td>
      <td>1.369863</td>
      <td>0.000000</td>
      <td>[axon-test-5.0.1]</td>
    </tr>
    <tr>
      <th>16</th>
      <td>org.axonframework</td>
      <td>1</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>0.000000</td>
      <td>42.857143</td>
      <td>42.857143</td>
      <td>...</td>
      <td>8</td>
      <td>8.0</td>
      <td>8.000000</td>
      <td>0.000000</td>
      <td>11.428571</td>
      <td>11.428571</td>
      <td>11.428571</td>
      <td>11.428571</td>
      <td>0.000000</td>
      <td>[axon-spring-boot-autoconfigure-5.0.1]</td>
    </tr>
    <tr>
      <th>17</th>
      <td>org.ehcache</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>7.692308</td>
      <td>7.692308</td>
      <td>...</td>
      <td>3</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>0.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>0.000000</td>
      <td>[axon-common-5.0.1]</td>
    </tr>
    <tr>
      <th>18</th>
      <td>org.hamcrest</td>
      <td>1</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>0.000000</td>
      <td>60.000000</td>
      <td>60.000000</td>
      <td>...</td>
      <td>22</td>
      <td>22.0</td>
      <td>22.000000</td>
      <td>0.000000</td>
      <td>30.136986</td>
      <td>30.136986</td>
      <td>30.136986</td>
      <td>30.136986</td>
      <td>0.000000</td>
      <td>[axon-test-5.0.1]</td>
    </tr>
    <tr>
      <th>19</th>
      <td>org.junit</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>...</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>1.369863</td>
      <td>1.369863</td>
      <td>1.369863</td>
      <td>1.369863</td>
      <td>0.000000</td>
      <td>[axon-test-5.0.1]</td>
    </tr>
  </tbody>
</table>
<p>20 rows × 25 columns</p>
</div>



#### Table 4 Chart 1a - Most widely spread second level external packages in % by type (more than 0.5% overall)

External package groups that are used less than 0.5% are grouped into the name "others" to get a cleaner chart
with the most significant external packages and how ofter they are called in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_53_1.png)
    


#### Table 4 Chart 1b - Most widely spread second level external packages in % by type  (less than 0.5% overall "others" drill-down)

External packages that are used less than 0.5% are grouped into the name "others" to get a cleaner chart with the most significant external packages.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_55_1.png)
    


#### Table 4 Chart 2a - Most widely spread second level external packages in % by package (more than 0.5% overall)

External package groups that are used less than 0.5% are grouped into the name "others" to get a cleaner chart
with the most significant external packages and how ofter they are called in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_57_1.png)
    


#### Table 4 Chart 2b - Most widely spread second level external packages in % by package (less than 0.5% overall "others" drill-down)

External packages that are used less than 0.5% are grouped into the name "others" to get a cleaner chart with the most significant external packages.

    No data to plot for title 'Top external package (less than 0.7% overall "others" drill-down)'.


### Table 5 - Top 20 least used external packages overall

This table identifies external packages that aren't used very often. This could help to find libraries that aren't actually needed or maybe easily replaceable. Some of them might be used sparsely on purpose for example as an adapter to an external library that is actually important. Thus, decisions need to be made on a case-by-case basis.

Only the last 20 entries are shown. The whole table can be found in the following CSV report:
`External_package_usage_overall`

**Columns:**
- *externalPackageName* identifies the external package as described above
- *numberOfExternalTypeCalls* includes every invocation or reference to the types in the external package




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalPackageName</th>
      <th>numberOfExternalTypeCalls</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>reactor.core.scheduler</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>org.springframework.boot.context.properties.bind</td>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>org.springframework.boot.docker.compose.core</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>org.springframework.boot.docker.compose.servic...</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>org.testcontainers.utility</td>
      <td>2</td>
    </tr>
    <tr>
      <th>5</th>
      <td>org.testcontainers.containers</td>
      <td>2</td>
    </tr>
    <tr>
      <th>6</th>
      <td>org.testcontainers.containers.wait.strategy</td>
      <td>2</td>
    </tr>
    <tr>
      <th>7</th>
      <td>org.axonframework.extension.spring.conversion....</td>
      <td>3</td>
    </tr>
    <tr>
      <th>8</th>
      <td>javax.cache.configuration</td>
      <td>3</td>
    </tr>
    <tr>
      <th>9</th>
      <td>io.grpc.stub</td>
      <td>4</td>
    </tr>
    <tr>
      <th>10</th>
      <td>org.springframework.beans.factory</td>
      <td>4</td>
    </tr>
    <tr>
      <th>11</th>
      <td>com.google.gson</td>
      <td>4</td>
    </tr>
    <tr>
      <th>12</th>
      <td>org.apache.avro.specific</td>
      <td>4</td>
    </tr>
    <tr>
      <th>13</th>
      <td>org.springframework.boot.testcontainers.servic...</td>
      <td>4</td>
    </tr>
    <tr>
      <th>14</th>
      <td>io.axoniq.axonserver.grpc.event</td>
      <td>5</td>
    </tr>
    <tr>
      <th>15</th>
      <td>jakarta.validation</td>
      <td>5</td>
    </tr>
    <tr>
      <th>16</th>
      <td>org.springframework.context</td>
      <td>5</td>
    </tr>
    <tr>
      <th>17</th>
      <td>com.fasterxml.jackson.databind.node</td>
      <td>5</td>
    </tr>
    <tr>
      <th>18</th>
      <td>io.axoniq.axonserver.connector.query</td>
      <td>6</td>
    </tr>
    <tr>
      <th>19</th>
      <td>org.apache.avro.generic</td>
      <td>7</td>
    </tr>
  </tbody>
</table>
</div>



### Table 6 - External usage per artifact sorted by highest external type rate descending

The following table shows the most used external packages separately for each artifact including external annotations. The results are sorted by the artifacts with the highest external type usage rate descending. 

The intention of this table is to find artifacts that use a lot of external dependencies in relation to their size and get all the external packages and their usage.

Only the last 40 entries are shown. The whole table can be found in the following CSV report:
`External_package_usage_per_artifact_sorted`

**Columns:**
- *artifactName* is used to group the the external package usage per artifact for a more detailed analysis.
- *externalPackageName* identifies the external package as described above
- *numberOfExternalTypeCaller* refers to the distinct types that make use of the external package
- *numberOfExternalTypeCalls* includes every invocation or reference to the types in the external package
- *numberOfTypesInArtifact* represents the total count of all analyzed types for the artifact
- *numberOfExternalTypesInArtifact* is the number of all external types that are used by the artifact
- *numberOfExternalPackagesInArtifact* is the number of all external packages that are used by the artifact
- *externalTypeRate* is the numberOfExternalTypesInArtifact / numberOfTypesInArtifact * 100
- *externalTypeNames* contains a list of actually utilized types of the external package




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>externalPackageName</th>
      <th>numberOfExternalTypeCaller</th>
      <th>numberOfExternalTypeCalls</th>
      <th>numberOfTypesInArtifact</th>
      <th>numberOfExternalTypesInArtifact</th>
      <th>numberOfExternalPackagesInArtifact</th>
      <th>externalTypeRate</th>
      <th>externalTypeNames</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>io.opentelemetry.api.trace</td>
      <td>9</td>
      <td>46</td>
      <td>5</td>
      <td>16</td>
      <td>6</td>
      <td>320.000000</td>
      <td>[Tracer, SpanKind, SpanBuilder, Span, StatusCo...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>io.opentelemetry.context.propagation</td>
      <td>9</td>
      <td>15</td>
      <td>5</td>
      <td>16</td>
      <td>6</td>
      <td>320.000000</td>
      <td>[ContextPropagators, TextMapPropagator, TextMa...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>jakarta.annotation</td>
      <td>3</td>
      <td>8</td>
      <td>5</td>
      <td>16</td>
      <td>6</td>
      <td>320.000000</td>
      <td>[Nonnull]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>io.opentelemetry.context</td>
      <td>2</td>
      <td>7</td>
      <td>5</td>
      <td>16</td>
      <td>6</td>
      <td>320.000000</td>
      <td>[Context, Scope]</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>org.slf4j</td>
      <td>2</td>
      <td>7</td>
      <td>5</td>
      <td>16</td>
      <td>6</td>
      <td>320.000000</td>
      <td>[Logger, LoggerFactory]</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>io.opentelemetry.api</td>
      <td>1</td>
      <td>2</td>
      <td>5</td>
      <td>16</td>
      <td>6</td>
      <td>320.000000</td>
      <td>[GlobalOpenTelemetry]</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.grpc</td>
      <td>40</td>
      <td>271</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[ErrorMessage, ProcessingInstruction$Builder, ...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-server-connector-5.0.1</td>
      <td>jakarta.annotation</td>
      <td>33</td>
      <td>199</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[Nonnull, Nullable]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.grpc.event.dcb</td>
      <td>28</td>
      <td>104</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[GetHeadResponse, Event, GetTailResponse, GetS...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.grpc</td>
      <td>23</td>
      <td>51</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[Channel, ClientCall, MethodDescriptor, CallOp...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.connector</td>
      <td>22</td>
      <td>123</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[Registration, AxonServerConnection, ResultStr...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.slf4j</td>
      <td>19</td>
      <td>70</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[Logger, LoggerFactory]</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.grpc.query</td>
      <td>14</td>
      <td>98</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[QueryUpdate$Builder, QueryRequest$Builder, Su...</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.grpc.control</td>
      <td>13</td>
      <td>86</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[TopologyChange, QuerySubscription, CommandSub...</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-server-connector-5.0.1</td>
      <td>com.google.protobuf</td>
      <td>8</td>
      <td>29</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[ByteString, MessageLite]</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.connector.event</td>
      <td>8</td>
      <td>38</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[DcbEventChannel, DcbEventChannel$AppendEvents...</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.grpc.command</td>
      <td>8</td>
      <td>63</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[CommandResponse$Builder, Command$Builder, Com...</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.connector.query</td>
      <td>6</td>
      <td>19</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[SubscriptionQueryResult, QueryDefinition, Que...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.grpc.event</td>
      <td>5</td>
      <td>31</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[Confirmation, Event$Builder, Event, EventWith...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.connector.control</td>
      <td>4</td>
      <td>5</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[ProcessorInstructionHandler, ControlChannel]</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.grpc.stub</td>
      <td>4</td>
      <td>11</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[ClientCallStreamObserver, ClientResponseObser...</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-server-connector-5.0.1</td>
      <td>reactor.core.scheduler</td>
      <td>2</td>
      <td>2</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[Scheduler, Schedulers]</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.connector.admin</td>
      <td>1</td>
      <td>3</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[AdminChannel]</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.connector.command</td>
      <td>1</td>
      <td>3</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[CommandChannel]</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.axoniq.axonserver.connector.impl</td>
      <td>1</td>
      <td>3</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[ServerAddress]</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.grpc.netty.shaded.io.grpc.netty</td>
      <td>1</td>
      <td>1</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[GrpcSslContexts]</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-server-connector-5.0.1</td>
      <td>io.grpc.netty.shaded.io.netty.handler.ssl</td>
      <td>1</td>
      <td>2</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[SslContextBuilder]</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-server-connector-5.0.1</td>
      <td>javax.annotation</td>
      <td>1</td>
      <td>1</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[Nonnull]</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.springframework.boot.context.properties</td>
      <td>1</td>
      <td>2</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>[ConfigurationProperties]</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.springframework.boot.autoconfigure.condition</td>
      <td>42</td>
      <td>72</td>
      <td>70</td>
      <td>87</td>
      <td>36</td>
      <td>124.285714</td>
      <td>[ConditionalOnProperty, ConditionalOnMissingBe...</td>
    </tr>
    <tr>
      <th>30</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.springframework.context.annotation</td>
      <td>36</td>
      <td>64</td>
      <td>70</td>
      <td>87</td>
      <td>36</td>
      <td>124.285714</td>
      <td>[Conditional, Bean, Primary, Condition, Condit...</td>
    </tr>
    <tr>
      <th>31</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.springframework.boot.autoconfigure</td>
      <td>29</td>
      <td>30</td>
      <td>70</td>
      <td>87</td>
      <td>36</td>
      <td>124.285714</td>
      <td>[AutoConfiguration, AutoConfigureBefore, AutoC...</td>
    </tr>
    <tr>
      <th>32</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.springframework.boot.context.properties</td>
      <td>20</td>
      <td>26</td>
      <td>70</td>
      <td>87</td>
      <td>36</td>
      <td>124.285714</td>
      <td>[EnableConfigurationProperties, ConfigurationP...</td>
    </tr>
    <tr>
      <th>33</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>jakarta.annotation</td>
      <td>12</td>
      <td>25</td>
      <td>70</td>
      <td>87</td>
      <td>36</td>
      <td>124.285714</td>
      <td>[Nonnull]</td>
    </tr>
    <tr>
      <th>34</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.spring.config</td>
      <td>9</td>
      <td>35</td>
      <td>70</td>
      <td>87</td>
      <td>36</td>
      <td>124.285714</td>
      <td>[SpringComponentRegistry, SpringLifecycleRegis...</td>
    </tr>
    <tr>
      <th>35</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.springframework.boot.actuate.health</td>
      <td>7</td>
      <td>24</td>
      <td>70</td>
      <td>87</td>
      <td>36</td>
      <td>124.285714</td>
      <td>[Status, SimpleStatusAggregator, Health$Builde...</td>
    </tr>
    <tr>
      <th>36</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>jakarta.persistence</td>
      <td>5</td>
      <td>8</td>
      <td>70</td>
      <td>87</td>
      <td>36</td>
      <td>124.285714</td>
      <td>[EntityManagerFactory, EntityManager, Persiste...</td>
    </tr>
    <tr>
      <th>37</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.springframework.context</td>
      <td>5</td>
      <td>9</td>
      <td>70</td>
      <td>87</td>
      <td>36</td>
      <td>124.285714</td>
      <td>[ApplicationContext, ApplicationContextAware]</td>
    </tr>
    <tr>
      <th>38</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.apache.avro.message</td>
      <td>4</td>
      <td>10</td>
      <td>70</td>
      <td>87</td>
      <td>36</td>
      <td>124.285714</td>
      <td>[SchemaStore, SchemaStore$Cache]</td>
    </tr>
    <tr>
      <th>39</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.slf4j</td>
      <td>4</td>
      <td>6</td>
      <td>70</td>
      <td>87</td>
      <td>36</td>
      <td>124.285714</td>
      <td>[LoggerFactory, Logger]</td>
    </tr>
  </tbody>
</table>
</div>



### Table 7 - Artifacts and their external packages

The following table shows the artifacts with the highest external dependency usage broken down by each external package including external annotations. The results are sorted by the artifacts with the highest external package usage rate descending. 

The intention of this table is to find artifacts that use a lot of external dependencies and show in detail which external packages are used by them and how many internal packages.

Only the last 30 entries are shown. The whole table can be found in the following CSV report:
`External_package_usage_per_artifact_and_external_package`

**Columns:**
- *artifactName* is the name of the artifact with external dependencies (first grouping column)
- *artifactPackages* is the number of packages in the artifact
- *artifactTypes* is the number of types in the artifact
- *artifactExternalPackages* is the number of external packages used by the artifact
- *artifactExternalCallingPackages* is the number of packages that use external packages in the artifact 
- *artifactExternalCallingPackagesRate* is artifactExternalCallingPackages / artifactPackages * 100%
- *externalPackageName* the name of the external package (second grouping column)
- *numberOfPackages* is the number of internal packages of the artifact that use the external packages
- *numberOfTypes* is the number of internal types of the artifact that use the external packages
- *packagesCallingExternalRate* is numberOfPackages / artifactPackages * 100%
- *typesCallingExternalRate* is numberOfTypes / artifactTypes * 100%
- *nameOfPackages* names of the internal packages that use the external package in the artifact
- *someTypeNames* some (10) names of the internal types that use the external package in the artifact




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>artifactPackages</th>
      <th>artifactTypes</th>
      <th>artifactExternalPackages</th>
      <th>artifactExternalCallingPackages</th>
      <th>artifactExternalCallingPackagesRate</th>
      <th>externalPackageName</th>
      <th>numberOfPackages</th>
      <th>numberOfTypes</th>
      <th>packagesCallingExternalRate</th>
      <th>typesCallingExternalRate</th>
      <th>nameOfPackages</th>
      <th>someTypeNames</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>11</td>
      <td>4</td>
      <td>100.0</td>
      <td>jakarta.annotation</td>
      <td>4</td>
      <td>25</td>
      <td>100.000000</td>
      <td>83.333333</td>
      <td>[org.axonframework.conversion, org.axonframewo...</td>
      <td>[org.axonframework.conversion.PassThroughConve...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>11</td>
      <td>4</td>
      <td>100.0</td>
      <td>org.slf4j</td>
      <td>3</td>
      <td>3</td>
      <td>75.000000</td>
      <td>10.000000</td>
      <td>[org.axonframework.conversion, org.axonframewo...</td>
      <td>[org.axonframework.conversion.ChainingContentT...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>11</td>
      <td>4</td>
      <td>100.0</td>
      <td>com.fasterxml.jackson.core</td>
      <td>1</td>
      <td>1</td>
      <td>25.000000</td>
      <td>3.333333</td>
      <td>[org.axonframework.conversion.json]</td>
      <td>[org.axonframework.conversion.json.JsonNodeToB...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>11</td>
      <td>4</td>
      <td>100.0</td>
      <td>com.fasterxml.jackson.databind</td>
      <td>1</td>
      <td>5</td>
      <td>25.000000</td>
      <td>16.666667</td>
      <td>[org.axonframework.conversion.json]</td>
      <td>[org.axonframework.conversion.json.JsonNodeToO...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>11</td>
      <td>4</td>
      <td>100.0</td>
      <td>com.fasterxml.jackson.databind.node</td>
      <td>1</td>
      <td>2</td>
      <td>25.000000</td>
      <td>6.666667</td>
      <td>[org.axonframework.conversion.json]</td>
      <td>[org.axonframework.conversion.json.JsonNodeToO...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>11</td>
      <td>4</td>
      <td>100.0</td>
      <td>org.apache.avro</td>
      <td>1</td>
      <td>4</td>
      <td>25.000000</td>
      <td>13.333333</td>
      <td>[org.axonframework.conversion.avro]</td>
      <td>[org.axonframework.conversion.avro.SpecificRec...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>11</td>
      <td>4</td>
      <td>100.0</td>
      <td>org.apache.avro.generic</td>
      <td>1</td>
      <td>6</td>
      <td>25.000000</td>
      <td>20.000000</td>
      <td>[org.axonframework.conversion.avro]</td>
      <td>[org.axonframework.conversion.avro.SpecificRec...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>11</td>
      <td>4</td>
      <td>100.0</td>
      <td>org.apache.avro.io</td>
      <td>1</td>
      <td>1</td>
      <td>25.000000</td>
      <td>3.333333</td>
      <td>[org.axonframework.conversion.avro]</td>
      <td>[org.axonframework.conversion.avro.ByteArrayTo...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>11</td>
      <td>4</td>
      <td>100.0</td>
      <td>org.apache.avro.message</td>
      <td>1</td>
      <td>6</td>
      <td>25.000000</td>
      <td>20.000000</td>
      <td>[org.axonframework.conversion.avro]</td>
      <td>[org.axonframework.conversion.avro.AvroConvert...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>11</td>
      <td>4</td>
      <td>100.0</td>
      <td>org.apache.avro.specific</td>
      <td>1</td>
      <td>2</td>
      <td>25.000000</td>
      <td>6.666667</td>
      <td>[org.axonframework.conversion.avro]</td>
      <td>[org.axonframework.conversion.avro.SpecificRec...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>11</td>
      <td>4</td>
      <td>100.0</td>
      <td>org.apache.commons.lang3.tuple</td>
      <td>1</td>
      <td>1</td>
      <td>25.000000</td>
      <td>3.333333</td>
      <td>[org.axonframework.conversion.avro]</td>
      <td>[org.axonframework.conversion.avro.DefaultSche...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>6</td>
      <td>7</td>
      <td>100.0</td>
      <td>jakarta.annotation</td>
      <td>7</td>
      <td>62</td>
      <td>100.000000</td>
      <td>62.000000</td>
      <td>[org.axonframework.eventsourcing, org.axonfram...</td>
      <td>[org.axonframework.eventsourcing.CriteriaResol...</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>6</td>
      <td>7</td>
      <td>100.0</td>
      <td>org.slf4j</td>
      <td>2</td>
      <td>6</td>
      <td>28.571429</td>
      <td>6.000000</td>
      <td>[org.axonframework.eventsourcing.eventstore.in...</td>
      <td>[org.axonframework.eventsourcing.eventstore.in...</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>6</td>
      <td>7</td>
      <td>100.0</td>
      <td>IdTypeParameterResolver</td>
      <td>1</td>
      <td>1</td>
      <td>14.285714</td>
      <td>1.000000</td>
      <td>[org.axonframework.eventsourcing.annotation.re...</td>
      <td>[org.axonframework.eventsourcing.annotation.re...</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>6</td>
      <td>7</td>
      <td>100.0</td>
      <td>ScannedEntityCreator</td>
      <td>1</td>
      <td>1</td>
      <td>14.285714</td>
      <td>1.000000</td>
      <td>[org.axonframework.eventsourcing.annotation.re...</td>
      <td>[org.axonframework.eventsourcing.annotation.re...</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>6</td>
      <td>7</td>
      <td>100.0</td>
      <td>WrappedEventCriteriaBuilderMethod</td>
      <td>1</td>
      <td>1</td>
      <td>14.285714</td>
      <td>1.000000</td>
      <td>[org.axonframework.eventsourcing.annotation]</td>
      <td>[org.axonframework.eventsourcing.annotation.An...</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>6</td>
      <td>7</td>
      <td>100.0</td>
      <td>jakarta.persistence</td>
      <td>1</td>
      <td>4</td>
      <td>14.285714</td>
      <td>4.000000</td>
      <td>[org.axonframework.eventsourcing.eventstore.jpa]</td>
      <td>[org.axonframework.eventsourcing.eventstore.jp...</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>2</td>
      <td>13</td>
      <td>4</td>
      <td>2</td>
      <td>100.0</td>
      <td>io.micrometer.core.instrument</td>
      <td>2</td>
      <td>12</td>
      <td>100.000000</td>
      <td>92.307692</td>
      <td>[org.axonframework.extension.metrics.micromete...</td>
      <td>[org.axonframework.extension.metrics.micromete...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>2</td>
      <td>13</td>
      <td>4</td>
      <td>2</td>
      <td>100.0</td>
      <td>io.micrometer.core.instrument.simple</td>
      <td>1</td>
      <td>1</td>
      <td>50.000000</td>
      <td>7.692308</td>
      <td>[org.axonframework.extension.metrics.micrometer]</td>
      <td>[org.axonframework.extension.metrics.micromete...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>2</td>
      <td>13</td>
      <td>4</td>
      <td>2</td>
      <td>100.0</td>
      <td>jakarta.annotation</td>
      <td>1</td>
      <td>5</td>
      <td>50.000000</td>
      <td>38.461538</td>
      <td>[org.axonframework.extension.metrics.micrometer]</td>
      <td>[org.axonframework.extension.metrics.micromete...</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>2</td>
      <td>13</td>
      <td>4</td>
      <td>2</td>
      <td>100.0</td>
      <td>org.slf4j</td>
      <td>1</td>
      <td>1</td>
      <td>50.000000</td>
      <td>7.692308</td>
      <td>[org.axonframework.extension.metrics.micrometer]</td>
      <td>[org.axonframework.extension.metrics.micromete...</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-modelling-5.0.1</td>
      <td>7</td>
      <td>93</td>
      <td>2</td>
      <td>7</td>
      <td>100.0</td>
      <td>jakarta.annotation</td>
      <td>7</td>
      <td>77</td>
      <td>100.000000</td>
      <td>82.795699</td>
      <td>[org.axonframework.modelling, org.axonframewor...</td>
      <td>[org.axonframework.modelling.EntityEvolvingCom...</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-modelling-5.0.1</td>
      <td>7</td>
      <td>93</td>
      <td>2</td>
      <td>7</td>
      <td>100.0</td>
      <td>org.slf4j</td>
      <td>3</td>
      <td>3</td>
      <td>42.857143</td>
      <td>3.225806</td>
      <td>[org.axonframework.modelling, org.axonframewor...</td>
      <td>[org.axonframework.modelling.SimpleEntityEvolv...</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>23</td>
      <td>5</td>
      <td>100.0</td>
      <td>io.axoniq.axonserver.grpc</td>
      <td>5</td>
      <td>18</td>
      <td>100.000000</td>
      <td>25.000000</td>
      <td>[org.axonframework.axonserver.connector, org.a...</td>
      <td>[org.axonframework.axonserver.connector.ErrorC...</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>23</td>
      <td>5</td>
      <td>100.0</td>
      <td>jakarta.annotation</td>
      <td>5</td>
      <td>25</td>
      <td>100.000000</td>
      <td>34.722222</td>
      <td>[org.axonframework.axonserver.connector, org.a...</td>
      <td>[org.axonframework.axonserver.connector.Metada...</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>23</td>
      <td>5</td>
      <td>100.0</td>
      <td>com.google.protobuf</td>
      <td>4</td>
      <td>8</td>
      <td>80.000000</td>
      <td>11.111111</td>
      <td>[org.axonframework.axonserver.connector.util, ...</td>
      <td>[org.axonframework.axonserver.connector.util.G...</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>23</td>
      <td>5</td>
      <td>100.0</td>
      <td>io.axoniq.axonserver.connector</td>
      <td>4</td>
      <td>15</td>
      <td>80.000000</td>
      <td>20.833333</td>
      <td>[org.axonframework.axonserver.connector, org.a...</td>
      <td>[org.axonframework.axonserver.connector.AxonSe...</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>23</td>
      <td>5</td>
      <td>100.0</td>
      <td>org.slf4j</td>
      <td>4</td>
      <td>12</td>
      <td>80.000000</td>
      <td>16.666667</td>
      <td>[org.axonframework.axonserver.connector.util, ...</td>
      <td>[org.axonframework.axonserver.connector.util.G...</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>23</td>
      <td>5</td>
      <td>100.0</td>
      <td>io.grpc</td>
      <td>3</td>
      <td>7</td>
      <td>60.000000</td>
      <td>9.722222</td>
      <td>[org.axonframework.axonserver.connector, org.a...</td>
      <td>[org.axonframework.axonserver.connector.Manage...</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>23</td>
      <td>5</td>
      <td>100.0</td>
      <td>io.axoniq.axonserver.connector.control</td>
      <td>2</td>
      <td>4</td>
      <td>40.000000</td>
      <td>5.555556</td>
      <td>[org.axonframework.axonserver.connector, org.a...</td>
      <td>[org.axonframework.axonserver.connector.AxonSe...</td>
    </tr>
  </tbody>
</table>
</div>



### Table 7a - Artifacts and their external packages (first 2 levels)

The following table groups the external packages by their first two levels. For example `javax.xml.namespace` and `javax.xml.stream` will be grouped together to `javax.xml`.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>artifactPackages</th>
      <th>artifactTypes</th>
      <th>artifactExternalPackagesFirst2Levels</th>
      <th>artifactExternalCallingPackages</th>
      <th>artifactExternalCallingPackagesRate</th>
      <th>externalPackageNameFirst2Levels</th>
      <th>numberOfPackages</th>
      <th>numberOfTypes</th>
      <th>packagesCallingExternalRate</th>
      <th>typesCallingExternalRate</th>
      <th>nameOfPackages</th>
      <th>someTypeNames</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>4</td>
      <td>4</td>
      <td>100.0</td>
      <td>jakarta.annotation</td>
      <td>4</td>
      <td>25</td>
      <td>100.000000</td>
      <td>83.333333</td>
      <td>[org.axonframework.conversion, org.axonframewo...</td>
      <td>[org.axonframework.conversion.PassThroughConve...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>4</td>
      <td>4</td>
      <td>100.0</td>
      <td>org.slf4j</td>
      <td>3</td>
      <td>3</td>
      <td>75.000000</td>
      <td>10.000000</td>
      <td>[org.axonframework.conversion, org.axonframewo...</td>
      <td>[org.axonframework.conversion.ChainingContentT...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>4</td>
      <td>4</td>
      <td>100.0</td>
      <td>com.fasterxml</td>
      <td>1</td>
      <td>5</td>
      <td>25.000000</td>
      <td>16.666667</td>
      <td>[org.axonframework.conversion.json]</td>
      <td>[org.axonframework.conversion.json.JsonNodeToO...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>4</td>
      <td>4</td>
      <td>100.0</td>
      <td>org.apache</td>
      <td>1</td>
      <td>9</td>
      <td>25.000000</td>
      <td>30.000000</td>
      <td>[org.axonframework.conversion.avro]</td>
      <td>[org.axonframework.conversion.avro.AvroConvert...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>6</td>
      <td>7</td>
      <td>100.0</td>
      <td>jakarta.annotation</td>
      <td>7</td>
      <td>62</td>
      <td>100.000000</td>
      <td>62.000000</td>
      <td>[org.axonframework.eventsourcing, org.axonfram...</td>
      <td>[org.axonframework.eventsourcing.CriteriaResol...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>6</td>
      <td>7</td>
      <td>100.0</td>
      <td>org.slf4j</td>
      <td>2</td>
      <td>6</td>
      <td>28.571429</td>
      <td>6.000000</td>
      <td>[org.axonframework.eventsourcing.eventstore.in...</td>
      <td>[org.axonframework.eventsourcing.eventstore.in...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>6</td>
      <td>7</td>
      <td>100.0</td>
      <td>IdTypeParameterResolver</td>
      <td>1</td>
      <td>1</td>
      <td>14.285714</td>
      <td>1.000000</td>
      <td>[org.axonframework.eventsourcing.annotation.re...</td>
      <td>[org.axonframework.eventsourcing.annotation.re...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>6</td>
      <td>7</td>
      <td>100.0</td>
      <td>ScannedEntityCreator</td>
      <td>1</td>
      <td>1</td>
      <td>14.285714</td>
      <td>1.000000</td>
      <td>[org.axonframework.eventsourcing.annotation.re...</td>
      <td>[org.axonframework.eventsourcing.annotation.re...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>6</td>
      <td>7</td>
      <td>100.0</td>
      <td>WrappedEventCriteriaBuilderMethod</td>
      <td>1</td>
      <td>1</td>
      <td>14.285714</td>
      <td>1.000000</td>
      <td>[org.axonframework.eventsourcing.annotation]</td>
      <td>[org.axonframework.eventsourcing.annotation.An...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>6</td>
      <td>7</td>
      <td>100.0</td>
      <td>jakarta.persistence</td>
      <td>1</td>
      <td>4</td>
      <td>14.285714</td>
      <td>4.000000</td>
      <td>[org.axonframework.eventsourcing.eventstore.jpa]</td>
      <td>[org.axonframework.eventsourcing.eventstore.jp...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>2</td>
      <td>13</td>
      <td>3</td>
      <td>2</td>
      <td>100.0</td>
      <td>io.micrometer</td>
      <td>2</td>
      <td>12</td>
      <td>100.000000</td>
      <td>92.307692</td>
      <td>[org.axonframework.extension.metrics.micromete...</td>
      <td>[org.axonframework.extension.metrics.micromete...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>2</td>
      <td>13</td>
      <td>3</td>
      <td>2</td>
      <td>100.0</td>
      <td>jakarta.annotation</td>
      <td>1</td>
      <td>5</td>
      <td>50.000000</td>
      <td>38.461538</td>
      <td>[org.axonframework.extension.metrics.micrometer]</td>
      <td>[org.axonframework.extension.metrics.micromete...</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>2</td>
      <td>13</td>
      <td>3</td>
      <td>2</td>
      <td>100.0</td>
      <td>org.slf4j</td>
      <td>1</td>
      <td>1</td>
      <td>50.000000</td>
      <td>7.692308</td>
      <td>[org.axonframework.extension.metrics.micrometer]</td>
      <td>[org.axonframework.extension.metrics.micromete...</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-modelling-5.0.1</td>
      <td>7</td>
      <td>93</td>
      <td>2</td>
      <td>7</td>
      <td>100.0</td>
      <td>jakarta.annotation</td>
      <td>7</td>
      <td>77</td>
      <td>100.000000</td>
      <td>82.795699</td>
      <td>[org.axonframework.modelling, org.axonframewor...</td>
      <td>[org.axonframework.modelling.EntityEvolvingCom...</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-modelling-5.0.1</td>
      <td>7</td>
      <td>93</td>
      <td>2</td>
      <td>7</td>
      <td>100.0</td>
      <td>org.slf4j</td>
      <td>3</td>
      <td>3</td>
      <td>42.857143</td>
      <td>3.225806</td>
      <td>[org.axonframework.modelling, org.axonframewor...</td>
      <td>[org.axonframework.modelling.SimpleEntityEvolv...</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>8</td>
      <td>5</td>
      <td>100.0</td>
      <td>io.axoniq</td>
      <td>5</td>
      <td>44</td>
      <td>100.000000</td>
      <td>61.111111</td>
      <td>[org.axonframework.axonserver.connector, org.a...</td>
      <td>[org.axonframework.axonserver.connector.Topolo...</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>8</td>
      <td>5</td>
      <td>100.0</td>
      <td>jakarta.annotation</td>
      <td>5</td>
      <td>25</td>
      <td>100.000000</td>
      <td>34.722222</td>
      <td>[org.axonframework.axonserver.connector, org.a...</td>
      <td>[org.axonframework.axonserver.connector.Metada...</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>8</td>
      <td>5</td>
      <td>100.0</td>
      <td>com.google</td>
      <td>4</td>
      <td>8</td>
      <td>80.000000</td>
      <td>11.111111</td>
      <td>[org.axonframework.axonserver.connector.util, ...</td>
      <td>[org.axonframework.axonserver.connector.util.G...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>8</td>
      <td>5</td>
      <td>100.0</td>
      <td>org.slf4j</td>
      <td>4</td>
      <td>12</td>
      <td>80.000000</td>
      <td>16.666667</td>
      <td>[org.axonframework.axonserver.connector.util, ...</td>
      <td>[org.axonframework.axonserver.connector.util.G...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>8</td>
      <td>5</td>
      <td>100.0</td>
      <td>io.grpc</td>
      <td>3</td>
      <td>10</td>
      <td>60.000000</td>
      <td>13.888889</td>
      <td>[org.axonframework.axonserver.connector, org.a...</td>
      <td>[org.axonframework.axonserver.connector.Manage...</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>8</td>
      <td>5</td>
      <td>100.0</td>
      <td>javax.annotation</td>
      <td>1</td>
      <td>1</td>
      <td>20.000000</td>
      <td>1.388889</td>
      <td>[org.axonframework.axonserver.connector]</td>
      <td>[org.axonframework.axonserver.connector.AxonSe...</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>8</td>
      <td>5</td>
      <td>100.0</td>
      <td>org.springframework</td>
      <td>1</td>
      <td>1</td>
      <td>20.000000</td>
      <td>1.388889</td>
      <td>[org.axonframework.axonserver.connector]</td>
      <td>[org.axonframework.axonserver.connector.AxonSe...</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>8</td>
      <td>5</td>
      <td>100.0</td>
      <td>reactor.core</td>
      <td>1</td>
      <td>1</td>
      <td>20.000000</td>
      <td>1.388889</td>
      <td>[org.axonframework.axonserver.connector.util]</td>
      <td>[org.axonframework.axonserver.connector.util.P...</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>7</td>
      <td>70</td>
      <td>8</td>
      <td>7</td>
      <td>100.0</td>
      <td>org.springframework</td>
      <td>6</td>
      <td>54</td>
      <td>85.714286</td>
      <td>77.142857</td>
      <td>[org.axonframework.extension.springboot, org.a...</td>
      <td>[org.axonframework.extension.springboot.EventP...</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>7</td>
      <td>70</td>
      <td>8</td>
      <td>7</td>
      <td>100.0</td>
      <td>jakarta.annotation</td>
      <td>4</td>
      <td>12</td>
      <td>57.142857</td>
      <td>17.142857</td>
      <td>[org.axonframework.extension.springboot, org.a...</td>
      <td>[org.axonframework.extension.springboot.EventP...</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>7</td>
      <td>70</td>
      <td>8</td>
      <td>7</td>
      <td>100.0</td>
      <td>org.axonframework</td>
      <td>3</td>
      <td>8</td>
      <td>42.857143</td>
      <td>11.428571</td>
      <td>[org.axonframework.extension.springboot, org.a...</td>
      <td>[org.axonframework.extension.springboot.EventP...</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>7</td>
      <td>70</td>
      <td>8</td>
      <td>7</td>
      <td>100.0</td>
      <td>jakarta.persistence</td>
      <td>2</td>
      <td>4</td>
      <td>28.571429</td>
      <td>5.714286</td>
      <td>[org.axonframework.extension.springboot.autoco...</td>
      <td>[org.axonframework.extension.springboot.autoco...</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>7</td>
      <td>70</td>
      <td>8</td>
      <td>7</td>
      <td>100.0</td>
      <td>org.slf4j</td>
      <td>2</td>
      <td>2</td>
      <td>28.571429</td>
      <td>2.857143</td>
      <td>[org.axonframework.extension.springboot.servic...</td>
      <td>[org.axonframework.extension.springboot.servic...</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>7</td>
      <td>70</td>
      <td>8</td>
      <td>7</td>
      <td>100.0</td>
      <td>com.fasterxml</td>
      <td>1</td>
      <td>4</td>
      <td>14.285714</td>
      <td>5.714286</td>
      <td>[org.axonframework.extension.springboot.autoco...</td>
      <td>[org.axonframework.extension.springboot.autoco...</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>7</td>
      <td>70</td>
      <td>8</td>
      <td>7</td>
      <td>100.0</td>
      <td>io.axoniq</td>
      <td>1</td>
      <td>1</td>
      <td>14.285714</td>
      <td>1.428571</td>
      <td>[org.axonframework.extension.springboot.autoco...</td>
      <td>[org.axonframework.extension.springboot.autoco...</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 7b - Top 15 external dependency using artifacts as columns with their external packages

The following table uses pivot to show the artifacts in columns, the external dependencies in rows and the number of internal packages as values.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>artifactName</th>
      <th>axon-messaging-5.0.1</th>
      <th>axon-spring-boot-autoconfigure-5.0.1</th>
      <th>axon-server-connector-5.0.1</th>
      <th>axon-common-5.0.1</th>
      <th>axon-conversion-5.0.1</th>
      <th>axon-test-5.0.1</th>
      <th>axon-eventsourcing-5.0.1</th>
      <th>axon-modelling-5.0.1</th>
      <th>axon-update-5.0.1</th>
      <th>axon-tracing-opentelemetry-5.0.1</th>
      <th>axon-metrics-micrometer-5.0.1</th>
    </tr>
    <tr>
      <th>externalPackageName</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>IdTypeParameterResolver</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>ScannedEntityCreator</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>WrappedEventCriteriaBuilderMethod</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>com.fasterxml.jackson.annotation</th>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>com.fasterxml.jackson.core</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>org.testcontainers.containers.wait.strategy</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>org.testcontainers.utility</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>reactor.core.publisher</th>
      <td>5</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>reactor.core.scheduler</th>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>reactor.util.concurrent</th>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>89 rows × 11 columns</p>
</div>



#### Table 7c - Top 15 external dependency using artifacts as columns with their external packages (first 2 levels)

The following table uses pivot to show the artifacts in columns, the external package name grouped by its first two levels in rows and the number of internal packages as values. For example `javax.xml.namespace` and `javax.xml.stream` will be grouped together to `javax.xml`.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>artifactName</th>
      <th>axon-messaging-5.0.1</th>
      <th>axon-server-connector-5.0.1</th>
      <th>axon-spring-boot-autoconfigure-5.0.1</th>
      <th>axon-common-5.0.1</th>
      <th>axon-eventsourcing-5.0.1</th>
      <th>axon-test-5.0.1</th>
      <th>axon-modelling-5.0.1</th>
      <th>axon-conversion-5.0.1</th>
      <th>axon-update-5.0.1</th>
      <th>axon-metrics-micrometer-5.0.1</th>
      <th>axon-tracing-opentelemetry-5.0.1</th>
    </tr>
    <tr>
      <th>externalPackageNameFirst2Levels</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>IdTypeParameterResolver</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>ScannedEntityCreator</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>WrappedEventCriteriaBuilderMethod</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>com.fasterxml</th>
      <td>3</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>com.google</th>
      <td>0</td>
      <td>4</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>io.axoniq</th>
      <td>0</td>
      <td>5</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>io.grpc</th>
      <td>0</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>io.micrometer</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>io.opentelemetry</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>jakarta.annotation</th>
      <td>56</td>
      <td>5</td>
      <td>4</td>
      <td>6</td>
      <td>7</td>
      <td>3</td>
      <td>7</td>
      <td>4</td>
      <td>4</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>jakarta.persistence</th>
      <td>1</td>
      <td>0</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>jakarta.validation</th>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>javax.annotation</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>javax.cache</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>org.apache</th>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>org.awaitility</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>org.axonframework</th>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>org.ehcache</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>org.hamcrest</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>org.jetbrains</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>org.junit</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>org.reactivestreams</th>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>org.slf4j</th>
      <td>14</td>
      <td>4</td>
      <td>2</td>
      <td>4</td>
      <td>2</td>
      <td>1</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>org.springframework</th>
      <td>0</td>
      <td>1</td>
      <td>6</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>org.testcontainers</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>reactor.core</th>
      <td>5</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>reactor.util</th>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 7 Chart 1 - Top 15 external dependency using artifacts and their external packages stacked

The following chart shows the top 15 external package using artifacts and breaks down which external packages they use in how many different internal packages with stacked bars. 

Note that every external dependency is counted separately so that if on internal package uses two external packages it will be displayed for both and so stacked twice.  


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_74_1.png)
    


#### Table 7 Chart 2 - Top 15 external dependency using artifacts and their external packages (first 2 levels) stacked

The following chart shows the top 15 external package using artifacts and breaks down which external packages (first 2 levels) are used in how many different internal packages with stacked bars. 

Note that every external dependency is counted separately so that if on internal package uses two external packages it will be displayed for both and so stacked twice.  


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_76_1.png)
    


### Table 8 - External usage per artifact

The following table shows the most used external packages separately for each artifact including external annotations. The results are grouped per artifact and sorted by the artifacts with the highest external type usage rate descending. Additionally, for each artifact the top 5 used external packages are listed in the top5ExternalPackages column. 

The intention of this table is to find artifacts that use a lot of external dependencies in relation to their size and get an overview per artifact with the top 5 used external packages, the number of external types and packages used etc. .

Only the last 40 entries are shown. The whole table can be found in the following CSV report:
`External_package_usage_per_artifact_sorted_top`

**Columns:**
- *artifactName* is used to group the the external package usage per artifact for a more detailed analysis.
- *numberOfTypesInArtifact* represents the total count of all analyzed types for the artifact
- *numberOfExternalTypesInArtifact* is the number of all external types that are used by the artifact
- *numberOfExternalPackagesInArtifact* is the number of all external packages that are used by the artifact
- *externalTypeRate* is the numberOfExternalTypesInArtifact / numberOfTypesInArtifact * 100
- *numberOfExternalTypeCaller* refers to the distinct types that make use of the external package
- *numberOfExternalTypeCalls* includes every invocation or reference to the types in the external package
- *numberOfExternalPackages* is the number of distinct external packages used by the artifact
- *top5ExternalPackages* contains a list of the top 5 most used external packages of the artifact
- *someExternalTypes* contains a list of lists and is also mean't to provide some examples of external types used




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>numberOfTypesInArtifact</th>
      <th>numberOfExternalTypesInArtifact</th>
      <th>numberOfExternalPackagesInArtifact</th>
      <th>externalTypeRate</th>
      <th>numberOfExternalTypeCaller</th>
      <th>numberOfExternalTypeCalls</th>
      <th>numberOfExternalPackages</th>
      <th>top5ExternalPackages</th>
      <th>someExternalTypes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>5</td>
      <td>16</td>
      <td>6</td>
      <td>320.000000</td>
      <td>26</td>
      <td>85</td>
      <td>6</td>
      <td>[io.opentelemetry.api.trace, io.opentelemetry....</td>
      <td>[Tracer, SpanKind, SpanBuilder, Span, StatusCo...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-server-connector-5.0.1</td>
      <td>72</td>
      <td>113</td>
      <td>23</td>
      <td>156.944444</td>
      <td>244</td>
      <td>1215</td>
      <td>23</td>
      <td>[io.axoniq.axonserver.grpc, jakarta.annotation...</td>
      <td>[ErrorMessage, ProcessingInstruction$Builder, ...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>70</td>
      <td>87</td>
      <td>36</td>
      <td>124.285714</td>
      <td>220</td>
      <td>411</td>
      <td>36</td>
      <td>[org.springframework.boot.autoconfigure.condit...</td>
      <td>[ConditionalOnProperty, ConditionalOnMissingBe...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-conversion-5.0.1</td>
      <td>30</td>
      <td>32</td>
      <td>11</td>
      <td>106.666667</td>
      <td>99</td>
      <td>421</td>
      <td>11</td>
      <td>[jakarta.annotation, org.apache.avro, com.fast...</td>
      <td>[Nonnull, Nullable, SchemaCompatibility$Incomp...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>13</td>
      <td>13</td>
      <td>4</td>
      <td>100.000000</td>
      <td>46</td>
      <td>152</td>
      <td>4</td>
      <td>[io.micrometer.core.instrument, jakarta.annota...</td>
      <td>[Clock, Counter, Tag, MeterRegistry, Timer, Ti...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-test-5.0.1</td>
      <td>73</td>
      <td>24</td>
      <td>11</td>
      <td>32.876712</td>
      <td>94</td>
      <td>456</td>
      <td>11</td>
      <td>[org.hamcrest, jakarta.annotation, com.google....</td>
      <td>[Matcher, Description, TypeSafeMatcher, BaseMa...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>100</td>
      <td>20</td>
      <td>6</td>
      <td>20.000000</td>
      <td>102</td>
      <td>419</td>
      <td>6</td>
      <td>[jakarta.annotation, jakarta.persistence, org....</td>
      <td>[Nonnull, Nullable, EntityExistsException, Typ...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-common-5.0.1</td>
      <td>150</td>
      <td>28</td>
      <td>11</td>
      <td>18.666667</td>
      <td>109</td>
      <td>524</td>
      <td>11</td>
      <td>[jakarta.annotation, org.slf4j, javax.cache.ev...</td>
      <td>[Nonnull, Nullable, Logger, LoggerFactory, Cac...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-update-5.0.1</td>
      <td>23</td>
      <td>4</td>
      <td>2</td>
      <td>17.391304</td>
      <td>28</td>
      <td>129</td>
      <td>2</td>
      <td>[jakarta.annotation, org.slf4j]</td>
      <td>[Nonnull, Nullable, Logger, LoggerFactory]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-messaging-5.0.1</td>
      <td>570</td>
      <td>32</td>
      <td>8</td>
      <td>5.614035</td>
      <td>602</td>
      <td>3181</td>
      <td>8</td>
      <td>[jakarta.annotation, org.slf4j, com.fasterxml....</td>
      <td>[Nonnull, Nullable, Logger, LoggerFactory, Jso...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-modelling-5.0.1</td>
      <td>93</td>
      <td>4</td>
      <td>2</td>
      <td>4.301075</td>
      <td>92</td>
      <td>586</td>
      <td>2</td>
      <td>[jakarta.annotation, org.slf4j]</td>
      <td>[Nonnull, Nullable, LoggerFactory, Logger]</td>
    </tr>
  </tbody>
</table>
</div>



### Table 9 - External usage per artifact and package

This table lists internal packages and the artifacts they belong to that use many different external types of a specific external package without taking external annotations into account. 

Only the last 40 entries are shown. The whole table can be found in the following CSV report:
`External_package_usage_per_artifact_and_package`

**Columns:**
- *artifactName* that contains the type that calls the external package
- *fullPackageName* is the package within the artifact that contains the type that calls the external package
- *externalPackageName* identifies the external package as described above
- *numberOfExternalTypeCaller* refers to the distinct types that make use of the external package
- *numberOfExternalTypeCalls* includes every invocation or reference to the types in the external package
- *numberOfTypesInPackage* represents the total count of all types in that package
- *externalTypeNames* contains a list of actually utilized types of the external package
- *packageName* contains the name of the package (last part of *fullPackageName*)




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>fullPackageName</th>
      <th>externalPackageName</th>
      <th>numberOfExternalTypeCaller</th>
      <th>numberOfExternalTypeCalls</th>
      <th>numberOfTypesInPackage</th>
      <th>externalTypeNames</th>
      <th>packageName</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>org.axonframework.extension.metrics.micrometer</td>
      <td>io.micrometer.core.instrument</td>
      <td>37</td>
      <td>136</td>
      <td>12</td>
      <td>[MeterRegistry, Tags, Clock, Tag, Timer$Builde...</td>
      <td>micrometer</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-test-5.0.1</td>
      <td>org.axonframework.test.matchers</td>
      <td>org.hamcrest</td>
      <td>36</td>
      <td>142</td>
      <td>23</td>
      <td>[Description, Matcher, BaseMatcher, TypeSafeMa...</td>
      <td>matchers</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>io.axoniq.axonserver.grpc.event.dcb</td>
      <td>28</td>
      <td>104</td>
      <td>14</td>
      <td>[Tag, Tag$Builder, ConsistencyCondition$Builde...</td>
      <td>event</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>io.grpc</td>
      <td>17</td>
      <td>35</td>
      <td>13</td>
      <td>[ClientCall$Listener, ForwardingClientCallList...</td>
      <td>util</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-conversion-5.0.1</td>
      <td>org.axonframework.conversion.avro</td>
      <td>org.apache.avro</td>
      <td>16</td>
      <td>54</td>
      <td>10</td>
      <td>[AvroRuntimeException, Schema, SchemaCompatibi...</td>
      <td>avro</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.proc...</td>
      <td>org.slf4j</td>
      <td>15</td>
      <td>72</td>
      <td>24</td>
      <td>[LoggerFactory, Logger]</td>
      <td>pooled</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>io.axoniq.axonserver.grpc.query</td>
      <td>14</td>
      <td>98</td>
      <td>11</td>
      <td>[QueryUpdate, QueryResponse$Builder, QueryResp...</td>
      <td>query</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>io.axoniq.axonserver.grpc</td>
      <td>12</td>
      <td>94</td>
      <td>28</td>
      <td>[ErrorMessage, ErrorMessage$Builder, Instructi...</td>
      <td>connector</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>org.slf4j</td>
      <td>10</td>
      <td>44</td>
      <td>14</td>
      <td>[LoggerFactory, Logger]</td>
      <td>event</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>io.axoniq.axonserver.connector</td>
      <td>10</td>
      <td>37</td>
      <td>11</td>
      <td>[ResultStream, FlowControl, ReplyChannel, Regi...</td>
      <td>query</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>io.axoniq.axonserver.grpc</td>
      <td>9</td>
      <td>50</td>
      <td>11</td>
      <td>[MetaDataValue$Builder, MetaDataValue, Process...</td>
      <td>query</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>io.opentelemetry.context.propagation</td>
      <td>9</td>
      <td>15</td>
      <td>5</td>
      <td>[TextMapSetter, TextMapPropagator, TextMapGett...</td>
      <td>opentelemetry</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>org.axonframework.extension.tracing.opentelemetry</td>
      <td>io.opentelemetry.api.trace</td>
      <td>9</td>
      <td>46</td>
      <td>5</td>
      <td>[Span, StatusCode, SpanContext, SpanBuilder, S...</td>
      <td>opentelemetry</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.caching</td>
      <td>org.ehcache.event</td>
      <td>8</td>
      <td>30</td>
      <td>13</td>
      <td>[EventType, EventOrdering, EventFiring, CacheE...</td>
      <td>caching</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.caching</td>
      <td>javax.cache.event</td>
      <td>8</td>
      <td>26</td>
      <td>13</td>
      <td>[CacheEntryCreatedListener, CacheEntryListener...</td>
      <td>caching</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-conversion-5.0.1</td>
      <td>org.axonframework.conversion.avro</td>
      <td>org.apache.avro.message</td>
      <td>8</td>
      <td>28</td>
      <td>10</td>
      <td>[SchemaStore, BinaryMessageEncoder, BinaryMess...</td>
      <td>avro</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-conversion-5.0.1</td>
      <td>org.axonframework.conversion.json</td>
      <td>com.fasterxml.jackson.databind</td>
      <td>8</td>
      <td>42</td>
      <td>5</td>
      <td>[JsonNode, ObjectMapper, JavaType]</td>
      <td>json</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.annotation</td>
      <td>org.slf4j</td>
      <td>8</td>
      <td>17</td>
      <td>50</td>
      <td>[LoggerFactory, Logger]</td>
      <td>annotation</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>io.axoniq.axonserver.grpc.control</td>
      <td>8</td>
      <td>46</td>
      <td>28</td>
      <td>[TopologyChange, QuerySubscription, CommandSub...</td>
      <td>connector</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.command</td>
      <td>io.axoniq.axonserver.grpc.command</td>
      <td>8</td>
      <td>63</td>
      <td>6</td>
      <td>[CommandResponse$Builder, Command$Builder, Com...</td>
      <td>command</td>
    </tr>
    <tr>
      <th>20</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>io.axoniq.axonserver.connector.event</td>
      <td>8</td>
      <td>38</td>
      <td>14</td>
      <td>[AggregateEventStream, AppendEventsTransaction...</td>
      <td>event</td>
    </tr>
    <tr>
      <th>21</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.util</td>
      <td>io.axoniq.axonserver.grpc</td>
      <td>8</td>
      <td>81</td>
      <td>13</td>
      <td>[ErrorMessage, SerializedObject, ErrorMessage$...</td>
      <td>util</td>
    </tr>
    <tr>
      <th>22</th>
      <td>axon-update-5.0.1</td>
      <td>org.axonframework.update</td>
      <td>org.slf4j</td>
      <td>8</td>
      <td>27</td>
      <td>5</td>
      <td>[Logger, LoggerFactory]</td>
      <td>update</td>
    </tr>
    <tr>
      <th>23</th>
      <td>axon-conversion-5.0.1</td>
      <td>org.axonframework.conversion.avro</td>
      <td>org.apache.avro.generic</td>
      <td>7</td>
      <td>30</td>
      <td>10</td>
      <td>[GenericRecord, GenericData, GenericDatumReader]</td>
      <td>avro</td>
    </tr>
    <tr>
      <th>24</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>org.axonframework.eventsourcing.eventstore.jpa</td>
      <td>jakarta.persistence</td>
      <td>7</td>
      <td>41</td>
      <td>13</td>
      <td>[Index, GenerationType, EntityExistsException,...</td>
      <td>jpa</td>
    </tr>
    <tr>
      <th>25</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>org.axonframework.eventsourcing.eventstore.jpa</td>
      <td>org.slf4j</td>
      <td>7</td>
      <td>16</td>
      <td>13</td>
      <td>[Logger, LoggerFactory]</td>
      <td>jpa</td>
    </tr>
    <tr>
      <th>26</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>reactor.core.publisher</td>
      <td>7</td>
      <td>30</td>
      <td>80</td>
      <td>[Flux, Mono, FluxSink]</td>
      <td>core</td>
    </tr>
    <tr>
      <th>27</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.command</td>
      <td>io.axoniq.axonserver.grpc</td>
      <td>7</td>
      <td>31</td>
      <td>6</td>
      <td>[SerializedObject$Builder, ProcessingInstructi...</td>
      <td>command</td>
    </tr>
    <tr>
      <th>28</th>
      <td>axon-test-5.0.1</td>
      <td>org.axonframework.test.fixture</td>
      <td>org.hamcrest</td>
      <td>7</td>
      <td>45</td>
      <td>31</td>
      <td>[Matcher, StringDescription, Description, Core...</td>
      <td>fixture</td>
    </tr>
    <tr>
      <th>29</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.query</td>
      <td>io.axoniq.axonserver.connector.query</td>
      <td>6</td>
      <td>19</td>
      <td>11</td>
      <td>[SubscriptionQueryResult, QueryDefinition, Que...</td>
      <td>query</td>
    </tr>
    <tr>
      <th>30</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>org.axonframework.extension.spring.config</td>
      <td>6</td>
      <td>27</td>
      <td>34</td>
      <td>[EventProcessorSettings$MapWrapper, SpringComp...</td>
      <td>autoconfig</td>
    </tr>
    <tr>
      <th>31</th>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common</td>
      <td>org.slf4j</td>
      <td>5</td>
      <td>14</td>
      <td>34</td>
      <td>[Logger, LoggerFactory]</td>
      <td>common</td>
    </tr>
    <tr>
      <th>32</th>
      <td>axon-common-5.0.1</td>
      <td>org.axonframework.common.configuration</td>
      <td>org.slf4j</td>
      <td>5</td>
      <td>27</td>
      <td>46</td>
      <td>[Logger, LoggerFactory]</td>
      <td>configuration</td>
    </tr>
    <tr>
      <th>33</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core</td>
      <td>org.reactivestreams</td>
      <td>5</td>
      <td>10</td>
      <td>80</td>
      <td>[Subscription, Subscriber, Publisher]</td>
      <td>core</td>
    </tr>
    <tr>
      <th>34</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.core.interception</td>
      <td>jakarta.validation</td>
      <td>5</td>
      <td>16</td>
      <td>19</td>
      <td>[ConstraintViolation, ValidatorFactory, Valida...</td>
      <td>interception</td>
    </tr>
    <tr>
      <th>35</th>
      <td>axon-messaging-5.0.1</td>
      <td>org.axonframework.messaging.eventhandling.proc...</td>
      <td>jakarta.persistence</td>
      <td>5</td>
      <td>54</td>
      <td>4</td>
      <td>[LockModeType, EntityManager, Query, TypedQuery]</td>
      <td>jpa</td>
    </tr>
    <tr>
      <th>36</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>io.axoniq.axonserver.connector</td>
      <td>5</td>
      <td>38</td>
      <td>28</td>
      <td>[AxonServerConnection, AxonServerConnectionFac...</td>
      <td>connector</td>
    </tr>
    <tr>
      <th>37</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>io.axoniq.axonserver.grpc.event</td>
      <td>5</td>
      <td>31</td>
      <td>14</td>
      <td>[Event$Builder, Event, EventWithToken, Confirm...</td>
      <td>event</td>
    </tr>
    <tr>
      <th>38</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>io.axoniq.axonserver.connector</td>
      <td>5</td>
      <td>37</td>
      <td>14</td>
      <td>[AxonServerConnection, ResultStream]</td>
      <td>event</td>
    </tr>
    <tr>
      <th>39</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>io.axoniq.axonserver.grpc.control</td>
      <td>5</td>
      <td>40</td>
      <td>14</td>
      <td>[EventProcessorInfo, EventProcessorInfo$Segmen...</td>
      <td>event</td>
    </tr>
  </tbody>
</table>
</div>



### Table 10 - Top 20 external package usage per type

This table shows internal types that utilize the most different external types and packages. These have the highest probability of change depending on external libraries. A case-by-case approach is also advisable here because there could for example also be code units that encapsulate an external library and have this high count of external dependencies on purpose.

Only the last 20 entries are shown. The whole table can be found in the following CSV report:
`External_package_usage_per_type`

**Columns:**
- *artifactName* that contains the type that calls the external package
- *fullPackageName* is the package within the artifact that contains the type that calls external types
- *typeName* identifies the internal type within the package and artifact that calls external types
- *numberOfExternalTypeCaller* and *numberOfExternalTypes* refers to the distinct external types that are used by the internal type
- *numberOfExternalTypeCalls* includes every invocation or reference to the types in the external package
- *numberOfTypesInPackage* represents the total count of all types in that package
- *numberOfExternalPackages* shows how many different external packages are used by the internal type
- *externalPackageNames* contains the list of names of the different external packages that are used by the internal type
- *externalTypeNames* contains a list of actually utilized types of the external package
- *packageName* contains the name of the package (last part of *fullPackageName*)




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>fullPackageName</th>
      <th>typeName</th>
      <th>numberOfExternalTypeCaller</th>
      <th>numberOfExternalTypeCalls</th>
      <th>numberOfExternalPackages</th>
      <th>numberOfExternalTypes</th>
      <th>externalPackageNames</th>
      <th>externalTypeNames</th>
      <th>packageName</th>
      <th>fullTypeName</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>ConverterAutoConfiguration</td>
      <td>16</td>
      <td>45</td>
      <td>11</td>
      <td>16</td>
      <td>[jakarta.annotation, org.springframework.boot....</td>
      <td>[jakarta.annotation.Nonnull, org.springframewo...</td>
      <td>autoconfig</td>
      <td>org.axonframework.extension.springboot.autocon...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>AxonServerAutoConfiguration</td>
      <td>14</td>
      <td>22</td>
      <td>10</td>
      <td>14</td>
      <td>[jakarta.annotation, org.springframework.boot....</td>
      <td>[jakarta.annotation.Nonnull, org.springframewo...</td>
      <td>autoconfig</td>
      <td>org.axonframework.extension.springboot.autocon...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>AvroSchemaStoreAutoConfiguration</td>
      <td>14</td>
      <td>28</td>
      <td>8</td>
      <td>14</td>
      <td>[org.springframework.boot.autoconfigure, org.s...</td>
      <td>[org.springframework.boot.autoconfigure.AutoCo...</td>
      <td>autoconfig</td>
      <td>org.axonframework.extension.springboot.autocon...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.util</td>
      <td>AbstractQualifiedBeanCondition</td>
      <td>12</td>
      <td>24</td>
      <td>8</td>
      <td>12</td>
      <td>[jakarta.annotation, org.springframework.conte...</td>
      <td>[jakarta.annotation.Nonnull, org.springframewo...</td>
      <td>util</td>
      <td>org.axonframework.extension.springboot.util.Ab...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>JpaEventStoreAutoConfiguration</td>
      <td>8</td>
      <td>8</td>
      <td>7</td>
      <td>8</td>
      <td>[org.springframework.boot.autoconfigure, org.s...</td>
      <td>[org.springframework.boot.autoconfigure.AutoCo...</td>
      <td>autoconfig</td>
      <td>org.axonframework.extension.springboot.autocon...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector</td>
      <td>AxonServerConnectionManager$Builder</td>
      <td>9</td>
      <td>45</td>
      <td>6</td>
      <td>9</td>
      <td>[io.axoniq.axonserver.connector, io.axoniq.axo...</td>
      <td>[io.axoniq.axonserver.connector.AxonServerConn...</td>
      <td>connector</td>
      <td>org.axonframework.axonserver.connector.AxonSer...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>AggregateBasedAxonServerEventStorageEngine</td>
      <td>13</td>
      <td>69</td>
      <td>6</td>
      <td>13</td>
      <td>[io.axoniq.axonserver.grpc, jakarta.annotation...</td>
      <td>[io.axoniq.axonserver.grpc.MetaDataValue$Build...</td>
      <td>event</td>
      <td>org.axonframework.axonserver.connector.event.A...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>EventProcessorControlService</td>
      <td>7</td>
      <td>31</td>
      <td>6</td>
      <td>7</td>
      <td>[jakarta.annotation, org.slf4j, io.axoniq.axon...</td>
      <td>[jakarta.annotation.Nonnull, org.slf4j.Logger,...</td>
      <td>event</td>
      <td>org.axonframework.axonserver.connector.event.E...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>TransactionAutoConfiguration</td>
      <td>7</td>
      <td>9</td>
      <td>6</td>
      <td>7</td>
      <td>[org.springframework.boot.autoconfigure, org.s...</td>
      <td>[org.springframework.boot.autoconfigure.AutoCo...</td>
      <td>autoconfig</td>
      <td>org.axonframework.extension.springboot.autocon...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>JpaAutoConfiguration</td>
      <td>8</td>
      <td>13</td>
      <td>6</td>
      <td>8</td>
      <td>[org.springframework.boot.autoconfigure, org.s...</td>
      <td>[org.springframework.boot.autoconfigure.AutoCo...</td>
      <td>autoconfig</td>
      <td>org.axonframework.extension.springboot.autocon...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.util</td>
      <td>DefaultEntityRegistrar</td>
      <td>6</td>
      <td>7</td>
      <td>6</td>
      <td>6</td>
      <td>[jakarta.annotation, org.springframework.boot....</td>
      <td>[jakarta.annotation.Nonnull, org.springframewo...</td>
      <td>util</td>
      <td>org.axonframework.extension.springboot.util.De...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>axon-conversion-5.0.1</td>
      <td>org.axonframework.conversion.avro</td>
      <td>SpecificRecordBaseConverterStrategy</td>
      <td>8</td>
      <td>38</td>
      <td>5</td>
      <td>8</td>
      <td>[jakarta.annotation, org.apache.avro.generic, ...</td>
      <td>[jakarta.annotation.Nonnull, org.apache.avro.g...</td>
      <td>avro</td>
      <td>org.axonframework.conversion.avro.SpecificReco...</td>
    </tr>
    <tr>
      <th>12</th>
      <td>axon-conversion-5.0.1</td>
      <td>org.axonframework.conversion.avro</td>
      <td>AvroUtil</td>
      <td>16</td>
      <td>71</td>
      <td>5</td>
      <td>16</td>
      <td>[jakarta.annotation, org.apache.avro, org.apac...</td>
      <td>[jakarta.annotation.Nonnull, org.apache.avro.S...</td>
      <td>avro</td>
      <td>org.axonframework.conversion.avro.AvroUtil</td>
    </tr>
    <tr>
      <th>13</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.command</td>
      <td>AxonServerCommandBusConnector</td>
      <td>9</td>
      <td>40</td>
      <td>5</td>
      <td>9</td>
      <td>[jakarta.annotation, org.slf4j, io.axoniq.axon...</td>
      <td>[jakarta.annotation.Nonnull, org.slf4j.Logger,...</td>
      <td>command</td>
      <td>org.axonframework.axonserver.connector.command...</td>
    </tr>
    <tr>
      <th>14</th>
      <td>axon-server-connector-5.0.1</td>
      <td>org.axonframework.axonserver.connector.event</td>
      <td>AxonServerEventStorageEngine</td>
      <td>12</td>
      <td>53</td>
      <td>5</td>
      <td>12</td>
      <td>[jakarta.annotation, org.slf4j, io.axoniq.axon...</td>
      <td>[jakarta.annotation.Nonnull, org.slf4j.Logger,...</td>
      <td>event</td>
      <td>org.axonframework.axonserver.connector.event.A...</td>
    </tr>
    <tr>
      <th>15</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>AxonTimeoutAutoConfiguration</td>
      <td>5</td>
      <td>6</td>
      <td>5</td>
      <td>5</td>
      <td>[jakarta.annotation, org.springframework.boot....</td>
      <td>[jakarta.annotation.Nonnull, org.springframewo...</td>
      <td>autoconfig</td>
      <td>org.axonframework.extension.springboot.autocon...</td>
    </tr>
    <tr>
      <th>16</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>AxonAutoConfiguration</td>
      <td>9</td>
      <td>37</td>
      <td>5</td>
      <td>9</td>
      <td>[org.springframework.boot.autoconfigure, org.s...</td>
      <td>[org.springframework.boot.autoconfigure.AutoCo...</td>
      <td>autoconfig</td>
      <td>org.axonframework.extension.springboot.autocon...</td>
    </tr>
    <tr>
      <th>17</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>ObjectMapperAutoConfiguration</td>
      <td>9</td>
      <td>12</td>
      <td>5</td>
      <td>9</td>
      <td>[org.springframework.boot.autoconfigure, org.s...</td>
      <td>[org.springframework.boot.autoconfigure.AutoCo...</td>
      <td>autoconfig</td>
      <td>org.axonframework.extension.springboot.autocon...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>org.axonframework.extension.springboot.autoconfig</td>
      <td>CBORMapperAutoConfiguration</td>
      <td>8</td>
      <td>13</td>
      <td>5</td>
      <td>8</td>
      <td>[org.springframework.boot.autoconfigure, org.s...</td>
      <td>[org.springframework.boot.autoconfigure.AutoCo...</td>
      <td>autoconfig</td>
      <td>org.axonframework.extension.springboot.autocon...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>axon-conversion-5.0.1</td>
      <td>org.axonframework.conversion.avro</td>
      <td>AvroConverter</td>
      <td>6</td>
      <td>34</td>
      <td>4</td>
      <td>6</td>
      <td>[org.slf4j, jakarta.annotation, org.apache.avr...</td>
      <td>[org.slf4j.Logger, jakarta.annotation.Nonnull,...</td>
      <td>avro</td>
      <td>org.axonframework.conversion.avro.AvroConverter</td>
    </tr>
  </tbody>
</table>
</div>



### Table 11 - External package usage distribution per type

This table shows how many types use one external package, how many use two, etc. .
This gives an overview of the distribution of external package calls and the overall coupling to external libraries. The higher the count of distinct external packages the lower should be the count of types that use them. Dependencies to external annotations are left out here.

More details about which types have the highest external package dependency usage can be in the tables 4 and 5 above.

Only the last 40 entries are shown. The whole table can be found in the following CSV report:
`External_package_usage_per_artifact_distribution`

**Columns:**
- *artifactName* that contains the type that calls the external package
- *artifactTypes* the total count of types in the artifact
- *numberOfExternalPackages* the number of distinct external packages used
- *numberOfTypes* in the artifact where the *numberOfExternalPackages* applies
- *numberOfTypesPercentage* in the artifact where the *numberOfExternalPackages* applies in %




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>artifactPackages</th>
      <th>artifactTypes</th>
      <th>numberOfExternalPackages</th>
      <th>numberOfPackages</th>
      <th>numberOfTypes</th>
      <th>typesCallingExternalRate</th>
      <th>packagesCallingExternalRate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-messaging-5.0.1</td>
      <td>57</td>
      <td>570</td>
      <td>7</td>
      <td>18</td>
      <td>45</td>
      <td>7.894737</td>
      <td>31.578947</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-common-5.0.1</td>
      <td>13</td>
      <td>150</td>
      <td>10</td>
      <td>7</td>
      <td>16</td>
      <td>10.666667</td>
      <td>53.846154</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>7</td>
      <td>70</td>
      <td>31</td>
      <td>7</td>
      <td>31</td>
      <td>44.285714</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>72</td>
      <td>20</td>
      <td>5</td>
      <td>51</td>
      <td>70.833333</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>100</td>
      <td>5</td>
      <td>4</td>
      <td>9</td>
      <td>9.000000</td>
      <td>57.142857</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-test-5.0.1</td>
      <td>5</td>
      <td>73</td>
      <td>9</td>
      <td>4</td>
      <td>24</td>
      <td>32.876712</td>
      <td>80.000000</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>30</td>
      <td>10</td>
      <td>3</td>
      <td>15</td>
      <td>50.000000</td>
      <td>75.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-modelling-5.0.1</td>
      <td>7</td>
      <td>93</td>
      <td>1</td>
      <td>3</td>
      <td>3</td>
      <td>3.225806</td>
      <td>42.857143</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-update-5.0.1</td>
      <td>5</td>
      <td>23</td>
      <td>1</td>
      <td>3</td>
      <td>7</td>
      <td>30.434783</td>
      <td>60.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>2</td>
      <td>13</td>
      <td>3</td>
      <td>2</td>
      <td>12</td>
      <td>92.307692</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>1</td>
      <td>5</td>
      <td>5</td>
      <td>1</td>
      <td>5</td>
      <td>100.000000</td>
      <td>100.000000</td>
    </tr>
  </tbody>
</table>
</div>



### Table 12 - External package usage per artifact grouped by number of internal packages

The following table shows the external package usage for every artifact grouped by the number of distinct internal dependent packages. The intention is to find external package usage spread across multiple internal packages in artifacts. 

Artifacts that encapsulate external dependency calls in one internal package overall (or each) are easier to change if those external dependencies change and are most likely applying a [Hexagonal architecture](https://alistair.cockburn.us/hexagonal-architecture). Artifacts that use external dependencies in multiple internal packages need more effort to adapt to changes of those external dependencies. On one hand this could be intended e.g. when using standardized libraries. On the other hand this might indicate higher than necessary coupling.

The whole table can be found in the following CSV report:
`External_package_usage_per_internal_package_count`




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>artifactName</th>
      <th>axon-common-5.0.1</th>
      <th>axon-conversion-5.0.1</th>
      <th>axon-eventsourcing-5.0.1</th>
      <th>axon-messaging-5.0.1</th>
      <th>axon-metrics-micrometer-5.0.1</th>
      <th>axon-modelling-5.0.1</th>
      <th>axon-server-connector-5.0.1</th>
      <th>axon-spring-boot-autoconfigure-5.0.1</th>
      <th>axon-test-5.0.1</th>
      <th>axon-update-5.0.1</th>
    </tr>
    <tr>
      <th>numberOfPackages</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>0.000000</td>
      <td>0.0</td>
      <td>28.571429</td>
      <td>0.000000</td>
      <td>100.0</td>
      <td>0.000000</td>
      <td>40.0</td>
      <td>28.571429</td>
      <td>40.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.000000</td>
      <td>75.0</td>
      <td>0.000000</td>
      <td>5.263158</td>
      <td>0.0</td>
      <td>42.857143</td>
      <td>60.0</td>
      <td>42.857143</td>
      <td>60.0</td>
      <td>60.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>30.769231</td>
      <td>100.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>80.0</td>
      <td>57.142857</td>
      <td>0.0</td>
      <td>80.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>8.771930</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>100.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>46.153846</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0.000000</td>
      <td>0.0</td>
      <td>100.000000</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>100.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>24.561404</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>56</th>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>98.245614</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>



### Table 13 - External package usage aggregated

This table lists all artifacts and their external package dependencies usage aggregated over internal packages. 

The intention behind this is to find artifacts that use an external dependency across multiple internal packages. This might be intended for frameworks and standardized libraries and helps to quantify how widely those are used. For some external dependencies it might be beneficial to only access it from one package and provide an abstraction for internal usage following a [Hexagonal architecture](https://alistair.cockburn.us/hexagonal-architecture). Thus, this table may also help in finding application for the Hexagonal architecture or similar approaches (Domain Driven Design Anti Corruption Layer). After all it is easier to update or replace such external dependencies when they are used in specific areas and not all over the code.

Only the last 40 entries are shown. The whole table can be found in the following CSV report:
`External_package_usage_per_artifact_package_aggregated`

**Columns:**
- *artifactName* that contains the type that calls the external package
- *artifactPackages* is the total count of packages in the artifact
- *artifactTypes* is the total count of types in the artifact
- *numberOfExternalPackages* the number of distinct external packages used
- *[min,max,med,avg,std]NumberOfPackages* provide statistics based on each external package and its package usage within the artifact
- *[min,max,med,avg,std]NumberOfPackagesPercentage* provide statistics in % based on each external package and its package usage within the artifact in respect to the overall count of packages in the artifact
- *[min,max,med,avg,std]NumberOfTypes* provide statistics based on each external package and its type usage within the artifact
- *[min,max,med,avg,std]NumberOfTypePercentage* provide statistics in % based on each external package and its type usage within the artifact in respect to the overall count of packages in the artifact
- *numberOfTypes* in the artifact where the *numberOfExternalPackages* applies
- *numberOfTypesPercentage* in the artifact where the *numberOfExternalPackages* applies in %

#### Table 13a - External package usage aggregated - count of internal packages




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>artifactPackages</th>
      <th>numberOfExternalPackages</th>
      <th>minNumberOfPackages</th>
      <th>medNumberOfPackages</th>
      <th>avgNumberOfPackages</th>
      <th>maxNumberOfPackages</th>
      <th>stdNumberOfPackages</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-messaging-5.0.1</td>
      <td>57</td>
      <td>7</td>
      <td>1</td>
      <td>1.0</td>
      <td>3.714286</td>
      <td>14</td>
      <td>4.785892</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>20</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.900000</td>
      <td>5</td>
      <td>1.333772</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-common-5.0.1</td>
      <td>13</td>
      <td>10</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.300000</td>
      <td>4</td>
      <td>0.948683</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>10</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.200000</td>
      <td>3</td>
      <td>0.632456</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-modelling-5.0.1</td>
      <td>7</td>
      <td>1</td>
      <td>3</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>3</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>7</td>
      <td>31</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.290323</td>
      <td>3</td>
      <td>0.528744</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-test-5.0.1</td>
      <td>5</td>
      <td>9</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.222222</td>
      <td>3</td>
      <td>0.666667</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-update-5.0.1</td>
      <td>5</td>
      <td>1</td>
      <td>3</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>3</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>5</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.200000</td>
      <td>2</td>
      <td>0.447214</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>2</td>
      <td>3</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.333333</td>
      <td>2</td>
      <td>0.577350</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>1</td>
      <td>5</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 13b - External package usage aggregated - percentage of internal packages




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>artifactPackages</th>
      <th>numberOfExternalPackages</th>
      <th>minNumberOfPackagesPercentage</th>
      <th>medNumberOfPackagesPercentage</th>
      <th>avgNumberOfPackagesPercentage</th>
      <th>maxNumberOfPackagesPercentage</th>
      <th>stdNumberOfPackagesPercentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-messaging-5.0.1</td>
      <td>57</td>
      <td>7</td>
      <td>1.754386</td>
      <td>1.754386</td>
      <td>6.516291</td>
      <td>24.561404</td>
      <td>8.396302</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-server-connector-5.0.1</td>
      <td>5</td>
      <td>20</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>38.000000</td>
      <td>100.000000</td>
      <td>26.675437</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-common-5.0.1</td>
      <td>13</td>
      <td>10</td>
      <td>7.692308</td>
      <td>7.692308</td>
      <td>10.000000</td>
      <td>30.769231</td>
      <td>7.297564</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-conversion-5.0.1</td>
      <td>4</td>
      <td>10</td>
      <td>25.000000</td>
      <td>25.000000</td>
      <td>30.000000</td>
      <td>75.000000</td>
      <td>15.811388</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-modelling-5.0.1</td>
      <td>7</td>
      <td>1</td>
      <td>42.857143</td>
      <td>42.857143</td>
      <td>42.857143</td>
      <td>42.857143</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>7</td>
      <td>31</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>18.433180</td>
      <td>42.857143</td>
      <td>7.553481</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-test-5.0.1</td>
      <td>5</td>
      <td>9</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>24.444444</td>
      <td>60.000000</td>
      <td>13.333333</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-update-5.0.1</td>
      <td>5</td>
      <td>1</td>
      <td>60.000000</td>
      <td>60.000000</td>
      <td>60.000000</td>
      <td>60.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>7</td>
      <td>5</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>17.142857</td>
      <td>28.571429</td>
      <td>6.388766</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>2</td>
      <td>3</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>66.666667</td>
      <td>100.000000</td>
      <td>28.867513</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>1</td>
      <td>5</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>0.000000</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 13c - External package usage aggregated - count of internal types




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>artifactTypes</th>
      <th>numberOfExternalPackages</th>
      <th>minNumberOfTypes</th>
      <th>medNumberOfTypes</th>
      <th>avgNumberOfTypes</th>
      <th>maxNumberOfTypes</th>
      <th>stdNumberOfTypes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-messaging-5.0.1</td>
      <td>570</td>
      <td>7</td>
      <td>2</td>
      <td>2.0</td>
      <td>7.428571</td>
      <td>30</td>
      <td>10.244627</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-server-connector-5.0.1</td>
      <td>72</td>
      <td>20</td>
      <td>1</td>
      <td>3.5</td>
      <td>5.200000</td>
      <td>18</td>
      <td>4.840618</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-common-5.0.1</td>
      <td>150</td>
      <td>10</td>
      <td>1</td>
      <td>1.0</td>
      <td>2.100000</td>
      <td>8</td>
      <td>2.183270</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-conversion-5.0.1</td>
      <td>30</td>
      <td>10</td>
      <td>1</td>
      <td>2.5</td>
      <td>3.100000</td>
      <td>6</td>
      <td>2.024846</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-modelling-5.0.1</td>
      <td>93</td>
      <td>1</td>
      <td>3</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>3</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>70</td>
      <td>31</td>
      <td>1</td>
      <td>2.0</td>
      <td>2.193548</td>
      <td>7</td>
      <td>1.536649</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-test-5.0.1</td>
      <td>73</td>
      <td>9</td>
      <td>1</td>
      <td>1.0</td>
      <td>3.333333</td>
      <td>22</td>
      <td>7.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-update-5.0.1</td>
      <td>23</td>
      <td>1</td>
      <td>7</td>
      <td>7.0</td>
      <td>7.000000</td>
      <td>7</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>100</td>
      <td>5</td>
      <td>1</td>
      <td>1.0</td>
      <td>2.600000</td>
      <td>6</td>
      <td>2.302173</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>13</td>
      <td>3</td>
      <td>1</td>
      <td>1.0</td>
      <td>4.666667</td>
      <td>12</td>
      <td>6.350853</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>5</td>
      <td>5</td>
      <td>1</td>
      <td>2.0</td>
      <td>2.200000</td>
      <td>4</td>
      <td>1.303840</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 13d - External package usage aggregated - percentage of internal types




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>artifactTypes</th>
      <th>numberOfExternalPackages</th>
      <th>minNumberOfTypesPercentage</th>
      <th>medNumberOfTypesPercentage</th>
      <th>avgNumberOfTypesPercentage</th>
      <th>maxNumberOfTypesPercentage</th>
      <th>stdNumberOfTypesPercentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-messaging-5.0.1</td>
      <td>570</td>
      <td>7</td>
      <td>0.350877</td>
      <td>0.350877</td>
      <td>1.303258</td>
      <td>5.263158</td>
      <td>1.797303</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-server-connector-5.0.1</td>
      <td>72</td>
      <td>20</td>
      <td>1.388889</td>
      <td>4.861111</td>
      <td>7.222222</td>
      <td>25.000000</td>
      <td>6.723080</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-common-5.0.1</td>
      <td>150</td>
      <td>10</td>
      <td>0.666667</td>
      <td>0.666667</td>
      <td>1.400000</td>
      <td>5.333333</td>
      <td>1.455513</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-conversion-5.0.1</td>
      <td>30</td>
      <td>10</td>
      <td>3.333333</td>
      <td>8.333333</td>
      <td>10.333333</td>
      <td>20.000000</td>
      <td>6.749486</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-modelling-5.0.1</td>
      <td>93</td>
      <td>1</td>
      <td>3.225806</td>
      <td>3.225806</td>
      <td>3.225806</td>
      <td>3.225806</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>axon-spring-boot-autoconfigure-5.0.1</td>
      <td>70</td>
      <td>31</td>
      <td>1.428571</td>
      <td>2.857143</td>
      <td>3.133641</td>
      <td>10.000000</td>
      <td>2.195213</td>
    </tr>
    <tr>
      <th>6</th>
      <td>axon-test-5.0.1</td>
      <td>73</td>
      <td>9</td>
      <td>1.369863</td>
      <td>1.369863</td>
      <td>4.566210</td>
      <td>30.136986</td>
      <td>9.589041</td>
    </tr>
    <tr>
      <th>7</th>
      <td>axon-update-5.0.1</td>
      <td>23</td>
      <td>1</td>
      <td>30.434783</td>
      <td>30.434783</td>
      <td>30.434783</td>
      <td>30.434783</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>axon-eventsourcing-5.0.1</td>
      <td>100</td>
      <td>5</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>2.600000</td>
      <td>6.000000</td>
      <td>2.302173</td>
    </tr>
    <tr>
      <th>9</th>
      <td>axon-metrics-micrometer-5.0.1</td>
      <td>13</td>
      <td>3</td>
      <td>7.692308</td>
      <td>7.692308</td>
      <td>35.897436</td>
      <td>92.307692</td>
      <td>48.852715</td>
    </tr>
    <tr>
      <th>10</th>
      <td>axon-tracing-opentelemetry-5.0.1</td>
      <td>5</td>
      <td>5</td>
      <td>20.000000</td>
      <td>40.000000</td>
      <td>44.000000</td>
      <td>80.000000</td>
      <td>26.076810</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 13 Chart 1 - External package usage - max percentage of internal types

This chart shows per artifact the maximum percentage of internal packages (compared to all packages in that artifact) that use one specific external package. 

**Example:** One artifact might use 10 external packages where 7 of them are used in one internal package, 2 of them are used in two packages and one external dependency is used in 5 packages. So for this artifact there will be a point at x = 10 (external packages used by the artifact) and 5 (max internal packages). Instead of the count the percentage of internal packages compared to all packages in that artifact is used to get a normalized plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_98_1.png)
    


#### Table 13 Chart 2 - External package usage - median percentage of internal types

This chart shows per artifact the median (0.5 percentile) of internal packages (compared to all packages in that artifact) that use one specific external package. 

**Example:** One artifact might use 9 external packages where 3 of them are used in 1 internal package, 3 of them are used in 2 package and the last 3 ones are used in 3 packages. So for this artifact there will be a point at x = 10 (external packages used by the artifact) and 2 (median internal packages). Instead of the count the percentage of internal packages compared to all packages in that artifact is used to get a normalized plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesJava_files/ExternalDependenciesJava_100_1.png)
    


## Maven POMs


### Table 14 - Maven POMs and their declared dependencies

If Maven is used as for package and dependency management and a ".pom" file is included in the artifact, the following table shows the external dependencies that are declared there.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>pom.artifactId</th>
      <th>pom.name</th>
      <th>scope</th>
      <th>dependency.optional</th>
      <th>dependentArtifact.group</th>
      <th>dependentArtifact.name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>axon-common</td>
      <td>Axon Framework - Common</td>
      <td>test</td>
      <td>False</td>
      <td>org.springframework</td>
      <td>spring-tx</td>
    </tr>
    <tr>
      <th>1</th>
      <td>axon-common</td>
      <td>Axon Framework - Common</td>
      <td>default</td>
      <td>True</td>
      <td>com.fasterxml.jackson.datatype</td>
      <td>jackson-datatype-jsr310</td>
    </tr>
    <tr>
      <th>2</th>
      <td>axon-common</td>
      <td>Axon Framework - Common</td>
      <td>default</td>
      <td>True</td>
      <td>jakarta.validation</td>
      <td>jakarta.validation-api</td>
    </tr>
    <tr>
      <th>3</th>
      <td>axon-common</td>
      <td>Axon Framework - Common</td>
      <td>default</td>
      <td>False</td>
      <td>com.fasterxml.jackson.core</td>
      <td>jackson-databind</td>
    </tr>
    <tr>
      <th>4</th>
      <td>axon-common</td>
      <td>Axon Framework - Common</td>
      <td>default</td>
      <td>False</td>
      <td>org.reactivestreams</td>
      <td>reactive-streams</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>189</th>
      <td>axon-tracing-opentelemetry</td>
      <td>Axon Extension - Tracing - OpenTelemetry</td>
      <td>default</td>
      <td>False</td>
      <td>io.opentelemetry</td>
      <td>opentelemetry-api</td>
    </tr>
    <tr>
      <th>190</th>
      <td>axon-tracing-opentelemetry</td>
      <td>Axon Extension - Tracing - OpenTelemetry</td>
      <td>provided</td>
      <td>False</td>
      <td>com.google.code.findbugs</td>
      <td>jsr305</td>
    </tr>
    <tr>
      <th>191</th>
      <td>axon-update</td>
      <td>Axon Framework - Update</td>
      <td>default</td>
      <td>False</td>
      <td>org.axonframework</td>
      <td>axon-common</td>
    </tr>
    <tr>
      <th>192</th>
      <td>axon-update</td>
      <td>Axon Framework - Update</td>
      <td>default</td>
      <td>False</td>
      <td>jakarta.annotation</td>
      <td>jakarta.annotation-api</td>
    </tr>
    <tr>
      <th>193</th>
      <td>axon-update</td>
      <td>Axon Framework - Update</td>
      <td>test</td>
      <td>False</td>
      <td>org.axonframework</td>
      <td>axon-common</td>
    </tr>
  </tbody>
</table>
<p>194 rows × 6 columns</p>
</div>


