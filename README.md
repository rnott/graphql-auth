# graphql-auth
Policy based authorization for GraphQL services.

Initially, this is a personal project to teach myself:
* GraphQL
* Golang
* OPA

Overtime, I expect this project to become production quality, as it is something I believe would be valuable to have for production use with enterprise and multi-tenat GraphQL based data services.

## Goal:
Intercept GraphQL requests/responses and apply fine-grained access control policies (via OPA) to:

* Filter input arguments before execution
* Filter response data after execution
* Enforce ABAC/RBAC using OPA (Open Policy Agent) policies
* Deployable as a sidecar for API gateways or GraphQL services

## Key Components

1. GraphQL Proxy / Filter Layer
This sits between clients and the real GraphQL service. It:

* Parses and validates GraphQL queries
* Applies input policy checks
* Proxies to backend GraphQL service
* Applies output filtering based on response structure

2. OPA Policies
3. Sidecar Deployment

## Desired Features
* Actions
  * ALLOW
  * DENY
    * Erase
    * Fail
* JSON Web Tokens
  * Attributes
  * Roles
* Policies
  * Registry
  * WASM
* Auditing
* Metrics (OTEL)
