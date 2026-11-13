# Los Rojas Coffee — Prototype

A responsive, bilingual Spanish and English coffee showcase for Los Rojas Coffee. This first version is a static site with no framework, build command, backend, cookies, forms, cart, or payment flow.

## Run locally

Open `index.html` in a browser, or serve the repository root with any static web server. The site uses Google Fonts when a network connection is available and falls back to system fonts.

## Publish with Cloudflare Pages

The project brief names Cloudflare Pages as the provisional host. No hosting account or deployment connection is configured in this repository. To publish:

1. An adult account owner should sign in to Cloudflare and create a Pages project connected to the private GitHub repository `2009Juan-Sep/los-rojas-coffee`.
2. Select branch `prototype/initial-site` for the first prototype.
3. Choose **None** as the framework preset. Leave the build command empty and set the output directory to `/` (the repository root).
4. Start the deployment and wait for Cloudflare to show a successful build and HTTPS `pages.dev` address.
5. Open the public address on desktop and mobile, confirm that the page loads over HTTPS and that both language choices work. Add a custom domain only after its adult owner registers and configures it.

The repository is private. Connecting it to hosting requires authorization in the hosting account and GitHub. This repository does not contain a Cloudflare token, deployment secret, or domain configuration.

## Confirmed-content boundaries

- The farm is Finca Bella Vista in Manaure, Cesar, Colombia. Gladys Rojas is its owner and leads production.
- Tabi, Caturro and Castillo varieties and 250 g and 500 g formats were communicated by the brand; availability, product composition and product-specific roast are not confirmed.
- Medium and medium-high roasts are mentioned in the brief but are not assigned to products here.
- The Castillo Honey sensory analysis dated November 24, 2024 is identified as one sample, not a current product specification.
- The Honey explanation follows the brief's cautious wording.
- Contact channels and the desired domain `losrojascoffee.com` remain unconfirmed. No contact information is invented.
- No original photos or video assets were present in the repository at implementation time. The abstract artwork is drawn with CSS and does not claim to depict the actual farm or coffee.

The bilingual selector remembers the visitor's choice in local browser storage. No product administration, AI assistant, ordering, or checkout is implemented.
