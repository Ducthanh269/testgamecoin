# Coin Catcher — Facebook/HTML5 learning demo

This is a deliberately small HTML5 game for learning the publishing pipeline, now successfully updated with Facebook Instant Games SDK.

## Files
- index.html — complete playable game, integrated with FBInstant SDK.
- README.md — setup/publishing notes

## Run locally
Option 1: You can still double-click index.html, but the Meta SDK may throw cross-origin or initialization errors in the browser console.
Option 2 (Recommended): Serve the folder over HTTP to test loading behaviors:
  Python:
    python -m http.server 8080
  then open:
    http://localhost:8080

## Production architecture
Browser/Facebook -> HTTPS game URL -> your hosting -> index.html

## Important Notes on Meta SDK
This demo now contains the Meta Instant Games SDK (`fbinstant.6.3.js`).
It handles the basic SDK lifecycle: 
1. `FBInstant.initializeAsync()`
2. `FBInstant.setLoadingProgress(100)`
3. `FBInstant.startGameAsync()`

The demo still does not include ads or in-app payments. Focus on verifying the game can be hosted, loaded correctly in Facebook's iframe, and successfully starts the game loop.

## Suggested next implementation stages
1. Deploy this folder to HTTPS hosting.
2. Create/configure the Meta developer app/game product available to your account.
3. Add the Web Hosting URL in Meta's dashboard.
4. Test the game directly inside Meta's platform to ensure the SDK initializes without errors.
5. Add analytics events or leaderboards.
6. Add monetization using the currently supported Meta game monetization flow.