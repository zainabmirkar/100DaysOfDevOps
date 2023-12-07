# Decoupled and Event Driven Architecture

- Monolithic: if a change is made in the backend it could disrupt frontend because they are tightly coupled.
- Decoupled: where you build components which are independent of each other.
- event driven: closely relate and interract with decoupled aechitecture. they are triggered by events within the infrastructure
  - producer: element in the infra which will push an event to an event router
  - event router: processes the event and takes the necessary action in pushing the outcome to the users. eg: amazon sns, lambda and aws kinesis
  - consumer executes the action as requested 
