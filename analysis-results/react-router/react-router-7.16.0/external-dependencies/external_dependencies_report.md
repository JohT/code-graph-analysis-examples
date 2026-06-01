---
title: "External Dependencies Report"
generated: "2026-06-01"
model_version: "v4.0.1"
dataset: "react-router-7.16.0"
authors: ["JohT/code-graph-analysis-pipeline"]
---

# 📦 External Dependencies Report

## 1. Executive Overview

Analyzes which external packages, modules, and namespaces the codebase depends on, their spread, and per-artifact usage.

> **Who imports whom?**
> High spread (many internal modules referencing the same external package) = candidate for a **facade** or **anti-corruption layer**.

## 📚 Table of Contents

1. [Executive Overview](#1-executive-overview)
1. [Java External Dependencies](#2-java-external-dependencies)
1. [TypeScript External Dependencies](#3-typescript-external-dependencies)
1. [Package Management](#4-package-management)
1. [Glossary](#5-glossary)

---

## 2. Java External Dependencies

### 2.1 Most Used External Packages

External Java packages by internal caller type count. High `numberOfExternalCallerTypes` = deeply embedded.



### 2.2 Most Used External Packages — Second-Level Grouping

Second-level package names (e.g. `javax.xml` from `javax.xml.stream`) reveal **framework-level** coupling that is hidden when viewing full package names.



### 2.3 Most Spread External Packages

Packages referenced from the highest number of **different internal packages**.  
High spread indicates a pervasive cross-cutting dependency that is hard to replace.



### 2.4 External Package Usage per Artifact (Top)

Artifacts ranked by number of internal packages with external dependencies.



### 2.5 Aggregated External Package Usage per Artifact

Per-artifact: how many internal packages use external ones and their percentage.



### 2.6 Java Charts



---

## 3. TypeScript External Dependencies

### 3.1 Most Used External Modules

External npm modules ranked by how many internal TypeScript elements import them.

| externalModuleName | numberOfExternalCallerModules | numberOfExternalCallerElements | numberOfExternalDeclarationCalls | numberOfExternalDeclarationCallsWeighted | allModules | allInternalElements | exampleStories |
| --- | --- | --- | --- | --- | --- | --- | --- |
| node | 22 | 30 | 261 | 416 | 139 | 640 | ["<reactRouterVitePlugin> of module <plugin> imports <ModuleNode.file> from external module <node>","<reactRouterVitePlugin> of module <plugin> imports <ViteDevServer.pluginContainer> from external module <node>","<reactRouterVitePlugin> of module <plugin> imports <PreviewServer> from external module <node>","<reactRouterVitePlugin> of module <plugin> imports <ResolvedBuildOptions.assetsDir> from external module <node>"] |
| @types/process | 19 | 21 | 48 | 145 | 139 | 640 | ["<Context> of module <create-react-router> imports <global.NodeJS.WriteStream> from external module <process>","<Context> of module <create-react-router> imports <global.NodeJS.ReadStream> from external module <process>","<renderLoadingIndicator> of module <loading-indicator> imports <global.NodeJS.ReadStream> from external module <process>","<renderLoadingIndicator> of module <loading-indicator> imports <global.NodeJS.WriteStream> from external module <process>"] |
| dist | 17 | 27 | 104 | 296 | 139 | 640 | ["<relative> of module <routes> imports <resolve> from external module <dist>","<relative> of module <routes> imports <resolve> from external module <dist>","<reactRouterRSCVitePlugin> of module <plugin> imports <path.join> from external module <dist>","<reactRouterRSCVitePlugin> of module <plugin> imports <relative> from external module <dist>"] |
| @types/path | 14 | 20 | 55 | 122 | 139 | 640 | ["<stripDirectoryFromPath> of module <utils> imports <path.PlatformPath.sep> from external module <path>","<getDirectoryFilesRecursive> of module <utils> imports <path.PlatformPath.sep> from external module <path>","<createFileSessionStorage> of module <react-router-node> imports <path.PlatformPath.dirname> from external module <path>","<createFileSessionStorage> of module <fileStorage> imports <path.PlatformPath.dirname> from external module <path>"] |
| node:fs | 10 | 12 | 26 | 49 | 139 | 640 | ["<fileExists> of module <utils> imports <node:fs> from external module <node:fs>","<fileExists> of module <utils> imports <.promises> from external module <node:fs>","<ensureDirectory> of module <utils> imports <node:fs> from external module <node:fs>","<ensureDirectory> of module <utils> imports <.promises> from external module <node:fs>"] |
| picocolors | 10 | 11 | 14 | 85 | 139 | 640 | ["<color> of module <utils> imports <picocolors> from external module <picocolors>","<reactRouterVitePlugin> of module <plugin> imports <picocolors> from external module <picocolors>","<reactRouterVitePlugin> of module <vite> imports <picocolors> from external module <picocolors>","<reactRouterRSCVitePlugin> of module <plugin> imports <picocolors> from external module <picocolors>"] |
| promises | 9 | 13 | 37 | 59 | 139 | 640 | ["<fileExists> of module <utils> imports <.stat> from external module <promises>","<ensureDirectory> of module <utils> imports <.mkdir> from external module <promises>","<directoryExists> of module <utils> imports <.stat> from external module <promises>","<getDirectoryFilesRecursive> of module <utils> imports <readdir> from external module <promises>"] |
| @types/react | 8 | 24 | 91 | 292 | 139 | 640 | ["<AwaitContextProvider> of module <context> imports <React.ProviderProps> from external module <react>","<AwaitContextProvider> of module <context> imports <React.FunctionComponentElement> from external module <react>","<AwaitContextProvider> of module <context> imports <React.createElement> from external module <react>","<AwaitContextProvider> of module <context> imports <React.Context.Provider> from external module <react>"] |
| @types/module | 7 | 8 | 9 | 11 | 139 | 640 | ["<reactRouterVitePlugin> of module <plugin> imports <global.NodeJS.Require.resolve> from external module <module>","<reactRouterVitePlugin> of module <vite> imports <global.NodeJS.Require.resolve> from external module <module>","<generateEntry> of module <commands> imports <global.NodeJS.Require.resolve> from external module <module>","<run> of module <run> imports <global.NodeJS.Require.main> from external module <module>"] |
| http | 7 | 6 | 16 | 22 | 139 | 640 | ["<createRemixHeaders> of module <server> imports <IncomingHttpHeaders> from external module <http>","<createRequestListener> of module <server> imports <RequestListener> from external module <http>","<createRequestListener> of module <react-router-node> imports <RequestListener> from external module <http>","<reactRouterVitePlugin> of module <plugin> imports <ServerResponse.end> from external module <http>"] |
| node:path | 7 | 11 | 11 | 28 | 139 | 640 | ["<stripDirectoryFromPath> of module <utils> imports <node:path> from external module <node:path>","<getDirectoryFilesRecursive> of module <utils> imports <node:path> from external module <node:path>","<pathContains> of module <utils> imports <node:path> from external module <node:path>","<stop> of module <profiler> imports <node:path> from external module <node:path>"] |
| @types/babel__generator | 6 | 7 | 12 | 14 | 139 | 640 | ["<reactRouterVitePlugin> of module <plugin> imports <GeneratorResult.code> from external module <babel__generator>","<reactRouterVitePlugin> of module <plugin> imports <GeneratorResult> from external module <babel__generator>","<reactRouterVitePlugin> of module <vite> imports <GeneratorResult.code> from external module <babel__generator>","<reactRouterVitePlugin> of module <vite> imports <GeneratorResult> from external module <babel__generator>"] |
| @types/buffer | 6 | 4 | 12 | 13 | 139 | 640 | ["<createReactRouterRequest> of module <server> imports <global.BufferConstructor.from> from external module <buffer>","<createReactRouterRequest> of module <server> imports <global.Buffer.toString> from external module <buffer>","<readableStreamToString> of module <react-router-node> imports <global.BufferConstructor.concat> from external module <buffer>","<readableStreamToString> of module <react-router-node> imports <global.Buffer.toString> from external module <buffer>"] |
| fs | 6 | 6 | 17 | 27 | 139 | 640 | ["<fileExists> of module <utils> imports <Stats.isFile> from external module <fs>","<directoryExists> of module <utils> imports <Stats.isDirectory> from external module <fs>","<reactRouterVitePlugin> of module <plugin> imports <Dirent.name> from external module <fs>","<reactRouterVitePlugin> of module <plugin> imports <Dirent.isFile> from external module <fs>"] |
| readline | 6 | 6 | 10 | 104 | 139 | 640 | ["<ConfirmPrompt> of module <prompts-confirm> imports <Key> from external module <readline>","<MultiSelectPrompt> of module <prompts-multi-select> imports <Key> from external module <readline>","<Prompt> of module <prompts-prompt-base> imports <Interface.close> from external module <readline>","<Prompt> of module <prompts-prompt-base> imports <Key> from external module <readline>"] |
| sisteransi | 6 | 6 | 27 | 292 | 139 | 640 | ["<ConfirmPrompt> of module <prompts-confirm> imports <erase> from external module <sisteransi>","<ConfirmPrompt> of module <prompts-confirm> imports <cursor.hide> from external module <sisteransi>","<ConfirmPrompt> of module <prompts-confirm> imports <cursor.to> from external module <sisteransi>","<ConfirmPrompt> of module <prompts-confirm> imports <erase.line> from external module <sisteransi>"] |
| @babel/lib | 5 | 7 | 65 | 143 | 139 | 640 | ["<transpile> of module <useJavascript> imports <lib> from external module <lib>","<transpile> of module <useJavascript> imports <lib> from external module <lib>","<removeExports> of module <remove-exports> imports <ExportSpecifier.local> from external module <lib>","<removeExports> of module <remove-exports> imports <ExportNamedDeclaration.specifiers> from external module <lib>"] |
| @types/pick | 5 | 5 | 9 | 9 | 139 | 640 | ["<layout> of module <routes> imports <pick> from external module <pick>","<layout> of module <routes> imports <pick> from external module <pick>","<index> of module <routes> imports <pick> from external module <pick>","<index> of module <routes> imports <pick> from external module <pick>"] |
| lexer | 4 | 3 | 6 | 6 | 139 | 640 | ["<reactRouterVitePlugin> of module <plugin> imports <init> from external module <lexer>","<reactRouterVitePlugin> of module <vite> imports <init> from external module <lexer>","<reactRouterRSCVitePlugin> of module <plugin> imports <init> from external module <lexer>","<reactRouterRSCVitePlugin> of module <vite> imports <init> from external module <lexer>"] |
| @cloudflare/workers-types | 3 | 5 | 52 | 68 | 139 | 640 | ["<createWorkersKVSessionStorage> of module <react-router-cloudflare> imports <KVNamespace.get> from external module <workers-types>","<createWorkersKVSessionStorage> of module <react-router-cloudflare> imports <Crypto.getRandomValues> from external module <workers-types>","<createWorkersKVSessionStorage> of module <react-router-cloudflare> imports <KVNamespace.delete> from external module <workers-types>","<createWorkersKVSessionStorage> of module <react-router-cloudflare> imports <KVNamespace.put> from external module <workers-types>"] |
| @types/babel__core | 3 | 2 | 8 | 9 | 139 | 640 | ["<reactRouterVitePlugin> of module <plugin> imports <transformAsync> from external module <babel__core>","<reactRouterVitePlugin> of module <plugin> imports <BabelFileResult.code> from external module <babel__core>","<reactRouterVitePlugin> of module <plugin> imports <BabelFileResult.map> from external module <babel__core>","<reactRouterVitePlugin> of module <vite> imports <transformAsync> from external module <babel__core>"] |
| @types/babel__traverse | 3 | 3 | 17 | 49 | 139 | 640 | ["<removeExports> of module <remove-exports> imports <NodePath.remove> from external module <babel__traverse>","<removeExports> of module <remove-exports> imports <NodePath.parentPath> from external module <babel__traverse>","<removeExports> of module <remove-exports> imports <NodePath.isProgram> from external module <babel__traverse>","<removeExports> of module <remove-exports> imports <NodePath.node> from external module <babel__traverse>"] |
| node:process | 3 | 7 | 7 | 138 | 139 | 640 | ["<Context> of module <create-react-router> imports <node:process> from external module <node:process>","<Prompt> of module <prompts-prompt-base> imports <node:process> from external module <node:process>","<PromptOptions> of module <prompts-prompt-base> imports <node:process> from external module <node:process>","<setStderr> of module <utils> imports <node:process> from external module <node:process>"] |
| node:url | 3 | 2 | 4 | 6 | 139 | 640 | ["<copyTemplate> of module <copy-template> imports <.fileURLToPath> from external module <node:url>","<copyTemplate> of module <copy-template> imports <node:url> from external module <node:url>","<reactRouterVitePlugin> of module <plugin> imports <.pathToFileURL> from external module <node:url>","<reactRouterVitePlugin> of module <vite> imports <.pathToFileURL> from external module <node:url>"] |
| @architect/functions | 2 | 1 | 4 | 4 | 139 | 640 | ["<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <tables> from external module <functions>","<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <functions> from external module <functions>","<createArcTableSessionStorage> of module <react-router-architect> imports <tables> from external module <functions>","<createArcTableSessionStorage> of module <react-router-architect> imports <functions> from external module <functions>"] |
| @architect/tables | 2 | 1 | 6 | 10 | 139 | 640 | ["<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <ArcTable.put> from external module <tables>","<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <ArcTable.delete> from external module <tables>","<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <ArcTable.get> from external module <tables>","<createArcTableSessionStorage> of module <react-router-architect> imports <ArcTable.put> from external module <tables>"] |
| @babel/babel-parser | 2 | 2 | 3 | 5 | 139 | 640 | ["<removeExports> of module <remove-exports> imports <ParseResult> from external module <babel-parser>","<decorateComponentExportsWithProps> of module <with-props> imports <ParseResult> from external module <babel-parser>","<decorateComponentExportsWithProps> of module <with-props> imports <ParseResult.program> from external module <babel-parser>"] |
| @mjackson/node-fetch-server | 2 | 2 | 4 | 18 | 139 | 640 | ["<createRequestListener> of module <server> imports <createRequestListener> from external module <node-fetch-server>","<createRequestListener> of module <react-router-node> imports <createRequestListener> from external module <node-fetch-server>","<RequestListenerOptions> of module <server> imports <ClientAddress> from external module <node-fetch-server>","<RequestListenerOptions> of module <react-router-node> imports <ClientAddress> from external module <node-fetch-server>"] |
| @types/api-gateway-proxy | 2 | 5 | 23 | 30 | 139 | 640 | ["<GetLoadContextFunction> of module <react-router-architect> imports <APIGatewayEventRequestContextV2> from external module <api-gateway-proxy>","<GetLoadContextFunction> of module <react-router-architect> imports <APIGatewayProxyEventV2> from external module <api-gateway-proxy>","<GetLoadContextFunction> of module <server> imports <APIGatewayEventRequestContextV2> from external module <api-gateway-proxy>","<GetLoadContextFunction> of module <server> imports <APIGatewayProxyEventV2> from external module <api-gateway-proxy>"] |
| @types/express | 2 | 4 | 25 | 29 | 139 | 640 | ["<RequestHandler> of module <server> imports <e.Response> from external module <express>","<RequestHandler> of module <server> imports <e.NextFunction> from external module <express>","<RequestHandler> of module <server> imports <e.Request> from external module <express>","<RequestHandler> of module <react-router-express> imports <e.Response> from external module <express>"] |
| @types/express-serve-static-core | 2 | 3 | 5 | 5 | 139 | 640 | ["<RequestHandler> of module <server> imports <ParamsDictionary> from external module <express-serve-static-core>","<RequestHandler> of module <react-router-express> imports <ParamsDictionary> from external module <express-serve-static-core>","<GetLoadContextFunction> of module <server> imports <ParamsDictionary> from external module <express-serve-static-core>","<GetLoadContextFunction> of module <react-router-express> imports <ParamsDictionary> from external module <express-serve-static-core>"] |
| @types/handler | 2 | 1 | 4 | 4 | 139 | 640 | ["<RequestHandler> of module <react-router-architect> imports <Context> from external module <handler>","<RequestHandler> of module <react-router-architect> imports <Callback> from external module <handler>","<RequestHandler> of module <server> imports <Context> from external module <handler>","<RequestHandler> of module <server> imports <Callback> from external module <handler>"] |
| @types/jsesc | 2 | 1 | 2 | 4 | 139 | 640 | ["<reactRouterVitePlugin> of module <plugin> imports <jsesc> from external module <jsesc>","<reactRouterVitePlugin> of module <vite> imports <jsesc> from external module <jsesc>"] |
| @types/qs | 2 | 3 | 5 | 5 | 139 | 640 | ["<RequestHandler> of module <server> imports <QueryString.ParsedQs> from external module <qs>","<RequestHandler> of module <react-router-express> imports <QueryString.ParsedQs> from external module <qs>","<GetLoadContextFunction> of module <server> imports <QueryString.ParsedQs> from external module <qs>","<GetLoadContextFunction> of module <react-router-express> imports <QueryString.ParsedQs> from external module <qs>"] |
| @types/stream | 2 | 3 | 18 | 20 | 139 | 640 | ["<writeReadableStreamToWritable> of module <react-router-node> imports <Stream.Writable> from external module <stream>","<writeReadableStreamToWritable> of module <react-router-node> imports <Stream.Writable.write> from external module <stream>","<writeReadableStreamToWritable> of module <react-router-node> imports <Stream.Writable.destroy> from external module <stream>","<writeReadableStreamToWritable> of module <react-router-node> imports <Stream.Writable.end> from external module <stream>"] |
| async_hooks | 2 | 4 | 8 | 8 | 139 | 640 | ["<replace> of module <react-router> imports <AsyncLocalStorage.getStore> from external module <async_hooks>","<replace> of module <server> imports <AsyncLocalStorage.getStore> from external module <async_hooks>","<redirectDocument> of module <server> imports <AsyncLocalStorage.getStore> from external module <async_hooks>","<redirectDocument> of module <react-router> imports <AsyncLocalStorage.getStore> from external module <async_hooks>"] |
| cli | 2 | 1 | 2 | 4 | 139 | 640 | ["<cloudflareDevProxyVitePlugin> of module <cloudflare> imports <GetPlatformProxyOptions> from external module <cli>","<cloudflareDevProxyVitePlugin> of module <cloudflare-dev-proxy> imports <GetPlatformProxyOptions> from external module <cli>"] |
| crypto | 2 | 1 | 4 | 4 | 139 | 640 | ["<reactRouterVitePlugin> of module <plugin> imports <Hash.update> from external module <crypto>","<reactRouterVitePlugin> of module <plugin> imports <Hash.digest> from external module <crypto>","<reactRouterVitePlugin> of module <vite> imports <Hash.update> from external module <crypto>","<reactRouterVitePlugin> of module <vite> imports <Hash.digest> from external module <crypto>"] |
| esm | 2 | 2 | 6 | 7 | 139 | 640 | ["<createConfigLoader> of module <config> imports <FSWatcher.unwatch> from external module <esm>","<createConfigLoader> of module <config> imports <_default.watch> from external module <esm>","<createConfigLoader> of module <config> imports <esm> from external module <esm>","<createConfigLoader> of module <config> imports <FSWatcher.on> from external module <esm>"] |
| module-runner | 2 | 1 | 2 | 2 | 139 | 640 | ["<reactRouterVitePlugin> of module <plugin> imports <ModuleRunner.import> from external module <module-runner>","<reactRouterVitePlugin> of module <vite> imports <ModuleRunner.import> from external module <module-runner>"] |
| node:crypto | 2 | 1 | 2 | 2 | 139 | 640 | ["<reactRouterVitePlugin> of module <plugin> imports <createHash> from external module <node:crypto>","<reactRouterVitePlugin> of module <vite> imports <createHash> from external module <node:crypto>"] |
| rollup | 2 | 1 | 6 | 10 | 139 | 640 | ["<reactRouterVitePlugin> of module <plugin> imports <PluginContext.resolve> from external module <rollup>","<reactRouterVitePlugin> of module <plugin> imports <PluginContext.environment> from external module <rollup>","<reactRouterVitePlugin> of module <plugin> imports <ResolvedId.id> from external module <rollup>","<reactRouterVitePlugin> of module <vite> imports <PluginContext.resolve> from external module <rollup>"] |
| url | 2 | 1 | 2 | 4 | 139 | 640 | ["<reactRouterVitePlugin> of module <plugin> imports <URL.href> from external module <url>","<reactRouterVitePlugin> of module <vite> imports <URL.href> from external module <url>"] |
| @types/APIGatewayProxyEventHeaders."content-type | 1 | 1 | 1 | 1 | 139 | 640 | ["<createReactRouterRequest> of module <server> imports <APIGatewayProxyEventHeaders.\"content-type\"> from external module <APIGatewayProxyEventHeaders.\"content-type>"] |
| @types/APIGatewayProxyEventHeaders."x-forwarded-host | 1 | 1 | 1 | 1 | 139 | 640 | ["<createReactRouterRequest> of module <server> imports <APIGatewayProxyEventHeaders.\"x-forwarded-host\"> from external module <APIGatewayProxyEventHeaders.\"x-forwarded-host>"] |
| @types/events | 1 | 1 | 1 | 1 | 139 | 640 | ["<Prompt> of module <prompts-prompt-base> imports <EventEmitter> from external module <events>"] |
| @types/isEqual | 1 | 1 | 1 | 2 | 139 | 640 | ["<createConfigLoader> of module <config> imports <isEqual> from external module <isEqual>"] |
| @types/kebabCase | 1 | 1 | 1 | 1 | 139 | 640 | ["<getEnvironmentOptionsResolvers> of module <plugin> imports <kebabCase> from external module <kebabCase>"] |
| @types/semver | 1 | 1 | 2 | 2 | 139 | 640 | ["<run> of module <run> imports <major> from external module <semver>","<run> of module <run> imports <semver> from external module <semver>"] |
| @types/timers | 1 | 1 | 1 | 13 | 139 | 640 | ["<SelectPrompt> of module <prompts-select> imports <global.NodeJS.Timeout> from external module <timers>"] |
| arg | 1 | 1 | 2 | 3 | 139 | 640 | ["<run> of module <run> imports <arg> from external module <arg>","<run> of module <run> imports <arg.Result._> from external module <arg>"] |
| arg.Result."--no-typescript | 1 | 1 | 1 | 1 | 139 | 640 | ["<run> of module <run> imports <arg.Result.\"--no-typescript\"> from external module <arg.Result.\"--no-typescript>"] |
| exit-hook | 1 | 1 | 1 | 1 | 139 | 640 | ["<dev> of module <commands> imports <exit-hook> from external module <exit-hook>"] |
| inspector | 1 | 3 | 4 | 6 | 139 | 640 | ["<stop> of module <profiler> imports <Session.post> from external module <inspector>","<start> of module <profiler> imports <Session.connect> from external module <inspector>","<start> of module <profiler> imports <Session.post> from external module <inspector>","<getSession> of module <profiler> imports <Session> from external module <inspector>"] |
| node:child_process | 1 | 1 | 1 | 1 | 139 | 640 | ["<resolveEntryFiles> of module <config> imports <execSync> from external module <node:child_process>"] |
| node:inspector | 1 | 1 | 1 | 1 | 139 | 640 | ["<start> of module <profiler> imports <.Session> from external module <node:inspector>"] |
| node:readline | 1 | 1 | 3 | 52 | 139 | 640 | ["<Prompt> of module <prompts-prompt-base> imports <.createInterface> from external module <node:readline>","<Prompt> of module <prompts-prompt-base> imports <node:readline> from external module <node:readline>","<Prompt> of module <prompts-prompt-base> imports <.emitKeypressEvents> from external module <node:readline>"] |
| p-map | 1 | 1 | 1 | 1 | 139 | 640 | ["<prerender> of module <prerender> imports <p-map> from external module <p-map>"] |
| prettier | 1 | 1 | 2 | 2 | 139 | 640 | ["<transpile> of module <useJavascript> imports <prettier> from external module <prettier>","<transpile> of module <useJavascript> imports <format> from external module <prettier>"] |
| server | 1 | 2 | 4 | 4 | 139 | 640 | ["<Context> of module <vite-node> imports <ViteNodeServer> from external module <server>","<createContext> of module <vite-node> imports <ViteNodeServer.resolveId> from external module <server>","<createContext> of module <vite-node> imports <ViteNodeServer.fetchModule> from external module <server>","<createContext> of module <vite-node> imports <ViteNodeServer.getSourceMap> from external module <server>"] |
| types | 1 | 1 | 1 | 2 | 139 | 640 | ["<color> of module <utils> imports <Formatter> from external module <types>"] |

### 3.2 Most Used External Namespaces

Groups by namespace to reveal declaration-level coupling within npm packages.

| externalNamespaceName | numberOfExternalCallerModules | numberOfExternalCallerElements | numberOfExternalDeclarationCalls | numberOfExternalDeclarationCallsWeighted | allModules | allInternalElements | exampleStories |
| --- | --- | --- | --- | --- | --- | --- | --- |
| no namespace | 53 | 97 | 593 | 1643 | 139 | 640 | ["<copyTemplate> of module <copy-template> imports <.fileURLToPath> from external namespace <>","<copyTemplate> of module <copy-template> imports <node:url> from external namespace <>","<Context> of module <create-react-router> imports <node:process> from external namespace <>","<ConfirmPrompt> of module <prompts-confirm> imports <Key> from external namespace <>"] |
| @types | 51 | 93 | 351 | 782 | 139 | 640 | ["<Context> of module <create-react-router> imports <global.NodeJS.WriteStream> from external namespace <@types>","<Context> of module <create-react-router> imports <global.NodeJS.ReadStream> from external namespace <@types>","<renderLoadingIndicator> of module <loading-indicator> imports <global.NodeJS.ReadStream> from external namespace <@types>","<renderLoadingIndicator> of module <loading-indicator> imports <global.NodeJS.WriteStream> from external namespace <@types>"] |
| @babel | 5 | 7 | 68 | 148 | 139 | 640 | ["<transpile> of module <useJavascript> imports <lib> from external namespace <@babel>","<transpile> of module <useJavascript> imports <lib> from external namespace <@babel>","<removeExports> of module <remove-exports> imports <ExportSpecifier.local> from external namespace <@babel>","<removeExports> of module <remove-exports> imports <ExportNamedDeclaration.specifiers> from external namespace <@babel>"] |
| @cloudflare | 3 | 5 | 52 | 68 | 139 | 640 | ["<createWorkersKVSessionStorage> of module <react-router-cloudflare> imports <KVNamespace.get> from external namespace <@cloudflare>","<createWorkersKVSessionStorage> of module <react-router-cloudflare> imports <Crypto.getRandomValues> from external namespace <@cloudflare>","<createWorkersKVSessionStorage> of module <react-router-cloudflare> imports <KVNamespace.delete> from external namespace <@cloudflare>","<createWorkersKVSessionStorage> of module <react-router-cloudflare> imports <KVNamespace.put> from external namespace <@cloudflare>"] |
| @architect | 2 | 1 | 10 | 14 | 139 | 640 | ["<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <tables> from external namespace <@architect>","<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <ArcTable.put> from external namespace <@architect>","<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <functions> from external namespace <@architect>","<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <ArcTable.delete> from external namespace <@architect>"] |
| @mjackson | 2 | 2 | 4 | 18 | 139 | 640 | ["<createRequestListener> of module <server> imports <createRequestListener> from external namespace <@mjackson>","<createRequestListener> of module <react-router-node> imports <createRequestListener> from external namespace <@mjackson>","<RequestListenerOptions> of module <server> imports <ClientAddress> from external namespace <@mjackson>","<RequestListenerOptions> of module <react-router-node> imports <ClientAddress> from external namespace <@mjackson>"] |

### 3.3 Most Spread External Modules

External modules referenced from the highest number of **different internal TypeScript modules**.

| externalModuleName | numberOfInternalModules | sumNumberOfUsedExternalDeclarations | minNumberOfUsedExternalDeclarations | maxNumberOfUsedExternalDeclarations | medNumberOfUsedExternalDeclarations | avgNumberOfUsedExternalDeclarations | stdNumberOfUsedExternalDeclarations | sumNumberOfInternalElements | minNumberOfInternalElements | maxNumberOfInternalElements | medNumberOfInternalElements | avgNumberOfInternalElements | stdNumberOfInternalElements | minNumberOfInternalElementsPercentage | maxNumberOfInternalElementsPercentage | medNumberOfInternalElementsPercentage | avgNumberOfInternalElementsPercentage | stdNumberOfInternalElementsPercentage | internalModuleExamples |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| node | 20 | 229 | 1 | 75 | 3 | 11.450000000000005 | 21.60768625427438 | 33 | 1 | 8 | 1 | 1.65 | 1.7554426642213128 | 0.15625 | 1.25 | 0.15625 | 0.2578125 | 0.27428791628458016 | ["plugin","vite","commands","config"] |
| @types/process | 17 | 42 | 1 | 5 | 2 | 2.4705882352941178 | 1.5458673560021057 | 24 | 1 | 4 | 1 | 1.411764705882353 | 0.7952062255644574 | 0.15625 | 0.625 | 0.15625 | 0.22058823529411764 | 0.12425097274444645 | ["create-react-router","loading-indicator","prompts-prompt-base","utils"] |
| dist | 15 | 80 | 1 | 26 | 4 | 5.333333333333333 | 6.309478885734052 | 31 | 1 | 5 | 1 | 2.066666666666667 | 1.4375905768565218 | 0.15625 | 0.78125 | 0.15625 | 0.32291666666666674 | 0.2246235276338315 | ["routes","plugin","vite","commands"] |
| @types/path | 13 | 41 | 1 | 7 | 2 | 3.1538461538461533 | 2.192645048267573 | 22 | 1 | 5 | 1 | 1.6923076923076923 | 1.1821319289469756 | 0.15625 | 0.78125 | 0.15625 | 0.2644230769230769 | 0.18470811389796496 | ["utils","react-router-node","fileStorage","plugin"] |
| node:fs | 10 | 21 | 1 | 4 | 2 | 2.1 | 0.9944289260117533 | 14 | 1 | 3 | 1 | 1.4 | 0.8432740427115678 | 0.15625 | 0.46875 | 0.15625 | 0.21875 | 0.13176156917368248 | ["utils","react-router-node","fileStorage","plugin"] |
| picocolors | 9 | 10 | 1 | 2 | 1 | 1.1111111111111114 | 0.33333333333333337 | 13 | 1 | 3 | 1 | 1.4444444444444444 | 0.7264831572567788 | 0.15625 | 0.46875 | 0.15625 | 0.22569444444444445 | 0.11351299332137171 | ["utils","plugin","vite","commands"] |
| promises | 8 | 31 | 2 | 7 | 3.5 | 3.8750000000000004 | 2.100170061141308 | 16 | 1 | 4 | 1.5 | 2 | 1.3093073414159542 | 0.15625 | 0.625 | 0.234375 | 0.3125 | 0.20457927209624283 | ["utils","react-router-node","fileStorage","plugin"] |
| @types/module | 7 | 7 | 1 | 1 | 1 | 1 | 0 | 9 | 1 | 2 | 1 | 1.2857142857142856 | 0.4879500364742666 | 0.15625 | 0.3125 | 0.15625 | 0.20089285714285715 | 0.07624219319910415 | ["plugin","vite","commands","run"] |
| @types/babel__generator | 6 | 9 | 1 | 2 | 1.5 | 1.5 | 0.5477225575051661 | 8 | 1 | 3 | 1 | 1.3333333333333333 | 0.816496580927726 | 0.15625 | 0.46875 | 0.15625 | 0.20833333333333334 | 0.12757759076995717 | ["plugin","vite","generate","babel"] |
| @types/buffer | 6 | 11 | 1 | 3 | 2 | 1.8333333333333333 | 0.752772652709081 | 7 | 1 | 2 | 1 | 1.1666666666666665 | 0.408248290463863 | 0.15625 | 0.3125 | 0.15625 | 0.18229166666666666 | 0.06378879538497859 | ["server","react-router-node","stream","fileStorage"] |
| @types/react | 6 | 34 | 1 | 12 | 4.5 | 5.666666666666667 | 4.179314138308661 | 38 | 1 | 14 | 4 | 6.333333333333333 | 5.715476066494082 | 0.15625 | 2.1875 | 0.625 | 0.9895833333333334 | 0.8930431353897004 | ["context","react-router","server","utils"] |
| node:path | 6 | 6 | 1 | 1 | 1 | 1 | 0 | 11 | 1 | 3 | 1.5 | 1.8333333333333333 | 0.983192080250175 | 0.15625 | 0.46875 | 0.234375 | 0.2864583333333333 | 0.15362376253908985 | ["utils","profiler","prerender","normalizeSlashes"] |
| readline | 6 | 10 | 1 | 4 | 1 | 1.6666666666666665 | 1.2110601416389966 | 6 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["prompts-confirm","prompts-multi-select","prompts-prompt-base","prompts-select"] |
| sisteransi | 6 | 27 | 3 | 7 | 4 | 4.5 | 1.378404875209022 | 6 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["prompts-confirm","prompts-multi-select","prompts-prompt-base","prompts-select"] |
| @babel/lib | 5 | 49 | 2 | 17 | 8 | 9.8 | 6.496152707564686 | 7 | 1 | 3 | 1 | 1.4 | 0.8944271909999159 | 0.15625 | 0.46875 | 0.15625 | 0.21875 | 0.13975424859373686 | ["useJavascript","remove-exports","route-chunks","styles"] |
| fs | 5 | 17 | 2 | 5 | 3 | 3.4 | 1.51657508881031 | 8 | 1 | 2 | 2 | 1.6 | 0.5477225575051662 | 0.15625 | 0.3125 | 0.3125 | 0.25 | 0.0855816496101822 | ["utils","plugin","vite","config"] |
| http | 5 | 11 | 1 | 3 | 2 | 2.2 | 0.8366600265340756 | 9 | 1 | 2 | 2 | 1.8 | 0.4472135954999579 | 0.15625 | 0.3125 | 0.3125 | 0.28125 | 0.06987712429686842 | ["server","react-router-node","plugin","vite"] |
| @types/pick | 4 | 4 | 1 | 1 | 1 | 1 | 0 | 6 | 1 | 3 | 1 | 1.5 | 1 | 0.15625 | 0.46875 | 0.15625 | 0.234375 | 0.15625 | ["routes","plugin","vite","config"] |
| @cloudflare/workers-types | 3 | 44 | 4 | 22 | 18 | 14.666666666666666 | 9.451631252505218 | 10 | 1 | 5 | 4 | 3.3333333333333335 | 2.0816659994661326 | 0.15625 | 0.78125 | 0.625 | 0.5208333333333334 | 0.3252603124165832 | ["react-router-cloudflare","workersKVStorage","worker"] |
| @types/babel__core | 3 | 8 | 2 | 3 | 3 | 2.6666666666666665 | 0.5773502691896257 | 3 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["plugin","vite","useJavascript"] |
| @types/babel__traverse | 3 | 17 | 2 | 11 | 4 | 5.666666666666666 | 4.725815626252609 | 3 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["remove-exports","styles","with-props"] |
| lexer | 3 | 4 | 1 | 2 | 1 | 1.3333333333333333 | 0.5773502691896258 | 5 | 1 | 2 | 2 | 1.6666666666666667 | 0.5773502691896258 | 0.15625 | 0.3125 | 0.3125 | 0.2604166666666667 | 0.09021097956087903 | ["plugin","vite","virtual-route-modules"] |
| node:process | 3 | 3 | 1 | 1 | 1 | 1 | 0 | 7 | 1 | 4 | 2 | 2.3333333333333335 | 1.5275252316519465 | 0.15625 | 0.625 | 0.3125 | 0.36458333333333337 | 0.23867581744561667 | ["create-react-router","prompts-prompt-base","utils"] |
| node:url | 3 | 4 | 1 | 2 | 1 | 1.3333333333333333 | 0.5773502691896257 | 3 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["copy-template","plugin","vite"] |
| @architect/functions | 2 | 4 | 2 | 2 | 2 | 2 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["arcTableSessionStorage","react-router-architect"] |
| @architect/tables | 2 | 6 | 3 | 3 | 3 | 3 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["arcTableSessionStorage","react-router-architect"] |
| @babel/babel-parser | 2 | 3 | 1 | 2 | 1.5 | 1.5 | 0.7071067811865476 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["remove-exports","with-props"] |
| @mjackson/node-fetch-server | 2 | 4 | 2 | 2 | 2 | 2 | 0 | 4 | 2 | 2 | 2 | 2 | 0 | 0.3125 | 0.3125 | 0.3125 | 0.3125 | 0 | ["server","react-router-node"] |
| @types/api-gateway-proxy | 2 | 17 | 3 | 14 | 8.5 | 8.5 | 7.7781745930520225 | 7 | 2 | 5 | 3.5 | 3.5 | 2.1213203435596424 | 0.3125 | 0.78125 | 0.546875 | 0.546875 | 0.33145630368119416 | ["react-router-architect","server"] |
| @types/express | 2 | 18 | 3 | 15 | 9 | 9 | 8.48528137423857 | 6 | 2 | 4 | 3 | 3 | 1.4142135623730951 | 0.3125 | 0.625 | 0.46875 | 0.46875 | 0.2209708691207961 | ["server","react-router-express"] |
| @types/express-serve-static-core | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 5 | 2 | 3 | 2.5 | 2.5 | 0.7071067811865476 | 0.3125 | 0.46875 | 0.390625 | 0.390625 | 0.11048543456039805 | ["server","react-router-express"] |
| @types/handler | 2 | 4 | 2 | 2 | 2 | 2 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["react-router-architect","server"] |
| @types/jsesc | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["plugin","vite"] |
| @types/qs | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 5 | 2 | 3 | 2.5 | 2.5 | 0.7071067811865476 | 0.3125 | 0.46875 | 0.390625 | 0.390625 | 0.11048543456039805 | ["server","react-router-express"] |
| @types/stream | 2 | 10 | 5 | 5 | 5 | 5 | 0 | 6 | 3 | 3 | 3 | 3 | 0 | 0.46875 | 0.46875 | 0.46875 | 0.46875 | 0 | ["react-router-node","stream"] |
| async_hooks | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 8 | 4 | 4 | 4 | 4 | 0 | 0.625 | 0.625 | 0.625 | 0.625 | 0 | ["react-router","server"] |
| cli | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["cloudflare","cloudflare-dev-proxy"] |
| crypto | 2 | 4 | 2 | 2 | 2 | 2 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["plugin","vite"] |
| esm | 2 | 6 | 1 | 5 | 3 | 3 | 2.8284271247461903 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["config","flatRoutes"] |
| module-runner | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["plugin","vite"] |
| node:crypto | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["plugin","vite"] |
| rollup | 2 | 6 | 3 | 3 | 3 | 3 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["plugin","vite"] |
| url | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["plugin","vite"] |
| @types/APIGatewayProxyEventHeaders."content-type | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["server"] |
| @types/APIGatewayProxyEventHeaders."x-forwarded-host | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["server"] |
| @types/events | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["prompts-prompt-base"] |
| @types/isEqual | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["config"] |
| @types/kebabCase | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["plugin"] |
| @types/semver | 1 | 2 | 2 | 2 | 2 | 2 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["run"] |
| @types/timers | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["prompts-select"] |
| arg | 1 | 2 | 2 | 2 | 2 | 2 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["run"] |
| arg.Result."--no-typescript | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["run"] |
| exit-hook | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["commands"] |
| inspector | 1 | 3 | 3 | 3 | 3 | 3 | 0 | 3 | 3 | 3 | 3 | 3 | 0 | 0.46875 | 0.46875 | 0.46875 | 0.46875 | 0 | ["profiler"] |
| node:child_process | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["config"] |
| node:inspector | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["profiler"] |
| node:readline | 1 | 3 | 3 | 3 | 3 | 3 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["prompts-prompt-base"] |
| p-map | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["prerender"] |
| prettier | 1 | 2 | 2 | 2 | 2 | 2 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["useJavascript"] |
| server | 1 | 4 | 4 | 4 | 4 | 4 | 0 | 2 | 2 | 2 | 2 | 2 | 0 | 0.3125 | 0.3125 | 0.3125 | 0.3125 | 0 | ["vite-node"] |
| types | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15625 | 0.15625 | 0.15625 | 0.15625 | 0 | ["utils"] |

### 3.4 External Module Usage per Internal Module (Sorted)

Which internal TypeScript modules depend on the most external modules?

| internalModuleName | externalModuleName | numberOfExternalDeclarationCaller | numberOfExternalDeclarationCalls | numberOfAllElementsInInternalModule | numberOfAllExternalDeclarationsUsedInInternalModule | numberOfAllExternalModulesUsedInInternalModule | externalDeclarationRate | externalDeclarationNames |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| remove-exports | @babel/lib | 16 | 56 | 1 | 23 | 4 | 2300 | ["ExportSpecifier.local","ExportNamedDeclaration.specifiers","MemberExpression.object","ExportNamedDeclaration.declaration","ExportDefaultDeclaration.declaration","VariableDeclaration.declarations","LVal.type","ExportDeclaration.type","VariableDeclarator.id","ExportSpecifier.exported","AssignmentExpression.left","Identifier.name","ExpressionStatement.expression","FunctionDeclaration.id","Expression.type","ClassDeclaration.id"] |
| remove-exports | @types/babel__traverse | 4 | 24 | 1 | 23 | 4 | 2300 | ["NodePath.remove","NodePath.parentPath","NodePath.isProgram","NodePath.node"] |
| remove-exports | dist | 2 | 2 | 1 | 23 | 4 | 2300 | ["findReferencedIdentifiers","deadCodeElimination"] |
| remove-exports | @babel/babel-parser | 1 | 2 | 1 | 23 | 4 | 2300 | ["ParseResult"] |
| vite | node | 83 | 145 | 6 | 128 | 25 | 2133.3333333333335 | ["ModuleNode.file","ViteDevServer.pluginContainer","PreviewServer","ResolvedBuildOptions.assetsDir","ViteBuilder.environments","ResolvedConfig.build","createLogger","Connect.Server.use","RunnableDevEnvironment.runner","ResolvedConfig.root","ManifestChunk.assets","ResolvedConfig.mode","Connect.IncomingMessage.url","HotUpdatePluginContext.environment","EnvironmentOptions.resolve","PreviewServer.middlewares","UserConfig.build","ViteDevServer.ssrFixStacktrace","EnvironmentOptions.optimizeDeps","ResolvedConfig.server","ModuleNode.url","UserConfig.logLevel","ResolvedConfig.command","ConfigEnv.isSsrBuild","UserConfig.base","ViteDevServer.transformRequest","Logger.error","ViteDevServer.hot","normalizePath","Environment.name","DevEnvironment.name","HotBroadcaster.send","ViteDevServer.config","UserConfig.plugins","UserConfig.server","UserConfig.environments","Logger.warn","PluginContainer.buildStart","ConfigEnv.command","ResolvedConfig.logger","ManifestChunk.css","ManifestChunk.file","createServer","DevEnvironment.moduleGraph","UserConfig.root","loadConfigFromFile","ViteDevServer.environments","ResolvedConfig.configFile","Plugin.name","ResolvedServerOptions.middlewareMode","ViteDevServer.ssrLoadModule","Plugin","defaultClientConditions","ResolvedConfig","ViteBuilder.build","Logger.info","DevEnvironment.reloadModule","Environment.config","ViteDevServer.middlewares","isRunnableDevEnvironment","ConfigEnv.mode","EnvironmentOptions","ViteDevServer","PluginOption","ResolvedBuildEnvironmentOptions.outDir","transformWithEsbuild","ResolvedConfig.environments","ResolvedConfig.base","ResolvedEnvironmentOptions.build","ESBuildOptions","version","node"] |
| vite | @types/process | 7 | 15 | 6 | 128 | 25 | 2133.3333333333335 | ["global.NodeJS.Process.env","global.NodeJS.Process.cwd","global.NodeJS.ProcessEnv.IS_RR_BUILD_REQUEST","global.NodeJS.ProcessEnv.REACT_ROUTER_ROOT","global.NodeJS.Process.exit"] |
| vite | dist | 7 | 23 | 6 | 128 | 25 | 2133.3333333333335 | ["path.join","relative","path.extname","dist","join","path.normalize","resolve"] |
| vite | promises | 7 | 14 | 6 | 128 | 25 | 2133.3333333333335 | ["rename","mkdir","cp","readdir","readFile","rm"] |
| vite | @types/path | 6 | 25 | 6 | 128 | 25 | 2133.3333333333335 | ["path.PlatformPath.resolve","path.PlatformPath.dirname","path.PlatformPath.posix","path.PlatformPath.basename","path.PlatformPath.join","path.PlatformPath.relative"] |
| vite | fs | 5 | 10 | 6 | 128 | 25 | 2133.3333333333335 | ["Dirent.name","Dirent.isFile","Dirent.parentPath","Dirent.path","existsSync"] |
| vite | http | 5 | 8 | 6 | 128 | 25 | 2133.3333333333335 | ["ServerResponse.end","ServerResponse.setHeader","ServerResponse.statusCode"] |
| vite | @types/babel__core | 3 | 3 | 6 | 128 | 25 | 2133.3333333333335 | ["transformAsync","BabelFileResult.code","BabelFileResult.map"] |
| vite | node:fs | 3 | 8 | 6 | 128 | 25 | 2133.3333333333335 | ["readdirSync","existsSync","rmSync"] |
| vite | rollup | 3 | 5 | 6 | 128 | 25 | 2133.3333333333335 | ["PluginContext.resolve","PluginContext.environment","ResolvedId.id"] |
| vite | @types/babel__generator | 2 | 2 | 6 | 128 | 25 | 2133.3333333333335 | ["GeneratorResult.code","GeneratorResult"] |
| vite | crypto | 2 | 2 | 6 | 128 | 25 | 2133.3333333333335 | ["Hash.update","Hash.digest"] |
| vite | lexer | 2 | 2 | 6 | 128 | 25 | 2133.3333333333335 | ["init"] |
| vite | picocolors | 2 | 14 | 6 | 128 | 25 | 2133.3333333333335 | ["picocolors"] |
| vite | @types/buffer | 1 | 1 | 6 | 128 | 25 | 2133.3333333333335 | ["global.NonSharedBuffer.toString"] |
| vite | @types/jsesc | 1 | 2 | 6 | 128 | 25 | 2133.3333333333335 | ["jsesc"] |
| vite | @types/module | 1 | 2 | 6 | 128 | 25 | 2133.3333333333335 | ["global.NodeJS.Require.resolve"] |
| vite | @types/pick | 1 | 1 | 6 | 128 | 25 | 2133.3333333333335 | ["pick"] |
| vite | module-runner | 1 | 1 | 6 | 128 | 25 | 2133.3333333333335 | ["ModuleRunner.import"] |
| vite | node:crypto | 1 | 1 | 6 | 128 | 25 | 2133.3333333333335 | ["createHash"] |
| vite | node:url | 1 | 2 | 6 | 128 | 25 | 2133.3333333333335 | [".pathToFileURL"] |
| vite | url | 1 | 2 | 6 | 128 | 25 | 2133.3333333333335 | ["URL.href"] |
| with-props | @types/babel__traverse | 11 | 23 | 1 | 21 | 4 | 2100 | ["NodePath.isFunctionDeclaration","NodePath.node","NodePath.isExpression","NodePath.isExportNamedDeclaration","NodePath.scope","NodePath.isVariableDeclaration","NodePath.isIdentifier","Scope.generateUidIdentifier","NodePath.isExportDefaultDeclaration","NodePath.get","NodePath.replaceWith"] |
| with-props | @babel/lib | 8 | 11 | 1 | 21 | 4 | 2100 | ["callExpression","variableDeclaration","importSpecifier","identifier","importDeclaration","Program.body","stringLiteral","variableDeclarator"] |
| with-props | @babel/babel-parser | 2 | 3 | 1 | 21 | 4 | 2100 | ["ParseResult","ParseResult.program"] |
| cloudflare | node | 13 | 18 | 1 | 15 | 4 | 1500 | ["EnvironmentOptions.resolve","UserConfig.root","ViteDevServer.config","Plugin.name","Plugin","ViteDevServer.ssrLoadModule","Connect.Server.use","ResolvedServerOptions.middlewareMode","ResolvedConfig.server","ResolvedConfig.plugins","ViteDevServer.middlewares","ConfigEnv.mode","EnvironmentResolveOptions.externalConditions"] |
| cloudflare | @types/process | 1 | 1 | 1 | 15 | 4 | 1500 | ["global.NodeJS.Process.cwd"] |
| cloudflare | cli | 1 | 2 | 1 | 15 | 4 | 1500 | ["GetPlatformProxyOptions"] |
| cloudflare-dev-proxy | node | 13 | 18 | 1 | 15 | 4 | 1500 | ["EnvironmentOptions.resolve","UserConfig.root","ViteDevServer.config","Plugin.name","Plugin","ViteDevServer.ssrLoadModule","Connect.Server.use","ResolvedServerOptions.middlewareMode","ResolvedConfig.server","ResolvedConfig.plugins","ViteDevServer.middlewares","ConfigEnv.mode","EnvironmentResolveOptions.externalConditions"] |
| cloudflare-dev-proxy | @types/process | 1 | 1 | 1 | 15 | 4 | 1500 | ["global.NodeJS.Process.cwd"] |
| cloudflare-dev-proxy | cli | 1 | 2 | 1 | 15 | 4 | 1500 | ["GetPlatformProxyOptions"] |
| warn-on-client-source-maps | node | 11 | 12 | 1 | 12 | 2 | 1200 | ["ConfigEnv.command","ResolvedEnvironmentOptions.build","ResolvedBuildEnvironmentOptions.sourcemap","ResolvedConfig.mode","ResolvedConfig.environments","ResolvedConfig.build","Plugin","Logger.warn","ResolvedBuildOptions.sourcemap","ResolvedBuildOptions.ssr","ResolvedConfig.logger"] |
| warn-on-client-source-maps | picocolors | 1 | 2 | 1 | 12 | 2 | 1200 | ["picocolors"] |
| run | @types/process | 2 | 4 | 1 | 8 | 5 | 800 | ["global.NodeJS.ProcessVersions.node","global.NodeJS.Process.versions"] |
| run | @types/semver | 2 | 2 | 1 | 8 | 5 | 800 | ["major","semver"] |
| run | arg | 2 | 3 | 1 | 8 | 5 | 800 | ["arg","arg.Result._"] |
| run | @types/module | 1 | 1 | 1 | 8 | 5 | 800 | ["global.NodeJS.Require.main"] |
| run | arg.Result."--no-typescript | 1 | 1 | 1 | 8 | 5 | 800 | ["arg.Result.\"--no-typescript\""] |
| plugin | node | 95 | 162 | 18 | 134 | 26 | 744.4444444444445 | ["ModuleNode.file","ViteDevServer.pluginContainer","PreviewServer","ResolvedBuildOptions.assetsDir","ViteBuilder.environments","ResolvedConfig.build","createLogger","Connect.Server.use","RunnableDevEnvironment.runner","ResolvedConfig.root","ManifestChunk.assets","ResolvedConfig.mode","Connect.IncomingMessage.url","HotUpdatePluginContext.environment","EnvironmentOptions.resolve","PreviewServer.middlewares","UserConfig.build","ViteDevServer.ssrFixStacktrace","EnvironmentOptions.optimizeDeps","ResolvedConfig.server","ModuleNode.url","UserConfig.logLevel","ResolvedConfig.command","ConfigEnv.isSsrBuild","UserConfig.base","ViteDevServer.transformRequest","Logger.error","ViteDevServer.hot","normalizePath","Environment.name","DevEnvironment.name","HotBroadcaster.send","ViteDevServer.config","UserConfig.plugins","UserConfig.server","UserConfig.environments","Logger.warn","PluginContainer.buildStart","ConfigEnv.command","ResolvedConfig.logger","ManifestChunk.css","ManifestChunk.file","createServer","DevEnvironment.moduleGraph","UserConfig.root","loadConfigFromFile","ViteDevServer.environments","ResolvedConfig.configFile","Plugin.name","ResolvedServerOptions.middlewareMode","ViteDevServer.ssrLoadModule","Plugin","defaultClientConditions","ResolvedConfig","ViteBuilder.build","Logger.info","DevEnvironment.reloadModule","Environment.config","ViteDevServer.middlewares","isRunnableDevEnvironment","ConfigEnv.mode","EnvironmentOptions","ViteDevServer","ResolvedBuildOptions.emptyOutDir","defaultServerConditions","UserConfig","resolveConfig","ResolvedBuildOptions.manifest","ModuleNode","PluginOption","ResolvedBuildEnvironmentOptions.outDir","transformWithEsbuild","ResolvedConfig.environments","ResolvedConfig.base","ResolvedEnvironmentOptions.build"] |
| plugin | @types/path | 17 | 41 | 18 | 134 | 26 | 744.4444444444445 | ["path.PlatformPath.join","path.PlatformPath.dirname","path.PlatformPath.resolve","path.PlatformPath.posix","path.PlatformPath.basename","path.PlatformPath.relative","path.PlatformPath.isAbsolute"] |
| plugin | promises | 10 | 18 | 18 | 134 | 26 | 744.4444444444445 | ["rm","readdir","rename","mkdir","cp","readFile"] |
| plugin | @types/process | 7 | 15 | 18 | 134 | 26 | 744.4444444444445 | ["global.NodeJS.Process.env","global.NodeJS.Process.cwd","global.NodeJS.ProcessEnv.IS_RR_BUILD_REQUEST","global.NodeJS.ProcessEnv.REACT_ROUTER_ROOT","global.NodeJS.Process.exit"] |
| plugin | dist | 7 | 23 | 18 | 134 | 26 | 744.4444444444445 | ["path.join","relative","path.extname","dist","join","path.normalize","resolve"] |
| plugin | fs | 5 | 10 | 18 | 134 | 26 | 744.4444444444445 | ["Dirent.name","Dirent.isFile","Dirent.parentPath","Dirent.path","existsSync"] |
| plugin | http | 5 | 8 | 18 | 134 | 26 | 744.4444444444445 | ["ServerResponse.end","ServerResponse.setHeader","ServerResponse.statusCode"] |
| plugin | node:fs | 5 | 10 | 18 | 134 | 26 | 744.4444444444445 | ["existsSync","readdirSync","rmSync","readFileSync"] |
| plugin | @types/babel__core | 3 | 3 | 18 | 134 | 26 | 744.4444444444445 | ["transformAsync","BabelFileResult.code","BabelFileResult.map"] |
| plugin | picocolors | 3 | 15 | 18 | 134 | 26 | 744.4444444444445 | ["picocolors"] |
| plugin | rollup | 3 | 5 | 18 | 134 | 26 | 744.4444444444445 | ["PluginContext.resolve","PluginContext.environment","ResolvedId.id"] |
| plugin | @types/babel__generator | 2 | 2 | 18 | 134 | 26 | 744.4444444444445 | ["GeneratorResult.code","GeneratorResult"] |
| plugin | @types/module | 2 | 3 | 18 | 134 | 26 | 744.4444444444445 | ["global.NodeJS.Require.resolve"] |
| plugin | crypto | 2 | 2 | 18 | 134 | 26 | 744.4444444444445 | ["Hash.update","Hash.digest"] |
| plugin | lexer | 2 | 2 | 18 | 134 | 26 | 744.4444444444445 | ["init"] |
| plugin | @types/buffer | 1 | 1 | 18 | 134 | 26 | 744.4444444444445 | ["global.NonSharedBuffer.toString"] |
| plugin | @types/jsesc | 1 | 2 | 18 | 134 | 26 | 744.4444444444445 | ["jsesc"] |
| plugin | @types/kebabCase | 1 | 1 | 18 | 134 | 26 | 744.4444444444445 | ["kebabCase"] |
| plugin | @types/pick | 1 | 1 | 18 | 134 | 26 | 744.4444444444445 | ["pick"] |
| plugin | module-runner | 1 | 1 | 18 | 134 | 26 | 744.4444444444445 | ["ModuleRunner.import"] |
| plugin | node:crypto | 1 | 1 | 18 | 134 | 26 | 744.4444444444445 | ["createHash"] |
| plugin | node:url | 1 | 2 | 18 | 134 | 26 | 744.4444444444445 | [".pathToFileURL"] |
| plugin | url | 1 | 2 | 18 | 134 | 26 | 744.4444444444445 | ["URL.href"] |
| prompts-prompt-base | @types/process | 4 | 52 | 2 | 14 | 6 | 700 | ["global.NodeJS.Process.stdout","global.NodeJS.Process.stdin","global.NodeJS.ReadStream","global.NodeJS.WriteStream"] |
| prompts-prompt-base | node:readline | 3 | 52 | 2 | 14 | 6 | 700 | [".createInterface","node:readline",".emitKeypressEvents"] |
| prompts-prompt-base | sisteransi | 3 | 39 | 2 | 14 | 6 | 700 | ["cursor","cursor.show","beep"] |
| prompts-prompt-base | node:process | 2 | 78 | 2 | 14 | 6 | 700 | ["node:process"] |
| prompts-prompt-base | readline | 2 | 26 | 2 | 14 | 6 | 700 | ["Interface.close","Key"] |
| prompts-prompt-base | @types/events | 1 | 1 | 2 | 14 | 6 | 700 | ["EventEmitter"] |
| vite-node | node | 8 | 9 | 2 | 13 | 4 | 650 | ["ViteDevServer","ResolvedConfig.base","ResolvedConfig.root","Logger","ViteDevServer.pluginContainer","createServer","ViteDevServer.config","PluginContainer.buildStart"] |
| vite-node | server | 4 | 4 | 2 | 13 | 4 | 650 | ["ViteNodeServer","ViteNodeServer.resolveId","ViteNodeServer.fetchModule","ViteNodeServer.getSourceMap"] |
| vite-node | dist | 1 | 1 | 2 | 13 | 4 | 650 | ["ViteNodeRunner"] |
| useJavascript | @babel/lib | 2 | 2 | 1 | 6 | 5 | 600 | ["lib"] |
| useJavascript | @types/babel__core | 2 | 3 | 1 | 6 | 5 | 600 | ["BabelFileResult.code","transformSync"] |
| useJavascript | prettier | 2 | 2 | 1 | 6 | 5 | 600 | ["prettier","format"] |
| arcTableSessionStorage | @architect/tables | 3 | 5 | 1 | 5 | 2 | 500 | ["ArcTable.put","ArcTable.delete","ArcTable.get"] |
| arcTableSessionStorage | @architect/functions | 2 | 2 | 1 | 5 | 2 | 500 | ["tables","functions"] |
| is-react-router-repo | dist | 4 | 6 | 1 | 5 | 2 | 500 | ["path.resolve","dist","path.basename","path.dirname"] |
| is-react-router-repo | @types/module | 1 | 1 | 1 | 5 | 2 | 500 | ["global.NodeJS.Require.resolve"] |
| react-router-fs-routes | @types/path | 2 | 2 | 1 | 5 | 3 | 500 | ["path.PlatformPath.relative","path.PlatformPath.resolve"] |
| react-router-fs-routes | node:fs | 2 | 2 | 1 | 5 | 3 | 500 | ["node:fs",".existsSync"] |
| react-router-fs-routes | node:path | 1 | 2 | 1 | 5 | 3 | 500 | ["node:path"] |
| resolve-file-url | @types/path | 4 | 6 | 1 | 5 | 2 | 500 | ["path.PlatformPath.isAbsolute","path.PlatformPath.join","path.PlatformPath.relative","path.PlatformPath.posix"] |
| resolve-file-url | node | 1 | 3 | 1 | 5 | 2 | 500 | ["normalizePath"] |
| fileStorage | promises | 4 | 7 | 2 | 9 | 5 | 450 | [".unlink",".writeFile",".mkdir",".readFile"] |
| fileStorage | @types/buffer | 2 | 2 | 2 | 9 | 5 | 450 | ["global.Buffer.toString","global.BufferConstructor.from"] |
| fileStorage | @types/path | 2 | 3 | 2 | 9 | 5 | 450 | ["path.PlatformPath.join","path.PlatformPath.dirname"] |
| fileStorage | node:fs | 1 | 7 | 2 | 9 | 5 | 450 | ["promises"] |
| load-dotenv | node | 3 | 3 | 1 | 4 | 2 | 400 | ["UserConfig","UserConfig.envDir","loadEnv"] |
| load-dotenv | @types/process | 1 | 1 | 1 | 4 | 2 | 400 | ["global.NodeJS.Process.env"] |
| prompts-text | sisteransi | 7 | 91 | 2 | 8 | 2 | 400 | ["cursor.restore","cursor.down","erase.line","cursor.move","erase","cursor.save","cursor.to"] |
| prompts-text | readline | 1 | 13 | 2 | 8 | 2 | 400 | ["Key"] |
| workersKVStorage | @cloudflare/workers-types | 4 | 6 | 1 | 4 | 1 | 400 | ["KVNamespace.get","Crypto.getRandomValues","KVNamespace.delete","KVNamespace.put"] |
| react-router-cloudflare | @cloudflare/workers-types | 26 | 34 | 6 | 22 | 2 | 366.6666666666667 | ["KVNamespace.get","Crypto.getRandomValues","KVNamespace.delete","KVNamespace.put","CacheStorage","IncomingRequestCfProperties","CfProperties","Request","EventContext","Response","EventContext.request","Request.headers","Response.body","Request.clone","Response.status","Console.error","Headers.delete","Request.url","EventContext.env","EventContext.passThroughOnException","EventContext.waitUntil","Request.cf"] |
| worker | @cloudflare/workers-types | 22 | 28 | 5 | 18 | 2 | 360 | ["Response","EventContext","EventContext.passThroughOnException","EventContext.waitUntil","EventContext.request","Request.cf","Request.headers","Response.body","Request.clone","Response.status","Console.error","Headers.delete","Request.url","EventContext.env","CacheStorage","IncomingRequestCfProperties","CfProperties","Request"] |
| has-rsc-plugin | node | 3 | 3 | 1 | 3 | 2 | 300 | ["ResolvedConfig.plugins","Plugin.name","resolveConfig"] |
| optimize-deps-entries | node | 2 | 2 | 1 | 3 | 2 | 300 | ["version","normalizePath"] |
| optimize-deps-entries | dist | 1 | 1 | 1 | 3 | 2 | 300 | ["escapePath"] |
| profiler | inspector | 4 | 6 | 3 | 9 | 6 | 300 | ["Session.post","Session.connect","Session"] |
| profiler | node:fs | 2 | 2 | 3 | 9 | 6 | 300 | ["node:fs",".writeFileSync"] |
| profiler | @types/path | 1 | 1 | 3 | 9 | 6 | 300 | ["path.PlatformPath.resolve"] |
| profiler | node:inspector | 1 | 1 | 3 | 9 | 6 | 300 | [".Session"] |
| profiler | node:path | 1 | 1 | 3 | 9 | 6 | 300 | ["node:path"] |
| profiler | picocolors | 1 | 3 | 3 | 9 | 6 | 300 | ["picocolors"] |
| resolve-relative-route-file-path | dist | 2 | 2 | 1 | 3 | 2 | 300 | ["path.resolve","dist"] |
| resolve-relative-route-file-path | node | 1 | 1 | 1 | 3 | 2 | 300 | ["normalizePath"] |
| styles | @babel/lib | 6 | 8 | 4 | 12 | 5 | 300 | ["VariableDeclarator.init","VariableDeclarator.id","Identifier.name","VariableDeclaration.declarations","StringLiteral.value","LVal.type"] |
| styles | @types/babel__traverse | 2 | 2 | 4 | 12 | 5 | 300 | ["NodePath.node","NodePath.stop"] |
| styles | @types/path | 2 | 3 | 4 | 12 | 5 | 300 | ["path.PlatformPath.relative","path.PlatformPath.resolve"] |
| styles | @types/process | 1 | 1 | 4 | 12 | 5 | 300 | ["global.NodeJS.Process.cwd"] |
| styles | node | 1 | 2 | 4 | 12 | 5 | 300 | ["ViteDevServer"] |
| validate-plugin-order | node | 3 | 3 | 1 | 3 | 1 | 300 | ["Plugin.name","Plugin","ResolvedConfig.plugins"] |
| dev | node | 9 | 14 | 5 | 14 | 5 | 280 | ["ViteDevServer.printUrls","ViteDevServer.listen","Plugin.name","ViteDevServer.config","createServer","ViteDevServer.bindCLIShortcuts","ResolvedConfig.plugins","ResolvedConfig.logger","Logger.info"] |
| dev | @types/process | 4 | 5 | 5 | 14 | 5 | 280 | ["global.NodeJS.Process.exit","global.NodeJS.Process.env","global.NodeJS.ProcessEnv.IS_RR_BUILD_REQUEST","global.NodeJS.ProcessEnv.hasOwnProperty"] |
| dev | picocolors | 1 | 1 | 5 | 14 | 5 | 280 | ["picocolors"] |
| node-adapter | node | 4 | 6 | 2 | 5 | 2 | 250 | ["Connect.IncomingMessage.originalUrl","Connect.IncomingMessage.url","Connect.IncomingMessage"] |
| node-adapter | http | 3 | 3 | 2 | 5 | 2 | 250 | ["ServerResponse","IncomingMessage"] |
| prompts-multi-select | sisteransi | 4 | 52 | 2 | 5 | 2 | 250 | ["erase","cursor.to","cursor.hide","erase.line"] |
| prompts-multi-select | readline | 1 | 13 | 2 | 5 | 2 | 250 | ["Key"] |
| react-router-architect | @types/api-gateway-proxy | 5 | 5 | 4 | 10 | 4 | 250 | ["APIGatewayEventRequestContextV2","APIGatewayProxyEventV2","APIGatewayProxyResultV2"] |
| react-router-architect | @architect/tables | 3 | 5 | 4 | 10 | 4 | 250 | ["ArcTable.put","ArcTable.delete","ArcTable.get"] |
| react-router-architect | @architect/functions | 2 | 2 | 4 | 10 | 4 | 250 | ["tables","functions"] |
| react-router-architect | @types/handler | 2 | 2 | 4 | 10 | 4 | 250 | ["Context","Callback"] |
| react-router-node | @types/stream | 9 | 10 | 7 | 17 | 8 | 242.85714285714286 | ["Stream.Writable","Stream.Writable.write","Stream.Writable.destroy","Stream.Writable.end","Stream.Readable"] |
| react-router-node | @types/buffer | 4 | 4 | 7 | 17 | 8 | 242.85714285714286 | ["global.BufferConstructor.concat","global.Buffer.toString","global.BufferConstructor.from"] |
| react-router-node | promises | 4 | 7 | 7 | 17 | 8 | 242.85714285714286 | [".unlink",".writeFile",".mkdir",".readFile"] |
| react-router-node | @mjackson/node-fetch-server | 2 | 9 | 7 | 17 | 8 | 242.85714285714286 | ["createRequestListener","ClientAddress"] |
| react-router-node | @types/path | 1 | 2 | 7 | 17 | 8 | 242.85714285714286 | ["path.PlatformPath.dirname"] |
| react-router-node | http | 1 | 1 | 7 | 17 | 8 | 242.85714285714286 | ["RequestListener"] |
| react-router-node | node:fs | 1 | 7 | 7 | 17 | 8 | 242.85714285714286 | ["promises"] |
| commands | @types/path | 3 | 9 | 5 | 12 | 9 | 240 | ["path.PlatformPath.dirname","path.PlatformPath.resolve","path.PlatformPath.relative"] |
| commands | picocolors | 2 | 6 | 5 | 12 | 9 | 240 | ["picocolors"] |
| commands | promises | 2 | 3 | 5 | 12 | 9 | 240 | ["writeFile","copyFile"] |
| commands | @types/module | 1 | 1 | 5 | 12 | 9 | 240 | ["global.NodeJS.Require.resolve"] |
| commands | @types/process | 1 | 1 | 5 | 12 | 9 | 240 | ["global.NodeJS.Process.exit"] |
| commands | dist | 1 | 1 | 5 | 12 | 9 | 240 | ["PackageJson.dependencies"] |
| commands | exit-hook | 1 | 1 | 5 | 12 | 9 | 240 | ["exit-hook"] |
| commands | node | 1 | 1 | 5 | 12 | 9 | 240 | ["createLogger"] |
| commands | node:fs | 1 | 1 | 5 | 12 | 9 | 240 | ["existsSync"] |
| config | dist | 15 | 43 | 14 | 31 | 15 | 221.42857142857144 | ["path.dirname","PackageJson.dependencies","path.resolve","dist","path.join","path.normalize","ViteNodeRunner.moduleCache","path.relative","ModuleCacheMap.clear"] |
| config | esm | 5 | 6 | 14 | 31 | 15 | 221.42857142857144 | ["FSWatcher.unwatch","_default.watch","esm","FSWatcher.on","FSWatcher.add"] |
| config | node | 5 | 8 | 14 | 31 | 15 | 221.42857142857144 | ["ModuleGraph.invalidateAll","ModuleGraph.getModuleById","createLogger","ViteDevServer.close","ViteDevServer.moduleGraph"] |
| config | @types/process | 3 | 3 | 14 | 31 | 15 | 221.42857142857144 | ["global.NodeJS.ProcessEnv.REACT_ROUTER_ROOT","global.NodeJS.Process.cwd","global.NodeJS.Process.env"] |
| config | @types/module | 2 | 2 | 14 | 31 | 15 | 221.42857142857144 | ["global.NodeJS.Require.resolve"] |
| config | fs | 2 | 2 | 14 | 31 | 15 | 221.42857142857144 | ["Stats.isFile","Stats.isDirectory"] |
| config | node:fs | 2 | 2 | 14 | 31 | 15 | 221.42857142857144 | ["node:fs",".statSync"] |
| config | @types/isEqual | 1 | 2 | 14 | 31 | 15 | 221.42857142857144 | ["isEqual"] |
| config | @types/pick | 1 | 1 | 14 | 31 | 15 | 221.42857142857144 | ["pick"] |
| config | node:child_process | 1 | 1 | 14 | 31 | 15 | 221.42857142857144 | ["execSync"] |
| config | picocolors | 1 | 1 | 14 | 31 | 15 | 221.42857142857144 | ["picocolors"] |
| loading-indicator | @types/process | 2 | 2 | 1 | 2 | 1 | 200 | ["global.NodeJS.ReadStream","global.NodeJS.WriteStream"] |
| prerender | @types/path | 3 | 3 | 6 | 12 | 6 | 200 | ["path.PlatformPath.dirname","path.PlatformPath.relative","path.PlatformPath.join"] |
| prerender | node | 3 | 3 | 6 | 12 | 6 | 200 | ["ResolvedConfig.root","Plugin","PreviewServer.close"] |
| prerender | @types/process | 2 | 6 | 6 | 12 | 6 | 200 | ["global.NodeJS.Process.env","global.NodeJS.ProcessEnv.IS_RR_BUILD_REQUEST"] |
| prerender | promises | 2 | 2 | 6 | 12 | 6 | 200 | ["mkdir","writeFile"] |
| prerender | node:path | 1 | 3 | 6 | 12 | 6 | 200 | ["node:path"] |
| prerender | p-map | 1 | 1 | 6 | 12 | 6 | 200 | ["p-map"] |
| prompts-select | sisteransi | 4 | 52 | 3 | 6 | 3 | 200 | ["cursor.to","erase.line","erase","cursor.hide"] |
| prompts-select | @types/timers | 1 | 13 | 3 | 6 | 3 | 200 | ["global.NodeJS.Timeout"] |
| prompts-select | readline | 1 | 13 | 3 | 6 | 3 | 200 | ["Key"] |
| virtual-route-config | dist | 2 | 2 | 1 | 2 | 1 | 200 | ["dist","path.resolve"] |
| stream | @types/stream | 9 | 10 | 4 | 7 | 3 | 175 | ["Stream.Readable","Stream.Writable","Stream.Writable.write","Stream.Writable.destroy","Stream.Writable.end"] |
| stream | @types/buffer | 2 | 2 | 4 | 7 | 3 | 175 | ["global.BufferConstructor.concat","global.Buffer.toString"] |
| prompts-confirm | sisteransi | 4 | 52 | 3 | 5 | 2 | 166.66666666666669 | ["erase","cursor.hide","cursor.to","erase.line"] |
| prompts-confirm | readline | 1 | 13 | 3 | 5 | 2 | 166.66666666666669 | ["Key"] |
| react-router-express | @types/express | 5 | 5 | 3 | 5 | 3 | 166.66666666666669 | ["e.Response","e.NextFunction","e.Request"] |
| react-router-express | @types/express-serve-static-core | 2 | 2 | 3 | 5 | 3 | 166.66666666666669 | ["ParamsDictionary"] |
| react-router-express | @types/qs | 2 | 2 | 3 | 5 | 3 | 166.66666666666669 | ["QueryString.ParsedQs"] |
| typegen | promises | 4 | 4 | 3 | 5 | 3 | 166.66666666666669 | ["promises",".rm"] |
| typegen | picocolors | 2 | 4 | 3 | 5 | 3 | 166.66666666666669 | ["red","green"] |
| typegen | node | 1 | 2 | 3 | 5 | 3 | 166.66666666666669 | ["node"] |
| create-react-router | @types/process | 2 | 26 | 2 | 3 | 2 | 150 | ["global.NodeJS.WriteStream","global.NodeJS.ReadStream"] |
| create-react-router | node:process | 1 | 52 | 2 | 3 | 2 | 150 | ["node:process"] |
| normalizeSlashes | @types/path | 4 | 4 | 2 | 3 | 2 | 150 | ["path.PlatformPath.win32","path.PlatformPath.sep"] |
| normalizeSlashes | node:path | 2 | 2 | 2 | 3 | 2 | 150 | ["node:path"] |
| routes | dist | 30 | 96 | 18 | 27 | 4 | 150 | ["resolve","BaseIssue","BaseSchema","array","ArraySchema","safeParse","flatten","LazySchema","CustomSchema","StringSchema","OptionalSchema","SchemaWithPipe","pipe","BooleanSchema","boolean","notValue","string","NotValueAction","custom","lazy","optional","CustomIssue","ObjectSchema","object","isAbsolute","relative"] |
| routes | @types/pick | 3 | 3 | 18 | 27 | 4 | 150 | ["pick"] |
| route-chunks | @babel/lib | 33 | 66 | 13 | 19 | 3 | 146.15384615384616 | ["File.program","ExportNamedDeclaration.specifiers","isVariableDeclaration","isNodesEquivalent","Identifier.name","ExportNamedDeclaration.declaration","ImportDeclaration.specifiers","isExportAllDeclaration","isExportNamedDeclaration","isFunctionDeclaration","isClassDeclaration","isImportDeclaration","isExportDeclaration","VariableDeclaration.declarations","isExportDefaultDeclaration","Program.body","File"] |
| route-chunks | @types/babel__generator | 5 | 5 | 13 | 19 | 3 | 146.15384615384616 | ["GeneratorOptions","GeneratorResult"] |
| server | @types/express | 20 | 24 | 41 | 50 | 14 | 121.95121951219512 | ["e.Response.end","e.Response","e.Response.flushHeaders","e.Response.statusMessage","e.Response.append","e.Response.status","e.Request","e.NextFunction","e.Request.protocol","e.Response.on","e.Request.headers","e.Request.originalUrl","e.Request.hostname","e.Request.method","e.Request.get"] |
| server | @types/api-gateway-proxy | 18 | 25 | 41 | 50 | 14 | 121.95121951219512 | ["APIGatewayEventRequestContextV2","APIGatewayProxyEventV2","APIGatewayProxyResultV2","APIGatewayProxyEventHeaders","APIGatewayProxyStructuredResultV2","APIGatewayProxyEventHeaders.host","APIGatewayProxyEventV2.isBase64Encoded","APIGatewayProxyEventV2.rawPath","APIGatewayProxyEventV2.rawQueryString","APIGatewayProxyEventV2.body","APIGatewayProxyEventV2.requestContext","APIGatewayProxyEventV2.headers","APIGatewayEventRequestContextV2.http","APIGatewayProxyEventV2.cookies"] |
| server | @types/react | 6 | 22 | 41 | 50 | 14 | 121.95121951219512 | ["React.ReactElement","React.ReactNode","React.Fragment","React.createElement","React.FunctionComponent","React.ComponentClass"] |
| server | async_hooks | 4 | 4 | 41 | 50 | 14 | 121.95121951219512 | ["AsyncLocalStorage.getStore"] |
| server | @types/express-serve-static-core | 3 | 3 | 41 | 50 | 14 | 121.95121951219512 | ["ParamsDictionary"] |
| server | @types/qs | 3 | 3 | 41 | 50 | 14 | 121.95121951219512 | ["QueryString.ParsedQs"] |
| server | @mjackson/node-fetch-server | 2 | 9 | 41 | 50 | 14 | 121.95121951219512 | ["createRequestListener","ClientAddress"] |
| server | @types/buffer | 2 | 3 | 41 | 50 | 14 | 121.95121951219512 | ["global.BufferConstructor.from","global.Buffer.toString"] |
| server | @types/handler | 2 | 2 | 41 | 50 | 14 | 121.95121951219512 | ["Context","Callback"] |
| server | @types/process | 2 | 2 | 41 | 50 | 14 | 121.95121951219512 | ["global.NodeJS.Process.env","global.NodeJS.ProcessEnv.ARC_SANDBOX"] |
| server | http | 2 | 2 | 41 | 50 | 14 | 121.95121951219512 | ["IncomingHttpHeaders","RequestListener"] |
| server | @types/APIGatewayProxyEventHeaders."content-type | 1 | 1 | 41 | 50 | 14 | 121.95121951219512 | ["APIGatewayProxyEventHeaders.\"content-type\""] |
| server | @types/APIGatewayProxyEventHeaders."x-forwarded-host | 1 | 1 | 41 | 50 | 14 | 121.95121951219512 | ["APIGatewayProxyEventHeaders.\"x-forwarded-host\""] |
| flatRoutes | @types/path | 8 | 18 | 13 | 15 | 5 | 115.38461538461539 | ["path.PlatformPath.win32","path.PlatformPath.sep","path.PlatformPath.join","path.PlatformPath.dirname","path.PlatformPath.relative","path.PlatformPath.extname","path.PlatformPath.posix"] |
| flatRoutes | fs | 3 | 3 | 13 | 15 | 5 | 115.38461538461539 | ["Dirent.isFile","Dirent.isDirectory","Dirent.name"] |
| flatRoutes | node:fs | 3 | 4 | 13 | 15 | 5 | 115.38461538461539 | [".readdirSync",".existsSync","node:fs"] |
| flatRoutes | node:path | 3 | 13 | 13 | 15 | 5 | 115.38461538461539 | ["node:path"] |
| flatRoutes | esm | 1 | 1 | 13 | 15 | 5 | 115.38461538461539 | ["makeRe"] |
| cookies | dist | 7 | 19 | 6 | 6 | 2 | 100 | ["Cookies.name","serialize","parse","ParseOptions","SerializeOptions","StringifyOptions"] |
| copy-template | node:url | 2 | 2 | 2 | 2 | 1 | 100 | [".fileURLToPath","node:url"] |
| detectPackageManager | @types/process | 1 | 1 | 1 | 1 | 1 | 100 | ["global.NodeJS.Process.env"] |
| has-dependency | @types/module | 1 | 1 | 1 | 1 | 1 | 100 | ["global.NodeJS.Require.resolve"] |
| virtual-route-modules | lexer | 2 | 2 | 3 | 3 | 2 | 100 | ["init","parse"] |
| virtual-route-modules | @types/babel__generator | 1 | 1 | 3 | 3 | 2 | 100 | ["GeneratorResult.code"] |
| babel | @types/babel__generator | 1 | 1 | 2 | 1 | 1 | 50 | ["generate"] |
| sessions | dist | 6 | 32 | 11 | 5 | 1 | 45.45454545454546 | ["SerializeOptions.maxAge","SerializeOptions.expires","ParseOptions","SerializeOptions","StringifyOptions"] |
| context | @types/react | 27 | 51 | 21 | 9 | 1 | 42.857142857142854 | ["React.createContext","React.Context","React.ProviderProps","React.FunctionComponentElement","React.createElement","React.Context.Provider","React.ReactElement","React.ReactNode","React.useContext"] |
| generate | dist | 4 | 4 | 5 | 2 | 2 | 40 | ["join"] |
| generate | @types/babel__generator | 1 | 3 | 5 | 2 | 2 | 40 | ["GeneratorResult.code"] |
| utils | @types/process | 7 | 9 | 149 | 29 | 12 | 19.46308724832215 | ["global.NodeJS.WriteStream","global.NodeJS.Process.stdout","global.NodeJS.ProcessEnv.TERM","global.NodeJS.Process.env","global.NodeJS.Process.stderr"] |
| utils | @types/react | 6 | 27 | 149 | 29 | 12 | 19.46308724832215 | ["React.ReactNode","React.ComponentClass","React.FunctionComponent"] |
| utils | node:fs | 6 | 6 | 149 | 29 | 12 | 19.46308724832215 | ["node:fs",".promises"] |
| utils | sisteransi | 5 | 6 | 149 | 29 | 12 | 19.46308724832215 | ["cursor","erase","erase.line","cursor.to","erase.lines"] |
| utils | node:process | 4 | 8 | 149 | 29 | 12 | 19.46308724832215 | ["node:process"] |
| utils | promises | 4 | 4 | 149 | 29 | 12 | 19.46308724832215 | [".stat",".mkdir","readdir"] |
| utils | readline | 4 | 26 | 149 | 29 | 12 | 19.46308724832215 | ["Key.meta","Key.ctrl","Key","Key.name"] |
| utils | node:path | 3 | 7 | 149 | 29 | 12 | 19.46308724832215 | ["node:path"] |
| utils | @types/path | 2 | 5 | 149 | 29 | 12 | 19.46308724832215 | ["path.PlatformPath.sep"] |
| utils | fs | 2 | 2 | 149 | 29 | 12 | 19.46308724832215 | ["Stats.isFile","Stats.isDirectory"] |
| utils | picocolors | 1 | 39 | 149 | 29 | 12 | 19.46308724832215 | ["picocolors"] |
| utils | types | 1 | 2 | 149 | 29 | 12 | 19.46308724832215 | ["Formatter"] |
| build | node | 1 | 1 | 7 | 1 | 1 | 14.285714285714286 | ["version"] |
| fog-of-war | @types/react | 1 | 1 | 7 | 1 | 1 | 14.285714285714286 | ["React.useEffect"] |
| routeModules | @types/react | 12 | 86 | 21 | 3 | 1 | 14.285714285714285 | ["React.FunctionComponent","React.ComponentClass","React.ReactElement"] |
| react-router | @types/react | 31 | 79 | 179 | 19 | 4 | 10.614525139664805 | ["React.ProviderProps","React.FunctionComponentElement","React.createElement","React.Context.Provider","React.FunctionComponent","React.ComponentClass","React.ReactElement","React.ReactNode","React.Fragment","React.createContext","React.Context","React.useEffect"] |
| react-router | dist | 7 | 19 | 179 | 19 | 4 | 10.614525139664805 | ["Cookies.name","serialize","parse","StringifyOptions","ParseOptions","SerializeOptions"] |
| react-router | async_hooks | 4 | 4 | 179 | 19 | 4 | 10.614525139664805 | ["AsyncLocalStorage.getStore"] |

