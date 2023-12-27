# Microservice patterns

## Decomposition
- Decompose by business capability
- Decompose by subdomain

## Reliability
- circuit breaker
- rate limiter

## Communication
- Remote procedure invocation
- API gateway
- Service discovery

## Networking
- Self registration
- Client-side discovery
- **3rd party registration** - Service instances are automatically registered with the service registry by a third party.
- **Server-side discovery** - A client makes a request to a router, which is responsible for service discovery.

## Data
- **Transactional outbox** - Publish an event or message as part of a database transaction by saving it in an OUTBOX in the database.
- **Polling publisher** - Publish messages by polling the outbox in the database.
- **Transaction log tailing** - Publish changes made to the database by tailing the transaction log.
- **Saga** - Maintain data consistency across services using a sequence of local transactions that are coordinated using asynchronous messaging.
- **Event sourcing** - Persist an aggregate as a sequence of domain events that represent state changes.
- **API composition** - Implement a query that retrieves data from several services by querying each service via its API and combining the results.
- **Command query responsibility segregation** - Implement a query that needs data from several services by using events to maintain a read-only view that replicates data from the services.

## Code organization
- **Transaction script** - Organize the business logic as a collection of procedural transaction scripts, one for each type of request.
- **Domain model** - Organize the business logic as an object model consisting of classes that have state and behavior.
- **Aggregate** - Organize a domain model as a collection of aggregates, each of which is a graph of objects that can be treated as a unit.
- **Domain event** - An aggregate publishes a domain event when it’s created or undergoes some other significant change.
- **API gateway** - Implement a service that’s the entry point into the microservices-based application from external API clients.
- **Backends for frontends** - Implement a separate API gateway for each type of client.
