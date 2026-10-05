# Filled Example — FEAT-001 User Signup

Shows a completed spec for a small feature. Copy the format, not the content.

## Goal
Allow a new user to create an account with email + password.

## User Story
As a visitor, I want to sign up with email and password so I can use the app.

## Requirements
- Email uniqueness enforced
- Password min 8 chars, hashed before storage
- Confirm email not required in v1

## Out of Scope
- OAuth, password reset, 2FA

## Files Expected To Change
- src/auth/signup.ts (new)
- src/auth/validation.ts (new)
- src/routes/auth.ts (add route)
- tests/auth/signup.test.ts (new)

## Files That Must Not Change
- .github/workflows/**, migrations/** (none needed in v1)

## Security Considerations
- Rate limit signup endpoint
- Never log passwords
- Return generic errors (don't leak whether email exists beyond expected flow)

## Edge Cases
- Duplicate email, invalid format, very long input, concurrent signups

## Acceptance Criteria
- [ ] Valid signup creates user and returns 201
- [ ] Duplicate email returns 409
- [ ] Invalid input returns 400 with field errors

## Test Requirements
- unit: validation function
- integration: POST /signup happy + errors

## Rollback Plan
- Revert route + delete files; no DB change in v1
