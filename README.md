# The .github repository

GitHub has many special repositories.

You might already be familiar with the `.github` directory in a repository. It houses workflows, templates, configurations, and some other files specific to a project.

But another special repository you can create is the `.github` repository. It acts as a fallback for all of your repositories that don't have an actual `.github` directory with configurations,  templates and other community health files.

Just note that the files inside a repository's `.github` directory will be chosen over the ones in the `.github` directory. For example, if my new-project repo has a `.github` directory with a  template inside, that will be used instead of the generic feature request template from the `.github` repo.

# The .github repository for an organization account

The `.github` repository on an organization account works just like the `.github` repository on a personal account – except there is one difference.

Organizations can also have profile READMEs that show up on the organization page on GitHub. This README resides on the /profile directory of the organization's `.github` repository.

# Templates

### modyo-labeler

Used by **labeler**'s workflow, to add proper labels into pull request according to specific text found in commits, branches or pull requests. 

| Commit Type | Title                    | Description                                                                                                 |
| ----------- | ------------------------ | ----------------------------------------------------------------------------------------------------------- |
| `feat`      | Features                 | A new feature                                                                                               |
| `fix`       | Bug Fixes                | A bug Fix                                                                                                   |
| `docs`      | Documentation            | Documentation only changes                                                                                  |
| `style`     | Styles                   | Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)      |
| `refactor`  | Code Refactoring         | A code change that neither fixes a bug nor adds a feature                                                   |
| `perf`      | Performance Improvements | A code change that improves performance                                                                     |
| `test`      | Tests                    | Adding missing tests or correcting existing tests                                                           |
| `build`     | Builds                   | Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)         |
| `ci`        | Continuous Integrations  | Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs) |
| `chore`     | Chores                   | Other changes that don't modify src or test files                                                           |
| `revert`    | Reverts                  | Reverts a previous commit                                                                                   |

### modyo-release-drafter

Used by **release drafter**'s workflow, to create or update a draft release after a merge into master/main branch.
