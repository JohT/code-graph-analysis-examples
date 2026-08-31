---
title: "External Dependencies Report"
generated: "2026-08-31"
model_version: "v4.0.2"
dataset: "react-router-7.18.3"
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
| node | 22 | 30 | 263 | 422 | 140 | 648 | ["<reactRouterRSCVitePlugin> of module <vite> imports <UserConfig.base> from external module <node>","<reactRouterRSCVitePlugin> of module <vite> imports <Logger.error> from external module <node>","<reactRouterRSCVitePlugin> of module <vite> imports <normalizePath> from external module <node>","<reactRouterRSCVitePlugin> of module <vite> imports <PluginOption> from external module <node>"] |
| @types/process | 19 | 21 | 48 | 97 | 140 | 648 | ["<getBuildTimeHeader> of module <dev> imports <global.NodeJS.ProcessEnv.hasOwnProperty> from external module <process>","<getBuildTimeHeader> of module <dev> imports <global.NodeJS.Process.env> from external module <process>","<getBuildTimeHeader> of module <dev> imports <global.NodeJS.ProcessEnv.IS_RR_BUILD_REQUEST> from external module <process>","<Context> of module <create-react-router> imports <global.NodeJS.ReadStream> from external module <process>"] |
| dist | 17 | 27 | 104 | 373 | 140 | 648 | ["<CookieOptions> of module <react-router> imports <ParseOptions> from external module <dist>","<CookieOptions> of module <react-router> imports <StringifyOptions> from external module <dist>","<CookieOptions> of module <react-router> imports <ParseOptions> from external module <dist>","<CookieOptions> of module <react-router> imports <StringifyOptions> from external module <dist>"] |
| @types/path | 14 | 20 | 55 | 122 | 140 | 648 | ["<normalizeSlashes> of module <normalizeSlashes> imports <path.PlatformPath.win32> from external module <path>","<normalizeSlashes> of module <normalizeSlashes> imports <path.PlatformPath.sep> from external module <path>","<flatRoutesUniversal> of module <flatRoutes> imports <path.PlatformPath.dirname> from external module <path>","<flatRoutesUniversal> of module <flatRoutes> imports <path.PlatformPath.relative> from external module <path>"] |
| node:fs | 10 | 12 | 26 | 49 | 140 | 648 | ["<flatRoutes> of module <flatRoutes> imports <.existsSync> from external module <node:fs>","<flatRoutes> of module <flatRoutes> imports <.readdirSync> from external module <node:fs>","<flatRoutes> of module <flatRoutes> imports <node:fs> from external module <node:fs>","<flatRoutes> of module <react-router-fs-routes> imports <.existsSync> from external module <node:fs>"] |
| picocolors | 10 | 11 | 14 | 85 | 140 | 648 | ["<color> of module <utils> imports <picocolors> from external module <picocolors>","<reactRouterRSCVitePlugin> of module <vite> imports <picocolors> from external module <picocolors>","<reactRouterRSCVitePlugin> of module <plugin> imports <picocolors> from external module <picocolors>","<reactRouterVitePlugin> of module <vite> imports <picocolors> from external module <picocolors>"] |
| promises | 9 | 13 | 37 | 59 | 140 | 648 | ["<fileExists> of module <utils> imports <.stat> from external module <promises>","<getDirectoryFilesRecursive> of module <utils> imports <readdir> from external module <promises>","<directoryExists> of module <utils> imports <.stat> from external module <promises>","<ensureDirectory> of module <utils> imports <.mkdir> from external module <promises>"] |
| @types/react | 8 | 24 | 91 | 390 | 140 | 648 | ["<AwaitContextProvider> of module <react-router> imports <React.Context.Provider> from external module <react>","<AwaitContextProvider> of module <react-router> imports <React.createElement> from external module <react>","<AwaitContextProvider> of module <react-router> imports <React.ProviderProps> from external module <react>","<AwaitContextProvider> of module <react-router> imports <React.FunctionComponentElement> from external module <react>"] |
| @types/module | 7 | 8 | 9 | 11 | 140 | 648 | ["<reactRouterVitePlugin> of module <vite> imports <global.NodeJS.Require.resolve> from external module <module>","<reactRouterVitePlugin> of module <plugin> imports <global.NodeJS.Require.resolve> from external module <module>","<generateEntry> of module <commands> imports <global.NodeJS.Require.resolve> from external module <module>","<run> of module <run> imports <global.NodeJS.Require.main> from external module <module>"] |
| http | 7 | 6 | 16 | 22 | 140 | 648 | ["<createRemixHeaders> of module <server> imports <IncomingHttpHeaders> from external module <http>","<reactRouterRSCVitePlugin> of module <vite> imports <ServerResponse.end> from external module <http>","<reactRouterRSCVitePlugin> of module <vite> imports <ServerResponse.setHeader> from external module <http>","<reactRouterRSCVitePlugin> of module <vite> imports <ServerResponse.statusCode> from external module <http>"] |
| node:path | 7 | 11 | 11 | 28 | 140 | 648 | ["<normalizeSlashes> of module <normalizeSlashes> imports <node:path> from external module <node:path>","<flatRoutesUniversal> of module <flatRoutes> imports <node:path> from external module <node:path>","<isSegmentSeparator> of module <flatRoutes> imports <node:path> from external module <node:path>","<flatRoutes> of module <flatRoutes> imports <node:path> from external module <node:path>"] |
| @types/babel__generator | 6 | 8 | 13 | 15 | 140 | 648 | ["<reactRouterVitePlugin> of module <vite> imports <GeneratorResult.code> from external module <babel__generator>","<reactRouterVitePlugin> of module <vite> imports <GeneratorResult> from external module <babel__generator>","<reactRouterVitePlugin> of module <plugin> imports <GeneratorResult.code> from external module <babel__generator>","<reactRouterVitePlugin> of module <plugin> imports <GeneratorResult> from external module <babel__generator>"] |
| @types/buffer | 6 | 4 | 12 | 13 | 140 | 648 | ["<reactRouterVitePlugin> of module <vite> imports <global.NonSharedBuffer.toString> from external module <buffer>","<reactRouterVitePlugin> of module <plugin> imports <global.NonSharedBuffer.toString> from external module <buffer>","<createReactRouterRequest> of module <server> imports <global.BufferConstructor.from> from external module <buffer>","<createReactRouterRequest> of module <server> imports <global.Buffer.toString> from external module <buffer>"] |
| fs | 6 | 6 | 17 | 27 | 140 | 648 | ["<flatRoutes> of module <flatRoutes> imports <Dirent.isDirectory> from external module <fs>","<flatRoutes> of module <flatRoutes> imports <Dirent.isFile> from external module <fs>","<flatRoutes> of module <flatRoutes> imports <Dirent.name> from external module <fs>","<fileExists> of module <utils> imports <Stats.isFile> from external module <fs>"] |
| readline | 6 | 6 | 10 | 56 | 140 | 648 | ["<ConfirmPrompt> of module <prompts-confirm> imports <Key> from external module <readline>","<MultiSelectPrompt> of module <prompts-multi-select> imports <Key> from external module <readline>","<Prompt> of module <prompts-prompt-base> imports <Interface.close> from external module <readline>","<Prompt> of module <prompts-prompt-base> imports <Key> from external module <readline>"] |
| sisteransi | 6 | 6 | 27 | 116 | 140 | 648 | ["<ConfirmPrompt> of module <prompts-confirm> imports <cursor.hide> from external module <sisteransi>","<ConfirmPrompt> of module <prompts-confirm> imports <cursor.to> from external module <sisteransi>","<ConfirmPrompt> of module <prompts-confirm> imports <erase> from external module <sisteransi>","<ConfirmPrompt> of module <prompts-confirm> imports <erase.line> from external module <sisteransi>"] |
| @babel/lib | 5 | 7 | 65 | 143 | 140 | 648 | ["<transpile> of module <useJavascript> imports <lib> from external module <lib>","<transpile> of module <useJavascript> imports <lib> from external module <lib>","<removeExports> of module <remove-exports> imports <ExportDefaultDeclaration.declaration> from external module <lib>","<removeExports> of module <remove-exports> imports <ExpressionStatement.expression> from external module <lib>"] |
| @types/pick | 5 | 5 | 9 | 9 | 140 | 648 | ["<layout> of module <routes> imports <pick> from external module <pick>","<layout> of module <routes> imports <pick> from external module <pick>","<index> of module <routes> imports <pick> from external module <pick>","<index> of module <routes> imports <pick> from external module <pick>"] |
| lexer | 4 | 3 | 6 | 6 | 140 | 648 | ["<reactRouterRSCVitePlugin> of module <vite> imports <init> from external module <lexer>","<reactRouterRSCVitePlugin> of module <plugin> imports <init> from external module <lexer>","<reactRouterVitePlugin> of module <vite> imports <init> from external module <lexer>","<reactRouterVitePlugin> of module <plugin> imports <init> from external module <lexer>"] |
| @cloudflare/workers-types | 3 | 5 | 52 | 68 | 140 | 648 | ["<createRequestHandler> of module <worker> imports <EventContext.waitUntil> from external module <workers-types>","<createRequestHandler> of module <worker> imports <EventContext.passThroughOnException> from external module <workers-types>","<createRequestHandler> of module <worker> imports <Request.cf> from external module <workers-types>","<createRequestHandler> of module <worker> imports <EventContext.request> from external module <workers-types>"] |
| @types/babel__core | 3 | 2 | 8 | 9 | 140 | 648 | ["<reactRouterVitePlugin> of module <vite> imports <BabelFileResult.code> from external module <babel__core>","<reactRouterVitePlugin> of module <vite> imports <transformAsync> from external module <babel__core>","<reactRouterVitePlugin> of module <vite> imports <BabelFileResult.map> from external module <babel__core>","<reactRouterVitePlugin> of module <plugin> imports <BabelFileResult.code> from external module <babel__core>"] |
| @types/babel__traverse | 3 | 3 | 17 | 49 | 140 | 648 | ["<removeExports> of module <remove-exports> imports <NodePath.node> from external module <babel__traverse>","<removeExports> of module <remove-exports> imports <NodePath.remove> from external module <babel__traverse>","<removeExports> of module <remove-exports> imports <NodePath.isProgram> from external module <babel__traverse>","<removeExports> of module <remove-exports> imports <NodePath.parentPath> from external module <babel__traverse>"] |
| node:process | 3 | 7 | 7 | 58 | 140 | 648 | ["<Context> of module <create-react-router> imports <node:process> from external module <node:process>","<Prompt> of module <prompts-prompt-base> imports <node:process> from external module <node:process>","<PromptOptions> of module <prompts-prompt-base> imports <node:process> from external module <node:process>","<log> of module <utils> imports <node:process> from external module <node:process>"] |
| node:url | 3 | 2 | 4 | 6 | 140 | 648 | ["<copyTemplate> of module <copy-template> imports <.fileURLToPath> from external module <node:url>","<copyTemplate> of module <copy-template> imports <node:url> from external module <node:url>","<reactRouterVitePlugin> of module <vite> imports <.pathToFileURL> from external module <node:url>","<reactRouterVitePlugin> of module <plugin> imports <.pathToFileURL> from external module <node:url>"] |
| @architect/functions | 2 | 1 | 4 | 4 | 140 | 648 | ["<createArcTableSessionStorage> of module <react-router-architect> imports <functions> from external module <functions>","<createArcTableSessionStorage> of module <react-router-architect> imports <tables> from external module <functions>","<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <functions> from external module <functions>","<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <tables> from external module <functions>"] |
| @architect/tables | 2 | 1 | 6 | 10 | 140 | 648 | ["<createArcTableSessionStorage> of module <react-router-architect> imports <ArcTable.get> from external module <tables>","<createArcTableSessionStorage> of module <react-router-architect> imports <ArcTable.delete> from external module <tables>","<createArcTableSessionStorage> of module <react-router-architect> imports <ArcTable.put> from external module <tables>","<createArcTableSessionStorage> of module <arcTableSessionStorage> imports <ArcTable.get> from external module <tables>"] |
| @babel/babel-parser | 2 | 2 | 3 | 5 | 140 | 648 | ["<removeExports> of module <remove-exports> imports <ParseResult> from external module <babel-parser>","<decorateComponentExportsWithProps> of module <with-props> imports <ParseResult.program> from external module <babel-parser>","<decorateComponentExportsWithProps> of module <with-props> imports <ParseResult> from external module <babel-parser>"] |
| @mjackson/node-fetch-server | 2 | 2 | 4 | 4 | 140 | 648 | ["<createRequestListener> of module <react-router-node> imports <createRequestListener> from external module <node-fetch-server>","<createRequestListener> of module <server> imports <createRequestListener> from external module <node-fetch-server>","<RequestListenerOptions> of module <server> imports <ClientAddress> from external module <node-fetch-server>","<RequestListenerOptions> of module <react-router-node> imports <ClientAddress> from external module <node-fetch-server>"] |
| @types/api-gateway-proxy | 2 | 5 | 24 | 34 | 140 | 648 | ["<RequestHandler> of module <server> imports <APIGatewayEventRequestContextV2> from external module <api-gateway-proxy>","<RequestHandler> of module <server> imports <APIGatewayProxyResultV2> from external module <api-gateway-proxy>","<RequestHandler> of module <server> imports <APIGatewayProxyEventV2> from external module <api-gateway-proxy>","<RequestHandler> of module <react-router-architect> imports <APIGatewayEventRequestContextV2> from external module <api-gateway-proxy>"] |
| @types/express | 2 | 4 | 26 | 30 | 140 | 648 | ["<RequestHandler> of module <react-router-express> imports <e.Response> from external module <express>","<RequestHandler> of module <react-router-express> imports <e.NextFunction> from external module <express>","<RequestHandler> of module <react-router-express> imports <e.Request> from external module <express>","<RequestHandler> of module <server> imports <e.Response> from external module <express>"] |
| @types/express-serve-static-core | 2 | 3 | 6 | 6 | 140 | 648 | ["<RequestHandler> of module <react-router-express> imports <ParamsDictionary> from external module <express-serve-static-core>","<RequestHandler> of module <server> imports <ParamsDictionary> from external module <express-serve-static-core>","<GetLoadContextFunction> of module <server> imports <ParamsDictionary> from external module <express-serve-static-core>","<GetLoadContextFunction> of module <react-router-express> imports <ParamsDictionary> from external module <express-serve-static-core>"] |
| @types/handler | 2 | 1 | 4 | 4 | 140 | 648 | ["<RequestHandler> of module <server> imports <Context> from external module <handler>","<RequestHandler> of module <server> imports <Callback> from external module <handler>","<RequestHandler> of module <react-router-architect> imports <Context> from external module <handler>","<RequestHandler> of module <react-router-architect> imports <Callback> from external module <handler>"] |
| @types/jsesc | 2 | 1 | 2 | 4 | 140 | 648 | ["<reactRouterVitePlugin> of module <vite> imports <jsesc> from external module <jsesc>","<reactRouterVitePlugin> of module <plugin> imports <jsesc> from external module <jsesc>"] |
| @types/qs | 2 | 3 | 5 | 5 | 140 | 648 | ["<RequestHandler> of module <react-router-express> imports <QueryString.ParsedQs> from external module <qs>","<RequestHandler> of module <server> imports <QueryString.ParsedQs> from external module <qs>","<GetLoadContextFunction> of module <server> imports <QueryString.ParsedQs> from external module <qs>","<GetLoadContextFunction> of module <react-router-express> imports <QueryString.ParsedQs> from external module <qs>"] |
| @types/stream | 2 | 3 | 14 | 16 | 140 | 648 | ["<createReadableStreamFromReadable> of module <react-router-node> imports <Stream.Readable> from external module <stream>","<createReadableStreamFromReadable> of module <stream> imports <Stream.Readable> from external module <stream>","<writeReadableStreamToWritable> of module <react-router-node> imports <Stream.Writable.write> from external module <stream>","<writeReadableStreamToWritable> of module <react-router-node> imports <Stream.Writable.end> from external module <stream>"] |
| async_hooks | 2 | 4 | 8 | 8 | 140 | 648 | ["<getRequest> of module <react-router> imports <AsyncLocalStorage.getStore> from external module <async_hooks>","<getRequest> of module <server> imports <AsyncLocalStorage.getStore> from external module <async_hooks>","<redirectDocument> of module <react-router> imports <AsyncLocalStorage.getStore> from external module <async_hooks>","<redirectDocument> of module <server> imports <AsyncLocalStorage.getStore> from external module <async_hooks>"] |
| cli | 2 | 1 | 2 | 4 | 140 | 648 | ["<cloudflareDevProxyVitePlugin> of module <cloudflare-dev-proxy> imports <GetPlatformProxyOptions> from external module <cli>","<cloudflareDevProxyVitePlugin> of module <cloudflare> imports <GetPlatformProxyOptions> from external module <cli>"] |
| crypto | 2 | 1 | 4 | 4 | 140 | 648 | ["<reactRouterVitePlugin> of module <vite> imports <Hash.digest> from external module <crypto>","<reactRouterVitePlugin> of module <vite> imports <Hash.update> from external module <crypto>","<reactRouterVitePlugin> of module <plugin> imports <Hash.digest> from external module <crypto>","<reactRouterVitePlugin> of module <plugin> imports <Hash.update> from external module <crypto>"] |
| esm | 2 | 2 | 6 | 7 | 140 | 648 | ["<flatRoutes> of module <flatRoutes> imports <makeRe> from external module <esm>","<createConfigLoader> of module <config> imports <_default.watch> from external module <esm>","<createConfigLoader> of module <config> imports <FSWatcher.add> from external module <esm>","<createConfigLoader> of module <config> imports <FSWatcher.unwatch> from external module <esm>"] |
| module-runner | 2 | 1 | 2 | 2 | 140 | 648 | ["<reactRouterVitePlugin> of module <vite> imports <ModuleRunner.import> from external module <module-runner>","<reactRouterVitePlugin> of module <plugin> imports <ModuleRunner.import> from external module <module-runner>"] |
| node:crypto | 2 | 1 | 2 | 2 | 140 | 648 | ["<reactRouterVitePlugin> of module <vite> imports <createHash> from external module <node:crypto>","<reactRouterVitePlugin> of module <plugin> imports <createHash> from external module <node:crypto>"] |
| rollup | 2 | 1 | 6 | 10 | 140 | 648 | ["<reactRouterVitePlugin> of module <vite> imports <ResolvedId.id> from external module <rollup>","<reactRouterVitePlugin> of module <vite> imports <PluginContext.environment> from external module <rollup>","<reactRouterVitePlugin> of module <vite> imports <PluginContext.resolve> from external module <rollup>","<reactRouterVitePlugin> of module <plugin> imports <ResolvedId.id> from external module <rollup>"] |
| url | 2 | 1 | 2 | 4 | 140 | 648 | ["<reactRouterVitePlugin> of module <vite> imports <URL.href> from external module <url>","<reactRouterVitePlugin> of module <plugin> imports <URL.href> from external module <url>"] |
| @types/APIGatewayProxyEventHeaders."content-type | 1 | 1 | 1 | 1 | 140 | 648 | ["<createReactRouterRequest> of module <server> imports <APIGatewayProxyEventHeaders.\"content-type\"> from external module <APIGatewayProxyEventHeaders.\"content-type>"] |
| @types/APIGatewayProxyEventHeaders."x-forwarded-host | 1 | 1 | 1 | 1 | 140 | 648 | ["<createReactRouterRequest> of module <server> imports <APIGatewayProxyEventHeaders.\"x-forwarded-host\"> from external module <APIGatewayProxyEventHeaders.\"x-forwarded-host>"] |
| @types/events | 1 | 1 | 1 | 1 | 140 | 648 | ["<Prompt> of module <prompts-prompt-base> imports <EventEmitter> from external module <events>"] |
| @types/isEqual | 1 | 1 | 1 | 2 | 140 | 648 | ["<createConfigLoader> of module <config> imports <isEqual> from external module <isEqual>"] |
| @types/kebabCase | 1 | 1 | 1 | 1 | 140 | 648 | ["<getEnvironmentOptionsResolvers> of module <plugin> imports <kebabCase> from external module <kebabCase>"] |
| @types/semver | 1 | 1 | 2 | 2 | 140 | 648 | ["<run> of module <run> imports <semver> from external module <semver>","<run> of module <run> imports <major> from external module <semver>"] |
| @types/timers | 1 | 1 | 1 | 5 | 140 | 648 | ["<SelectPrompt> of module <prompts-select> imports <global.NodeJS.Timeout> from external module <timers>"] |
| arg | 1 | 1 | 2 | 3 | 140 | 648 | ["<run> of module <run> imports <arg.Result._> from external module <arg>","<run> of module <run> imports <arg> from external module <arg>"] |
| arg.Result."--no-typescript | 1 | 1 | 1 | 1 | 140 | 648 | ["<run> of module <run> imports <arg.Result.\"--no-typescript\"> from external module <arg.Result.\"--no-typescript>"] |
| exit-hook | 1 | 1 | 1 | 1 | 140 | 648 | ["<dev> of module <commands> imports <exit-hook> from external module <exit-hook>"] |
| inspector | 1 | 3 | 4 | 6 | 140 | 648 | ["<stop> of module <profiler> imports <Session.post> from external module <inspector>","<start> of module <profiler> imports <Session.connect> from external module <inspector>","<start> of module <profiler> imports <Session.post> from external module <inspector>","<getSession> of module <profiler> imports <Session> from external module <inspector>"] |
| node:child_process | 1 | 1 | 1 | 1 | 140 | 648 | ["<resolveEntryFiles> of module <config> imports <execSync> from external module <node:child_process>"] |
| node:inspector | 1 | 1 | 1 | 1 | 140 | 648 | ["<start> of module <profiler> imports <.Session> from external module <node:inspector>"] |
| node:readline | 1 | 1 | 3 | 20 | 140 | 648 | ["<Prompt> of module <prompts-prompt-base> imports <.emitKeypressEvents> from external module <node:readline>","<Prompt> of module <prompts-prompt-base> imports <.createInterface> from external module <node:readline>","<Prompt> of module <prompts-prompt-base> imports <node:readline> from external module <node:readline>"] |
| p-map | 1 | 1 | 1 | 1 | 140 | 648 | ["<prerender> of module <prerender> imports <p-map> from external module <p-map>"] |
| prettier | 1 | 1 | 2 | 2 | 140 | 648 | ["<transpile> of module <useJavascript> imports <prettier> from external module <prettier>","<transpile> of module <useJavascript> imports <format> from external module <prettier>"] |
| server | 1 | 2 | 4 | 4 | 140 | 648 | ["<createContext> of module <vite-node> imports <ViteNodeServer.fetchModule> from external module <server>","<createContext> of module <vite-node> imports <ViteNodeServer.resolveId> from external module <server>","<createContext> of module <vite-node> imports <ViteNodeServer.getSourceMap> from external module <server>","<Context> of module <vite-node> imports <ViteNodeServer> from external module <server>"] |
| types | 1 | 1 | 1 | 2 | 140 | 648 | ["<color> of module <utils> imports <Formatter> from external module <types>"] |

