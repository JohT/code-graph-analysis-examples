---
title: "Java Report"
generated: "2026-08-25"
model_version: "v4.0.2"
dataset: "AxonFramework-5.1.2"
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
| /axon-modelling-5.1.2.jar | 2 | 64 |
| /axon-test-5.1.2.jar | 0 | 0 |
| /axon-messaging-5.1.2.jar | 7 | 1306 |
| /axon-server-connector-5.1.2.jar | 1 | 16 |
| /axon-metrics-micrometer-5.1.2.jar | 0 | 0 |
| /axon-common-5.1.2.jar | 10 | 1732 |
| /axon-update-5.1.2.jar | 0 | 0 |
| /axon-tracing-opentelemetry-5.1.2.jar | 0 | 0 |
| /axon-eventsourcing-5.1.2.jar | 2 | 92 |
| /axon-conversion-5.1.2.jar | 5 | 112 |

[Full data](./IncomingDependencies.csv)

### 2.2 Outgoing Artifact Dependencies

| a.fileName | outgoingDependencies | outgoingDependenciesWeight |
| --- | --- | --- |
| /axon-modelling-5.1.2.jar | 3 | 500 |
| /axon-test-5.1.2.jar | 3 | 290 |
| /axon-messaging-5.1.2.jar | 2 | 1068 |
| /axon-server-connector-5.1.2.jar | 5 | 504 |
| /axon-metrics-micrometer-5.1.2.jar | 2 | 82 |
| /axon-common-5.1.2.jar | 0 | 0 |
| /axon-update-5.1.2.jar | 1 | 54 |
| /axon-tracing-opentelemetry-5.1.2.jar | 2 | 24 |
| /axon-eventsourcing-5.1.2.jar | 4 | 708 |
| /axon-conversion-5.1.2.jar | 1 | 34 |

[Full data](./OutgoingDependencies.csv)

### 2.3 Most Used Internal Dependencies

| dependency | usedByPackages | usedByTypes | providesPackages | providesTypes | interfaceRate | someProvidedPackages | someProvidedTypes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| axon-common-5.1.2 | 94 | 460 | 12 | 73 | 39.73 | ["org.axonframework.common","org.axonframework.common.io","org.axonframework.common.annotation","org.axonframework.common.jdbc","org.axonframework.common.util"] | ["DirectExecutor","Registration","IdentifierFactory","Priority","AxonNonTransientException"] |
| axon-messaging-5.1.2 | 33 | 189 | 31 | 107 | 52.34 | ["org.axonframework.messaging.monitoring","org.axonframework.messaging.monitoring.configuration","org.axonframework.messaging.commandhandling","org.axonframework.messaging.commandhandling.annotation","org.axonframework.messaging.commandhandling.configuration"] | ["NoOpMessageMonitor","NoOpMessageMonitorCallback","MessageMonitor","MultiMessageMonitor","MessageMonitor$MonitorCallback"] |
| axon-conversion-5.1.2 | 25 | 48 | 2 | 6 | 33.33 | ["org.axonframework.conversion","org.axonframework.conversion.jackson"] | ["Converter","DelegatingGeneralConverter","CachingSupplier","ConversionException","GeneralConverter"] |
| axon-modelling-5.1.2 | 6 | 18 | 6 | 16 | 68.75 | ["org.axonframework.modelling","org.axonframework.modelling.annotation","org.axonframework.modelling.entity","org.axonframework.modelling.entity.annotation","org.axonframework.modelling.configuration"] | ["ConcurrencyException","StateManager","EntityEvolver","EntityIdResolver","EntityIdResolverDefinition"] |
| axon-eventsourcing-5.1.2 | 5 | 13 | 3 | 20 | 45 | ["org.axonframework.eventsourcing.snapshot.store","org.axonframework.eventsourcing.snapshot.api","org.axonframework.eventsourcing.eventstore"] | ["SnapshotStore","Snapshot","EventStoreException","GlobalIndexPosition","SourcingCondition"] |
| axon-server-connector-5.1.2 | 3 | 5 | 2 | 5 | 20 | ["io.axoniq.framework.axonserver.connector.api","io.axoniq.framework.axonserver.connector.configuration"] | ["TagsConfiguration","AxonServerConnectionManager","AxonServerConfiguration","TopologyChangeListener","AxonServerConfigurationEnhancer"] |

[Full data](./MostUsedDependenciesAcrossArtifacts.csv)

### 2.4 All Artifact Dependencies

