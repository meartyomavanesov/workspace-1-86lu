# Implementation instructions

## Critical Rules - Follow Strictly
- Do not delete the spec directory or any files within it unless explicitly instructed by the user.
- Do not change the overall architecture, folder structure, or tech stack unless explicitly instructed by the user.
- Do not introduce new major dependencies (e.g., new state library, UI framework) without explicit approval.
- Do not remove or significantly refactor existing code unless directly required for the task.

## Implementation Requirements
- Make minimal, focused changes — only modify what is necessary to fulfill the requirement.
- Prefer reusing existing components, patterns, and utilities.
- Ensure the implementation is immediately testable:
- Use fake/mock data if real data is not available.
- Avoid hard dependencies on external services during development.
- Write clean, readable code with meaningful variable and function names.
- Follow existing naming conventions and Tailwind patterns.

## User Experience
- If the task requires user action to complete (e.g., connecting GitHub, running a migration, manual setup), provide **clear, step-by-step instructions** in a comment or visible message.
- Show loading states, success feedback, and helpful error messages.
- Maintain consistency with existing UI (colors, spacing, typography).

## Quality & Safety
- Preserve existing functionality — do not break unrelated features.
- Handle edge cases mentioned in the requirement.
- Add or update comments if logic is non-obvious.
- Ensure responsiveness (mobile-friendly by default via Tailwind).
- Follow accessibility best practices (semantic HTML, labels, focus states).

## After Implementation
- Commit message should clearly describe what was built and why.
- If tests are needed, add basic ones or note where they should go.
- Leave the codebase in a stable, working state.