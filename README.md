# Modyo Connect - Organization Repository

Este repositorio especial `.github` contiene la configuración a nivel de organización para Modyo Connect.

## Organization Profile

El directorio `profile/` contiene el README que se muestra en la [página de la organización](https://github.com/modyo-connect).

## Organization Templates

### modyo-labeler

Configuración para el workflow **labeler** que añade labels automáticamente según commits y PRs:

| Tipo | Label | Descripción |
|------|-------|-------------|
| `feat` | Features | Nueva funcionalidad |
| `fix` | Bug Fixes | Corrección de errores |
| `docs` | Documentation | Solo documentación |
| `refactor` | Code Refactoring | Cambio sin nueva funcionalidad |
| `perf` | Performance | Mejora de rendimiento |
| `test` | Tests | Añadir o corregir tests |
| `chore` | Chores | Mantenimiento |

### modyo-release-drafter

Configuración para **release drafter** que crea drafts de releases automáticamente al mergear a main.

## Repository Structure

```
.github/
├── .github/
│   ├── modyo-labeler.yml
│   └── modyo-release-drafter.yml
├── profile/
│   ├── README.md              # Organization profile
│   └── assets/
│       ├── logo-light.svg
│       └── logo-dark.svg
└── README.md
```

## Links

- **Guidelines**: [modyo-connect/.guidelines](https://github.com/modyo-connect/.guidelines)
- **BFF Template**: [modyo-connect/modyo-connect-bff-template](https://github.com/modyo-connect/modyo-connect-bff-template)
- **Widget Template**: [dynamic-framework/dynamic-react-base-template](https://github.com/dynamic-framework/dynamic-react-base-template)
- **Workflows**: [modyo-connect/workflows](https://github.com/modyo-connect/workflows)

---

**Modyo Connect** | Last updated: January 2025