| artifactName | packagesInArtifactCount | packagesCount | packageSpread | typesInArtifactCount | typesCount | typesSpread | dependencyArtifactName | dependencyTypeIsInterface | dependencyPackagesCount | dependencyTypesCount | someDependencyPackages | someDependencyTypes | someCallingPackages | someCallingTypes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| axon-messaging-5.1.2 | 57 | 50 | 87.72 | 633 | 214 | 33.81 | axon-common-5.1.2 | false | 7 | 36 | ["org.axonframework.common","org.axonframework.common.annotation"] | ["DirectExecutor","IdentifierFactory","Priority","AxonNonTransientException"] | ["org.axonframework.messaging.core.unitofwork","org.axonframework.messaging.core"] | ["UnitOfWorkConfiguration","GenericMessage","SimpleResourceParameterResolverFactory","HierarchicalParameterResolverFactory"] |
| axon-messaging-5.1.2 | 57 | 37 | 64.91 | 633 | 108 | 17.06 | axon-common-5.1.2 | true | 8 | 24 | ["org.axonframework.common","org.axonframework.common.jdbc"] | ["Registration","JdbcUtils$SqlResultConverter","Property","TransactionalExecutor"] | ["org.axonframework.messaging.eventhandling","org.axonframework.messaging.eventhandling.processing.subscribing"] | ["EventSubscribers","SubscribingEventProcessor","InterceptingEventBus","SubscribableEventSource"] |
| axon-messaging-5.1.2 | 57 | 14 | 24.56 | 633 | 36 | 5.69 | axon-conversion-5.1.2 | true | 1 | 2 | ["org.axonframework.conversion"] | ["Converter","GeneralConverter"] | ["org.axonframework.messaging.queryhandling","org.axonframework.messaging.commandhandling"] | ["GenericSubscriptionQueryUpdateMessage","GenericCommandResultMessage","JdbcTokenStore","CommandResultMessage"] |
| axon-eventsourcing-5.1.2 | 11 | 10 | 90.91 | 130 | 38 | 29.23 | axon-messaging-5.1.2 | false | 8 | 20 | ["org.axonframework.messaging.eventhandling","org.axonframework.messaging.eventhandling.annotation"] | ["InterceptingEventBus","SimpleEventBus","GenericEventMessage","EventHandler"] | ["org.axonframework.eventsourcing.eventstore","org.axonframework.eventsourcing.configuration"] | ["InterceptingEventStore","EventSourcingConfigurationDefaults","SnapshottingEntityLifecycleHandler","GapAwareTrackingTokenOperations"] |
| axon-eventsourcing-5.1.2 | 11 | 9 | 81.82 | 130 | 54 | 41.54 | axon-messaging-5.1.2 | true | 13 | 30 | ["org.axonframework.messaging.commandhandling","org.axonframework.messaging.commandhandling.configuration"] | ["CommandBus","CommandHandlingComponent","CommandHandlingModule","EventMessage"] | ["org.axonframework.eventsourcing.configuration","org.axonframework.eventsourcing.eventstore"] | ["SimpleEventSourcedEntityModule","EventSourcingConfigurer","MultiTagResolver","InMemoryEventStorageEngine"] |
| axon-eventsourcing-5.1.2 | 11 | 8 | 72.73 | 130 | 29 | 22.31 | axon-common-5.1.2 | true | 6 | 17 | ["org.axonframework.common","org.axonframework.common.jdbc"] | ["Registration","PersistenceExceptionResolver","TransactionalExecutor","DescribableComponent"] | ["org.axonframework.eventsourcing.eventstore","org.axonframework.eventsourcing.eventstore.jpa"] | ["StorageEngineBackedEventStore","ContinuousMessageStream","AggregateBasedJpaEventStorageEngine","InterceptingEventStore"] |
| axon-server-connector-5.1.2 | 10 | 8 | 80 | 79 | 27 | 34.18 | axon-common-5.1.2 | false | 5 | 16 | ["org.axonframework.common","org.axonframework.common.annotation"] | ["FutureUtils","StringUtils","ObjectUtils","AxonConfigurationException"] | ["io.axoniq.framework.axonserver.connector.query","io.axoniq.framework.axonserver.connector.event"] | ["AxonServerQueryBusConnector$LocalSegmentAdapter","EventProcessorControlService","AxonServerQueryBusConnector","AxonServerQueryBusConnector$AxonServerUpdateCallback"] |
| axon-modelling-5.1.2 | 7 | 7 | 100 | 99 | 43 | 43.43 | axon-messaging-5.1.2 | true | 11 | 23 | ["org.axonframework.messaging.commandhandling","org.axonframework.messaging.commandhandling.annotation"] | ["CommandHandler","CommandResultMessage","CommandBus","CommandHandlingComponent"] | ["org.axonframework.modelling.entity","org.axonframework.modelling.entity.child"] | ["PolymorphicEntityMetamodelBuilder","PolymorphicEntityMetamodel$Builder","EntityMetamodelBuilder","ConcreteEntityMetamodel$Builder"] |
| axon-server-connector-5.1.2 | 10 | 7 | 70 | 79 | 21 | 26.58 | axon-messaging-5.1.2 | false | 9 | 29 | ["org.axonframework.messaging.commandhandling","org.axonframework.messaging.eventhandling"] | ["NoHandlerForCommandException","CommandDispatchException","CommandExecutionException","GenericCommandResultMessage"] | ["io.axoniq.framework.axonserver.connector.shared","io.axoniq.framework.axonserver.connector.api.command"] | ["ExceptionFactory","AxonServerCommandDispatchException","CommandConverter","AggregateBasedAxonServerEventStorageEngine"] |
| axon-modelling-5.1.2 | 7 | 7 | 100 | 99 | 20 | 20.2 | axon-messaging-5.1.2 | false | 5 | 13 | ["org.axonframework.messaging.commandhandling","org.axonframework.messaging.core"] | ["NoHandlerForCommandException","DuplicateCommandHandlerSubscriptionException","GenericCommandResultMessage","QualifiedName"] | ["org.axonframework.modelling.entity","org.axonframework.modelling.entity.annotation"] | ["ConcreteEntityMetamodel","PolymorphicEntityMetamodel","EntityCommandHandlingComponent","ConcreteEntityMetamodel$Builder"] |

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
| axon-common-5.1.2.jar | 1 | 392 |
| axon-common-5.1.2.jar | 2 | 152 |
| axon-common-5.1.2.jar | 3 | 101 |
| axon-common-5.1.2.jar | 4 | 37 |
| axon-common-5.1.2.jar | 5 | 38 |
| axon-common-5.1.2.jar | 6 | 38 |
| axon-common-5.1.2.jar | 7 | 19 |
| axon-common-5.1.2.jar | 8 | 18 |
| axon-common-5.1.2.jar | 9 | 12 |
| axon-common-5.1.2.jar | 10 | 6 |

[Full data](./EffectiveMethodLineCountDistribution.csv)

### 3.2 Top Types by Effective LOC

| artifactName | packageName | typeName | sumEffectiveLinesOfMethodCode | maxEffectiveLinesOfMethodCode | methodWithMaxEffectiveLinesOfMethodCode | maxCyclomaticComplexity | methodWithMaxCyclomaticComplexity |
| --- | --- | --- | --- | --- | --- | --- | --- |
| axon-messaging-5.1.2 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | Coordinator$CoordinationTask | 398 | 111 | run | 25 | run |
| axon-messaging-5.1.2 | org.axonframework.messaging.eventhandling.processing.streaming.token.store.jdbc | JdbcTokenStore | 305 | 25 | updateToken | 8 | updateToken |
| axon-test-5.1.2 | org.axonframework.test.fixture | Reporter | 224 | 45 | appendEventOverview | 11 | appendEventOverview |
| axon-eventsourcing-5.1.2 | org.axonframework.eventsourcing.eventstore.jpa | AggregateBasedJpaEventStorageEngine | 197 | 18 | <init> | 6 | lambda$queryBatch$16 |
| axon-messaging-5.1.2 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | WorkPackage | 190 | 25 | processEvents | 7 | processEvents |
| axon-common-5.1.2 | org.axonframework.common.configuration | DefaultComponentRegistry | 185 | 18 | invokeEnhancers | 8 | registerComponent |
| axon-common-5.1.2 | org.axonframework.common | ReflectionUtils | 177 | 17 | fieldNameFromMember | 9 | fieldNameFromMember |
| axon-messaging-5.1.2 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | PooledStreamingEventProcessor | 175 | 37 | <init> | 3 | lambda$processWithErrorHandling$20 |
| axon-modelling-5.1.2 | org.axonframework.modelling.entity.annotation | AnnotatedEntityMetamodel | 166 | 18 | createOptionalChildForMember | 6 | getExpectedRepresentation |
| axon-messaging-5.1.2 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | PooledStreamingEventProcessorConfiguration | 160 | 18 | describeTo | 2 | interceptors |

