# Changelog

All notable changes to this extension are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/)
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
Content is generated from commits ([Conventional Commits](https://www.conventionalcommits.org/)).

## [2.11.1] - 2026-11-22

### Bug Fixes

- **build:** `CHANGELOG.md` is now included in the published package, both in
  `files` and copied into `dist/`. Previously it shipped in the repository but
  was missing from the npm tarball.

## [2.11.0] - 2026-11-22

Adds a changelog to the release flow and tightens task reporting.

### Features

- **task:** Reports are now written to a dedicated task directory and follow a
  two-level tree, so nested work keeps its artifacts in one place.
- **task:** Task follow-ups and notifications now reflect the current task count
  and the responsible role.
- **todos:** Pending todos are only surfaced when they actually need attention,
  based on teammate status.
- **markdown:** Custom bullet markers (e.g. `-`, `*`, `+`) are preserved when
  formatting nested unordered lists.

### Bug Fixes

- **task:** Task completion no longer sends a stale teammate reference in notifications.
- **i18n:** Error messages for task nesting and artifact-name validation are clearer.

### Documentation

- The release flow now requires a `CHANGELOG.md` entry for every published version;
  `bun run changelog` drafts the entry and the publish workflow enforces it.

## [2.10.1] - 2026-11-19

### Tests

- **tools:** Remove normalize tool arguments test

### Chores

- **release:** Bump version to 2.10.1

## [2.10.0] - 2026-11-18

### Features

- **tools:** Normalize tool arguments before validation
- **teammates:** Log tool execution start before validation

### Chores

- **release:** Bump version to 2.10.0

## [2.9.0] - 2026-11-17

### Features

- **teammates:** Limit direct teammate spawns

### Bug Fixes

- **teammates:** Enforce direct limit in validator
- **teammates:** Enforce configured direct teammate limit

### Other

- Merge pull request #47 from aelinrezende/feat/teammate-limit

feat(teammates): limit direct teammate spawns
- Merge branch 'main' of https://github.com/aelinrezende/pipa-source

### Documentation

- **README:** Update teammate definition frontmatter fields and validation notes
- **teammates:** Translate limit configuration comment

### Tests

- **i18n:** Add locale parity check

### Chores

- **release:** Update dependencies for 2.9.0

## [2.8.0] - 2026-11-12

### Features

- **tools:** Add contextual follow-ups to responses
- **tools:** Refine next step suggestions

### Bug Fixes

- **tools:** Remove extra follow-up spacing
- **tools:** Isolate follow-up generation

### Other

- Merge pull request #46 from aelinrezende/feat/tool-response-follow-ups

feat(tools): add contextual follow-ups to responses

### Refactor

- **tools:** Compose follow-ups directly

### Chores

- **release:** Bump version to 2.8.0

## [2.7.11] - 2026-11-11

### Bug Fixes

- **tools:** Correct pause notices and trim responses

## [2.7.10] - 2026-11-11

### Bug Fixes

- **teammates:** Clarify idle options and chat response

### Refactor

- **reminders:** Remove unused constant MAX_NUDGES_WITHOUT_TOOL

## [2.7.9] - 2026-11-07

### Bug Fixes

- **reminders:** Improve escalation nudge with teammate chat payload

### Refactor

- **reminders:** Remove unused tool tracking and escalation logic from todo feature

### Chores

- **release:** Bump version to 2.7.9

## [2.7.8] - 2026-11-04

### Chores

- **release:** Bump version to 2.7.8

## [2.7.7] - 2026-11-03

### Bug Fixes

- **reminders:** Update error handling to fallback on event message error
- **teammate:** Increase MAX_IDLE_NUDGES to 3 and update nudge message format
- **task:** Prevent artifact overwrite on completion

### Other

- Merge pull request #45 from aelinrezende/fix/task-complete-artifact-collision

fix(task): prevent artifact overwrite on completion

### Documentation

- **tools:** Require shared artifact directory for related work

### Chores

- Add JSDoc
- **release:** Bump version to 2.7.7

## [2.7.6] - 2026-11-01

### Bug Fixes

- **tui:** Pad tree widgets
- **tui:** Remove trailing widget blank lines

### Other

- Merge pull request #44 from aelinrezende/feat/tui-widget-padding

fix(tui): pad tree widgets

### Refactor

- Apply formatting

### Chores

- **release:** Bump version to 2.7.6

## [2.7.5] - 2026-10-28

### Features

- **teammates:** Nudge agents with unfinished tasks

### Bug Fixes

- **hooks:** Remind agents of eligible pending tasks
- **teammates:** Clarify idle task reminders

### Other

- Merge pull request #41 from aelinrezende/feat/idle-agent-end

feat(teammates): nudge agents with unfinished tasks

### Refactor

- **reminders:** Centralize idle nudge prompts
- **task:** Centralize task reminder prompts

### Chores

- **release:** Bump version to 2.7.5

## [2.7.4] - 2026-10-28

### Features

- **task:** Allow supervisors to reopen tasks

### Other

- Merge pull request #40 from aelinrezende/feat/task-reopen-iGr6eaxv

feat(task): allow supervisors to reopen tasks

### Chores

- **release:** Bump version to 2.7.4

## [2.7.3] - 2026-10-27

### Features

- **tasks:** Replace squads with task hierarchy

### Bug Fixes

- **tasks:** Require explicit parent task relationships
- **teammates:** Require subtasks for distinct deliverables
- **teammate:** Update instructions for task setup and naming conventions
- **teammate:** Clarify role scope and bump version

### Other

- Merge pull request #39 from aelinrezende/feat/epic-spawn

feat(tasks): replace squads with task hierarchy
- Remove

### Refactor

- **task:** Move parent notifications to tooling
- **task:** Mix in parent notifications
- **task:** Extract parent notification helpers
- **task:** Simplify parent readiness notification
- **teammates:** Update desenvolvedora description

## [2.7.2] - 2026-10-27

### Bug Fixes

- **nudge:** Route teammate messages and bump version

## [2.7.1] - 2026-10-27

### Bug Fixes

- **permission:** Allow format command and bump version

## [2.7.0] - 2026-10-25

### Features

- **teammate:** Add command guidelines and update blocked commands

### Bug Fixes

- **build:** Add 'skills/infra-evolve' skill

### Chores

- **release:** Bump version to 2.7.0

## [2.6.1] - 2026-10-25

### Bug Fixes

- **teammate:** Update status from 'idle' to 'running' during session initialization

### Chores

- **release:** Bump version to 2.6.1

## [2.6.0] - 2026-10-25

### Features

- **teammates:** Gate reminders on real tool usage and escalate idle

### Bug Fixes

- **permission:** Remove main edit/write confirmation gate
- **interpolate:** Replace undefined values with placeholder [value]
- **interpolate:** Fix interpolation
- **teammate:** Update instantiate return type and optimize imports
- **interpolate:** Corrigir substituição de placeholders para retornar o valor correto
- **teammates:** Correct reminder text and drop unused activity field
- **todo:** Address pending reminder to the teammate in second person
- **todo:** Ask for multiple checklist steps in empty reminder

### Other

- Merge pull request #38 from aelinrezende/feat/reminders-incisivos

feat(teammates): gate reminders on real tool usage and escalate idle

### Documentation

- Add system profile

### Chores

- **release:** Bump version to 2.6.0

## [2.5.0] - 2026-10-23

### Features

- **tasks:** Persist completion opinions

### Bug Fixes

- **tasks:** Require completion output directory
- **tasks:** Validate completion artifact before writing
- **tools:** Require non-empty output directories

### Other

- Merge pull request #35 from aelinrezende/feat/task-complete-parecer

feat(tasks): persist completion opinions

### Refactor

- **prompts:** Inline completion report instruction

### Chores

- **release:** Bump version to 2.5.0

## [2.4.0] - 2026-10-22

### Features

- **task:** Replace claim with explicit start

### Other

- Merge pull request #34 from aelinrezende/feat/task-start-lifecycle

feat(task): replace claim with explicit start

### Chores

- **release:** Bump version to 2.4.0

## [2.3.8] - 2026-10-22

### Features

- **task:** Validate artifact paths and pause blockers

### Other

- Merge pull request #33 from aelinrezende/feat/subagent-execution-policy

feat(task): validate artifact paths and pause blockers

### Chores

- **release:** Bump version to 2.3.8

## [2.3.7] - 2026-10-22

### Features

- **i18n:** Add localized task and teammate messages

### Bug Fixes

- **teammate:** Increase stuck timeout to fifteen minutes

## [2.3.5] - 2026-10-19

### Bug Fixes

- **onboarding:** Inject prompt into agent system prompt
- **release:** Restore dependency ranges

### Chores

- **release:** V2.3.5

## [2.3.4] - 2026-10-19

### Bug Fixes

- **onboarding:** Resolve bundled templates directory at runtime
- **onboarding:** Require valid teammate frontmatter and validate generated files

### Other

- Merge pull request #32 from aelinrezende/fix/onboarding-templates-path

fix(onboarding): resolve bundled templates directory at runtime
- V2.3.4

## [2.3.3] - 2026-10-18

### Features

- Internationalize onboarding and document domain profiles
- Support onboarding without ask_user_question

### Reverts

- Keep onboarding prompt loader unchanged

### Other

- Merge pull request #31 from aelinrezende/docs/onboarding-and-profiles

feat: internationalize onboarding and document domain profiles

### Refactor

- Infer onboarding language from first message
- Remove locale-specific onboarding prompt

### Documentation

- Explain first-message language detection

### Chores

- Release v2.3.3

## [2.3.2] - 2026-10-18

### Other

- Merge pull request #30 from aelinrezende/docs/readme-and-npm-publish

docs: rewrite README and publish extension to npm

### Documentation

- Rewrite README and publish extension to npm

### Chores

- **release:** V2.3.2 and add repository field

## [2.3.1] - 2026-10-18

### Documentation

- **readme:** Clarify feature requirements and toast api

### Chores

- **release:** Bump version to 2.3.1

## [2.3.0] - 2026-10-18

### Features

- **i18n:** Add locale layer and migrate task feature
- **i18n:** Localize remaining feature definitions and widgets
- **teammate:** Define subagent behavior policy

### Bug Fixes

- **skills:** Align role ownership in plan, execute and finish flows
- **i18n:** Complete catalog coverage and fix paragraph punctuation
- **i18n:** Translate updatedAt field

### Other

- Merge pull request #28 from aelinrezende/feat/i18n-remaining-features

feat(i18n): localize remaining feature definitions and widgets
- Merge pull request #29 from aelinrezende/feat/subagent-policy

feat(teammate): define subagent behavior policy

### Style

- **teammate:** Collapse multi-line statements
- **teammate:** Add section titles and dividers to policy prompt

### Chores

- **release:** Bump version to 2.3.0

## [2.2.2] - 2026-10-18

### Bug Fixes

- **tools:** Render tool results as markdown in both states

### Chores

- **release:** Bump version to 2.2.2

## [2.2.1] - 2026-10-18

### Bug Fixes

- **tools:** Add renderResult to remaining features

### Chores

- **release:** Bump version to 2.2.1

## [2.2.0] - 2026-10-18

### Features

- **teammate:** Add force flag to dismiss with task cascade
- **tools:** Return structured tool results with rendered content

### Other

- Merge pull request #26 from aelinrezende/feat/desambiguar-papeis-teammates

Feat/desambiguar papeis teammates
- Merge pull request #27 from aelinrezende/feat/dismiss-force-cascade

feat(teammate): add force flag to dismiss with task cascade

### Refactor

- **teammates:** Desambiguate roles and add investigador
- **teammates:** Drop cross-role names from profile bodies

### Chores

- **release:** Bump version to 2.2.0

## [2.1.8] - 2026-10-17

### Features

- **task:** Compact session on terminal complete and pause
- **teammate:** Add compacting status and suppress spurious failure
- **config:** Add compactAfterTaskAction flag

### Other

- Merge pull request #25 from aelinrezende/feat/task-terminal-compact

feat(teammate): compact session on terminal actions with compacting status

### Documentation

- **readme:** Document missing config fields

### Style

- **teammate:** Remove explanatory comments from compacting changes

### Chores

- **release:** Bump version to 2.1.8

## [2.1.7] - 2026-10-09

### Features

- **task:** Add reopen reason support
- **task:** Merge reopen reason support

### Chores

- **release:** Bump version to 2.1.7

## [2.1.6] - 2026-10-08

### Features

- **teammates:** Show active thinking in tree

### Chores

- **release:** Bump version to 2.1.6

## [2.1.5] - 2026-10-07

### Bug Fixes

- **task:** Allow supervisors to reopen tasks
- **teammates:** Handle prompt rejection
- **task:** Notify owner when supervisor reopens task

### Documentation

- **task:** Clarify task tool operations

### Chores

- **release:** Bump version to 2.1.5

## [2.1.4] - 2026-10-06

### Bug Fixes

- **docs:** Persist new documents before emitting events

## [2.1.3] - 2026-10-06

### Bug Fixes

- **repository:** Return current repository items

## [2.1.2] - 2026-10-06

### Chores

- **release:** Prepare v2.1.2 package metadata

## [2.1.1] - 2026-10-05

### Features

- **core:** Export repositories from core index

### Chores

- **release:** Bump version to 2.1.1

## [2.1.0] - 2026-10-01

### Features

- **config:** Add persistMessages option for logging teammate messages

### Bug Fixes

- **teammate:** Update teammate tool behavior
- **dependencies:** Update package versions to latest stable releases
- **teammate:** Change dirs to a Set for unique directory handling
- **repository:** Optimize data retrieval by using cached values
- **apply-features:** Remove async modifier from applyFeatures function
- **task-repository:** Refactor getActiveTask to use findOneBy
- **tui-register:** Add UI context check in initialize method
- **teammate-repository:** Update persist logic to use pick for teammate properties

### Chores

- **tui:** Simplify widget registration
- **release:** Bump version to 2.1.0

## [2.0.6] - 2026-09-29

### Bug Fixes

- **core:** Forward session start payload

### Refactor

- **teammate:** Migrate from Hub to Tool term

## [2.0.5] - 2026-09-28

### Bug Fixes

- **teammates:** Register subagent before extension binding

## [2.0.4] - 2026-09-28

### Bug Fixes

- **tui:** Register task widget only in main session

## [2.0.3] - 2026-09-28

### Bug Fixes

- **core:** Preserve session getter during feature refresh

## [2.0.2] - 2026-09-28

### Bug Fixes

- **core:** Preserve session getter during API refresh

## [2.0.1] - 2026-09-28

### Bug Fixes

- **core:** Avoid merging the session getter

## [2.0.0] - 2026-09-28

### Other

- Merge pull request #23 from aelinrezende/feat/desacoplar-features-repository

refactor: decouple features from SDK via Repository pattern

### Refactor

- **core:** Decouple repository-backed features

### Chores

- **release:** Bump version to 2.0.0

## [1.3.0] - 2026-09-25

### Features

- **task:** Add pause and resume actions for active tasks

### Bug Fixes

- **task:** Remove orphan push call in guard collapseBlockedLoop

### Other

- Merge pull request #22 from aelinrezende/feat/task-pause-resume

feat(task): add pause and resume actions for active tasks

### Refactor

- **teammate:** Rename teammates to role-based names
- **skill:** Rename teammates to role-based names in plan and execute skills
- **task:** Drop dead dependent warning from pause handler

### Documentation

- **readme:** Translate READMEs to English and add npm badges

### Style

- **task:** Normalize line endings to LF in task feature files
- **task:** Use warning color and "pausada" label for stopped tasks

### Chores

- Add .gitattributes and normalize line endings
- **release:** Bump version to 1.3.0

## [1.2.0] - 2026-09-23

### Features

- **teammate:** Add optional thinking level to frontmatter

### Other

- Merge pull request #21 from aelinrezende/feat/teammate-thinking-level

feat(teammate): add optional thinking level to frontmatter

### Refactor

- **teammate:** Move thinking levels constant to constants

### Chores

- **release:** Bump version to 1.2.0

## [1.1.0] - 2026-09-23

### Features

- **task:** Add reopen action for completed tasks

### Other

- Merge pull request #20 from aelinrezende/feat/task-reopen

feat(task): action reopen — reabertura de tarefa concluída

### Chores

- **release:** Bump version to 1.1.0

## [1.0.9] - 2026-09-20

### Documentation

- **prompt:** Allow direct simple reads/writes for supervisor

### Chores

- **release:** Bump version to 1.0.9

## [1.0.8] - 2026-09-20

### Bug Fixes

- **sdk:** Migrate to pi-coding-agent 0.86.1 readonly systemPrompt

## [1.0.7] - 2026-09-20

### Bug Fixes

- **config:** Update default model and thinking level for consistency
- **task-guard:** Add termination response for stopped teammates
- **package:** Update version to 1.0.6 and add prompts section
- **custom-tools:** Add stopping teammate response

## [1.0.5] - 2026-09-20

### Bug Fixes

- **teammate-tui:** Stop rendering elapsed label when status is stopping

### Documentation

- **sdk:** Document npm install for pipa-core

### Chores

- **release:** Bump version to 1.0.5

## [1.0.4] - 2026-09-20

### Features

- **release:** Unify version source and publish all targets on tag

## [1.0.3] - 2026-09-20

### Chores

- **pipa-core:** Bump version to 1.0.3

## [1.0.2] - 2026-09-20

### Build

- **ci:** Migrate workflows from pnpm to bun

## [1.0.1] - 2026-09-20

### Features

- Bootstrap Pipa project framework with task management, Teammate agent system, and CLI utilities
- Altera para lodash-es para lodash
- Add system prompt tool injection for custom features
- Implement teammate frontmatter management and path resolution utilities
- Add skills configuration path to package.json
- Implement deferred event handling and teammate execution context orchestration
- Add ponytail extension and register additional Claude models to pipa configuration
- Add claude-sonnet, claude-haiku, and claude-opus to concurrentlyModels configuration
- Add @juicesharp/rpiv-ask-user-question to pi extensions
- Implement add SYSTEM_PIPA.md system prompt definition
- **pipa:** Implement native toast notifications on agent finish
- **pipa/toast:** Prevent duplicate concurrent toasts
- **pipa:** Implement todo tool feature for agent self-planning
- Increment counter state for manage-backlog skill
- Add build script and github action to automate minified releases
- Copy assets folders to dist during build
- Include prompts directory in release bundle
- Include prompts directory with gitkeep and restore build logic
- **pipa:** Add support for merging external user configuration
- **pipa:** Add todo count to teammate TUI and fix config array merge
- **teammate:** Send pending todos nudge on agent end
- **teammates:** Expand Stephanie prompt with diff and docs requirements
- **TeammateTreeWidget:** Update todo label in TUI
- **todo:** Extract TodoReminders and prompt creation on start
- **guard:** Allow 'todo' tool without active task
- **skills:** Flexibiliza coleta de brief na skill nova-tarefa usando contexto
- **teammate:** Descentraliza orquestracao e utiliza contexto no frontmatter
- **skills:** Add package manager detection and run command generation to task-finish
- **squad:** Squad auto-organizada no task manager
- **teammate:** Incluir task em setup como ativa e reorganizar imports
- **permission:** Bloqueia criação de tarefas pelo supervisor
- **state:** Inclui tarefas em setup como ativas em listActive e hasActiveTask
- **tui:** Tag squad, truncamento de nome e descrição aprimorada
- **spawn:** Squad reflection prompt for agents without squad
- **task:** Auto-link squad task to parent epic on create
- **pipa:** Improve squad prompt
- **task:** Altera status da tarefa pai e bloqueia conclusão com subtarefas pendentes
- **teammate:** Adiciona orientacao de reuso de squads ao instanciar agente
- **teammate:** Recomenda criação de squad para tarefas de múltiplos colegas
- **pipa:** Torna Pipa agnóstica a código com onboarding e templates
- **onboarding:** IsOnboarding agora busca no root da extensão para injetar PROFILE.md
- Implement onboarding logic and project path discovery utilities
- Adiciona colegas (giulia, ella, maria) e skills (plan, execute, finish); exclui arquivos dev-only do build via excludeFromBuild
- Validadores lançam PipaException em vez de retornar {success:false}
- Rename task-manager tool to task
- Implementa backlog tool — persistência gray-matter, parâmetros diretos, busca fuzzy, guard
- Adiciona cache em memória e leitura de arquivos markdown no backlog
- Adiciona validação de path duplicado e bloqueio de find no backlog
- Adiciona feedback dinâmico nas ações do backlog e trata nudges sem conteúdo
- **backlog:** Migrate storage to JSON and drop path field
- **backlog:** Propaga status do pai ao criar/atualizar item
- **backlog:** Adiciona action remove restrita a main com confirmacao
- **teammates:** Adiciona agents edu (QA) e filipe (produto)
- **todo:** Suprime nudge todo.pending com subordinado ativo
- **tools:** Renomeia actions de criação para instantiate e simplifica retornos
- **task:** Remove campo de competencia (self-only) e restringe force ao main
- **task:** Grava role do criador na Task e remove linha obsoleta do SYSTEM_AGENTS
- **task:** Hidrata TaskState a partir de tasks.json no constructor do TaskHub
- **task:** Hidrata TaskState via constructor (padrão BacklogState)
- **stores:** Load stores from disk on session boot
- Adiciona build e publicação do SDK pipa-core
- Adiciona geração de tipagem TypeScript ao build do pipa-core
- Exporta applyFeatures para simplificar registro de features no SDK
- Implementa nova DocsFeature para gerenciamento de base de conhecimento via Agente
- **docs:** Add body to search keys
- **core:** Eventos de dominio tipados (DomainEventMap) com roteamento via EventBus
- **docs:** Adiciona parentCode e publish hierárquico
- **docs:** Add update-metadata action to docs tool
- **docs:** Add required summary and lean list projection
- Suggest teammate dismiss on task completion nudge
- **teammates:** Add lore git/repo engineer
- **teammates:** Require reason on dismiss and guide completion nudge
- **core:** Emit domain events across feature hubs
- **task:** Add ReminderCleaner to prune redundant nudges
- Refactor updateBody methods to use updateText utility for better text handling
- **compactor:** Implement periodic micro-compact for old tool results
- **teammates:** Dismiss teammates asynchronously
- **pipa-core:** Publish to npm via OIDC trusted publishing

### Bug Fixes

- **tsconfig:** Set target to es2022 to fix Map iterator compilation error
- **teammate:** Wrap fs.readFileSync in try/catch to avoid ENOENT crashes when loading teammates
- **teammate:** Use paths helpers and safely read SYSTEM_AGENTS.md to prevent ENOENT crash
- **pipa:** Render todo list results to subagent via nudge
- Specify pnpm version in workflow
- Use import type for extension types to prevent runtime require
- Remove dependencies from published package.json to prevent redundant installation
- Restore assets copy logic after revert
- Use fs.cp instead of shell cp to copy assets
- Resolve path correctly in minified bundle
- Externalize libraries with native binaries and retain their dependencies
- **pipa:** Properly parse all frontmatter fields and update teammates docs
- **tsconfig:** Correct paths alias for pi-coding-agent types
- **TaskTreeWidget:** Update shortcut visibility logic
- **reminders:** Clear todo state when no pending items remain
- **skills:** Atualiza caminho do PROJECT-REFERENCE.md
- **teammate:** Instanciacao do Teammate com propriedade frontmatter correta
- **core:** Enforce hierarchical delegation to prevent main agent micromanagement
- **tui:** Show most recent completed task at top
- **pipa:** Pass constructor arguments to super() in mixin hubs
- **pipa:** Fix typescript type error by passing only pipa to super
- **pipa:** Change blocked task-manager command from create to instantiate
- **task:** Resolve array vazio no schema de roles
- **onboarding:** Alinha geração de skills (plan, execute, finish) com o plano de implementação
- **templates:** Reescreve arquivos com cópia verbatim do plano de implementação
- **onboarding:** Check parent directories for .pi and PROFILE.md
- Normaliza \n literal em newlines reais no updateBody
- BacklogHub.instantiate cria novo BacklogItem internamente (review #9)
- MkdirSync em vez de ensureDirSync
- Fse.writeFileSync já cria diretório
- **todo:** Suprime task.reminder e teammates.idle com subordinado ativo
- **tools:** Resolve review comments do PR #12
- **tools:** Instantiate retorna dado real como BacklogHub e remove parametros nao usados
- **tools:** Resolve review comments PR #12 (remove PipaHub, tipa params, simplifica update)
- **tools:** Get lança PipaException e clear do todo vira void
- **task:** Descricao do force no complete e ajusta SYSTEM_AGENTS apos review
- **task:** Fallback por nome do teammate em elegibilidade (role) quando criador offline
- **task:** CanComplete exibe orientação de force só p/ main e valida ownership antes de subtarefas
- **task:** CanClaim usa fallback isEligibleForTask (criador offline -> role)
- **task:** Guard keyBy owner in reminders to avoid crash on ownerless épicos
- **task-tree:** Remove branch prefix from overflow labels
- Corrige caminhos relativos gerados no index.d.ts do pipa-core
- Mantém todas as dependências no SDK publicado para suportar a tipagem TypeScript
- **docs:** Add DocsFeature to internal index.ts registry
- **docs:** Publish com url fixa, retorno { path, url } e serve em background
- **core:** Persiste task do spawn no disco (regressao load stores)
- **core:** Hydrate domain event features
- **teammate:** Remove redundant task persist on spawn
- **task:** Use string-path predicates in syncParentStatus
- **task:** Only collapse duplicate reminders, keep tool-result nudges
- **core:** Flatten PipaException message formatting
- **pipa:** Encode compacted tool result filenames
- **teammates:** Simplify dismissal lifecycle
- **teammate:** Suppress reminders during shutdown
- **teammate-tui:** Hide elapsed duration for stopping status
- **docs:** Correct artifacts path from .pi/artifacts to .artifacts
- **teammate-tui:** Use isStopping getter in elapsed label

### Reverts

- **core:** Remove references section

### Other

- Merge pull request #4 from aelinrezende/feature/squad-task-manager

feat(squad): squad auto-organizada no task manager
- Merge pull request #5 from aelinrezende/feature/tag-squad-truncamento-tui

feat(tui): tag squad, truncamento de nome e descrição aprimorada
- Merge pull request #6 from aelinrezende/feature/auto-link-squad-no-create

feat(task): auto-link squad task to parent epic on create
- Merge pull request #7 from aelinrezende/feature/generic-agent

feat(pipa): Pipa genérica, onboarding e templates
- Chat vira padrao, inbox vira excecao
- MaxVisible conta subtasks no total de linhas
- Altera bloqueio de task-manager: instantiate → create
- Merge pull request #8 from aelinrezende/feat/rename-task-tool

feat: rename task-manager tool to task
- Merge pull request #9 from aelinrezende/feat/backlog-tool

feat: backlog tool — gray-matter persistence, direct params, fuzzy search, guard
- Merge pull request #10 from aelinrezende/backlog-actions

refactor: unifica types do backlog e centraliza dispatch de ações
- Merge pull request #11 from aelinrezende/feat/todo-pending-reminder

feat(todo): suprime nudge todo.pending com subordinado ativo
- Merge pull request #12 from aelinrezende/feat/refactor-tools-padrao-backlog

refactor(tools): unifica task/todo/teammate no padrão backlog
- Merge pull request #13 from aelinrezende/feature/evolucao-tool-task

feat(task): self-only e force restrito ao main
- Merge pull request #14 from aelinrezende/feature/eventos-dominio

feat(core): eventos de dominio tipados (DomainEventMap) com roteamento via EventBus
- Merge pull request #15 from aelinrezende/feature/docs-hierarquia

feat(docs): parentCode e publish hierárquico
- Merge pull request #16 from aelinrezende/feature/reminders-cleaner

feat(task): ReminderCleaner — prune redundant nudges from LLM context
- Merge pull request #17 from aelinrezende/fix/reminders-cleaner-solo-colapso

fix(task): only collapse duplicate reminders, keep tool-result nudges
- Merge pull request #18 from aelinrezende/feat/async-teammate-dismissal

feat(teammates): dismiss teammates asynchronously
- Fix typo in teammate status translation for 'stopping'
- Merge pull request #19 from aelinrezende/fix/prevent-reminders-on-teammate-shutdown

fix(teammate): suppress reminders during shutdown

### Refactor

- Move npm packages from extensions to dedicated packages configuration in pi settings
- **pipa/toast:** Update toast messages and formatting
- Use find-up to dynamically discover package root
- **SessionIntervalRegistry:** Change Map for Set
- **llm:** Extract and improve toHumanReadable logic for LLM prompts
- **TaskManager:** List only teammate own tasks
- **TaskManager:** Simplify state persistence
- **skills:** Update nova-tarefa skill
- **teammate:** Refina formatacao do texto de colaboracao no system prompt
- **skills:** Replace copilot with thiago for PR reviews and remove auto-merge in task-finish
- **skills:** Decouple manage-backlog and manage-docs from justfile by invoking bash scripts directly
- **pipa:** Migrar arquitetura de Manager para Hub com Mixins Core
- **pipa:** Remove unused intercom feature and cross-cutting module
- **pipa:** Merge permission checks and rename subagent to colega
- **pipa:** Modularize permission feature
- **onboarding:** Move auto-inject logic to utils
- **paths:** Deduplicate file lookup logic
- Validadores usam spread de NUDGE.failed em vez de .code
- PipaException aceita spread de strings e ajusta formatação
- Create recebe p direto em vez de mapear campos manualmente
- BacklogHub.instantiate segue padrão TaskHub — lógica de criação no Hub, demais no Core
- Export * em hub/index.ts
- Usa spread do payload no instantiate
- BacklogItemFrontmatter type com Pick, Remove Record<string, unknown>
- Troca fs nativo por fs-extra (padrão lib/file.ts)
- Actions recebem p diretamente
- Substitui cache em disco por store em memória no backlog
- Unifica types do backlog e centraliza dispatch de ações
- Extrai types do backlog para entidade e unifica tipos de params
- **tools:** Unifica task/todo/teammate no padrao backlog (setToolActions + details real)
- **task:** Mensagens do canComplete via lista + filter(Boolean) (review)
- **task:** TaskHub usa Mixin(TaskCore, TaskSquad) (sem TaskValidator/TaskState duplicados)
- Apply project best practices and use fs-extra in DocsFeature
- **core:** Ajustes review PR #14
- **docs:** Extrai mensagens de erro para constantes
- **docs:** Move helpers de path para lib/doc.ts
- **task:** Centraliza persistência no TaskState e remove persist do TaskCore
- **features:** Torna métodos de carregamento públicos e adiciona comando "docs-publish"
- **backlog:** Centraliza persistência no BacklogState e remove persist do core
- **task:** Move ReminderCleaner to dedicated feature
- **task:** Split ReminderCleaner types and helpers into layers
- **teammate:** Centralize stopping state check

### Documentation

- Rewrite README to include new features and manual dependencies
- **pipa:** Mention custom teammates loading from user workspace
- **pipa:** Improve formatting and clarify teammate loading behavior
- **README:** Add mermaid to describe flow
- **teammates:** Add explicit instructions to invoke colleagues
- **pipa:** Add short JSDocs to core hub mixins
- **squad:** Add item 5 about squads in workflow section of SYSTEM_PIPA.md
- **core:** Readme do SDK pipa-core + copia no build
- **tools:** Improve descriptions, params and discoverability for pipa tools
- **skills:** Add cleanup step to plan, execute and finish skills
- **teammates:** Enforce english conventional commit standard for lore
- **teammates:** Declare ownership boundaries for ella lore maria giulia
- **core:** Remove stale references section
- **core:** Restore references section
- **core:** Rebuild package README

### Tests

- **ci:** Linha em branco em edu.md para testar filtro paths
- **core:** Regressao E4 eventos de dominio (tool -> hub -> emit -> handler)
- **core:** Remove testes de regressao E4 (decisao do usuario)

### Style

- Rename variable and formatting in build-ext.ts
- Apply prettier formatting to squad files
- **teammate:** Reorganiza imports e remove ícone ativo para idle
- Apply prettier formatting
- Prettier auto-format
- Aplica CODE-STANDARDS.md — chaves em if, blank lines, tipagem explícita
- **tools:** Desestrutura payload direto no parametro dos hubs
- **teammate:** Address review comments

### Build

- Add root package.json for Pi Git installation
- Consolidate pipa dependencies into root package.json

### CI

- Inherit commit message from main branch trigger
- Deploy to external public repository
- Fix commit message leaking private repository name

### Chores

- **TaskTreeWidget:** Atualiza label de tarefas
- Make release workflow run automatically on push
- Improve code legibility
- Improve code legibility
- **TeammateExchange:** Simply user nudge message on new message
- Format code
- Update pnpm-lock.yaml dependencies and remove obsolete lockfile entry
- **pipa:** Refactor toast trigger on nudge
- **teammates:** Simplify frontmatter
- **teammates:** Update descriptions
- **PermissionFeature:** Add "todo" to main's block list
- **TodoReminders:** Improve nudge about pending and missing todos
- **ci:** Remove force_orphan to keep commit history on release branch
- Migrate to new ModelRuntime pattern from v0.80.8
- Update project dependencies to version 0.80.10
- **TeammateHub:** Remove unused imports
- **bunfig:** Add bun configuration for faster installs
- **OnboardingFeature:** Inject onboarding in prompt
- Sincroniza mudanças pendentes
- Remove artifacts do tracking (devem ficar no .gitignore)
- Remove scripts temporários
- Remove create do BacklogCore (criação só no Hub)
- Formata código com prettier
- Formata código com prettier
- **ci:** Filtra release de agents locais e usa glob no build
- **task:** Remove scripts/test-task.ts do PR (review)
- **task:** Ajusta JSDoc do role e remove abreviação no filter (review)
- Remove artefatos de build do versionamento (d.ts residuais e dist-core)
- Remove .d.ts residuais do source (gerados por engano, idênticos ao dist-core)
- Remove dist-core do versionamento (regenerado no CI)
- **docs:** Remove script de teste
- **core:** Completa barrel de exports de lib
- Atualizar dependências
- Enable pi-web-access npm extension
- Drop generated pipa.config.d.ts from tracking
- **ReminderCleaner:** Rename hook
- Remove ProjectSearchFeature and SecureExecutor implementations
- Apply code formatting
- Update dependencies and change default settings

---
*Generated by `git-cliff` from the repository history.*