### 3.5 TypeScript Charts


![Typescript_Top_external_modules_by_elements_above_threshold](./Typescript_Top_external_modules_by_elements_above_threshold.svg)

![Typescript_Top_external_modules_by_elements_others_drilldown](./Typescript_Top_external_modules_by_elements_others_drilldown.svg)

![Typescript_Top_external_modules_by_modules_above_threshold](./Typescript_Top_external_modules_by_modules_above_threshold.svg)

![Typescript_Top_external_namespaces_by_elements_above_threshold](./Typescript_Top_external_namespaces_by_elements_above_threshold.svg)

![Typescript_Top_external_namespaces_by_modules_above_threshold](./Typescript_Top_external_namespaces_by_modules_above_threshold.svg)

![Typescript_Most_spread_modules_by_declarations_above_threshold](./Typescript_Most_spread_modules_by_declarations_above_threshold.svg)

![Typescript_Most_spread_modules_by_modules_above_threshold](./Typescript_Most_spread_modules_by_modules_above_threshold.svg)

![Typescript_Most_spread_namespaces_by_declarations_above_threshold](./Typescript_Most_spread_namespaces_by_declarations_above_threshold.svg)

![Typescript_Most_spread_namespaces_by_modules_above_threshold](./Typescript_Most_spread_namespaces_by_modules_above_threshold.svg)

