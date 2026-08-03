# AI Development Agent Instructions

## General Principles

- Always understand the existing codebase before making changes.
- Follow the existing architecture, coding style, naming conventions, and project structure.
- Prefer consistency with the current codebase over introducing new patterns.
- Keep changes as small, isolated, and maintainable as possible.
- Prefer modifying existing files instead of creating new ones.
- Never rewrite working code without a clear reason.
- Solve only the requested task. Do not perform unrelated refactoring unless explicitly requested.
- Prefer fixing the root cause instead of masking symptoms.
- If existing project conventions conflict with general best practices, follow the project's conventions unless explicitly instructed otherwise.

---

## Tech Stack

### Frontend

- React 19
- Vite
- Tailwind CSS v4
- shadcn/ui

### Backend

- Hono
- Bun runtime

### Database

- Supabase (PostgreSQL)

### Package Manager

- pnpm

---

## Before Writing Code

- Carefully inspect the surrounding code before making changes.
- Read existing code before writing new code.
- Search for existing implementations before creating new ones.
- Understand the existing implementation instead of making assumptions.
- Never assume the task is isolated.
- Identify all usages of the modified code before making changes.
- Prefer extending existing implementations over introducing parallel ones.
- Reuse existing project utilities whenever possible.
- Never invent APIs, functions, files, configurations, libraries, project behavior, database schema, environment variables, or business logic.
- If something cannot be determined from the codebase, explicitly state that instead of guessing.
- If requirements are ambiguous or incomplete, stop and ask for clarification before writing code.
- If multiple implementation options exist, briefly explain the trade-offs before choosing.
- Clearly mention assumptions when necessary.
- If confidence is low, explicitly say so.
- Never fabricate certainty.
- Before implementing changes affecting multiple modules, briefly explain the implementation plan.

---

## React Rules

- Keep components small and reusable.
- Prefer composition over duplication.
- Avoid unnecessary re-renders.
- Use correct dependency arrays in useEffect.
- Clean up subscriptions, timers, and event listeners.
- Prefer existing hooks before creating new ones.
- Avoid recreating objects and functions unnecessarily inside components.
- Use memoization only when it provides measurable value.

Never create:

- Infinite useEffect loops.
- Duplicate API requests.
- Repeated fetches on every render.
- Duplicate hooks that already exist in the project.

---

## Supabase Rules

- Select only the required columns.
- Avoid SELECT * unless explicitly requested.
- Reuse existing queries whenever possible.
- Prefer pagination for large datasets.
- Avoid N+1 queries.
- Never perform multiple sequential queries when a single query can solve the problem.
- Never create recursive or infinite database requests.

---

## Performance

Always consider performance.

Prefer:

- Efficient database queries.
- Lazy loading.
- Pagination.
- Memoization when appropriate.
- Stable references for frequently passed props.

Avoid:

- Duplicate requests.
- Unnecessary renders.
- Fetching unused data.
- Premature optimization.

Optimize only when there is a measurable benefit or a clear performance issue.

---

## Code Style

- Use modern JavaScript/TypeScript.
- Prefer const over let.
- Prefer async/await.
- Write meaningful variable names.
- Keep functions small.
- Avoid duplicated code.
- Prefer simple solutions over clever ones.
- Avoid unnecessary abstractions.
- Avoid overengineering.
- Write self-documenting code.
- Prefer existing project types over creating duplicate interfaces.
- Never rename files, variables, functions, or classes solely for personal preference.
- Never change public APIs unless explicitly requested.
- Preserve existing formatting unless the modified lines require changes.
- Do not reformat unrelated code.
- Do not duplicate existing business logic.
- Extract shared logic only when duplication already exists.

---

## Comments

- Write comments only when they provide real value.
- All comments must be written in English.
- Never write comments in any other language.
- Never leave AI signatures, watermarks, hidden markers, invisible Unicode characters, or identifying phrases.

---

## Dependencies

- Do not add dependencies unless absolutely necessary.
- Before introducing a new library, verify that equivalent functionality does not already exist in the project.
- Prefer built-in language or framework capabilities.

---

## Git Workflow

- Never commit automatically.
- Never push automatically.
- Never create branches automatically.
- Never merge automatically.
- Never rewrite Git history.
- Never commit directly to the main branch for feature work.
- Create a feature branch for each task.
- Keep commits focused.
- Do not modify unrelated files.
- Only provide suggested Git commands if explicitly requested.

---

## Security

- Never expose secrets.
- Never hardcode credentials.
- Never log sensitive information.
- Preserve existing security practices.

---

## Debugging

When fixing bugs:

- Identify the root cause before making changes.
- Do not apply speculative fixes.
- Explain why the bug occurred.
- Verify that the fix does not introduce regressions.

---

## After Every Change

After implementing any change:

- Review every modified file.
- Review all directly affected modules.
- Review related code paths that may now be affected.
- Verify imports, exports, types, interfaces, dependencies, and function calls.
- Verify that existing functionality remains intact.
- Check for possible regressions.
- Check loading states.
- Check error handling.
- Check empty states.
- Ensure there are no obvious runtime errors.
- Ensure there are no compilation or type errors.
- Ensure the solution follows the project's architecture.
- Ensure the requested task is fully completed before considering it finished.

---

## Final Checklist

Before finishing:

- Verify the project builds successfully.
- Check for obvious bugs.
- Verify imports and exports.
- Verify all affected files remain consistent.
- Check related usages of modified code.
- Verify edge cases.
- Ensure the implementation is production-ready.
- Minimize side effects.
- Ensure the implementation fully satisfies the original request.
- Perform a final self-review before responding.

---

## Forbidden Behavior

Never:

- Hallucinate project structure.
- Invent business logic.
- Invent API behavior.
- Invent database schema.
- Invent configuration values.
- Invent environment variables.
- Silently change unrelated code.
- Leave TODOs instead of implementing requested functionality unless explicitly requested.
- Add AI signatures, hidden markers, invisible Unicode characters, watermarks, or comments indicating AI-generated code.

---

## Decision Priority

When making decisions, prioritize:

1. Correctness.
2. Simplicity.
3. Consistency with the existing project.
4. Readability.
5. Maintainability.
6. Performance (when appropriate).