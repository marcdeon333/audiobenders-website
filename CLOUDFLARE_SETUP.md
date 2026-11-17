# Cloudflare setup

This repository contains the uploaded V2 storefront. It differs from the site previously served at audiobendersco.com. The root wrangler.jsonc points Workers Static Assets at Audio_Benders_Website_V2; no build step is required.

## Connect GitHub

In GitHub Settings > Applications > Installed GitHub Apps, configure Cloudflare Workers & Pages to allow this repository. In Cloudflare Workers & Pages, select marcdeon333/audiobenders-website.

Use these Workers deployment settings:

- Worker name: audiobenders-website (must match wrangler.jsonc)
- Production branch: main
- Root directory: repository root (leave default)
- Build command: blank
- Deploy command: npx wrangler deploy

First verify the generated workers.dev preview. Connect or migrate audiobendersco.com only after reviewing that preview and identifying the existing Cloudflare project that serves the domain. This repository does not change DNS or attach the domain automatically.

## Payments are not yet connected

The uploaded index.html expects window.ABC_CHECKOUT_LINKS, keyed by product ID, for hosted checkout links. Actual Stripe payment links or a server-side Checkout integration are still needed. Product details and prices are illustrative until verified. Do not place secret API keys in HTML or GitHub; use Cloudflare encrypted secrets for server-side integrations. Digital fulfillment and payment confirmation also require setup before launch.
