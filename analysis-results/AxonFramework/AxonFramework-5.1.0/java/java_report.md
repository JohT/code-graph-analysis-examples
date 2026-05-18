---
title: "Java Report"
generated: "2026-05-18"
model_version: "v4.0.1"
dataset: "AxonFramework-5.1.0"
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
| /axon-eventsourcing-5.1.0.jar | 2 | 88 |
| /axon-conversion-5.1.0.jar | 5 | 112 |
| /axon-update-5.1.0.jar | 0 | 0 |
| /axoniq-spring-boot-autoconfigure-5.1.0.jar | 0 | 0 |
| /axon-modelling-5.1.0.jar | 2 | 56 |
| /axon-metrics-micrometer-5.1.0.jar | 0 | 0 |
| /axon-test-5.1.0.jar | 0 | 0 |
| /axon-tracing-opentelemetry-5.1.0.jar | 0 | 0 |
| /axon-messaging-5.1.0.jar | 7 | 1282 |
| /axon-server-connector-5.1.0.jar | 1 | 16 |

[Full data](./IncomingDependencies.csv)

### 2.2 Outgoing Artifact Dependencies

| a.fileName | outgoingDependencies | outgoingDependenciesWeight |
| --- | --- | --- |
| /axon-eventsourcing-5.1.0.jar | 4 | 662 |
| /axon-conversion-5.1.0.jar | 1 | 34 |
| /axon-update-5.1.0.jar | 1 | 54 |
| /axoniq-spring-boot-autoconfigure-5.1.0.jar | 4 | 58 |
| /axon-modelling-5.1.0.jar | 3 | 494 |
| /axon-metrics-micrometer-5.1.0.jar | 2 | 82 |
| /axon-test-5.1.0.jar | 3 | 290 |
| /axon-tracing-opentelemetry-5.1.0.jar | 2 | 24 |
| /axon-messaging-5.1.0.jar | 2 | 1070 |
| /axon-server-connector-5.1.0.jar | 5 | 504 |

[Full data](./OutgoingDependencies.csv)

### 2.3 Most Used Internal Dependencies

| dependency | usedByPackages | usedByTypes | providesPackages | providesTypes | interfaceRate | someProvidedPackages | someProvidedTypes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| axon-common-5.1.0 | 95 | 458 | 12 | 73 | 39.73 | ["org.axonframework.common","org.axonframework.common.io","org.axonframework.common.annotation","org.axonframework.common.jdbc","org.axonframework.common.util"] | ["DateTimeUtils","CollectionUtils","FutureUtils","ClassUtils","AxonTransientException"] |
| axon-messaging-5.1.0 | 33 | 184 | 31 | 108 | 51.85 | ["org.axonframework.messaging.monitoring","org.axonframework.messaging.monitoring.configuration","org.axonframework.messaging.commandhandling","org.axonframework.messaging.commandhandling.annotation","org.axonframework.messaging.commandhandling.configuration"] | ["MultiMessageMonitor","NoOpMessageMonitorCallback","NoOpMessageMonitor","MessageMonitor","MessageMonitor$MonitorCallback"] |
| axon-conversion-5.1.0 | 25 | 48 | 2 | 6 | 33.33 | ["org.axonframework.conversion","org.axonframework.conversion.jackson"] | ["ConversionException","Converter","CachingSupplier","GeneralConverter","DelegatingGeneralConverter"] |
| axon-eventsourcing-5.1.0 | 5 | 13 | 3 | 19 | 47.37 | ["org.axonframework.eventsourcing.snapshot.store","org.axonframework.eventsourcing.snapshot.api","org.axonframework.eventsourcing.eventstore"] | ["SnapshotStore","Snapshot","EventStoreException","EventStorageEngine$AppendTransaction","GlobalIndexPosition"] |
| axon-modelling-5.1.0 | 5 | 14 | 6 | 16 | 68.75 | ["org.axonframework.modelling","org.axonframework.modelling.annotation","org.axonframework.modelling.entity","org.axonframework.modelling.entity.annotation","org.axonframework.modelling.configuration"] | ["EntityEvolver","EntityIdResolver","StateManager","ConcurrencyException","EntityIdResolverDefinition"] |
| axon-server-connector-5.1.0 | 3 | 5 | 2 | 5 | 20 | ["io.axoniq.framework.axonserver.connector.api","io.axoniq.framework.axonserver.connector.configuration"] | ["AxonServerConfiguration","AxonServerConnectionManager","TagsConfiguration","TopologyChangeListener","AxonServerConfigurationEnhancer"] |

[Full data](./MostUsedDependenciesAcrossArtifacts.csv)

### 2.4 All Artifact Dependencies

