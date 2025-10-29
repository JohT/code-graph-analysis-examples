# Object Oriented Design Quality Metrics
<br>  

### References
- [Analyze java package metrics in a graph database](https://joht.github.io/johtizen/data/2023/04/21/java-package-metrics-analysis.html)
- [Calculate metrics](https://101.jqassistant.org/calculate-metrics/index.html)
- [jqassistant](https://jqassistant.org)
- [notebook walks through examples for integrating various packages with Neo4j](https://nicolewhite.github.io/neo4j-jupyter/hello-world.html)
- [OO Design Quality Metrics](https://api.semanticscholar.org/CorpusID:18246616)
- [A Validation of Martin's Metric](https://www.researchgate.net/publication/31598248_A_Validation_of_Martin's_Metric)
- [Neo4j Python Driver](https://neo4j.com/docs/api/python-driver/current)





## Incoming Dependencies

Incoming dependencies are also denoted as "Fan-in", "Afferent Coupling" or "in-degree".
These are the ones that use the listed package. 
   
If these packages get changed, the incoming dependencies might be affected by the change. The more incoming dependencies, the harder it gets to change the code without the need to adapt the dependent code (“rigid code”). Even worse, it might affect the behavior of the dependent code in an unwanted way (“fragile code”).

Since Java Packages are organized hierarchically, incoming dependencies can be count for every package in isolation or by including all of its sub-packages. The latter one is done without top level packages like for example "org" or "org.company" by assuring that only packages are considered that have other packages or types in the same hierarchy level ("siblings").

#### Table 1a
- Show the top 20 Typescript modules with the most incoming dependencies
- Set the property "incomingDependencies" on Module nodes if not already done.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>fullQualifiedModuleName</th>
      <th>moduleName</th>
      <th>incomingDependencies</th>
      <th>incomingDependenciesWeight</th>
      <th>incomingDependentAbstractTypes</th>
      <th>incomingDependentAbstractTypeWeight</th>
      <th>incomingDependentModules</th>
      <th>incomingDependentPackages</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router-dom</td>
      <td>7</td>
      <td>280</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router-dom-v5-compat</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>server</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router-native</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>router</td>
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



## Outgoing Dependencies

Outgoing dependencies are also denoted as "Fan-out", "Efferent Coupling" or "out-degree".
These are the ones that are used by the listed package. 

Code from other packages and libraries you’re depending on (outgoing) might change over time. The more outgoing changes, the more likely and frequently code changes are needed. This involves time and effort which can be reduced by automation of tests and version updates. Automated tests are crucial to reveal updates, that change the behavior of the code unexpectedly (“fragile code”). As soon as more effort is required, keeping up becomes difficult (“rigid code”). Not being able to use a newer version might not only restrict features, it can get problematic if there are security issues. This might force you to take “fast but ugly” solutions into account which further increases technical dept.

Since Java Packages are organized hierarchically, outgoing dependencies can be count for every package in isolation or by including all of its sub-packages. The latter one is done without top level packages like for example "org" or "org.company" by assuring that only packages are considered that have other packages or types in the same hierarchy level ("siblings").

#### Table 2a

- Show the top 20 Typescript modules with the most outgoing dependencies
- Set the "outgoingDependencies" properties on Module nodes if not already done




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>fullQualifiedModuleName</th>
      <th>sourceName</th>
      <th>outgoingDependencies</th>
      <th>outgoingDependenciesWeight</th>
      <th>outgoingDependentAbstractTypes</th>
      <th>outgoingDependentAbstractTypeWeight</th>
      <th>outgoingDependentModules</th>
      <th>outgoingDependentPackages</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router-dom</td>
      <td>156</td>
      <td>10765</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>server</td>
      <td>39</td>
      <td>1650</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router-native</td>
      <td>24</td>
      <td>764</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router</td>
      <td>17</td>
      <td>261</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router-dom-v5-compat</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>router</td>
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



## Instability

$$ Instability = \frac{Outgoing\:Dependencies}{Outgoing\:Dependencies + Incoming\:Dependencies} $$

*Instability* is expressed as the ratio of the number of outgoing dependencies of a module (i.e., the number of packages that depend on it) to the total number of dependencies (i.e., the sum of incoming and outgoing dependencies).

Small values near zero indicate low *Instability*. With no outgoing but some incoming dependencies the Instability is zero which is denoted as maximally stable. Such code units are more rigid and difficult to change without impacting other parts of the system. If they are changed less because of that, they are considered stable.

Conversely, high values approaching one indicate high *Instability*. With some outgoing dependencies but no incoming ones the *Instability* is denoted as maximally unstable. Such code units are easier to change without affecting other modules, making them more flexible and less prone to cascading changes throughout the system. If they are changed more often because of that, they are considered unstable.

Since Java Packages are organized hierarchically, *Instability* can be calculated for every package in isolation or by including all of its sub-packages. 

#### Table 3a

- Show the top 20 Typescript modules with the lowest *Instability*
- Set the property "instability" on Module nodes if not already done




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>projectName</th>
      <th>fullQualifiedModuleName</th>
      <th>moduleName</th>
      <th>instability</th>
      <th>instabilityAbstractTypes</th>
      <th>instabilityModules</th>
      <th>instabilityPackages</th>
      <th>module.outgoingDependencies</th>
      <th>module.incomingDependencies</th>
      <th>module.outgoingDependentAbstractTypes</th>
      <th>module.incomingDependentAbstractTypes</th>
      <th>module.outgoingDependentModules</th>
      <th>module.incomingDependentModules</th>
      <th>module.outgoingDependentPackages</th>
      <th>module.incomingDependentPackages</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>react-router-dom-v5-compat</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router-dom-v5-compat</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
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
      <th>1</th>
      <td>router</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>router</td>
      <td>0.000000</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
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
      <th>2</th>
      <td>react-router-dom</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router-dom</td>
      <td>0.957055</td>
      <td>0.0</td>
      <td>0.8</td>
      <td>0.0</td>
      <td>156</td>
      <td>7</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>react-router-dom</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>server</td>
      <td>1.000000</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>39</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>react-router-native</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router-native</td>
      <td>1.000000</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>24</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>react-router</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router</td>
      <td>1.000000</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>17</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>



## Abstractness

$$ Abstractness = \frac{abstract\:classes\:in\:category}{total\:number\:of\:classes\:in\:category} $$

Package *Abstractness* is expressed as the ratio of the number of abstract classes and interfaces to the total number of classes of a package.

Zero *Abstractness* means that there are no abstract types or interfaces in the package. On the other hand, a value of one means that there are only abstract types.

Since Java Packages are organized hierarchically, *Abstractness* can be calculated for every package in isolation or by including all of its sub-packages. 

#### Table 4a

- Show the top 30 Typescript modules with the lowest *Abstractness*
- Set the property "abstractness" on Module nodes if not already done.

    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownPropertyKeyWarning} {category: UNRECOGNIZED} {title: The provided property key is not in the database} {description: One of the property names in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing property name is: numberAbstractTypes)} {position: line: 10, column: 16, offset: 500} for query: "// Get Typscript Modules with the lowest abstractness first (if set before)\n \n MATCH (module:TS:Module)\n WHERE module.abstractness IS NOT NULL \n OPTIONAL MATCH (projectdir:Directory)<-[:HAS_ROOT]-(project:TS:Project)-[:CONTAINS]->(module)\n RETURN reverse(split(reverse(projectdir.absoluteFileName), '/')[0]) AS projectName\n       ,module.globalFqn           AS fullQualifiedModuleName\n       ,module.name                AS moduleName\n       ,module.abstractness        AS abstractness\n       ,module.numberAbstractTypes AS numberAbstractTypes\n       ,module.numberTypes         AS numberTypes\n ORDER BY abstractness ASC, numberTypes DESC\nLIMIT 20"


    Received notification from DBMS server: {severity: WARNING} {code: Neo.ClientNotification.Statement.UnknownPropertyKeyWarning} {category: UNRECOGNIZED} {title: The provided property key is not in the database} {description: One of the property names in your query is not available in the database, make sure you didn't misspell it or that the label is available when you run this statement in your application (the missing property name is: numberTypes)} {position: line: 11, column: 16, offset: 558} for query: "// Get Typscript Modules with the lowest abstractness first (if set before)\n \n MATCH (module:TS:Module)\n WHERE module.abstractness IS NOT NULL \n OPTIONAL MATCH (projectdir:Directory)<-[:HAS_ROOT]-(project:TS:Project)-[:CONTAINS]->(module)\n RETURN reverse(split(reverse(projectdir.absoluteFileName), '/')[0]) AS projectName\n       ,module.globalFqn           AS fullQualifiedModuleName\n       ,module.name                AS moduleName\n       ,module.abstractness        AS abstractness\n       ,module.numberAbstractTypes AS numberAbstractTypes\n       ,module.numberTypes         AS numberTypes\n ORDER BY abstractness ASC, numberTypes DESC\nLIMIT 20"





<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>projectName</th>
      <th>fullQualifiedModuleName</th>
      <th>moduleName</th>
      <th>abstractness</th>
      <th>numberAbstractTypes</th>
      <th>numberTypes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>router</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>router</td>
      <td>0.000000</td>
      <td>None</td>
      <td>None</td>
    </tr>
    <tr>
      <th>1</th>
      <td>react-router-dom-v5-compat</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router-dom-v5-compat</td>
      <td>0.000000</td>
      <td>None</td>
      <td>None</td>
    </tr>
    <tr>
      <th>2</th>
      <td>react-router-dom</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router-dom</td>
      <td>0.206349</td>
      <td>None</td>
      <td>None</td>
    </tr>
    <tr>
      <th>3</th>
      <td>react-router-native</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router-native</td>
      <td>0.277778</td>
      <td>None</td>
      <td>None</td>
    </tr>
    <tr>
      <th>4</th>
      <td>react-router-dom</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>server</td>
      <td>0.333333</td>
      <td>None</td>
      <td>None</td>
    </tr>
    <tr>
      <th>5</th>
      <td>react-router</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>react-router</td>
      <td>0.714286</td>
      <td>None</td>
      <td>None</td>
    </tr>
  </tbody>
</table>
</div>



## Distance from the main sequence

The *main sequence* is a imaginary line that represents a good compromise between *Abstractness* and *Instability*. A high distance to this line may indicate problems. For example is very *stable* (rigid) code with low abstractness hard to change.

Read more details on that in [OO Design Quality Metrics](https://api.semanticscholar.org/CorpusID:18246616) and [Calculate metrics](https://101.jqassistant.org/calculate-metrics/index.html).

#### Table 5a

- Show the top 30 Typescript modules with the highest distance from the "main sequence"




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>artifactName</th>
      <th>fullQualifiedName</th>
      <th>name</th>
      <th>distance</th>
      <th>abstractness</th>
      <th>instability</th>
      <th>elementsCount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>router</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>./index.ts</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>react-router-dom-v5-compat</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>./index.ts</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>react-router</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>./index.ts</td>
      <td>0.714286</td>
      <td>0.714286</td>
      <td>1.000000</td>
      <td>7</td>
    </tr>
    <tr>
      <th>3</th>
      <td>react-router-dom</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>./server.tsx</td>
      <td>0.333333</td>
      <td>0.333333</td>
      <td>1.000000</td>
      <td>6</td>
    </tr>
    <tr>
      <th>4</th>
      <td>react-router-native</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>./index.tsx</td>
      <td>0.277778</td>
      <td>0.277778</td>
      <td>1.000000</td>
      <td>18</td>
    </tr>
    <tr>
      <th>5</th>
      <td>react-router-dom</td>
      <td>/home/runner/work/code-graph-analysis-examples...</td>
      <td>./index.tsx</td>
      <td>0.163404</td>
      <td>0.206349</td>
      <td>0.957055</td>
      <td>63</td>
    </tr>
  </tbody>
</table>
</div>



### *Abstractness* vs. *Instability* Plot with "Main Sequence" line as reference

- Plot *Abstractness* vs. *Instability* of all packages
- Draw the "main sequence" as dashed green diagonal line 
- Scale the packages by the number of types they contain
- Color the packages by their distance to the "main sequence" (blue=near, red=far)

#### Figure 5a - Typescript Modules


    
![png](ObjectOrientedDesignMetricsTypescript_files/ObjectOrientedDesignMetricsTypescript_26_0.png)
    

