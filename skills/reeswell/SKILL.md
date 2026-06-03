---
name: reeswell
description: Reeswell JavaScript and TypeScript coding conventions. Use when editing, reviewing, refactoring, or generating frontend, backend, or full-stack JavaScript or TypeScript code, especially when the user asks for Reeswell preferences, simple maintainable structure, immutable state updates, focused file organization, or stronger TypeScript typing.
metadata:
  author: reeswell
  version: "2026.06.03"
---

Project conventions, framework requirements, and explicit user instructions take
precedence over this skill.

## Core Principles

- Prefer the simplest solution that actually works.
- Avoid premature optimization and speculative abstractions.
- Optimize for clarity over cleverness.
- Extract repeated logic into shared functions or utilities when repetition is
  real.
- Do not build features, options, or abstractions before they are needed.

## Immutability

Prefer immutable updates for shared application state, props, inputs, and
API-derived data:

- Return a new copy with the change instead of modifying the original in place.
- Allow local mutation when it is scoped, framework-idiomatic, or clearer.
- Treat immutable data as the default for avoiding hidden side effects,
  improving debugging, and supporting safe concurrency.

## File Organization

- Give each source file a clear, focused responsibility.
- Split files that grow too large or take on too many concerns.
- Keep small local types near usage.
- Move exported, shared, or complex types to `types.ts` or `types/*.ts`.
- Move meaningful shared constants to `constants.ts`.
- Prefer feature or domain organization over file-type organization.
- Prefer many cohesive small files over a few large files.
- Treat 200 to 400 lines as typical and 800 lines as a ceiling unless there is
  a clear reason.

## TypeScript

- Declare explicit return types when feasible.
- Extract complex inline types into named `type` or `interface` declarations.
- Avoid `any`; use `unknown` and narrow before use.