### 3.2 Most Used External Namespaces

Groups by namespace to reveal declaration-level coupling within npm packages.

| externalNamespaceName | numberOfExternalCallerModules | numberOfExternalCallerElements | numberOfExternalDeclarationCalls | numberOfExternalDeclarationCallsWeighted | allModules | allInternalElements | exampleStories |
| --- | --- | --- | --- | --- | --- | --- | --- |
| no namespace | 53 | 97 | 595 | 1390 | 140 | 648 | ["<CookieOptions> of module <react-router> imports <ParseOptions> from external namespace <>","<CookieOptions> of module <react-router> imports <StringifyOptions> from external namespace <>","<CookieOptions> of module <react-router> imports <ParseOptions> from external namespace <>","<CookieOptions> of module <react-router> imports <StringifyOptions> from external namespace <>"] |
| @types | 51 | 94 | 351 | 827 | 140 | 648 | ["<AwaitContextProvider> of module <react-router> imports <React.Context.Provider> from external namespace <@types>","<AwaitContextProvider> of module <react-router> imports <React.createElement> from external namespace <@types>","<AwaitContextProvider> of module <react-router> imports <React.ProviderProps> from external namespace <@types>","<AwaitContextProvider> of module <react-router> imports <React.FunctionComponentElement> from external namespace <@types>"] |
| @babel | 5 | 7 | 68 | 148 | 140 | 648 | ["<transpile> of module <useJavascript> imports <lib> from external namespace <@babel>","<transpile> of module <useJavascript> imports <lib> from external namespace <@babel>","<removeExports> of module <remove-exports> imports <ExportDefaultDeclaration.declaration> from external namespace <@babel>","<removeExports> of module <remove-exports> imports <ExpressionStatement.expression> from external namespace <@babel>"] |
| @cloudflare | 3 | 5 | 52 | 68 | 140 | 648 | ["<createRequestHandler> of module <worker> imports <EventContext.waitUntil> from external namespace <@cloudflare>","<createRequestHandler> of module <worker> imports <EventContext.passThroughOnException> from external namespace <@cloudflare>","<createRequestHandler> of module <worker> imports <Request.cf> from external namespace <@cloudflare>","<createRequestHandler> of module <worker> imports <EventContext.request> from external namespace <@cloudflare>"] |
| @architect | 2 | 1 | 10 | 14 | 140 | 648 | ["<createArcTableSessionStorage> of module <react-router-architect> imports <functions> from external namespace <@architect>","<createArcTableSessionStorage> of module <react-router-architect> imports <ArcTable.get> from external namespace <@architect>","<createArcTableSessionStorage> of module <react-router-architect> imports <tables> from external namespace <@architect>","<createArcTableSessionStorage> of module <react-router-architect> imports <ArcTable.delete> from external namespace <@architect>"] |
| @mjackson | 2 | 2 | 4 | 4 | 140 | 648 | ["<createRequestListener> of module <react-router-node> imports <createRequestListener> from external namespace <@mjackson>","<createRequestListener> of module <server> imports <createRequestListener> from external namespace <@mjackson>","<RequestListenerOptions> of module <server> imports <ClientAddress> from external namespace <@mjackson>","<RequestListenerOptions> of module <react-router-node> imports <ClientAddress> from external namespace <@mjackson>"] |

