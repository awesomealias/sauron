# Sauron

> WIP Hackathon Alpha!

Sauron is an open source system for managing security development CICD life cycles from code commit
through production by providing basic mechanisms for code/runtime analysis, vulnerability management
and risk scoring.

Sauron is:
* **minimal**: simple, easily accessible
* **portable**: public, private, hybrid
* **extensible**: pluggable, modular, hookable, composable

Sauron enables:
* programmatic initiation of security checks for scanning/compliance
* programmatic hooks to influence CICD with security risk information
* security trending over time

Sauron is NOT:
* a build system
* a code test coverage framework
* your typical vulnerability scanner

Concepts
--------

Sauron works with the following concepts:

[**Cluster/Architecture**](./docs/design/architecture.md)
: The cluster is a holistic idea of loosely coupled components that realize the 
Sauron service.

Clusters container the following components.

[**Api**](./docs/design/api.md)
: The API exposes access for agents as well as 3rd party integrations such as 
Jenkins or web hooks to perform CRUD actions on various [resources](./docs/user-guide/resources.md).

[**Node**](./docs/design/node.md)
: Any Docker enabled host that can launch an Agent.

[**Agent**](./docs/design/agent.md)
: The Agent sits on any Docker enabled host and provides the ability to execute various workflow
steps, such as Checkers, Notifiers, or Publishers

[**Checker**](./docs/design/checker.md)
:A Checker is an implementation of a scanner or validator plugin launched by an Agent against
a specified endpoint such as a URL or github repository. 

[**Notifier**](./docs/design/checker.md)
:A Notifier is an implementation of a notification plugin launched by an Agent to send status
to a 3rd party system.  This could be a simple notification of scan results or even an 
actionable alerting system.

[**Publisher**](./docs/design/publisher.md)
:A Publisher is an implementation of a publisher plugin launched by an Agent to publish content
to a 3rd party system or call a webhook. 


Documentation
-------------

Sauron documentation is broken out into the following categories

* **[Admin documentation](./docs/admin)**
 * for those wishing to create a Sauron cluster
* **[Design documentation and proposals](./docs/design)**
 * for those who want to understand the architecture and design
 * for those interested in feature proposals
* **[User documentation](./docs/user)**
 * for those wishing to build and integrate Sauron into existing CICD pipeline 
   components.
* **[Developer and API Documentation](../docs/developer)**
 * for those who wish to create Checker, Notifier, Publisher plugins

Community
---------
TBD

Contributing
------------
TBD

