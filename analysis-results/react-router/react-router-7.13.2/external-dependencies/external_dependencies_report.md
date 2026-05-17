---
title: "External Dependencies Report"
generated: "2026-05-17"
model_version: "v4.0.1"
dataset: "react-router-7.13.2"
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
| node | 23 | 29 | 280 | 436 | 139 | 631 | ["<reactRouterRSCVitePlugin> of module <vite> imports <EnvironmentModuleNode.file> from external module <node>","<reactRouterRSCVitePlugin> of module <vite> imports <PluginOption> from external module <node>","<reactRouterRSCVitePlugin> of module <vite> imports <isCSSRequest> from external module <node>","<reactRouterRSCVitePlugin> of module <vite> imports <createLogger> from external module <node>"] |
| @types/process | 17 | 20 | 42 | 126 | 139 | 631 | ["<Context> of module <create-react-router> imports <global.NodeJS.ReadStream> from external module <process>","<Context> of module <create-react-router> imports <global.NodeJS.WriteStream> from external module <process>","<renderLoadingIndicator> of module <loading-indicator> imports <global.NodeJS.ReadStream> from external module <process>","<renderLoadingIndicator> of module <loading-indicator> imports <global.NodeJS.WriteStream> from external module <process>"] |
| dist | 17 | 27 | 99 | 267 | 139 | 631 | ["<relative> of module <routes> imports <resolve> from external module <dist>","<relative> of module <routes> imports <resolve> from external module <dist>","<reactRouterRSCVitePlugin> of module <vite> imports <join> from external module <dist>","<reactRouterRSCVitePlugin> of module <vite> imports <resolve> from external module <dist>"] |
| @types/path | 14 | 20 | 55 | 117 | 139 | 631 | ["<stripDirectoryFromPath> of module <utils> imports <path.PlatformPath.sep> from external module <path>","<getDirectoryFilesRecursive> of module <utils> imports <path.PlatformPath.sep> from external module <path>","<createFileSessionStorage> of module <fileStorage> imports <path.PlatformPath.dirname> from external module <path>","<createFileSessionStorage> of module <react-router-node> imports <path.PlatformPath.dirname> from external module <path>"] |
| picocolors | 10 | 11 | 14 | 83 | 139 | 631 | ["<color> of module <utils> imports <picocolors> from external module <picocolors>","<reactRouterRSCVitePlugin> of module <vite> imports <picocolors> from external module <picocolors>","<reactRouterRSCVitePlugin> of module <plugin> imports <picocolors> from external module <picocolors>","<reactRouterVitePlugin> of module <vite> imports <picocolors> from external module <picocolors>"] |
| node:fs | 9 | 11 | 25 | 48 | 139 | 631 | ["<fileExists> of module <utils> imports <.promises> from external module <node:fs>","<fileExists> of module <utils> imports <node:fs> from external module <node:fs>","<ensureDirectory> of module <utils> imports <node:fs> from external module <node:fs>","<ensureDirectory> of module <utils> imports <.promises> from external module <node:fs>"] |
| promises | 9 | 13 | 36 | 60 | 139 | 631 | ["<getDirectoryFilesRecursive> of module <utils> imports <readdir> from external module <promises>","<fileExists> of module <utils> imports <.stat> from external module <promises>","<ensureDirectory> of module <utils> imports <.mkdir> from external module <promises>","<directoryExists> of module <utils> imports <.stat> from external module <promises>"] |
| @types/globals | 8 | 9 | 11 | 15 | 139 | 631 | ["<reactRouterRSCVitePlugin> of module <vite> imports <global.NodeRequire.resolve> from external module <globals>","<reactRouterRSCVitePlugin> of module <plugin> imports <global.NodeRequire.resolve> from external module <globals>","<reactRouterVitePlugin> of module <vite> imports <global.NodeRequire.resolve> from external module <globals>","<reactRouterVitePlugin> of module <plugin> imports <global.NodeRequire.resolve> from external module <globals>"] |
| @types/react | 8 | 24 | 91 | 292 | 139 | 631 | ["<AwaitContextProvider> of module <context> imports <React.FunctionComponentElement> from external module <react>","<AwaitContextProvider> of module <context> imports <React.createElement> from external module <react>","<AwaitContextProvider> of module <context> imports <React.ProviderProps> from external module <react>","<AwaitContextProvider> of module <context> imports <React.Context.Provider> from external module <react>"] |
| node:path | 7 | 11 | 11 | 28 | 139 | 631 | ["<stripDirectoryFromPath> of module <utils> imports <node:path> from external module <node:path>","<getDirectoryFilesRecursive> of module <utils> imports <node:path> from external module <node:path>","<pathContains> of module <utils> imports <node:path> from external module <node:path>","<stop> of module <profiler> imports <node:path> from external module <node:path>"] |
| @types/babel__generator | 6 | 7 | 12 | 14 | 139 | 631 | ["<reactRouterVitePlugin> of module <vite> imports <GeneratorResult> from external module <babel__generator>","<reactRouterVitePlugin> of module <vite> imports <GeneratorResult.code> from external module <babel__generator>","<reactRouterVitePlugin> of module <plugin> imports <GeneratorResult> from external module <babel__generator>","<reactRouterVitePlugin> of module <plugin> imports <GeneratorResult.code> from external module <babel__generator>"] |
| @types/buffer | 6 | 4 | 12 | 13 | 139 | 631 | ["<createReactRouterRequest> of module <server> imports <global.Buffer.toString> from external module <buffer>","<createReactRouterRequest> of module <server> imports <global.BufferConstructor.from> from external module <buffer>","<readableStreamToString> of module <stream> imports <global.Buffer.toString> from external module <buffer>","<readableStreamToString> of module <stream> imports <global.BufferConstructor.concat> from external module <buffer>"] |
| http | 6 | 5 | 10 | 10 | 139 | 631 | ["<createRemixHeaders> of module <server> imports <IncomingHttpHeaders> from external module <http>","<createRequestListener> of module <react-router-node> imports <RequestListener> from external module <http>","<createRequestListener> of module <server> imports <RequestListener> from external module <http>","<reactRouterVitePlugin> of module <vite> imports <ServerResponse.end> from external module <http>"] |
| readline | 6 | 6 | 10 | 104 | 139 | 631 | ["<ConfirmPrompt> of module <prompts-confirm> imports <Key> from external module <readline>","<MultiSelectPrompt> of module <prompts-multi-select> imports <Key> from external module <readline>","<Prompt> of module <prompts-prompt-base> imports <Key> from external module <readline>","<Prompt> of module <prompts-prompt-base> imports <Interface.close> from external module <readline>"] |
| sisteransi | 6 | 6 | 27 | 292 | 139 | 631 | ["<ConfirmPrompt> of module <prompts-confirm> imports <cursor.hide> from external module <sisteransi>","<ConfirmPrompt> of module <prompts-confirm> imports <erase.line> from external module <sisteransi>","<ConfirmPrompt> of module <prompts-confirm> imports <cursor.to> from external module <sisteransi>","<ConfirmPrompt> of module <prompts-confirm> imports <erase> from external module <sisteransi>"] |
| @babel/lib | 5 | 6 | 64 | 142 | 139 | 631 | ["<transpile> of module <useJavascript> imports <lib> from external module <lib>","<transpile> of module <useJavascript> imports <lib> from external module <lib>","<removeExports> of module <remove-exports> imports <AssignmentExpression.left> from external module <lib>","<removeExports> of module <remove-exports> imports <ExportNamedDeclaration.specifiers> from external module <lib>"] |
| @types/pick | 5 | 5 | 9 | 9 | 139 | 631 | ["<route> of module <routes> imports <pick> from external module <pick>","<route> of module <routes> imports <pick> from external module <pick>","<index> of module <routes> imports <pick> from external module <pick>","<index> of module <routes> imports <pick> from external module <pick>"] |
| fs | 5 | 5 | 13 | 19 | 139 | 631 | ["<fileExists> of module <utils> imports <Stats.isFile> from external module <fs>","<directoryExists> of module <utils> imports <Stats.isDirectory> from external module <fs>","<reactRouterVitePlugin> of module <vite> imports <Dirent.name> from external module <fs>","<reactRouterVitePlugin> of module <vite> imports <Dirent.isFile> from external module <fs>"] |
| @types/babel__core | 4 | 3 | 14 | 15 | 139 | 631 | ["<reactRouterRSCVitePlugin> of module <vite> imports <transformAsync> from external module <babel__core>","<reactRouterRSCVitePlugin> of module <vite> imports <BabelFileResult.map> from external module <babel__core>","<reactRouterRSCVitePlugin> of module <vite> imports <BabelFileResult.code> from external module <babel__core>","<reactRouterRSCVitePlugin> of module <plugin> imports <transformAsync> from external module <babel__core>"] |
| lexer | 4 | 3 | 5 | 5 | 139 | 631 | ["<reactRouterRSCVitePlugin> of module <vite> imports <init> from external module <lexer>","<reactRouterRSCVitePlugin> of module <plugin> imports <init> from external module <lexer>","<reactRouterVitePlugin> of module <vite> imports <init> from external module <lexer>","<reactRouterVitePlugin> of module <plugin> imports <init> from external module <lexer>"] |
| @cloudflare/workers-types | 3 | 5 | 52 | 68 | 139 | 631 | ["<createRequestHandler> of module <react-router-cloudflare> imports <EventContext.request> from external module <workers-types>","<createRequestHandler> of module <react-router-cloudflare> imports <EventContext.waitUntil> from external module <workers-types>","<createRequestHandler> of module <react-router-cloudflare> imports <EventContext.passThroughOnException> from external module <workers-types>","<createRequestHandler> of module <react-router-cloudflare> imports <Request.cf> from external module <workers-types>"] |
| @types/babel__traverse | 3 | 3 | 17 | 49 | 139 | 631 | ["<removeExports> of module <remove-exports> imports <NodePath.node> from external module <babel__traverse>","<removeExports> of module <remove-exports> imports <NodePath.isProgram> from external module <babel__traverse>","<removeExports> of module <remove-exports> imports <NodePath.parentPath> from external module <babel__traverse>","<removeExports> of module <remove-exports> imports <NodePath.remove> from external module <babel__traverse>"] |
| node:process | 3 | 7 | 7 | 138 | 139 | 631 | ["<Context> of module <create-react-router> imports <node:process> from external module <node:process>","<Prompt> of module <prompts-prompt-base> imports <node:process> from external module <node:process>","<PromptOptions> of module <prompts-prompt-base> imports <node:process> from external module <node:process>","<isInteractive> of module <utils> imports <node:process> from external module <node:process>"] |
| node:url | 3 | 2 | 4 | 4 | 139 | 631 | ["<copyTemplate> of module <copy-template> imports <node:url> from external module <node:url>","<copyTemplate> of module <copy-template> imports <.fileURLToPath> from external module <node:url>","<reactRouterVitePlugin> of module <vite> imports <.pathToFileURL> from external module <node:url>","<reactRouterVitePlugin> of module <plugin> imports <.pathToFileURL> from external module <node:url>"] |
| rollup | 3 | 3 | 18 | 32 | 139 | 631 | ["<reactRouterRSCVitePlugin> of module <vite> imports <RollupOptions.onwarn> from external module <rollup>","<reactRouterRSCVitePlugin> of module <vite> imports <RollupLog.message> from external module <rollup>","<reactRouterRSCVitePlugin> of module <vite> imports <RollupLog.pos> from external module <rollup>","<reactRouterRSCVitePlugin> of module <vite> imports <RollupLog.code> from external module <rollup>"] |
| @architect/functions | 2 | 1 | 4 | 4 | 139 | 631 | ["<createArcTableSessionStorage> of module <react-router-architect> imports <tables> from external module <functions>","<createArcTableSessionStorage> of module <react-router-architect> imports <functions> from external module <functions>","<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <tables> from external module <functions>","<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <functions> from external module <functions>"] |
| @architect/tables | 2 | 1 | 6 | 10 | 139 | 631 | ["<createArcTableSessionStorage> of module <react-router-architect> imports <ArcTable.delete> from external module <tables>","<createArcTableSessionStorage> of module <react-router-architect> imports <ArcTable.put> from external module <tables>","<createArcTableSessionStorage> of module <react-router-architect> imports <ArcTable.get> from external module <tables>","<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <ArcTable.delete> from external module <tables>"] |
| @babel/babel-parser | 2 | 2 | 3 | 5 | 139 | 631 | ["<removeExports> of module <remove-exports> imports <ParseResult> from external module <babel-parser>","<decorateComponentExportsWithProps> of module <with-props> imports <ParseResult> from external module <babel-parser>","<decorateComponentExportsWithProps> of module <with-props> imports <ParseResult.program> from external module <babel-parser>"] |
| @mjackson/node-fetch-server | 2 | 2 | 4 | 18 | 139 | 631 | ["<createRequestListener> of module <react-router-node> imports <createRequestListener> from external module <node-fetch-server>","<createRequestListener> of module <server> imports <createRequestListener> from external module <node-fetch-server>","<RequestListenerOptions> of module <server> imports <ClientAddress> from external module <node-fetch-server>","<RequestListenerOptions> of module <react-router-node> imports <ClientAddress> from external module <node-fetch-server>"] |
| @types/api-gateway-proxy | 2 | 5 | 23 | 30 | 139 | 631 | ["<GetLoadContextFunction> of module <react-router-architect> imports <APIGatewayEventRequestContextV2> from external module <api-gateway-proxy>","<GetLoadContextFunction> of module <react-router-architect> imports <APIGatewayProxyEventV2> from external module <api-gateway-proxy>","<GetLoadContextFunction> of module <server> imports <APIGatewayEventRequestContextV2> from external module <api-gateway-proxy>","<GetLoadContextFunction> of module <server> imports <APIGatewayProxyEventV2> from external module <api-gateway-proxy>"] |
| @types/express | 2 | 4 | 25 | 29 | 139 | 631 | ["<RequestHandler> of module <server> imports <e.Request> from external module <express>","<RequestHandler> of module <server> imports <e.NextFunction> from external module <express>","<RequestHandler> of module <server> imports <e.Response> from external module <express>","<RequestHandler> of module <react-router-express> imports <e.Request> from external module <express>"] |
| @types/express-serve-static-core | 2 | 3 | 5 | 5 | 139 | 631 | ["<RequestHandler> of module <server> imports <ParamsDictionary> from external module <express-serve-static-core>","<RequestHandler> of module <react-router-express> imports <ParamsDictionary> from external module <express-serve-static-core>","<GetLoadContextFunction> of module <react-router-express> imports <ParamsDictionary> from external module <express-serve-static-core>","<GetLoadContextFunction> of module <server> imports <ParamsDictionary> from external module <express-serve-static-core>"] |
| @types/handler | 2 | 1 | 4 | 4 | 139 | 631 | ["<RequestHandler> of module <react-router-architect> imports <Context> from external module <handler>","<RequestHandler> of module <react-router-architect> imports <Callback> from external module <handler>","<RequestHandler> of module <server> imports <Context> from external module <handler>","<RequestHandler> of module <server> imports <Callback> from external module <handler>"] |
| @types/jsesc | 2 | 1 | 2 | 4 | 139 | 631 | ["<reactRouterVitePlugin> of module <vite> imports <jsesc> from external module <jsesc>","<reactRouterVitePlugin> of module <plugin> imports <jsesc> from external module <jsesc>"] |
| @types/qs | 2 | 3 | 5 | 5 | 139 | 631 | ["<RequestHandler> of module <server> imports <QueryString.ParsedQs> from external module <qs>","<RequestHandler> of module <react-router-express> imports <QueryString.ParsedQs> from external module <qs>","<GetLoadContextFunction> of module <react-router-express> imports <QueryString.ParsedQs> from external module <qs>","<GetLoadContextFunction> of module <server> imports <QueryString.ParsedQs> from external module <qs>"] |
| @types/stream | 2 | 3 | 18 | 20 | 139 | 631 | ["<writeReadableStreamToWritable> of module <react-router-node> imports <Stream.Writable.destroy> from external module <stream>","<writeReadableStreamToWritable> of module <react-router-node> imports <Stream.Writable.write> from external module <stream>","<writeReadableStreamToWritable> of module <react-router-node> imports <Stream.Writable> from external module <stream>","<writeReadableStreamToWritable> of module <react-router-node> imports <Stream.Writable.end> from external module <stream>"] |
| async_hooks | 2 | 4 | 8 | 8 | 139 | 631 | ["<redirect> of module <react-router> imports <AsyncLocalStorage.getStore> from external module <async_hooks>","<redirect> of module <server> imports <AsyncLocalStorage.getStore> from external module <async_hooks>","<getRequest> of module <react-router> imports <AsyncLocalStorage.getStore> from external module <async_hooks>","<getRequest> of module <server> imports <AsyncLocalStorage.getStore> from external module <async_hooks>"] |
| cli | 2 | 1 | 2 | 4 | 139 | 631 | ["<cloudflareDevProxyVitePlugin> of module <cloudflare> imports <GetPlatformProxyOptions> from external module <cli>","<cloudflareDevProxyVitePlugin> of module <cloudflare-dev-proxy> imports <GetPlatformProxyOptions> from external module <cli>"] |
| crypto | 2 | 1 | 4 | 4 | 139 | 631 | ["<reactRouterVitePlugin> of module <vite> imports <Hash.update> from external module <crypto>","<reactRouterVitePlugin> of module <vite> imports <Hash.digest> from external module <crypto>","<reactRouterVitePlugin> of module <plugin> imports <Hash.update> from external module <crypto>","<reactRouterVitePlugin> of module <plugin> imports <Hash.digest> from external module <crypto>"] |
| esm | 2 | 2 | 6 | 7 | 139 | 631 | ["<createConfigLoader> of module <config> imports <_default.watch> from external module <esm>","<createConfigLoader> of module <config> imports <esm> from external module <esm>","<createConfigLoader> of module <config> imports <FSWatcher.on> from external module <esm>","<createConfigLoader> of module <config> imports <FSWatcher.unwatch> from external module <esm>"] |
| module-runner | 2 | 1 | 2 | 2 | 139 | 631 | ["<reactRouterVitePlugin> of module <vite> imports <ModuleRunner.import> from external module <module-runner>","<reactRouterVitePlugin> of module <plugin> imports <ModuleRunner.import> from external module <module-runner>"] |
| node:crypto | 2 | 1 | 2 | 2 | 139 | 631 | ["<reactRouterVitePlugin> of module <vite> imports <createHash> from external module <node:crypto>","<reactRouterVitePlugin> of module <plugin> imports <createHash> from external module <node:crypto>"] |
| url | 2 | 1 | 2 | 2 | 139 | 631 | ["<reactRouterVitePlugin> of module <vite> imports <URL.href> from external module <url>","<reactRouterVitePlugin> of module <plugin> imports <URL.href> from external module <url>"] |
| @types/APIGatewayProxyEventHeaders."content-type | 1 | 1 | 1 | 1 | 139 | 631 | ["<createReactRouterRequest> of module <server> imports <APIGatewayProxyEventHeaders.\"content-type\"> from external module <APIGatewayProxyEventHeaders.\"content-type>"] |
| @types/APIGatewayProxyEventHeaders."x-forwarded-host | 1 | 1 | 1 | 1 | 139 | 631 | ["<createReactRouterRequest> of module <server> imports <APIGatewayProxyEventHeaders.\"x-forwarded-host\"> from external module <APIGatewayProxyEventHeaders.\"x-forwarded-host>"] |
| @types/events | 1 | 1 | 1 | 1 | 139 | 631 | ["<Prompt> of module <prompts-prompt-base> imports <EventEmitter> from external module <events>"] |
| @types/isEqual | 1 | 1 | 1 | 2 | 139 | 631 | ["<createConfigLoader> of module <config> imports <isEqual> from external module <isEqual>"] |
| @types/kebabCase | 1 | 1 | 1 | 1 | 139 | 631 | ["<getEnvironmentOptionsResolvers> of module <plugin> imports <kebabCase> from external module <kebabCase>"] |
| @types/semver | 1 | 1 | 2 | 2 | 139 | 631 | ["<run> of module <run> imports <semver> from external module <semver>","<run> of module <run> imports <major> from external module <semver>"] |
| @types/timers | 1 | 1 | 1 | 13 | 139 | 631 | ["<SelectPrompt> of module <prompts-select> imports <global.NodeJS.Timeout> from external module <timers>"] |
| arg | 1 | 1 | 2 | 3 | 139 | 631 | ["<run> of module <run> imports <arg> from external module <arg>","<run> of module <run> imports <arg.Result._> from external module <arg>"] |
| arg.Result."--no-typescript | 1 | 1 | 1 | 1 | 139 | 631 | ["<run> of module <run> imports <arg.Result.\"--no-typescript\"> from external module <arg.Result.\"--no-typescript>"] |
| exit-hook | 1 | 1 | 1 | 1 | 139 | 631 | ["<dev> of module <commands> imports <exit-hook> from external module <exit-hook>"] |
| inspector | 1 | 3 | 5 | 7 | 139 | 631 | ["<getSession> of module <profiler> imports <Session> from external module <inspector>","<start> of module <profiler> imports <Session.connect> from external module <inspector>","<start> of module <profiler> imports <.Session> from external module <inspector>","<start> of module <profiler> imports <Session.post> from external module <inspector>"] |
| node:child_process | 1 | 1 | 1 | 1 | 139 | 631 | ["<resolveEntryFiles> of module <config> imports <execSync> from external module <node:child_process>"] |
| node:readline | 1 | 1 | 3 | 52 | 139 | 631 | ["<Prompt> of module <prompts-prompt-base> imports <node:readline> from external module <node:readline>","<Prompt> of module <prompts-prompt-base> imports <.emitKeypressEvents> from external module <node:readline>","<Prompt> of module <prompts-prompt-base> imports <.createInterface> from external module <node:readline>"] |
| p-map | 1 | 1 | 1 | 1 | 139 | 631 | ["<prerender> of module <prerender> imports <p-map> from external module <p-map>"] |
| prettier | 1 | 1 | 2 | 2 | 139 | 631 | ["<transpile> of module <useJavascript> imports <format> from external module <prettier>","<transpile> of module <useJavascript> imports <prettier> from external module <prettier>"] |
| server | 1 | 2 | 4 | 4 | 139 | 631 | ["<Context> of module <vite-node> imports <ViteNodeServer> from external module <server>","<createContext> of module <vite-node> imports <ViteNodeServer.fetchModule> from external module <server>","<createContext> of module <vite-node> imports <ViteNodeServer.resolveId> from external module <server>","<createContext> of module <vite-node> imports <ViteNodeServer.getSourceMap> from external module <server>"] |
| types | 1 | 1 | 1 | 2 | 139 | 631 | ["<color> of module <utils> imports <Formatter> from external module <types>"] |