| artifactName | packagesInArtifactCount | packagesCount | packageSpread | typesInArtifactCount | typesCount | typesSpread | dependencyArtifactName | dependencyTypeIsInterface | dependencyPackagesCount | dependencyTypesCount | someDependencyPackages | someDependencyTypes | someCallingPackages | someCallingTypes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| axon-messaging-5.1.0 | 57 | 50 | 87.72 | 634 | 215 | 33.91 | axon-common-5.1.0 | false | 7 | 36 | ["org.axonframework.common","org.axonframework.common.annotation"] | ["DateTimeUtils","CollectionUtils","FutureUtils","ClassUtils"] | ["org.axonframework.messaging.eventhandling.processing.streaming.token.store.jdbc","org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa"] | ["JdbcTokenEntry","JpaTokenStore","JdbcTokenStore","TokenEntry"] |
| axon-messaging-5.1.0 | 57 | 37 | 64.91 | 634 | 108 | 17.03 | axon-common-5.1.0 | true | 8 | 24 | ["org.axonframework.common","org.axonframework.common.jdbc"] | ["Registration","JdbcUtils$SqlResultConverter","Property","TransactionalExecutor"] | ["org.axonframework.messaging.core","org.axonframework.messaging.eventhandling"] | ["SubscribableEventSource","EventSubscribers","InterceptingEventBus","DelegatingEventBus"] |
| axon-messaging-5.1.0 | 57 | 14 | 24.56 | 634 | 36 | 5.68 | axon-conversion-5.1.0 | true | 1 | 2 | ["org.axonframework.conversion"] | ["Converter","GeneralConverter"] | ["org.axonframework.messaging.core.conversion","org.axonframework.messaging.eventhandling.processing.streaming.token.store.jdbc"] | ["MessageConverter","JdbcTokenEntry","ResultMessage","GenericQueryMessage"] |
| axon-eventsourcing-5.1.0 | 11 | 10 | 90.91 | 121 | 34 | 28.1 | axon-messaging-5.1.0 | false | 8 | 20 | ["org.axonframework.messaging.eventhandling","org.axonframework.messaging.eventhandling.annotation"] | ["TerminalEventMessage","SimpleEventBus","GenericEventMessage","InterceptingEventBus"] | ["org.axonframework.eventsourcing.eventstore.inmemory","org.axonframework.eventsourcing.eventstore.jpa"] | ["InMemoryEventStorageEngine$MapBackedSourcingEventMessageStream","AggregateBasedJpaEventStorageEngine","EventSourcingConfigurationDefaults","StoreBackedSnapshotter"] |
| axon-eventsourcing-5.1.0 | 11 | 9 | 81.82 | 121 | 52 | 42.98 | axon-messaging-5.1.0 | true | 13 | 30 | ["org.axonframework.messaging.commandhandling","org.axonframework.messaging.commandhandling.configuration"] | ["CommandHandlingComponent","CommandBus","CommandHandlingModule","EventBus"] | ["org.axonframework.eventsourcing.configuration","org.axonframework.eventsourcing.eventstore"] | ["SimpleEventSourcedEntityModule","EventSourcingConfigurer","StorageEngineBackedEventStore","EventStore"] |
| axon-eventsourcing-5.1.0 | 11 | 8 | 72.73 | 121 | 40 | 33.06 | axon-common-5.1.0 | false | 4 | 16 | ["org.axonframework.common","org.axonframework.common.io"] | ["DateTimeUtils","CollectionUtils","FutureUtils","AxonConfigurationException"] | ["org.axonframework.eventsourcing.eventstore.jpa","org.axonframework.eventsourcing.eventstore"] | ["AggregateBasedJpaEventStorageEngine","AggregateEventEntry","GapAwareTrackingTokenOperations","AggregateBasedConsistencyMarker"] |
| axon-server-connector-5.1.0 | 10 | 8 | 80 | 79 | 27 | 34.18 | axon-common-5.1.0 | false | 5 | 16 | ["org.axonframework.common","org.axonframework.common.annotation"] | ["FutureUtils","AxonConfigurationException","BuilderUtils","ExceptionUtils"] | ["io.axoniq.framework.axonserver.connector.query","io.axoniq.framework.axonserver.connector.configuration"] | ["AxonServerQueryBusConnector$AxonServerUpdateCallback","AxonServerQueryBusConnector","AxonServerConfigurationEnhancer","EventProcessorControlService"] |
| axon-eventsourcing-5.1.0 | 11 | 8 | 72.73 | 121 | 27 | 22.31 | axon-common-5.1.0 | true | 6 | 17 | ["org.axonframework.common","org.axonframework.common.jdbc"] | ["Registration","PersistenceExceptionResolver","TransactionalExecutor","DescribableComponent"] | ["org.axonframework.eventsourcing.eventstore","org.axonframework.eventsourcing.eventstore.jpa"] | ["StorageEngineBackedEventStore","InterceptingEventStore","AggregateBasedJpaEventStorageEngine","ContinuousMessageStream"] |
| axon-modelling-5.1.0 | 7 | 7 | 100 | 99 | 43 | 43.43 | axon-messaging-5.1.0 | true | 11 | 23 | ["org.axonframework.messaging.commandhandling","org.axonframework.messaging.commandhandling.annotation"] | ["CommandHandlingComponent","CommandHandler","CommandMessage","CommandResultMessage"] | ["org.axonframework.modelling.entity","org.axonframework.modelling.configuration"] | ["EntityCommandHandlingComponent","SimpleStateBasedEntityModule","EntityMetamodelBuilder","PolymorphicEntityMetamodelBuilder"] |
| axon-server-connector-5.1.0 | 10 | 7 | 70 | 79 | 21 | 26.58 | axon-messaging-5.1.0 | false | 9 | 30 | ["org.axonframework.messaging.commandhandling","org.axonframework.messaging.eventhandling"] | ["CommandDispatchException","GenericCommandResultMessage","NoHandlerForCommandException","CommandExecutionException"] | ["io.axoniq.framework.axonserver.connector.api.command","io.axoniq.framework.axonserver.connector.command"] | ["AxonServerCommandDispatchException","CommandConverter","ExceptionFactory","AggregateBasedAxonServerEventStorageEngine"] |

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
| axon-common-5.1.0.jar | 1 | 392 |
| axon-common-5.1.0.jar | 2 | 152 |
| axon-common-5.1.0.jar | 3 | 101 |
| axon-common-5.1.0.jar | 4 | 37 |
| axon-common-5.1.0.jar | 5 | 38 |
| axon-common-5.1.0.jar | 6 | 38 |
| axon-common-5.1.0.jar | 7 | 19 |
| axon-common-5.1.0.jar | 8 | 18 |
| axon-common-5.1.0.jar | 9 | 12 |
| axon-common-5.1.0.jar | 10 | 6 |

[Full data](./EffectiveMethodLineCountDistribution.csv)

### 3.2 Top Types by Effective LOC

| artifactName | packageName | typeName | sumEffectiveLinesOfMethodCode | maxEffectiveLinesOfMethodCode | methodWithMaxEffectiveLinesOfMethodCode | maxCyclomaticComplexity | methodWithMaxCyclomaticComplexity |
| --- | --- | --- | --- | --- | --- | --- | --- |
| axon-messaging-5.1.0 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | Coordinator$CoordinationTask | 398 | 111 | run | 25 | run |
| axon-messaging-5.1.0 | org.axonframework.messaging.eventhandling.processing.streaming.token.store.jdbc | JdbcTokenStore | 305 | 25 | updateToken | 8 | updateToken |
| axon-test-5.1.0 | org.axonframework.test.fixture | Reporter | 224 | 45 | appendEventOverview | 11 | appendEventOverview |
| axon-eventsourcing-5.1.0 | org.axonframework.eventsourcing.eventstore.jpa | AggregateBasedJpaEventStorageEngine | 191 | 17 | <init> | 5 | lambda$queryTokensAndEventsBy$16 |
| axon-messaging-5.1.0 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | WorkPackage | 190 | 25 | processEvents | 7 | processEvents |
| axon-common-5.1.0 | org.axonframework.common.configuration | DefaultComponentRegistry | 185 | 18 | invokeEnhancers | 8 | registerComponent |
| axon-common-5.1.0 | org.axonframework.common | ReflectionUtils | 177 | 17 | fieldNameFromMember | 9 | fieldNameFromMember |
| axon-messaging-5.1.0 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | PooledStreamingEventProcessor | 175 | 37 | <init> | 3 | lambda$processWithErrorHandling$20 |
| axon-modelling-5.1.0 | org.axonframework.modelling.entity.annotation | AnnotatedEntityMetamodel | 168 | 18 | createOptionalChildForMember | 6 | getExpectedRepresentation |
| axon-messaging-5.1.0 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | PooledStreamingEventProcessorConfiguration | 160 | 18 | describeTo | 2 | ignoredMessageHandler |