[Full data](./EffectiveLinesOfMethodCodePerType.csv)

### 3.3 Top Packages by Effective LOC

| artifactName | fullPackageName | linesInPackage | complexityInPackage | methodCount | maxLinesMethod | maxLinesMethodType | maxLinesMethodName | maxComplexity | maxComplexityType | maxComplexityMethod | packageName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| axon-messaging-5.1.2 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | 1496 | 586 | 428 | 111 | Coordinator$CoordinationTask | run | 25 | Coordinator$CoordinationTask | run | pooled |
| axon-messaging-5.1.2 | org.axonframework.messaging.core | 1187 | 740 | 520 | 23 | AbstractMessageStream | next | 11 | QueueMessageStream | fetchNext | core |
| axon-common-5.1.2 | org.axonframework.common.configuration | 766 | 411 | 303 | 26 | DefaultAxonApplication$AxonConfigurationImpl | invokeLifecycleHandlers | 8 | DefaultComponentRegistry | registerComponent | configuration |
| axon-test-5.1.2 | org.axonframework.test.fixture | 752 | 324 | 211 | 45 | Reporter | appendEventOverview | 11 | Reporter | appendEventOverview | fixture |
| axon-messaging-5.1.2 | org.axonframework.messaging.core.annotation | 714 | 379 | 239 | 23 | MethodInvokingMessageHandlingMember | <init> | 13 | MessageStreamResolverUtils | resolveToStream | annotation |
| axon-eventsourcing-5.1.2 | org.axonframework.eventsourcing.eventstore | 684 | 438 | 281 | 19 | AnnotationBasedTagResolver | createTagsForValue | 8 | AggregateBasedConsistencyMarker | from | eventstore |
| axon-common-5.1.2 | org.axonframework.common | 654 | 408 | 194 | 24 | TypeReflectionUtils | getExactDirectSuperTypesOfParameterizedTypeOrClass | 9 | ConstructorUtils | doConstructionWithOptionalArgument | common |
| axon-server-connector-5.1.2 | io.axoniq.framework.axonserver.connector.event | 542 | 217 | 161 | 22 | AggregateBasedAxonServerEventStorageEngine | lambda$appendEvents$0 | 4 | AggregateBasedAxonServerEventStorageEngine | lambda$appendEvents$0 | event |
| axon-eventsourcing-5.1.2 | org.axonframework.eventsourcing.eventstore.jpa | 452 | 219 | 144 | 20 | GapAwareTrackingTokenOperations | withGapsCleaned | 8 | SQLErrorCodesResolver | loadKeyViolationCodes | jpa |
| axon-messaging-5.1.2 | org.axonframework.messaging.eventhandling.processing.streaming.token.store.jdbc | 443 | 194 | 109 | 25 | JdbcTokenStore | updateToken | 8 | JdbcTokenStore | updateToken | jdbc |

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
| org.jspecify.annotations.NullMarked | Interface | 124 | ["org.axonframework.modelling.annotation.package-info","org.axonframework.modelling.package-info","org.axonframework.modelling.entity.annotation.package-info","org.axonframework.modelling.entity.package-info","org.axonframework.modelling.entity.child.package-info","org.axonframework.modelling.configuration.package-info","org.axonframework.modelling.repository.package-info","org.axonframework.test.fixture.package-info","org.axonframework.test.extension.package-info"] |
| org.axonframework.common.annotation.Internal | Class | 91 | ["org.axonframework.modelling.entity.annotation.AbstractEntityChildModelDefinition","org.axonframework.modelling.entity.annotation.RoutingKeyUtils","org.axonframework.modelling.entity.annotation.AnnotatedEntityModelRoutingKeyMatcher","org.axonframework.test.fixture.RecordingComponentsRegistry","org.axonframework.test.fixture.RecordingCommandBus","org.axonframework.test.fixture.RecordingEventBus","org.axonframework.test.fixture.RecordingEventStore","org.axonframework.test.extension.ProvidedAxonTestFixtureUtils","org.axonframework.test.util.RecordingCommandBus"] |
| java.lang.FunctionalInterface | Interface | 58 | ["org.axonframework.modelling.EntityIdResolver","org.axonframework.modelling.annotation.EntityIdResolverDefinition","org.axonframework.modelling.entity.child.EventTargetMatcher","org.axonframework.modelling.entity.child.CommandTargetResolver","org.axonframework.modelling.entity.annotation.CommandTargetResolverDefinition","org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodelFactory","org.axonframework.modelling.EntityEvolver","org.axonframework.modelling.entity.EntityCommandHandler","org.axonframework.modelling.configuration.EntityMetamodelConfigurationBuilder"] |
| java.lang.annotation.Retention | Annotation | 43 | ["org.axonframework.modelling.annotation.TargetEntityId","org.axonframework.modelling.annotation.InjectEntity","org.axonframework.modelling.entity.annotation.EntityMember","org.axonframework.test.extension.ProvidedAxonTestFixture","org.axonframework.messaging.commandhandling.annotation.CommandHandler","org.axonframework.messaging.commandhandling.annotation.Command","org.axonframework.messaging.eventhandling.annotation.SequenceNumber","org.axonframework.messaging.eventhandling.annotation.EventHandler","org.axonframework.messaging.eventhandling.annotation.Timestamp"] |
| java.lang.annotation.Target | Annotation | 43 | ["org.axonframework.modelling.annotation.TargetEntityId","org.axonframework.modelling.annotation.InjectEntity","org.axonframework.modelling.entity.annotation.EntityMember","org.axonframework.test.extension.ProvidedAxonTestFixture","org.axonframework.messaging.commandhandling.annotation.CommandHandler","org.axonframework.messaging.commandhandling.annotation.Command","org.axonframework.messaging.eventhandling.annotation.SequenceNumber","org.axonframework.messaging.eventhandling.annotation.EventHandler","org.axonframework.messaging.eventhandling.annotation.Timestamp"] |
| org.axonframework.common.annotation.Internal | Interface | 26 | ["org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodelFactory","org.axonframework.messaging.monitoring.configuration.MessageMonitorRegistry","org.axonframework.messaging.commandhandling.annotation.CommandHandlingMember","org.axonframework.messaging.eventhandling.annotation.EventHandlingMember","org.axonframework.messaging.eventhandling.replay.ReplayStatusChangedHandlerRegistry","org.axonframework.messaging.eventhandling.replay.ReplayStatusChangedHandler","org.axonframework.messaging.eventhandling.replay.ReplayStatusChanged","org.axonframework.messaging.queryhandling.annotation.QueryHandlingMember","org.axonframework.messaging.core.annotation.MessageHandlingMember"] |
| org.axonframework.common.annotation.Internal | Constructor | 19 | ["org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessorConfiguration.<init>","org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessorsConfigurer.<init>","org.axonframework.messaging.eventhandling.processing.streaming.segmenting.Segment.<init>","org.axonframework.messaging.eventhandling.processing.streaming.segmenting.SequenceCachingEventHandlingComponent.<init>","org.axonframework.messaging.eventhandling.processing.subscribing.SubscribingEventProcessorConfiguration.<init>","org.axonframework.messaging.eventhandling.processing.subscribing.SubscribingEventProcessorsConfigurer.<init>","org.axonframework.messaging.eventhandling.InterceptingEventBus.<init>","org.axonframework.messaging.eventhandling.configuration.EventProcessorConfiguration.<init>","org.axonframework.messaging.eventhandling.configuration.EventProcessingConfigurer.<init>"] |
| java.lang.annotation.Documented | Annotation | 15 | ["org.axonframework.modelling.entity.annotation.EntityMember","org.axonframework.messaging.commandhandling.annotation.CommandHandler","org.axonframework.messaging.eventhandling.annotation.EventHandler","org.axonframework.messaging.eventhandling.replay.annotation.AllowReplay","org.axonframework.messaging.eventhandling.replay.annotation.DisallowReplay","org.axonframework.messaging.queryhandling.annotation.QueryHandler","org.axonframework.messaging.core.annotation.MetadataValue","org.axonframework.messaging.core.annotation.MessageHandlerTimeout","org.axonframework.messaging.core.annotation.SequencingPolicy"] |
| org.springframework.context.annotation.Bean | Method | 14 | ["org.axonframework.extension.metrics.micrometer.springboot.MicrometerMetricsAutoConfiguration.disableMetricsConfigurationEnhancer","org.axonframework.extension.metrics.micrometer.springboot.MicrometerMetricsAutoConfiguration.meterRegistry","io.axoniq.framework.springboot.autoconfig.PostgresqlAutoConfiguration.disablePostgresqlConfigurationEnhancer","io.axoniq.framework.springboot.autoconfig.JpaDeadLetterQueueAutoConfiguration.jpaDeadLetterQueueFactory","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.disableAxonServerConfigurationEnhancer","io.axoniq.framework.springboot.autoconfig.DeadLetterQueueAutoConfiguration.dlqCustomization","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.axonServerConfigurationEnhancer","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.axonServerConfigurationWithConnectionDetails","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.tagsConfiguration"] |
| java.lang.Deprecated | Method | 13 | ["org.axonframework.test.fixture.AxonTestThenCommand.resultMessagePayloadSatisfies","org.axonframework.test.fixture.AxonTestPhase$Then$Command.resultMessagePayloadSatisfies","org.axonframework.messaging.eventhandling.configuration.DefaultEventHandlingComponentsConfigurer.declarative","org.axonframework.messaging.eventhandling.configuration.EventHandlingComponentsConfigurer$ComponentsPhase.declarative","org.axonframework.messaging.eventhandling.configuration.EventHandlingComponentsConfigurer$ComponentsPhase.autodetected","org.axonframework.messaging.core.GenericResultMessage.asResultMessage","org.axonframework.messaging.core.annotation.MessageHandlingMember.handleSync","org.axonframework.messaging.core.interception.annotation.MessageHandlerInterceptorMemberChain.handleSync","org.axonframework.messaging.core.interception.annotation.NoMoreInterceptors.handleSync"] |

