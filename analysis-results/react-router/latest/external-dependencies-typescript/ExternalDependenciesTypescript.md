# External Dependencies for Typescript
<br>  

### References
- [jqassistant](https://jqassistant.org)
- [Neo4j Python Driver](https://neo4j.com/docs/api/python-driver/current)

    Unable to revert mtime: /usr/share/fonts
    Unable to revert mtime: /usr/share/fonts/truetype
    Unable to revert mtime: /usr/share/fonts/truetype/dejavu


    Unable to revert mtime: /usr/share/fonts/truetype/lato


    Unable to revert mtime: /usr/share/fonts/truetype/liberation
    Unable to revert mtime: /usr/share/fonts/truetype/noto






## External Typescript Module Usage

### External Module

An external Typescript module is marked with the label `ExternalModule` and the declarations it provides with  `ExternalDeclaration`. In practice, the distinction between internal and external isn't always that clear. When there is a problem following the project configuration like discussed in [Missing Interfaces and other elements in the Graph](https://github.com/jqassistant-plugin/jqassistant-typescript-plugin/issues/35), some internal dependencies might be imported as external ones. 

To have a second indicator, the property `isNodeModule` is written with [Add_module_properties.cypher](./../cypher/Typescript_Enrichment/Add_module_properties.cypher) in [prepareAnalysis.sh](./../scripts/prepareAnalysis.sh). For most package managers this should then be sufficient. As of now (June 2024), it might not work with [Yarn Plug'n'Play](https://yarnpkg.com/features/pnp).

### Table 1 - Top 20 most used external packages overall

This table shows the external packages that are used by the most different internal types overall.
Additionally, it shows which types of the external modules are actually used. External annotations are also listed.

Only the top 20 entries are shown. The whole table can be found in the following CSV report:
`External_module_usage_overall_for_Typescript`

**Columns:**
- *externalModuleName* is the name of the external module prepended by its namespace if given. Example: "@types/react"
- *numberOfExternalCallerModules* is the number of modules that use that external module
- *numberOfExternalCallerElements* is the number of elements (functions, classes,...) that use that external module
- *numberOfExternalDeclarationCalls* is how often the external declarations of that external module are imported
- *numberOfExternalDeclarationCallsWeighted* is how often the external declarations of that external module are actually used
- *allModules* contains the total count of all analyzed internal modules
- *allInternalElements* contains the total count of all analyzed exported internal elements (function, classes,...)
- *exampleStories* contains a list of sentences that contain concrete examples (for explanation and debugging)




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalModuleName</th>
      <th>numberOfExternalCallerModules</th>
      <th>numberOfExternalCallerElements</th>
      <th>numberOfExternalDeclarationCalls</th>
      <th>numberOfExternalDeclarationCallsWeighted</th>
      <th>allModules</th>
      <th>allInternalElements</th>
      <th>exampleStories</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>node</td>
      <td>23</td>
      <td>29</td>
      <td>280</td>
      <td>436</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;reactRouterVitePlugin&gt; of module &lt;vite&gt; impo...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>@types/process</td>
      <td>17</td>
      <td>20</td>
      <td>42</td>
      <td>126</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;Context&gt; of module &lt;create-react-router&gt; imp...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>dist</td>
      <td>17</td>
      <td>27</td>
      <td>99</td>
      <td>234</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;relative&gt; of module &lt;routes&gt; imports &lt;resolv...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>@types/path</td>
      <td>14</td>
      <td>20</td>
      <td>55</td>
      <td>117</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;getDirectoryFilesRecursive&gt; of module &lt;utils...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>picocolors</td>
      <td>10</td>
      <td>11</td>
      <td>14</td>
      <td>83</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;color&gt; of module &lt;utils&gt; imports &lt;picocolors...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>node:fs</td>
      <td>9</td>
      <td>11</td>
      <td>25</td>
      <td>48</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;ensureDirectory&gt; of module &lt;utils&gt; imports &lt;...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>promises</td>
      <td>9</td>
      <td>13</td>
      <td>36</td>
      <td>60</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;getDirectoryFilesRecursive&gt; of module &lt;utils...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>@types/globals</td>
      <td>8</td>
      <td>9</td>
      <td>11</td>
      <td>15</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;reactRouterVitePlugin&gt; of module &lt;vite&gt; impo...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>@types/react</td>
      <td>8</td>
      <td>24</td>
      <td>91</td>
      <td>250</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;AwaitContextProvider&gt; of module &lt;react-route...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>node:path</td>
      <td>7</td>
      <td>11</td>
      <td>11</td>
      <td>28</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;getDirectoryFilesRecursive&gt; of module &lt;utils...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>@types/babel__generator</td>
      <td>6</td>
      <td>7</td>
      <td>12</td>
      <td>14</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;reactRouterVitePlugin&gt; of module &lt;vite&gt; impo...</td>
    </tr>
    <tr>
      <th>11</th>
      <td>@types/buffer</td>
      <td>6</td>
      <td>4</td>
      <td>12</td>
      <td>13</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;createReactRouterRequest&gt; of module &lt;server&gt;...</td>
    </tr>
    <tr>
      <th>12</th>
      <td>http</td>
      <td>6</td>
      <td>5</td>
      <td>10</td>
      <td>10</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;reactRouterVitePlugin&gt; of module &lt;vite&gt; impo...</td>
    </tr>
    <tr>
      <th>13</th>
      <td>readline</td>
      <td>6</td>
      <td>6</td>
      <td>10</td>
      <td>104</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;ConfirmPrompt&gt; of module &lt;prompts-confirm&gt; i...</td>
    </tr>
    <tr>
      <th>14</th>
      <td>sisteransi</td>
      <td>6</td>
      <td>6</td>
      <td>27</td>
      <td>292</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;ConfirmPrompt&gt; of module &lt;prompts-confirm&gt; i...</td>
    </tr>
    <tr>
      <th>15</th>
      <td>@babel/lib</td>
      <td>5</td>
      <td>6</td>
      <td>64</td>
      <td>142</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;transpile&gt; of module &lt;useJavascript&gt; imports...</td>
    </tr>
    <tr>
      <th>16</th>
      <td>@types/pick</td>
      <td>5</td>
      <td>5</td>
      <td>9</td>
      <td>9</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;layout&gt; of module &lt;routes&gt; imports &lt;pick&gt; fr...</td>
    </tr>
    <tr>
      <th>17</th>
      <td>fs</td>
      <td>5</td>
      <td>5</td>
      <td>13</td>
      <td>19</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;directoryExists&gt; of module &lt;utils&gt; imports &lt;...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>@types/babel__core</td>
      <td>4</td>
      <td>3</td>
      <td>14</td>
      <td>15</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;reactRouterVitePlugin&gt; of module &lt;vite&gt; impo...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>lexer</td>
      <td>4</td>
      <td>3</td>
      <td>5</td>
      <td>5</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;reactRouterVitePlugin&gt; of module &lt;vite&gt; impo...</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 1 Chart 1a - Most called external modules in % by internal elements (more than 0.7% overall)

External modules that are used less than 0.7% are grouped into "others" to get a cleaner chart
containing the most significant external modules and how ofter they are called by internal elements in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_15_1.png)
    


#### Table 1 Chart 1b - Most called external modules in % by internal elements (less than 0.7% overall "others" drill-down)

Shows the lowest (less than 0.7% overall) most called external modules. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_17_1.png)
    


#### Table 1 Chart 2a - Most called external modules in % by internal modules (more than 0.7% overall)

External modules that are used less than 0.7% are grouped into "others" to get a cleaner chart
containing the most significant external modules and how ofter they are called by internal modules in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_19_1.png)
    


#### Table 1 Chart 2b - Most called external modules in % by internal modules (less than 0.7% overall "others" drill-down)

Shows the lowest (less than 0.7% overall) most called external modules. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_21_1.png)
    


### Table 2 - Top 20 most used external namespaces

This table shows external namespaces that are used by the most different internal elements (functions, classes,...) overall. 

Additionally, it shows how many of the declarations of the external namespace are actually used.

Only the top 20 entries are shown. The whole table can be found in the following CSV report:
`External_namespace_usage_overall_for_Typescript`

**Columns:**
- *externalNamespaceName* is the name of the external namespace (empty if none). Example: "@types". All other columns are aggregated/grouped by it.
- *numberOfExternalCallerModules* is the number of modules that use that external module
- *numberOfExternalCallerElements* is the number of elements (functions, classes,...) that use that external module
- *numberOfExternalDeclarationCalls* is how often the external declarations of that external module are imported
- *numberOfExternalDeclarationCallsWeighted* is how often the external declarations of that external module are actually used
- *allModules* contains the total count of all analyzed internal modules
- *allInternalElements* contains the total count of all analyzed exported internal elements (function, classes,...)
- *exampleStories* contains a list of sentences that contain concrete examples (for explanation and debugging)




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalNamespaceName</th>
      <th>numberOfExternalCallerModules</th>
      <th>numberOfExternalCallerElements</th>
      <th>numberOfExternalDeclarationCalls</th>
      <th>numberOfExternalDeclarationCallsWeighted</th>
      <th>allModules</th>
      <th>allInternalElements</th>
      <th>exampleStories</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>no namespace</td>
      <td>53</td>
      <td>96</td>
      <td>606</td>
      <td>1596</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;copyTemplate&gt; of module &lt;copy-template&gt; impo...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>@types</td>
      <td>51</td>
      <td>93</td>
      <td>353</td>
      <td>726</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;Context&gt; of module &lt;create-react-router&gt; imp...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>@babel</td>
      <td>5</td>
      <td>6</td>
      <td>67</td>
      <td>147</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;transpile&gt; of module &lt;useJavascript&gt; imports...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>@cloudflare</td>
      <td>3</td>
      <td>5</td>
      <td>52</td>
      <td>68</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;RequestHandler&gt; of module &lt;react-router-clou...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>@architect</td>
      <td>2</td>
      <td>1</td>
      <td>10</td>
      <td>14</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;createArcTableSessionStorage&gt; of module &lt;rea...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>@mjackson</td>
      <td>2</td>
      <td>2</td>
      <td>4</td>
      <td>10</td>
      <td>139</td>
      <td>631</td>
      <td>[&lt;createRequestListener&gt; of module &lt;react-rout...</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 2 Chart 1a - Most called external namespaces in % by internal element (more than 0.7% overall)

External namespaces that are used less than 0.7% are grouped into "others" to get a cleaner chart
containing the most significant external namespaces and how ofter they are called by internal elements in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_25_1.png)
    


#### Table 2 Chart 1a - Most called external namespaces in % by internal element (less than 0.7% overall "others" drill-down)

Shows the lowest (less than 0.7% overall) most called external namespaces. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_27_1.png)
    


#### Table 2 Chart 2a - Most called external namespaces in % by internal modules (more than 0.7% overall)

External namespaces that are used less than 0.7% are grouped into "others" to get a cleaner chart
containing the most significant external namespaces and how ofter they are called by internal modules in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_29_1.png)
    


#### Table 2 Chart 2b - Most called external namespaces in % by internal modules (less than 0.7% overall "others" drill-down)

Shows the lowest (less than 0.7% overall) most called external namespaces. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.

    No data to plot for title 'Top external namespace usage [%] by internal modules (less than 0.7% overall "others" drill-down)'.


### Table 3 - Top 20 most widely spread external modules

The following tables shows external modules that are used by many different internal modules with the highest number of artifacts first.

Statistics like minimum, maximum, average, median and standard deviation are provided for the number of internally exported elements (function, class, ...) and the external declarations they use for every external module. 

The intuition behind that is to find external modules and the external declarations they provide that are used in a widely spread manner. This can help to distinguish widely used libraries and frameworks from external modules that are used for specific tasks. It can also be used to find external modules that are used sparsely regarding internal modules but where many different external declarations are used. 

