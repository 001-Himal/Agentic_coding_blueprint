# frontend.md

- Reuse the design system — never invent ad-hoc styles.
- Every screen handles loading/empty/error.
- Mobile-first and usable at small widths.
- Accessibility: semantic HTML, keyboard nav, alt text, contrast.
- User-centric copy only: Never reveal tech stack, database vendors, auth providers, or protocols in UI text (e.g., no "Powered by Neon PostgreSQL", "Supabase Auth", "Quick Match • WebSocket", "Real-time matchmaking"). Statuses and loaders must describe user actions ("Finding match...", "Saving..."), never plumbing ("WebSocket connecting...", "Executing query...").