[Full data](./AnnotatedCodeElements.csv)

### 4.2 Annotated Code Elements per Artifact

| artifactName | annotationName | languageElement | numberOfAnnotatedElements | examples |
| --- | --- | --- | --- | --- |
| axon-common-5.1.2 | org.jspecify.annotations.NullMarked | Interface | 15 | ["org.axonframework.common.io.package-info","org.axonframework.common.jdbc.package-info","org.axonframework.common.package-info","org.axonframework.common.util.package-info","org.axonframework.common.annotation.package-info","org.axonframework.common.property.package-info","org.axonframework.common.caching.package-info","org.axonframework.common.tx.package-info","org.axonframework.common.digest.package-info"] |
| axon-common-5.1.2 | java.lang.FunctionalInterface | Interface | 12 | ["org.axonframework.common.jdbc.JdbcUtils$SqlResultConverter","org.axonframework.common.jdbc.ConnectionProvider","org.axonframework.common.jdbc.JdbcUtils$SqlFunction","org.axonframework.common.util.ExecutorServiceFactory","org.axonframework.common.property.Property","org.axonframework.common.Registration","org.axonframework.common.lock.LockFactory","org.axonframework.common.infra.DescribableComponent","org.axonframework.common.configuration.ConfigurationEnhancer"] |
| axon-common-5.1.2 | org.axonframework.common.annotation.Internal | Class | 7 | ["org.axonframework.common.jdbc.ConnectionExecutor","org.axonframework.common.jdbc.JdbcUtils","org.axonframework.common.jpa.EntityManagerExecutor","org.axonframework.common.configuration.LazyInitializedComponentDefinition","org.axonframework.common.configuration.ConfigurationExtensions","org.axonframework.common.configuration.InstantiatedComponentDefinition","org.axonframework.common.configuration.Components"] |
| axon-common-5.1.2 | org.axonframework.common.annotation.Internal | Interface | 7 | ["org.axonframework.common.jdbc.ConnectionProvider","org.axonframework.common.tx.TransactionalExecutor","org.axonframework.common.jpa.EntityManagerProvider","org.axonframework.common.configuration.ExtensibleConfigurer","org.axonframework.common.configuration.ConfigurationExtension","org.axonframework.common.configuration.Component","org.axonframework.common.configuration.ExtendedConfiguration"] |
| axon-common-5.1.2 | java.lang.annotation.Target | Annotation | 3 | ["org.axonframework.common.annotation.Internal","org.axonframework.common.annotation.RegistrationScope","org.axonframework.common.Priority"] |
| axon-common-5.1.2 | java.lang.annotation.Retention | Annotation | 3 | ["org.axonframework.common.annotation.Internal","org.axonframework.common.annotation.RegistrationScope","org.axonframework.common.Priority"] |
| axon-common-5.1.2 | java.lang.annotation.Documented | Annotation | 2 | ["org.axonframework.common.annotation.Internal","org.axonframework.common.annotation.RegistrationScope"] |
| axon-common-5.1.2 | org.axonframework.common.annotation.Internal | Method | 2 | ["org.axonframework.common.configuration.DefaultComponentRegistry.create","org.axonframework.common.configuration.DefaultComponentRegistry.createLocalConfiguration"] |
| axon-common-5.1.2 | java.lang.annotation.Inherited | Annotation | 1 | ["org.axonframework.common.Priority"] |
| axon-conversion-5.1.2 | org.jspecify.annotations.NullMarked | Interface | 5 | ["org.axonframework.conversion.package-info","org.axonframework.conversion.jackson.package-info","org.axonframework.conversion.converter.package-info","org.axonframework.conversion.jackson2.package-info","org.axonframework.conversion.avro.package-info"] |

