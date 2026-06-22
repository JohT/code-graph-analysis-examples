---
title: "Java Report"
generated: "2026-06-22"
model_version: "v4.0.1"
dataset: "AxonFramework-5.1.1"
authors: ["JohT/code-graph-analysis-pipeline"]
---

# ☕ Java Report

## 1. Overview

Analyzes the Java codebase:

- **Artifact dependencies** — which artifacts depend on which, and spread across modules
- **Method metrics** — effective LOC per type and package
- **Java code quality** — annotation usage, deprecated element usages, and reflection
- **Web framework annotations** — Spring Web and Jakarta EE REST endpoints

> High dependency counts may indicate coupling hotspots.  
> Deprecated element usages should be migrated to their replacements.

## 📚 Table of Contents

1. [Overview](#1-overview)
1. [Artifact Dependencies](#2-artifact-dependencies)
1. [Method Metrics](#3-method-metrics)
1. [Java Code Quality](#4-java-code-quality)
1. [Web Framework Annotations](#5-web-framework-annotations)
1. [Duplicate Package Names](#6-duplicate-package-names)
1. [Dependency Spread](#7-dependency-spread)
1. [Glossary and Column Definitions](#8-glossary-and-column-definitions)

---

## 2. Artifact Dependencies

Maven artifact dependencies. High incoming = central/shared; high outgoing = depends on many others.

### 2.1 Incoming Artifact Dependencies

| a.fileName | incomingDependencies | incomingDependenciesWeight |
| --- | --- | --- |
| /axon-eventsourcing-5.1.1.jar | 2 | 92 |
| /axon-update-5.1.1.jar | 0 | 0 |
| /axon-tracing-opentelemetry-5.1.1.jar | 0 | 0 |
| /axoniq-spring-boot-autoconfigure-5.1.1.jar | 0 | 0 |
| /axon-common-5.1.1.jar | 10 | 1728 |
| /axon-test-5.1.1.jar | 0 | 0 |
| /axon-conversion-5.1.1.jar | 5 | 112 |
| /axon-metrics-micrometer-5.1.1.jar | 0 | 0 |
| /axon-server-connector-5.1.1.jar | 1 | 16 |
| /axon-modelling-5.1.1.jar | 2 | 64 |

[Full data](./IncomingDependencies.csv)

### 2.2 Outgoing Artifact Dependencies

| a.fileName | outgoingDependencies | outgoingDependenciesWeight |
| --- | --- | --- |
| /axon-eventsourcing-5.1.1.jar | 4 | 702 |
| /axon-update-5.1.1.jar | 1 | 54 |
| /axon-tracing-opentelemetry-5.1.1.jar | 2 | 24 |
| /axoniq-spring-boot-autoconfigure-5.1.1.jar | 4 | 58 |
| /axon-common-5.1.1.jar | 0 | 0 |
| /axon-test-5.1.1.jar | 3 | 290 |
| /axon-conversion-5.1.1.jar | 1 | 34 |
| /axon-metrics-micrometer-5.1.1.jar | 2 | 82 |
| /axon-server-connector-5.1.1.jar | 5 | 504 |
| /axon-modelling-5.1.1.jar | 3 | 500 |

[Full data](./OutgoingDependencies.csv)

### 2.3 Most Used Internal Dependencies

| dependency | usedByPackages | usedByTypes | providesPackages | providesTypes | interfaceRate | someProvidedPackages | someProvidedTypes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| axon-common-5.1.1 | 94 | 459 | 12 | 73 | 39.73 | ["org.axonframework.common","org.axonframework.common.lifecycle","org.axonframework.common.property","org.axonframework.common.function","org.axonframework.common.io"] | ["Priority","TypeReference","IdentifierFactory","DateTimeUtils","ObjectUtils"] |
| axon-messaging-5.1.1 | 33 | 188 | 31 | 107 | 52.34 | ["org.axonframework.messaging.commandhandling","org.axonframework.messaging.commandhandling.annotation","org.axonframework.messaging.commandhandling.configuration","org.axonframework.messaging.eventhandling","org.axonframework.messaging.eventhandling.conversion"] | ["GenericCommandResultMessage","CommandMessage","CommandHandlerRegistry","CommandBus","CommandExecutionException"] |
| axon-conversion-5.1.1 | 25 | 48 | 2 | 6 | 33.33 | ["org.axonframework.conversion","org.axonframework.conversion.jackson"] | ["Converter","CachingSupplier","DelegatingGeneralConverter","GeneralConverter","ConversionException"] |
| axon-modelling-5.1.1 | 6 | 18 | 6 | 16 | 68.75 | ["org.axonframework.modelling","org.axonframework.modelling.entity","org.axonframework.modelling.entity.annotation","org.axonframework.modelling.repository","org.axonframework.modelling.annotation"] | ["StateManager","EntityIdResolver","EntityEvolver","ConcurrencyException","EntityCommandHandlingComponent"] |
| axon-eventsourcing-5.1.1 | 5 | 13 | 3 | 20 | 45 | ["org.axonframework.eventsourcing.snapshot.api","org.axonframework.eventsourcing.snapshot.store","org.axonframework.eventsourcing.eventstore"] | ["Snapshot","SnapshotStore","EventStoreTransaction","EventStore","EmptyAppendTransaction"] |
| axon-server-connector-5.1.1 | 3 | 5 | 2 | 5 | 20 | ["io.axoniq.framework.axonserver.connector.api","io.axoniq.framework.axonserver.connector.configuration"] | ["AxonServerConnectionManager","TagsConfiguration","AxonServerConfiguration","TopologyChangeListener","AxonServerConfigurationEnhancer"] |

[Full data](./MostUsedDependenciesAcrossArtifacts.csv)

### 2.4 All Artifact Dependencies

| artifactName | packagesInArtifactCount | packagesCount | packageSpread | typesInArtifactCount | typesCount | typesSpread | dependencyArtifactName | dependencyTypeIsInterface | dependencyPackagesCount | dependencyTypesCount | someDependencyPackages | someDependencyTypes | someCallingPackages | someCallingTypes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| axon-messaging-5.1.1 | 57 | 50 | 87.72 | 633 | 214 | 33.81 | axon-common-5.1.1 | false | 7 | 36 | ["org.axonframework.common","org.axonframework.common.property"] | ["Priority","TypeReference","IdentifierFactory","DateTimeUtils"] | ["org.axonframework.messaging.eventhandling.annotation","org.axonframework.messaging.core.annotation"] | ["TimestampParameterResolverFactory","MessageIdentifierParameterResolverFactory","SourceIdParameterResolverFactory","InterceptorChainParameterResolverFactory"] |
| axon-messaging-5.1.1 | 57 | 37 | 64.91 | 633 | 108 | 17.06 | axon-common-5.1.1 | true | 8 | 24 | ["org.axonframework.common","org.axonframework.common.property"] | ["Registration","Property","ThrowingFunction","ComponentDescriptor"] | ["org.axonframework.messaging.eventhandling","org.axonframework.messaging.eventhandling.processing.subscribing"] | ["DelegatingEventBus","InterceptingEventBus","EventSubscribers","SubscribingEventProcessor"] |
| axon-messaging-5.1.1 | 57 | 14 | 24.56 | 633 | 36 | 5.69 | axon-conversion-5.1.1 | true | 1 | 2 | ["org.axonframework.conversion"] | ["Converter","GeneralConverter"] | ["org.axonframework.messaging.eventhandling.processing.streaming.token","org.axonframework.messaging.eventhandling.conversion"] | ["ReplayToken","DelegatingEventConverter","ResetContext","GenericReplayStatusChanged"] |
| axon-eventsourcing-5.1.1 | 11 | 10 | 90.91 | 128 | 37 | 28.91 | axon-messaging-5.1.1 | false | 8 | 20 | ["org.axonframework.messaging.eventhandling","org.axonframework.messaging.eventhandling.processing.streaming.token"] | ["GenericEventMessage","SimpleEventBus","InterceptingEventBus","GlobalSequenceTrackingToken"] | ["org.axonframework.eventsourcing.eventstore","org.axonframework.eventsourcing.handler"] | ["SnapshotEventMessage","SnapshottingEntityLifecycleHandler","TerminalEventMessage","AggregateBasedJpaEventStorageEngine"] |
| axon-eventsourcing-5.1.1 | 11 | 9 | 81.82 | 128 | 54 | 42.19 | axon-messaging-5.1.1 | true | 13 | 30 | ["org.axonframework.messaging.commandhandling","org.axonframework.messaging.commandhandling.configuration"] | ["CommandBus","CommandHandlingComponent","CommandHandlingModule","EventMessage"] | ["org.axonframework.eventsourcing.configuration","org.axonframework.eventsourcing.snapshot.api"] | ["SimpleEventSourcedEntityModule","EventSourcingConfigurer","SnapshotPolicy$2","SnapshotPolicy$1"] |
| axon-server-connector-5.1.1 | 10 | 8 | 80 | 79 | 27 | 34.18 | axon-common-5.1.1 | false | 5 | 16 | ["org.axonframework.common","org.axonframework.common.lifecycle"] | ["ObjectUtils","Assert","ExceptionUtils","FutureUtils"] | ["io.axoniq.framework.axonserver.connector.command","io.axoniq.framework.axonserver.connector.api"] | ["CommandConverter","AxonServerConnectionManager$Builder","ExceptionConverter","AxonServerCommandBusConnector"] |
| axon-eventsourcing-5.1.1 | 11 | 8 | 72.73 | 128 | 29 | 22.66 | axon-common-5.1.1 | true | 6 | 17 | ["org.axonframework.common","org.axonframework.common.infra"] | ["Registration","ComponentDescriptor","DescribableComponent","PersistenceExceptionResolver"] | ["org.axonframework.eventsourcing.eventstore","org.axonframework.eventsourcing.eventstore.jpa"] | ["StorageEngineBackedEventStore","InterceptingEventStore","AggregateBasedJpaEventStorageEngine","ContinuousMessageStream"] |
| axon-modelling-5.1.1 | 7 | 7 | 100 | 99 | 23 | 23.23 | axon-common-5.1.1 | false | 4 | 13 | ["org.axonframework.common","org.axonframework.common.property"] | ["TypeReference","ReflectionUtils","ConstructorUtils","Assert"] | ["org.axonframework.modelling.configuration","org.axonframework.modelling.entity.annotation"] | ["SimpleStateBasedEntityModule$3","SimpleStateBasedEntityModule$1","SimpleStateBasedEntityModule$2","SingleEntityChildModelDefinition"] |
| axon-eventsourcing-5.1.1 | 11 | 7 | 63.64 | 128 | 41 | 32.03 | axon-common-5.1.1 | false | 4 | 16 | ["org.axonframework.common","org.axonframework.common.io"] | ["TypeReference","DateTimeUtils","ObjectUtils","ReflectionUtils"] | ["org.axonframework.eventsourcing.configuration","org.axonframework.eventsourcing.eventstore.jpa"] | ["SimpleEventSourcedEntityModule$5","SimpleEventSourcedEntityModule$2","AggregateBasedJpaEventStorageEngine","SimpleEventSourcedEntityModule$4"] |
| axon-modelling-5.1.1 | 7 | 7 | 100 | 99 | 30 | 30.3 | axon-common-5.1.1 | true | 3 | 14 | ["org.axonframework.common.property","org.axonframework.common.infra"] | ["Property","ComponentDescriptor","DescribableComponent","ModuleBuilder"] | ["org.axonframework.modelling","org.axonframework.modelling.entity.annotation"] | ["PropertyBasedEntityIdResolver","AnnotatedEntityModelRoutingKeyMatcher","SimpleStateManager","AnnotatedEntityMetamodel"] |

[Full data](./DependenciesAcrossArtifacts.csv)

### 2.5 Artifact Dependency Charts


![ArtifactDependencies_IncomingTop20_Bar](./ArtifactDependencies_IncomingTop20_Bar.svg)

![ArtifactDependencies_MostUsedTop20_Bar](./ArtifactDependencies_MostUsedTop20_Bar.svg)

![ArtifactDependencies_OutgoingTop20_Bar](./ArtifactDependencies_OutgoingTop20_Bar.svg)

![ArtifactDependencies_SpreadPerDependency_Bar](./ArtifactDependencies_SpreadPerDependency_Bar.svg)

![ArtifactDependencies_SpreadPerDependent_Bar](./ArtifactDependencies_SpreadPerDependent_Bar.svg)

---

## 3. Method Metrics

Effective Lines Of Code (LOC) per type and package. High values = complex or large.

### 3.1 Effective Method Line Count Distribution

| artifactName | effectiveLineCount | methods |
| --- | --- | --- |
| axon-common-5.1.1.jar | 1 | 392 |
| axon-common-5.1.1.jar | 2 | 152 |
| axon-common-5.1.1.jar | 3 | 101 |
| axon-common-5.1.1.jar | 4 | 37 |
| axon-common-5.1.1.jar | 5 | 38 |
| axon-common-5.1.1.jar | 6 | 38 |
| axon-common-5.1.1.jar | 7 | 19 |
| axon-common-5.1.1.jar | 8 | 18 |
| axon-common-5.1.1.jar | 9 | 12 |
| axon-common-5.1.1.jar | 10 | 6 |

[Full data](./EffectiveMethodLineCountDistribution.csv)

### 3.2 Top Types by Effective LOC

| artifactName | packageName | typeName | sumEffectiveLinesOfMethodCode | maxEffectiveLinesOfMethodCode | methodWithMaxEffectiveLinesOfMethodCode | maxCyclomaticComplexity | methodWithMaxCyclomaticComplexity |
| --- | --- | --- | --- | --- | --- | --- | --- |
| axon-messaging-5.1.1 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | Coordinator$CoordinationTask | 398 | 111 | run | 25 | run |
| axon-messaging-5.1.1 | org.axonframework.messaging.eventhandling.processing.streaming.token.store.jdbc | JdbcTokenStore | 305 | 25 | updateToken | 8 | updateToken |
| axon-test-5.1.1 | org.axonframework.test.fixture | Reporter | 224 | 45 | appendEventOverview | 11 | appendEventOverview |
| axon-eventsourcing-5.1.1 | org.axonframework.eventsourcing.eventstore.jpa | AggregateBasedJpaEventStorageEngine | 193 | 17 | <init> | 5 | lambda$queryTokensAndEventsBy$16 |
| axon-messaging-5.1.1 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | WorkPackage | 190 | 25 | processEvents | 7 | processEvents |
| axon-common-5.1.1 | org.axonframework.common.configuration | DefaultComponentRegistry | 185 | 18 | invokeEnhancers | 8 | hasComponent |
| axon-common-5.1.1 | org.axonframework.common | ReflectionUtils | 177 | 17 | fieldNameFromMember | 9 | fieldNameFromMember |
| axon-messaging-5.1.1 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | PooledStreamingEventProcessor | 175 | 37 | <init> | 3 | lambda$new$0 |
| axon-modelling-5.1.1 | org.axonframework.modelling.entity.annotation | AnnotatedEntityMetamodel | 166 | 18 | createOptionalChildForMember | 6 | getExpectedRepresentation |
| axon-messaging-5.1.1 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | PooledStreamingEventProcessorConfiguration | 160 | 18 | describeTo | 2 | interceptors |

[Full data](./EffectiveLinesOfMethodCodePerType.csv)

### 3.3 Top Packages by Effective LOC

| artifactName | fullPackageName | linesInPackage | complexityInPackage | methodCount | maxLinesMethod | maxLinesMethodType | maxLinesMethodName | maxComplexity | maxComplexityType | maxComplexityMethod | packageName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| axon-messaging-5.1.1 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | 1496 | 586 | 428 | 111 | Coordinator$CoordinationTask | run | 25 | Coordinator$CoordinationTask | run | pooled |
| axon-messaging-5.1.1 | org.axonframework.messaging.core | 1183 | 738 | 519 | 23 | AbstractMessageStream | next | 11 | AbstractMessageStream | next | core |
| axon-common-5.1.1 | org.axonframework.common.configuration | 766 | 411 | 303 | 26 | DefaultAxonApplication$AxonConfigurationImpl | invokeLifecycleHandlers | 8 | DefaultComponentRegistry | hasComponent | configuration |
| axon-test-5.1.1 | org.axonframework.test.fixture | 752 | 324 | 211 | 45 | Reporter | appendEventOverview | 11 | Reporter | appendEventOverview | fixture |
| axon-messaging-5.1.1 | org.axonframework.messaging.core.annotation | 713 | 379 | 239 | 23 | MethodInvokingMessageHandlingMember | <init> | 13 | MessageStreamResolverUtils | resolveToStream | annotation |
| axon-eventsourcing-5.1.1 | org.axonframework.eventsourcing.eventstore | 679 | 434 | 278 | 19 | AnnotationBasedTagResolver | createTagsForValue | 8 | AggregateBasedConsistencyMarker | from | eventstore |
| axon-common-5.1.1 | org.axonframework.common | 654 | 408 | 194 | 24 | TypeReflectionUtils | getExactDirectSuperTypesOfParameterizedTypeOrClass | 9 | TypeReflectionUtils | getExactDirectSuperTypesOfParameterizedTypeOrClass | common |
| axon-server-connector-5.1.1 | io.axoniq.framework.axonserver.connector.event | 541 | 217 | 161 | 21 | AggregateBasedAxonServerEventStorageEngine | lambda$appendEvents$0 | 4 | EventProcessorControlService$AxonProcessorInstructionHandler | releaseSegment | event |
| axon-messaging-5.1.1 | org.axonframework.messaging.eventhandling.processing.streaming.token.store.jdbc | 443 | 194 | 109 | 25 | JdbcTokenStore | updateToken | 8 | JdbcTokenStore | updateToken | jdbc |
| axon-eventsourcing-5.1.1 | org.axonframework.eventsourcing.eventstore.jpa | 439 | 207 | 135 | 20 | GapAwareTrackingTokenOperations | withGapsCleaned | 8 | GapAwareTrackingTokenOperations | withGapsCleaned | jpa |

[Full data](./EffectiveLinesOfMethodCodePerPackage.csv)

### 3.4 Method Metrics Charts


![MethodMetrics_CyclomaticComplexityDistribution_Normalized](./MethodMetrics_CyclomaticComplexityDistribution_Normalized.svg)

![MethodMetrics_LineCountDistribution_Histogram](./MethodMetrics_LineCountDistribution_Histogram.svg)

![MethodMetrics_TopPackagesLOC_Bar](./MethodMetrics_TopPackagesLOC_Bar.svg)

![MethodMetrics_TopTypesLOC_Bar](./MethodMetrics_TopTypesLOC_Bar.svg)

---

## 4. Java Code Quality

Annotations, deprecated API usages, and reflection calls.

### 4.1 Annotated Code Elements

| annotationName | languageElement | numberOfAnnotatedElements | examples |
| --- | --- | --- | --- |
| org.jspecify.annotations.NullMarked | Interface | 124 | ["org.axonframework.eventsourcing.snapshot.api.package-info","org.axonframework.eventsourcing.snapshot.inmemory.package-info","org.axonframework.eventsourcing.snapshot.store.package-info","org.axonframework.eventsourcing.package-info","org.axonframework.eventsourcing.handler.package-info","org.axonframework.eventsourcing.eventstore.package-info","org.axonframework.eventsourcing.eventstore.inmemory.package-info","org.axonframework.eventsourcing.eventstore.jpa.package-info","org.axonframework.eventsourcing.annotation.package-info"] |
| org.axonframework.common.annotation.Internal | Class | 91 | ["org.axonframework.eventsourcing.handler.SimpleEntityLifecycleHandler","org.axonframework.eventsourcing.handler.InitializingEntityEvolver","org.axonframework.eventsourcing.handler.SnapshottingEntityLifecycleHandler","org.axonframework.eventsourcing.eventstore.InterceptingEventStore","org.axonframework.eventsourcing.eventstore.StreamSpliterator","org.axonframework.eventsourcing.eventstore.ContinuousMessageStream","org.axonframework.eventsourcing.eventstore.TerminalEventMessage","org.axonframework.eventsourcing.eventstore.SnapshotEventMessage","org.axonframework.eventsourcing.eventstore.SnapshotCapableEventStorageEngine"] |
| java.lang.FunctionalInterface | Interface | 57 | ["org.axonframework.eventsourcing.EventSourcedEntityFactory","org.axonframework.eventsourcing.eventstore.TagResolver","org.axonframework.eventsourcing.CriteriaResolver","org.axonframework.update.configuration.EnvironmentVariableUsagePropertyProvider$EnvironmentVariableSupplier","org.axonframework.common.Registration","org.axonframework.common.property.Property","org.axonframework.common.infra.DescribableComponent","org.axonframework.common.jdbc.JdbcUtils$SqlFunction","org.axonframework.common.jdbc.ConnectionProvider"] |
| java.lang.annotation.Retention | Annotation | 43 | ["org.axonframework.eventsourcing.annotation.EventTag","org.axonframework.eventsourcing.annotation.EventTags","org.axonframework.eventsourcing.annotation.Snapshotting","org.axonframework.eventsourcing.annotation.reflection.EntityCreator","org.axonframework.eventsourcing.annotation.EventSourcedEntity","org.axonframework.eventsourcing.annotation.EventCriteriaBuilder","org.axonframework.eventsourcing.annotation.reflection.InjectEntityId","org.axonframework.eventsourcing.annotation.EventSourcingHandler","org.axonframework.common.Priority"] |
| java.lang.annotation.Target | Annotation | 43 | ["org.axonframework.eventsourcing.annotation.EventTag","org.axonframework.eventsourcing.annotation.EventTags","org.axonframework.eventsourcing.annotation.Snapshotting","org.axonframework.eventsourcing.annotation.reflection.EntityCreator","org.axonframework.eventsourcing.annotation.EventSourcedEntity","org.axonframework.eventsourcing.annotation.EventCriteriaBuilder","org.axonframework.eventsourcing.annotation.reflection.InjectEntityId","org.axonframework.eventsourcing.annotation.EventSourcingHandler","org.axonframework.common.Priority"] |
| org.axonframework.common.annotation.Internal | Interface | 26 | ["org.axonframework.eventsourcing.snapshot.store.SnapshotStore","org.axonframework.eventsourcing.handler.SourcingHandler","org.axonframework.eventsourcing.eventstore.EventStorageEngine","org.axonframework.eventsourcing.eventstore.EventCoordinator","org.axonframework.update.configuration.UsagePropertyProvider","org.axonframework.common.jdbc.ConnectionProvider","org.axonframework.common.tx.TransactionalExecutor","org.axonframework.common.jpa.EntityManagerProvider","org.axonframework.common.configuration.ExtensibleConfigurer"] |
| org.axonframework.common.annotation.Internal | Constructor | 19 | ["org.axonframework.eventsourcing.eventstore.InterceptingEventStore.<init>","org.axonframework.eventsourcing.eventstore.AggregateSequenceNumberPosition.<init>","org.axonframework.eventsourcing.eventstore.GlobalIndexPosition.<init>","org.axonframework.conversion.jackson.JacksonConverter.<init>","org.axonframework.conversion.jackson2.Jackson2Converter.<init>","org.axonframework.conversion.avro.AvroConverter.<init>","org.axonframework.messaging.eventhandling.InterceptingEventBus.<init>","org.axonframework.messaging.eventhandling.processing.subscribing.SubscribingEventProcessorConfiguration.<init>","org.axonframework.messaging.eventhandling.processing.subscribing.SubscribingEventProcessorsConfigurer.<init>"] |
| java.lang.annotation.Documented | Annotation | 15 | ["org.axonframework.eventsourcing.annotation.Snapshotting","org.axonframework.eventsourcing.annotation.EventSourcingHandler","org.axonframework.common.annotation.Internal","org.axonframework.common.annotation.RegistrationScope","org.axonframework.modelling.entity.annotation.EntityMember","org.axonframework.messaging.commandhandling.annotation.CommandHandler","org.axonframework.messaging.eventhandling.replay.annotation.AllowReplay","org.axonframework.messaging.eventhandling.replay.annotation.DisallowReplay","org.axonframework.messaging.eventhandling.annotation.EventHandler"] |
| org.springframework.context.annotation.Bean | Method | 15 | ["io.axoniq.framework.springboot.autoconfig.AxonServerActuatorAutoConfiguration.axonServerHealthIndicator","io.axoniq.framework.springboot.autoconfig.AxonServerActuatorAutoConfiguration.axonServerStatusAggregator","io.axoniq.framework.springboot.autoconfig.PostgresqlAutoConfiguration.disablePostgresqlConfigurationEnhancer","io.axoniq.framework.springboot.autoconfig.JpaDeadLetterQueueAutoConfiguration.jpaDeadLetterQueueFactory","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.disableAxonServerConfigurationEnhancer","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.axonServerConfigurationEnhancer","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.axonServerConfigurationWithConnectionDetails","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.tagsConfiguration","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.topologyChangeListenerConfigurerModule"] |
| java.lang.Deprecated | Method | 13 | ["org.axonframework.eventsourcing.eventstore.SourcingCondition.start","org.axonframework.test.fixture.AxonTestThenCommand.resultMessagePayloadSatisfies","org.axonframework.test.fixture.AxonTestPhase$Then$Command.resultMessagePayloadSatisfies","io.axoniq.framework.axonserver.connector.api.AxonServerConfiguration.getQueryResponseThreads","io.axoniq.framework.axonserver.connector.api.AxonServerConfiguration.setQueryResponseThreads","org.axonframework.messaging.eventhandling.configuration.DefaultEventHandlingComponentsConfigurer.declarative","org.axonframework.messaging.eventhandling.configuration.EventHandlingComponentsConfigurer$ComponentsPhase.declarative","org.axonframework.messaging.eventhandling.configuration.EventHandlingComponentsConfigurer$ComponentsPhase.autodetected","org.axonframework.messaging.core.GenericResultMessage.asResultMessage"] |

[Full data](./AnnotatedCodeElements.csv)

### 4.2 Annotated Code Elements per Artifact

| artifactName | annotationName | languageElement | numberOfAnnotatedElements | examples |
| --- | --- | --- | --- | --- |
| axon-common-5.1.1 | org.jspecify.annotations.NullMarked | Interface | 15 | ["org.axonframework.common.lifecycle.package-info","org.axonframework.common.property.package-info","org.axonframework.common.package-info","org.axonframework.common.digest.package-info","org.axonframework.common.function.package-info","org.axonframework.common.io.package-info","org.axonframework.common.caching.package-info","org.axonframework.common.infra.package-info","org.axonframework.common.jdbc.package-info"] |
| axon-common-5.1.1 | java.lang.FunctionalInterface | Interface | 12 | ["org.axonframework.common.Registration","org.axonframework.common.property.Property","org.axonframework.common.infra.DescribableComponent","org.axonframework.common.jdbc.JdbcUtils$SqlFunction","org.axonframework.common.jdbc.ConnectionProvider","org.axonframework.common.jdbc.JdbcUtils$SqlResultConverter","org.axonframework.common.util.ExecutorServiceFactory","org.axonframework.common.lock.LockFactory","org.axonframework.common.configuration.ComponentLifecycleHandler"] |
| axon-common-5.1.1 | org.axonframework.common.annotation.Internal | Interface | 7 | ["org.axonframework.common.jdbc.ConnectionProvider","org.axonframework.common.tx.TransactionalExecutor","org.axonframework.common.jpa.EntityManagerProvider","org.axonframework.common.configuration.ExtensibleConfigurer","org.axonframework.common.configuration.ConfigurationExtension","org.axonframework.common.configuration.Component","org.axonframework.common.configuration.ExtendedConfiguration"] |
| axon-common-5.1.1 | org.axonframework.common.annotation.Internal | Class | 7 | ["org.axonframework.common.jdbc.JdbcUtils","org.axonframework.common.jdbc.ConnectionExecutor","org.axonframework.common.jpa.EntityManagerExecutor","org.axonframework.common.configuration.Components","org.axonframework.common.configuration.InstantiatedComponentDefinition","org.axonframework.common.configuration.LazyInitializedComponentDefinition","org.axonframework.common.configuration.ConfigurationExtensions"] |
| axon-common-5.1.1 | java.lang.annotation.Retention | Annotation | 3 | ["org.axonframework.common.Priority","org.axonframework.common.annotation.Internal","org.axonframework.common.annotation.RegistrationScope"] |
| axon-common-5.1.1 | java.lang.annotation.Target | Annotation | 3 | ["org.axonframework.common.Priority","org.axonframework.common.annotation.Internal","org.axonframework.common.annotation.RegistrationScope"] |
| axon-common-5.1.1 | java.lang.annotation.Documented | Annotation | 2 | ["org.axonframework.common.annotation.Internal","org.axonframework.common.annotation.RegistrationScope"] |
| axon-common-5.1.1 | org.axonframework.common.annotation.Internal | Method | 2 | ["org.axonframework.common.configuration.DefaultComponentRegistry.create","org.axonframework.common.configuration.DefaultComponentRegistry.createLocalConfiguration"] |
| axon-common-5.1.1 | java.lang.annotation.Inherited | Annotation | 1 | ["org.axonframework.common.Priority"] |
| axon-conversion-5.1.1 | org.jspecify.annotations.NullMarked | Interface | 5 | ["org.axonframework.conversion.jackson.package-info","org.axonframework.conversion.converter.package-info","org.axonframework.conversion.jackson2.package-info","org.axonframework.conversion.package-info","org.axonframework.conversion.avro.package-info"] |

[Full data](./AnnotatedCodeElementsPerArtifact.csv)

### 4.3 Deprecated Element Usages

| artifactName | deprecatedElement | numberOfElementsUsingDeprecatedElements | someElementsUsingDeprecatedElements |
| --- | --- | --- | --- |
| axon-eventsourcing-5.1.1 | Field | 2 | ["org.axonframework.eventsourcing.eventstore.jpa.GapAwareTrackingTokenOperations.gapTimeoutThreshold","org.axonframework.eventsourcing.handler.SnapshottingEntityLifecycleHandler.storeSnapshot"] |
| axon-messaging-5.1.1 | Method | 3 | ["org.axonframework.messaging.core.annotation.ChainedMessageHandlerInterceptorMember.doHandleSync","org.axonframework.messaging.core.annotation.WrappedMessageHandlingMember.handleSync","org.axonframework.messaging.core.interception.annotation.MessageHandlerInterceptorMemberChain.handle"] |
| axon-messaging-5.1.1 | Class | 1 | ["org.axonframework.messaging.core.interception.annotation.MessageHandlerInterceptorMemberChain"] |
| axon-messaging-5.1.1 | Field | 1 | ["org.axonframework.messaging.eventhandling.GenericEventMessage.<init>"] |
| axon-server-connector-5.1.1 | Method | 2 | ["io.axoniq.framework.axonserver.connector.event.AggregateBasedAxonServerEventStorageEngine.aggregateSourceForCriterion","io.axoniq.framework.axonserver.connector.event.ConditionConverter.convertSourcingCondition"] |

[Full data](./DeprecatedElementUsage.csv)

### 4.4 Reflection Usages

| dependentArtifactName | numberOfReflectionCaller | someReflectionCaller | someReflectionTypes |
| --- | --- | --- | --- |
| axon-eventsourcing-5.1.1 | 128 | ["org.axonframework.eventsourcing.annotation.AnnotationBasedEventCriteriaResolver","org.axonframework.eventsourcing.configuration.EventSourcedEntityModule$MessagingModelPhase","org.axonframework.eventsourcing.eventstore.SourcingStrategy$Snapshot","org.axonframework.eventsourcing.annotation.reflection.AnnotationBasedEventSourcedEntityFactoryDefinition","org.axonframework.eventsourcing.eventstore.AggregateBasedEventStorageEngineUtils","org.axonframework.eventsourcing.eventstore.AggregateBasedConsistencyMarker","org.axonframework.eventsourcing.eventstore.inmemory.InMemoryEventStorageEngine$1","org.axonframework.eventsourcing.configuration.AnnotatedEventSourcedEntityModule","org.axonframework.eventsourcing.eventstore.NoAppendCondition","org.axonframework.eventsourcing.eventstore.ConsistencyMarkers$OriginConsistencyMarker","org.axonframework.eventsourcing.eventstore.inmemory.InMemoryEventStorageEngine$MapBackedSourcingEventMessageStream","org.axonframework.eventsourcing.eventstore.EventCoordinator$Handle","org.axonframework.eventsourcing.snapshot.api.SnapshotPolicy$2","org.axonframework.eventsourcing.snapshot.inmemory.InMemorySnapshotStore","org.axonframework.eventsourcing.eventstore.StorageEngineBackedEventStore","org.axonframework.eventsourcing.annotation.EventSourcedEntity","org.axonframework.eventsourcing.handler.SnapshottingEntityLifecycleHandler","org.axonframework.eventsourcing.snapshot.inmemory.package-info","org.axonframework.eventsourcing.eventstore.ConsistencyMarkers"] | ["java.lang.reflect.Method","java.lang.reflect.Constructor","java.lang.reflect.Executable","java.lang.reflect.Modifier","java.lang.reflect.AnnotatedElement","java.lang.reflect.Field","java.lang.reflect.Member","java.lang.reflect.InvocationTargetException"] |
| axon-update-5.1.1 | 28 | ["org.axonframework.update.configuration.UsagePropertyProvider","org.axonframework.update.configuration.CommandLineUsagePropertyProvider","org.axonframework.update.detection.package-info","org.axonframework.update.api.Artifact","org.axonframework.update.UpdateCheckerHttpClient","org.axonframework.update.detection.TestEnvironmentDetector","org.axonframework.update.api.package-info","org.axonframework.update.detection.KotlinVersion","org.axonframework.update.configuration.EnvironmentVariableUsagePropertyProvider","org.axonframework.update.UpdateCheckerReporter","org.axonframework.update.detection.MachineId","org.axonframework.update.configuration.DefaultUsagePropertyProvider","org.axonframework.update.common.DelayedTask","org.axonframework.update.api.ArtifactAvailableUpgrade","org.axonframework.update.LoggingUpdateCheckerReporter","org.axonframework.update.api.DetectedVulnerabilitySeverity","org.axonframework.update.api.DetectedVulnerability","org.axonframework.update.detection.AxonVersionDetector","org.axonframework.update.api.UpdateCheckRequest"] | ["java.lang.reflect.Method"] |
| axon-tracing-opentelemetry-5.1.1 | 6 | ["org.axonframework.extension.tracing.opentelemetry.OpenTelemetrySpanFactory","org.axonframework.extension.tracing.opentelemetry.OpenTelemetrySpan","org.axonframework.extension.tracing.opentelemetry.MetadataContextSetter","org.axonframework.extension.tracing.opentelemetry.package-info","org.axonframework.extension.tracing.opentelemetry.OpenTelemetrySpanFactory$Builder","org.axonframework.extension.tracing.opentelemetry.MetadataContextGetter"] | [] |
| axoniq-spring-boot-autoconfigure-5.1.1 | 26 | ["io.axoniq.framework.springboot.package-info","io.axoniq.framework.springboot.autoconfig.JdbcDeadLetterQueueAutoConfiguration","io.axoniq.framework.springboot.DeadLetterQueueProcessorProperties","io.axoniq.framework.springboot.service.connection.AxonServerTestContainerConnectionDetailsFactory","io.axoniq.framework.springboot.autoconfig.PostgresqlAutoConfiguration$1","io.axoniq.framework.springboot.service.connection.AxonServerTestContainerConnectionDetailsFactory$AxonServerContainerConnectionDetails","io.axoniq.framework.springboot.autoconfig.AxonServerActuatorAutoConfiguration","io.axoniq.framework.springboot.autoconfig.PostgresqlAutoConfiguration","io.axoniq.framework.springboot.TagsConfigurationProperties","io.axoniq.framework.springboot.service.connection.package-info","io.axoniq.framework.springboot.actuator.axonserver.AxonServerHealthIndicator","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration$1","io.axoniq.framework.springboot.PostgresqlProperties","io.axoniq.framework.springboot.autoconfig.DeadLetterQueueAutoConfiguration","io.axoniq.framework.springboot.autoconfig.package-info","io.axoniq.framework.springboot.actuator.axonserver.AxonServerStatusAggregator","io.axoniq.framework.springboot.service.connection.AxonServerDockerComposeConnectionDetailsFactory","io.axoniq.framework.springboot.DeadLetterQueueProcessorProperties$Dlq","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration"] | [] |
| axon-common-5.1.1 | 175 | ["org.axonframework.common.TypeReflectionUtils$VarMap$UnresolvedTypeVariableException","org.axonframework.common.infra.FilesystemStyleComponentDescriptor$TreeRenderer$RenderContext","org.axonframework.common.ExceptionUtils","org.axonframework.common.configuration.ComponentOverrideException","org.axonframework.common.configuration.DecoratorDefinition$2","org.axonframework.common.BuilderUtils","org.axonframework.common.property.Property","org.axonframework.common.configuration.DecoratorDefinition$PartialDecoratorDefinition","org.axonframework.common.configuration.ComponentRegistry","org.axonframework.common.AxonException","org.axonframework.common.Priority","org.axonframework.common.jpa.SimpleEntityManagerProvider","org.axonframework.common.caching.EhCacheAdapter$CacheEventListenerAdapter","org.axonframework.common.configuration.ConfigurationExtensions","org.axonframework.common.jdbc.ConnectionWrapperFactory$ConnectionCloseHandler","org.axonframework.common.lock.PessimisticLockFactory$Builder","org.axonframework.common.caching.NoCache","org.axonframework.common.caching.JCacheAdapter","org.axonframework.common.util.ClasspathResolver"] | ["java.lang.reflect.TypeVariable","java.lang.reflect.ParameterizedType","java.lang.reflect.Type","java.lang.reflect.Field","java.lang.reflect.AccessibleObject","java.lang.reflect.Executable","java.lang.reflect.InvocationTargetException","java.lang.reflect.Member","java.lang.reflect.Method","java.lang.reflect.Modifier","java.lang.reflect.Array","java.lang.reflect.GenericArrayType","java.lang.reflect.WildcardType","java.lang.reflect.Proxy","java.lang.reflect.Constructor","java.lang.reflect.AnnotatedElement"] |
| axon-test-5.1.1 | 79 | ["org.axonframework.test.fixture.AxonTestPhase$Then$Message","org.axonframework.test.matchers.MapStringEntryMatcher$Matching","org.axonframework.test.fixture.AxonTestPhase","org.axonframework.test.fixture.AxonTestPhase$Setup","org.axonframework.test.util.RecordingMessageMonitor$1","org.axonframework.test.matchers.ListWithAnyOfMatcher","org.axonframework.test.matchers.DeepEqualsMatcher","org.axonframework.test.fixture.AxonTestFixture","org.axonframework.test.matchers.Matchers","org.axonframework.test.extension.AxonTestFixtureProvider","org.axonframework.test.util.MessageMonitorReport","org.axonframework.test.util.MessageMonitorReport$Report","org.axonframework.test.matchers.ExactSequenceMatcher","org.axonframework.test.fixture.AxonTestPhase$Then","org.axonframework.test.fixture.AxonTestPhase$Given","org.axonframework.test.fixture.CommandValidator","org.axonframework.test.matchers.IgnoreField","org.axonframework.test.fixture.RecordingCommandBus","org.axonframework.test.fixture.AxonTestThenEvent"] | ["java.lang.reflect.Field","java.lang.reflect.Parameter","java.lang.reflect.Modifier","java.lang.reflect.AnnotatedElement","java.lang.reflect.Constructor","java.lang.reflect.Method","java.lang.reflect.Executable"] |
| axon-conversion-5.1.1 | 41 | ["org.axonframework.conversion.converter.InputStreamToByteArrayConverter","org.axonframework.conversion.Converter","org.axonframework.conversion.jackson.ObjectNodeToJsonNodeConverter","org.axonframework.conversion.avro.SpecificRecordBaseConverterStrategy","org.axonframework.conversion.jackson2.JsonNodeToObjectNodeConverter","org.axonframework.conversion.package-info","org.axonframework.conversion.avro.ByteArrayToGenericRecordConverter","org.axonframework.conversion.converter.StringToByteArrayConverter","org.axonframework.conversion.jackson.package-info","org.axonframework.conversion.jackson.JacksonConverter","org.axonframework.conversion.ChainedConverter","org.axonframework.conversion.GeneralConverter","org.axonframework.conversion.jackson2.Jackson2Converter","org.axonframework.conversion.converter.ByteArrayToStringConverter","org.axonframework.conversion.DelegatingGeneralConverter","org.axonframework.conversion.PassThroughConverter","org.axonframework.conversion.ChainedConverter$RouteCalculator","org.axonframework.conversion.avro.AvroConverterConfiguration","org.axonframework.conversion.avro.AvroUtil"] | ["java.lang.reflect.Type","java.lang.reflect.InvocationTargetException","java.lang.reflect.Method","java.lang.reflect.Constructor"] |
| axon-metrics-micrometer-5.1.1 | 19 | ["org.axonframework.extension.metrics.micrometer.MessageCountingMonitor$1","org.axonframework.extension.metrics.micrometer.springboot.package-info","org.axonframework.extension.metrics.micrometer.MessageTimerMonitor","org.axonframework.extension.metrics.micrometer.springboot.MetricsProperties","org.axonframework.extension.metrics.micrometer.springboot.MetricsProperties$Micrometer","org.axonframework.extension.metrics.micrometer.CapacityMonitor$1","org.axonframework.extension.metrics.micrometer.MessageCountingMonitor","org.axonframework.extension.metrics.micrometer.reservoir.SlidingTimeWindowReservoir","org.axonframework.extension.metrics.micrometer.springboot.MicrometerMetricsAutoConfiguration$1","org.axonframework.extension.metrics.micrometer.CapacityMonitor","org.axonframework.extension.metrics.micrometer.MetricsConfigurationEnhancer","org.axonframework.extension.metrics.micrometer.TagsUtil","org.axonframework.extension.metrics.micrometer.springboot.MicrometerMetricsAutoConfiguration","org.axonframework.extension.metrics.micrometer.MessageTimerMonitor$Builder","org.axonframework.extension.metrics.micrometer.EventProcessorLatencyMonitor","org.axonframework.extension.metrics.micrometer.EventProcessorLatencyMonitor$Builder","org.axonframework.extension.metrics.micrometer.reservoir.package-info","org.axonframework.extension.metrics.micrometer.package-info","org.axonframework.extension.metrics.micrometer.MessageTimerMonitor$1"] | [] |
| axon-server-connector-5.1.1 | 79 | ["io.axoniq.framework.axonserver.connector.configuration.TopologyChange","io.axoniq.framework.axonserver.connector.util.PriorityExecutorService","io.axoniq.framework.axonserver.connector.api.AxonServerConfiguration$HeartbeatConfiguration","io.axoniq.framework.axonserver.connector.api.AxonServerException","io.axoniq.framework.axonserver.connector.command.AxonServerCommandBusConnector","io.axoniq.framework.axonserver.connector.command.CommandConverter","io.axoniq.framework.axonserver.connector.util.GrpcMessageSizeWarningThresholdReachedException","io.axoniq.framework.axonserver.connector.api.AxonServerConnectionManager$Builder","io.axoniq.framework.axonserver.connector.util.GrpcMessageSizeExceededException","io.axoniq.framework.axonserver.connector.util.PriorityTaskSchedulers","io.axoniq.framework.axonserver.connector.event.AxonServerMessageStream","io.axoniq.framework.axonserver.connector.configuration.TopologyChange$1","io.axoniq.framework.axonserver.connector.configuration.package-info","io.axoniq.framework.axonserver.connector.shared.ExceptionFactory","io.axoniq.framework.axonserver.connector.query.AxonServerQueryBusConnector$LocalSegmentAdapter","io.axoniq.framework.axonserver.connector.event.StreamingEventMessageStream","io.axoniq.framework.axonserver.connector.configuration.ManagedChannelCustomizer","io.axoniq.framework.axonserver.connector.util.Scheduler$ScheduledTask","io.axoniq.framework.axonserver.connector.shared.MetadataConverter$1"] | [] |
| axon-modelling-5.1.1 | 99 | ["org.axonframework.modelling.entity.child.ChildAmbiguityException","org.axonframework.modelling.entity.annotation.package-info","org.axonframework.modelling.configuration.ModellingConfigurer","org.axonframework.modelling.configuration.StateBasedEntityModule$MessagingMetamodelPhase","org.axonframework.modelling.entity.annotation.ListEntityChildModelDefinition","org.axonframework.modelling.entity.child.AbstractEntityChildMetamodel","org.axonframework.modelling.entity.EntityMetamodelBuilder","org.axonframework.modelling.SimpleStateManager","org.axonframework.modelling.configuration.EntityModule","org.axonframework.modelling.entity.annotation.SingleEntityChildModelDefinition","org.axonframework.modelling.configuration.SimpleStateBasedEntityModule$1","org.axonframework.modelling.annotation.AnnotationBasedEntityIdResolver","org.axonframework.modelling.entity.WrongPolymorphicEntityTypeException","org.axonframework.modelling.configuration.package-info","org.axonframework.modelling.MissingRepositoryException","org.axonframework.modelling.entity.child.ListEntityChildMetamodel","org.axonframework.modelling.entity.annotation.EntityChildModelDefinition","org.axonframework.modelling.entity.ConcreteEntityMetamodel$Builder","org.axonframework.modelling.entity.child.ChildEntityFieldDefinition"] | ["java.lang.reflect.Member","java.lang.reflect.AnnotatedElement","java.lang.reflect.Executable","java.lang.reflect.Parameter","java.lang.reflect.ParameterizedType","java.lang.reflect.Method","java.lang.reflect.Modifier","java.lang.reflect.Field"] |

[Full data](./ReflectionUsage.csv)

### 4.5 Java Code Quality Charts


![JavaCodeQuality_AnnotatedElementsPerArtifact_Bar](./JavaCodeQuality_AnnotatedElementsPerArtifact_Bar.svg)

![JavaCodeQuality_AnnotationTypeDistribution_Bar](./JavaCodeQuality_AnnotationTypeDistribution_Bar.svg)

![JavaCodeQuality_DeprecatedElementUsageTop20_Bar](./JavaCodeQuality_DeprecatedElementUsageTop20_Bar.svg)

---

## 5. Web Framework Annotations

HTTP mapping annotations from Spring Web and Jakarta EE REST — declared REST endpoints.

### 5.1 Spring Web Request Annotations



### 5.2 Jakarta EE REST Annotations



### 5.3 Web Framework Charts



---

## 6. Duplicate Package Names

Package names in multiple artifacts. Can cause split-package issues on the module path.



---

## 7. Dependency Spread

How many distinct artifacts each internal module is depended on by (spread) and vice versa. Highly spread = critical infrastructure.

### 7.1 Spread per Dependency (most used by others)

| dependencyArtifactName | dependencyTypeIsInterface | usedInArtifacts | usedInPackages | minPackageSpread | maxPackageSpread | avgPackageSpread | stdPackageSpread | per5PackageSpread | minPackageCount | maxPackageCount | avgPackageCount | stdPackageCount | per5PackageCount | minTypeSpread | maxTypeSpread | avgTypeSpread | stdTypeSpread | per5TypeSpread |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| axon-common-5.1.1 | false | 7 | 86 | 63.63636363636364 | 100 | 87.3365231259968 | 13.847888884820794 | 87.71929824561403 | 4 | 50 | 12.285714285714286 | 16.690459207925603 | 7 | 18.9873417721519 | 71.42857142857143 | 33.31088053249909 | 18.04040625801803 | 32.03125 |
| axon-common-5.1.1 | true | 7 | 64 | 40 | 100 | 66.32946001367054 | 21.40920350674398 | 66.66666666666667 | 2 | 37 | 9.142857142857142 | 12.495713550768405 | 4 | 11.39240506329114 | 30.303030303030305 | 19.73447595846951 | 6.027722909024434 | 18.9873417721519 |
| axon-conversion-5.1.1 | true | 3 | 21 | 24.561403508771928 | 40 | 30.6113769271664 | 8.243027449975816 | 27.272727272727273 | 3 | 14 | 7 | 6.082762530298219 | 4 | 2.34375 | 5.687203791469194 | 4.364748310236567 | 1.777819556897452 | 5.063291139240507 |
| axon-conversion-5.1.1 | false | 1 | 5 | 8.771929824561402 | 8.771929824561402 | 8.771929824561402 | 0 | 8.771929824561402 | 5 | 5 | 5 | 0 | 5 | 0.7898894154818326 | 0.7898894154818326 | 0.7898894154818326 | 0 | 0.7898894154818326 |
| axon-eventsourcing-5.1.1 | false | 1 | 3 | 30 | 30 | 30 | 0 | 30 | 3 | 3 | 3 | 0 | 3 | 11.39240506329114 | 11.39240506329114 | 11.39240506329114 | 0 | 11.39240506329114 |
| axon-eventsourcing-5.1.1 | true | 1 | 3 | 30 | 30 | 30 | 0 | 30 | 3 | 3 | 3 | 0 | 3 | 11.39240506329114 | 11.39240506329114 | 11.39240506329114 | 0 | 11.39240506329114 |
| axon-messaging-5.1.1 | false | 4 | 26 | 40 | 100 | 75.22727272727273 | 26.632640136891368 | 70 | 2 | 10 | 6.5 | 3.3166247903554 | 7 | 11.39240506329114 | 28.90625 | 21.770738436581002 | 7.836604778802304 | 20.202020202020204 |
| axon-messaging-5.1.1 | true | 4 | 24 | 40 | 100 | 75.45454545454545 | 25.302576660785583 | 80 | 4 | 9 | 6 | 2.449489742783178 | 4 | 30.37974683544304 | 43.43434343434344 | 38.494068453522566 | 5.892360293357161 | 37.9746835443038 |
| axon-modelling-5.1.1 | true | 1 | 5 | 45.45454545454546 | 45.45454545454546 | 45.45454545454546 | 0 | 45.45454545454546 | 5 | 5 | 5 | 0 | 5 | 13.28125 | 13.28125 | 13.28125 | 0 | 13.28125 |
| axon-modelling-5.1.1 | false | 1 | 2 | 18.181818181818183 | 18.181818181818183 | 18.181818181818183 | 0 | 18.181818181818183 | 2 | 2 | 2 | 0 | 2 | 3.125 | 3.125 | 3.125 | 0 | 3.125 |

[Full data](./InternalArtifactUsageSpreadPerDependency.csv)

### 7.2 Spread per Dependent (depends on most others)

| artifactName | dependencyTypeIsInterface | artifactDependencies | artifactDependencyPackages | dependentPackagesRate | minPackageSpread | maxPackageSpread | avgPackageSpread | stdPackageSpread | per5PackageSpread | minPackageCount | maxPackageCount | avgPackageCount | stdPackageCount | per5PackageCount | minTypeSpread | maxTypeSpread | avgTypeSpread | stdTypeSpread | per5TypeSpread |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| axon-conversion-5.1.1 | false | 1 | 2 | 80 | 80 | 80 | 80 | 0 | 80 | 4 | 4 | 4 | 0 | 4 | 19.51219512195122 | 19.51219512195122 | 19.51219512195122 | 0 | 19.51219512195122 |
| axon-conversion-5.1.1 | true | 1 | 1 | 80 | 80 | 80 | 80 | 0 | 80 | 4 | 4 | 4 | 0 | 4 | 21.95121951219512 | 21.95121951219512 | 21.95121951219512 | 0 | 21.95121951219512 |
| axon-eventsourcing-5.1.1 | false | 3 | 15 | 57.57575757575758 | 18.181818181818183 | 90.90909090909092 | 57.57575757575758 | 36.74047167570347 | 63.63636363636364 | 2 | 10 | 6.333333333333333 | 4.041451884327381 | 7 | 3.125 | 32.03125 | 21.354166666666668 | 15.86405667762295 | 28.90625 |
| axon-eventsourcing-5.1.1 | true | 4 | 25 | 56.81818181818182 | 27.272727272727273 | 81.81818181818183 | 56.81818181818182 | 25.034411578573195 | 45.45454545454546 | 3 | 9 | 6.25 | 2.753785273643051 | 5 | 2.34375 | 42.1875 | 20.1171875 | 16.89349632547858 | 13.28125 |
| axon-messaging-5.1.1 | false | 2 | 9 | 48.24561403508772 | 8.771929824561402 | 87.71929824561403 | 48.24561403508771 | 55.82421956735901 | 8.771929824561402 | 5 | 50 | 27.5 | 31.81980515339464 | 5 | 0.7898894154818326 | 33.80726698262244 | 17.298578199052134 | 23.346811574721713 | 0.7898894154818326 |
| axon-messaging-5.1.1 | true | 2 | 9 | 44.73684210526316 | 24.561403508771928 | 64.91228070175438 | 44.73684210526316 | 28.532378889983498 | 24.561403508771928 | 14 | 37 | 25.5 | 16.263455967290593 | 14 | 5.687203791469194 | 17.061611374407583 | 11.374407582938389 | 8.042920733875421 | 5.687203791469194 |
| axon-metrics-micrometer-5.1.1 | true | 1 | 1 | 66.66666666666667 | 66.66666666666667 | 66.66666666666667 | 66.66666666666667 | 0 | 66.66666666666667 | 2 | 2 | 2 | 0 | 2 | 15.789473684210527 | 15.789473684210527 | 15.789473684210527 | 0 | 15.789473684210527 |
| axon-modelling-5.1.1 | false | 2 | 9 | 100 | 100 | 100 | 100 | 0 | 100 | 7 | 7 | 7 | 0 | 7 | 20.202020202020204 | 23.232323232323235 | 21.71717171717172 | 2.142747821777417 | 20.202020202020204 |
| axon-modelling-5.1.1 | true | 2 | 14 | 100 | 100 | 100 | 100 | 0 | 100 | 7 | 7 | 7 | 0 | 7 | 30.303030303030305 | 43.43434343434344 | 36.86868686868687 | 9.285240561035476 | 30.303030303030305 |
| axon-server-connector-5.1.1 | false | 3 | 16 | 60 | 30 | 80 | 60 | 26.457513110645905 | 70 | 3 | 8 | 6 | 2.6457513110645907 | 7 | 11.39240506329114 | 34.17721518987342 | 24.050632911392405 | 11.60145745558441 | 26.58227848101266 |

[Full data](./InternalArtifactUsageSpreadPerDependent.csv)

---

## 8. Glossary and Column Definitions

| Term | Definition |
|------|-----------|
| `a.fileName` | File path of the artifact (JAR/WAR/EAR) |
| `incomingDependencies` | Number of other artifacts that depend on this artifact |
| `outgoingDependencies` | Number of artifacts this artifact depends on |
| `dependency` | Name of an internal artifact that others depend upon |
| `usedByPackages` | Number of distinct packages depending on this artifact |
| `dependencyArtifactName` | Name of the dependency artifact in a spread analysis |
| `usedInArtifacts` | Number of distinct artifacts using this dependency (spread) |
| `artifactDependencies` | Number of distinct dependency artifacts used by this artifact (spread) |
| `typeName` | Simple name of a Java type (class, interface, enum, annotation type) |
| `packageName` | Simple name of a Java package |
| `fullPackageName` | Fully qualified name of a Java package |
| `artifactName` | Name of the artifact (JAR/module) containing the element |
| `methods` | Number of methods with a given effective line count |
| `effectiveLineCount` | Non-blank, non-comment lines in a method |
| `sumEffectiveLinesOfMethodCode` | Sum of effective lines of method code in a type |
| `linesInPackage` | Sum of effective lines across all methods in a package |
| `annotationName` | Fully qualified name of a Java annotation type |
| `languageElement` | Kind of code element annotated (Class, Method, Field, Type, Parameter, etc.) |
| `numberOfAnnotatedElements` | Count of distinct elements annotated with a particular annotation |
| `deprecatedElement` | Kind of deprecated code element (Class, Method, Field, etc.) |
| `numberOfElementsUsingDeprecatedElements` | Count of distinct non-deprecated elements using a deprecated element |
