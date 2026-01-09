## Tech Stack
- Framework: React 18+ (functional components and hooks only)
- Build Tool: Vite
- Styling: Tailwind CSS (utility-first; no custom CSS files unless scoped via `.module.scss`)
- State Management: Redux Toolkit (RTK) – use slices per feature; prefer local state or custom hooks first
- Backend / Data: Firebase
- Authentication (email magic links / passwordless)
- Firestore (primary database)
- Storage (for files/images if needed)
- Hosting (deployment)
- Functions (server-side logic when required)
- Routing: React Router v6+ (only if multi-page views are needed)
- Forms: React Hook Form preferred; otherwise controlled components
- UI Library: Custom components only (no external component libraries)

## Key Conventions

### Component Organization
- components/ → Pure, stateless, reusable across the app (e.g., `<Button />`, `<Input />`, `<Modal />`).
- modules/ → Feature-specific containers that hold state and orchestrate child components (e.g., `Board`, `TicketDetails`, `Authenticate`).

### Naming
- Components & modules: PascalCase (files and exports)
- Hooks & utilities: camelCase (e.g., `useAuthenticateForm`, `formatDate`)
- Redux slices: camelCase ending with `Slice` (e.g., `ticketSlice`)
- CSS modules: PascalCase.module.scss matching the component/module name

### State Management
- Use local component state first.
- Move to custom hooks for shared logic within a module.
- Use Redux only for truly global or cross-module state.

### Styling
- Tailwind classes only in JSX.
- Scoped overrides via CSS modules (`.module.scss`) when Tailwind cannot achieve the desired result.
- No inline styles or `!important` unless absolutely necessary.

### Firebase Usage
- Import modular SDK (`import { getAuth, sendSignInLinkToEmail } from 'firebase/auth'`).
- Keep Firebase rules tight and validate data on client only for UX, not security.

### Code Quality
- Write readable, self-documenting code.
- Keep components small and single-responsibility.
- Handle loading, success, and error states explicitly.
- Ensure responsiveness (Tailwind mobile-first).
- Follow accessibility best practices (semantic HTML, labels, ARIA where needed).

### Testing & Development
- Every new feature must be testable immediately (use mock/fake data when real data is unavailable).
- Prefer minimal changes focused on the current requirement.