[Full data](./EffectiveLinesOfMethodCodePerType.csv)

### 3.3 Top Packages by Effective LOC

| artifactName | fullPackageName | linesInPackage | complexityInPackage | methodCount | maxLinesMethod | maxLinesMethodType | maxLinesMethodName | maxComplexity | maxComplexityType | maxComplexityMethod | packageName |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| axon-messaging-5.1.0 | org.axonframework.messaging.eventhandling.processing.streaming.pooled | 1502 | 588 | 430 | 111 | Coordinator$CoordinationTask | run | 25 | Coordinator$CoordinationTask | run | pooled |
| axon-messaging-5.1.0 | org.axonframework.messaging.core | 1180 | 746 | 530 | 20 | AbstractMessageStream | next | 11 | QueueMessageStream | fetchNext | core |
| axon-common-5.1.0 | org.axonframework.common.configuration | 766 | 411 | 303 | 26 | DefaultAxonApplication$AxonConfigurationImpl | invokeLifecycleHandlers | 8 | DefaultComponentRegistry | registerComponent | configuration |
| axon-test-5.1.0 | org.axonframework.test.fixture | 752 | 324 | 211 | 45 | Reporter | appendEventOverview | 11 | Reporter | appendEventOverview | fixture |
| axon-messaging-5.1.0 | org.axonframework.messaging.core.annotation | 713 | 378 | 239 | 23 | MethodInvokingMessageHandlingMember | <init> | 13 | MessageStreamResolverUtils | resolveToStream | annotation |
| axon-common-5.1.0 | org.axonframework.common | 654 | 408 | 194 | 24 | TypeReflectionUtils | getExactDirectSuperTypesOfParameterizedTypeOrClass | 9 | ReflectionUtils | fieldNameFromMember | common |
| axon-eventsourcing-5.1.0 | org.axonframework.eventsourcing.eventstore | 589 | 368 | 231 | 19 | AnnotationBasedTagResolver | createTagsForValue | 8 | AggregateBasedConsistencyMarker | from | eventstore |
| axon-server-connector-5.1.0 | io.axoniq.framework.axonserver.connector.event | 541 | 217 | 161 | 21 | AggregateBasedAxonServerEventStorageEngine | lambda$appendEvents$0 | 4 | AggregateBasedAxonServerEventStorageEngine | lambda$appendEvents$0 | event |
| axon-messaging-5.1.0 | org.axonframework.messaging.eventhandling.processing.streaming.token.store.jdbc | 443 | 194 | 109 | 25 | JdbcTokenStore | updateToken | 8 | JdbcTokenStore | updateToken | jdbc |
| axon-eventsourcing-5.1.0 | org.axonframework.eventsourcing.eventstore.jpa | 437 | 204 | 135 | 20 | GapAwareTrackingTokenOperations | withGapsCleaned | 8 | SQLErrorCodesResolver | loadKeyViolationCodes | jpa |

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
| org.jspecify.annotations.NullMarked | Interface | 124 | ["org.axonframework.eventsourcing.annotation.reflection.package-info","org.axonframework.eventsourcing.annotation.package-info","org.axonframework.eventsourcing.snapshot.inmemory.package-info","org.axonframework.eventsourcing.snapshot.store.package-info","org.axonframework.eventsourcing.snapshot.api.package-info","org.axonframework.eventsourcing.package-info","org.axonframework.eventsourcing.handler.package-info","org.axonframework.eventsourcing.eventstore.inmemory.package-info","org.axonframework.eventsourcing.eventstore.package-info"] |
| org.axonframework.common.annotation.Internal | Class | 90 | ["org.axonframework.eventsourcing.snapshot.store.StoreBackedSnapshotter","org.axonframework.eventsourcing.handler.InitializingEntityEvolver","org.axonframework.eventsourcing.handler.SimpleSourcingHandler","org.axonframework.eventsourcing.handler.SnapshottingSourcingHandler","org.axonframework.eventsourcing.eventstore.ContinuousMessageStream","org.axonframework.eventsourcing.eventstore.InterceptingEventStore","org.axonframework.eventsourcing.eventstore.jpa.JpaPollingEventCoordinator","org.axonframework.eventsourcing.eventstore.StreamSpliterator","org.axonframework.update.UpdateChecker"] |
| java.lang.FunctionalInterface | Interface | 57 | ["org.axonframework.eventsourcing.EventSourcedEntityFactory","org.axonframework.eventsourcing.CriteriaResolver","org.axonframework.eventsourcing.eventstore.TagResolver","org.axonframework.update.configuration.EnvironmentVariableUsagePropertyProvider$EnvironmentVariableSupplier","org.axonframework.modelling.EntityIdResolver","org.axonframework.modelling.annotation.EntityIdResolverDefinition","org.axonframework.modelling.entity.EntityCommandHandler","org.axonframework.modelling.entity.child.EventTargetMatcher","org.axonframework.modelling.entity.child.CommandTargetResolver"] |
| java.lang.annotation.Target | Annotation | 42 | ["org.axonframework.eventsourcing.annotation.EventSourcedEntity","org.axonframework.eventsourcing.annotation.EventTag","org.axonframework.eventsourcing.annotation.reflection.EntityCreator","org.axonframework.eventsourcing.annotation.EventTags","org.axonframework.eventsourcing.annotation.reflection.InjectEntityId","org.axonframework.eventsourcing.annotation.EventSourcingHandler","org.axonframework.eventsourcing.annotation.EventCriteriaBuilder","org.axonframework.modelling.annotation.TargetEntityId","org.axonframework.modelling.annotation.InjectEntity"] |
| java.lang.annotation.Retention | Annotation | 42 | ["org.axonframework.eventsourcing.annotation.EventSourcedEntity","org.axonframework.eventsourcing.annotation.EventTag","org.axonframework.eventsourcing.annotation.reflection.EntityCreator","org.axonframework.eventsourcing.annotation.EventTags","org.axonframework.eventsourcing.annotation.reflection.InjectEntityId","org.axonframework.eventsourcing.annotation.EventSourcingHandler","org.axonframework.eventsourcing.annotation.EventCriteriaBuilder","org.axonframework.modelling.annotation.TargetEntityId","org.axonframework.modelling.annotation.InjectEntity"] |
| org.axonframework.common.annotation.Internal | Interface | 27 | ["org.axonframework.eventsourcing.snapshot.store.SnapshotStore","org.axonframework.eventsourcing.handler.SourcingHandler","org.axonframework.eventsourcing.snapshot.api.Snapshotter","org.axonframework.eventsourcing.eventstore.EventCoordinator","org.axonframework.eventsourcing.eventstore.EventStorageEngine","org.axonframework.update.configuration.UsagePropertyProvider","org.axonframework.modelling.entity.annotation.AnnotatedEntityMetamodelFactory","org.axonframework.messaging.monitoring.configuration.MessageMonitorRegistry","org.axonframework.messaging.commandhandling.annotation.CommandHandlingMember"] |
| org.axonframework.common.annotation.Internal | Constructor | 19 | ["org.axonframework.eventsourcing.eventstore.AggregateSequenceNumberPosition.<init>","org.axonframework.eventsourcing.eventstore.InterceptingEventStore.<init>","org.axonframework.eventsourcing.eventstore.GlobalIndexPosition.<init>","org.axonframework.conversion.jackson.JacksonConverter.<init>","org.axonframework.conversion.jackson2.Jackson2Converter.<init>","org.axonframework.conversion.avro.AvroConverter.<init>","org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessorsConfigurer.<init>","org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessorConfiguration.<init>","org.axonframework.messaging.eventhandling.processing.streaming.segmenting.SequenceCachingEventHandlingComponent.<init>"] |
| org.springframework.context.annotation.Bean | Method | 15 | ["io.axoniq.framework.springboot.autoconfig.PostgresqlAutoConfiguration.disablePostgresqlConfigurationEnhancer","io.axoniq.framework.springboot.autoconfig.JpaDeadLetterQueueAutoConfiguration.jpaDeadLetterQueueFactory","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.disableAxonServerConfigurationEnhancer","io.axoniq.framework.springboot.autoconfig.DeadLetterQueueAutoConfiguration.dlqCustomization","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.axonServerConfigurationEnhancer","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.axonServerConfigurationWithConnectionDetails","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.tagsConfiguration","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration.topologyChangeListenerConfigurerModule","io.axoniq.framework.springboot.autoconfig.JdbcDeadLetterQueueAutoConfiguration.deadLetterSchema"] |
| java.lang.annotation.Documented | Annotation | 14 | ["org.axonframework.eventsourcing.annotation.EventSourcingHandler","org.axonframework.modelling.entity.annotation.EntityMember","org.axonframework.messaging.commandhandling.annotation.CommandHandler","org.axonframework.messaging.eventhandling.annotation.EventHandler","org.axonframework.messaging.eventhandling.replay.annotation.AllowReplay","org.axonframework.messaging.eventhandling.replay.annotation.DisallowReplay","org.axonframework.messaging.queryhandling.annotation.QueryHandler","org.axonframework.messaging.core.annotation.SequencingPolicy","org.axonframework.messaging.core.annotation.HasHandlerAttributes"] |
| org.axonframework.common.annotation.Internal | Method | 13 | ["org.axonframework.conversion.DelegatingGeneralConverter.delegate","org.axonframework.messaging.eventhandling.processing.streaming.token.store.jdbc.JdbcTokenStore.converter","org.axonframework.messaging.eventhandling.conversion.DelegatingEventConverter.delegate","org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa.JpaTokenStore.converter","org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessorsConfigurer.build","org.axonframework.messaging.eventhandling.processing.subscribing.SubscribingEventProcessorsConfigurer.build","org.axonframework.messaging.core.interception.annotation.MessageHandlerInterceptorMemberChain.handleSync","org.axonframework.messaging.core.annotation.MessageHandlingMember.handleSync","org.axonframework.messaging.core.Context.resources"] |

