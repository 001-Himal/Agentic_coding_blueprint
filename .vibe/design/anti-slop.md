# design anti-slop.md

Do NOT:
- generic gradients without design justification
- excessive glassmorphism
- random rounded cards everywhere
- excessive shadows
- animations that exist just because "AI does that"
- inconsistent button styles
- new colors when a token works
- duplicate components with slightly different styling
- icons where text is clearer
- sacrifice usability for visual novelty
- display tech stack badges, library names, or architecture bragging in UI (e.g., "Powered by X", "Auth via Supabase", "Database: PostgreSQL")
- expose backend protocols or transport mechanisms on user-facing controls/badges (e.g., "Quick Match • WebSocket", "Real-time matchmaking via Socket.io")

Every visual element must have a purpose. All UI text must serve the end user, not advertise the implementation.
