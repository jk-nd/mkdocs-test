# NOUMENA Protocol Technology

## Introduction

## Overview

### The problem

Enterprise software development is way too expensive.

There are many recent improvements: shift left, cloud native development, microservices. But all still suffer from the
same problem. Programming languages have not kept up with the times.

Enterprise software has many requirements. Strong authorization guarantees. Strong privacy guarantees (reinforced by
GDPR, CCPA, FADP etc). Audit trails. Metrics. Integration with various frontends. Integration with various backends.

Traditionally solved by adding frameworks and layers, but those all rely on correct configuration and have associated
maintenance costs.

Once the software is running, it must be maintained as well. Outdated documentation. Overly complex implementations.

### The solution

NOUMENA is reinventing the way to develop enterprise software: NOUMENA Protocol Technology.

> The key idea is: pack the business data, the rules governing access to this data and the rules on how this data can be
> manipulated into one object: the NOUMENA Protocol.

> The NOUMENA Protocol securely binds together all the data, access and business rules (and only those) associated
> to any specific business process into an independently executable piece of software, a service. Every individual
> business process / event is associated with a unique and autonomous instance of such a service (or Protocol).

TODO blahblah user centric design.

## Architecture

### NOUMENA Protocol Language

NPL is a revolutionary programming language that includes [authorization as a first class citizen](authorization.md).
Based on the notion of [parties, permissions and obligations](Design_Philosophy.md) it provides an all-encompassing
approach to writing secure, modern enterprise applications.

NPL's explicit authorization-based modeling approach makes it a perfect fit for [domain driven design](ddd.md) to
naturally match business reality and code. Its inclusion of [finite state machines](fsm.md) provides a natural fit for
many business applications.

The structure of NPL programs also enables [automatically generated visualizations](visualization.md) that are much more
expressive than those derived from traditional programming languages. Such visualizations are invaluable when it comes
to software maintenance.

Finally, NPL is designed to be [transactional and deterministic](TransactionalDeterministicLanguage.md), TODO blahblah
advantage.

### NOUMENA Operating Engine

NPL is compiled to [bytecode](bytecode.md) and executed by the [NOUMENA Runtime](runtime.md) which is embedded in the
NOUMENA Operating Engine. Whereas the runtime merely takes care of the execution, the Operating Engine takes care of
everything around it, most notably [OIDC-based authorization](party_and_OIDC.md),
[straightforward data persistence](persistence.md).

Because of the explicit structure NPL provides, the Operating Engine can provide various features that are hard to
accomplish automatically in more traditional environments such
as [structured audit logging](audit.md), [partial independent verification](verification.md)
and [automated data anonymization](anonymization.md)

Finally, the Operating Engine takes care of the entire [application lifecycle management](migrations.md).

#### Deployment

Deployment -> package NPL and Operating Engine together as a Docker image. [Cloud-native deployment](cloud-native.md)

- horizontal scaling, metrics, kubernetes, ...

Requires a PostgreSQL database and an OIDC-compatible identity management system.

Alternative: PaaS

#### Systems integration

General: [streaming](reactive-applications.md), notifications [to an AMQP-compatible queue](amqp.md) or
notifications [for strongly authorized protocol-to-protocol communication](multinode.md)

For frontends: [automated REST APIs](npl_apis.md).

### NOUMENA Network

Single NPL applications are amazing, but connecting multiple applications is even better. Using NPL enables all kinds
of [discoverability](discoverability.md): allowing users to find their data, but also allowing system integrators to
discover the structure of data.

For applications that meet [certain constraints](verification.md#limitations), independent verification of calculations
can be offloaded to NOUMENA verifier nodes.

## Use cases

## Comparative analysis

## Future development

## References