[Full data](./AnnotatedCodeElements.csv)

### 4.2 Annotated Code Elements per Artifact

| artifactName | annotationName | languageElement | numberOfAnnotatedElements | examples |
| --- | --- | --- | --- | --- |
| axon-common-5.1.0 | org.jspecify.annotations.NullMarked | Interface | 15 | ["org.axonframework.common.io.package-info","org.axonframework.common.annotation.package-info","org.axonframework.common.jdbc.package-info","org.axonframework.common.package-info","org.axonframework.common.util.package-info","org.axonframework.common.property.package-info","org.axonframework.common.caching.package-info","org.axonframework.common.digest.package-info","org.axonframework.common.tx.package-info"] |
| axon-common-5.1.0 | java.lang.FunctionalInterface | Interface | 12 | ["org.axonframework.common.jdbc.JdbcUtils$SqlResultConverter","org.axonframework.common.jdbc.ConnectionProvider","org.axonframework.common.jdbc.JdbcUtils$SqlFunction","org.axonframework.common.util.ExecutorServiceFactory","org.axonframework.common.property.Property","org.axonframework.common.Registration","org.axonframework.common.infra.DescribableComponent","org.axonframework.common.lock.LockFactory","org.axonframework.common.configuration.ConfigurationEnhancer"] |
| axon-common-5.1.0 | org.axonframework.common.annotation.Internal | Class | 7 | ["org.axonframework.common.jdbc.ConnectionExecutor","org.axonframework.common.jdbc.JdbcUtils","org.axonframework.common.jpa.EntityManagerExecutor","org.axonframework.common.configuration.LazyInitializedComponentDefinition","org.axonframework.common.configuration.ConfigurationExtensions","org.axonframework.common.configuration.InstantiatedComponentDefinition","org.axonframework.common.configuration.Components"] |
| axon-common-5.1.0 | org.axonframework.common.annotation.Internal | Interface | 7 | ["org.axonframework.common.jdbc.ConnectionProvider","org.axonframework.common.tx.TransactionalExecutor","org.axonframework.common.jpa.EntityManagerProvider","org.axonframework.common.configuration.ExtensibleConfigurer","org.axonframework.common.configuration.ConfigurationExtension","org.axonframework.common.configuration.Component","org.axonframework.common.configuration.ExtendedConfiguration"] |
| axon-common-5.1.0 | java.lang.annotation.Retention | Annotation | 3 | ["org.axonframework.common.annotation.Internal","org.axonframework.common.annotation.RegistrationScope","org.axonframework.common.Priority"] |
| axon-common-5.1.0 | java.lang.annotation.Target | Annotation | 3 | ["org.axonframework.common.annotation.Internal","org.axonframework.common.annotation.RegistrationScope","org.axonframework.common.Priority"] |
| axon-common-5.1.0 | java.lang.annotation.Documented | Annotation | 2 | ["org.axonframework.common.annotation.Internal","org.axonframework.common.annotation.RegistrationScope"] |
| axon-common-5.1.0 | org.axonframework.common.annotation.Internal | Method | 2 | ["org.axonframework.common.configuration.DefaultComponentRegistry.create","org.axonframework.common.configuration.DefaultComponentRegistry.createLocalConfiguration"] |
| axon-common-5.1.0 | java.lang.annotation.Inherited | Annotation | 1 | ["org.axonframework.common.Priority"] |
| axon-conversion-5.1.0 | org.jspecify.annotations.NullMarked | Interface | 5 | ["org.axonframework.conversion.package-info","org.axonframework.conversion.jackson.package-info","org.axonframework.conversion.converter.package-info","org.axonframework.conversion.jackson2.package-info","org.axonframework.conversion.avro.package-info"] |

