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

## Code organization
- **Transaction script** - Organize the business logic as a collection of procedural transaction scripts, one for each type of request.
- **Domain model** - Organize the business logic as an object model consisting of classes that have state and behavior.
- **Aggregate** - Organize a domain model as a collection of aggregates, each of which is a graph of objects that can be treated as a unit.