[Full data](./AnnotatedCodeElementsPerArtifact.csv)

### 4.3 Deprecated Element Usages

| artifactName | deprecatedElement | numberOfElementsUsingDeprecatedElements | someElementsUsingDeprecatedElements |
| --- | --- | --- | --- |
| axon-eventsourcing-5.1.2 | Field | 2 | ["org.axonframework.eventsourcing.eventstore.jpa.GapAwareTrackingTokenOperations.gapTimeoutThreshold","org.axonframework.eventsourcing.handler.SnapshottingEntityLifecycleHandler.storeSnapshot"] |
| axon-messaging-5.1.2 | Class | 1 | ["org.axonframework.messaging.core.interception.annotation.MessageHandlerInterceptorMemberChain"] |
| axon-messaging-5.1.2 | Method | 3 | ["org.axonframework.messaging.core.interception.annotation.MessageHandlerInterceptorMemberChain.handle","org.axonframework.messaging.core.annotation.WrappedMessageHandlingMember.handleSync","org.axonframework.messaging.core.annotation.ChainedMessageHandlerInterceptorMember.doHandleSync"] |
| axon-messaging-5.1.2 | Field | 8 | ["org.axonframework.messaging.eventhandling.processing.streaming.pooled.WorkPackage$Builder.<init>","org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessor.releaseSegment","org.axonframework.messaging.eventhandling.processing.streaming.pooled.Coordinator$CoordinationTask.lambda$releaseSegmentsIfTooManyClaimed$13","org.axonframework.messaging.eventhandling.processing.streaming.pooled.Coordinator$Builder.<init>","org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessorConfiguration.<init>","org.axonframework.messaging.eventhandling.gateway.EventPublishingUtils.lambda$asEventMessage$1","org.axonframework.messaging.eventhandling.gateway.EventPublishingUtils.lambda$asEventMessage$0","org.axonframework.messaging.eventhandling.GenericEventMessage.<init>"] |
| axon-server-connector-5.1.2 | Method | 2 | ["io.axoniq.framework.axonserver.connector.event.ConditionConverter.convertSourcingCondition","io.axoniq.framework.axonserver.connector.event.AggregateBasedAxonServerEventStorageEngine.aggregateSourceForCriterion"] |

[Full data](./DeprecatedElementUsage.csv)

### 4.4 Reflection Usages