[Full data](./AnnotatedCodeElementsPerArtifact.csv)

### 4.3 Deprecated Element Usages

| artifactName | deprecatedElement | numberOfElementsUsingDeprecatedElements | someElementsUsingDeprecatedElements |
| --- | --- | --- | --- |
| axon-eventsourcing-5.1.0 | Field | 2 | ["org.axonframework.eventsourcing.snapshot.store.StoreBackedSnapshotter.store","org.axonframework.eventsourcing.eventstore.jpa.GapAwareTrackingTokenOperations.gapTimeoutThreshold"] |
| axon-messaging-5.1.0 | Class | 1 | ["org.axonframework.messaging.core.interception.annotation.MessageHandlerInterceptorMemberChain"] |
| axon-messaging-5.1.0 | Method | 3 | ["org.axonframework.messaging.core.annotation.WrappedMessageHandlingMember.handleSync","org.axonframework.messaging.core.annotation.ChainedMessageHandlerInterceptorMember.doHandleSync","org.axonframework.messaging.core.interception.annotation.MessageHandlerInterceptorMemberChain.handle"] |
| axon-messaging-5.1.0 | Field | 8 | ["org.axonframework.messaging.eventhandling.processing.streaming.pooled.WorkPackage$Builder.<init>","org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessor.releaseSegment","org.axonframework.messaging.eventhandling.processing.streaming.pooled.PooledStreamingEventProcessorConfiguration.<init>","org.axonframework.messaging.eventhandling.processing.streaming.pooled.Coordinator$CoordinationTask.lambda$releaseSegmentsIfTooManyClaimed$13","org.axonframework.messaging.eventhandling.processing.streaming.pooled.Coordinator$Builder.<init>","org.axonframework.messaging.eventhandling.gateway.EventPublishingUtils.lambda$asEventMessage$1","org.axonframework.messaging.eventhandling.GenericEventMessage.<init>","org.axonframework.messaging.eventhandling.gateway.EventPublishingUtils.lambda$asEventMessage$0"] |

[Full data](./DeprecatedElementUsage.csv)

### 4.4 Reflection Usages

