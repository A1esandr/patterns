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