### 3.3 Most Spread External Modules

External modules referenced from the highest number of **different internal TypeScript modules**.

| externalModuleName | numberOfInternalModules | sumNumberOfUsedExternalDeclarations | minNumberOfUsedExternalDeclarations | maxNumberOfUsedExternalDeclarations | medNumberOfUsedExternalDeclarations | avgNumberOfUsedExternalDeclarations | stdNumberOfUsedExternalDeclarations | sumNumberOfInternalElements | minNumberOfInternalElements | maxNumberOfInternalElements | medNumberOfInternalElements | avgNumberOfInternalElements | stdNumberOfInternalElements | minNumberOfInternalElementsPercentage | maxNumberOfInternalElementsPercentage | medNumberOfInternalElementsPercentage | avgNumberOfInternalElementsPercentage | stdNumberOfInternalElementsPercentage | internalModuleExamples |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| node | 20 | 231 | 1 | 76 | 3 | 11.55 | 21.91004335915381 | 33 | 1 | 8 | 1 | 1.65 | 1.7554426642213128 | 0.15432098765432098 | 1.2345679012345678 | 0.15432098765432098 | 0.25462962962962965 | 0.27090164571316555 | ["vite","plugin","commands","config"] |
| @types/process | 17 | 42 | 1 | 5 | 2 | 2.4705882352941178 | 1.5458673560021057 | 24 | 1 | 4 | 1 | 1.411764705882353 | 0.7952062255644572 | 0.15432098765432098 | 0.6172839506172839 | 0.15432098765432098 | 0.2178649237472767 | 0.12271701011797181 | ["dev","create-react-router","loading-indicator","prompts-prompt-base"] |
| dist | 15 | 80 | 1 | 26 | 4 | 5.333333333333334 | 6.309478885734052 | 31 | 1 | 5 | 1 | 2.0666666666666664 | 1.4375905768565218 | 0.15432098765432098 | 0.7716049382716049 | 0.15432098765432098 | 0.3189300411522633 | 0.22185039766304343 | ["react-router","cookies","sessions","routes"] |
| @types/path | 13 | 41 | 1 | 7 | 2 | 3.1538461538461537 | 2.192645048267573 | 22 | 1 | 5 | 1 | 1.6923076923076923 | 1.1821319289469756 | 0.15432098765432098 | 0.7716049382716049 | 0.15432098765432098 | 0.26115859449192774 | 0.18242776681280484 | ["normalizeSlashes","flatRoutes","react-router-fs-routes","utils"] |
| node:fs | 10 | 21 | 1 | 4 | 2 | 2.1 | 0.9944289260117533 | 14 | 1 | 3 | 1 | 1.4 | 0.8432740427115678 | 0.15432098765432098 | 0.4629629629629629 | 0.15432098765432098 | 0.21604938271604934 | 0.13013488313450117 | ["flatRoutes","react-router-fs-routes","utils","vite"] |
| picocolors | 9 | 10 | 1 | 2 | 1 | 1.1111111111111114 | 0.33333333333333337 | 13 | 1 | 3 | 1 | 1.4444444444444444 | 0.7264831572567788 | 0.15432098765432098 | 0.4629629629629629 | 0.15432098765432098 | 0.22290809327846361 | 0.11211159834209551 | ["utils","vite","plugin","commands"] |
| promises | 8 | 31 | 2 | 7 | 3.5 | 3.875 | 2.1001700611413083 | 16 | 1 | 4 | 1.5 | 2 | 1.3093073414159542 | 0.15432098765432098 | 0.6172839506172839 | 0.23148148148148145 | 0.30864197530864196 | 0.2020536020703633 | ["utils","vite","plugin","commands"] |
| @types/module | 7 | 7 | 1 | 1 | 1 | 1 | 0 | 9 | 1 | 2 | 1 | 1.2857142857142856 | 0.4879500364742666 | 0.15432098765432098 | 0.30864197530864196 | 0.15432098765432098 | 0.19841269841269837 | 0.07530093155467077 | ["vite","plugin","commands","run"] |
| @types/babel__generator | 6 | 10 | 1 | 2 | 2 | 1.6666666666666667 | 0.5163977794943222 | 9 | 1 | 3 | 1 | 1.5 | 0.8366600265340756 | 0.15432098765432098 | 0.4629629629629629 | 0.15432098765432098 | 0.23148148148148145 | 0.12911420162562892 | ["vite","plugin","generate","babel"] |
| @types/buffer | 6 | 11 | 1 | 3 | 2 | 1.8333333333333335 | 0.752772652709081 | 7 | 1 | 2 | 1 | 1.1666666666666665 | 0.408248290463863 | 0.15432098765432098 | 0.30864197530864196 | 0.15432098765432098 | 0.18004115226337447 | 0.06300127939257145 | ["vite","plugin","server","react-router-node"] |
| @types/react | 6 | 34 | 1 | 12 | 4.5 | 5.666666666666667 | 4.179314138308661 | 38 | 1 | 14 | 4 | 6.333333333333333 | 5.715476066494082 | 0.15432098765432098 | 2.1604938271604937 | 0.6172839506172839 | 0.9773662551440327 | 0.8820179114960003 | ["react-router","context","server","utils"] |
| node:path | 6 | 6 | 1 | 1 | 1 | 1 | 0 | 11 | 1 | 3 | 1.5 | 1.8333333333333333 | 0.983192080250175 | 0.15432098765432098 | 0.4629629629629629 | 0.23148148148148145 | 0.28292181069958844 | 0.1517271728781134 | ["normalizeSlashes","flatRoutes","react-router-fs-routes","utils"] |
| readline | 6 | 10 | 1 | 4 | 1 | 1.6666666666666665 | 1.2110601416389966 | 6 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["prompts-confirm","prompts-multi-select","prompts-prompt-base","prompts-select"] |
| sisteransi | 6 | 27 | 3 | 7 | 4 | 4.5 | 1.378404875209022 | 6 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["prompts-confirm","prompts-multi-select","prompts-prompt-base","prompts-select"] |
| @babel/lib | 5 | 49 | 2 | 17 | 8 | 9.8 | 6.496152707564686 | 7 | 1 | 3 | 1 | 1.4 | 0.8944271909999159 | 0.15432098765432098 | 0.4629629629629629 | 0.15432098765432098 | 0.21604938271604937 | 0.138028887499987 | ["useJavascript","remove-exports","route-chunks","styles"] |
| fs | 5 | 17 | 2 | 5 | 3 | 3.4 | 1.51657508881031 | 8 | 1 | 2 | 2 | 1.6 | 0.5477225575051662 | 0.15432098765432098 | 0.30864197530864196 | 0.30864197530864196 | 0.24691358024691357 | 0.08452508603474786 | ["flatRoutes","utils","vite","plugin"] |
| http | 5 | 11 | 1 | 3 | 2 | 2.2 | 0.8366600265340756 | 9 | 1 | 2 | 2 | 1.8 | 0.4472135954999579 | 0.15432098765432098 | 0.30864197530864196 | 0.30864197530864196 | 0.2777777777777778 | 0.0690144437499935 | ["server","vite","plugin","node-adapter"] |
| @types/pick | 4 | 4 | 1 | 1 | 1 | 1 | 0 | 6 | 1 | 3 | 1 | 1.5 | 1 | 0.15432098765432098 | 0.4629629629629629 | 0.15432098765432098 | 0.23148148148148148 | 0.15432098765432098 | ["routes","vite","plugin","config"] |
| @cloudflare/workers-types | 3 | 44 | 4 | 22 | 18 | 14.666666666666668 | 9.451631252505218 | 10 | 1 | 5 | 4 | 3.333333333333333 | 2.0816659994661326 | 0.15432098765432098 | 0.7716049382716049 | 0.6172839506172839 | 0.51440329218107 | 0.3212447530040328 | ["worker","react-router-cloudflare","workersKVStorage"] |
| @types/babel__core | 3 | 8 | 2 | 3 | 3 | 2.6666666666666665 | 0.5773502691896257 | 3 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["vite","plugin","useJavascript"] |
| @types/babel__traverse | 3 | 17 | 2 | 11 | 4 | 5.666666666666666 | 4.725815626252609 | 3 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["remove-exports","styles","with-props"] |
| lexer | 3 | 4 | 1 | 2 | 1 | 1.3333333333333333 | 0.5773502691896258 | 5 | 1 | 2 | 2 | 1.6666666666666667 | 0.5773502691896258 | 0.15432098765432098 | 0.30864197530864196 | 0.30864197530864196 | 0.257201646090535 | 0.08909726376383113 | ["vite","plugin","virtual-route-modules"] |
| node:process | 3 | 3 | 1 | 1 | 1 | 1 | 0 | 7 | 1 | 4 | 2 | 2.3333333333333335 | 1.5275252316519465 | 0.15432098765432098 | 0.6172839506172839 | 0.30864197530864196 | 0.36008230452674894 | 0.23572920241542386 | ["create-react-router","prompts-prompt-base","utils"] |
| node:url | 3 | 4 | 1 | 2 | 1 | 1.3333333333333333 | 0.5773502691896257 | 3 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["copy-template","vite","plugin"] |
| @architect/functions | 2 | 4 | 2 | 2 | 2 | 2 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["react-router-architect","arcTableSessionStorage"] |
| @architect/tables | 2 | 6 | 3 | 3 | 3 | 3 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["react-router-architect","arcTableSessionStorage"] |
| @babel/babel-parser | 2 | 3 | 1 | 2 | 1.5 | 1.5 | 0.7071067811865476 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["remove-exports","with-props"] |
| @mjackson/node-fetch-server | 2 | 4 | 2 | 2 | 2 | 2 | 0 | 4 | 2 | 2 | 2 | 2 | 0 | 0.30864197530864196 | 0.30864197530864196 | 0.30864197530864196 | 0.30864197530864196 | 0 | ["react-router-node","server"] |
| @types/api-gateway-proxy | 2 | 18 | 3 | 15 | 9 | 9 | 8.48528137423857 | 7 | 2 | 5 | 3.5 | 3.5 | 2.1213203435596424 | 0.30864197530864196 | 0.7716049382716049 | 0.5401234567901234 | 0.5401234567901234 | 0.32736425054932755 | ["server","react-router-architect"] |
| @types/express | 2 | 19 | 3 | 16 | 9.5 | 9.5 | 9.192388155425117 | 6 | 2 | 4 | 3 | 3 | 1.4142135623730951 | 0.30864197530864196 | 0.6172839506172839 | 0.4629629629629629 | 0.4629629629629629 | 0.21824283369955172 | ["react-router-express","server"] |
| @types/express-serve-static-core | 2 | 3 | 1 | 2 | 1.5 | 1.5 | 0.7071067811865476 | 5 | 2 | 3 | 2.5 | 2.5 | 0.7071067811865476 | 0.30864197530864196 | 0.4629629629629629 | 0.3858024691358024 | 0.3858024691358024 | 0.10912141684977585 | ["react-router-express","server"] |
| @types/handler | 2 | 4 | 2 | 2 | 2 | 2 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["server","react-router-architect"] |
| @types/jsesc | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["vite","plugin"] |
| @types/qs | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 5 | 2 | 3 | 2.5 | 2.5 | 0.7071067811865476 | 0.30864197530864196 | 0.4629629629629629 | 0.3858024691358024 | 0.3858024691358024 | 0.10912141684977585 | ["react-router-express","server"] |
| @types/stream | 2 | 8 | 4 | 4 | 4 | 4 | 0 | 6 | 3 | 3 | 3 | 3 | 0 | 0.4629629629629629 | 0.4629629629629629 | 0.4629629629629629 | 0.4629629629629629 | 0 | ["react-router-node","stream"] |
| async_hooks | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 8 | 4 | 4 | 4 | 4 | 0 | 0.6172839506172839 | 0.6172839506172839 | 0.6172839506172839 | 0.6172839506172839 | 0 | ["react-router","server"] |
| cli | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["cloudflare-dev-proxy","cloudflare"] |
| crypto | 2 | 4 | 2 | 2 | 2 | 2 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["vite","plugin"] |
| esm | 2 | 6 | 1 | 5 | 3 | 3 | 2.8284271247461903 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["flatRoutes","config"] |
| module-runner | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["vite","plugin"] |
| node:crypto | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["vite","plugin"] |
| rollup | 2 | 6 | 3 | 3 | 3 | 3 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["vite","plugin"] |
| url | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["vite","plugin"] |
| @types/APIGatewayProxyEventHeaders."content-type | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["server"] |
| @types/APIGatewayProxyEventHeaders."x-forwarded-host | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["server"] |
| @types/events | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["prompts-prompt-base"] |
| @types/isEqual | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["config"] |
| @types/kebabCase | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["plugin"] |
| @types/semver | 1 | 2 | 2 | 2 | 2 | 2 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["run"] |
| @types/timers | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["prompts-select"] |
| arg | 1 | 2 | 2 | 2 | 2 | 2 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["run"] |
| arg.Result."--no-typescript | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["run"] |
| exit-hook | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["commands"] |
| inspector | 1 | 3 | 3 | 3 | 3 | 3 | 0 | 3 | 3 | 3 | 3 | 3 | 0 | 0.4629629629629629 | 0.4629629629629629 | 0.4629629629629629 | 0.4629629629629629 | 0 | ["profiler"] |
| node:child_process | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["config"] |
| node:inspector | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["profiler"] |
| node:readline | 1 | 3 | 3 | 3 | 3 | 3 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["prompts-prompt-base"] |
| p-map | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["prerender"] |
| prettier | 1 | 2 | 2 | 2 | 2 | 2 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["useJavascript"] |
| server | 1 | 4 | 4 | 4 | 4 | 4 | 0 | 2 | 2 | 2 | 2 | 2 | 0 | 0.30864197530864196 | 0.30864197530864196 | 0.30864197530864196 | 0.30864197530864196 | 0 | ["vite-node"] |
| types | 1 | 1 | 1 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 0 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0.15432098765432098 | 0 | ["utils"] |