| dependentArtifactName | numberOfReflectionCaller | someReflectionCaller | someReflectionTypes |
| --- | --- | --- | --- |
| axon-eventsourcing-5.1.0 | 121 | ["org.axonframework.eventsourcing.snapshot.api.Snapshotter","org.axonframework.eventsourcing.eventstore.inmemory.InMemoryEventStorageEngine$MapBackedSourcingEventMessageStream","org.axonframework.eventsourcing.handler.InitializingEntityEvolver","org.axonframework.eventsourcing.handler.SnapshottingSourcingHandler","org.axonframework.eventsourcing.handler.SourcingHandler","org.axonframework.eventsourcing.annotation.reflection.package-info","org.axonframework.eventsourcing.eventstore.EventStorageEngine$AppendTransaction","org.axonframework.eventsourcing.eventstore.AggregateSequenceNumberPosition","org.axonframework.eventsourcing.CriteriaResolver","org.axonframework.eventsourcing.snapshot.store.package-info","org.axonframework.eventsourcing.annotation.reflection.AnnotationBasedEventSourcedEntityFactory$ScannedEntityCreator","org.axonframework.eventsourcing.eventstore.AbstractConsistencyMarker","org.axonframework.eventsourcing.annotation.reflection.AnnotationBasedEventSourcedEntityFactory","org.axonframework.eventsourcing.configuration.SimpleEventSourcedEntityModule$5","org.axonframework.eventsourcing.eventstore.jpa.AggregateBasedJpaEventStorageEngine$1","org.axonframework.eventsourcing.eventstore.GenericTaggedEventMessage","org.axonframework.eventsourcing.eventstore.EventCoordinator","org.axonframework.eventsourcing.EventSourcingRepository","org.axonframework.eventsourcing.eventstore.inmemory.InMemoryEventStorageEngine$MapBackedStreamingEventMessageStream"] | ["java.lang.reflect.Constructor","java.lang.reflect.Executable","java.lang.reflect.Method","java.lang.reflect.Modifier","java.lang.reflect.InvocationTargetException","java.lang.reflect.AnnotatedElement","java.lang.reflect.Field","java.lang.reflect.Member"] |
| axon-conversion-5.1.0 | 41 | ["org.axonframework.conversion.jackson2.ObjectNodeToJsonNodeConverter","org.axonframework.conversion.ChainedConverter","org.axonframework.conversion.avro.AvroConverter","org.axonframework.conversion.jackson2.package-info","org.axonframework.conversion.jackson.JsonNodeToObjectNodeConverter","org.axonframework.conversion.jackson2.JsonNodeToObjectNodeConverter","org.axonframework.conversion.PassThroughConverter","org.axonframework.conversion.converter.ByteArrayToInputStreamConverter","org.axonframework.conversion.avro.ByteArrayToGenericRecordConverter","org.axonframework.conversion.ContentTypeConverter","org.axonframework.conversion.jackson2.Jackson2Converter","org.axonframework.conversion.converter.ByteArrayToStringConverter","org.axonframework.conversion.GeneralConverter","org.axonframework.conversion.package-info","org.axonframework.conversion.converter.InputStreamToByteArrayConverter","org.axonframework.conversion.ChainingContentTypeConverter","org.axonframework.conversion.avro.AvroConverterConfiguration","org.axonframework.conversion.jackson2.ByteArrayToJsonNodeConverter","org.axonframework.conversion.avro.SpecificRecordBaseConverterStrategy"] | ["java.lang.reflect.Type","java.lang.reflect.Constructor","java.lang.reflect.InvocationTargetException","java.lang.reflect.Method"] |
| axon-update-5.1.0 | 28 | ["org.axonframework.update.configuration.UsagePropertyProvider","org.axonframework.update.api.DetectedVulnerabilitySeverity","org.axonframework.update.configuration.HierarchicalUsagePropertyProvider","org.axonframework.update.detection.TestEnvironmentDetector","org.axonframework.update.api.Artifact","org.axonframework.update.configuration.EnvironmentVariableUsagePropertyProvider$EnvironmentVariableSupplier","org.axonframework.update.configuration.package-info","org.axonframework.update.configuration.PropertyFileUsagePropertyProvider","org.axonframework.update.UpdateChecker","org.axonframework.update.detection.MachineId","org.axonframework.update.api.package-info","org.axonframework.update.detection.package-info","org.axonframework.update.api.ArtifactAvailableUpgrade","org.axonframework.update.package-info","org.axonframework.update.configuration.CommandLineUsagePropertyProvider","org.axonframework.update.UpdateCheckerHttpClient","org.axonframework.update.detection.AxonVersionDetector","org.axonframework.update.api.UpdateCheckRequest","org.axonframework.update.api.UpdateCheckResponse"] | ["java.lang.reflect.Method"] |
| axoniq-spring-boot-autoconfigure-5.1.0 | 26 | ["io.axoniq.framework.springboot.actuator.axonserver.AxonServerHealthIndicator","io.axoniq.framework.springboot.autoconfig.package-info","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration$1","io.axoniq.framework.springboot.actuator.axonserver.AxonServerStatusAggregator","io.axoniq.framework.springboot.service.connection.AxonServerConnectionDetails","io.axoniq.framework.springboot.actuator.HealthStatus","io.axoniq.framework.springboot.actuator.axonserver.package-info","io.axoniq.framework.springboot.PostgresqlProperties","io.axoniq.framework.springboot.DeadLetterQueueProcessorProperties$DlqProcessorSettings","io.axoniq.framework.springboot.service.connection.AxonServerTestContainerConnectionDetailsFactory","io.axoniq.framework.springboot.autoconfig.JpaDeadLetterQueueAutoConfiguration","io.axoniq.framework.springboot.service.connection.AxonServerDockerComposeConnectionDetailsFactory","io.axoniq.framework.springboot.DeadLetterQueueProcessorProperties","io.axoniq.framework.springboot.TagsConfigurationProperties","io.axoniq.framework.springboot.actuator.package-info","io.axoniq.framework.springboot.DeadLetterQueueProcessorProperties$DlqCache","io.axoniq.framework.springboot.autoconfig.DeadLetterQueueAutoConfiguration","io.axoniq.framework.springboot.autoconfig.AxonServerAutoConfiguration","io.axoniq.framework.springboot.autoconfig.PostgresqlAutoConfiguration"] | [] |
| axon-modelling-5.1.0 | 99 | ["org.axonframework.modelling.EntityIdResolutionException","org.axonframework.modelling.configuration.StateBasedEntityModule$PersisterPhase","org.axonframework.modelling.entity.PolymorphicEntityMetamodel$Builder","org.axonframework.modelling.StateEvolvingException","org.axonframework.modelling.SimpleEntityEvolvingComponent","org.axonframework.modelling.entity.child.AbstractEntityChildMetamodel$Builder","org.axonframework.modelling.StateManager","org.axonframework.modelling.entity.annotation.RoutingKeyEventTargetMatcher","org.axonframework.modelling.repository.InMemoryRepository","org.axonframework.modelling.entity.child.GetterEvolverChildEntityFieldDefinition","org.axonframework.modelling.PropertyBasedEntityIdResolver","org.axonframework.modelling.RepositoryAlreadyRegisteredException","org.axonframework.modelling.entity.annotation.RoutingKeyCommandTargetResolverDefinition","org.axonframework.modelling.repository.SimpleRepository","org.axonframework.modelling.annotation.TargetEntityIdMemberMismatchException","org.axonframework.modelling.entity.child.EventTargetMatcher","org.axonframework.modelling.annotation.AnnotationBasedEntityIdResolverDefinition","org.axonframework.modelling.entity.annotation.RoutingKeyUtils","org.axonframework.modelling.configuration.SimpleStateBasedEntityModule$3"] | ["java.lang.reflect.AnnotatedElement","java.lang.reflect.Member","java.lang.reflect.Executable","java.lang.reflect.Parameter","java.lang.reflect.ParameterizedType","java.lang.reflect.Field","java.lang.reflect.Method","java.lang.reflect.Modifier"] |
| axon-metrics-micrometer-5.1.0 | 19 | ["org.axonframework.extension.metrics.micrometer.EventProcessorLatencyMonitor","org.axonframework.extension.metrics.micrometer.springboot.MicrometerMetricsAutoConfiguration","org.axonframework.extension.metrics.micrometer.MessageTimerMonitor$1","org.axonframework.extension.metrics.micrometer.MessageCountingMonitor$1","org.axonframework.extension.metrics.micrometer.reservoir.SlidingTimeWindowReservoir","org.axonframework.extension.metrics.micrometer.reservoir.package-info","org.axonframework.extension.metrics.micrometer.springboot.package-info","org.axonframework.extension.metrics.micrometer.springboot.MetricsProperties","org.axonframework.extension.metrics.micrometer.springboot.MetricsProperties$Micrometer","org.axonframework.extension.metrics.micrometer.MetricsConfigurationEnhancer","org.axonframework.extension.metrics.micrometer.TagsUtil","org.axonframework.extension.metrics.micrometer.package-info","org.axonframework.extension.metrics.micrometer.CapacityMonitor$1","org.axonframework.extension.metrics.micrometer.MessageTimerMonitor$Builder","org.axonframework.extension.metrics.micrometer.CapacityMonitor","org.axonframework.extension.metrics.micrometer.MessageCountingMonitor","org.axonframework.extension.metrics.micrometer.springboot.MicrometerMetricsAutoConfiguration$1","org.axonframework.extension.metrics.micrometer.MessageTimerMonitor","org.axonframework.extension.metrics.micrometer.EventProcessorLatencyMonitor$Builder"] | [] |
| axon-test-5.1.0 | 79 | ["org.axonframework.test.fixture.AxonTestGiven","org.axonframework.test.fixture.AxonTestPhase$Then","org.axonframework.test.fixture.AxonTestThenMessage","org.axonframework.test.fixture.RecordingEventBus","org.axonframework.test.package-info","org.axonframework.test.matchers.MapStringEntryMatcher$Matching","org.axonframework.test.matchers.NonStaticFieldsFilter","org.axonframework.test.extension.AxonFrameworkExtension","org.axonframework.test.fixture.AxonTestThenCommand","org.axonframework.test.matchers.FieldFilter","org.axonframework.test.fixture.AxonTestWhen","org.axonframework.test.fixture.AxonTestPhase","org.axonframework.test.matchers.Matchers","org.axonframework.test.extension.ProvidedAxonTestFixture","org.axonframework.test.matchers.MatchAllFieldFilter","org.axonframework.test.matchers.ListMatcher","org.axonframework.test.matchers.NonTransientFieldsFilter","org.axonframework.test.matchers.EmptyCollectionMatcher","org.axonframework.test.FixtureResourceParameterResolverFactory$FailingParameterResolver"] | ["java.lang.reflect.Field","java.lang.reflect.Modifier","java.lang.reflect.Parameter","java.lang.reflect.Executable","java.lang.reflect.AnnotatedElement","java.lang.reflect.Constructor","java.lang.reflect.Method"] |
| axon-tracing-opentelemetry-5.1.0 | 6 | ["org.axonframework.extension.tracing.opentelemetry.package-info","org.axonframework.extension.tracing.opentelemetry.MetadataContextGetter","org.axonframework.extension.tracing.opentelemetry.OpenTelemetrySpan","org.axonframework.extension.tracing.opentelemetry.OpenTelemetrySpanFactory","org.axonframework.extension.tracing.opentelemetry.MetadataContextSetter","org.axonframework.extension.tracing.opentelemetry.OpenTelemetrySpanFactory$Builder"] | [] |
| axon-messaging-5.1.0 | 634 | ["org.axonframework.messaging.commandhandling.SimpleCommandHandlingComponent","org.axonframework.messaging.queryhandling.annotation.QueryHandlingMember","org.axonframework.messaging.core.unitofwork.UnitOfWorkConfiguration","org.axonframework.messaging.queryhandling.tracing.QueryBusSpanFactory","org.axonframework.messaging.queryhandling.SubscriptionQueryAlreadyRegisteredException","org.axonframework.messaging.queryhandling.SubscriptionQueryUpdateMessage","org.axonframework.messaging.core.interception.HandlerInterceptorFactory","org.axonframework.messaging.core.RemoteExceptionDescription","org.axonframework.messaging.monitoring.configuration.package-info","org.axonframework.messaging.commandhandling.CommandBus","org.axonframework.messaging.core.interception.DefaultDispatchInterceptorRegistry$5","org.axonframework.messaging.commandhandling.gateway.ConvertingCommandGateway","org.axonframework.messaging.eventhandling.processing.streaming.token.store.jpa.TokenEntry$PK","org.axonframework.messaging.core.correlation.MessageOriginProvider","org.axonframework.messaging.eventhandling.processing.streaming.segmenting.SequenceCachingEventHandlingComponent$SequenceIdentifiersCache","org.axonframework.messaging.core.Message","org.axonframework.messaging.core.unitofwork.TransactionalUnitOfWorkFactory","org.axonframework.messaging.tracing.HandlerSpanFactory","org.axonframework.messaging.core.unitofwork.UnitOfWork$UnitOfWorkProcessingContext"] | ["java.lang.reflect.Type","java.lang.reflect.Member","java.lang.reflect.Executable","java.lang.reflect.Parameter","java.lang.reflect.Method","java.lang.reflect.Constructor","java.lang.reflect.Modifier","java.lang.reflect.AnnotatedElement","java.lang.reflect.Field","java.lang.reflect.InvocationTargetException","java.lang.reflect.WildcardType"] |
| axon-server-connector-5.1.0 | 79 | ["io.axoniq.framework.axonserver.connector.configuration.TopologyChange$HandlerSubscription","io.axoniq.framework.axonserver.connector.query.package-info","io.axoniq.framework.axonserver.connector.query.AxonServerQueryBusConnector$AxonServerUpdateCallback","io.axoniq.framework.axonserver.connector.query.AxonServerQueryBusConnector$LocalSegmentAdapter","io.axoniq.framework.axonserver.connector.api.command.AxonServerCommandDispatchException","io.axoniq.framework.axonserver.connector.query.FlowControlledResponseSender","io.axoniq.framework.axonserver.connector.util.Scheduler","io.axoniq.framework.axonserver.connector.event.AggregateBasedAxonServerEventStorageEngine$1","io.axoniq.framework.axonserver.connector.util.GrpcMessageSizeInterceptor$1$1","io.axoniq.framework.axonserver.connector.command.CommandConverter","io.axoniq.framework.axonserver.connector.api.command.AxonServerRemoteCommandHandlingException","io.axoniq.framework.axonserver.connector.api.command.package-info","io.axoniq.framework.axonserver.connector.api.AxonServerConfiguration$Eventhandling$ProcessorSettings","io.axoniq.framework.axonserver.connector.api.AxonServerConfiguration$Eventhandling","io.axoniq.framework.axonserver.connector.event.AxonServerMessageStream","io.axoniq.framework.axonserver.connector.api.AxonServerConnectionManager$Builder","io.axoniq.framework.axonserver.connector.configuration.TopologyChange$Type","io.axoniq.framework.axonserver.connector.snapshot.AxonServerSnapshotStore","io.axoniq.framework.axonserver.connector.util.package-info"] | [] |

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
| axon-common-5.1.0 | false | 7 | 86 | 72.72727272727273 | 100 | 86.59440809816749 | 10.333841343344218 | 85.71428571428572 | 4 | 50 | 12.285714285714286 | 16.700441967348105 | 6 | 18.9873417721519 | 71.42857142857143 | 33.328152699818546 | 18.132188715158485 | 33.057851239669425 |
| axon-common-5.1.0 | true | 7 | 64 | 40 | 100 | 66.32946001367054 | 21.40920350674398 | 66.66666666666667 | 2 | 37 | 9.142857142857142 | 12.495713550768405 | 4 | 11.39240506329114 | 30.303030303030305 | 19.68174574815904 | 6.003377070092554 | 18.9873417721519 |
| axon-conversion-5.1.0 | false | 1 | 5 | 8.771929824561402 | 8.771929824561402 | 8.771929824561402 | 0 | 8.771929824561402 | 5 | 5 | 5 | 0 | 5 | 0.7886435331230284 | 0.7886435331230284 | 0.7886435331230284 | 0 | 0.7886435331230284 |
| axon-conversion-5.1.0 | true | 3 | 21 | 24.561403508771928 | 40 | 30.6113769271664 | 8.243027449975816 | 27.272727272727273 | 3 | 14 | 7 | 6.082762530298219 | 4 | 2.479338842975207 | 5.678233438485804 | 4.406954473567172 | 1.6974436727995181 | 5.063291139240507 |
| axon-eventsourcing-5.1.0 | true | 1 | 3 | 30 | 30 | 30 | 0 | 30 | 3 | 3 | 3 | 0 | 3 | 11.39240506329114 | 11.39240506329114 | 11.39240506329114 | 0 | 11.39240506329114 |
| axon-eventsourcing-5.1.0 | false | 1 | 3 | 30 | 30 | 30 | 0 | 30 | 3 | 3 | 3 | 0 | 3 | 11.39240506329114 | 11.39240506329114 | 11.39240506329114 | 0 | 11.39240506329114 |
| axon-messaging-5.1.0 | true | 4 | 24 | 40 | 100 | 75.45454545454547 | 25.302576660785586 | 80 | 4 | 9 | 6 | 2.449489742783178 | 4 | 30.37974683544304 | 43.43434343434344 | 38.69099510641513 | 6.067502826718603 | 37.9746835443038 |
| axon-messaging-5.1.0 | false | 4 | 26 | 40 | 100 | 75.22727272727273 | 26.632640136891368 | 70 | 2 | 10 | 6.5 | 3.3166247903554 | 7 | 11.39240506329114 | 28.09917355371901 | 21.568969325010755 | 7.598417511562199 | 20.202020202020204 |
| axon-modelling-5.1.0 | true | 1 | 4 | 36.36363636363637 | 36.36363636363637 | 36.36363636363637 | 0 | 36.36363636363637 | 4 | 4 | 4 | 0 | 4 | 10.743801652892563 | 10.743801652892563 | 10.743801652892563 | 0 | 10.743801652892563 |
| axon-modelling-5.1.0 | false | 1 | 2 | 18.181818181818183 | 18.181818181818183 | 18.181818181818183 | 0 | 18.181818181818183 | 2 | 2 | 2 | 0 | 2 | 3.3057851239669422 | 3.3057851239669422 | 3.3057851239669422 | 0 | 3.3057851239669422 |