| dependentArtifactName | numberOfReflectionCaller | someReflectionCaller | someReflectionTypes |
| --- | --- | --- | --- |
| axon-modelling-5.1.2 | 99 | ["org.axonframework.modelling.configuration.ModellingConfigurationDefaults","org.axonframework.modelling.entity.PolymorphicEntityMetamodel","org.axonframework.modelling.annotation.AnnotationBasedEntityIdResolverDefinition","org.axonframework.modelling.annotation.EntityIdResolverDefinition","org.axonframework.modelling.PayloadBasedEntityEvolver","org.axonframework.modelling.EntityIdResolver","org.axonframework.modelling.entity.ConcreteEntityMetamodel","org.axonframework.modelling.repository.SimpleRepository$SimpleEntity","org.axonframework.modelling.entity.annotation.SingleEntityChildModelDefinition","org.axonframework.modelling.EntityIdResolutionException","org.axonframework.modelling.ConcurrencyException","org.axonframework.modelling.entity.PolymorphicEntityMetamodel$Builder","org.axonframework.modelling.entity.EntityMetamodel","org.axonframework.modelling.LoadedEntityNotOfExpectedTypeException","org.axonframework.modelling.configuration.StateBasedEntityModule","org.axonframework.modelling.annotation.TargetEntityId","org.axonframework.modelling.entity.child.ChildAmbiguityException","org.axonframework.modelling.configuration.ModellingConfigurer","org.axonframework.modelling.repository.Repository"] | ["java.lang.reflect.Member","java.lang.reflect.AnnotatedElement","java.lang.reflect.Method","java.lang.reflect.Modifier","java.lang.reflect.Executable","java.lang.reflect.Parameter","java.lang.reflect.ParameterizedType","java.lang.reflect.Field"] |
| axon-test-5.1.2 | 79 | ["org.axonframework.test.matchers.NonTransientFieldsFilter","org.axonframework.test.fixture.RecordingEventStore","org.axonframework.test.fixture.RecordingEventBus","org.axonframework.test.fixture.AxonTestPhase$When","org.axonframework.test.matchers.SequenceMatcher","org.axonframework.test.util.RecordingCommandBus","org.axonframework.test.fixture.RecordingEventSink","org.axonframework.test.matchers.MapStringEntryMatcher$Matching","org.axonframework.test.util.DefaultCallbackBehavior","org.axonframework.test.fixture.AxonTestThenMessage","org.axonframework.test.fixture.AxonTestWhen","org.axonframework.test.fixture.AxonTestPhase$When$Nothing","org.axonframework.test.fixture.AxonTestWhen$Command","org.axonframework.test.matchers.PayloadMatcher","org.axonframework.test.matchers.ListWithAllOfMatcher","org.axonframework.test.matchers.MapStringEntryMatcher","org.axonframework.test.fixture.AxonTestPhase$Then$Nothing","org.axonframework.test.fixture.package-info","org.axonframework.test.util.DescriptionUtils"] | ["java.lang.reflect.Field","java.lang.reflect.AnnotatedElement","java.lang.reflect.Constructor","java.lang.reflect.Method","java.lang.reflect.Modifier","java.lang.reflect.Executable","java.lang.reflect.Parameter"] |
| axon-messaging-5.1.2 | 633 | ["org.axonframework.messaging.core.FluxMessageStream$1","org.axonframework.messaging.eventhandling.replay.GenericReplayStatusChanged","org.axonframework.messaging.queryhandling.tracing.TracingQueryBus","org.axonframework.messaging.tracing.Span","org.axonframework.messaging.core.MessageTypeResolver","org.axonframework.messaging.commandhandling.RoutingStrategy","org.axonframework.messaging.queryhandling.SimpleQueryUpdateEmitter","org.axonframework.messaging.eventhandling.processing.streaming.token.LatestTrackingToken","org.axonframework.messaging.commandhandling.gateway.ConvertingCommandGateway$ConvertingCommandResult","org.axonframework.messaging.commandhandling.gateway.package-info","org.axonframework.messaging.tracing.NoOpSpanFactory$NoOpSpan","org.axonframework.messaging.eventstreaming.OrEventCriteria","org.axonframework.messaging.eventhandling.annotation.MethodSequencingPolicyEventHandlerDefinition$SequencingPolicyEventMessageHandlingMember","org.axonframework.messaging.queryhandling.configuration.QueryHandlingModule$SetupPhase","org.axonframework.messaging.core.GenericMessage","org.axonframework.messaging.tracing.HandlerSpanFactory","org.axonframework.messaging.core.interception.annotation.MessageHandlerInterceptorDefinition$InterceptedMessageHandlingMember","org.axonframework.messaging.queryhandling.QueryUpdateEmitter","org.axonframework.messaging.core.AbstractMessageStream$FetchResult$Value"] | ["java.lang.reflect.Type","java.lang.reflect.Constructor","java.lang.reflect.Member","java.lang.reflect.Method","java.lang.reflect.Parameter","java.lang.reflect.Executable","java.lang.reflect.WildcardType","java.lang.reflect.AnnotatedElement","java.lang.reflect.Modifier","java.lang.reflect.Field","java.lang.reflect.InvocationTargetException"] |
| axon-server-connector-5.1.2 | 79 | ["io.axoniq.framework.axonserver.connector.api.AxonServerConfiguration","io.axoniq.framework.axonserver.connector.api.AxonServerException","io.axoniq.framework.axonserver.connector.api.command.AxonServerRemoteCommandHandlingException","io.axoniq.framework.axonserver.connector.command.CommandConverter","io.axoniq.framework.axonserver.connector.event.StreamingEventMessageStream","io.axoniq.framework.axonserver.connector.api.AxonServerConfiguration$HeartbeatConfiguration","io.axoniq.framework.axonserver.connector.snapshot.AxonServerSnapshotStore","io.axoniq.framework.axonserver.connector.shared.MetadataConverter$1","io.axoniq.framework.axonserver.connector.configuration.ManagedChannelCustomizer","io.axoniq.framework.axonserver.connector.api.query.AxonServerRemoteQueryHandlingException","io.axoniq.framework.axonserver.connector.configuration.TopologyChange$1","io.axoniq.framework.axonserver.connector.event.EventProcessorInfoUtils","io.axoniq.framework.axonserver.connector.shared.ExceptionFactory$1","io.axoniq.framework.axonserver.connector.query.AxonServerQueryBusConnector$AxonServerUpdateCallback","io.axoniq.framework.axonserver.connector.configuration.package-info","io.axoniq.framework.axonserver.connector.event.EventProcessorControlService","io.axoniq.framework.axonserver.connector.event.TaggedEventConverter","io.axoniq.framework.axonserver.connector.shared.ErrorCode","io.axoniq.framework.axonserver.connector.util.GrpcMessageSizeInterceptor$1$1"] | [] |
| axon-metrics-micrometer-5.1.2 | 19 | ["org.axonframework.extension.metrics.micrometer.CapacityMonitor","org.axonframework.extension.metrics.micrometer.springboot.MetricsProperties$Micrometer","org.axonframework.extension.metrics.micrometer.CapacityMonitor$1","org.axonframework.extension.metrics.micrometer.EventProcessorLatencyMonitor$Builder","org.axonframework.extension.metrics.micrometer.package-info","org.axonframework.extension.metrics.micrometer.reservoir.SlidingTimeWindowReservoir","org.axonframework.extension.metrics.micrometer.EventProcessorLatencyMonitor","org.axonframework.extension.metrics.micrometer.springboot.package-info","org.axonframework.extension.metrics.micrometer.reservoir.package-info","org.axonframework.extension.metrics.micrometer.MessageTimerMonitor$Builder","org.axonframework.extension.metrics.micrometer.MessageTimerMonitor$1","org.axonframework.extension.metrics.micrometer.MetricsConfigurationEnhancer","org.axonframework.extension.metrics.micrometer.springboot.MicrometerMetricsAutoConfiguration","org.axonframework.extension.metrics.micrometer.TagsUtil","org.axonframework.extension.metrics.micrometer.MessageCountingMonitor$1","org.axonframework.extension.metrics.micrometer.MessageTimerMonitor","org.axonframework.extension.metrics.micrometer.springboot.MetricsProperties","org.axonframework.extension.metrics.micrometer.springboot.MicrometerMetricsAutoConfiguration$1","org.axonframework.extension.metrics.micrometer.MessageCountingMonitor"] | [] |
| axon-common-5.1.2 | 175 | ["org.axonframework.common.configuration.AbstractComponent","org.axonframework.common.IdentifierValidator","org.axonframework.common.lock.Lock","org.axonframework.common.TypeReflectionUtils$VarMap$ParameterizedTypeImpl","org.axonframework.common.configuration.ComponentDefinition$ComponentCreator","org.axonframework.common.property.PropertyAccessStrategy","org.axonframework.common.annotation.Internal","org.axonframework.common.configuration.ComponentDefinition$IncompleteComponentDefinition","org.axonframework.common.configuration.AbstractComponent$HandlerRegistration","org.axonframework.common.DefaultIdentifierFactory","org.axonframework.common.configuration.DefaultAxonApplication$LifecycleState","org.axonframework.common.annotation.AnnotationUtils","org.axonframework.common.configuration.DefaultComponentRegistry","org.axonframework.common.caching.Cache","org.axonframework.common.infra.ComponentDescriptor","org.axonframework.common.property.MethodAccessedProperty","org.axonframework.common.ReflectionUtils","org.axonframework.common.TypeReference$2","org.axonframework.common.jpa.EntityManagerProvider"] | ["java.lang.reflect.ParameterizedType","java.lang.reflect.Type","java.lang.reflect.AnnotatedElement","java.lang.reflect.InvocationTargetException","java.lang.reflect.Member","java.lang.reflect.Method","java.lang.reflect.AccessibleObject","java.lang.reflect.Executable","java.lang.reflect.Field","java.lang.reflect.Modifier","java.lang.reflect.Constructor","java.lang.reflect.Array","java.lang.reflect.GenericArrayType","java.lang.reflect.TypeVariable","java.lang.reflect.WildcardType","java.lang.reflect.Proxy"] |
| axon-update-5.1.2 | 28 | ["org.axonframework.update.UpdateCheckerReporter","org.axonframework.update.LoggingUpdateCheckerReporter","org.axonframework.update.api.package-info","org.axonframework.update.detection.package-info","org.axonframework.update.configuration.EnvironmentVariableUsagePropertyProvider$EnvironmentVariableSupplier","org.axonframework.update.detection.KotlinVersion","org.axonframework.update.package-info","org.axonframework.update.UpdateCheckerConfigurationEnhancer","org.axonframework.update.api.DetectedVulnerability","org.axonframework.update.api.Artifact","org.axonframework.update.configuration.HierarchicalUsagePropertyProvider","org.axonframework.update.configuration.UsagePropertyProvider","org.axonframework.update.detection.AxonVersionDetector","org.axonframework.update.api.DetectedVulnerabilitySeverity","org.axonframework.update.common.package-info","org.axonframework.update.configuration.PropertyFileUsagePropertyProvider","org.axonframework.update.UpdateCheckerHttpClient","org.axonframework.update.api.UpdateCheckRequest","org.axonframework.update.detection.MachineId"] | ["java.lang.reflect.Method"] |
| axon-tracing-opentelemetry-5.1.2 | 6 | ["org.axonframework.extension.tracing.opentelemetry.OpenTelemetrySpanFactory$Builder","org.axonframework.extension.tracing.opentelemetry.package-info","org.axonframework.extension.tracing.opentelemetry.OpenTelemetrySpanFactory","org.axonframework.extension.tracing.opentelemetry.MetadataContextSetter","org.axonframework.extension.tracing.opentelemetry.OpenTelemetrySpan","org.axonframework.extension.tracing.opentelemetry.MetadataContextGetter"] | [] |
| axon-eventsourcing-5.1.2 | 130 | ["org.axonframework.eventsourcing.EventSourcingRepository","org.axonframework.eventsourcing.handler.SimpleEntityLifecycleHandler","org.axonframework.eventsourcing.eventstore.SnapshotCapableEventStorageEngine","org.axonframework.eventsourcing.eventstore.jpa.JpaPollingEventCoordinator$1","org.axonframework.eventsourcing.annotation.AnnotationBasedEventCriteriaResolver$WrappedEventCriteriaBuilderMethod","org.axonframework.eventsourcing.EventSourcingRepository$EventSourcedEntity","org.axonframework.eventsourcing.eventstore.PayloadBasedTagResolver","org.axonframework.eventsourcing.annotation.reflection.InjectEntityId","org.axonframework.eventsourcing.annotation.reflection.package-info","org.axonframework.eventsourcing.CriteriaResolver","org.axonframework.eventsourcing.annotation.CriteriaResolverDefinition","org.axonframework.eventsourcing.eventstore.GenericTaggedEventMessage","org.axonframework.eventsourcing.configuration.EventSourcedEntityModule$EntityFactoryPhase","org.axonframework.eventsourcing.handler.InitializingEntityEvolver","org.axonframework.eventsourcing.annotation.EventCriteriaBuilder","org.axonframework.eventsourcing.annotation.package-info","org.axonframework.eventsourcing.annotation.EventSourcingHandler","org.axonframework.eventsourcing.eventstore.SourcingStrategy$Absolute","org.axonframework.eventsourcing.annotation.AnnotationBasedEventCriteriaResolver"] | ["java.lang.reflect.InvocationTargetException","java.lang.reflect.Method","java.lang.reflect.Modifier","java.lang.reflect.Constructor","java.lang.reflect.Executable","java.lang.reflect.AnnotatedElement","java.lang.reflect.Field","java.lang.reflect.Member"] |
| axon-conversion-5.1.2 | 41 | ["org.axonframework.conversion.CachingSupplier","org.axonframework.conversion.converter.InputStreamToByteArrayConverter","org.axonframework.conversion.ChainedConverter","org.axonframework.conversion.jackson.JsonNodeToByteArrayConverter","org.axonframework.conversion.jackson.package-info","org.axonframework.conversion.Converter","org.axonframework.conversion.avro.AvroConverterStrategy","org.axonframework.conversion.avro.SpecificRecordBaseConverterStrategy","org.axonframework.conversion.converter.ByteArrayToInputStreamConverter","org.axonframework.conversion.GeneralConverter","org.axonframework.conversion.ChainedConverter$RouteCalculator","org.axonframework.conversion.jackson2.ByteArrayToJsonNodeConverter","org.axonframework.conversion.avro.AvroConverter","org.axonframework.conversion.avro.package-info","org.axonframework.conversion.jackson.ByteArrayToJsonNodeConverter","org.axonframework.conversion.jackson2.package-info","org.axonframework.conversion.avro.ByteArrayToGenericRecordConverter","org.axonframework.conversion.avro.DefaultSchemaIncompatibilityChecker","org.axonframework.conversion.avro.GenericRecordToByteArrayConverter"] | ["java.lang.reflect.Type","java.lang.reflect.Constructor","java.lang.reflect.InvocationTargetException","java.lang.reflect.Method"] |

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
| axon-common-5.1.2 | false | 7 | 86 | 63.63636363636364 | 100 | 87.3365231259968 | 13.847888884820795 | 87.71929824561403 | 4 | 50 | 12.285714285714286 | 16.690459207925603 | 7 | 18.9873417721519 | 71.42857142857143 | 33.35037229074085 | 18.03744051894984 | 32.30769230769231 |
| axon-common-5.1.2 | true | 7 | 64 | 40 | 100 | 66.32946001367054 | 21.40920350674398 | 66.66666666666667 | 2 | 37 | 9.142857142857142 | 12.495713550768405 | 4 | 11.39240506329114 | 30.303030303030305 | 19.684682002425557 | 6.00094414198861 | 18.9873417721519 |
| axon-conversion-5.1.2 | true | 3 | 21 | 24.561403508771928 | 40 | 30.6113769271664 | 8.243027449975816 | 27.272727272727273 | 3 | 14 | 7 | 6.082762530298219 | 4 | 2.307692307692308 | 5.687203791469194 | 4.352729079467337 | 1.7983181859272792 | 5.063291139240507 |
| axon-conversion-5.1.2 | false | 1 | 5 | 8.771929824561402 | 8.771929824561402 | 8.771929824561402 | 0 | 8.771929824561402 | 5 | 5 | 5 | 0 | 5 | 0.7898894154818326 | 0.7898894154818326 | 0.7898894154818326 | 0 | 0.7898894154818326 |
| axon-eventsourcing-5.1.2 | true | 1 | 3 | 30 | 30 | 30 | 0 | 30 | 3 | 3 | 3 | 0 | 3 | 11.39240506329114 | 11.39240506329114 | 11.39240506329114 | 0 | 11.39240506329114 |
| axon-eventsourcing-5.1.2 | false | 1 | 3 | 30 | 30 | 30 | 0 | 30 | 3 | 3 | 3 | 0 | 3 | 11.39240506329114 | 11.39240506329114 | 11.39240506329114 | 0 | 11.39240506329114 |
| axon-messaging-5.1.2 | true | 4 | 24 | 40 | 100 | 75.45454545454545 | 25.302576660785583 | 80 | 4 | 9 | 6 | 2.449489742783178 | 4 | 30.37974683544304 | 43.43434343434344 | 38.33180883813795 | 5.764295545747308 | 37.9746835443038 |
| axon-messaging-5.1.2 | false | 4 | 26 | 40 | 100 | 75.22727272727273 | 26.632640136891368 | 70 | 2 | 10 | 6.5 | 3.3166247903554 | 7 | 11.39240506329114 | 29.230769230769234 | 21.851868244273312 | 7.936147876923812 | 20.202020202020204 |
| axon-modelling-5.1.2 | true | 1 | 5 | 45.45454545454546 | 45.45454545454546 | 45.45454545454546 | 0 | 45.45454545454546 | 5 | 5 | 5 | 0 | 5 | 13.076923076923078 | 13.076923076923078 | 13.076923076923078 | 0 | 13.076923076923078 |
| axon-modelling-5.1.2 | false | 1 | 2 | 18.181818181818183 | 18.181818181818183 | 18.181818181818183 | 0 | 18.181818181818183 | 2 | 2 | 2 | 0 | 2 | 3.076923076923077 | 3.076923076923077 | 3.076923076923077 | 0 | 3.076923076923077 |

