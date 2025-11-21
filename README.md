# Modyo Connect - Organization Repository

Este repositorio especial `.github` sirve como **fuente central de configuración** para toda la organización Modyo Connect.

## .guidelines - Development Standards

El directorio `.guidelines/` contiene los estándares de desarrollo que se distribuyen automáticamente a todos los proyectos de la organización.

```
.guidelines/
├── content/                    # Contenido IA-agnóstico
│   ├── backend/               # Java/Spring Boot BFFs
│   │   ├── agents/            # java-architect, bff-scaffolder
│   │   ├── commands/          # /create-bff
│   │   └── prompts/           # api-review, error-handling
│   ├── frontend/              # React/TypeScript Widgets
│   │   ├── agents/            # modyo-widget-expert
│   │   ├── commands/          # /create-widget
│   │   └── prompts/           # component-review, accessibility
│   └── shared/                # Común a ambos
│       ├── agents/            # github-admin, sonarcloud-admin
│       ├── commands/          # /review-pr
│       └── prompts/           # pr-description, commit-message
├── references/                 # Documentación técnica detallada
│   ├── backend/               # architecture, api-design, testing, etc.
│   ├── frontend/              # react-patterns, widget-structure
│   └── shared/                # github-workflows, docker
├── validation/                 # Reglas de validación (fail build)
│   ├── backend/               # ArchUnit, Checkstyle
│   └── frontend/              # ESLint
├── sync-config.yml            # Configuración de transformaciones
└── sync.sh                    # Script de sincronización
```

### Sincronización Automática

El workflow `sync-guidelines.yml` distribuye los estándares a todos los repositorios:

- **Trigger**: Push a main, cron semanal (Lunes 8am UTC), o manual
- **Proceso**: Transforma contenido IA-agnóstico a formatos específicos
- **Output**: Crea PRs en cada repositorio con los cambios

#### Formatos generados por proyecto:

| Herramienta | Ubicación | Descripción |
|-------------|-----------|-------------|
| Claude Code | `.claude/` | Agents, commands, prompts con frontmatter |
| GitHub Copilot | `.github/copilot-instructions.md` | Instructions compiladas |
| Cursor | `.cursor/rules/` | Rules por tipo (backend/frontend) |
| Genérico | `CONVENTIONS.md` | Para cualquier otra IA |

### Uso Local

```bash
# Sincronizar a un proyecto local
.guidelines/sync.sh sync /path/to/project

# Detectar tipo de proyecto
.guidelines/sync.sh detect /path/to/project
```

## Templates de Organización

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

## Estructura del Repositorio

```
.github/
├── .guidelines/           # Estándares de desarrollo (ver arriba)
├── workflows/
│   └── sync-guidelines.yml
├── .github/
│   ├── modyo-labeler.yml
│   └── modyo-release-drafter.yml
└── README.md
```

## Links Útiles

- **BFF Template**: [modyo-connect-bff-template](https://github.com/modyo-connect/modyo-connect-bff-template)
- **Widget Template**: [dynamic-react-base-template](https://github.com/dynamic-framework/dynamic-react-base-template)
- **Workflows**: [modyo-connect/workflows](https://github.com/modyo-connect/workflows)
- **SonarCloud**: [modyo-connect organization](https://sonarcloud.io/organizations/modyo-connect)

## Contribuir

Los cambios a `.guidelines/` se propagan automáticamente a todos los repositorios. Para modificar estándares:

1. Crea un branch desde `main`
2. Modifica archivos en `.guidelines/`
3. Crea PR y solicita review
4. Al mergear, el workflow creará PRs en los repositorios afectados

---

**Modyo Connect** | Last updated: January 2025
