# Cloudflare setup

Workers serves original-site, restoring the original Audio Benders storefront with templates, beats, mixing services, and the illustrative order dashboard. The V2 folder is retained as an unused alternative.

Production branch: main. Root directory: repository root. Build command: blank. Deploy command: npx wrangler deploy. Worker name: audiobenders-website.

The original HTML was recovered from https://audiobendersco.com/. Its referenced assets/studio.jpg returned HTTP 404 on recovery; no substitute image was introduced.

Stripe checkout, uploads, order management and automatic digital delivery remain demo placeholders. No secret keys belong in the site or repository. Payment verification and private delivery must be implemented before launch.