### 3.2 Most Used External Namespaces

Groups by namespace to reveal declaration-level coupling within npm packages.

| externalNamespaceName | numberOfExternalCallerModules | numberOfExternalCallerElements | numberOfExternalDeclarationCalls | numberOfExternalDeclarationCallsWeighted | allModules | allInternalElements | exampleStories |
| --- | --- | --- | --- | --- | --- | --- | --- |
| no namespace | 53 | 96 | 606 | 1629 | 139 | 631 | ["<copyTemplate> of module <copy-template> imports <node:url> from external namespace <>","<copyTemplate> of module <copy-template> imports <.fileURLToPath> from external namespace <>","<Context> of module <create-react-router> imports <node:process> from external namespace <>","<ConfirmPrompt> of module <prompts-confirm> imports <Key> from external namespace <>"] |
| @types | 51 | 93 | 353 | 768 | 139 | 631 | ["<Context> of module <create-react-router> imports <global.NodeJS.ReadStream> from external namespace <@types>","<Context> of module <create-react-router> imports <global.NodeJS.WriteStream> from external namespace <@types>","<renderLoadingIndicator> of module <loading-indicator> imports <global.NodeJS.ReadStream> from external namespace <@types>","<renderLoadingIndicator> of module <loading-indicator> imports <global.NodeJS.WriteStream> from external namespace <@types>"] |
| @babel | 5 | 6 | 67 | 147 | 139 | 631 | ["<transpile> of module <useJavascript> imports <lib> from external namespace <@babel>","<transpile> of module <useJavascript> imports <lib> from external namespace <@babel>","<removeExports> of module <remove-exports> imports <AssignmentExpression.left> from external namespace <@babel>","<removeExports> of module <remove-exports> imports <ExportNamedDeclaration.specifiers> from external namespace <@babel>"] |
| @cloudflare | 3 | 5 | 52 | 68 | 139 | 631 | ["<createRequestHandler> of module <react-router-cloudflare> imports <EventContext.request> from external namespace <@cloudflare>","<createRequestHandler> of module <react-router-cloudflare> imports <EventContext.waitUntil> from external namespace <@cloudflare>","<createRequestHandler> of module <react-router-cloudflare> imports <EventContext.passThroughOnException> from external namespace <@cloudflare>","<createRequestHandler> of module <react-router-cloudflare> imports <Request.cf> from external namespace <@cloudflare>"] |
| @architect | 2 | 1 | 10 | 14 | 139 | 631 | ["<createArcTableSessionStorage> of module <react-router-architect> imports <ArcTable.delete> from external namespace <@architect>","<createArcTableSessionStorage> of module <react-router-architect> imports <ArcTable.put> from external namespace <@architect>","<createArcTableSessionStorage> of module <react-router-architect> imports <ArcTable.get> from external namespace <@architect>","<createArcTableSessionStorage> of module <react-router-architect> imports <tables> from external namespace <@architect>"] |
| @mjackson | 2 | 2 | 4 | 18 | 139 | 631 | ["<createRequestListener> of module <react-router-node> imports <createRequestListener> from external namespace <@mjackson>","<createRequestListener> of module <server> imports <createRequestListener> from external namespace <@mjackson>","<RequestListenerOptions> of module <server> imports <ClientAddress> from external namespace <@mjackson>","<RequestListenerOptions> of module <react-router-node> imports <ClientAddress> from external namespace <@mjackson>"] |

