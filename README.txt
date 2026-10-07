# Family Column Game

A phone-friendly multiplayer Column Game.

## What it does
- One person creates a game and gets an invite link.
- Family members open the invite link on their own phones.
- Each player types answers privately on their own device.
- Players press "I'm finished" and their answers are locked.
- The host reveals the round.
- Scoring is automatic:
  - 10 points = unique answer
  - 5 points = same answer as someone else
  - 0 points = blank
- A leaderboard shows totals.

## Important
The host's browser must stay open during the game. This version uses PeerJS/WebRTC for direct browser connections, so there is no database or account system.

## Put it online
The easiest options are GitHub Pages, Netlify, or Cloudflare Pages.

### GitHub Pages
1. Create a GitHub repository.
2. Upload `index.html`.
3. In the repository, open Settings -> Pages.
4. Choose "Deploy from a branch", select the main branch and `/root`.
5. Open the resulting HTTPS website on your phone.
6. Create a game and send the invite link to your family.

### Netlify
1. Create a Netlify account.
2. Choose to deploy a site manually.
3. Upload `index.html`.
4. Open the HTTPS site and create a game.

## Notes
- HTTPS is recommended/required by browsers for reliable WebRTC connections.
- The public PeerJS signalling service is used only to establish browser connections; game answers are sent peer-to-peer when the host reveals.
- This is designed for casual family play, not for high-security or competitive use.
