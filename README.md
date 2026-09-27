# Coin Catcher — Facebook/HTML5 learning demo

This is a deliberately small HTML5 game for learning the publishing pipeline.

## Files
- index.html — complete playable game, no external libraries
- README.md — setup/publishing notes

## Run locally
Option 1: double-click index.html (most gameplay works).
Option 2: serve the folder over HTTP:
  Python:
    python -m http.server 8080
  then open:
    http://localhost:8080

## Production architecture
Browser/Facebook -> HTTPS game URL -> your hosting -> index.html

## Important
This demo contains NO Meta SDK, NO ads, and NO payments yet.
That is intentional: first prove the game can be hosted and loaded correctly.
Add Meta-specific integration only after the basic deployment works and after checking
the current Meta developer documentation/dashboard options.

## Suggested next implementation stages
1. Deploy this folder to HTTPS hosting.
2. Create/configure the Meta developer app/game product available to your account.
3. Test the game URL and required settings in Meta's current dashboard.
4. Add analytics events.
5. Add monetization using the currently supported Meta game monetization flow.
6. Test review/policy requirements before production release.
