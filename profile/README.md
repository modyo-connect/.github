<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://docs.modyo.com/assets/img/modyo-logo-light.png">
  <source media="(prefers-color-scheme: light)" srcset="https://docs.modyo.com/assets/img/modyo-logo.png">
  <img alt="Modyo Logo" src="https://docs.modyo.com/assets/img/modyo-logo.png" width="200">
</picture>

# Modyo Connect

**Secure cloud infrastructure for enterprise digital experiences.**

Modyo Connect provides a managed layer of integration APIs and microservices on AWS, enabling organizations to securely connect business systems with [Modyo](https://www.modyo.com)-powered applications.

## What We Build

| Type | Description | Stack |
|------|-------------|-------|
| **Micro Frontends** | Widgets deployed on Modyo Platform | React 18, TypeScript, Dynamic Framework |
| **BFF Services** | Backend for Frontend APIs | Java 21, Spring Boot 3.5 |
| **Shared Libraries** | Reusable components and utilities | Published to GitHub Packages |

## Platform Capabilities

- **API Gateway** — Managed entry point for all services
- **Container Orchestration** — ECS-based microservices deployment
- **Security** — WAF, TLS certificates, OAuth2/OIDC integration
- **DevOps** — Blue/green deployments, centralized logging, real-time monitoring
- **Quality** — SonarCloud analysis, automated testing, code review standards

## Development Standards

Our repositories follow consistent patterns and conventions documented in [`.github/.guidelines`](https://github.com/modyo-connect/.github/tree/main/.guidelines), automatically distributed across all projects.

## Resources

- [Modyo Connect Documentation](https://docs.modyo.com/es/connect/)
- [Modyo Platform](https://www.modyo.com)
- [Dynamic Framework](https://dynamicframework.dev)

---

<sub>Operated by Modyo's Site Reliability Engineers with high availability infrastructure on AWS.</sub>
