# Incognito

A front-end prototype for an anonymous, quiz-based social game. Open `index.html` directly in a browser.

## Included Prototype Flows

- Anonymous local profile setup with a custom username, optional gender, vibe, and quiz.
- Safety-first profile text guidance and a visible pending-review state.
- Universe, college, and invite-only room servers. College and room names can be changed in a production version; Universe is fixed.
- Drag or button swipe interactions: left to pass, right to open a profile's quiz.
- Correct quiz flow that creates a reciprocal quiz notification and explains the mutual-unlock chat rule.
- Creation of a custom invite-only room in the interface.
- A shareable invite link for custom rooms, plus a separate global directory search for public school and college servers.
- An anonymous browser-local account with a generated user address, generated password, password hash, and saved profile/quiz data.

## Production Requirements

This prototype stores one anonymous profile in the current browser's local storage. It does not provide cross-device accounts, server-side data storage, real location, or encryption. A real launch needs:

- A privacy-reviewed database model with random user IDs, minimal retention, profile moderation queues, reports, and rate limits.
- Server-side quiz and match verification, so users cannot inspect answers in the browser.
- A consent-driven location service that stores only coarse, short-lived proximity data for Universe, never exact public coordinates.
- End-to-end encrypted chat built with an audited protocol and a separate key-management design.
- A moderator console that only sees submitted profile content needed for review, not real-world identity fields.

