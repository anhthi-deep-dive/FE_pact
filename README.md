# What is Contract Testing?

Contract testing is a technique `for testing an integration point` by `checking each application in isolation` to ensure the `messages it sends or receives conform to a shared understanding` that is documented in a "contract".

Pros

- Test a single integration at a time - without having to deploy
- No dedicated test environment - run on a dev machine
- Get fast, reliable feedback
- Tests that scale linearly
- Deploy services independently

Const

- The contract must be defined before development
- All consumers must strictly follow the contract

# What is Pact?

Pact is a code-first tool for `testing HTTP and message integrations` using contract tests. Contract tests assert that `inter-application messages conform to a shared understanding` that is documented in a contract.

Pact allows you to safely `confirm that your applications will work together without having to deploy` the world first

Use cases:

- Javascript web integration(e.g React)
- Native mobile applications
- RESTFul microservices with JSON and XML
- Asynchronous messaging (e.g MQ)

# How Pact works?

Remember these definitions from the introduction

- **Consumer**: An application that `makes use of the functionality or data from another application` to do its job

- **Provider**: An application (often called a service) that `provides functionality or data for other applications to use`, often via an API

A contract between a consumer and provider is called a pact. Each pact is a collection of interactions. Each interaction describes

For HTTP

- An expected request - describing `what the consumer is expected to send to the provider`
- A minimal expected response - describing `the parts of the response the consumer wants the provider to return`
