# UI Guidelines

Core rules and principles for user interface copy, interaction, and aesthetics.

---

## 1. No Tech-Stack or Plumbing Leakage in UI Copy

AI models frequently leak internal technologies, infrastructure vendors, and protocol names into user-facing copy, badges, footers, buttons, and loading states. **This is considered AI slop and is strictly prohibited.**

### The Core Rule
All user-facing copy must be **100% user-centric and domain-focused**. Users care about what the product does for them, not what packages are in `package.json` or what database hosts their data.

### Anti-Patterns to Avoid vs. What to Write

| Bad (Tech-Stack / Plumbing Slop) | Good (User-Centric Copy) | Why |
|---|---|---|
| `"Powered by Neon PostgreSQL"` | *(Omit or use company/product branding)* | Users don't care which DB vendor stores data. |
| `"Supabase Authentication"` | `"Sign In"` / `"Secure Account Access"` | Auth vendor is an implementation detail. |
| `"Quick Match • WebSocket"` | `"Quick Match"` / `"Play Now"` | Transport protocol has no meaning to players. |
| `"Real-time matchmaking (SSE / Socket.io)"` | `"Live Matchmaking"` / `"Finding an opponent..."` | Users want the outcome, not the mechanism. |
| `"Connecting to WebSocket server..."` | `"Connecting..."` / `"Joining room..."` | Describes user state rather than network socket. |
| `"Querying Postgres table 'games'..."` | `"Loading your games..."` | Never expose internal schema or SQL verbs. |
| `"State synced with Zustand store"` | *(Silent / subtle UI update)* | Internal state management is invisible to users. |
| `"Database error 500: unique constraint"` | `"An account with this email already exists."` | Raw DB errors are confusing and security risks. |
| `"Built with Next.js 14, Tailwind & Prisma"` | `"Fast, modern web experience"` | Tech stack brags belong in README, not UI. |

---

## 2. Interaction & State Feedback

- **Loading States**: Describe the human action taking place (`"Preparing your game..."`, `"Saving changes..."`).
- **Empty States**: Guide the user on what action to take (`"No matches played yet. Start your first game!"`).
- **Error States**: Be polite, clear, and actionable (`"We couldn't reach the server. Please check your connection and retry."`).

---

## 3. Visual & Aesthetic Restraint

- **Purposeful Elements**: Every card, badge, and border must have a functional purpose.
- **No Decorative Badges**: Do not slap tech badges or framework pills onto headers, footers, or cards.
- **Consistent Tokens**: Rely exclusively on design tokens for color, typography, radius, and spacing.
