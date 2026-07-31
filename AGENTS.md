# AI Agent Instructions

## Project Overview

This project follows an AI-assisted development workflow.

Always understand the existing codebase before making changes.
Prefer small, maintainable changes over large rewrites.

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

## Development Rules

- Read existing code before writing new code.
- Follow the current architecture.
- Prefer modifying existing files instead of creating new ones.
- Keep changes small and focused.
- Do not introduce unnecessary dependencies.
- Ask for clarification if requirements are ambiguous.
- Explain the implementation plan before making major changes.

---

## React Rules

- Avoid unnecessary re-renders.
- Use correct dependency arrays in useEffect.
- Clean up subscriptions and event listeners.
- Keep components small and reusable.
- Prefer composition over duplication.

Never create:

- Infinite useEffect loops.
- Duplicate API requests.
- Repeated fetches on every render.

---

## Supabase Rules

- Select only required columns.
- Avoid SELECT * unless explicitly requested.
- Prefer pagination for large datasets.
- Reuse existing queries whenever possible.
- Avoid N+1 queries.
- Never create recursive or infinite database requests.

---

## Performance

Always think about performance.

Prefer:

- Efficient database queries.
- Lazy loading.
- Pagination.
- Memoization when appropriate.

Avoid:

- Duplicate requests.
- Unnecessary renders.
- Fetching unused data.

---

## Code Style

- Use modern JavaScript.
- Prefer const over let.
- Prefer async/await.
- Write meaningful variable names.
- Avoid duplicated code.
- Keep functions small.
- Write self-documenting code.

---

## Git Workflow

- Never commit directly to main for feature work.
- Create a feature branch for each task.
- Keep commits focused.
- Do not modify unrelated files.

---

## Final Checklist

Before finishing:

- Verify the code builds successfully.
- Check for obvious bugs.
- Check imports.
- Check edge cases.
- Ensure the solution follows the project architecture.