[Full data](./InternalArtifactUsageSpreadPerDependency.csv)

### 7.2 Spread per Dependent (depends on most others)

| artifactName | dependencyTypeIsInterface | artifactDependencies | artifactDependencyPackages | dependentPackagesRate | minPackageSpread | maxPackageSpread | avgPackageSpread | stdPackageSpread | per5PackageSpread | minPackageCount | maxPackageCount | avgPackageCount | stdPackageCount | per5PackageCount | minTypeSpread | maxTypeSpread | avgTypeSpread | stdTypeSpread | per5TypeSpread |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| axon-conversion-5.1.0 | false | 1 | 2 | 80 | 80 | 80 | 80 | 0 | 80 | 4 | 4 | 4 | 0 | 4 | 19.51219512195122 | 19.51219512195122 | 19.51219512195122 | 0 | 19.51219512195122 |
| axon-conversion-5.1.0 | true | 1 | 1 | 80 | 80 | 80 | 80 | 0 | 80 | 4 | 4 | 4 | 0 | 4 | 21.95121951219512 | 21.95121951219512 | 21.95121951219512 | 0 | 21.95121951219512 |
| axon-eventsourcing-5.1.0 | true | 4 | 25 | 54.54545454545455 | 27.272727272727273 | 81.81818181818183 | 54.54545454545455 | 26.762911716144995 | 36.36363636363637 | 3 | 9 | 6 | 2.943920288775949 | 4 | 2.479338842975207 | 42.97520661157025 | 19.62809917355372 | 17.562388587127792 | 10.743801652892563 |
| axon-eventsourcing-5.1.0 | false | 3 | 15 | 60.60606060606061 | 18.181818181818183 | 90.90909090909092 | 60.60606060606061 | 37.848472717566054 | 72.72727272727273 | 2 | 10 | 6.666666666666667 | 4.163331998932265 | 8 | 3.3057851239669422 | 33.057851239669425 | 21.487603305785125 | 15.939918613211498 | 28.09917355371901 |
| axon-messaging-5.1.0 | false | 2 | 9 | 48.24561403508772 | 8.771929824561402 | 87.71929824561403 | 48.24561403508772 | 55.82421956735901 | 8.771929824561402 | 5 | 50 | 27.5 | 31.81980515339464 | 5 | 0.7886435331230284 | 33.91167192429022 | 17.350157728706623 | 23.42151798882886 | 0.7886435331230284 |
| axon-messaging-5.1.0 | true | 2 | 9 | 44.73684210526316 | 24.561403508771928 | 64.91228070175438 | 44.73684210526315 | 28.532378889983498 | 24.561403508771928 | 14 | 37 | 25.5 | 16.263455967290593 | 14 | 5.678233438485804 | 17.034700315457414 | 11.35646687697161 | 8.030234739027039 | 5.678233438485804 |
| axon-metrics-micrometer-5.1.0 | true | 1 | 1 | 66.66666666666667 | 66.66666666666667 | 66.66666666666667 | 66.66666666666667 | 0 | 66.66666666666667 | 2 | 2 | 2 | 0 | 2 | 15.789473684210527 | 15.789473684210527 | 15.789473684210527 | 0 | 15.789473684210527 |
| axon-modelling-5.1.0 | true | 2 | 14 | 100 | 100 | 100 | 100 | 0 | 100 | 7 | 7 | 7 | 0 | 7 | 30.303030303030305 | 43.43434343434344 | 36.86868686868687 | 9.285240561035476 | 30.303030303030305 |
| axon-modelling-5.1.0 | false | 2 | 9 | 92.85714285714286 | 85.71428571428572 | 100 | 92.85714285714286 | 10.101525445522102 | 85.71428571428572 | 6 | 7 | 6.5 | 0.7071067811865476 | 6 | 20.202020202020204 | 22.222222222222225 | 21.212121212121215 | 1.4284985478516117 | 20.202020202020204 |
| axon-server-connector-5.1.0 | true | 4 | 19 | 37.5 | 30 | 40 | 37.5 | 5.000000000000001 | 40 | 3 | 4 | 3.75 | 0.5 | 4 | 5.063291139240507 | 30.37974683544304 | 14.556962025316455 | 10.962346883347326 | 11.39240506329114 |

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