### 3.3 Most Spread External Modules

External modules referenced from the highest number of **different internal TypeScript modules**.

| externalModuleName | numberOfInternalModules | sumNumberOfUsedExternalDeclarations | minNumberOfUsedExternalDeclarations | maxNumberOfUsedExternalDeclarations | medNumberOfUsedExternalDeclarations | avgNumberOfUsedExternalDeclarations | stdNumberOfUsedExternalDeclarations | sumNumberOfInternalElements | minNumberOfInternalElements | maxNumberOfInternalElements | medNumberOfInternalElements | avgNumberOfInternalElements | stdNumberOfInternalElements | minNumberOfInternalElementsPercentage | maxNumberOfInternalElementsPercentage | medNumberOfInternalElementsPercentage | avgNumberOfInternalElementsPercentage | stdNumberOfInternalElementsPercentage | internalModuleExamples |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| node | 21 | 241 | 1 | 81 | 3 | 11.476190476190476 | 22.653077158785834 | 32 | 1 | 8 | 1 | 1.5238095238095235 | 1.569045812557671 | 0.15847860538827258 | 1.2678288431061806 | 0.15847860538827258 | 0.24149120821070102 | 0.24866019216444862 | ["vite","plugin","commands","config"] |
| @types/process | 16 | 39 | 1 | 5 | 2 | 2.4375 | 1.5478479684172257 | 22 | 1 | 4 | 1 | 1.3750000000000002 | 0.806225774829855 | 0.15847860538827258 | 0.6339144215530903 | 0.15847860538827258 | 0.21790808240887474 | 0.12776953642311487 | ["create-react-router","loading-indicator","prompts-prompt-base","utils"] |
| dist | 15 | 73 | 1 | 26 | 4 | 4.866666666666667 | 6.289068369192766 | 31 | 1 | 5 | 1 | 2.066666666666667 | 1.4375905768565218 | 0.15847860538827258 | 0.7923930269413628 | 0.15847860538827258 | 0.32752245113576334 | 0.22782734973954383 | ["routes","vite","plugin","commands"] |
| @types/path | 13 | 41 | 1 | 7 | 2 | 3.1538461538461533 | 2.192645048267573 | 22 | 1 | 5 | 1 | 1.6923076923076923 | 1.1821319289469756 | 0.15847860538827258 | 0.7923930269413628 | 0.15847860538827258 | 0.26819456296476896 | 0.1873426194844652 | ["utils","fileStorage","react-router-node","vite"] |
| node:fs | 9 | 20 | 1 | 4 | 2 | 2.2222222222222228 | 0.97182531580755 | 13 | 1 | 3 | 1 | 1.4444444444444444 | 0.881917103688197 | 0.15847860538827258 | 0.4754358161648177 | 0.15847860538827258 | 0.2289135411163937 | 0.13976499266057002 | ["utils","fileStorage","react-router-node","vite"] |
| picocolors | 9 | 10 | 1 | 2 | 1 | 1.1111111111111114 | 0.33333333333333337 | 13 | 1 | 3 | 1 | 1.4444444444444444 | 0.7264831572567788 | 0.15847860538827258 | 0.4754358161648177 | 0.15847860538827258 | 0.2289135411163937 | 0.11513203760012343 | ["utils","vite","plugin","commands"] |
| promises | 8 | 30 | 1 | 7 | 3.5 | 3.7499999999999996 | 2.2519832529192065 | 16 | 1 | 4 | 1.5 | 2 | 1.3093073414159542 | 0.15847860538827258 | 0.6339144215530903 | 0.23771790808240886 | 0.31695721077654515 | 0.20749720149222728 | ["utils","fileStorage","react-router-node","vite"] |
| @types/globals | 7 | 7 | 1 | 1 | 1 | 1 | 0 | 11 | 1 | 3 | 1 | 1.5714285714285714 | 0.7867957924694431 | 0.15847860538827258 | 0.4754358161648177 | 0.15847860538827258 | 0.24903780846728546 | 0.12469029991591807 | ["vite","plugin","commands","run"] |
| @types/babel__generator | 6 | 9 | 1 | 2 | 1.5 | 1.5 | 0.5477225575051661 | 8 | 1 | 3 | 1 | 1.3333333333333333 | 0.816496580927726 | 0.15847860538827258 | 0.4754358161648177 | 0.15847860538827258 | 0.21130480718436345 | 0.12939723944971887 | ["vite","plugin","generate","babel"] |
| @types/buffer | 6 | 11 | 1 | 3 | 2 | 1.8333333333333333 | 0.752772652709081 | 7 | 1 | 2 | 1 | 1.1666666666666665 | 0.408248290463863 | 0.15847860538827258 | 0.31695721077654515 | 0.15847860538827258 | 0.18489170628631799 | 0.06469861972485942 | ["server","stream","react-router-node","fileStorage"] |
| @types/react | 6 | 34 | 1 | 12 | 4.5 | 5.666666666666667 | 4.179314138308661 | 38 | 1 | 14 | 4 | 6.333333333333333 | 5.715476066494082 | 0.15847860538827258 | 2.218700475435816 | 0.6339144215530903 | 1.0036978341257263 | 0.905780676148032 | ["context","react-router","server","utils"] |
| node:path | 6 | 6 | 1 | 1 | 1 | 1 | 0 | 11 | 1 | 3 | 1.5 | 1.8333333333333333 | 0.983192080250175 | 0.15847860538827258 | 0.4754358161648177 | 0.23771790808240886 | 0.2905441098784997 | 0.1558149097068423 | ["utils","profiler","prerender","normalizeSlashes"] |
| readline | 6 | 10 | 1 | 4 | 1 | 1.6666666666666665 | 1.2110601416389966 | 6 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["prompts-confirm","prompts-multi-select","prompts-prompt-base","prompts-select"] |
| sisteransi | 6 | 27 | 3 | 7 | 4 | 4.5 | 1.378404875209022 | 6 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["prompts-confirm","prompts-multi-select","prompts-prompt-base","prompts-select"] |
| @babel/lib | 5 | 48 | 2 | 16 | 8 | 9.6 | 6.2289646009589745 | 6 | 1 | 2 | 1 | 1.2 | 0.4472135954999579 | 0.15847860538827258 | 0.31695721077654515 | 0.15847860538827258 | 0.19017432646592708 | 0.07087378692550839 | ["useJavascript","remove-exports","route-chunks","styles"] |
| fs | 5 | 13 | 2 | 3 | 3 | 2.6 | 0.5477225575051661 | 6 | 1 | 2 | 1 | 1.2 | 0.4472135954999579 | 0.15847860538827258 | 0.31695721077654515 | 0.15847860538827258 | 0.19017432646592708 | 0.07087378692550839 | ["utils","vite","plugin","config"] |
| http | 5 | 9 | 1 | 2 | 2 | 1.8 | 0.4472135954999579 | 7 | 1 | 2 | 1 | 1.4 | 0.5477225575051662 | 0.15847860538827258 | 0.31695721077654515 | 0.15847860538827258 | 0.22187004754358158 | 0.08680230705311666 | ["server","react-router-node","vite","plugin"] |
| @types/pick | 4 | 4 | 1 | 1 | 1 | 1 | 0 | 6 | 1 | 3 | 1 | 1.5 | 1 | 0.15847860538827258 | 0.4754358161648177 | 0.15847860538827258 | 0.23771790808240884 | 0.15847860538827258 | ["routes","vite","plugin","config"] |
| @cloudflare/workers-types | 3 | 44 | 4 | 22 | 18 | 14.666666666666668 | 9.451631252505218 | 10 | 1 | 5 | 4 | 3.333333333333333 | 2.0816659994661326 | 0.15847860538827258 | 0.7923930269413628 | 0.6339144215530903 | 0.5282620179609085 | 0.32989952447957727 | ["react-router-cloudflare","worker","workersKVStorage"] |
| @types/babel__core | 3 | 8 | 2 | 3 | 3 | 2.6666666666666665 | 0.5773502691896257 | 5 | 1 | 2 | 2 | 1.6666666666666667 | 0.5773502691896258 | 0.15847860538827258 | 0.31695721077654515 | 0.31695721077654515 | 0.2641310089804543 | 0.09149766548171565 | ["vite","plugin","useJavascript"] |
| @types/babel__traverse | 3 | 17 | 2 | 11 | 4 | 5.666666666666666 | 4.725815626252609 | 3 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["remove-exports","styles","with-props"] |
| lexer | 3 | 3 | 1 | 1 | 1 | 1 | 0 | 5 | 1 | 2 | 2 | 1.6666666666666667 | 0.5773502691896258 | 0.15847860538827258 | 0.31695721077654515 | 0.31695721077654515 | 0.2641310089804543 | 0.09149766548171565 | ["vite","plugin","virtual-route-modules"] |
| node:process | 3 | 3 | 1 | 1 | 1 | 1 | 0 | 7 | 1 | 4 | 2 | 2.3333333333333335 | 1.5275252316519465 | 0.15847860538827258 | 0.6339144215530903 | 0.31695721077654515 | 0.369783412572636 | 0.2420800684075985 | ["create-react-router","prompts-prompt-base","utils"] |
| node:url | 3 | 4 | 1 | 2 | 1 | 1.3333333333333333 | 0.5773502691896257 | 3 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["copy-template","vite","plugin"] |
| @architect/functions | 2 | 4 | 2 | 2 | 2 | 2 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["react-router-architect","arcTableSessionStorage"] |
| @architect/tables | 2 | 6 | 3 | 3 | 3 | 3 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["react-router-architect","arcTableSessionStorage"] |
| @babel/babel-parser | 2 | 3 | 1 | 2 | 1.5 | 1.5 | 0.7071067811865476 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["remove-exports","with-props"] |
| @mjackson/node-fetch-server | 2 | 4 | 2 | 2 | 2 | 2 | 0 | 4 | 2 | 2 | 2 | 2 | 0 | 0.31695721077654515 | 0.31695721077654515 | 0.31695721077654515 | 0.31695721077654515 | 0 | ["react-router-node","server"] |
| @types/api-gateway-proxy | 2 | 17 | 3 | 14 | 8.5 | 8.5 | 7.7781745930520225 | 7 | 2 | 5 | 3.5 | 3.5 | 2.1213203435596424 | 0.31695721077654515 | 0.7923930269413628 | 0.554675118858954 | 0.554675118858954 | 0.33618388962910334 | ["react-router-architect","server"] |
| @types/express | 2 | 18 | 3 | 15 | 9 | 9 | 8.48528137423857 | 6 | 2 | 4 | 3 | 3 | 1.4142135623730951 | 0.31695721077654515 | 0.6339144215530903 | 0.4754358161648177 | 0.4754358161648177 | 0.22412259308606894 | ["server","react-router-express"] |
| @types/express-serve-static-core | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 5 | 2 | 3 | 2.5 | 2.5 | 0.7071067811865476 | 0.31695721077654515 | 0.4754358161648177 | 0.3961965134706814 | 0.3961965134706814 | 0.11206129654303446 | ["server","react-router-express"] |
| @types/handler | 2 | 4 | 2 | 2 | 2 | 2 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["react-router-architect","server"] |
| @types/jsesc | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["vite","plugin"] |
| @types/qs | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 5 | 2 | 3 | 2.5 | 2.5 | 0.7071067811865476 | 0.31695721077654515 | 0.4754358161648177 | 0.3961965134706814 | 0.3961965134706814 | 0.11206129654303446 | ["server","react-router-express"] |
| @types/stream | 2 | 10 | 5 | 5 | 5 | 5 | 0 | 6 | 3 | 3 | 3 | 3 | 0 | 0.4754358161648177 | 0.4754358161648177 | 0.4754358161648177 | 0.4754358161648177 | 0 | ["react-router-node","stream"] |
| async_hooks | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 8 | 4 | 4 | 4 | 4 | 0 | 0.6339144215530903 | 0.6339144215530903 | 0.6339144215530903 | 0.6339144215530903 | 0 | ["react-router","server"] |
| cli | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["cloudflare","cloudflare-dev-proxy"] |
| crypto | 2 | 4 | 2 | 2 | 2 | 2 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["vite","plugin"] |
| esm | 2 | 6 | 1 | 5 | 3 | 3 | 2.8284271247461903 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["config","flatRoutes"] |
| module-runner | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["vite","plugin"] |
| node:crypto | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["vite","plugin"] |
| rollup | 2 | 16 | 8 | 8 | 8 | 8 | 0 | 5 | 2 | 3 | 2.5 | 2.5 | 0.7071067811865476 | 0.31695721077654515 | 0.4754358161648177 | 0.3961965134706814 | 0.3961965134706814 | 0.11206129654303448 | ["vite","plugin"] |
| url | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["vite","plugin"] |
| @types/APIGatewayProxyEventHeaders."content-type | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["server"] |
| @types/APIGatewayProxyEventHeaders."x-forwarded-host | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["server"] |
| @types/events | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["prompts-prompt-base"] |
| @types/isEqual | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["config"] |
| @types/kebabCase | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["plugin"] |
| @types/semver | 1 | 2 | 2 | 2 | 2 | 2 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["run"] |
| @types/timers | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["prompts-select"] |
| arg | 1 | 2 | 2 | 2 | 2 | 2 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["run"] |
| arg.Result."--no-typescript | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["run"] |
| exit-hook | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["commands"] |
| inspector | 1 | 4 | 4 | 4 | 4 | 4 | 0 | 3 | 3 | 3 | 3 | 3 | 0 | 0.4754358161648177 | 0.4754358161648177 | 0.4754358161648177 | 0.4754358161648177 | 0 | ["profiler"] |
| node:child_process | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["config"] |
| node:readline | 1 | 3 | 3 | 3 | 3 | 3 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["prompts-prompt-base"] |
| p-map | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["prerender"] |
| prettier | 1 | 2 | 2 | 2 | 2 | 2 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["useJavascript"] |
| server | 1 | 4 | 4 | 4 | 4 | 4 | 0 | 2 | 2 | 2 | 2 | 2 | 0 | 0.31695721077654515 | 0.31695721077654515 | 0.31695721077654515 | 0.31695721077654515 | 0 | ["vite-node"] |
| types | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0.15847860538827258 | 0 | ["utils"] |