### 3.4 External Module Usage per Internal Module (Sorted)

Which internal TypeScript modules depend on the most external modules?

| internalModuleName | externalModuleName | numberOfExternalDeclarationCaller | numberOfExternalDeclarationCalls | numberOfAllElementsInInternalModule | numberOfAllExternalDeclarationsUsedInInternalModule | numberOfAllExternalModulesUsedInInternalModule | externalDeclarationRate | externalDeclarationNames |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| remove-exports | @babel/lib | 16 | 56 | 1 | 23 | 4 | 2300 | ["ExportDefaultDeclaration.declaration","ExpressionStatement.expression","Identifier.name","VariableDeclarator.id","ExportNamedDeclaration.declaration","MemberExpression.object","ClassDeclaration.id","Expression.type","AssignmentExpression.left","VariableDeclaration.declarations","LVal.type","ExportDeclaration.type","ExportNamedDeclaration.specifiers","FunctionDeclaration.id","ExportSpecifier.exported","ExportSpecifier.local"] |
| remove-exports | @types/babel__traverse | 4 | 24 | 1 | 23 | 4 | 2300 | ["NodePath.node","NodePath.remove","NodePath.isProgram","NodePath.parentPath"] |
| remove-exports | dist | 2 | 2 | 1 | 23 | 4 | 2300 | ["deadCodeElimination","findReferencedIdentifiers"] |
| remove-exports | @babel/babel-parser | 1 | 2 | 1 | 23 | 4 | 2300 | ["ParseResult"] |
| vite | node | 84 | 148 | 6 | 129 | 25 | 2150 | ["UserConfig.base","Logger.error","normalizePath","PluginOption","transformWithEsbuild","ResolvedBuildEnvironmentOptions.outDir","UserConfig.server","ResolvedEnvironmentOptions.build","ResolvedConfig.base","UserConfig.logLevel","Connect.Server.use","createLogger","Logger.info","ResolvedConfig.environments","Connect.IncomingMessage.url","PreviewServer.middlewares","ResolvedConfig.build","loadConfigFromFile","UserConfig.environments","ConfigEnv.isSsrBuild","UserConfig.root","defaultClientConditions","ViteDevServer.environments","ModuleNode.file","ManifestChunk.assets","ViteDevServer.ssrFixStacktrace","ViteDevServer.ssrLoadModule","Environment.config","ViteDevServer.pluginContainer","ConfigEnv.mode","ResolvedConfig.command","DevEnvironment.moduleGraph","HotUpdatePluginContext.environment","Logger.warn","ModuleNode.url","ViteBuilder.build","DevEnvironment.name","ResolvedConfig","ViteDevServer.hot","PreviewServer","Environment.name","createServer","HotBroadcaster.send","PluginContainer.buildStart","ViteDevServer","Plugin","EnvironmentOptions.resolve","ManifestChunk.file","ResolvedServerOptions.middlewareMode","ResolvedConfig.server","ResolvedConfig.mode","ViteDevServer.config","Plugin.name","EnvironmentOptions.optimizeDeps","EnvironmentOptions","ConfigEnv.command","ResolvedServerOptions.watch","ResolvedConfig.configFile","ResolvedConfig.logger","ViteBuilder.environments","ViteDevServer.middlewares","UserConfig.plugins","UserConfig.build","ResolvedBuildOptions.assetsDir","RunnableDevEnvironment.runner","ResolvedConfig.root","isRunnableDevEnvironment","ViteDevServer.transformRequest","DevEnvironment.reloadModule","ManifestChunk.css","version","node","ESBuildOptions"] |
| vite | @types/process | 7 | 15 | 6 | 129 | 25 | 2150 | ["global.NodeJS.Process.env","global.NodeJS.ProcessEnv.IS_RR_BUILD_REQUEST","global.NodeJS.ProcessEnv.REACT_ROUTER_ROOT","global.NodeJS.Process.cwd","global.NodeJS.Process.exit"] |
| vite | dist | 7 | 23 | 6 | 129 | 25 | 2150 | ["relative","join","path.join","path.extname","path.normalize","resolve","dist"] |
| vite | promises | 7 | 14 | 6 | 129 | 25 | 2150 | ["readFile","readdir","mkdir","cp","rename","rm"] |
| vite | @types/path | 6 | 25 | 6 | 129 | 25 | 2150 | ["path.PlatformPath.posix","path.PlatformPath.basename","path.PlatformPath.dirname","path.PlatformPath.relative","path.PlatformPath.resolve","path.PlatformPath.join"] |
| vite | fs | 5 | 10 | 6 | 129 | 25 | 2150 | ["existsSync","Dirent.name","Dirent.isFile","Dirent.parentPath","Dirent.path"] |
| vite | http | 5 | 8 | 6 | 129 | 25 | 2150 | ["ServerResponse.end","ServerResponse.setHeader","ServerResponse.statusCode"] |
| vite | @types/babel__core | 3 | 3 | 6 | 129 | 25 | 2150 | ["BabelFileResult.code","transformAsync","BabelFileResult.map"] |
| vite | node:fs | 3 | 8 | 6 | 129 | 25 | 2150 | ["readdirSync","rmSync","existsSync"] |
| vite | rollup | 3 | 5 | 6 | 129 | 25 | 2150 | ["ResolvedId.id","PluginContext.environment","PluginContext.resolve"] |
| vite | @types/babel__generator | 2 | 2 | 6 | 129 | 25 | 2150 | ["GeneratorResult.code","GeneratorResult"] |
| vite | crypto | 2 | 2 | 6 | 129 | 25 | 2150 | ["Hash.digest","Hash.update"] |
| vite | lexer | 2 | 2 | 6 | 129 | 25 | 2150 | ["init"] |
| vite | picocolors | 2 | 14 | 6 | 129 | 25 | 2150 | ["picocolors"] |
| vite | @types/buffer | 1 | 1 | 6 | 129 | 25 | 2150 | ["global.NonSharedBuffer.toString"] |
| vite | @types/jsesc | 1 | 2 | 6 | 129 | 25 | 2150 | ["jsesc"] |
| vite | @types/module | 1 | 2 | 6 | 129 | 25 | 2150 | ["global.NodeJS.Require.resolve"] |
| vite | @types/pick | 1 | 1 | 6 | 129 | 25 | 2150 | ["pick"] |
| vite | module-runner | 1 | 1 | 6 | 129 | 25 | 2150 | ["ModuleRunner.import"] |
| vite | node:crypto | 1 | 1 | 6 | 129 | 25 | 2150 | ["createHash"] |
| vite | node:url | 1 | 2 | 6 | 129 | 25 | 2150 | [".pathToFileURL"] |
| vite | url | 1 | 2 | 6 | 129 | 25 | 2150 | ["URL.href"] |
| with-props | @types/babel__traverse | 11 | 23 | 1 | 21 | 4 | 2100 | ["NodePath.node","NodePath.isExportNamedDeclaration","NodePath.isExportDefaultDeclaration","NodePath.get","NodePath.replaceWith","NodePath.scope","NodePath.isFunctionDeclaration","Scope.generateUidIdentifier","NodePath.isVariableDeclaration","NodePath.isIdentifier","NodePath.isExpression"] |
| with-props | @babel/lib | 8 | 11 | 1 | 21 | 4 | 2100 | ["identifier","Program.body","callExpression","importDeclaration","variableDeclaration","variableDeclarator","stringLiteral","importSpecifier"] |
| with-props | @babel/babel-parser | 2 | 3 | 1 | 21 | 4 | 2100 | ["ParseResult.program","ParseResult"] |
| cloudflare | node | 13 | 18 | 1 | 15 | 4 | 1500 | ["Plugin.name","ViteDevServer.middlewares","ResolvedServerOptions.middlewareMode","Connect.Server.use","Plugin","ConfigEnv.mode","ResolvedConfig.server","ViteDevServer.config","UserConfig.root","ViteDevServer.ssrLoadModule","ResolvedConfig.plugins","EnvironmentResolveOptions.externalConditions","EnvironmentOptions.resolve"] |
| cloudflare | @types/process | 1 | 1 | 1 | 15 | 4 | 1500 | ["global.NodeJS.Process.cwd"] |
| cloudflare | cli | 1 | 2 | 1 | 15 | 4 | 1500 | ["GetPlatformProxyOptions"] |
| cloudflare-dev-proxy | node | 13 | 18 | 1 | 15 | 4 | 1500 | ["Plugin.name","ViteDevServer.middlewares","ResolvedServerOptions.middlewareMode","Connect.Server.use","Plugin","ConfigEnv.mode","ResolvedConfig.server","ViteDevServer.config","UserConfig.root","ViteDevServer.ssrLoadModule","ResolvedConfig.plugins","EnvironmentResolveOptions.externalConditions","EnvironmentOptions.resolve"] |
| cloudflare-dev-proxy | @types/process | 1 | 1 | 1 | 15 | 4 | 1500 | ["global.NodeJS.Process.cwd"] |
| cloudflare-dev-proxy | cli | 1 | 2 | 1 | 15 | 4 | 1500 | ["GetPlatformProxyOptions"] |
| warn-on-client-source-maps | node | 11 | 12 | 1 | 12 | 2 | 1200 | ["ResolvedEnvironmentOptions.build","ResolvedBuildEnvironmentOptions.sourcemap","Plugin","ResolvedConfig.mode","ResolvedConfig.environments","Logger.warn","ResolvedBuildOptions.ssr","ResolvedConfig.logger","ResolvedConfig.build","ResolvedBuildOptions.sourcemap","ConfigEnv.command"] |
| warn-on-client-source-maps | picocolors | 1 | 2 | 1 | 12 | 2 | 1200 | ["picocolors"] |
| run | @types/process | 2 | 4 | 1 | 8 | 5 | 800 | ["global.NodeJS.Process.versions","global.NodeJS.ProcessVersions.node"] |
| run | @types/semver | 2 | 2 | 1 | 8 | 5 | 800 | ["semver","major"] |
| run | arg | 2 | 3 | 1 | 8 | 5 | 800 | ["arg.Result._","arg"] |
| run | @types/module | 1 | 1 | 1 | 8 | 5 | 800 | ["global.NodeJS.Require.main"] |
| run | arg.Result."--no-typescript | 1 | 1 | 1 | 8 | 5 | 800 | ["arg.Result.\"--no-typescript\""] |
| plugin | node | 96 | 165 | 18 | 135 | 26 | 750 | ["UserConfig","ResolvedConfig","ResolvedConfig.build","ResolvedBuildOptions.emptyOutDir","UserConfig.build","defaultServerConditions","UserConfig.environments","resolveConfig","ResolvedBuildOptions.manifest","Plugin","ModuleNode","ViteDevServer","UserConfig.logLevel","loadConfigFromFile","Logger.info","ConfigEnv.isSsrBuild","UserConfig.root","defaultClientConditions","ViteDevServer.environments","ModuleNode.file","ManifestChunk.assets","ViteDevServer.ssrFixStacktrace","ViteDevServer.ssrLoadModule","Environment.config","ViteDevServer.pluginContainer","ConfigEnv.mode","ResolvedConfig.command","DevEnvironment.moduleGraph","HotUpdatePluginContext.environment","Logger.warn","ModuleNode.url","ViteBuilder.build","UserConfig.server","DevEnvironment.name","ViteDevServer.hot","PreviewServer","Logger.error","Environment.name","createServer","HotBroadcaster.send","PluginContainer.buildStart","UserConfig.base","EnvironmentOptions.resolve","ManifestChunk.file","ResolvedServerOptions.middlewareMode","ResolvedConfig.server","normalizePath","ResolvedConfig.mode","createLogger","ViteDevServer.config","Plugin.name","EnvironmentOptions.optimizeDeps","EnvironmentOptions","Connect.IncomingMessage.url","ConfigEnv.command","Connect.Server.use","ResolvedServerOptions.watch","ResolvedConfig.configFile","ResolvedConfig.logger","ViteBuilder.environments","ViteDevServer.middlewares","UserConfig.plugins","PreviewServer.middlewares","ResolvedBuildOptions.assetsDir","RunnableDevEnvironment.runner","ResolvedConfig.root","isRunnableDevEnvironment","ViteDevServer.transformRequest","DevEnvironment.reloadModule","ManifestChunk.css","PluginOption","transformWithEsbuild","ResolvedBuildEnvironmentOptions.outDir","ResolvedEnvironmentOptions.build","ResolvedConfig.base","ResolvedConfig.environments"] |
| plugin | @types/path | 17 | 41 | 18 | 135 | 26 | 750 | ["path.PlatformPath.isAbsolute","path.PlatformPath.relative","path.PlatformPath.resolve","path.PlatformPath.join","path.PlatformPath.dirname","path.PlatformPath.posix","path.PlatformPath.basename"] |
| plugin | promises | 10 | 18 | 18 | 135 | 26 | 750 | ["rm","readdir","readFile","mkdir","cp","rename"] |
| plugin | @types/process | 7 | 15 | 18 | 135 | 26 | 750 | ["global.NodeJS.ProcessEnv.REACT_ROUTER_ROOT","global.NodeJS.Process.env","global.NodeJS.Process.cwd","global.NodeJS.Process.exit","global.NodeJS.ProcessEnv.IS_RR_BUILD_REQUEST"] |
| plugin | dist | 7 | 23 | 18 | 135 | 26 | 750 | ["relative","join","path.join","path.extname","path.normalize","resolve","dist"] |
| plugin | fs | 5 | 10 | 18 | 135 | 26 | 750 | ["Dirent.name","Dirent.isFile","Dirent.parentPath","Dirent.path","existsSync"] |
| plugin | http | 5 | 8 | 18 | 135 | 26 | 750 | ["ServerResponse.end","ServerResponse.setHeader","ServerResponse.statusCode"] |
| plugin | node:fs | 5 | 10 | 18 | 135 | 26 | 750 | ["readFileSync","existsSync","readdirSync","rmSync"] |
| plugin | @types/babel__core | 3 | 3 | 18 | 135 | 26 | 750 | ["BabelFileResult.code","transformAsync","BabelFileResult.map"] |
| plugin | picocolors | 3 | 15 | 18 | 135 | 26 | 750 | ["picocolors"] |
| plugin | rollup | 3 | 5 | 18 | 135 | 26 | 750 | ["ResolvedId.id","PluginContext.environment","PluginContext.resolve"] |
| plugin | @types/babel__generator | 2 | 2 | 18 | 135 | 26 | 750 | ["GeneratorResult.code","GeneratorResult"] |
| plugin | @types/module | 2 | 3 | 18 | 135 | 26 | 750 | ["global.NodeJS.Require.resolve"] |
| plugin | crypto | 2 | 2 | 18 | 135 | 26 | 750 | ["Hash.digest","Hash.update"] |
| plugin | lexer | 2 | 2 | 18 | 135 | 26 | 750 | ["init"] |
| plugin | @types/buffer | 1 | 1 | 18 | 135 | 26 | 750 | ["global.NonSharedBuffer.toString"] |
| plugin | @types/jsesc | 1 | 2 | 18 | 135 | 26 | 750 | ["jsesc"] |
| plugin | @types/kebabCase | 1 | 1 | 18 | 135 | 26 | 750 | ["kebabCase"] |
| plugin | @types/pick | 1 | 1 | 18 | 135 | 26 | 750 | ["pick"] |
| plugin | module-runner | 1 | 1 | 18 | 135 | 26 | 750 | ["ModuleRunner.import"] |
| plugin | node:crypto | 1 | 1 | 18 | 135 | 26 | 750 | ["createHash"] |
| plugin | node:url | 1 | 2 | 18 | 135 | 26 | 750 | [".pathToFileURL"] |
| plugin | url | 1 | 2 | 18 | 135 | 26 | 750 | ["URL.href"] |
| prompts-prompt-base | @types/process | 4 | 20 | 2 | 14 | 6 | 700 | ["global.NodeJS.Process.stdout","global.NodeJS.Process.stdin","global.NodeJS.ReadStream","global.NodeJS.WriteStream"] |
| prompts-prompt-base | node:readline | 3 | 20 | 2 | 14 | 6 | 700 | [".emitKeypressEvents",".createInterface","node:readline"] |
| prompts-prompt-base | sisteransi | 3 | 15 | 2 | 14 | 6 | 700 | ["cursor","beep","cursor.show"] |
| prompts-prompt-base | node:process | 2 | 30 | 2 | 14 | 6 | 700 | ["node:process"] |
| prompts-prompt-base | readline | 2 | 10 | 2 | 14 | 6 | 700 | ["Interface.close","Key"] |
| prompts-prompt-base | @types/events | 1 | 1 | 2 | 14 | 6 | 700 | ["EventEmitter"] |
| vite-node | node | 8 | 9 | 2 | 13 | 4 | 650 | ["ViteDevServer.config","Logger","PluginContainer.buildStart","ViteDevServer.pluginContainer","createServer","ResolvedConfig.base","ResolvedConfig.root","ViteDevServer"] |
| vite-node | server | 4 | 4 | 2 | 13 | 4 | 650 | ["ViteNodeServer.fetchModule","ViteNodeServer.resolveId","ViteNodeServer.getSourceMap","ViteNodeServer"] |
| vite-node | dist | 1 | 1 | 2 | 13 | 4 | 650 | ["ViteNodeRunner"] |
| useJavascript | @babel/lib | 2 | 2 | 1 | 6 | 5 | 600 | ["lib"] |
| useJavascript | @types/babel__core | 2 | 3 | 1 | 6 | 5 | 600 | ["BabelFileResult.code","transformSync"] |
| useJavascript | prettier | 2 | 2 | 1 | 6 | 5 | 600 | ["prettier","format"] |
| arcTableSessionStorage | @architect/tables | 3 | 5 | 1 | 5 | 2 | 500 | ["ArcTable.get","ArcTable.delete","ArcTable.put"] |
| arcTableSessionStorage | @architect/functions | 2 | 2 | 1 | 5 | 2 | 500 | ["functions","tables"] |
| is-react-router-repo | dist | 4 | 6 | 1 | 5 | 2 | 500 | ["path.basename","path.dirname","dist","path.resolve"] |
| is-react-router-repo | @types/module | 1 | 1 | 1 | 5 | 2 | 500 | ["global.NodeJS.Require.resolve"] |
| react-router-fs-routes | @types/path | 2 | 2 | 1 | 5 | 3 | 500 | ["path.PlatformPath.resolve","path.PlatformPath.relative"] |
| react-router-fs-routes | node:fs | 2 | 2 | 1 | 5 | 3 | 500 | [".existsSync","node:fs"] |
| react-router-fs-routes | node:path | 1 | 2 | 1 | 5 | 3 | 500 | ["node:path"] |
| resolve-file-url | @types/path | 4 | 6 | 1 | 5 | 2 | 500 | ["path.PlatformPath.relative","path.PlatformPath.join","path.PlatformPath.isAbsolute","path.PlatformPath.posix"] |
| resolve-file-url | node | 1 | 3 | 1 | 5 | 2 | 500 | ["normalizePath"] |
| fileStorage | promises | 4 | 7 | 2 | 9 | 5 | 450 | [".mkdir",".readFile",".unlink",".writeFile"] |
| fileStorage | @types/buffer | 2 | 2 | 2 | 9 | 5 | 450 | ["global.Buffer.toString","global.BufferConstructor.from"] |
| fileStorage | @types/path | 2 | 3 | 2 | 9 | 5 | 450 | ["path.PlatformPath.dirname","path.PlatformPath.join"] |
| fileStorage | node:fs | 1 | 7 | 2 | 9 | 5 | 450 | ["promises"] |
| load-dotenv | node | 3 | 3 | 1 | 4 | 2 | 400 | ["UserConfig.envDir","UserConfig","loadEnv"] |
| load-dotenv | @types/process | 1 | 1 | 1 | 4 | 2 | 400 | ["global.NodeJS.Process.env"] |
| prompts-text | sisteransi | 7 | 35 | 2 | 8 | 2 | 400 | ["cursor.restore","cursor.to","cursor.move","erase","cursor.down","erase.line","cursor.save"] |
| prompts-text | readline | 1 | 5 | 2 | 8 | 2 | 400 | ["Key"] |
| workersKVStorage | @cloudflare/workers-types | 4 | 6 | 1 | 4 | 1 | 400 | ["KVNamespace.delete","KVNamespace.get","KVNamespace.put","Crypto.getRandomValues"] |
| react-router-cloudflare | @cloudflare/workers-types | 26 | 34 | 6 | 22 | 2 | 366.6666666666667 | ["EventContext.waitUntil","EventContext.passThroughOnException","Request.cf","EventContext.request","Request","CacheStorage","CfProperties","EventContext","IncomingRequestCfProperties","KVNamespace.delete","KVNamespace.get","KVNamespace.put","Crypto.getRandomValues","Response","Response.body","Request.url","Request.clone","Console.error","Request.headers","Headers.delete","EventContext.env","Response.status"] |
| worker | @cloudflare/workers-types | 22 | 28 | 5 | 18 | 2 | 360 | ["Response.body","Request.url","Response","EventContext","Request.clone","EventContext.request","Console.error","Request.headers","Headers.delete","EventContext.env","Response.status","Request","CacheStorage","CfProperties","IncomingRequestCfProperties","EventContext.waitUntil","EventContext.passThroughOnException","Request.cf"] |
| has-rsc-plugin | node | 3 | 3 | 1 | 3 | 2 | 300 | ["Plugin.name","ResolvedConfig.plugins","resolveConfig"] |
| optimize-deps-entries | node | 2 | 2 | 1 | 3 | 2 | 300 | ["normalizePath","version"] |
| optimize-deps-entries | dist | 1 | 1 | 1 | 3 | 2 | 300 | ["escapePath"] |
| profiler | inspector | 4 | 6 | 3 | 9 | 6 | 300 | ["Session.post","Session.connect","Session"] |
| profiler | node:fs | 2 | 2 | 3 | 9 | 6 | 300 | ["node:fs",".writeFileSync"] |
| profiler | @types/path | 1 | 1 | 3 | 9 | 6 | 300 | ["path.PlatformPath.resolve"] |
| profiler | node:inspector | 1 | 1 | 3 | 9 | 6 | 300 | [".Session"] |
| profiler | node:path | 1 | 1 | 3 | 9 | 6 | 300 | ["node:path"] |
| profiler | picocolors | 1 | 3 | 3 | 9 | 6 | 300 | ["picocolors"] |
| resolve-relative-route-file-path | dist | 2 | 2 | 1 | 3 | 2 | 300 | ["path.resolve","dist"] |
| resolve-relative-route-file-path | node | 1 | 1 | 1 | 3 | 2 | 300 | ["normalizePath"] |
| styles | @babel/lib | 6 | 8 | 4 | 12 | 5 | 300 | ["StringLiteral.value","VariableDeclarator.init","LVal.type","VariableDeclaration.declarations","Identifier.name","VariableDeclarator.id"] |
| styles | @types/babel__traverse | 2 | 2 | 4 | 12 | 5 | 300 | ["NodePath.node","NodePath.stop"] |
| styles | @types/path | 2 | 3 | 4 | 12 | 5 | 300 | ["path.PlatformPath.resolve","path.PlatformPath.relative"] |
| styles | @types/process | 1 | 1 | 4 | 12 | 5 | 300 | ["global.NodeJS.Process.cwd"] |
| styles | node | 1 | 2 | 4 | 12 | 5 | 300 | ["ViteDevServer"] |
| validate-plugin-order | node | 3 | 3 | 1 | 3 | 1 | 300 | ["Plugin","Plugin.name","ResolvedConfig.plugins"] |
| dev | node | 9 | 14 | 5 | 14 | 5 | 280 | ["ViteDevServer.bindCLIShortcuts","ViteDevServer.config","Plugin.name","ViteDevServer.printUrls","ViteDevServer.listen","ResolvedConfig.logger","ResolvedConfig.plugins","createServer","Logger.info"] |
| dev | @types/process | 4 | 5 | 5 | 14 | 5 | 280 | ["global.NodeJS.ProcessEnv.hasOwnProperty","global.NodeJS.Process.env","global.NodeJS.ProcessEnv.IS_RR_BUILD_REQUEST","global.NodeJS.Process.exit"] |
| dev | picocolors | 1 | 1 | 5 | 14 | 5 | 280 | ["picocolors"] |
| node-adapter | node | 4 | 6 | 2 | 5 | 2 | 250 | ["Connect.IncomingMessage.originalUrl","Connect.IncomingMessage.url","Connect.IncomingMessage"] |
| node-adapter | http | 3 | 3 | 2 | 5 | 2 | 250 | ["ServerResponse","IncomingMessage"] |
| prompts-multi-select | sisteransi | 4 | 20 | 2 | 5 | 2 | 250 | ["erase","cursor.to","cursor.hide","erase.line"] |
| prompts-multi-select | readline | 1 | 5 | 2 | 5 | 2 | 250 | ["Key"] |
| react-router-architect | @types/api-gateway-proxy | 5 | 5 | 4 | 10 | 4 | 250 | ["APIGatewayEventRequestContextV2","APIGatewayProxyResultV2","APIGatewayProxyEventV2"] |
| react-router-architect | @architect/tables | 3 | 5 | 4 | 10 | 4 | 250 | ["ArcTable.get","ArcTable.delete","ArcTable.put"] |
| react-router-architect | @architect/functions | 2 | 2 | 4 | 10 | 4 | 250 | ["functions","tables"] |
| react-router-architect | @types/handler | 2 | 2 | 4 | 10 | 4 | 250 | ["Context","Callback"] |
| commands | @types/path | 3 | 9 | 5 | 12 | 9 | 240 | ["path.PlatformPath.relative","path.PlatformPath.dirname","path.PlatformPath.resolve"] |
| commands | picocolors | 2 | 6 | 5 | 12 | 9 | 240 | ["picocolors"] |
| commands | promises | 2 | 3 | 5 | 12 | 9 | 240 | ["copyFile","writeFile"] |
| commands | @types/module | 1 | 1 | 5 | 12 | 9 | 240 | ["global.NodeJS.Require.resolve"] |
| commands | @types/process | 1 | 1 | 5 | 12 | 9 | 240 | ["global.NodeJS.Process.exit"] |
| commands | dist | 1 | 1 | 5 | 12 | 9 | 240 | ["PackageJson.dependencies"] |
| commands | exit-hook | 1 | 1 | 5 | 12 | 9 | 240 | ["exit-hook"] |
| commands | node | 1 | 1 | 5 | 12 | 9 | 240 | ["createLogger"] |
| commands | node:fs | 1 | 1 | 5 | 12 | 9 | 240 | ["existsSync"] |
| react-router-node | @types/stream | 7 | 8 | 7 | 16 | 8 | 228.57142857142858 | ["Stream.Readable","Stream.Writable.write","Stream.Writable.end","Stream.Writable"] |
| react-router-node | @types/buffer | 4 | 4 | 7 | 16 | 8 | 228.57142857142858 | ["global.Buffer.toString","global.BufferConstructor.from","global.BufferConstructor.concat"] |
| react-router-node | promises | 4 | 7 | 7 | 16 | 8 | 228.57142857142858 | [".mkdir",".readFile",".unlink",".writeFile"] |
| react-router-node | @mjackson/node-fetch-server | 2 | 2 | 7 | 16 | 8 | 228.57142857142858 | ["createRequestListener","ClientAddress"] |
| react-router-node | @types/path | 1 | 2 | 7 | 16 | 8 | 228.57142857142858 | ["path.PlatformPath.dirname"] |
| react-router-node | http | 1 | 1 | 7 | 16 | 8 | 228.57142857142858 | ["RequestListener"] |
| react-router-node | node:fs | 1 | 7 | 7 | 16 | 8 | 228.57142857142858 | ["promises"] |
| config | dist | 15 | 43 | 14 | 31 | 15 | 221.42857142857144 | ["ViteNodeRunner.moduleCache","dist","path.normalize","ModuleCacheMap.clear","path.relative","path.join","path.dirname","path.resolve","PackageJson.dependencies"] |
| config | esm | 5 | 6 | 14 | 31 | 15 | 221.42857142857144 | ["_default.watch","FSWatcher.add","FSWatcher.unwatch","FSWatcher.on","esm"] |
| config | node | 5 | 8 | 14 | 31 | 15 | 221.42857142857144 | ["ModuleGraph.getModuleById","ModuleGraph.invalidateAll","ViteDevServer.moduleGraph","ViteDevServer.close","createLogger"] |
| config | @types/process | 3 | 3 | 14 | 31 | 15 | 221.42857142857144 | ["global.NodeJS.Process.cwd","global.NodeJS.Process.env","global.NodeJS.ProcessEnv.REACT_ROUTER_ROOT"] |
| config | @types/module | 2 | 2 | 14 | 31 | 15 | 221.42857142857144 | ["global.NodeJS.Require.resolve"] |
| config | fs | 2 | 2 | 14 | 31 | 15 | 221.42857142857144 | ["Stats.isFile","Stats.isDirectory"] |
| config | node:fs | 2 | 2 | 14 | 31 | 15 | 221.42857142857144 | [".statSync","node:fs"] |
| config | @types/isEqual | 1 | 2 | 14 | 31 | 15 | 221.42857142857144 | ["isEqual"] |
| config | @types/pick | 1 | 1 | 14 | 31 | 15 | 221.42857142857144 | ["pick"] |
| config | node:child_process | 1 | 1 | 14 | 31 | 15 | 221.42857142857144 | ["execSync"] |
| config | picocolors | 1 | 1 | 14 | 31 | 15 | 221.42857142857144 | ["picocolors"] |
| loading-indicator | @types/process | 2 | 2 | 1 | 2 | 1 | 200 | ["global.NodeJS.WriteStream","global.NodeJS.ReadStream"] |
| prerender | @types/path | 3 | 3 | 6 | 12 | 6 | 200 | ["path.PlatformPath.dirname","path.PlatformPath.join","path.PlatformPath.relative"] |
| prerender | node | 3 | 3 | 6 | 12 | 6 | 200 | ["Plugin","ResolvedConfig.root","PreviewServer.close"] |
| prerender | @types/process | 2 | 6 | 6 | 12 | 6 | 200 | ["global.NodeJS.Process.env","global.NodeJS.ProcessEnv.IS_RR_BUILD_REQUEST"] |
| prerender | promises | 2 | 2 | 6 | 12 | 6 | 200 | ["writeFile","mkdir"] |
| prerender | node:path | 1 | 3 | 6 | 12 | 6 | 200 | ["node:path"] |
| prerender | p-map | 1 | 1 | 6 | 12 | 6 | 200 | ["p-map"] |
| prompts-select | sisteransi | 4 | 20 | 3 | 6 | 3 | 200 | ["erase.line","erase","cursor.hide","cursor.to"] |
| prompts-select | @types/timers | 1 | 5 | 3 | 6 | 3 | 200 | ["global.NodeJS.Timeout"] |
| prompts-select | readline | 1 | 5 | 3 | 6 | 3 | 200 | ["Key"] |
| virtual-route-config | dist | 2 | 2 | 1 | 2 | 1 | 200 | ["path.resolve","dist"] |
| prompts-confirm | sisteransi | 4 | 20 | 3 | 5 | 2 | 166.66666666666669 | ["cursor.hide","cursor.to","erase","erase.line"] |
| prompts-confirm | readline | 1 | 5 | 3 | 5 | 2 | 166.66666666666669 | ["Key"] |
| react-router-express | @types/express | 5 | 5 | 3 | 5 | 3 | 166.66666666666669 | ["e.Response","e.NextFunction","e.Request"] |
| react-router-express | @types/express-serve-static-core | 2 | 2 | 3 | 5 | 3 | 166.66666666666669 | ["ParamsDictionary"] |
| react-router-express | @types/qs | 2 | 2 | 3 | 5 | 3 | 166.66666666666669 | ["QueryString.ParsedQs"] |
| typegen | promises | 4 | 4 | 3 | 5 | 3 | 166.66666666666669 | [".rm","promises"] |
| typegen | picocolors | 2 | 4 | 3 | 5 | 3 | 166.66666666666669 | ["red","green"] |
| typegen | node | 1 | 2 | 3 | 5 | 3 | 166.66666666666669 | ["node"] |
| create-react-router | @types/process | 2 | 10 | 2 | 3 | 2 | 150 | ["global.NodeJS.ReadStream","global.NodeJS.WriteStream"] |
| create-react-router | node:process | 1 | 20 | 2 | 3 | 2 | 150 | ["node:process"] |
| normalizeSlashes | @types/path | 4 | 4 | 2 | 3 | 2 | 150 | ["path.PlatformPath.win32","path.PlatformPath.sep"] |
| normalizeSlashes | node:path | 2 | 2 | 2 | 3 | 2 | 150 | ["node:path"] |
| routes | dist | 30 | 96 | 18 | 27 | 4 | 150 | ["resolve","array","ArraySchema","BaseSchema","BaseIssue","isAbsolute","relative","lazy","string","custom","notValue","StringSchema","NotValueAction","SchemaWithPipe","boolean","optional","BooleanSchema","object","CustomSchema","CustomIssue","OptionalSchema","ObjectSchema","LazySchema","pipe","flatten","safeParse"] |
| routes | @types/pick | 3 | 3 | 18 | 27 | 4 | 150 | ["pick"] |
| stream | @types/stream | 7 | 8 | 4 | 6 | 3 | 150 | ["Stream.Readable","Stream.Writable.write","Stream.Writable.end","Stream.Writable"] |
| stream | @types/buffer | 2 | 2 | 4 | 6 | 3 | 150 | ["global.BufferConstructor.concat","global.Buffer.toString"] |
| route-chunks | @babel/lib | 33 | 66 | 13 | 19 | 3 | 146.15384615384616 | ["isVariableDeclaration","ExportNamedDeclaration.specifiers","isClassDeclaration","Program.body","isFunctionDeclaration","ImportDeclaration.specifiers","isNodesEquivalent","ExportNamedDeclaration.declaration","isImportDeclaration","isExportNamedDeclaration","VariableDeclaration.declarations","Identifier.name","isExportDeclaration","isExportAllDeclaration","isExportDefaultDeclaration","File.program","File"] |
| route-chunks | @types/babel__generator | 5 | 5 | 13 | 19 | 3 | 146.15384615384616 | ["GeneratorResult","GeneratorOptions"] |
| server | @types/express | 21 | 25 | 41 | 53 | 14 | 129.2682926829268 | ["e.Response","e.NextFunction","e.Request","e.Response.flushHeaders","e.Response.statusMessage","e.Response.end","e.Response.status","e.Response.append","e.Request.hostname","e.Request.method","e.Request.originalUrl","e.Request.headers","e.Request.get","e.Response.on","e.Request.protocol","e.Request.app"] |
| server | @types/api-gateway-proxy | 19 | 29 | 41 | 53 | 14 | 129.2682926829268 | ["APIGatewayProxyEventHeaders","APIGatewayProxyEventV2","APIGatewayEventRequestContextV2.domainName","APIGatewayEventRequestContextV2.http","APIGatewayProxyEventV2.isBase64Encoded","APIGatewayProxyEventHeaders.host","APIGatewayProxyEventV2.requestContext","APIGatewayProxyEventV2.body","APIGatewayProxyEventV2.rawPath","APIGatewayEventRequestContextV2","APIGatewayProxyEventV2.rawQueryString","APIGatewayProxyEventV2.cookies","APIGatewayProxyEventV2.headers","APIGatewayProxyResultV2","APIGatewayProxyStructuredResultV2"] |
| server | @types/react | 6 | 22 | 41 | 53 | 14 | 129.2682926829268 | ["React.ReactNode","React.ReactElement","React.FunctionComponent","React.ComponentClass","React.Fragment","React.createElement"] |
| server | @types/express-serve-static-core | 4 | 4 | 41 | 53 | 14 | 129.2682926829268 | ["ParamsDictionary","Application.enabled"] |
| server | async_hooks | 4 | 4 | 41 | 53 | 14 | 129.2682926829268 | ["AsyncLocalStorage.getStore"] |
| server | @types/qs | 3 | 3 | 41 | 53 | 14 | 129.2682926829268 | ["QueryString.ParsedQs"] |
| server | @mjackson/node-fetch-server | 2 | 2 | 41 | 53 | 14 | 129.2682926829268 | ["ClientAddress","createRequestListener"] |
| server | @types/buffer | 2 | 3 | 41 | 53 | 14 | 129.2682926829268 | ["global.BufferConstructor.from","global.Buffer.toString"] |
| server | @types/handler | 2 | 2 | 41 | 53 | 14 | 129.2682926829268 | ["Context","Callback"] |
| server | @types/process | 2 | 2 | 41 | 53 | 14 | 129.2682926829268 | ["global.NodeJS.Process.env","global.NodeJS.ProcessEnv.ARC_SANDBOX"] |
| server | http | 2 | 2 | 41 | 53 | 14 | 129.2682926829268 | ["IncomingHttpHeaders","RequestListener"] |
| server | @types/APIGatewayProxyEventHeaders."content-type | 1 | 1 | 41 | 53 | 14 | 129.2682926829268 | ["APIGatewayProxyEventHeaders.\"content-type\""] |
| server | @types/APIGatewayProxyEventHeaders."x-forwarded-host | 1 | 1 | 41 | 53 | 14 | 129.2682926829268 | ["APIGatewayProxyEventHeaders.\"x-forwarded-host\""] |
| flatRoutes | @types/path | 8 | 18 | 13 | 15 | 5 | 115.38461538461539 | ["path.PlatformPath.dirname","path.PlatformPath.relative","path.PlatformPath.extname","path.PlatformPath.posix","path.PlatformPath.join","path.PlatformPath.sep","path.PlatformPath.win32"] |
| flatRoutes | fs | 3 | 3 | 13 | 15 | 5 | 115.38461538461539 | ["Dirent.isDirectory","Dirent.isFile","Dirent.name"] |
| flatRoutes | node:fs | 3 | 4 | 13 | 15 | 5 | 115.38461538461539 | [".existsSync",".readdirSync","node:fs"] |
| flatRoutes | node:path | 3 | 13 | 13 | 15 | 5 | 115.38461538461539 | ["node:path"] |
| flatRoutes | esm | 1 | 1 | 13 | 15 | 5 | 115.38461538461539 | ["makeRe"] |
| cookies | dist | 7 | 33 | 6 | 6 | 2 | 100 | ["ParseOptions","StringifyOptions","SerializeOptions","parse","serialize","Cookies.name"] |
| copy-template | node:url | 2 | 2 | 2 | 2 | 1 | 100 | [".fileURLToPath","node:url"] |
| detectPackageManager | @types/process | 1 | 1 | 1 | 1 | 1 | 100 | ["global.NodeJS.Process.env"] |
| has-dependency | @types/module | 1 | 1 | 1 | 1 | 1 | 100 | ["global.NodeJS.Require.resolve"] |
| virtual-route-modules | @types/babel__generator | 2 | 2 | 4 | 4 | 2 | 100 | ["GeneratorResult.code","GeneratorResult"] |
| virtual-route-modules | lexer | 2 | 2 | 4 | 4 | 2 | 100 | ["parse","init"] |
| babel | @types/babel__generator | 1 | 1 | 2 | 1 | 1 | 50 | ["generate"] |
| sessions | dist | 6 | 67 | 11 | 5 | 1 | 45.45454545454546 | ["ParseOptions","StringifyOptions","SerializeOptions","SerializeOptions.maxAge","SerializeOptions.expires"] |
| context | @types/react | 27 | 65 | 21 | 9 | 1 | 42.857142857142854 | ["React.createContext","React.Context","React.ReactElement","React.ReactNode","React.useContext","React.Context.Provider","React.createElement","React.ProviderProps","React.FunctionComponentElement"] |
| generate | dist | 4 | 4 | 5 | 2 | 2 | 40 | ["join"] |
| generate | @types/babel__generator | 1 | 3 | 5 | 2 | 2 | 40 | ["GeneratorResult.code"] |
| utils | @types/process | 7 | 9 | 149 | 29 | 12 | 19.46308724832215 | ["global.NodeJS.Process.stdout","global.NodeJS.WriteStream","global.NodeJS.ProcessEnv.TERM","global.NodeJS.Process.env","global.NodeJS.Process.stderr"] |
| utils | @types/react | 6 | 27 | 149 | 29 | 12 | 19.46308724832215 | ["React.ReactNode","React.FunctionComponent","React.ComponentClass"] |
| utils | node:fs | 6 | 6 | 149 | 29 | 12 | 19.46308724832215 | [".promises","node:fs"] |
| utils | sisteransi | 5 | 6 | 149 | 29 | 12 | 19.46308724832215 | ["cursor.to","cursor","erase.lines","erase","erase.line"] |
| utils | node:process | 4 | 8 | 149 | 29 | 12 | 19.46308724832215 | ["node:process"] |
| utils | promises | 4 | 4 | 149 | 29 | 12 | 19.46308724832215 | [".stat","readdir",".mkdir"] |
| utils | readline | 4 | 26 | 149 | 29 | 12 | 19.46308724832215 | ["Key.name","Key","Key.meta","Key.ctrl"] |
| utils | node:path | 3 | 7 | 149 | 29 | 12 | 19.46308724832215 | ["node:path"] |
| utils | @types/path | 2 | 5 | 149 | 29 | 12 | 19.46308724832215 | ["path.PlatformPath.sep"] |
| utils | fs | 2 | 2 | 149 | 29 | 12 | 19.46308724832215 | ["Stats.isFile","Stats.isDirectory"] |
| utils | picocolors | 1 | 39 | 149 | 29 | 12 | 19.46308724832215 | ["picocolors"] |
| utils | types | 1 | 2 | 149 | 29 | 12 | 19.46308724832215 | ["Formatter"] |
| build | node | 1 | 1 | 7 | 1 | 1 | 14.285714285714286 | ["version"] |
| routeModules | @types/react | 12 | 170 | 21 | 3 | 1 | 14.285714285714285 | ["React.FunctionComponent","React.ComponentClass","React.ReactElement"] |
| fog-of-war | @types/react | 1 | 1 | 8 | 1 | 1 | 12.5 | ["React.useEffect"] |
| react-router | @types/react | 31 | 79 | 178 | 19 | 4 | 10.674157303370787 | ["React.Context.Provider","React.createElement","React.ProviderProps","React.FunctionComponentElement","React.ReactNode","React.ReactElement","React.Fragment","React.FunctionComponent","React.ComponentClass","React.createContext","React.Context","React.useEffect"] |
| react-router | dist | 7 | 33 | 178 | 19 | 4 | 10.674157303370787 | ["ParseOptions","StringifyOptions","SerializeOptions","parse","serialize","Cookies.name"] |
| react-router | async_hooks | 4 | 4 | 178 | 19 | 4 | 10.674157303370787 | ["AsyncLocalStorage.getStore"] |

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
| react-router | 29 | 0 | ["@playground/perf-routes","@playground/split-route-modules","@playground/framework","@playground/framework-vite-7-beta","@playground/rsc-vite-7-framework","@playground/framework-vite-6","@playground/rsc-vite","@playground/split-route-modules-spa","react-router-scripts"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/performance","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/split-route-modules","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework-vite-7-beta"] |
| react | 26 | 0 | ["@playground/perf-routes","@playground/split-route-modules","@playground/framework","@playground/framework-vite-7-beta","@playground/rsc-vite-7-framework","@playground/framework-vite-6","@playground/rsc-vite","@playground/split-route-modules-spa","integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/performance","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/split-route-modules","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework-vite-7-beta"] |
| react-dom | 26 | 0 | ["@playground/perf-routes","@playground/split-route-modules","@playground/framework","@playground/framework-vite-7-beta","@playground/rsc-vite-7-framework","@playground/framework-vite-6","@playground/rsc-vite","@playground/split-route-modules-spa","integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/performance","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/split-route-modules","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework-vite-7-beta"] |
| isbot | 22 | 0 | ["@playground/perf-routes","@playground/split-route-modules","@playground/framework","@playground/framework-vite-7-beta","@playground/framework-vite-6","@playground/split-route-modules-spa","integration","integration-vite-8-template","integration-vite-6-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/performance","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/split-route-modules","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework-vite-7-beta"] |
| @react-router/node | 21 | 0 | ["@playground/perf-routes","@playground/split-route-modules","@playground/framework","@playground/framework-vite-7-beta","@playground/framework-vite-6","@playground/split-route-modules-spa","integration","integration-vite-8-template","integration-vite-6-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/performance","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/split-route-modules","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework-vite-7-beta"] |
| express | 15 | 0 | ["@playground/rsc-vite-7-framework","@playground/rsc-vite","integration","integration-vite-8-template","integration-vite-6-template","integration-rsc-vite-framework","integration-vite-plugin-cloudflare-template","integration-vite-5-template","integration-rsc-vite"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/rsc-vite-7-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-8-template"] |
| @react-router/serve | 13 | 0 | ["@playground/perf-routes","@playground/split-route-modules","@playground/framework","@playground/framework-vite-7-beta","@playground/framework-vite-6","integration-vite-8-template","integration-vite-6-template","integration-rsc-vite-framework","integration-vite-5-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/performance","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/split-route-modules","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework-vite-7-beta"] |
| compression | 8 | 0 | ["@playground/rsc-vite-7-framework","@playground/rsc-vite","integration-rsc-vite-framework","integration-rsc-vite","@react-router/serve","@playground/middleware","@playground/rsc-vite-framework","@playground/framework-express"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/rsc-vite-7-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/rsc-vite-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/rsc-vite"] |
| @react-router/express | 8 | 0 | ["integration","integration-vite-8-template","integration-vite-6-template","integration-vite-5-template","integration-vite-7-beta-template","@react-router/serve","@playground/middleware","@playground/framework-express"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-8-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-6-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-5-template"] |
| @mjackson/node-fetch-server | 7 | 0 | ["@playground/rsc-vite-7-framework","@playground/rsc-vite","integration-rsc-vite-framework","integration-rsc-vite","@react-router/serve","@react-router/node","@playground/rsc-vite-framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/rsc-vite-7-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/rsc-vite-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/rsc-vite"] |
| serialize-javascript | 7 | 0 | ["integration","integration-vite-8-template","integration-vite-6-template","integration-vite-plugin-cloudflare-template","integration-vite-5-template","integration-vite-7-beta-template","@playground/vite-plugin-cloudflare"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-8-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-6-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-plugin-cloudflare-template"] |
| react-server-dom-webpack | 6 | 0 | ["@playground/rsc-vite-7-framework","@playground/rsc-vite","integration","integration-rsc-vite-framework","integration-rsc-vite","@playground/rsc-vite-framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/rsc-vite-7-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/rsc-vite-framework"] |
| semver | 5 | 0 | ["react-router-scripts","integration","@remix-run/react-router","create-react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/scripts","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router"] |
| @vanilla-extract/vite-plugin | 5 | 0 | ["integration","integration-vite-8-template","integration-vite-6-template","integration-vite-5-template","integration-vite-7-beta-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-8-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-6-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-5-template"] |
| @vanilla-extract/css | 5 | 0 | ["integration","integration-vite-8-template","integration-vite-6-template","integration-vite-5-template","integration-vite-7-beta-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-8-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-6-template","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/vite-5-template"] |
| prettier | 3 | 0 | ["integration","@remix-run/react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| picocolors | 3 | 0 | ["@remix-run/react-router","create-react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| morgan | 3 | 0 | ["@react-router/serve","@playground/middleware","@playground/framework-express"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-serve","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/middleware","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/framework-express"] |
| remix-utils | 2 | 0 | ["@playground/rsc-vite-7-framework","@playground/rsc-vite-framework"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/rsc-vite-7-framework","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/rsc-vite-framework"] |
| @mdx-js/rollup | 2 | 0 | ["integration","@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| get-port | 2 | 0 | ["integration","@react-router/serve"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-serve"] |
| typescript | 2 | 0 | ["integration","@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| strip-ansi | 2 | 0 | ["integration","create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router"] |
| vite | 2 | 0 | ["integration","@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| @playwright/test | 2 | 0 | ["integration","@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| dedent | 2 | 0 | ["integration","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| pathe | 2 | 0 | ["integration","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| execa | 2 | 0 | ["integration","create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router"] |
| cross-env | 2 | 0 | ["integration-rsc-vite","@playground/middleware"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/rsc-vite","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/playground/middleware"] |
| @babel/core | 2 | 0 | ["@remix-run/react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| @babel/preset-typescript | 2 | 0 | ["@remix-run/react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| arg | 2 | 0 | ["create-react-router","@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router","/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| @octokit/request | 1 | 0 | ["react-router-scripts"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/scripts"] |
| @types/express | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| wait-on | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| cross-spawn | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| strip-indent | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| @types/semver | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| @react-router/dev | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| @types/cross-spawn | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| @types/dedent | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| vite-env-only | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| type-fest | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| postcss-import | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| vite-tsconfig-paths | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| postcss | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| shelljs | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| @types/shelljs | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| cheerio | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| glob | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| @types/glob | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| @types/wait-on | 1 | 0 | ["integration"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration"] |
| match-sorter | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/tutorials/address-book"] |
| tiny-invariant | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/tutorials/address-book"] |
| sort-by | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/tutorials/address-book"] |
| miniflare | 1 | 0 | ["integration-cloudflare-dev-proxy-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/cloudflare-dev-proxy-template"] |
| @react-router/cloudflare | 1 | 0 | ["integration-cloudflare-dev-proxy-template"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/integration/helpers/cloudflare-dev-proxy-template"] |
| set-cookie-parser | 1 | 0 | ["react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router"] |
| cookie | 1 | 0 | ["react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router"] |
| eslint | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| eslint-plugin-jsdoc | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| @types/react | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| fast-glob | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| jsonfile | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| remark-stringify | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| eslint-plugin-react-hooks | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| prompts | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| @babel/preset-env | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| @types/react-test-renderer | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| jest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| @typescript-eslint/parser | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| eslint-config-react-app | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| @types/jest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| @manypkg/get-packages | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| unified | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| typedoc | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| unist-util-remove | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| remark-gfm | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| eslint-plugin-react | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| remark-parse | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| babel-plugin-dev-expression | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| babel-jest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| vitest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| eslint-plugin-jsx-a11y | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| @types/react-dom | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| eslint-plugin-import | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| dox | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| @eslint/compat | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| @types/jsdom | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| @babel/preset-react | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| eslint-plugin-flowtype | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| @typescript-eslint/eslint-plugin | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| eslint-plugin-jest | 1 | 0 | ["@remix-run/react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3"] |
| source-map-support | 1 | 0 | ["@react-router/serve"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-serve"] |
| minimatch | 1 | 0 | ["@react-router/fs-routes"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-fs-routes"] |
| react-router-dom | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router/__tests__/fixtures/basic"] |
| not-react-router | 1 | 0 | [] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router/__tests__/fixtures/basic"] |
| sort-package-json | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router"] |
| proxy-agent | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router"] |
| tar-fs | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router"] |
| @remix-run/web-fetch | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router"] |
| log-update | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router"] |
| sisteransi | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router"] |
| gunzip-maybe | 1 | 0 | ["create-react-router"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/create-react-router"] |
| exit-hook | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| @babel/plugin-syntax-jsx | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| @babel/traverse | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| @babel/parser | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| p-map | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| lodash | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| tinyglobby | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| @babel/generator | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| es-module-lexer | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| @babel/types | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| valibot | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| react-refresh | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| chokidar | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| babel-dead-code-elimination | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| @remix-run/node-fetch-server | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| pkg-types | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| jsesc | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| vite-node | 1 | 0 | ["@react-router/dev"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-dev"] |
| @architect/functions | 1 | 0 | ["@react-router/architect"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-architect"] |
| @types/aws-lambda | 1 | 0 | ["@react-router/architect"] | [] | ["/home/runner/work/code-graph-analysis-examples/code-graph-analysis-examples/temp/react-router-7.18.3/./source/react-router-7.18.3/packages/react-router-architect"] |

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
