# Focus Group Dashboard

Static HTML dashboard for running the insurance focus group workflow in n8n and viewing results in collapsible per-persona sections.

## How it works

1. You paste copy (handwritten letter, landing page, ad, LinkedIn post) into the input
2. Click "Run focus group"
3. Dashboard POSTs to your n8n workflow's webhook (`/webhook/focus-group-insurance`)
4. n8n runs 8 personas → copywriter → prediction engine (~75 sec)
5. Dashboard renders the response with collapsible cards per persona, color-coded by role (target / borderline / filter), with YES/NO vote badges
6. Copy buttons everywhere, Markdown download for archiving

## Setup

1. Open the dashboard, click **⚙ Webhook settings**, paste your n8n production webhook URL (e.g. `https://n8n.aventra-ai.com/webhook/focus-group-insurance`)
2. In n8n: activate the workflow so the production webhook URL is live
3. Run

## Local dev

It's a single HTML file with no build step. Just open `index.html` in a browser.

## Deployment

Hosted on GitHub Pages. Push to `main` → auto-deploys.
