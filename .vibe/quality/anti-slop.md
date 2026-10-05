# anti-slop.md

The agent must avoid:
- Placeholder functionality presented as finished
- Fake/mock data in production paths
- TODOs disguised as implementation
- Dead code, duplicate logic, needless abstractions
- Giant files/functions, copy-pasted components
- Generic error handling, `any` everywhere, silent failures
- Hardcoded values where config belongs
- Unused dependencies/imports
- Over-engineering, "future-proofing" without a requirement
- Architecture swaps because the AI prefers another stack
- Rewriting working code unnecessarily
- Inventing features, inventing APIs
- Claiming completion without verification
- Unnecessary documentation or verbose code
- Leaking tech stack, infrastructure, or protocols into user-facing UI/UX (e.g., "Powered by Neon PostgreSQL", "Supabase Authentication", "Quick Match • WebSocket", "Real-time matchmaking (SSE)"). All user-facing text must use clean domain language, never technical plumbing or stack bragging.

## Golden rule
Prefer the simplest correct implementation that fits the existing architecture.
