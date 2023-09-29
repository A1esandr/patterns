# Microservices patterns

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
