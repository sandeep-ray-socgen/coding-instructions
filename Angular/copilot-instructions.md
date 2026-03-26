# Instructions

## Context
- Language: TypeScript (Angular 19)
- Framework / Libraries: Angular 19, RxJS 7.8+, NgRx optional
- Build Tool: Angular CLI
- Architecture: Feature-based modules with shared/core
- Coding Style: ESLint + Prettier, strict typing

## Overview
This repository follows Angular best practices with clear separation of concerns,
predictable state management, and testable components and services. Favor
readability and strong typing over cleverness.

## General Guidelines
- Prefer standalone components and `provide*` APIs unless project conventions require modules.
- Use strict types; avoid `any` and non-null assertions (`!`) unless justified.
- Prefer `readonly` and `const` whenever possible.
- Use `async` pipe and signals to avoid manual subscriptions.
- Handle errors explicitly; never swallow errors silently.
- Keep components thin; move logic into services or facades.

## Project Structure And Patterns
- `core/`: singleton services, interceptors, guards, app-wide providers
- `shared/`: reusable UI components, pipes, directives
- `features/`: feature modules or standalone feature routes
- `models/`: domain interfaces and types
- `services/`: API clients and domain services
- `state/`: NgRx or signals-based state

### Patterns To Follow
- Use container/presentational split for complex UIs.
- Favor `OnPush` change detection with immutable data.
- Prefer RxJS `pipe` operators over nested subscriptions.
- Use `takeUntilDestroyed()` or `DestroyRef` for subscription cleanup.
- Use `trackBy` in `*ngFor` for performance.

### Patterns To Avoid
- No business logic inside templates.
- No subscriptions in `ngOnInit` without cleanup.
- Avoid `setTimeout` for change detection hacks.
- Avoid direct DOM manipulation; use Renderer2 or CDK.
- Avoid reassigning inputs inside components.

## Error Handling
- Centralize API error handling in interceptors or services.
- Use typed error models and map them at the boundary.
- Show user-friendly messages; log technical details.

## Performance
- Use `OnPush` and immutable data structures.
- Use `trackBy` functions for lists.
- Prefer `defer`/lazy routes for large features.
- Avoid excessive change detection cycles and manual `detectChanges`.

## Security
- Sanitize HTML via Angular `DomSanitizer` only when needed.
- Never bind untrusted HTML directly.
- Keep secrets out of client code.

## Testing
- Unit tests: Jest or Karma + Jasmine
- Use `TestBed` with shallow setup where possible
- Mock services with spies or test doubles
- Cover:
  - Component input/output behavior
  - Service API calls and error paths
  - State selectors and reducers (if NgRx)

## Tooling
- Lint: ESLint with project rules
- Format: Prettier (run before commit)
- Typecheck: `ng build` or `tsc -p tsconfig.app.json`

## Contribution Guidelines
- Keep changes focused and small.
- Add tests when behavior changes.
- Update documentation for new patterns or APIs.
