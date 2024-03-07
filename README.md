# Terraform Provider for SwaggerHub

The SwaggerHub provider allows [Terraform](https://terraform.io/) to  manage [SwaggerHub](https://app.swaggerhub.com) resources.

## Project Context

What is SwaggerHub?
> SwaggerHub is an online platform where you can design your APIs – be it public APIs, internal private APIs or microservices. The core principle behind SwaggerHub is Design First, Code Later. That is, you start by laying out your API, its resources, operations and data models, and once the design is complete you implement the business logic.

### Problem Statement
Even though SwaggerHub provides a roboust experience of designing APIs, it lacks proper capabilities to manage the APIs definitions in a "Infrastructure as a Code" (IaaC) way.

SwaggerHub offers a "Git Sync" integration, which allows for automatically synchronizing changes between Git repository and SwaggerHub. However, I personally found this feature very limited, as it requires manual synchronization, is prone to race conditions causing merge conflicts when many people co-develop the APIs at the same time. Moreover, the biggest shortcoming is lack of proper code-review experience, which is standard practice in IT industry.

The goal of this project is to create a Terraform Provider, which would allow to manage API specifications inside SwaggerHub, using Terraform Resources definitions, following tha IaaC approach.

## Project Scope
The following SwaggerHub resources/operations support will be implemented by the SwaggerHub Terraform Provider:

- [ ] APIs Management
  - [ ] Read
  - [ ] Write
  - [ ] Update
  - [ ] Delete
- [ ] Projects Management
  - [ ] Read
  - [ ] Write
  - [ ] Update
  - [ ] Delete
- [ ] Domains Management
  - [ ] Read
  - [ ] Write
  - [ ] Update
  - [ ] Delete
- [ ] Integrations Management
  - [ ] Read
  - [ ] Write
  - [ ] Update
  - [ ] Delete
- [ ] Templates Management
  - [ ] Read
  - [ ] Write
  - [ ] Update
  - [ ] Delete

Additional features:
- [ ] CI/CD Pipeline
  - [ ] Tests automation
  - [ ] [Terraform Provider docs generation](https://github.com/hashicorp/terraform-plugin-docs/)
  - [ ] Publishing the provider to Terraform Registry
- [ ] Generating models / client / server code based on the API spec and publishing it into 3rd party storage, e.g. S3, Azure Blob Storage, etc.
- [ ] Generating change logs for API definitions changes and publishing them into 3rd party storage
- [ ] Detecting breaking changes when doing API definition updates  

## Learning Resources
- https://developer.hashicorp.com/terraform/plugin/code-generation/specification (Terraform Plugin Framework SDK Reference)
- https://developer.hashicorp.com/terraform/plugin/code-generation/workflow-example
- https://developer.hashicorp.com/terraform/plugin/code-generation/framework-generator
- https://developer.hashicorp.com/terraform/plugin/code-generation/openapi-generator

Community providers:
- https://github.com/tdabasinskas/terraform-provider-backstage
- https://github.com/HenriquePiccolo/terraform-provider-grafana-v2

## License

This provider is distributed under the Mozilla Public License v2.0 license found in the [`LICENSE`](./LICENSE) file.