---

## 4. Package Management

### 4.1 Maven POM Declared Dependencies

Java dependencies declared in Maven `pom.xml` files.



### 4.2 package.json Declared Dependencies

Node.js dependencies declared in `package.json` files, ranked by occurrence across repository packages.

| dependencyName | usingPackageCount | dependencyVersionCount | packageNameExamples | dependencyVersionExamples | packageDirectory |
| --- | --- | --- | --- | --- | --- |
| react | 49 | 0 | ["integration-rsc-vite","@playground/framework-vite-5","@playground/perf-routes","@playground/framework-vite-7-beta","@playground/rsc-vite-7-framework","@playground/middleware","@playground/rsc-vite-framework","@playground/framework-express","@playground/framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-vite-5","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/performance","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-vite-7-beta"] |
| react-dom | 49 | 0 | ["integration-rsc-vite","@playground/framework-vite-5","@playground/perf-routes","@playground/framework-vite-7-beta","@playground/rsc-vite-7-framework","@playground/middleware","@playground/rsc-vite-framework","@playground/framework-express","@playground/framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-vite-5","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/performance","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-vite-7-beta"] |
| react-router | 30 | 0 | ["integration-rsc-vite","@playground/framework-vite-5","@playground/perf-routes","@playground/framework-vite-7-beta","@playground/rsc-vite-7-framework","@playground/middleware","@playground/rsc-vite-framework","@playground/framework-express","@playground/framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-vite-5","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/performance","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-vite-7-beta"] |
| react-router-dom | 23 | 0 | ["search-params","ssr","custom-query-parse-serialization","basic","error-boundaries","ssr-data-router","basic-data-router","auth","custom-link"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/examples/search-params","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/examples/ssr","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/examples/custom-query-parsing","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/examples/basic"] |
| isbot | 22 | 0 | ["@playground/framework-vite-5","@playground/perf-routes","@playground/framework-vite-7-beta","@playground/middleware","@playground/framework-express","@playground/framework","@playground/split-route-modules-spa","@remix-run/react-router","@playground/vite-plugin-cloudflare"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-vite-5","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/performance","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-vite-7-beta","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/middleware"] |
| @react-router/node | 21 | 0 | ["@playground/framework-vite-5","@playground/perf-routes","@playground/framework-vite-7-beta","@playground/middleware","@playground/framework-express","@playground/framework","@playground/split-route-modules-spa","@playground/split-route-modules","@playground/framework-vite-6"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-vite-5","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/performance","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-vite-7-beta","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/middleware"] |
| express | 18 | 0 | ["integration-rsc-vite","@playground/rsc-vite-7-framework","@playground/middleware","@playground/rsc-vite-framework","@playground/framework-express","@playground/vite-plugin-cloudflare","@playground/rsc-vite","ssr","integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/rsc-vite-7-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/rsc-vite-framework"] |
| @react-router/serve | 13 | 0 | ["@playground/framework-vite-5","@playground/perf-routes","@playground/framework-vite-7-beta","@playground/framework","@playground/split-route-modules","@playground/framework-vite-6","integration-vite-6-template","integration-vite-5-template","integration-vite-7-beta-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-vite-5","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/performance","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-vite-7-beta","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework"] |
| compression | 11 | 0 | ["integration-rsc-vite","@playground/rsc-vite-7-framework","@playground/middleware","@playground/rsc-vite-framework","@playground/framework-express","@playground/rsc-vite","ssr","ssr-data-router","multi-app"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/rsc-vite-7-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/rsc-vite-framework"] |
| @react-router/express | 8 | 0 | ["@playground/middleware","@playground/framework-express","integration","integration-vite-6-template","integration-vite-5-template","@react-router/serve","integration-vite-7-beta-template","integration-vite-8-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-express","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/vite-6-template"] |
| @mjackson/node-fetch-server | 7 | 0 | ["integration-rsc-vite","@playground/rsc-vite-7-framework","@playground/rsc-vite-framework","@playground/rsc-vite","@react-router/node","@react-router/serve","integration-rsc-vite-framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/rsc-vite-7-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/rsc-vite-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/rsc-vite"] |
| serialize-javascript | 7 | 0 | ["@playground/vite-plugin-cloudflare","integration","integration-vite-6-template","integration-vite-5-template","integration-vite-plugin-cloudflare-template","integration-vite-7-beta-template","integration-vite-8-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/vite-plugin-cloudflare","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/vite-6-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/vite-5-template"] |
| react-server-dom-webpack | 6 | 0 | ["integration-rsc-vite","@playground/rsc-vite-7-framework","@playground/rsc-vite-framework","@playground/rsc-vite","integration","integration-rsc-vite-framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/rsc-vite-7-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/rsc-vite-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/rsc-vite"] |
| cross-env | 5 | 0 | ["integration-rsc-vite","@playground/middleware","ssr","ssr-data-router","multi-app"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/examples/ssr","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/examples/ssr-data-router"] |
| semver | 5 | 0 | ["@remix-run/react-router","react-router-scripts","integration","create-react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/scripts","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router"] |
| @vanilla-extract/vite-plugin | 5 | 0 | ["integration","integration-vite-6-template","integration-vite-5-template","integration-vite-7-beta-template","integration-vite-8-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/vite-6-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/vite-5-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/vite-7-beta-template"] |
| @vanilla-extract/css | 5 | 0 | ["integration","integration-vite-6-template","integration-vite-5-template","integration-vite-7-beta-template","integration-vite-8-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/vite-6-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/vite-5-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/vite-7-beta-template"] |
| morgan | 3 | 0 | ["@playground/middleware","@playground/framework-express","@react-router/serve"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/framework-express","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-serve"] |
| picocolors | 3 | 0 | ["@remix-run/react-router","create-react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| prettier | 3 | 0 | ["@remix-run/react-router","integration","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| remix-utils | 2 | 0 | ["@playground/rsc-vite-7-framework","@playground/rsc-vite-framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/rsc-vite-7-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/playground/rsc-vite-framework"] |
| @babel/core | 2 | 0 | ["@remix-run/react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| typescript | 2 | 0 | ["@remix-run/react-router","integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| @mdx-js/rollup | 2 | 0 | ["@remix-run/react-router","integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| vite | 2 | 0 | ["@remix-run/react-router","integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| @playwright/test | 2 | 0 | ["@remix-run/react-router","integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| @babel/preset-typescript | 2 | 0 | ["@remix-run/react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| dedent | 2 | 0 | ["integration","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| execa | 2 | 0 | ["integration","create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router"] |
| strip-ansi | 2 | 0 | ["integration","create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router"] |
| get-port | 2 | 0 | ["integration","@react-router/serve"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-serve"] |
| pathe | 2 | 0 | ["integration","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| arg | 2 | 0 | ["create-react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| @babel/preset-react | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| @types/react | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| eslint-plugin-jsx-a11y | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| jsonfile | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| eslint-plugin-jest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| dox | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| prompts | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| jest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| @eslint/compat | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| eslint-plugin-jsdoc | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| @typescript-eslint/parser | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| vitest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| unist-util-remove | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| @types/jest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| @manypkg/get-packages | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| babel-plugin-dev-expression | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| eslint-plugin-import | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| remark-parse | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| babel-jest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| eslint-plugin-react-hooks | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| @typescript-eslint/eslint-plugin | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| @types/jsdom | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| fast-glob | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| unified | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| @types/react-dom | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| remark-gfm | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| @babel/preset-env | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| @types/react-test-renderer | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| eslint-config-react-app | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| remark-stringify | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| eslint-plugin-flowtype | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| typedoc | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| eslint | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| eslint-plugin-react | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0"] |
| @octokit/request | 1 | 0 | ["react-router-scripts"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/scripts"] |
| jsurl | 1 | 0 | ["custom-query-parse-serialization"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/examples/custom-query-parsing"] |
| postcss | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| shelljs | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| type-fest | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| glob | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| @types/dedent | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| @types/cross-spawn | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| @types/shelljs | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| strip-indent | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| cross-spawn | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| vite-env-only | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| @types/semver | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| cheerio | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| @types/glob | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| vite-tsconfig-paths | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| postcss-import | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| @react-router/dev | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| @types/express | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| @types/wait-on | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| wait-on | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration"] |
| history | 1 | 0 | ["ssr-data-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/examples/ssr-data-router"] |
| @remix-run/router | 1 | 0 | ["ssr-data-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/examples/ssr-data-router"] |
| @reach/dialog | 1 | 0 | ["modal-route-with-outlet"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/examples/modal-route-with-outlet"] |
| @reach/visually-hidden | 1 | 0 | ["custom-filter-link"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/examples/custom-filter-link"] |
| localforage | 1 | 0 | ["notes"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/examples/notes"] |
| sort-package-json | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router"] |
| proxy-agent | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router"] |
| sisteransi | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router"] |
| gunzip-maybe | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router"] |
| log-update | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router"] |
| tar-fs | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router"] |
| @remix-run/web-fetch | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router"] |
| not-react-router | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/create-react-router/__tests__/fixtures/basic"] |
| @architect/functions | 1 | 0 | ["@react-router/architect"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-architect"] |
| @types/aws-lambda | 1 | 0 | ["@react-router/architect"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-architect"] |
| @babel/generator | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| valibot | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| es-module-lexer | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| @babel/plugin-syntax-jsx | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| @remix-run/node-fetch-server | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| tinyglobby | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| babel-dead-code-elimination | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| vite-node | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| jsesc | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| @babel/types | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| @babel/parser | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| p-map | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| exit-hook | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| @babel/traverse | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| lodash | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| chokidar | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| pkg-types | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| react-refresh | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-dev"] |
| set-cookie-parser | 1 | 0 | ["react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router"] |
| cookie | 1 | 0 | ["react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router"] |
| source-map-support | 1 | 0 | ["@react-router/serve"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-serve"] |
| minimatch | 1 | 0 | ["@react-router/fs-routes"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/packages/react-router-fs-routes"] |
| match-sorter | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/tutorials/address-book"] |
| sort-by | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/tutorials/address-book"] |
| tiny-invariant | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/tutorials/address-book"] |
| @react-router/cloudflare | 1 | 0 | ["integration-cloudflare-dev-proxy-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/cloudflare-dev-proxy-template"] |
| miniflare | 1 | 0 | ["integration-cloudflare-dev-proxy-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.16.0/./source/react-router-7.16.0/integration/helpers/cloudflare-dev-proxy-template"] |

---

## 5. Glossary

| Term | Definition |
|------|-----------|
| **Second-level package** | First two dot-separated segments of a package name (e.g. `org.springframework`). Used to group variant packages under one framework name. |
| **numberOfExternalCallerTypes** | Count of *internal Java types* that directly reference the external package. |
| **numberOfExternalCallerPackages** | Count of *internal Java packages* containing at least one type referencing the external package. |
| **numberOfExternalCallerElements** | Count of *internal TypeScript elements* that import from the external module. |
| **numberOfExternalCallerModules** | Count of *internal TypeScript modules* that import from the external module. |
| **sumNumberOfTypes / sumNumberOfPackages** | Sum across all artifacts of internal types/packages dependent on the external package. Measures total spread. |
| **sumNumberOfUsedExternalDeclarations** | Total distinct external declarations imported from the module across all internal modules. |
| **packagesCallingExternalRate** | Ratio of internal packages with external references to total artifact packages. |
| **typesCallingExternalRate** | Ratio of internal types with external references to total artifact types. |
| **Anti-Corruption Layer (ACL)** | Isolates the internal domain from external library APIs by wrapping them behind an internal interface. |
| **Façade** | Simplified interface hiding external library complexity. Useful when many internal modules call the same external package. |
| **Hexagonal Architecture** | Ports & Adapters style that pushes all external dependencies to the outer ring, preventing them from leaking into the core domain. |