### 3.4 External Module Usage per Internal Module (Sorted)

Which internal TypeScript modules depend on the most external modules?

| internalModuleName | externalModuleName | numberOfExternalDeclarationCaller | numberOfExternalDeclarationCalls | numberOfAllElementsInInternalModule | numberOfAllExternalDeclarationsUsedInInternalModule | numberOfAllExternalModulesUsedInInternalModule | externalDeclarationRate | externalDeclarationNames |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| vite | node | 90 | 152 | 4 | 133 | 25 | 3325 | ["EnvironmentModuleNode.file","PluginOption","isCSSRequest","createLogger","DevEnvironment.name","ResolvedConfig.base","EnvironmentModuleGraph.getModulesByFile","DevEnvironment.moduleGraph","ViteDevServer.environments","DevEnvironment.pluginContainer","Logger.info","ResolvedBuildEnvironmentOptions.outDir","EnvironmentModuleNode.id","HotUpdatePluginContext.environment","ResolvedEnvironmentOptions.build","HotBroadcaster.send","BuildEnvironmentOptions.rollupOptions","UserConfig.base","UserConfig.build","EnvironmentPluginContainer.transform","ViteDevServer.hot","UserConfig.server","normalizePath","UserConfig.logLevel","Logger.error","ResolvedConfig.environments","ResolvedConfig.mode","ViteDevServer","ModuleNode.url","ViteDevServer.transformRequest","isRunnableDevEnvironment","ViteDevServer.pluginContainer","PreviewServer.middlewares","Logger.warn","ResolvedConfig.build","ResolvedConfig.logger","ViteDevServer.middlewares","ResolvedBuildOptions.assetsDir","EnvironmentOptions.resolve","ResolvedConfig","defaultClientConditions","Connect.IncomingMessage.url","ResolvedConfig.configFile","ConfigEnv.isSsrBuild","createServer","ViteDevServer.config","UserConfig.root","RunnableDevEnvironment.runner","ModuleNode.file","ConfigEnv.command","Environment.name","ResolvedConfig.command","ConfigEnv.mode","ManifestChunk.css","ResolvedConfig.server","ViteDevServer.ssrFixStacktrace","Plugin","ManifestChunk.assets","ResolvedConfig.root","ViteDevServer.ssrLoadModule","Connect.Server.use","EnvironmentOptions","UserConfig.plugins","PreviewServer","ResolvedServerOptions.middlewareMode","DevEnvironment.reloadModule","PluginContainer.buildStart","Plugin.name","ManifestChunk.file","EnvironmentOptions.optimizeDeps","loadConfigFromFile","ViteBuilder.build","Environment.config","UserConfig.environments","ViteBuilder.environments","node"] |
| vite | rollup | 8 | 15 | 4 | 133 | 25 | 3325 | ["RollupOptions.onwarn","RollupLog.message","RollupLog.pos","RollupLog.code","TransformPluginContext.environment","PluginContext.resolve","PluginContext.environment","ResolvedId.id"] |
| vite | promises | 7 | 15 | 4 | 133 | 25 | 3325 | ["readFile","rm","rename","mkdir","cp","readdir"] |
| vite | @types/babel__core | 6 | 6 | 4 | 133 | 25 | 3325 | ["transformAsync","BabelFileResult.map","BabelFileResult.code"] |
| vite | @types/path | 6 | 25 | 4 | 133 | 25 | 3325 | ["path.PlatformPath.resolve","path.PlatformPath.join","path.PlatformPath.basename","path.PlatformPath.relative","path.PlatformPath.posix","path.PlatformPath.dirname"] |
| vite | dist | 6 | 10 | 4 | 133 | 25 | 3325 | ["join","resolve","relative","path.normalize","path.dirname","dist"] |
| vite | @types/process | 5 | 9 | 4 | 133 | 25 | 3325 | ["global.NodeJS.ProcessEnv.REACT_ROUTER_ROOT","global.NodeJS.Process.env","global.NodeJS.Process.exit","global.NodeJS.ProcessEnv.IS_RR_BUILD_REQUEST","global.NodeJS.Process.cwd"] |
| vite | fs | 3 | 6 | 4 | 133 | 25 | 3325 | ["Dirent.name","Dirent.isFile","Dirent.path"] |
| vite | node:fs | 3 | 8 | 4 | 133 | 25 | 3325 | ["rmSync","existsSync","readdirSync"] |
| vite | @types/babel__generator | 2 | 2 | 4 | 133 | 25 | 3325 | ["GeneratorResult","GeneratorResult.code"] |
| vite | @types/globals | 2 | 4 | 4 | 133 | 25 | 3325 | ["global.NodeRequire.resolve"] |
| vite | crypto | 2 | 2 | 4 | 133 | 25 | 3325 | ["Hash.update","Hash.digest"] |
| vite | http | 2 | 2 | 4 | 133 | 25 | 3325 | ["ServerResponse.end","ServerResponse.setHeader"] |
| vite | lexer | 2 | 2 | 4 | 133 | 25 | 3325 | ["init"] |
| vite | picocolors | 2 | 13 | 4 | 133 | 25 | 3325 | ["picocolors"] |
| vite | @types/buffer | 1 | 1 | 4 | 133 | 25 | 3325 | ["global.Buffer.toString"] |
| vite | @types/jsesc | 1 | 2 | 4 | 133 | 25 | 3325 | ["jsesc"] |
| vite | @types/pick | 1 | 1 | 4 | 133 | 25 | 3325 | ["pick"] |
| vite | module-runner | 1 | 1 | 4 | 133 | 25 | 3325 | ["ModuleRunner.import"] |
| vite | node:crypto | 1 | 1 | 4 | 133 | 25 | 3325 | ["createHash"] |
| vite | node:url | 1 | 1 | 4 | 133 | 25 | 3325 | [".pathToFileURL"] |
| vite | url | 1 | 1 | 4 | 133 | 25 | 3325 | ["URL.href"] |
| remove-exports | @babel/lib | 16 | 56 | 1 | 23 | 4 | 2300 | ["AssignmentExpression.left","ExportNamedDeclaration.specifiers","FunctionDeclaration.id","ClassDeclaration.id","VariableDeclarator.id","Identifier.name","ExportDefaultDeclaration.declaration","ExpressionStatement.expression","Expression.type","ExportSpecifier.local","ExportDeclaration.type","ExportNamedDeclaration.declaration","MemberExpression.object","LVal.type","VariableDeclaration.declarations","ExportSpecifier.exported"] |
| remove-exports | @types/babel__traverse | 4 | 24 | 1 | 23 | 4 | 2300 | ["NodePath.node","NodePath.isProgram","NodePath.parentPath","NodePath.remove"] |
| remove-exports | dist | 2 | 2 | 1 | 23 | 4 | 2300 | ["findReferencedIdentifiers","deadCodeElimination"] |
| remove-exports | @babel/babel-parser | 1 | 2 | 1 | 23 | 4 | 2300 | ["ParseResult"] |
| with-props | @types/babel__traverse | 11 | 23 | 1 | 21 | 4 | 2100 | ["NodePath.isFunctionDeclaration","NodePath.scope","NodePath.isIdentifier","NodePath.isVariableDeclaration","NodePath.isExportNamedDeclaration","Scope.generateUidIdentifier","NodePath.replaceWith","NodePath.isExpression","NodePath.get","NodePath.isExportDefaultDeclaration","NodePath.node"] |
| with-props | @babel/lib | 8 | 11 | 1 | 21 | 4 | 2100 | ["variableDeclarator","stringLiteral","importSpecifier","Program.body","variableDeclaration","identifier","importDeclaration","callExpression"] |
| with-props | @babel/babel-parser | 2 | 3 | 1 | 21 | 4 | 2100 | ["ParseResult","ParseResult.program"] |
| cloudflare | node | 13 | 18 | 1 | 15 | 3 | 1500 | ["EnvironmentResolveOptions.externalConditions","Connect.Server.use","UserConfig.root","ConfigEnv.mode","ViteDevServer.middlewares","Plugin.name","ResolvedConfig.server","Plugin","ViteDevServer.config","EnvironmentOptions.resolve","ViteDevServer.ssrLoadModule","ResolvedConfig.plugins","ResolvedServerOptions.middlewareMode"] |
| cloudflare | @types/process | 1 | 1 | 1 | 15 | 3 | 1500 | ["global.NodeJS.Process.cwd"] |
| cloudflare | cli | 1 | 2 | 1 | 15 | 3 | 1500 | ["GetPlatformProxyOptions"] |
| cloudflare-dev-proxy | node | 13 | 18 | 1 | 15 | 3 | 1500 | ["EnvironmentResolveOptions.externalConditions","Connect.Server.use","UserConfig.root","ConfigEnv.mode","ViteDevServer.middlewares","Plugin.name","ResolvedConfig.server","Plugin","ViteDevServer.config","EnvironmentOptions.resolve","ViteDevServer.ssrLoadModule","ResolvedConfig.plugins","ResolvedServerOptions.middlewareMode"] |
| cloudflare-dev-proxy | @types/process | 1 | 1 | 1 | 15 | 3 | 1500 | ["global.NodeJS.Process.cwd"] |
| cloudflare-dev-proxy | cli | 1 | 2 | 1 | 15 | 3 | 1500 | ["GetPlatformProxyOptions"] |
| warn-on-client-source-maps | node | 11 | 12 | 1 | 12 | 2 | 1200 | ["ResolvedBuildOptions.sourcemap","Plugin","ResolvedConfig.environments","ResolvedBuildOptions.ssr","ResolvedConfig.mode","ConfigEnv.command","ResolvedConfig.build","ResolvedConfig.logger","Logger.warn","ResolvedEnvironmentOptions.build","ResolvedBuildEnvironmentOptions.sourcemap"] |
| warn-on-client-source-maps | picocolors | 1 | 2 | 1 | 12 | 2 | 1200 | ["picocolors"] |
| run | @types/process | 2 | 4 | 1 | 8 | 5 | 800 | ["global.NodeJS.ProcessVersions.node","global.NodeJS.Process.versions"] |
| run | @types/semver | 2 | 2 | 1 | 8 | 5 | 800 | ["semver","major"] |
| run | arg | 2 | 3 | 1 | 8 | 5 | 800 | ["arg","arg.Result._"] |
| run | @types/globals | 1 | 1 | 1 | 8 | 5 | 800 | ["global.NodeRequire.main"] |
| run | arg.Result."--no-typescript | 1 | 1 | 1 | 8 | 5 | 800 | ["arg.Result.\"--no-typescript\""] |
| plugin | node | 105 | 174 | 18 | 141 | 26 | 783.3333333333333 | ["UserConfig.build","defaultServerConditions","UserConfig.environments","ResolvedConfig","UserConfig","ViteDevServer","ModuleNode","resolveConfig","Plugin","ResolvedConfig.build","ResolvedBuildOptions.manifest","ResolvedConfig.mode","ModuleNode.url","ViteDevServer.transformRequest","isRunnableDevEnvironment","ViteDevServer.pluginContainer","ViteDevServer.environments","PreviewServer.middlewares","ViteDevServer.hot","Logger.warn","UserConfig.base","HotUpdatePluginContext.environment","createLogger","DevEnvironment.name","ResolvedConfig.logger","ViteDevServer.middlewares","ResolvedBuildOptions.assetsDir","EnvironmentOptions.resolve","UserConfig.logLevel","defaultClientConditions","Connect.IncomingMessage.url","UserConfig.server","ResolvedConfig.configFile","ConfigEnv.isSsrBuild","createServer","ViteDevServer.config","UserConfig.root","Logger.info","Logger.error","RunnableDevEnvironment.runner","ModuleNode.file","ConfigEnv.command","HotBroadcaster.send","Environment.name","ResolvedConfig.command","ConfigEnv.mode","ManifestChunk.css","ResolvedConfig.server","ViteDevServer.ssrFixStacktrace","ManifestChunk.assets","ResolvedConfig.root","ViteDevServer.ssrLoadModule","Connect.Server.use","EnvironmentOptions","UserConfig.plugins","PreviewServer","ResolvedServerOptions.middlewareMode","DevEnvironment.reloadModule","PluginContainer.buildStart","Plugin.name","ManifestChunk.file","EnvironmentOptions.optimizeDeps","normalizePath","loadConfigFromFile","ViteBuilder.build","Environment.config","DevEnvironment.moduleGraph","ViteBuilder.environments","ResolvedBuildOptions.emptyOutDir","EnvironmentModuleNode.file","PluginOption","isCSSRequest","ResolvedConfig.base","EnvironmentModuleGraph.getModulesByFile","DevEnvironment.pluginContainer","ResolvedBuildEnvironmentOptions.outDir","EnvironmentModuleNode.id","ResolvedEnvironmentOptions.build","BuildEnvironmentOptions.rollupOptions","EnvironmentPluginContainer.transform","ResolvedConfig.environments"] |
| plugin | @types/path | 17 | 41 | 18 | 141 | 26 | 783.3333333333333 | ["path.PlatformPath.resolve","path.PlatformPath.posix","path.PlatformPath.join","path.PlatformPath.dirname","path.PlatformPath.relative","path.PlatformPath.basename","path.PlatformPath.isAbsolute"] |
| plugin | promises | 10 | 19 | 18 | 141 | 26 | 783.3333333333333 | ["rm","rename","mkdir","cp","readdir","readFile"] |
| plugin | rollup | 10 | 17 | 18 | 141 | 26 | 783.3333333333333 | ["RollupLog.message","RollupLog.code","PluginContext.resolve","PluginContext.environment","ResolvedId.id","RollupOptions.onwarn","RollupLog.pos","TransformPluginContext.environment"] |
| plugin | @types/babel__core | 6 | 6 | 18 | 141 | 26 | 783.3333333333333 | ["BabelFileResult.map","BabelFileResult.code","transformAsync"] |
| plugin | dist | 6 | 10 | 18 | 141 | 26 | 783.3333333333333 | ["join","resolve","relative","path.normalize","path.dirname","dist"] |
| plugin | @types/process | 5 | 9 | 18 | 141 | 26 | 783.3333333333333 | ["global.NodeJS.ProcessEnv.REACT_ROUTER_ROOT","global.NodeJS.Process.env","global.NodeJS.Process.exit","global.NodeJS.ProcessEnv.IS_RR_BUILD_REQUEST","global.NodeJS.Process.cwd"] |
| plugin | node:fs | 5 | 10 | 18 | 141 | 26 | 783.3333333333333 | ["readFileSync","rmSync","existsSync","readdirSync"] |
| plugin | @types/globals | 3 | 5 | 18 | 141 | 26 | 783.3333333333333 | ["global.NodeRequire.resolve"] |
| plugin | fs | 3 | 6 | 18 | 141 | 26 | 783.3333333333333 | ["Dirent.name","Dirent.isFile","Dirent.path"] |
| plugin | picocolors | 3 | 14 | 18 | 141 | 26 | 783.3333333333333 | ["picocolors"] |
| plugin | @types/babel__generator | 2 | 2 | 18 | 141 | 26 | 783.3333333333333 | ["GeneratorResult","GeneratorResult.code"] |
| plugin | crypto | 2 | 2 | 18 | 141 | 26 | 783.3333333333333 | ["Hash.update","Hash.digest"] |
| plugin | http | 2 | 2 | 18 | 141 | 26 | 783.3333333333333 | ["ServerResponse.end","ServerResponse.setHeader"] |
| plugin | lexer | 2 | 2 | 18 | 141 | 26 | 783.3333333333333 | ["init"] |
| plugin | @types/buffer | 1 | 1 | 18 | 141 | 26 | 783.3333333333333 | ["global.Buffer.toString"] |
| plugin | @types/jsesc | 1 | 2 | 18 | 141 | 26 | 783.3333333333333 | ["jsesc"] |
| plugin | @types/kebabCase | 1 | 1 | 18 | 141 | 26 | 783.3333333333333 | ["kebabCase"] |
| plugin | @types/pick | 1 | 1 | 18 | 141 | 26 | 783.3333333333333 | ["pick"] |
| plugin | module-runner | 1 | 1 | 18 | 141 | 26 | 783.3333333333333 | ["ModuleRunner.import"] |
| plugin | node:crypto | 1 | 1 | 18 | 141 | 26 | 783.3333333333333 | ["createHash"] |
| plugin | node:url | 1 | 1 | 18 | 141 | 26 | 783.3333333333333 | [".pathToFileURL"] |
| plugin | url | 1 | 1 | 18 | 141 | 26 | 783.3333333333333 | ["URL.href"] |
| prompts-prompt-base | @types/process | 4 | 52 | 2 | 14 | 6 | 700 | ["global.NodeJS.Process.stdout","global.NodeJS.Process.stdin","global.NodeJS.WriteStream","global.NodeJS.ReadStream"] |
| prompts-prompt-base | node:readline | 3 | 52 | 2 | 14 | 6 | 700 | ["node:readline",".emitKeypressEvents",".createInterface"] |
| prompts-prompt-base | sisteransi | 3 | 39 | 2 | 14 | 6 | 700 | ["cursor","cursor.show","beep"] |
| prompts-prompt-base | node:process | 2 | 78 | 2 | 14 | 6 | 700 | ["node:process"] |
| prompts-prompt-base | readline | 2 | 26 | 2 | 14 | 6 | 700 | ["Key","Interface.close"] |
| prompts-prompt-base | @types/events | 1 | 1 | 2 | 14 | 6 | 700 | ["EventEmitter"] |
| vite-node | node | 8 | 9 | 2 | 13 | 4 | 650 | ["ViteDevServer","ResolvedConfig.base","createServer","ViteDevServer.pluginContainer","ResolvedConfig.root","Logger","PluginContainer.buildStart","ViteDevServer.config"] |
| vite-node | server | 4 | 4 | 2 | 13 | 4 | 650 | ["ViteNodeServer","ViteNodeServer.fetchModule","ViteNodeServer.resolveId","ViteNodeServer.getSourceMap"] |
| vite-node | dist | 1 | 1 | 2 | 13 | 4 | 650 | ["ViteNodeRunner"] |
| useJavascript | @babel/lib | 2 | 2 | 1 | 6 | 5 | 600 | ["lib"] |
| useJavascript | @types/babel__core | 2 | 3 | 1 | 6 | 5 | 600 | ["transformSync","BabelFileResult.code"] |
| useJavascript | prettier | 2 | 2 | 1 | 6 | 5 | 600 | ["format","prettier"] |
| arcTableSessionStorage | @architect/tables | 3 | 5 | 1 | 5 | 2 | 500 | ["ArcTable.delete","ArcTable.put","ArcTable.get"] |
| arcTableSessionStorage | @architect/functions | 2 | 2 | 1 | 5 | 2 | 500 | ["tables","functions"] |
| is-react-router-repo | dist | 4 | 6 | 1 | 5 | 2 | 500 | ["path.dirname","path.basename","path.resolve","dist"] |
| is-react-router-repo | @types/globals | 1 | 1 | 1 | 5 | 2 | 500 | ["global.NodeRequire.resolve"] |
| react-router-fs-routes | @types/path | 2 | 2 | 1 | 5 | 3 | 500 | ["path.PlatformPath.relative","path.PlatformPath.resolve"] |
| react-router-fs-routes | node:fs | 2 | 2 | 1 | 5 | 3 | 500 | [".existsSync","node:fs"] |
| react-router-fs-routes | node:path | 1 | 2 | 1 | 5 | 3 | 500 | ["node:path"] |
| resolve-file-url | @types/path | 4 | 4 | 1 | 5 | 2 | 500 | ["path.PlatformPath.relative","path.PlatformPath.posix","path.PlatformPath.isAbsolute","path.PlatformPath.join"] |
| resolve-file-url | node | 1 | 2 | 1 | 5 | 2 | 500 | ["normalizePath"] |
| fileStorage | promises | 4 | 7 | 2 | 9 | 5 | 450 | [".unlink",".readFile",".writeFile",".mkdir"] |
| fileStorage | @types/buffer | 2 | 2 | 2 | 9 | 5 | 450 | ["global.BufferConstructor.from","global.Buffer.toString"] |
| fileStorage | @types/path | 2 | 3 | 2 | 9 | 5 | 450 | ["path.PlatformPath.dirname","path.PlatformPath.join"] |
| fileStorage | node:fs | 1 | 7 | 2 | 9 | 5 | 450 | ["promises"] |
| load-dotenv | node | 3 | 3 | 1 | 4 | 3 | 400 | ["UserConfig.envDir","loadEnv","UserConfig"] |
| load-dotenv | @types/process | 1 | 1 | 1 | 4 | 3 | 400 | ["global.NodeJS.Process.env"] |
| prompts-text | sisteransi | 7 | 91 | 2 | 8 | 2 | 400 | ["cursor.move","erase.line","cursor.down","erase","cursor.to","cursor.restore","cursor.save"] |
| prompts-text | readline | 1 | 13 | 2 | 8 | 2 | 400 | ["Key"] |
| workersKVStorage | @cloudflare/workers-types | 4 | 6 | 1 | 4 | 1 | 400 | ["KVNamespace.put","KVNamespace.get","Crypto.getRandomValues","KVNamespace.delete"] |
| react-router-cloudflare | @cloudflare/workers-types | 26 | 34 | 6 | 22 | 2 | 366.6666666666667 | ["EventContext.request","EventContext.waitUntil","EventContext.passThroughOnException","Request.cf","KVNamespace.put","KVNamespace.get","Crypto.getRandomValues","KVNamespace.delete","CfProperties","IncomingRequestCfProperties","Request","EventContext","CacheStorage","Response","Request.headers","EventContext.env","Headers.delete","Response.body","Request.clone","Console.error","Request.url","Response.status"] |
| worker | @cloudflare/workers-types | 22 | 28 | 5 | 18 | 2 | 360 | ["Request.headers","EventContext.request","EventContext.env","Headers.delete","Response.body","EventContext","Request.clone","Response","Console.error","Request.url","Response.status","CfProperties","IncomingRequestCfProperties","Request","CacheStorage","EventContext.waitUntil","EventContext.passThroughOnException","Request.cf"] |
| has-rsc-plugin | node | 3 | 3 | 1 | 3 | 2 | 300 | ["ResolvedConfig.plugins","Plugin.name","resolveConfig"] |
| optimize-deps-entries | node | 2 | 2 | 1 | 3 | 2 | 300 | ["normalizePath","version"] |
| optimize-deps-entries | dist | 1 | 1 | 1 | 3 | 2 | 300 | ["escapePath"] |
| profiler | inspector | 5 | 7 | 3 | 9 | 5 | 300 | ["Session","Session.connect",".Session","Session.post"] |
| profiler | node:fs | 2 | 2 | 3 | 9 | 5 | 300 | ["node:fs",".writeFileSync"] |
| profiler | @types/path | 1 | 1 | 3 | 9 | 5 | 300 | ["path.PlatformPath.resolve"] |
| profiler | node:path | 1 | 1 | 3 | 9 | 5 | 300 | ["node:path"] |
| profiler | picocolors | 1 | 3 | 3 | 9 | 5 | 300 | ["picocolors"] |
| resolve-relative-route-file-path | dist | 2 | 2 | 1 | 3 | 2 | 300 | ["dist","path.resolve"] |
| resolve-relative-route-file-path | node | 1 | 1 | 1 | 3 | 2 | 300 | ["normalizePath"] |
| styles | @babel/lib | 6 | 8 | 4 | 12 | 5 | 300 | ["LVal.type","Identifier.name","VariableDeclarator.init","VariableDeclaration.declarations","StringLiteral.value","VariableDeclarator.id"] |
| styles | @types/babel__traverse | 2 | 2 | 4 | 12 | 5 | 300 | ["NodePath.node","NodePath.stop"] |
| styles | @types/path | 2 | 3 | 4 | 12 | 5 | 300 | ["path.PlatformPath.relative","path.PlatformPath.resolve"] |
| styles | @types/process | 1 | 1 | 4 | 12 | 5 | 300 | ["global.NodeJS.Process.cwd"] |
| styles | node | 1 | 2 | 4 | 12 | 5 | 300 | ["ViteDevServer"] |
| validate-plugin-order | node | 3 | 3 | 1 | 3 | 1 | 300 | ["ResolvedConfig.plugins","Plugin","Plugin.name"] |
| dev | node | 9 | 14 | 5 | 13 | 5 | 260 | ["createServer","ViteDevServer.listen","Logger.info","ViteDevServer.printUrls","ResolvedConfig.plugins","ResolvedConfig.logger","ViteDevServer.bindCLIShortcuts","Plugin.name","ViteDevServer.config"] |
| dev | @types/process | 3 | 3 | 5 | 13 | 5 | 260 | ["global.NodeJS.Process.exit","global.NodeJS.ProcessEnv.IS_RR_BUILD_REQUEST","global.NodeJS.Process.env"] |
| dev | picocolors | 1 | 1 | 5 | 13 | 5 | 260 | ["picocolors"] |
| node-adapter | node | 4 | 6 | 2 | 5 | 2 | 250 | ["Connect.IncomingMessage.originalUrl","Connect.IncomingMessage.url","Connect.IncomingMessage"] |
| node-adapter | http | 3 | 3 | 2 | 5 | 2 | 250 | ["ServerResponse","IncomingMessage"] |
| prompts-multi-select | sisteransi | 4 | 52 | 2 | 5 | 2 | 250 | ["erase.line","cursor.hide","cursor.to","erase"] |
| prompts-multi-select | readline | 1 | 13 | 2 | 5 | 2 | 250 | ["Key"] |
| react-router-architect | @types/api-gateway-proxy | 5 | 5 | 4 | 10 | 4 | 250 | ["APIGatewayEventRequestContextV2","APIGatewayProxyEventV2","APIGatewayProxyResultV2"] |
| react-router-architect | @architect/tables | 3 | 5 | 4 | 10 | 4 | 250 | ["ArcTable.delete","ArcTable.put","ArcTable.get"] |
| react-router-architect | @architect/functions | 2 | 2 | 4 | 10 | 4 | 250 | ["tables","functions"] |
| react-router-architect | @types/handler | 2 | 2 | 4 | 10 | 4 | 250 | ["Context","Callback"] |
| react-router-node | @types/stream | 9 | 10 | 7 | 17 | 8 | 242.85714285714286 | ["Stream.Writable.destroy","Stream.Writable.write","Stream.Writable","Stream.Writable.end","Stream.Readable"] |
| react-router-node | @types/buffer | 4 | 4 | 7 | 17 | 8 | 242.85714285714286 | ["global.Buffer.toString","global.BufferConstructor.concat","global.BufferConstructor.from"] |
| react-router-node | promises | 4 | 7 | 7 | 17 | 8 | 242.85714285714286 | [".unlink",".readFile",".writeFile",".mkdir"] |
| react-router-node | @mjackson/node-fetch-server | 2 | 9 | 7 | 17 | 8 | 242.85714285714286 | ["createRequestListener","ClientAddress"] |
| react-router-node | @types/path | 1 | 2 | 7 | 17 | 8 | 242.85714285714286 | ["path.PlatformPath.dirname"] |
| react-router-node | http | 1 | 1 | 7 | 17 | 8 | 242.85714285714286 | ["RequestListener"] |
| react-router-node | node:fs | 1 | 7 | 7 | 17 | 8 | 242.85714285714286 | ["promises"] |
| config | dist | 15 | 43 | 13 | 31 | 15 | 238.46153846153848 | ["PackageJson.dependencies","path.dirname","dist","path.resolve","path.normalize","path.relative","ViteNodeRunner.moduleCache","ModuleCacheMap.clear","path.join"] |
| config | esm | 5 | 6 | 13 | 31 | 15 | 238.46153846153848 | ["_default.watch","esm","FSWatcher.on","FSWatcher.unwatch","FSWatcher.add"] |
| config | node | 5 | 8 | 13 | 31 | 15 | 238.46153846153848 | ["ViteDevServer.close","ModuleGraph.getModuleById","ModuleGraph.invalidateAll","createLogger","ViteDevServer.moduleGraph"] |
| config | @types/process | 3 | 3 | 13 | 31 | 15 | 238.46153846153848 | ["global.NodeJS.Process.env","global.NodeJS.Process.cwd","global.NodeJS.ProcessEnv.REACT_ROUTER_ROOT"] |
| config | @types/globals | 2 | 2 | 13 | 31 | 15 | 238.46153846153848 | ["global.NodeRequire.resolve"] |
| config | fs | 2 | 2 | 13 | 31 | 15 | 238.46153846153848 | ["Stats.isDirectory","Stats.isFile"] |
| config | node:fs | 2 | 2 | 13 | 31 | 15 | 238.46153846153848 | [".statSync","node:fs"] |
| config | @types/isEqual | 1 | 2 | 13 | 31 | 15 | 238.46153846153848 | ["isEqual"] |
| config | @types/pick | 1 | 1 | 13 | 31 | 15 | 238.46153846153848 | ["pick"] |
| config | node:child_process | 1 | 1 | 13 | 31 | 15 | 238.46153846153848 | ["execSync"] |
| config | picocolors | 1 | 1 | 13 | 31 | 15 | 238.46153846153848 | ["picocolors"] |
| commands | @types/path | 3 | 6 | 5 | 10 | 8 | 200 | ["path.PlatformPath.relative","path.PlatformPath.dirname","path.PlatformPath.resolve"] |
| commands | @types/process | 2 | 2 | 5 | 10 | 8 | 200 | ["global.NodeJS.Process.exit"] |
| commands | picocolors | 2 | 6 | 5 | 10 | 8 | 200 | ["picocolors"] |
| commands | @types/globals | 1 | 1 | 5 | 10 | 8 | 200 | ["global.NodeRequire.resolve"] |
| commands | dist | 1 | 1 | 5 | 10 | 8 | 200 | ["PackageJson.dependencies"] |
| commands | exit-hook | 1 | 1 | 5 | 10 | 8 | 200 | ["exit-hook"] |
| commands | node | 1 | 1 | 5 | 10 | 8 | 200 | ["createLogger"] |
| commands | promises | 1 | 2 | 5 | 10 | 8 | 200 | ["writeFile"] |
| loading-indicator | @types/process | 2 | 2 | 1 | 2 | 1 | 200 | ["global.NodeJS.ReadStream","global.NodeJS.WriteStream"] |
| prompts-select | sisteransi | 4 | 52 | 3 | 6 | 3 | 200 | ["erase.line","erase","cursor.to","cursor.hide"] |
| prompts-select | @types/timers | 1 | 13 | 3 | 6 | 3 | 200 | ["global.NodeJS.Timeout"] |
| prompts-select | readline | 1 | 13 | 3 | 6 | 3 | 200 | ["Key"] |
| virtual-route-config | dist | 2 | 2 | 1 | 2 | 1 | 200 | ["path.resolve","dist"] |
| prerender | node | 4 | 4 | 6 | 11 | 5 | 183.33333333333334 | ["ResolvedConfig.root","HttpServer.close","PreviewServer.httpServer","Plugin"] |
| prerender | @types/path | 3 | 3 | 6 | 11 | 5 | 183.33333333333334 | ["path.PlatformPath.dirname","path.PlatformPath.join","path.PlatformPath.relative"] |
| prerender | promises | 2 | 2 | 6 | 11 | 5 | 183.33333333333334 | ["mkdir","writeFile"] |
| prerender | node:path | 1 | 3 | 6 | 11 | 5 | 183.33333333333334 | ["node:path"] |
| prerender | p-map | 1 | 1 | 6 | 11 | 5 | 183.33333333333334 | ["p-map"] |
| stream | @types/stream | 9 | 10 | 4 | 7 | 3 | 175 | ["Stream.Writable.destroy","Stream.Writable.write","Stream.Writable","Stream.Writable.end","Stream.Readable"] |
| stream | @types/buffer | 2 | 2 | 4 | 7 | 3 | 175 | ["global.Buffer.toString","global.BufferConstructor.concat"] |
| prompts-confirm | sisteransi | 4 | 52 | 3 | 5 | 2 | 166.66666666666669 | ["cursor.hide","erase.line","cursor.to","erase"] |
| prompts-confirm | readline | 1 | 13 | 3 | 5 | 2 | 166.66666666666669 | ["Key"] |
| react-router-express | @types/express | 5 | 5 | 3 | 5 | 3 | 166.66666666666669 | ["e.Request","e.NextFunction","e.Response"] |
| react-router-express | @types/express-serve-static-core | 2 | 2 | 3 | 5 | 3 | 166.66666666666669 | ["ParamsDictionary"] |
| react-router-express | @types/qs | 2 | 2 | 3 | 5 | 3 | 166.66666666666669 | ["QueryString.ParsedQs"] |
| typegen | promises | 4 | 4 | 3 | 5 | 3 | 166.66666666666669 | ["promises",".rm"] |
| typegen | picocolors | 2 | 4 | 3 | 5 | 3 | 166.66666666666669 | ["red","green"] |
| typegen | node | 1 | 2 | 3 | 5 | 3 | 166.66666666666669 | ["node"] |
| create-react-router | @types/process | 2 | 26 | 2 | 3 | 2 | 150 | ["global.NodeJS.ReadStream","global.NodeJS.WriteStream"] |
| create-react-router | node:process | 1 | 52 | 2 | 3 | 2 | 150 | ["node:process"] |
| normalizeSlashes | @types/path | 4 | 4 | 2 | 3 | 2 | 150 | ["path.PlatformPath.win32","path.PlatformPath.sep"] |
| normalizeSlashes | node:path | 2 | 2 | 2 | 3 | 2 | 150 | ["node:path"] |
| route-chunks | @babel/lib | 32 | 65 | 12 | 18 | 3 | 150 | ["ImportDeclaration.specifiers","Identifier.name","isExportAllDeclaration","isExportDeclaration","isExportDefaultDeclaration","ExportNamedDeclaration.specifiers","isNodesEquivalent","isExportNamedDeclaration","isImportDeclaration","isClassDeclaration","ExportNamedDeclaration.declaration","isFunctionDeclaration","Program.body","isVariableDeclaration","File.program","VariableDeclaration.declarations"] |
| route-chunks | @types/babel__generator | 5 | 5 | 12 | 18 | 3 | 150 | ["GeneratorResult","GeneratorOptions"] |
| routes | dist | 30 | 96 | 19 | 27 | 4 | 142.10526315789474 | ["resolve","relative","isAbsolute","array","NotValueAction","optional","notValue","lazy","boolean","ObjectSchema","CustomIssue","BaseIssue","object","ArraySchema","custom","SchemaWithPipe","StringSchema","string","pipe","BaseSchema","CustomSchema","LazySchema","OptionalSchema","BooleanSchema","safeParse","flatten"] |
| routes | @types/pick | 3 | 3 | 19 | 27 | 4 | 142.10526315789474 | ["pick"] |
| server | @types/express | 20 | 24 | 40 | 50 | 13 | 125 | ["e.Request.get","e.Request.protocol","e.Request.originalUrl","e.Request","e.Request.hostname","e.Response.on","e.Request.method","e.Response","e.Request.headers","e.Response.status","e.Response.end","e.Response.flushHeaders","e.Response.append","e.Response.statusMessage","e.NextFunction"] |
| server | @types/api-gateway-proxy | 18 | 25 | 40 | 50 | 13 | 125 | ["APIGatewayEventRequestContextV2","APIGatewayProxyEventV2","APIGatewayProxyResultV2","APIGatewayProxyEventV2.body","APIGatewayProxyEventV2.rawQueryString","APIGatewayProxyEventV2.rawPath","APIGatewayProxyEventV2.requestContext","APIGatewayProxyEventV2.headers","APIGatewayProxyEventV2.cookies","APIGatewayEventRequestContextV2.http","APIGatewayProxyEventV2.isBase64Encoded","APIGatewayProxyEventHeaders.host","APIGatewayProxyStructuredResultV2","APIGatewayProxyEventHeaders"] |
| server | @types/react | 6 | 22 | 40 | 50 | 13 | 125 | ["React.Fragment","React.createElement","React.ReactElement","React.ReactNode","React.ComponentClass","React.FunctionComponent"] |
| server | async_hooks | 4 | 4 | 40 | 50 | 13 | 125 | ["AsyncLocalStorage.getStore"] |
| server | @types/express-serve-static-core | 3 | 3 | 40 | 50 | 13 | 125 | ["ParamsDictionary"] |
| server | @types/qs | 3 | 3 | 40 | 50 | 13 | 125 | ["QueryString.ParsedQs"] |
| server | @mjackson/node-fetch-server | 2 | 9 | 40 | 50 | 13 | 125 | ["ClientAddress","createRequestListener"] |
| server | @types/buffer | 2 | 3 | 40 | 50 | 13 | 125 | ["global.Buffer.toString","global.BufferConstructor.from"] |
| server | @types/handler | 2 | 2 | 40 | 50 | 13 | 125 | ["Context","Callback"] |
| server | @types/process | 2 | 2 | 40 | 50 | 13 | 125 | ["global.NodeJS.ProcessEnv.ARC_SANDBOX","global.NodeJS.Process.env"] |
| server | http | 2 | 2 | 40 | 50 | 13 | 125 | ["IncomingHttpHeaders","RequestListener"] |
| server | @types/APIGatewayProxyEventHeaders."content-type | 1 | 1 | 40 | 50 | 13 | 125 | ["APIGatewayProxyEventHeaders.\"content-type\""] |
| server | @types/APIGatewayProxyEventHeaders."x-forwarded-host | 1 | 1 | 40 | 50 | 13 | 125 | ["APIGatewayProxyEventHeaders.\"x-forwarded-host\""] |
| flatRoutes | @types/path | 8 | 18 | 13 | 15 | 5 | 115.38461538461539 | ["path.PlatformPath.join","path.PlatformPath.sep","path.PlatformPath.win32","path.PlatformPath.relative","path.PlatformPath.extname","path.PlatformPath.posix","path.PlatformPath.dirname"] |
| flatRoutes | fs | 3 | 3 | 13 | 15 | 5 | 115.38461538461539 | ["Dirent.isDirectory","Dirent.name","Dirent.isFile"] |
| flatRoutes | node:fs | 3 | 4 | 13 | 15 | 5 | 115.38461538461539 | ["node:fs",".existsSync",".readdirSync"] |
| flatRoutes | node:path | 3 | 13 | 13 | 15 | 5 | 115.38461538461539 | ["node:path"] |
| flatRoutes | esm | 1 | 1 | 13 | 15 | 5 | 115.38461538461539 | ["makeRe"] |
| copy-template | node:url | 2 | 2 | 2 | 2 | 1 | 100 | ["node:url",".fileURLToPath"] |
| detectPackageManager | @types/process | 1 | 1 | 1 | 1 | 1 | 100 | ["global.NodeJS.Process.env"] |
| has-dependency | @types/globals | 1 | 1 | 1 | 1 | 1 | 100 | ["global.NodeRequire.resolve"] |
| virtual-route-modules | @types/babel__generator | 1 | 1 | 4 | 3 | 3 | 75 | ["GeneratorResult"] |
| virtual-route-modules | lexer | 1 | 1 | 4 | 3 | 3 | 75 | ["parse"] |
| virtual-route-modules | node | 1 | 1 | 4 | 3 | 3 | 75 | ["Environment"] |
| cookies | dist | 6 | 18 | 6 | 4 | 2 | 66.66666666666667 | ["ParseOptions","SerializeOptions","serialize","parse"] |
| babel | @types/babel__generator | 1 | 1 | 2 | 1 | 1 | 50 | ["generate"] |
| context | @types/react | 27 | 51 | 21 | 9 | 1 | 42.857142857142854 | ["React.FunctionComponentElement","React.createElement","React.ProviderProps","React.Context.Provider","React.Context","React.createContext","React.useContext","React.ReactNode","React.ReactElement"] |
| generate | dist | 4 | 4 | 5 | 2 | 2 | 40 | ["join"] |
| generate | @types/babel__generator | 1 | 3 | 5 | 2 | 2 | 40 | ["GeneratorResult.code"] |
| sessions | dist | 6 | 32 | 11 | 4 | 1 | 36.36363636363637 | ["SerializeOptions","ParseOptions","SerializeOptions.maxAge","SerializeOptions.expires"] |
| utils | @types/process | 7 | 9 | 144 | 29 | 12 | 20.13888888888889 | ["global.NodeJS.Process.env","global.NodeJS.ProcessEnv.TERM","global.NodeJS.Process.stdout","global.NodeJS.WriteStream","global.NodeJS.Process.stderr"] |
| utils | @types/react | 6 | 27 | 144 | 29 | 12 | 20.13888888888889 | ["React.ComponentClass","React.ReactNode","React.FunctionComponent"] |
| utils | node:fs | 6 | 6 | 144 | 29 | 12 | 20.13888888888889 | [".promises","node:fs"] |
| utils | sisteransi | 5 | 6 | 144 | 29 | 12 | 20.13888888888889 | ["cursor","erase","cursor.to","erase.line","erase.lines"] |
| utils | node:process | 4 | 8 | 144 | 29 | 12 | 20.13888888888889 | ["node:process"] |
| utils | promises | 4 | 4 | 144 | 29 | 12 | 20.13888888888889 | ["readdir",".stat",".mkdir"] |
| utils | readline | 4 | 26 | 144 | 29 | 12 | 20.13888888888889 | ["Key.ctrl","Key.meta","Key.name","Key"] |
| utils | node:path | 3 | 7 | 144 | 29 | 12 | 20.13888888888889 | ["node:path"] |
| utils | @types/path | 2 | 5 | 144 | 29 | 12 | 20.13888888888889 | ["path.PlatformPath.sep"] |
| utils | fs | 2 | 2 | 144 | 29 | 12 | 20.13888888888889 | ["Stats.isFile","Stats.isDirectory"] |
| utils | picocolors | 1 | 39 | 144 | 29 | 12 | 20.13888888888889 | ["picocolors"] |
| utils | types | 1 | 2 | 144 | 29 | 12 | 20.13888888888889 | ["Formatter"] |
| fog-of-war | @types/react | 1 | 1 | 6 | 1 | 1 | 16.666666666666668 | ["React.useEffect"] |
| build | node | 1 | 1 | 7 | 1 | 1 | 14.285714285714286 | ["version"] |
| routeModules | @types/react | 12 | 86 | 21 | 3 | 1 | 14.285714285714285 | ["React.ReactElement","React.FunctionComponent","React.ComponentClass"] |
| react-router | @types/react | 31 | 79 | 179 | 17 | 4 | 9.497206703910614 | ["React.FunctionComponentElement","React.createElement","React.ProviderProps","React.Context.Provider","React.ComponentClass","React.FunctionComponent","React.Fragment","React.ReactElement","React.ReactNode","React.Context","React.createContext","React.useEffect"] |
| react-router | dist | 6 | 18 | 179 | 17 | 4 | 9.497206703910614 | ["ParseOptions","SerializeOptions","serialize","parse"] |
| react-router | async_hooks | 4 | 4 | 179 | 17 | 4 | 9.497206703910614 | ["AsyncLocalStorage.getStore"] |

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
| react | 47 | 0 | ["integration-rsc-vite","@playground/framework-vite-5","@playground/framework-vite-7-beta","@playground/framework","@playground/rsc-vite-framework","@playground/framework-express","@playground/framework","@playground/split-route-modules-spa","@playground/vite-plugin-cloudflare"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-vite-5","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-vite-7-beta","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/middleware"] |
| react-dom | 47 | 0 | ["integration-rsc-vite","@playground/framework-vite-5","@playground/framework-vite-7-beta","@playground/framework","@playground/rsc-vite-framework","@playground/framework-express","@playground/framework","@playground/split-route-modules-spa","@playground/vite-plugin-cloudflare"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-vite-5","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-vite-7-beta","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/middleware"] |
| react-router | 27 | 0 | ["integration-rsc-vite","@playground/framework-vite-5","@playground/framework-vite-7-beta","@playground/framework","@playground/rsc-vite-framework","@playground/framework-express","@playground/framework","@playground/split-route-modules-spa","@playground/vite-plugin-cloudflare"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-vite-5","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-vite-7-beta","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/middleware"] |
| react-router-dom | 23 | 0 | ["search-params","ssr","custom-query-parse-serialization","basic","error-boundaries","ssr-data-router","basic-data-router","auth","custom-link"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/examples/search-params","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/examples/ssr","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/examples/custom-query-parsing","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/examples/basic"] |
| isbot | 21 | 0 | ["@playground/framework-vite-5","@playground/framework-vite-7-beta","@playground/framework","@playground/framework-express","@playground/framework","@playground/split-route-modules-spa","@playground/vite-plugin-cloudflare","@playground/split-route-modules","@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-vite-5","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-vite-7-beta","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-express"] |
| @react-router/node | 20 | 0 | ["@playground/framework-vite-5","@playground/framework-vite-7-beta","@playground/framework","@playground/framework-express","@playground/framework","@playground/split-route-modules-spa","@playground/split-route-modules","@playground/framework-rolldown-vite","@playground/framework-spa"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-vite-5","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-vite-7-beta","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-express"] |
| express | 17 | 0 | ["integration-rsc-vite","@playground/framework","@playground/rsc-vite-framework","@playground/framework-express","@playground/vite-plugin-cloudflare","@playground/rsc-vite","ssr","ssr-data-router","integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/rsc-vite-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-express"] |
| @react-router/serve | 12 | 0 | ["@playground/framework-vite-5","@playground/framework-vite-7-beta","@playground/framework","@playground/split-route-modules","@playground/framework-rolldown-vite","integration-vite-6-template","integration-vite-5-template","integration-vite-7-beta-template","integration-rsc-vite-framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-vite-5","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-vite-7-beta","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/split-route-modules"] |
| compression | 10 | 0 | ["integration-rsc-vite","@playground/framework","@playground/rsc-vite-framework","@playground/framework-express","@playground/rsc-vite","ssr","ssr-data-router","multi-app","@react-router/serve"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/rsc-vite-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-express"] |
| @react-router/express | 8 | 0 | ["@playground/framework","@playground/framework-express","integration","integration-vite-6-template","integration-vite-5-template","@react-router/serve","integration-vite-7-beta-template","integration-vite-rolldown-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-express","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/vite-6-template"] |
| serialize-javascript | 7 | 0 | ["@playground/vite-plugin-cloudflare","integration","integration-vite-6-template","integration-vite-5-template","integration-vite-plugin-cloudflare-template","integration-vite-7-beta-template","integration-vite-rolldown-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/vite-plugin-cloudflare","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/vite-6-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/vite-5-template"] |
| cross-env | 6 | 0 | ["integration-rsc-vite","@playground/framework","@playground/framework-rolldown-vite","ssr","ssr-data-router","multi-app"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-rolldown-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/examples/ssr"] |
| @mjackson/node-fetch-server | 6 | 0 | ["integration-rsc-vite","@playground/rsc-vite-framework","@playground/rsc-vite","@react-router/node","@react-router/serve","integration-rsc-vite-framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/rsc-vite-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-node"] |
| @vanilla-extract/vite-plugin | 5 | 0 | ["integration","integration-vite-6-template","integration-vite-5-template","integration-vite-7-beta-template","integration-vite-rolldown-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/vite-6-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/vite-5-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/vite-7-beta-template"] |
| @vanilla-extract/css | 5 | 0 | ["integration","integration-vite-6-template","integration-vite-5-template","integration-vite-7-beta-template","integration-vite-rolldown-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/vite-6-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/vite-5-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/vite-7-beta-template"] |
| react-server-dom-webpack | 4 | 0 | ["integration-rsc-vite","@playground/rsc-vite-framework","@playground/rsc-vite","integration-rsc-vite-framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/rsc-vite-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/rsc-vite-framework"] |
| semver | 4 | 0 | ["@remix-run/react-router","integration","create-react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| morgan | 3 | 0 | ["@playground/framework","@playground/framework-express","@react-router/serve"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/framework-express","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-serve"] |
| picocolors | 3 | 0 | ["@remix-run/react-router","create-react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| prettier | 3 | 0 | ["@remix-run/react-router","integration","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| @mdx-js/rollup | 2 | 0 | ["@remix-run/react-router","integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| @playwright/test | 2 | 0 | ["@remix-run/react-router","integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| vite | 2 | 0 | ["@remix-run/react-router","integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| @babel/preset-typescript | 2 | 0 | ["@remix-run/react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| @babel/core | 2 | 0 | ["@remix-run/react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| typescript | 2 | 0 | ["@remix-run/react-router","integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| execa | 2 | 0 | ["integration","create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router"] |
| dedent | 2 | 0 | ["integration","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| pathe | 2 | 0 | ["integration","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| get-port | 2 | 0 | ["integration","@react-router/serve"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-serve"] |
| strip-ansi | 2 | 0 | ["integration","create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router"] |
| arg | 2 | 0 | ["create-react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| remix-utils | 1 | 0 | ["@playground/rsc-vite-framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/playground/rsc-vite-framework"] |
| remark-stringify | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| eslint-plugin-jest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| dox | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| babel-plugin-dev-expression | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| prompts | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| @babel/preset-react | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| eslint-plugin-flowtype | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| @types/react-dom | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| eslint-plugin-jsx-a11y | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| remark-gfm | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| eslint-plugin-jsdoc | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| @changesets/cli | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| fast-glob | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| eslint-plugin-react | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| @typescript-eslint/parser | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| eslint-config-react-app | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| unist-util-remove | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| remark-parse | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| typedoc | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| @typescript-eslint/eslint-plugin | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| @types/react-test-renderer | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| eslint-plugin-import | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| @types/react | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| eslint-plugin-react-hooks | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| @remix-run/changelog-github | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| jsonfile | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| @types/jest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| unified | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| @types/jsdom | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| eslint | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| @babel/preset-env | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| babel-jest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| jest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| @manypkg/get-packages | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2"] |
| jsurl | 1 | 0 | ["custom-query-parse-serialization"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/examples/custom-query-parsing"] |
| @remix-run/router | 1 | 0 | ["ssr-data-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/examples/ssr-data-router"] |
| history | 1 | 0 | ["ssr-data-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/examples/ssr-data-router"] |
| @types/dedent | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| strip-indent | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| postcss | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| @types/shelljs | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| shelljs | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| vite-tsconfig-paths | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| @react-router/dev | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| @types/glob | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| @types/cross-spawn | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| postcss-import | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| type-fest | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| vite-env-only | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| cross-spawn | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| @types/wait-on | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| glob | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| @types/semver | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| @types/express | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| cheerio | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| wait-on | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration"] |
| @reach/dialog | 1 | 0 | ["modal-route-with-outlet"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/examples/modal-route-with-outlet"] |
| @reach/visually-hidden | 1 | 0 | ["custom-filter-link"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/examples/custom-filter-link"] |
| localforage | 1 | 0 | ["notes"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/examples/notes"] |
| sort-package-json | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router"] |
| @remix-run/web-fetch | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router"] |
| tar-fs | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router"] |
| sisteransi | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router"] |
| proxy-agent | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router"] |
| gunzip-maybe | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router"] |
| log-update | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router"] |
| not-react-router | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/create-react-router/__tests__/fixtures/basic"] |
| @architect/functions | 1 | 0 | ["@react-router/architect"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-architect"] |
| @types/aws-lambda | 1 | 0 | ["@react-router/architect"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-architect"] |
| pkg-types | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| @babel/plugin-syntax-jsx | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| @babel/parser | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| babel-dead-code-elimination | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| chokidar | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| jsesc | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| tinyglobby | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| valibot | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| vite-node | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| lodash | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| @babel/types | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| exit-hook | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| @remix-run/node-fetch-server | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| @babel/traverse | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| react-refresh | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| es-module-lexer | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| @babel/generator | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| p-map | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-dev"] |
| set-cookie-parser | 1 | 0 | ["react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router"] |
| cookie | 1 | 0 | ["react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router"] |
| source-map-support | 1 | 0 | ["@react-router/serve"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-serve"] |
| minimatch | 1 | 0 | ["@react-router/fs-routes"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/packages/react-router-fs-routes"] |
| match-sorter | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/tutorials/address-book"] |
| sort-by | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/tutorials/address-book"] |
| tiny-invariant | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/tutorials/address-book"] |
| miniflare | 1 | 0 | ["integration-cloudflare-dev-proxy-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/cloudflare-dev-proxy-template"] |
| @react-router/cloudflare | 1 | 0 | ["integration-cloudflare-dev-proxy-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.13.2/./source/react-router-7.13.2/integration/helpers/cloudflare-dev-proxy-template"] |

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
