# KSA Win Wall

A live celebration screen for the Bayzat KSA sales team. Leave it open on a
monitor or the sales-floor TV.

- **A deal closes** → full-screen takeover, screen shake, confetti and a gong.
  Shows the deal name, size, employee count and who closed it, plus month and
  quarter attainment.
- **A self-prospected opp is created** → a corner toast and a bell.
- **Hall of Fame** → leadership board, trophy cabinet and 17 unlockable
  achievements per rep.

## Using it

Open the site and tap **Arm the gong** once. Browsers block audio until
someone interacts with the page, so this is needed once per session — do it
each morning on the TV.

Sounds are synthesised in the browser; there are no audio files to load.
The page re-checks the source sheet every 45 seconds and only celebrates
deals dated within the last 30 days, so it won't replay history.

Each browser remembers what it has already celebrated, so opening the page
fresh will not re-fire old wins.

## Data

Reads three tabs from the team's published Google Sheet (synced from
Salesforce every 4 hours): won deals, self-prospected opps, and inbound.
Config lives in the `CONFIG` block at the top of the script in `index.html`.

Targets are per rep, per month in the `TEAM` array — update that array when
the team or the target schedule changes.

## Access

Private repo. Deployed on Cloudflare Pages behind Cloudflare Access,
restricted to `@bayzat.com` email addresses. Do not make this repo public —
the page carries the Sheet's publish ID.