[Full data](./InternalArtifactUsageSpreadPerDependency.csv)

### 7.2 Spread per Dependent (depends on most others)

| artifactName | dependencyTypeIsInterface | artifactDependencies | artifactDependencyPackages | dependentPackagesRate | minPackageSpread | maxPackageSpread | avgPackageSpread | stdPackageSpread | per5PackageSpread | minPackageCount | maxPackageCount | avgPackageCount | stdPackageCount | per5PackageCount | minTypeSpread | maxTypeSpread | avgTypeSpread | stdTypeSpread | per5TypeSpread |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| axon-conversion-5.1.2 | false | 1 | 2 | 80 | 80 | 80 | 80 | 0 | 80 | 4 | 4 | 4 | 0 | 4 | 19.51219512195122 | 19.51219512195122 | 19.51219512195122 | 0 | 19.51219512195122 |
| axon-conversion-5.1.2 | true | 1 | 1 | 80 | 80 | 80 | 80 | 0 | 80 | 4 | 4 | 4 | 0 | 4 | 21.95121951219512 | 21.95121951219512 | 21.95121951219512 | 0 | 21.95121951219512 |
| axon-eventsourcing-5.1.2 | true | 4 | 25 | 56.81818181818182 | 27.272727272727273 | 81.81818181818183 | 56.81818181818182 | 25.034411578573195 | 45.45454545454546 | 3 | 9 | 6.25 | 2.753785273643051 | 5 | 2.307692307692308 | 41.53846153846154 | 19.807692307692307 | 16.63359638200968 | 13.076923076923078 |
| axon-eventsourcing-5.1.2 | false | 3 | 15 | 57.57575757575758 | 18.181818181818183 | 90.90909090909092 | 57.57575757575758 | 36.74047167570347 | 63.63636363636364 | 2 | 10 | 6.333333333333333 | 4.041451884327381 | 7 | 3.076923076923077 | 32.30769230769231 | 21.53846153846154 | 16.062010013708537 | 29.230769230769234 |
| axon-messaging-5.1.2 | false | 2 | 9 | 48.24561403508772 | 8.771929824561402 | 87.71929824561403 | 48.24561403508771 | 55.82421956735901 | 8.771929824561402 | 5 | 50 | 27.5 | 31.81980515339464 | 5 | 0.7898894154818326 | 33.80726698262244 | 17.298578199052134 | 23.346811574721713 | 0.7898894154818326 |
| axon-messaging-5.1.2 | true | 2 | 9 | 44.73684210526316 | 24.561403508771928 | 64.91228070175438 | 44.73684210526316 | 28.532378889983498 | 24.561403508771928 | 14 | 37 | 25.5 | 16.263455967290593 | 14 | 5.687203791469194 | 17.061611374407583 | 11.374407582938389 | 8.042920733875421 | 5.687203791469194 |
| axon-metrics-micrometer-5.1.2 | true | 1 | 1 | 66.66666666666667 | 66.66666666666667 | 66.66666666666667 | 66.66666666666667 | 0 | 66.66666666666667 | 2 | 2 | 2 | 0 | 2 | 15.789473684210527 | 15.789473684210527 | 15.789473684210527 | 0 | 15.789473684210527 |
| axon-modelling-5.1.2 | true | 2 | 14 | 100 | 100 | 100 | 100 | 0 | 100 | 7 | 7 | 7 | 0 | 7 | 30.303030303030305 | 43.43434343434344 | 36.86868686868687 | 9.285240561035476 | 30.303030303030305 |
| axon-modelling-5.1.2 | false | 2 | 9 | 100 | 100 | 100 | 100 | 0 | 100 | 7 | 7 | 7 | 0 | 7 | 20.202020202020204 | 23.232323232323235 | 21.71717171717172 | 2.142747821777417 | 20.202020202020204 |
| axon-server-connector-5.1.2 | false | 3 | 16 | 60 | 30 | 80 | 60 | 26.457513110645905 | 70 | 3 | 8 | 6 | 2.6457513110645907 | 7 | 11.39240506329114 | 34.17721518987342 | 24.05063291139241 | 11.60145745558441 | 26.58227848101266 |

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
