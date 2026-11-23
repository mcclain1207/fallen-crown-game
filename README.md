# The Fallen Crown — Live Multiplayer Prototype

## Features
- Host creates a six-character room code.
- 10–30 players join from their own phones, no account needed.
- Unique secret roles randomly assigned with player-count scaling.
- Each player sees only their own role. Host sees private full roster.
- Host controls round phases and banishments; victory is automatically detected.
- Players' screens update approximately every 2.5 seconds.

## Run locally
Install Node.js 18+ and run `npm start`, then open http://localhost:3000.
For phones on the same Wi-Fi, use the host computer's LAN IP with port 3000 (and allow firewall access).

## Publish online
This is a Node server, NOT a static HTML-only site. Upload the project to a Node-compatible hosting provider (for example Render Web Service) with start command `npm start`. A static hosting drop alone will not work. Set `DATA_FILE` to a persistent disk path if your host supports persistent disks. Otherwise games will reset on redeploy or container restart.

## Security and youth safety
Room codes and host tokens are secrets. Do not share the host's browser/device. Students should use first names or nicknames, not personal contact details. No accounts or chat messages are stored. Player tokens are saved in the browser on their device. The server stores games in a JSON file; delete it to erase games. This is a small-group prototype, not a security-audited public service. Use HTTPS hosting for public play.

## Gameplay notes
The moderator conducts role powers, night actions, votes, and one final vote for banished players offline. The site does not yet automate those mechanics. The role list is a first-pass prototype and needs balance testing. No SMS messages are sent; share the join link through your usual texting app.