Refactoring with [Hexagonal architecture](https://alistair.cockburn.us/hexagonal-architecture) in mind can be considered for non-framework external modules that are used for very specific tasks and that are used in many different internal locations. This makes the internal code more robust against changes of these external modules or it is easier to update and migrate to newer versions of them. 

External modules that are only used in very few internal locations overall might be considered for removal if they are easy to replace with a similar library that is already used more often. Or they might also simply be replaced by very few lines of code. Replacing libraries with own code isn't recommended when you need to write a lot of code or for external modules that provide security relevant implementations (encryption, sanitizers, ...), because they will be tracked and maintained globally and security updates need to be adopted fast.

Only the top 20 entries are shown. The whole table can be found in the following CSV report:
`External_module_usage_spread_for_Typescript`

**Columns:**
- *externalModuleName* is the name of the external package prepended by its namespace if given. Example: "@types/react"
external package.
- *numberOfInternalModules* is the number of internal modules that are using that external module
- *\[min,max,med,avg,std\]NumberOfUsedExternalDeclarations* provide statistics for all internal modules and how their usage of the declarations provided by the external module are distributed. This provides an indicator on how strong the coupling to the external module is. For example, if many (high sum) elements provided by that external module are used constantly (low std), a higher coupling can be presumed. If there is only one (sum) element in use, this could be an indicator for an external module that could get replaced or that there is just one central entry point for it.
- *\[min/max/med/avg/std\]NumberOfInternalElements* provide statistics for all internal modules and how their usage of the external module is distributed across their internal elements. This provides an indicator on how widely an external module is spread across internal elements and if there are great differences between internal modules (high standard deviation) or not.
- *\[min/max/med/avg/std\]NumberOfInternalElementsPercentage* is similar to [min/max/med/avg/std]NumberOfUsedExternalDeclarations but provides the value in percent in relation to the total number of internal elements per internal module.
- *internalModuleExamples* some examples of included internal modules for debugging




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalModuleName</th>
      <th>numberOfInternalModules</th>
      <th>sumNumberOfUsedExternalDeclarations</th>
      <th>minNumberOfUsedExternalDeclarations</th>
      <th>maxNumberOfUsedExternalDeclarations</th>
      <th>medNumberOfUsedExternalDeclarations</th>
      <th>avgNumberOfUsedExternalDeclarations</th>
      <th>stdNumberOfUsedExternalDeclarations</th>
      <th>sumNumberOfInternalElements</th>
      <th>minNumberOfInternalElements</th>
      <th>maxNumberOfInternalElements</th>
      <th>medNumberOfInternalElements</th>
      <th>avgNumberOfInternalElements</th>
      <th>stdNumberOfInternalElements</th>
      <th>minNumberOfInternalElementsPercentage</th>
      <th>maxNumberOfInternalElementsPercentage</th>
      <th>medNumberOfInternalElementsPercentage</th>
      <th>avgNumberOfInternalElementsPercentage</th>
      <th>stdNumberOfInternalElementsPercentage</th>
      <th>internalModuleExamples</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>node</td>
      <td>21</td>
      <td>241</td>
      <td>1</td>
      <td>81</td>
      <td>3.0</td>
      <td>11.476190</td>
      <td>22.653077</td>
      <td>32</td>
      <td>1</td>
      <td>8</td>
      <td>1.0</td>
      <td>1.523810</td>
      <td>1.569046</td>
      <td>0.719424</td>
      <td>5.755396</td>
      <td>0.719424</td>
      <td>1.096266</td>
      <td>1.128810</td>
      <td>[@react-router/vite, @react-router/plugin, @re...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>@types/process</td>
      <td>17</td>
      <td>39</td>
      <td>1</td>
      <td>5</td>
      <td>2.0</td>
      <td>2.294118</td>
      <td>1.531531</td>
      <td>22</td>
      <td>1</td>
      <td>4</td>
      <td>1.0</td>
      <td>1.294118</td>
      <td>0.771744</td>
      <td>0.719424</td>
      <td>2.877698</td>
      <td>0.719424</td>
      <td>0.931020</td>
      <td>0.555211</td>
      <td>[create-react-router, loading-indicator, promp...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>dist</td>
      <td>15</td>
      <td>73</td>
      <td>1</td>
      <td>26</td>
      <td>4.0</td>
      <td>4.866667</td>
      <td>6.289068</td>
      <td>31</td>
      <td>1</td>
      <td>5</td>
      <td>1.0</td>
      <td>2.066667</td>
      <td>1.437591</td>
      <td>0.719424</td>
      <td>3.597122</td>
      <td>0.719424</td>
      <td>1.486811</td>
      <td>1.034238</td>
      <td>[@react-router/routes, @react-router/plugin, @...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>@types/path</td>
      <td>13</td>
      <td>41</td>
      <td>1</td>
      <td>7</td>
      <td>2.0</td>
      <td>3.153846</td>
      <td>2.192645</td>
      <td>22</td>
      <td>1</td>
      <td>5</td>
      <td>1.0</td>
      <td>1.692308</td>
      <td>1.182132</td>
      <td>0.719424</td>
      <td>3.597122</td>
      <td>0.719424</td>
      <td>1.217488</td>
      <td>0.850455</td>
      <td>[utils, @react-router/vite, @react-router/plug...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>node:fs</td>
      <td>9</td>
      <td>20</td>
      <td>1</td>
      <td>4</td>
      <td>2.0</td>
      <td>2.222222</td>
      <td>0.971825</td>
      <td>13</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.444444</td>
      <td>0.881917</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>1.039169</td>
      <td>0.634473</td>
      <td>[utils, @react-router/vite, @react-router/plug...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>picocolors</td>
      <td>9</td>
      <td>10</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.111111</td>
      <td>0.333333</td>
      <td>13</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.444444</td>
      <td>0.726483</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>1.039169</td>
      <td>0.522650</td>
      <td>[utils, @react-router/vite, @react-router/plug...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>promises</td>
      <td>8</td>
      <td>30</td>
      <td>1</td>
      <td>7</td>
      <td>3.5</td>
      <td>3.750000</td>
      <td>2.251983</td>
      <td>16</td>
      <td>1</td>
      <td>4</td>
      <td>1.5</td>
      <td>2.000000</td>
      <td>1.309307</td>
      <td>0.719424</td>
      <td>2.877698</td>
      <td>1.079137</td>
      <td>1.438849</td>
      <td>0.941948</td>
      <td>[utils, @react-router/vite, @react-router/plug...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>@types/globals</td>
      <td>7</td>
      <td>7</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>11</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.571429</td>
      <td>0.786796</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>1.130524</td>
      <td>0.566040</td>
      <td>[@react-router/vite, @react-router/plugin, @re...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>@types/babel__generator</td>
      <td>6</td>
      <td>9</td>
      <td>1</td>
      <td>2</td>
      <td>1.5</td>
      <td>1.500000</td>
      <td>0.547723</td>
      <td>8</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.333333</td>
      <td>0.816497</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>0.959233</td>
      <td>0.587408</td>
      <td>[@react-router/vite, @react-router/plugin, @re...</td>
    </tr>
    <tr>
      <th>9</th>
      <td>@types/buffer</td>
      <td>6</td>
      <td>11</td>
      <td>1</td>
      <td>3</td>
      <td>2.0</td>
      <td>1.833333</td>
      <td>0.752773</td>
      <td>7</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.166667</td>
      <td>0.408248</td>
      <td>0.719424</td>
      <td>1.438849</td>
      <td>0.719424</td>
      <td>0.839329</td>
      <td>0.293704</td>
      <td>[@react-router/server, @react-router/vite, @re...</td>
    </tr>
  </tbody>
</table>
</div>



### Table 3a - Top 20 most widely spread external packages - number of internal modules

This table shows the top 20 most widely spread external packages focussing on the spread across the number of internal modules.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalModuleName</th>
      <th>numberOfInternalModules</th>
      <th>minNumberOfInternalElements</th>
      <th>maxNumberOfInternalElements</th>
      <th>medNumberOfInternalElements</th>
      <th>avgNumberOfInternalElements</th>
      <th>stdNumberOfInternalElements</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>node</td>
      <td>21</td>
      <td>1</td>
      <td>8</td>
      <td>1.0</td>
      <td>1.523810</td>
      <td>1.569046</td>
    </tr>
    <tr>
      <th>1</th>
      <td>@types/process</td>
      <td>17</td>
      <td>1</td>
      <td>4</td>
      <td>1.0</td>
      <td>1.294118</td>
      <td>0.771744</td>
    </tr>
    <tr>
      <th>2</th>
      <td>dist</td>
      <td>15</td>
      <td>1</td>
      <td>5</td>
      <td>1.0</td>
      <td>2.066667</td>
      <td>1.437591</td>
    </tr>
    <tr>
      <th>3</th>
      <td>@types/path</td>
      <td>13</td>
      <td>1</td>
      <td>5</td>
      <td>1.0</td>
      <td>1.692308</td>
      <td>1.182132</td>
    </tr>
    <tr>
      <th>4</th>
      <td>node:fs</td>
      <td>9</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.444444</td>
      <td>0.881917</td>
    </tr>
    <tr>
      <th>5</th>
      <td>picocolors</td>
      <td>9</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.444444</td>
      <td>0.726483</td>
    </tr>
    <tr>
      <th>6</th>
      <td>promises</td>
      <td>8</td>
      <td>1</td>
      <td>4</td>
      <td>1.5</td>
      <td>2.000000</td>
      <td>1.309307</td>
    </tr>
    <tr>
      <th>7</th>
      <td>@types/globals</td>
      <td>7</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.571429</td>
      <td>0.786796</td>
    </tr>
    <tr>
      <th>8</th>
      <td>@types/babel__generator</td>
      <td>6</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.333333</td>
      <td>0.816497</td>
    </tr>
    <tr>
      <th>9</th>
      <td>@types/buffer</td>
      <td>6</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.166667</td>
      <td>0.408248</td>
    </tr>
    <tr>
      <th>10</th>
      <td>@types/react</td>
      <td>6</td>
      <td>1</td>
      <td>14</td>
      <td>4.0</td>
      <td>6.333333</td>
      <td>5.715476</td>
    </tr>
    <tr>
      <th>11</th>
      <td>node:path</td>
      <td>6</td>
      <td>1</td>
      <td>3</td>
      <td>1.5</td>
      <td>1.833333</td>
      <td>0.983192</td>
    </tr>
    <tr>
      <th>12</th>
      <td>readline</td>
      <td>6</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>sisteransi</td>
      <td>6</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>@babel/lib</td>
      <td>5</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.200000</td>
      <td>0.447214</td>
    </tr>
    <tr>
      <th>15</th>
      <td>fs</td>
      <td>5</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.200000</td>
      <td>0.447214</td>
    </tr>
    <tr>
      <th>16</th>
      <td>http</td>
      <td>5</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.400000</td>
      <td>0.547723</td>
    </tr>
    <tr>
      <th>17</th>
      <td>@types/pick</td>
      <td>4</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.500000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>@cloudflare/workers-types</td>
      <td>3</td>
      <td>1</td>
      <td>5</td>
      <td>4.0</td>
      <td>3.333333</td>
      <td>2.081666</td>
    </tr>
    <tr>
      <th>19</th>
      <td>@types/babel__core</td>
      <td>3</td>
      <td>1</td>
      <td>2</td>
      <td>2.0</td>
      <td>1.666667</td>
      <td>0.577350</td>
    </tr>
  </tbody>
</table>
</div>



### Table 3b - Top 20 most widely spread external packages - percentage of internal modules

This table shows the top 20 most widely spread external packages focussing on the spread across the percentage of internal modules.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalModuleName</th>
      <th>numberOfInternalModules</th>
      <th>minNumberOfInternalElementsPercentage</th>
      <th>maxNumberOfInternalElementsPercentage</th>
      <th>medNumberOfInternalElementsPercentage</th>
      <th>avgNumberOfInternalElementsPercentage</th>
      <th>stdNumberOfInternalElementsPercentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>node</td>
      <td>21</td>
      <td>0.719424</td>
      <td>5.755396</td>
      <td>0.719424</td>
      <td>1.096266</td>
      <td>1.128810</td>
    </tr>
    <tr>
      <th>1</th>
      <td>@types/process</td>
      <td>17</td>
      <td>0.719424</td>
      <td>2.877698</td>
      <td>0.719424</td>
      <td>0.931020</td>
      <td>0.555211</td>
    </tr>
    <tr>
      <th>2</th>
      <td>dist</td>
      <td>15</td>
      <td>0.719424</td>
      <td>3.597122</td>
      <td>0.719424</td>
      <td>1.486811</td>
      <td>1.034238</td>
    </tr>
    <tr>
      <th>3</th>
      <td>@types/path</td>
      <td>13</td>
      <td>0.719424</td>
      <td>3.597122</td>
      <td>0.719424</td>
      <td>1.217488</td>
      <td>0.850455</td>
    </tr>
    <tr>
      <th>4</th>
      <td>node:fs</td>
      <td>9</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>1.039169</td>
      <td>0.634473</td>
    </tr>
    <tr>
      <th>5</th>
      <td>picocolors</td>
      <td>9</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>1.039169</td>
      <td>0.522650</td>
    </tr>
    <tr>
      <th>6</th>
      <td>promises</td>
      <td>8</td>
      <td>0.719424</td>
      <td>2.877698</td>
      <td>1.079137</td>
      <td>1.438849</td>
      <td>0.941948</td>
    </tr>
    <tr>
      <th>7</th>
      <td>@types/globals</td>
      <td>7</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>1.130524</td>
      <td>0.566040</td>
    </tr>
    <tr>
      <th>8</th>
      <td>@types/babel__generator</td>
      <td>6</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>0.959233</td>
      <td>0.587408</td>
    </tr>
    <tr>
      <th>9</th>
      <td>@types/buffer</td>
      <td>6</td>
      <td>0.719424</td>
      <td>1.438849</td>
      <td>0.719424</td>
      <td>0.839329</td>
      <td>0.293704</td>
    </tr>
    <tr>
      <th>10</th>
      <td>@types/react</td>
      <td>6</td>
      <td>0.719424</td>
      <td>10.071942</td>
      <td>2.877698</td>
      <td>4.556355</td>
      <td>4.111853</td>
    </tr>
    <tr>
      <th>11</th>
      <td>node:path</td>
      <td>6</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>1.079137</td>
      <td>1.318945</td>
      <td>0.707332</td>
    </tr>
    <tr>
      <th>12</th>
      <td>readline</td>
      <td>6</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>sisteransi</td>
      <td>6</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>@babel/lib</td>
      <td>5</td>
      <td>0.719424</td>
      <td>1.438849</td>
      <td>0.719424</td>
      <td>0.863309</td>
      <td>0.321736</td>
    </tr>
    <tr>
      <th>15</th>
      <td>fs</td>
      <td>5</td>
      <td>0.719424</td>
      <td>1.438849</td>
      <td>0.719424</td>
      <td>0.863309</td>
      <td>0.321736</td>
    </tr>
    <tr>
      <th>16</th>
      <td>http</td>
      <td>5</td>
      <td>0.719424</td>
      <td>1.438849</td>
      <td>0.719424</td>
      <td>1.007194</td>
      <td>0.394045</td>
    </tr>
    <tr>
      <th>17</th>
      <td>@types/pick</td>
      <td>4</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>1.079137</td>
      <td>0.719424</td>
    </tr>
    <tr>
      <th>18</th>
      <td>@cloudflare/workers-types</td>
      <td>3</td>
      <td>0.719424</td>
      <td>3.597122</td>
      <td>2.877698</td>
      <td>2.398082</td>
      <td>1.497601</td>
    </tr>
    <tr>
      <th>19</th>
      <td>@types/babel__core</td>
      <td>3</td>
      <td>0.719424</td>
      <td>1.438849</td>
      <td>1.438849</td>
      <td>1.199041</td>
      <td>0.415360</td>
    </tr>
  </tbody>
</table>
</div>



### Table 3c - Top 20 most widely spread external packages - number of internal elements

This table shows the top 20 most widely spread external packages focussing on the spread across the number of internal elements.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalModuleName</th>
      <th>numberOfInternalModules</th>
      <th>minNumberOfInternalElements</th>
      <th>maxNumberOfInternalElements</th>
      <th>medNumberOfInternalElements</th>
      <th>avgNumberOfInternalElements</th>
      <th>stdNumberOfInternalElements</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>node</td>
      <td>21</td>
      <td>1</td>
      <td>8</td>
      <td>1.0</td>
      <td>1.523810</td>
      <td>1.569046</td>
    </tr>
    <tr>
      <th>1</th>
      <td>@types/process</td>
      <td>17</td>
      <td>1</td>
      <td>4</td>
      <td>1.0</td>
      <td>1.294118</td>
      <td>0.771744</td>
    </tr>
    <tr>
      <th>2</th>
      <td>dist</td>
      <td>15</td>
      <td>1</td>
      <td>5</td>
      <td>1.0</td>
      <td>2.066667</td>
      <td>1.437591</td>
    </tr>
    <tr>
      <th>3</th>
      <td>@types/path</td>
      <td>13</td>
      <td>1</td>
      <td>5</td>
      <td>1.0</td>
      <td>1.692308</td>
      <td>1.182132</td>
    </tr>
    <tr>
      <th>4</th>
      <td>node:fs</td>
      <td>9</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.444444</td>
      <td>0.881917</td>
    </tr>
    <tr>
      <th>5</th>
      <td>picocolors</td>
      <td>9</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.444444</td>
      <td>0.726483</td>
    </tr>
    <tr>
      <th>6</th>
      <td>promises</td>
      <td>8</td>
      <td>1</td>
      <td>4</td>
      <td>1.5</td>
      <td>2.000000</td>
      <td>1.309307</td>
    </tr>
    <tr>
      <th>7</th>
      <td>@types/globals</td>
      <td>7</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.571429</td>
      <td>0.786796</td>
    </tr>
    <tr>
      <th>8</th>
      <td>@types/babel__generator</td>
      <td>6</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.333333</td>
      <td>0.816497</td>
    </tr>
    <tr>
      <th>9</th>
      <td>@types/buffer</td>
      <td>6</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.166667</td>
      <td>0.408248</td>
    </tr>
    <tr>
      <th>10</th>
      <td>@types/react</td>
      <td>6</td>
      <td>1</td>
      <td>14</td>
      <td>4.0</td>
      <td>6.333333</td>
      <td>5.715476</td>
    </tr>
    <tr>
      <th>11</th>
      <td>node:path</td>
      <td>6</td>
      <td>1</td>
      <td>3</td>
      <td>1.5</td>
      <td>1.833333</td>
      <td>0.983192</td>
    </tr>
    <tr>
      <th>12</th>
      <td>readline</td>
      <td>6</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>sisteransi</td>
      <td>6</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>@babel/lib</td>
      <td>5</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.200000</td>
      <td>0.447214</td>
    </tr>
    <tr>
      <th>15</th>
      <td>fs</td>
      <td>5</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.200000</td>
      <td>0.447214</td>
    </tr>
    <tr>
      <th>16</th>
      <td>http</td>
      <td>5</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.400000</td>
      <td>0.547723</td>
    </tr>
    <tr>
      <th>17</th>
      <td>@types/pick</td>
      <td>4</td>
      <td>1</td>
      <td>3</td>
      <td>1.0</td>
      <td>1.500000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>@cloudflare/workers-types</td>
      <td>3</td>
      <td>1</td>
      <td>5</td>
      <td>4.0</td>
      <td>3.333333</td>
      <td>2.081666</td>
    </tr>
    <tr>
      <th>19</th>
      <td>@types/babel__core</td>
      <td>3</td>
      <td>1</td>
      <td>2</td>
      <td>2.0</td>
      <td>1.666667</td>
      <td>0.577350</td>
    </tr>
  </tbody>
</table>
</div>



### Table 3d - Top 20 most widely spread external packages - percentage of internal elements

This table shows the top 20 most widely spread external packages focussing on the spread across the percentage of internal elements.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalModuleName</th>
      <th>numberOfInternalModules</th>
      <th>minNumberOfInternalElementsPercentage</th>
      <th>maxNumberOfInternalElementsPercentage</th>
      <th>medNumberOfInternalElementsPercentage</th>
      <th>avgNumberOfInternalElementsPercentage</th>
      <th>stdNumberOfInternalElementsPercentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>node</td>
      <td>21</td>
      <td>0.719424</td>
      <td>5.755396</td>
      <td>0.719424</td>
      <td>1.096266</td>
      <td>1.128810</td>
    </tr>
    <tr>
      <th>1</th>
      <td>@types/process</td>
      <td>17</td>
      <td>0.719424</td>
      <td>2.877698</td>
      <td>0.719424</td>
      <td>0.931020</td>
      <td>0.555211</td>
    </tr>
    <tr>
      <th>2</th>
      <td>dist</td>
      <td>15</td>
      <td>0.719424</td>
      <td>3.597122</td>
      <td>0.719424</td>
      <td>1.486811</td>
      <td>1.034238</td>
    </tr>
    <tr>
      <th>3</th>
      <td>@types/path</td>
      <td>13</td>
      <td>0.719424</td>
      <td>3.597122</td>
      <td>0.719424</td>
      <td>1.217488</td>
      <td>0.850455</td>
    </tr>
    <tr>
      <th>4</th>
      <td>node:fs</td>
      <td>9</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>1.039169</td>
      <td>0.634473</td>
    </tr>
    <tr>
      <th>5</th>
      <td>picocolors</td>
      <td>9</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>1.039169</td>
      <td>0.522650</td>
    </tr>
    <tr>
      <th>6</th>
      <td>promises</td>
      <td>8</td>
      <td>0.719424</td>
      <td>2.877698</td>
      <td>1.079137</td>
      <td>1.438849</td>
      <td>0.941948</td>
    </tr>
    <tr>
      <th>7</th>
      <td>@types/globals</td>
      <td>7</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>1.130524</td>
      <td>0.566040</td>
    </tr>
    <tr>
      <th>8</th>
      <td>@types/babel__generator</td>
      <td>6</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>0.959233</td>
      <td>0.587408</td>
    </tr>
    <tr>
      <th>9</th>
      <td>@types/buffer</td>
      <td>6</td>
      <td>0.719424</td>
      <td>1.438849</td>
      <td>0.719424</td>
      <td>0.839329</td>
      <td>0.293704</td>
    </tr>
    <tr>
      <th>10</th>
      <td>@types/react</td>
      <td>6</td>
      <td>0.719424</td>
      <td>10.071942</td>
      <td>2.877698</td>
      <td>4.556355</td>
      <td>4.111853</td>
    </tr>
    <tr>
      <th>11</th>
      <td>node:path</td>
      <td>6</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>1.079137</td>
      <td>1.318945</td>
      <td>0.707332</td>
    </tr>
    <tr>
      <th>12</th>
      <td>readline</td>
      <td>6</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>sisteransi</td>
      <td>6</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>@babel/lib</td>
      <td>5</td>
      <td>0.719424</td>
      <td>1.438849</td>
      <td>0.719424</td>
      <td>0.863309</td>
      <td>0.321736</td>
    </tr>
    <tr>
      <th>15</th>
      <td>fs</td>
      <td>5</td>
      <td>0.719424</td>
      <td>1.438849</td>
      <td>0.719424</td>
      <td>0.863309</td>
      <td>0.321736</td>
    </tr>
    <tr>
      <th>16</th>
      <td>http</td>
      <td>5</td>
      <td>0.719424</td>
      <td>1.438849</td>
      <td>0.719424</td>
      <td>1.007194</td>
      <td>0.394045</td>
    </tr>
    <tr>
      <th>17</th>
      <td>@types/pick</td>
      <td>4</td>
      <td>0.719424</td>
      <td>2.158273</td>
      <td>0.719424</td>
      <td>1.079137</td>
      <td>0.719424</td>
    </tr>
    <tr>
      <th>18</th>
      <td>@cloudflare/workers-types</td>
      <td>3</td>
      <td>0.719424</td>
      <td>3.597122</td>
      <td>2.877698</td>
      <td>2.398082</td>
      <td>1.497601</td>
    </tr>
    <tr>
      <th>19</th>
      <td>@types/babel__core</td>
      <td>3</td>
      <td>0.719424</td>
      <td>1.438849</td>
      <td>1.438849</td>
      <td>1.199041</td>
      <td>0.415360</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 3 Chart 1a - Most widely spread external module in % by internal elements (more than 0.5% overall)

External modules that are used less than 0.5% are grouped into the name "others" to get a cleaner chart with the most significant external module.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_43_1.png)
    


#### Table 3 Chart 1b - Most widely spread external modules in % by types (less than 0.5% overall "others" drill-down)

Shows the lowest (less than 0.5% overall) most widely spread external modules. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_45_1.png)
    


#### Table 3 Chart 2a - Most widely spread external modules in % by internal modules (more than 0.5% overall)

External modules that are used less than 0.5% are grouped into "others" to get a cleaner chart containing the most significant external modules.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_47_1.png)
    


#### Table 3 Chart 2b - Most widely spread external modules in % by internal modules (less than 0.5% overall "others" drill-down)

Shows the lowest (less than 0.5% overall) most widely spread external modules. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_49_1.png)
    


### Table 4 - Top 20 most widely spread external namespaces

This table shows external namespaces that are used by different internal modules with the most used first. 

Statistics like minimum, maximum, average, median and standard deviation are provided for the number of internally exported elements (function, class, ...) and the external declarations they use for every external namespace. 

The intuition behind that is to find external namespaces that are used in a widely spread manner. This can help to distinguish widely used libraries and frameworks from external modules that are used for specific tasks. It can also be used to find external modules that are used sparsely regarding internal modules but where many different external declarations are used. 

Refactoring with a [Hexagonal architecture](https://alistair.cockburn.us/hexagonal-architecture) in mind can be considered for non-framework external namespaces that are used for very specific tasks and that are used in many different internal locations. This makes the internal code more robust against changes of these external modules or it is easier to update and migrate to newer versions of them. 

External namespaces that are only used in very few internal locations overall might be considered for removal if they are easy to replace with a similar library that is already used more often. Or they might also simply be replaced by very few lines of code. Replacing libraries with own code isn't recommended when you need to write a lot of code or for external modules that provide security relevant implementations (encryption, sanitizers, ...), because they will be tracked and maintained globally and security updates need to be adopted fast.

Only the top 20 entries are shown. The whole table can be found in the following CSV report:
`External_namespace_usage_spread_for_Typescript`

**Columns:**
- *externalModuleNamespace* identifies the external namespace for at least on external module in use. All other columns contain aggregated data for it.
- *numberOfInternalModules* is the number of internal modules that are using that external module
- *\[min,max,med,avg,std\]NumberOfUsedExternalDeclarations* provide statistics for all internal modules and how their usage of the declarations provided by the external module are distributed. This provides an indicator on how strong the coupling to the external module is. For example, if many (high sum) elements provided by that external module are used constantly (low std), a higher coupling can be presumed. If there is only one (sum) element in use, this could be an indicator for an external module that could get replaced or that there is just one central entry point for it.
- *\[min/max/med/avg/std\]NumberOfInternalElements* provide statistics for all internal modules and how their usage of the external module is distributed across their internal elements. This provides an indicator on how widely an external module is spread across internal elements and if there are great differences between internal modules (high standard deviation) or not.
- *\[min/max/med/avg/std\]NumberOfInternalElementsPercentage* is similar to [min/max/med/avg/std]NumberOfUsedExternalDeclarations but provides the value in percent in relation to the total number of internal elements per internal module.
- *internalModuleExamples* some examples of included internal modules for debugging

### Table 4 - Top 20 most widely spread external namespaces

This table shows external namespaces that are used by different internal modules with the most used first. 

Statistics like minimum, maximum, average, median and standard deviation are provided for the number of internally exported elements (function, class, ...) and the external declarations they use for every external namespace. 

The intuition behind that is to find external namespaces that are used in a widely spread manner. This can help to distinguish widely used libraries and frameworks from external modules that are used for specific tasks. It can also be used to find external modules that are used sparsely regarding internal modules but where many different external declarations are used. 

Refactoring with a [Hexagonal architecture](https://alistair.cockburn.us/hexagonal-architecture) in mind can be considered for non-framework external namespaces that are used for very specific tasks and that are used in many different internal locations. This makes the internal code more robust against changes of these external modules or it is easier to update and migrate to newer versions of them. 

External namespaces that are only used in very few internal locations overall might be considered for removal if they are easy to replace with a similar library that is already used more often. Or they might also simply be replaced by very few lines of code. Replacing libraries with own code isn't recommended when you need to write a lot of code or for external modules that provide security relevant implementations (encryption, sanitizers, ...), because they will be tracked and maintained globally and security updates need to be adopted fast.

Only the top 20 entries are shown. The whole table can be found in the following CSV report:
`External_namespace_usage_spread_for_Typescript`

**Columns:**
- *externalModuleNamespace* identifies the external namespace for at least on external module in use. All other columns contain aggregated data for it.
- *numberOfInternalModules* is the number of internal modules that are using that external module
- *\[min,max,med,avg,std\]NumberOfUsedExternalDeclarations* provide statistics for all internal modules and how their usage of the declarations provided by the external module are distributed. This provides an indicator on how strong the coupling to the external module is. For example, if many (high sum) elements provided by that external module are used constantly (low std), a higher coupling can be presumed. If there is only one (sum) element in use, this could be an indicator for an external module that could get replaced or that there is just one central entry point for it.
- *\[min/max/med/avg/std\]NumberOfInternalElements* provide statistics for all internal modules and how their usage of the external module is distributed across their internal elements. This provides an indicator on how widely an external module is spread across internal elements and if there are great differences between internal modules (high standard deviation) or not.
- *\[min/max/med/avg/std\]NumberOfInternalElementsPercentage* is similar to [min/max/med/avg/std]NumberOfUsedExternalDeclarations but provides the value in percent in relation to the total number of internal elements per internal module.
- *internalModuleExamples* some examples of included internal modules for debugging




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalModuleNamespace</th>
      <th>numberOfInternalModules</th>
      <th>sumNumberOfUsedExternalDeclarations</th>
      <th>minNumberOfUsedExternalDeclarations</th>
      <th>maxNumberOfUsedExternalDeclarations</th>
      <th>medNumberOfUsedExternalDeclarations</th>
      <th>avgNumberOfUsedExternalDeclarations</th>
      <th>stdNumberOfUsedExternalDeclarations</th>
      <th>sumNumberOfInternalElements</th>
      <th>minNumberOfInternalElements</th>
      <th>maxNumberOfInternalElements</th>
      <th>medNumberOfInternalElements</th>
      <th>avgNumberOfInternalElements</th>
      <th>stdNumberOfInternalElements</th>
      <th>minNumberOfInternalElementsPercentage</th>
      <th>maxNumberOfInternalElementsPercentage</th>
      <th>medNumberOfInternalElementsPercentage</th>
      <th>avgNumberOfInternalElementsPercentage</th>
      <th>stdNumberOfInternalElementsPercentage</th>
      <th>internalModuleExamples</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>no namespace</td>
      <td>47</td>
      <td>505</td>
      <td>1</td>
      <td>119</td>
      <td>5.0</td>
      <td>10.744681</td>
      <td>23.184016</td>
      <td>108</td>
      <td>1</td>
      <td>13</td>
      <td>1.0</td>
      <td>2.297872</td>
      <td>2.385781</td>
      <td>0.719424</td>
      <td>9.352518</td>
      <td>0.719424</td>
      <td>1.653146</td>
      <td>1.716389</td>
      <td>[copy-template, create-react-router, prompts-c...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>@types</td>
      <td>44</td>
      <td>233</td>
      <td>1</td>
      <td>39</td>
      <td>3.0</td>
      <td>5.295455</td>
      <td>7.000264</td>
      <td>119</td>
      <td>1</td>
      <td>14</td>
      <td>1.0</td>
      <td>2.704545</td>
      <td>3.039121</td>
      <td>0.719424</td>
      <td>10.071942</td>
      <td>0.719424</td>
      <td>1.945716</td>
      <td>2.186418</td>
      <td>[create-react-router, loading-indicator, promp...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>@babel</td>
      <td>5</td>
      <td>51</td>
      <td>2</td>
      <td>17</td>
      <td>10.0</td>
      <td>10.200000</td>
      <td>6.418723</td>
      <td>6</td>
      <td>1</td>
      <td>2</td>
      <td>1.0</td>
      <td>1.200000</td>
      <td>0.447214</td>
      <td>0.719424</td>
      <td>1.438849</td>
      <td>0.719424</td>
      <td>0.863309</td>
      <td>0.321736</td>
      <td>[@react-router/useJavascript, @react-router/re...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>@cloudflare</td>
      <td>3</td>
      <td>44</td>
      <td>4</td>
      <td>22</td>
      <td>18.0</td>
      <td>14.666667</td>
      <td>9.451631</td>
      <td>10</td>
      <td>1</td>
      <td>5</td>
      <td>4.0</td>
      <td>3.333333</td>
      <td>2.081666</td>
      <td>0.719424</td>
      <td>3.597122</td>
      <td>2.877698</td>
      <td>2.398082</td>
      <td>1.497601</td>
      <td>[@react-router/react-router-cloudflare, @react...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>@architect</td>
      <td>2</td>
      <td>10</td>
      <td>5</td>
      <td>5</td>
      <td>5.0</td>
      <td>5.000000</td>
      <td>0.000000</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.719424</td>
      <td>0.000000</td>
      <td>[@react-router/react-router-architect, @react-...</td>
    </tr>
    <tr>
      <th>5</th>
      <td>@mjackson</td>
      <td>2</td>
      <td>4</td>
      <td>2</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>0.000000</td>
      <td>4</td>
      <td>2</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>0.000000</td>
      <td>1.438849</td>
      <td>1.438849</td>
      <td>1.438849</td>
      <td>1.438849</td>
      <td>0.000000</td>
      <td>[@react-router/react-router-node, @react-route...</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 4 Chart 1a - Most widely spread external namespaces in % by internal element (less than 0.5% overall)

External namespaces that are used less than 0.5% are grouped into "others" to get a cleaner chart
containing the most significant external namespaces and how ofter they are called in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_54_1.png)
    


#### Table 4 Chart 1b - Most widely spread external namespaces in % by internal element (less than 0.5% overall "others" drill-down)

Shows the lowest (less than 0.5% overall) most widely spread external namespaces. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.

    No data to plot for title 'Top external namespace usage spread [%] by internal elements (less than 0.7% overall "others" drill-down)'.


#### Table 4 Chart 2a - Most widely spread external namespace in % by internal modules (more than 0.5% overall)

External namespaces that are used less than 0.5% are grouped into "others" to get a cleaner chart
containing the most significant external namespaces and how ofter they are called in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_58_1.png)
    


#### Table 4 Chart 2b - Most widely spread external namespace in % by internal modules (less than 0.5% overall "others" drill-down)

Shows the lowest (less than 0.5% overall) most widely spread external namespaces. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.

    No data to plot for title 'Top external namespace usage spread [%] by internal modules (less than 0.7% overall "others" drill-down)'.


#### Table 4 Chart 3a - External namespaces with the most used declarations in % (more than 0.5% overall)

External namespaces that are used less than 0.5% are grouped into "others" to get a cleaner chart
containing the most significant external namespaces and how ofter they are called in percent.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_62_1.png)
    


#### Table 4 Chart 3b - External namespaces with the most used declarations in % (less than 0.5% overall "others" drill-down)

Shows the lowest (less than 0.5% overall) external namespaces with the most used declarations. Therefore, this plot breaks down the "others" slice of the pie chart above. Values under 0.3% from that will be grouped into "others" to get a cleaner plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_64_1.png)
    


### Table 5 - Top 20 least used external modules overall

This table identifies external modules that aren't used very often. This could help to find libraries that aren't actually needed or maybe easily replaceable. Some of them might be used sparsely on purpose for example as an adapter to an external library that is actually important. Thus, decisions need to be made on a case-by-case basis.

Only the last 20 entries are shown. The whole table can be found in the following CSV report:
`External_module_usage_overall_for_Typescript`

**Columns:**
- *externalModuleName* identifies the external package as described above
- *numberOfExternalDeclarationCalls* includes every invocation or reference to the declarations in the external module




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>externalModuleName</th>
      <th>numberOfExternalDeclarationCalls</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>types</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>@types/events</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>@types/APIGatewayProxyEventHeaders."x-forwarde...</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>@types/APIGatewayProxyEventHeaders."content-type</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>@types/isEqual</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>@types/timers</td>
      <td>1</td>
    </tr>
    <tr>
      <th>6</th>
      <td>arg.Result."--no-typescript</td>
      <td>1</td>
    </tr>
    <tr>
      <th>7</th>
      <td>exit-hook</td>
      <td>1</td>
    </tr>
    <tr>
      <th>8</th>
      <td>@types/kebabCase</td>
      <td>1</td>
    </tr>
    <tr>
      <th>9</th>
      <td>p-map</td>
      <td>1</td>
    </tr>
    <tr>
      <th>10</th>
      <td>node:child_process</td>
      <td>1</td>
    </tr>
    <tr>
      <th>11</th>
      <td>prettier</td>
      <td>2</td>
    </tr>
    <tr>
      <th>12</th>
      <td>url</td>
      <td>2</td>
    </tr>
    <tr>
      <th>13</th>
      <td>node:crypto</td>
      <td>2</td>
    </tr>
    <tr>
      <th>14</th>
      <td>arg</td>
      <td>2</td>
    </tr>
    <tr>
      <th>15</th>
      <td>module-runner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>16</th>
      <td>cli</td>
      <td>2</td>
    </tr>
    <tr>
      <th>17</th>
      <td>@types/jsesc</td>
      <td>2</td>
    </tr>
    <tr>
      <th>18</th>
      <td>@types/semver</td>
      <td>2</td>
    </tr>
    <tr>
      <th>19</th>
      <td>node:readline</td>
      <td>3</td>
    </tr>
  </tbody>
</table>
</div>



### Table 6 - External usage per internal module sorted by highest external element usage rate descending

The following table shows the most used external packages separately for each artifact including external annotations. The results are sorted by the artifacts with the highest external type usage rate descending. 

The intention of this table is to find artifacts that use a lot of external dependencies in relation to their size and get all the external packages and their usage.

Only the first 40 entries are shown. The whole table can be found in the following CSV report:
`External_module_usage_per_internal_module_sorted_for_Typescript`

**Columns:**
- *internalModuleName* is the internal module that uses the external one. Both are used here as a group for a more detailed analysis.
- *externalModuleName* is the external module prepended by its namespace if given. Example: "@types/react"
- *numberOfExternalDeclarationCaller* is the count of distinct internal elements in the internal module that call the external module
- *numberOfExternalDeclarationCalls* is the count of how often the external module is called within the internal module
- *numberOfAllElementsInInternalModule* is the total count of all exported elements of the internal module
- *numberOfAllExternalDeclarationsUsedInInternalModule* is the total count of all distinct external declarations used in the internal module
- *numberOfAllExternalModulesUsedInInternalModule* is the total count of all distinct external modules used in the internal module
- *externalDeclarationRate* is the numberOfAllExternalDeclarationsUsedInInternalModule / numberOfAllElementsInInternalModule * 100 of the internal module for all external modules
- *externalDeclarationNames* contains a list of actually used external declarations

#### Table 6a - External module usage per internal module sorted by highest external element usage rate descending




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>internalModuleName</th>
      <th>externalModuleName</th>
      <th>numberOfExternalDeclarationCaller</th>
      <th>numberOfExternalDeclarationCalls</th>
      <th>numberOfAllElementsInInternalModule</th>
      <th>numberOfAllExternalDeclarationsUsedInInternalModule</th>
      <th>numberOfAllExternalModulesUsedInInternalModule</th>
      <th>externalDeclarationRate</th>
      <th>externalDeclarationNames</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>vite</td>
      <td>node</td>
      <td>90</td>
      <td>152</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[Plugin, createLogger, UserConfig.environments...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>vite</td>
      <td>rollup</td>
      <td>8</td>
      <td>15</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[PluginContext.environment, ResolvedId.id, Plu...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>vite</td>
      <td>promises</td>
      <td>7</td>
      <td>15</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[rm, readdir, cp, mkdir, readFile, rename]</td>
    </tr>
    <tr>
      <th>3</th>
      <td>vite</td>
      <td>@types/babel__core</td>
      <td>6</td>
      <td>6</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[BabelFileResult.code, BabelFileResult.map, tr...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>vite</td>
      <td>@types/path</td>
      <td>6</td>
      <td>25</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[path.PlatformPath.dirname, path.PlatformPath....</td>
    </tr>
    <tr>
      <th>5</th>
      <td>vite</td>
      <td>dist</td>
      <td>6</td>
      <td>10</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[relative, dist, resolve, path.normalize, path...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>vite</td>
      <td>@types/process</td>
      <td>5</td>
      <td>9</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[global.NodeJS.Process.env, global.NodeJS.Proc...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>vite</td>
      <td>fs</td>
      <td>3</td>
      <td>6</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[Dirent.name, Dirent.path, Dirent.isFile]</td>
    </tr>
    <tr>
      <th>8</th>
      <td>vite</td>
      <td>node:fs</td>
      <td>3</td>
      <td>8</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[rmSync, readdirSync, existsSync]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>vite</td>
      <td>@types/babel__generator</td>
      <td>2</td>
      <td>2</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[GeneratorResult.code, GeneratorResult]</td>
    </tr>
    <tr>
      <th>10</th>
      <td>vite</td>
      <td>@types/globals</td>
      <td>2</td>
      <td>4</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[global.NodeRequire.resolve]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>vite</td>
      <td>crypto</td>
      <td>2</td>
      <td>2</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[Hash.digest, Hash.update]</td>
    </tr>
    <tr>
      <th>12</th>
      <td>vite</td>
      <td>http</td>
      <td>2</td>
      <td>2</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[ServerResponse.end, ServerResponse.setHeader]</td>
    </tr>
    <tr>
      <th>13</th>
      <td>vite</td>
      <td>lexer</td>
      <td>2</td>
      <td>2</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[init]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>vite</td>
      <td>picocolors</td>
      <td>2</td>
      <td>13</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[picocolors]</td>
    </tr>
    <tr>
      <th>15</th>
      <td>vite</td>
      <td>@types/buffer</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[global.Buffer.toString]</td>
    </tr>
    <tr>
      <th>16</th>
      <td>vite</td>
      <td>@types/jsesc</td>
      <td>1</td>
      <td>2</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[jsesc]</td>
    </tr>
    <tr>
      <th>17</th>
      <td>vite</td>
      <td>@types/pick</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[pick]</td>
    </tr>
    <tr>
      <th>18</th>
      <td>vite</td>
      <td>module-runner</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[ModuleRunner.import]</td>
    </tr>
    <tr>
      <th>19</th>
      <td>vite</td>
      <td>node:crypto</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[createHash]</td>
    </tr>
    <tr>
      <th>20</th>
      <td>vite</td>
      <td>node:url</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[.pathToFileURL]</td>
    </tr>
    <tr>
      <th>21</th>
      <td>vite</td>
      <td>url</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.0</td>
      <td>[URL.href]</td>
    </tr>
    <tr>
      <th>22</th>
      <td>remove-exports</td>
      <td>@babel/lib</td>
      <td>16</td>
      <td>56</td>
      <td>1</td>
      <td>23</td>
      <td>4</td>
      <td>2300.0</td>
      <td>[ExportSpecifier.exported, ExpressionStatement...</td>
    </tr>
    <tr>
      <th>23</th>
      <td>remove-exports</td>
      <td>@types/babel__traverse</td>
      <td>4</td>
      <td>24</td>
      <td>1</td>
      <td>23</td>
      <td>4</td>
      <td>2300.0</td>
      <td>[NodePath.remove, NodePath.parentPath, NodePat...</td>
    </tr>
    <tr>
      <th>24</th>
      <td>remove-exports</td>
      <td>dist</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>23</td>
      <td>4</td>
      <td>2300.0</td>
      <td>[deadCodeElimination, findReferencedIdentifiers]</td>
    </tr>
    <tr>
      <th>25</th>
      <td>remove-exports</td>
      <td>@babel/babel-parser</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>23</td>
      <td>4</td>
      <td>2300.0</td>
      <td>[ParseResult]</td>
    </tr>
    <tr>
      <th>26</th>
      <td>with-props</td>
      <td>@types/babel__traverse</td>
      <td>11</td>
      <td>23</td>
      <td>1</td>
      <td>21</td>
      <td>4</td>
      <td>2100.0</td>
      <td>[NodePath.isFunctionDeclaration, NodePath.get,...</td>
    </tr>
    <tr>
      <th>27</th>
      <td>with-props</td>
      <td>@babel/lib</td>
      <td>8</td>
      <td>11</td>
      <td>1</td>
      <td>21</td>
      <td>4</td>
      <td>2100.0</td>
      <td>[variableDeclarator, importDeclaration, variab...</td>
    </tr>
    <tr>
      <th>28</th>
      <td>with-props</td>
      <td>@babel/babel-parser</td>
      <td>2</td>
      <td>3</td>
      <td>1</td>
      <td>21</td>
      <td>4</td>
      <td>2100.0</td>
      <td>[ParseResult.program, ParseResult]</td>
    </tr>
    <tr>
      <th>29</th>
      <td>cloudflare</td>
      <td>node</td>
      <td>13</td>
      <td>18</td>
      <td>1</td>
      <td>15</td>
      <td>3</td>
      <td>1500.0</td>
      <td>[ResolvedConfig.server, ViteDevServer.config, ...</td>
    </tr>
    <tr>
      <th>30</th>
      <td>cloudflare</td>
      <td>@types/process</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>15</td>
      <td>3</td>
      <td>1500.0</td>
      <td>[global.NodeJS.Process.cwd]</td>
    </tr>
    <tr>
      <th>31</th>
      <td>cloudflare</td>
      <td>cli</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>15</td>
      <td>3</td>
      <td>1500.0</td>
      <td>[GetPlatformProxyOptions]</td>
    </tr>
    <tr>
      <th>32</th>
      <td>cloudflare-dev-proxy</td>
      <td>node</td>
      <td>13</td>
      <td>18</td>
      <td>1</td>
      <td>15</td>
      <td>3</td>
      <td>1500.0</td>
      <td>[ResolvedConfig.server, ViteDevServer.config, ...</td>
    </tr>
    <tr>
      <th>33</th>
      <td>cloudflare-dev-proxy</td>
      <td>@types/process</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>15</td>
      <td>3</td>
      <td>1500.0</td>
      <td>[global.NodeJS.Process.cwd]</td>
    </tr>
    <tr>
      <th>34</th>
      <td>cloudflare-dev-proxy</td>
      <td>cli</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>15</td>
      <td>3</td>
      <td>1500.0</td>
      <td>[GetPlatformProxyOptions]</td>
    </tr>
    <tr>
      <th>35</th>
      <td>warn-on-client-source-maps</td>
      <td>node</td>
      <td>11</td>
      <td>12</td>
      <td>1</td>
      <td>12</td>
      <td>2</td>
      <td>1200.0</td>
      <td>[ResolvedBuildOptions.ssr, Plugin, Logger.warn...</td>
    </tr>
    <tr>
      <th>36</th>
      <td>warn-on-client-source-maps</td>
      <td>picocolors</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>12</td>
      <td>2</td>
      <td>1200.0</td>
      <td>[picocolors]</td>
    </tr>
    <tr>
      <th>37</th>
      <td>run</td>
      <td>@types/process</td>
      <td>2</td>
      <td>4</td>
      <td>1</td>
      <td>8</td>
      <td>5</td>
      <td>800.0</td>
      <td>[global.NodeJS.ProcessVersions.node, global.No...</td>
    </tr>
    <tr>
      <th>38</th>
      <td>run</td>
      <td>@types/semver</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>8</td>
      <td>5</td>
      <td>800.0</td>
      <td>[semver, major]</td>
    </tr>
    <tr>
      <th>39</th>
      <td>run</td>
      <td>arg</td>
      <td>2</td>
      <td>3</td>
      <td>1</td>
      <td>8</td>
      <td>5</td>
      <td>800.0</td>
      <td>[arg.Result._, arg]</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 6b - External namespace usage per internal module sorted by highest external element usage rate descending




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>internalModuleName</th>
      <th>externalNamespaceName</th>
      <th>numberOfExternalDeclarationCaller</th>
      <th>numberOfExternalDeclarationCalls</th>
      <th>numberOfAllElementsInInternalModule</th>
      <th>numberOfAllExternalDeclarationsUsedInInternalModule</th>
      <th>numberOfAllExternalModulesUsedInInternalModule</th>
      <th>externalDeclarationRate</th>
      <th>externalDeclarationNames</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>vite</td>
      <td>no namespace</td>
      <td>129</td>
      <td>229</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.000000</td>
      <td>[Plugin, createLogger, UserConfig.environments...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>vite</td>
      <td>@types</td>
      <td>24</td>
      <td>50</td>
      <td>4</td>
      <td>133</td>
      <td>25</td>
      <td>3325.000000</td>
      <td>[global.NodeJS.Process.env, GeneratorResult.co...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>remove-exports</td>
      <td>@babel</td>
      <td>17</td>
      <td>58</td>
      <td>1</td>
      <td>23</td>
      <td>4</td>
      <td>2300.000000</td>
      <td>[ExportSpecifier.exported, ExpressionStatement...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>remove-exports</td>
      <td>@types</td>
      <td>4</td>
      <td>24</td>
      <td>1</td>
      <td>23</td>
      <td>4</td>
      <td>2300.000000</td>
      <td>[NodePath.remove, NodePath.parentPath, NodePat...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>remove-exports</td>
      <td>no namespace</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>23</td>
      <td>4</td>
      <td>2300.000000</td>
      <td>[deadCodeElimination, findReferencedIdentifiers]</td>
    </tr>
    <tr>
      <th>5</th>
      <td>with-props</td>
      <td>@types</td>
      <td>11</td>
      <td>23</td>
      <td>1</td>
      <td>21</td>
      <td>4</td>
      <td>2100.000000</td>
      <td>[NodePath.isFunctionDeclaration, NodePath.get,...</td>
    </tr>
    <tr>
      <th>6</th>
      <td>with-props</td>
      <td>@babel</td>
      <td>10</td>
      <td>14</td>
      <td>1</td>
      <td>21</td>
      <td>4</td>
      <td>2100.000000</td>
      <td>[variableDeclarator, importDeclaration, variab...</td>
    </tr>
    <tr>
      <th>7</th>
      <td>cloudflare</td>
      <td>no namespace</td>
      <td>14</td>
      <td>20</td>
      <td>1</td>
      <td>15</td>
      <td>3</td>
      <td>1500.000000</td>
      <td>[ResolvedConfig.server, ViteDevServer.config, ...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>cloudflare</td>
      <td>@types</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>15</td>
      <td>3</td>
      <td>1500.000000</td>
      <td>[global.NodeJS.Process.cwd]</td>
    </tr>
    <tr>
      <th>9</th>
      <td>cloudflare-dev-proxy</td>
      <td>no namespace</td>
      <td>14</td>
      <td>20</td>
      <td>1</td>
      <td>15</td>
      <td>3</td>
      <td>1500.000000</td>
      <td>[ResolvedConfig.server, ViteDevServer.config, ...</td>
    </tr>
    <tr>
      <th>10</th>
      <td>cloudflare-dev-proxy</td>
      <td>@types</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>15</td>
      <td>3</td>
      <td>1500.000000</td>
      <td>[global.NodeJS.Process.cwd]</td>
    </tr>
    <tr>
      <th>11</th>
      <td>warn-on-client-source-maps</td>
      <td>no namespace</td>
      <td>12</td>
      <td>14</td>
      <td>1</td>
      <td>12</td>
      <td>2</td>
      <td>1200.000000</td>
      <td>[ResolvedBuildOptions.ssr, Plugin, Logger.warn...</td>
    </tr>
    <tr>
      <th>12</th>
      <td>run</td>
      <td>@types</td>
      <td>5</td>
      <td>7</td>
      <td>1</td>
      <td>8</td>
      <td>5</td>
      <td>800.000000</td>
      <td>[semver, global.NodeJS.ProcessVersions.node, m...</td>
    </tr>
    <tr>
      <th>13</th>
      <td>run</td>
      <td>no namespace</td>
      <td>3</td>
      <td>4</td>
      <td>1</td>
      <td>8</td>
      <td>5</td>
      <td>800.000000</td>
      <td>[arg.Result."--no-typescript", arg.Result._, arg]</td>
    </tr>
    <tr>
      <th>14</th>
      <td>plugin</td>
      <td>no namespace</td>
      <td>152</td>
      <td>260</td>
      <td>18</td>
      <td>141</td>
      <td>26</td>
      <td>783.333333</td>
      <td>[RollupLog.code, UserConfig.environments, Roll...</td>
    </tr>
    <tr>
      <th>15</th>
      <td>plugin</td>
      <td>@types</td>
      <td>37</td>
      <td>68</td>
      <td>18</td>
      <td>141</td>
      <td>26</td>
      <td>783.333333</td>
      <td>[kebabCase, path.PlatformPath.join, global.Nod...</td>
    </tr>
    <tr>
      <th>16</th>
      <td>prompts-prompt-base</td>
      <td>no namespace</td>
      <td>10</td>
      <td>195</td>
      <td>2</td>
      <td>14</td>
      <td>6</td>
      <td>700.000000</td>
      <td>[.emitKeypressEvents, node:readline, node:proc...</td>
    </tr>
    <tr>
      <th>17</th>
      <td>prompts-prompt-base</td>
      <td>@types</td>
      <td>5</td>
      <td>53</td>
      <td>2</td>
      <td>14</td>
      <td>6</td>
      <td>700.000000</td>
      <td>[global.NodeJS.Process.stdin, global.NodeJS.Pr...</td>
    </tr>
    <tr>
      <th>18</th>
      <td>vite-node</td>
      <td>no namespace</td>
      <td>13</td>
      <td>14</td>
      <td>2</td>
      <td>13</td>
      <td>4</td>
      <td>650.000000</td>
      <td>[ViteNodeRunner, ViteNodeServer, ViteDevServer...</td>
    </tr>
    <tr>
      <th>19</th>
      <td>useJavascript</td>
      <td>@babel</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>6</td>
      <td>5</td>
      <td>600.000000</td>
      <td>[lib]</td>
    </tr>
    <tr>
      <th>20</th>
      <td>useJavascript</td>
      <td>@types</td>
      <td>2</td>
      <td>3</td>
      <td>1</td>
      <td>6</td>
      <td>5</td>
      <td>600.000000</td>
      <td>[transformSync, BabelFileResult.code]</td>
    </tr>
    <tr>
      <th>21</th>
      <td>useJavascript</td>
      <td>no namespace</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>6</td>
      <td>5</td>
      <td>600.000000</td>
      <td>[format, prettier]</td>
    </tr>
    <tr>
      <th>22</th>
      <td>arcTableSessionStorage</td>
      <td>@architect</td>
      <td>5</td>
      <td>7</td>
      <td>1</td>
      <td>5</td>
      <td>2</td>
      <td>500.000000</td>
      <td>[ArcTable.put, ArcTable.delete, functions, tab...</td>
    </tr>
    <tr>
      <th>23</th>
      <td>is-react-router-repo</td>
      <td>no namespace</td>
      <td>4</td>
      <td>6</td>
      <td>1</td>
      <td>5</td>
      <td>2</td>
      <td>500.000000</td>
      <td>[path.dirname, dist, path.resolve, path.basename]</td>
    </tr>
    <tr>
      <th>24</th>
      <td>is-react-router-repo</td>
      <td>@types</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>2</td>
      <td>500.000000</td>
      <td>[global.NodeRequire.resolve]</td>
    </tr>
    <tr>
      <th>25</th>
      <td>react-router-fs-routes</td>
      <td>no namespace</td>
      <td>3</td>
      <td>4</td>
      <td>1</td>
      <td>5</td>
      <td>3</td>
      <td>500.000000</td>
      <td>[.existsSync, node:path, node:fs]</td>
    </tr>
    <tr>
      <th>26</th>
      <td>react-router-fs-routes</td>
      <td>@types</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>5</td>
      <td>3</td>
      <td>500.000000</td>
      <td>[path.PlatformPath.relative, path.PlatformPath...</td>
    </tr>
    <tr>
      <th>27</th>
      <td>resolve-file-url</td>
      <td>@types</td>
      <td>4</td>
      <td>4</td>
      <td>1</td>
      <td>5</td>
      <td>2</td>
      <td>500.000000</td>
      <td>[path.PlatformPath.posix, path.PlatformPath.is...</td>
    </tr>
    <tr>
      <th>28</th>
      <td>resolve-file-url</td>
      <td>no namespace</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>5</td>
      <td>2</td>
      <td>500.000000</td>
      <td>[normalizePath]</td>
    </tr>
    <tr>
      <th>29</th>
      <td>fileStorage</td>
      <td>no namespace</td>
      <td>5</td>
      <td>14</td>
      <td>2</td>
      <td>9</td>
      <td>5</td>
      <td>450.000000</td>
      <td>[promises, .readFile, .unlink, .writeFile, .mk...</td>
    </tr>
    <tr>
      <th>30</th>
      <td>fileStorage</td>
      <td>@types</td>
      <td>4</td>
      <td>5</td>
      <td>2</td>
      <td>9</td>
      <td>5</td>
      <td>450.000000</td>
      <td>[path.PlatformPath.join, global.BufferConstruc...</td>
    </tr>
    <tr>
      <th>31</th>
      <td>load-dotenv</td>
      <td>no namespace</td>
      <td>3</td>
      <td>3</td>
      <td>1</td>
      <td>4</td>
      <td>3</td>
      <td>400.000000</td>
      <td>[loadEnv, UserConfig.envDir, UserConfig]</td>
    </tr>
    <tr>
      <th>32</th>
      <td>load-dotenv</td>
      <td>@types</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>3</td>
      <td>400.000000</td>
      <td>[global.NodeJS.Process.env]</td>
    </tr>
    <tr>
      <th>33</th>
      <td>prompts-text</td>
      <td>no namespace</td>
      <td>8</td>
      <td>104</td>
      <td>2</td>
      <td>8</td>
      <td>2</td>
      <td>400.000000</td>
      <td>[cursor.move, cursor.restore, Key, erase, curs...</td>
    </tr>
    <tr>
      <th>34</th>
      <td>workersKVStorage</td>
      <td>@cloudflare</td>
      <td>4</td>
      <td>6</td>
      <td>1</td>
      <td>4</td>
      <td>1</td>
      <td>400.000000</td>
      <td>[Crypto.getRandomValues, KVNamespace.put, KVNa...</td>
    </tr>
    <tr>
      <th>35</th>
      <td>react-router-cloudflare</td>
      <td>@cloudflare</td>
      <td>26</td>
      <td>34</td>
      <td>6</td>
      <td>22</td>
      <td>2</td>
      <td>366.666667</td>
      <td>[Response, EventContext, Crypto.getRandomValue...</td>
    </tr>
    <tr>
      <th>36</th>
      <td>worker</td>
      <td>@cloudflare</td>
      <td>22</td>
      <td>28</td>
      <td>5</td>
      <td>18</td>
      <td>2</td>
      <td>360.000000</td>
      <td>[Response.status, Response, Headers.delete, Ev...</td>
    </tr>
    <tr>
      <th>37</th>
      <td>has-rsc-plugin</td>
      <td>no namespace</td>
      <td>3</td>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>2</td>
      <td>300.000000</td>
      <td>[resolveConfig, ResolvedConfig.plugins, Plugin...</td>
    </tr>
    <tr>
      <th>38</th>
      <td>optimize-deps-entries</td>
      <td>no namespace</td>
      <td>3</td>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>2</td>
      <td>300.000000</td>
      <td>[normalizePath, escapePath, version]</td>
    </tr>
    <tr>
      <th>39</th>
      <td>profiler</td>
      <td>no namespace</td>
      <td>9</td>
      <td>13</td>
      <td>3</td>
      <td>9</td>
      <td>5</td>
      <td>300.000000</td>
      <td>[Session, node:fs, picocolors, Session.post, n...</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 6c - Top 15 used external modules with the internal modules that use them the most

The following table uses pivot to show the internal modules in columns, the external modules in rows and the number of internal elements using them as values.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>internalModuleName</th>
      <th>plugin</th>
      <th>vite</th>
      <th>server</th>
      <th>utils</th>
      <th>react-router</th>
      <th>config</th>
      <th>route-chunks</th>
      <th>routes</th>
      <th>context</th>
      <th>react-router-cloudflare</th>
      <th>remove-exports</th>
      <th>react-router-node</th>
      <th>worker</th>
      <th>with-props</th>
      <th>flatRoutes</th>
    </tr>
    <tr>
      <th>externalModuleName</th>
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
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>@architect/functions</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@architect/tables</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@babel/babel-parser</th>
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
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@babel/lib</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>32</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>16</td>
      <td>0</td>
      <td>0</td>
      <td>8</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@cloudflare/workers-types</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>26</td>
      <td>0</td>
      <td>0</td>
      <td>22</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@mjackson/node-fetch-server</th>
      <td>0</td>
      <td>0</td>
      <td>2</td>
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
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/APIGatewayProxyEventHeaders."content-type</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/APIGatewayProxyEventHeaders."x-forwarded-host</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/api-gateway-proxy</th>
      <td>0</td>
      <td>0</td>
      <td>18</td>
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
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/babel__core</th>
      <td>6</td>
      <td>6</td>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/babel__generator</th>
      <td>2</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>5</td>
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
      <th>@types/babel__traverse</th>
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
      <td>4</td>
      <td>0</td>
      <td>0</td>
      <td>11</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/buffer</th>
      <td>1</td>
      <td>1</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/events</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/express</th>
      <td>0</td>
      <td>0</td>
      <td>20</td>
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
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/express-serve-static-core</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/globals</th>
      <td>3</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
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
      <th>@types/handler</th>
      <td>0</td>
      <td>0</td>
      <td>2</td>
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
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/isEqual</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/jsesc</th>
      <td>1</td>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/kebabCase</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/path</th>
      <td>17</td>
      <td>6</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <th>@types/pick</th>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/process</th>
      <td>5</td>
      <td>5</td>
      <td>2</td>
      <td>7</td>
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
      <th>@types/qs</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/react</th>
      <td>0</td>
      <td>0</td>
      <td>6</td>
      <td>6</td>
      <td>31</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>27</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/semver</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/stream</th>
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
      <td>0</td>
      <td>9</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types/timers</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>arg</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>arg.Result."--no-typescript</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>async_hooks</th>
      <td>0</td>
      <td>0</td>
      <td>4</td>
      <td>0</td>
      <td>4</td>
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
      <th>cli</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>crypto</th>
      <td>2</td>
      <td>2</td>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>dist</th>
      <td>6</td>
      <td>6</td>
      <td>0</td>
      <td>0</td>
      <td>6</td>
      <td>15</td>
      <td>0</td>
      <td>30</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>esm</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>5</td>
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
      <th>exit-hook</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>fs</th>
      <td>3</td>
      <td>3</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>http</th>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
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
    </tr>
    <tr>
      <th>inspector</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>lexer</th>
      <td>2</td>
      <td>2</td>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>module-runner</th>
      <td>1</td>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>node</th>
      <td>105</td>
      <td>90</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
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
    </tr>
    <tr>
      <th>node:child_process</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>node:crypto</th>
      <td>1</td>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>node:fs</th>
      <td>5</td>
      <td>3</td>
      <td>0</td>
      <td>6</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>node:path</th>
      <td>0</td>
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
      <td>0</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>node:process</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
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
      <td>0</td>
    </tr>
    <tr>
      <th>node:readline</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>node:url</th>
      <td>1</td>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>p-map</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>picocolors</th>
      <td>3</td>
      <td>2</td>
      <td>0</td>
      <td>1</td>
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
      <th>prettier</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>promises</th>
      <td>10</td>
      <td>7</td>
      <td>0</td>
      <td>4</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>readline</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>4</td>
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
      <td>0</td>
    </tr>
    <tr>
      <th>rollup</th>
      <td>10</td>
      <td>8</td>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>server</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>sisteransi</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
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
      <td>0</td>
    </tr>
    <tr>
      <th>types</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>url</th>
      <td>1</td>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 6d - Top 15 used external namespaces with the internal modules that use them the most

The following table uses pivot to show the internal modules in columns, the external namespaces in rows and the number of internal elements using them as values.




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>internalModuleName</th>
      <th>plugin</th>
      <th>vite</th>
      <th>server</th>
      <th>utils</th>
      <th>react-router</th>
      <th>config</th>
      <th>route-chunks</th>
      <th>routes</th>
      <th>context</th>
      <th>react-router-cloudflare</th>
      <th>remove-exports</th>
      <th>react-router-node</th>
      <th>worker</th>
      <th>with-props</th>
      <th>flatRoutes</th>
    </tr>
    <tr>
      <th>externalNamespaceName</th>
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
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>@architect</th>
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
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@babel</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>32</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>17</td>
      <td>0</td>
      <td>0</td>
      <td>10</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@cloudflare</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>26</td>
      <td>0</td>
      <td>0</td>
      <td>22</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@mjackson</th>
      <td>0</td>
      <td>0</td>
      <td>2</td>
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
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>@types</th>
      <td>37</td>
      <td>24</td>
      <td>58</td>
      <td>15</td>
      <td>31</td>
      <td>7</td>
      <td>5</td>
      <td>3</td>
      <td>27</td>
      <td>0</td>
      <td>4</td>
      <td>14</td>
      <td>0</td>
      <td>11</td>
      <td>8</td>
    </tr>
    <tr>
      <th>no namespace</th>
      <td>152</td>
      <td>129</td>
      <td>6</td>
      <td>30</td>
      <td>10</td>
      <td>31</td>
      <td>0</td>
      <td>30</td>
      <td>0</td>
      <td>0</td>
      <td>2</td>
      <td>6</td>
      <td>0</td>
      <td>0</td>
      <td>10</td>
    </tr>
  </tbody>
</table>
</div>



### Table 6e - External usage per internal module and its elements

This table lists internal elements and the modules they belong to that use many different external declarations of a specific external module. 




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>internalModuleName</th>
      <th>numberOfAllExternalDeclarationsUsedInInternalModule</th>
      <th>numberOfAllElementsInInternalModule</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>vite</td>
      <td>133</td>
      <td>4</td>
    </tr>
    <tr>
      <th>22</th>
      <td>remove-exports</td>
      <td>23</td>
      <td>1</td>
    </tr>
    <tr>
      <th>26</th>
      <td>with-props</td>
      <td>21</td>
      <td>1</td>
    </tr>
    <tr>
      <th>29</th>
      <td>cloudflare</td>
      <td>15</td>
      <td>1</td>
    </tr>
    <tr>
      <th>32</th>
      <td>cloudflare-dev-proxy</td>
      <td>15</td>
      <td>1</td>
    </tr>
    <tr>
      <th>35</th>
      <td>warn-on-client-source-maps</td>
      <td>12</td>
      <td>1</td>
    </tr>
    <tr>
      <th>37</th>
      <td>run</td>
      <td>8</td>
      <td>1</td>
    </tr>
    <tr>
      <th>42</th>
      <td>plugin</td>
      <td>141</td>
      <td>18</td>
    </tr>
    <tr>
      <th>65</th>
      <td>prompts-prompt-base</td>
      <td>14</td>
      <td>2</td>
    </tr>
    <tr>
      <th>71</th>
      <td>vite-node</td>
      <td>13</td>
      <td>2</td>
    </tr>
    <tr>
      <th>74</th>
      <td>useJavascript</td>
      <td>6</td>
      <td>1</td>
    </tr>
    <tr>
      <th>77</th>
      <td>arcTableSessionStorage</td>
      <td>5</td>
      <td>1</td>
    </tr>
    <tr>
      <th>79</th>
      <td>is-react-router-repo</td>
      <td>5</td>
      <td>1</td>
    </tr>
    <tr>
      <th>81</th>
      <td>react-router-fs-routes</td>
      <td>5</td>
      <td>1</td>
    </tr>
    <tr>
      <th>84</th>
      <td>resolve-file-url</td>
      <td>5</td>
      <td>1</td>
    </tr>
    <tr>
      <th>86</th>
      <td>fileStorage</td>
      <td>9</td>
      <td>2</td>
    </tr>
    <tr>
      <th>90</th>
      <td>load-dotenv</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>92</th>
      <td>prompts-text</td>
      <td>8</td>
      <td>2</td>
    </tr>
    <tr>
      <th>94</th>
      <td>workersKVStorage</td>
      <td>4</td>
      <td>1</td>
    </tr>
    <tr>
      <th>95</th>
      <td>react-router-cloudflare</td>
      <td>22</td>
      <td>6</td>
    </tr>
    <tr>
      <th>96</th>
      <td>worker</td>
      <td>18</td>
      <td>5</td>
    </tr>
    <tr>
      <th>97</th>
      <td>has-rsc-plugin</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>98</th>
      <td>optimize-deps-entries</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>100</th>
      <td>profiler</td>
      <td>9</td>
      <td>3</td>
    </tr>
    <tr>
      <th>105</th>
      <td>resolve-relative-route-file-path</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>107</th>
      <td>styles</td>
      <td>12</td>
      <td>4</td>
    </tr>
    <tr>
      <th>112</th>
      <td>validate-plugin-order</td>
      <td>3</td>
      <td>1</td>
    </tr>
    <tr>
      <th>113</th>
      <td>dev</td>
      <td>13</td>
      <td>5</td>
    </tr>
    <tr>
      <th>116</th>
      <td>node-adapter</td>
      <td>5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>118</th>
      <td>prompts-multi-select</td>
      <td>5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>120</th>
      <td>react-router-architect</td>
      <td>10</td>
      <td>4</td>
    </tr>
    <tr>
      <th>124</th>
      <td>react-router-node</td>
      <td>17</td>
      <td>7</td>
    </tr>
    <tr>
      <th>131</th>
      <td>config</td>
      <td>31</td>
      <td>13</td>
    </tr>
    <tr>
      <th>142</th>
      <td>commands</td>
      <td>10</td>
      <td>5</td>
    </tr>
    <tr>
      <th>150</th>
      <td>loading-indicator</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>151</th>
      <td>prompts-select</td>
      <td>6</td>
      <td>3</td>
    </tr>
    <tr>
      <th>154</th>
      <td>virtual-route-config</td>
      <td>2</td>
      <td>1</td>
    </tr>
    <tr>
      <th>155</th>
      <td>prerender</td>
      <td>11</td>
      <td>6</td>
    </tr>
    <tr>
      <th>160</th>
      <td>stream</td>
      <td>7</td>
      <td>4</td>
    </tr>
    <tr>
      <th>162</th>
      <td>prompts-confirm</td>
      <td>5</td>
      <td>3</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 6 Chart 1 - Top 15 external dependency using artifacts and their external packages stacked

The following chart shows the top 15 external package using artifacts and breaks down which external packages they use in how many different internal packages with stacked bars. 

Note that every external dependency is counted separately so that if on internal package uses two external packages it will be displayed for both and so stacked twice.  


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_80_1.png)
    


#### Table 6 Chart 2 - Top 15 external dependency using artifacts and their external packages (first 2 levels) stacked

The following chart shows the top 15 external package using artifacts and breaks down which external packages (first 2 levels) are used in how many different internal packages with stacked bars. 

Note that every external dependency is counted separately so that if on internal package uses two external packages it will be displayed for both and so stacked twice.  


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_82_1.png)
    


### Table 7 - External module usage distribution per internal element

This table shows how many internal elements use one external module, how many use two, etc. .
This gives an overview of the distribution of external module calls and the overall coupling to external libraries. The higher the count of distinct external modules the lower should be the count of internal elements that use them. 
More details about which types have the highest external package dependency usage can be in the tables 4 and 5 above.

Only the last 40 entries are shown. The whole table can be found in the following CSV report:
`External_module_usage_per_internal_module_distribution_for_Typescript`

**Columns:**
- *internalModuleName* is the internal module that uses at least one external module. All other columns refer to it.
- *numberOfAllInternalElements* the total number of all elements that are exported by the internal module
- *externalModuleCount* is the number of distinct external modules used by the internal module
- *internalElementCount* is the number of distinct internal elements that use at least one external one
- *internalElementsCallingExternalRate* is internalElementCount / numberOfAllInternalElements * 100 (in %)




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>internalModuleName</th>
      <th>numberOfAllInternalElements</th>
      <th>externalModuleCount</th>
      <th>internalElementCount</th>
      <th>internalElementsCallingExternalRate</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>react-router</td>
      <td>179</td>
      <td>3</td>
      <td>21</td>
      <td>11.731844</td>
    </tr>
    <tr>
      <th>1</th>
      <td>server</td>
      <td>40</td>
      <td>13</td>
      <td>19</td>
      <td>47.500000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>utils</td>
      <td>144</td>
      <td>12</td>
      <td>15</td>
      <td>10.416667</td>
    </tr>
    <tr>
      <th>3</th>
      <td>context</td>
      <td>21</td>
      <td>1</td>
      <td>13</td>
      <td>61.904762</td>
    </tr>
    <tr>
      <th>4</th>
      <td>plugin</td>
      <td>18</td>
      <td>23</td>
      <td>11</td>
      <td>61.111111</td>
    </tr>
    <tr>
      <th>5</th>
      <td>routes</td>
      <td>19</td>
      <td>2</td>
      <td>8</td>
      <td>42.105263</td>
    </tr>
    <tr>
      <th>6</th>
      <td>react-router-node</td>
      <td>7</td>
      <td>7</td>
      <td>7</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>7</th>
      <td>config</td>
      <td>13</td>
      <td>11</td>
      <td>5</td>
      <td>38.461538</td>
    </tr>
    <tr>
      <th>8</th>
      <td>react-router-cloudflare</td>
      <td>6</td>
      <td>1</td>
      <td>5</td>
      <td>83.333333</td>
    </tr>
    <tr>
      <th>9</th>
      <td>routeModules</td>
      <td>21</td>
      <td>1</td>
      <td>5</td>
      <td>23.809524</td>
    </tr>
    <tr>
      <th>10</th>
      <td>commands</td>
      <td>5</td>
      <td>8</td>
      <td>4</td>
      <td>80.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>generate</td>
      <td>5</td>
      <td>2</td>
      <td>4</td>
      <td>80.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>stream</td>
      <td>4</td>
      <td>2</td>
      <td>4</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>13</th>
      <td>worker</td>
      <td>5</td>
      <td>1</td>
      <td>4</td>
      <td>80.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>cookies</td>
      <td>6</td>
      <td>1</td>
      <td>3</td>
      <td>50.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>flatRoutes</td>
      <td>13</td>
      <td>5</td>
      <td>3</td>
      <td>23.076923</td>
    </tr>
    <tr>
      <th>16</th>
      <td>profiler</td>
      <td>3</td>
      <td>5</td>
      <td>3</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>react-router-architect</td>
      <td>4</td>
      <td>4</td>
      <td>3</td>
      <td>75.000000</td>
    </tr>
    <tr>
      <th>18</th>
      <td>route-chunks</td>
      <td>12</td>
      <td>2</td>
      <td>3</td>
      <td>25.000000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>sessions</td>
      <td>11</td>
      <td>1</td>
      <td>3</td>
      <td>27.272727</td>
    </tr>
    <tr>
      <th>20</th>
      <td>vite</td>
      <td>4</td>
      <td>22</td>
      <td>3</td>
      <td>75.000000</td>
    </tr>
    <tr>
      <th>21</th>
      <td>dev</td>
      <td>5</td>
      <td>3</td>
      <td>2</td>
      <td>40.000000</td>
    </tr>
    <tr>
      <th>22</th>
      <td>fileStorage</td>
      <td>2</td>
      <td>4</td>
      <td>2</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>23</th>
      <td>node-adapter</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>24</th>
      <td>normalizeSlashes</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>25</th>
      <td>prompts-prompt-base</td>
      <td>2</td>
      <td>6</td>
      <td>2</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>26</th>
      <td>react-router-express</td>
      <td>3</td>
      <td>3</td>
      <td>2</td>
      <td>66.666667</td>
    </tr>
    <tr>
      <th>27</th>
      <td>styles</td>
      <td>4</td>
      <td>5</td>
      <td>2</td>
      <td>50.000000</td>
    </tr>
    <tr>
      <th>28</th>
      <td>typegen</td>
      <td>3</td>
      <td>3</td>
      <td>2</td>
      <td>66.666667</td>
    </tr>
    <tr>
      <th>29</th>
      <td>virtual-route-modules</td>
      <td>4</td>
      <td>3</td>
      <td>2</td>
      <td>50.000000</td>
    </tr>
    <tr>
      <th>30</th>
      <td>vite-node</td>
      <td>2</td>
      <td>3</td>
      <td>2</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>31</th>
      <td>arcTableSessionStorage</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>32</th>
      <td>babel</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>50.000000</td>
    </tr>
    <tr>
      <th>33</th>
      <td>build</td>
      <td>7</td>
      <td>1</td>
      <td>1</td>
      <td>14.285714</td>
    </tr>
    <tr>
      <th>34</th>
      <td>cloudflare</td>
      <td>1</td>
      <td>3</td>
      <td>1</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>35</th>
      <td>cloudflare-dev-proxy</td>
      <td>1</td>
      <td>3</td>
      <td>1</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>36</th>
      <td>copy-template</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>50.000000</td>
    </tr>
    <tr>
      <th>37</th>
      <td>create-react-router</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>50.000000</td>
    </tr>
    <tr>
      <th>38</th>
      <td>detectPackageManager</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>100.000000</td>
    </tr>
    <tr>
      <th>39</th>
      <td>fog-of-war</td>
      <td>6</td>
      <td>1</td>
      <td>1</td>
      <td>16.666667</td>
    </tr>
  </tbody>
</table>
</div>



### Table 8 - External package usage aggregated

This table lists all artifacts and their external package dependencies usage aggregated over internal packages. 

The intention behind this is to find artifacts that use an external dependency across multiple internal packages. This might be intended for frameworks and standardized libraries and helps to quantify how widely those are used. For some external dependencies it might be beneficial to only access it from one package and provide an abstraction for internal usage following a [Hexagonal architecture](https://alistair.cockburn.us/hexagonal-architecture). Thus, this table may also help in finding application for the Hexagonal architecture or similar approaches (Domain Driven Design Anti Corruption Layer). After all it is easier to update or replace such external dependencies when they are used in specific areas and not all over the code.

Only the last 40 entries are shown. The whole table can be found in the following CSV report:
`External_module_usage_per_internal_module_aggregated_for_Typescript`

**Columns:**
- *internalModuleName* that contains the type that calls the external package
- *internalModuleElementsCount* is the total count of packages in the internal module
- *numberOfExternalModules* the number of distinct external packages used
- *[min,max,med,avg,std]NumberOfInternalModules* provide statistics based on each external package and its package usage within the internal module
- *[min,max,med,avg,std]NumberOfInternalElements* provide statistics based on each external package and its type usage within the internal module
- *[min,max,med,avg,std]NumberOfTypePercentage* provide statistics in % based on each external package and its type usage within the internal module in respect to the overall count of packages in the internal module
- *numberOfinternalElements* in the internal module where the *numberOfExternalModules* applies
- *numberOfTypesPercentage* in the internal module where the *numberOfExternalModules* applies in %

#### Table 8a - External module usage aggregated - count of internal modules




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>internalModuleName</th>
      <th>internalModuleElementsCount</th>
      <th>numberOfExternalModules</th>
      <th>minNumberOfInternalModules</th>
      <th>medNumberOfInternalModules</th>
      <th>avgNumberOfInternalModules</th>
      <th>maxNumberOfInternalModules</th>
      <th>stdNumberOfInternalModules</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>react-router</td>
      <td>179</td>
      <td>3</td>
      <td>2</td>
      <td>3.0</td>
      <td>4.000000</td>
      <td>7</td>
      <td>2.645751</td>
    </tr>
    <tr>
      <th>1</th>
      <td>context</td>
      <td>19</td>
      <td>1</td>
      <td>3</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>3</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>cookies</td>
      <td>6</td>
      <td>1</td>
      <td>3</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>3</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>react-router-cloudflare</td>
      <td>6</td>
      <td>1</td>
      <td>3</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>3</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>react-router-node</td>
      <td>7</td>
      <td>7</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.142857</td>
      <td>3</td>
      <td>0.377964</td>
    </tr>
    <tr>
      <th>5</th>
      <td>server</td>
      <td>25</td>
      <td>2</td>
      <td>2</td>
      <td>2.5</td>
      <td>2.500000</td>
      <td>3</td>
      <td>0.707107</td>
    </tr>
    <tr>
      <th>6</th>
      <td>vite</td>
      <td>2</td>
      <td>22</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.318182</td>
      <td>3</td>
      <td>0.476731</td>
    </tr>
    <tr>
      <th>7</th>
      <td>arcTableSessionStorage</td>
      <td>1</td>
      <td>2</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>cloudflare</td>
      <td>1</td>
      <td>3</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>cloudflare-dev-proxy</td>
      <td>1</td>
      <td>3</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>fileStorage</td>
      <td>2</td>
      <td>4</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>fog-of-war</td>
      <td>6</td>
      <td>1</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>plugin</td>
      <td>17</td>
      <td>22</td>
      <td>1</td>
      <td>2.0</td>
      <td>1.954545</td>
      <td>2</td>
      <td>0.213201</td>
    </tr>
    <tr>
      <th>13</th>
      <td>plugin</td>
      <td>1</td>
      <td>8</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>react-router-architect</td>
      <td>4</td>
      <td>4</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>react-router-express</td>
      <td>3</td>
      <td>3</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>routes</td>
      <td>15</td>
      <td>2</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>17</th>
      <td>server</td>
      <td>6</td>
      <td>6</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.333333</td>
      <td>2</td>
      <td>0.516398</td>
    </tr>
    <tr>
      <th>18</th>
      <td>server</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>19</th>
      <td>server</td>
      <td>6</td>
      <td>4</td>
      <td>1</td>
      <td>2.0</td>
      <td>1.750000</td>
      <td>2</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>20</th>
      <td>stream</td>
      <td>4</td>
      <td>2</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>21</th>
      <td>utils</td>
      <td>86</td>
      <td>1</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>22</th>
      <td>worker</td>
      <td>5</td>
      <td>1</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>23</th>
      <td>workersKVStorage</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>24</th>
      <td>babel</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25</th>
      <td>build</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>26</th>
      <td>commands</td>
      <td>5</td>
      <td>8</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>27</th>
      <td>config</td>
      <td>13</td>
      <td>11</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>28</th>
      <td>copy-template</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>29</th>
      <td>create-react-router</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 8b - External module usage aggregated - count of internal elements




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>internalModuleName</th>
      <th>internalModuleElementsCount</th>
      <th>numberOfExternalModules</th>
      <th>minNumberOfInternalElements</th>
      <th>medNumberOfInternalElements</th>
      <th>avgNumberOfInternalElements</th>
      <th>maxNumberOfInternalElements</th>
      <th>stdNumberOfInternalElements</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>react-router</td>
      <td>179</td>
      <td>3</td>
      <td>3</td>
      <td>4.0</td>
      <td>7.000000</td>
      <td>14</td>
      <td>6.082763</td>
    </tr>
    <tr>
      <th>1</th>
      <td>context</td>
      <td>19</td>
      <td>1</td>
      <td>13</td>
      <td>13.0</td>
      <td>13.000000</td>
      <td>13</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>cookies</td>
      <td>6</td>
      <td>1</td>
      <td>3</td>
      <td>3.0</td>
      <td>3.000000</td>
      <td>3</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>react-router-cloudflare</td>
      <td>6</td>
      <td>1</td>
      <td>5</td>
      <td>5.0</td>
      <td>5.000000</td>
      <td>5</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>react-router-node</td>
      <td>7</td>
      <td>7</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.571429</td>
      <td>3</td>
      <td>0.786796</td>
    </tr>
    <tr>
      <th>5</th>
      <td>server</td>
      <td>25</td>
      <td>2</td>
      <td>3</td>
      <td>3.5</td>
      <td>3.500000</td>
      <td>4</td>
      <td>0.707107</td>
    </tr>
    <tr>
      <th>6</th>
      <td>vite</td>
      <td>2</td>
      <td>22</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.318182</td>
      <td>2</td>
      <td>0.476731</td>
    </tr>
    <tr>
      <th>7</th>
      <td>arcTableSessionStorage</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>cloudflare</td>
      <td>1</td>
      <td>3</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>cloudflare-dev-proxy</td>
      <td>1</td>
      <td>3</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>fileStorage</td>
      <td>2</td>
      <td>4</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.250000</td>
      <td>2</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>fog-of-war</td>
      <td>6</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>plugin</td>
      <td>17</td>
      <td>22</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.772727</td>
      <td>7</td>
      <td>1.540928</td>
    </tr>
    <tr>
      <th>13</th>
      <td>plugin</td>
      <td>1</td>
      <td>8</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>react-router-architect</td>
      <td>4</td>
      <td>4</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.250000</td>
      <td>2</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>react-router-express</td>
      <td>3</td>
      <td>3</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>routes</td>
      <td>15</td>
      <td>2</td>
      <td>3</td>
      <td>4.0</td>
      <td>4.000000</td>
      <td>5</td>
      <td>1.414214</td>
    </tr>
    <tr>
      <th>17</th>
      <td>server</td>
      <td>6</td>
      <td>6</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.666667</td>
      <td>5</td>
      <td>1.632993</td>
    </tr>
    <tr>
      <th>18</th>
      <td>server</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>1.5</td>
      <td>1.500000</td>
      <td>2</td>
      <td>0.707107</td>
    </tr>
    <tr>
      <th>19</th>
      <td>server</td>
      <td>6</td>
      <td>4</td>
      <td>1</td>
      <td>3.0</td>
      <td>2.750000</td>
      <td>4</td>
      <td>1.258306</td>
    </tr>
    <tr>
      <th>20</th>
      <td>stream</td>
      <td>4</td>
      <td>2</td>
      <td>1</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>3</td>
      <td>1.414214</td>
    </tr>
    <tr>
      <th>21</th>
      <td>utils</td>
      <td>86</td>
      <td>1</td>
      <td>2</td>
      <td>2.0</td>
      <td>2.000000</td>
      <td>2</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>22</th>
      <td>worker</td>
      <td>5</td>
      <td>1</td>
      <td>4</td>
      <td>4.0</td>
      <td>4.000000</td>
      <td>4</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>23</th>
      <td>workersKVStorage</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>24</th>
      <td>babel</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25</th>
      <td>build</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>26</th>
      <td>commands</td>
      <td>5</td>
      <td>8</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.250000</td>
      <td>2</td>
      <td>0.462910</td>
    </tr>
    <tr>
      <th>27</th>
      <td>config</td>
      <td>13</td>
      <td>11</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.363636</td>
      <td>4</td>
      <td>0.924416</td>
    </tr>
    <tr>
      <th>28</th>
      <td>copy-template</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>29</th>
      <td>create-react-router</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>1.0</td>
      <td>1.000000</td>
      <td>1</td>
      <td>0.000000</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 8c - External module usage aggregated - percentage of internal elements




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>internalModuleName</th>
      <th>internalModuleElementsCount</th>
      <th>numberOfExternalModules</th>
      <th>minNumberOfInternalElementsPercentage</th>
      <th>medNumberOfInternalElementsPercentage</th>
      <th>avgNumberOfInternalElementsPercentage</th>
      <th>maxNumberOfInternalElementsPercentage</th>
      <th>stdNumberOfInternalElementsPercentage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>react-router</td>
      <td>179</td>
      <td>3</td>
      <td>1.675978</td>
      <td>2.234637</td>
      <td>3.910615</td>
      <td>7.821229</td>
      <td>3.398191</td>
    </tr>
    <tr>
      <th>1</th>
      <td>context</td>
      <td>19</td>
      <td>1</td>
      <td>68.421053</td>
      <td>68.421053</td>
      <td>68.421053</td>
      <td>68.421053</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>cookies</td>
      <td>6</td>
      <td>1</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>react-router-cloudflare</td>
      <td>6</td>
      <td>1</td>
      <td>83.333333</td>
      <td>83.333333</td>
      <td>83.333333</td>
      <td>83.333333</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>4</th>
      <td>react-router-node</td>
      <td>7</td>
      <td>7</td>
      <td>14.285714</td>
      <td>14.285714</td>
      <td>22.448980</td>
      <td>42.857143</td>
      <td>11.239940</td>
    </tr>
    <tr>
      <th>5</th>
      <td>server</td>
      <td>25</td>
      <td>2</td>
      <td>12.000000</td>
      <td>14.000000</td>
      <td>14.000000</td>
      <td>16.000000</td>
      <td>2.828427</td>
    </tr>
    <tr>
      <th>6</th>
      <td>vite</td>
      <td>2</td>
      <td>22</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>65.909091</td>
      <td>100.000000</td>
      <td>23.836565</td>
    </tr>
    <tr>
      <th>7</th>
      <td>arcTableSessionStorage</td>
      <td>1</td>
      <td>2</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>cloudflare</td>
      <td>1</td>
      <td>3</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>9</th>
      <td>cloudflare-dev-proxy</td>
      <td>1</td>
      <td>3</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>10</th>
      <td>fileStorage</td>
      <td>2</td>
      <td>4</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>62.500000</td>
      <td>100.000000</td>
      <td>25.000000</td>
    </tr>
    <tr>
      <th>11</th>
      <td>fog-of-war</td>
      <td>6</td>
      <td>1</td>
      <td>16.666667</td>
      <td>16.666667</td>
      <td>16.666667</td>
      <td>16.666667</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>12</th>
      <td>plugin</td>
      <td>17</td>
      <td>22</td>
      <td>5.882353</td>
      <td>5.882353</td>
      <td>10.427807</td>
      <td>41.176471</td>
      <td>9.064282</td>
    </tr>
    <tr>
      <th>13</th>
      <td>plugin</td>
      <td>1</td>
      <td>8</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>14</th>
      <td>react-router-architect</td>
      <td>4</td>
      <td>4</td>
      <td>25.000000</td>
      <td>25.000000</td>
      <td>31.250000</td>
      <td>50.000000</td>
      <td>12.500000</td>
    </tr>
    <tr>
      <th>15</th>
      <td>react-router-express</td>
      <td>3</td>
      <td>3</td>
      <td>66.666667</td>
      <td>66.666667</td>
      <td>66.666667</td>
      <td>66.666667</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>16</th>
      <td>routes</td>
      <td>15</td>
      <td>2</td>
      <td>20.000000</td>
      <td>26.666667</td>
      <td>26.666667</td>
      <td>33.333333</td>
      <td>9.428090</td>
    </tr>
    <tr>
      <th>17</th>
      <td>server</td>
      <td>6</td>
      <td>6</td>
      <td>16.666667</td>
      <td>16.666667</td>
      <td>27.777778</td>
      <td>83.333333</td>
      <td>27.216553</td>
    </tr>
    <tr>
      <th>18</th>
      <td>server</td>
      <td>2</td>
      <td>2</td>
      <td>50.000000</td>
      <td>75.000000</td>
      <td>75.000000</td>
      <td>100.000000</td>
      <td>35.355339</td>
    </tr>
    <tr>
      <th>19</th>
      <td>server</td>
      <td>6</td>
      <td>4</td>
      <td>16.666667</td>
      <td>50.000000</td>
      <td>45.833333</td>
      <td>66.666667</td>
      <td>20.971762</td>
    </tr>
    <tr>
      <th>20</th>
      <td>stream</td>
      <td>4</td>
      <td>2</td>
      <td>25.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>75.000000</td>
      <td>35.355339</td>
    </tr>
    <tr>
      <th>21</th>
      <td>utils</td>
      <td>86</td>
      <td>1</td>
      <td>2.325581</td>
      <td>2.325581</td>
      <td>2.325581</td>
      <td>2.325581</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>22</th>
      <td>worker</td>
      <td>5</td>
      <td>1</td>
      <td>80.000000</td>
      <td>80.000000</td>
      <td>80.000000</td>
      <td>80.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>23</th>
      <td>workersKVStorage</td>
      <td>1</td>
      <td>1</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>24</th>
      <td>babel</td>
      <td>2</td>
      <td>1</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25</th>
      <td>build</td>
      <td>2</td>
      <td>1</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>26</th>
      <td>commands</td>
      <td>5</td>
      <td>8</td>
      <td>20.000000</td>
      <td>20.000000</td>
      <td>25.000000</td>
      <td>40.000000</td>
      <td>9.258201</td>
    </tr>
    <tr>
      <th>27</th>
      <td>config</td>
      <td>13</td>
      <td>11</td>
      <td>7.692308</td>
      <td>7.692308</td>
      <td>10.489510</td>
      <td>30.769231</td>
      <td>7.110894</td>
    </tr>
    <tr>
      <th>28</th>
      <td>copy-template</td>
      <td>2</td>
      <td>1</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>29</th>
      <td>create-react-router</td>
      <td>2</td>
      <td>2</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>0.000000</td>
    </tr>
  </tbody>
</table>
</div>



#### Table 8 Chart 1 - External module usage - max percentage of internal types

This chart shows per internal module the maximum percentage of internal packages (compared to all packages in that internal module) that use one specific external package. 

**Example:** One internal module might use 10 external packages where 7 of them are used in one internal package, 2 of them are used in two packages and one external dependency is used in 5 packages. So for this internal module there will be a point at x = 10 (external packages used by the internal module) and 5 (max internal packages). Instead of the count the percentage of internal packages compared to all packages in that internal module is used to get a normalized plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_95_1.png)
    


#### Table 8 Chart 2 - External package usage - median percentage of internal types

This chart shows per internal module the median (0.5 percentile) of internal packages (compared to all packages in that internal module) that use one specific external package. 

**Example:** One internal module might use 9 external packages where 3 of them are used in 1 internal package, 3 of them are used in 2 package and the last 3 ones are used in 3 packages. So for this internal module there will be a point at x = 10 (external packages used by the internal module) and 2 (median internal packages). Instead of the count the percentage of internal packages compared to all packages in that internal module is used to get a normalized plot.


    <Figure size 640x480 with 0 Axes>



    
![png](ExternalDependenciesTypescript_files/ExternalDependenciesTypescript_97_1.png)
    

