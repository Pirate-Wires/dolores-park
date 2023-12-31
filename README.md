# dolores-park

This repository deploys a Serverless Function (`api/index.js`) to Vercel for redirecting the dolorespark.pw domain to https://piratewires.us/.

The api/index.js file exports a function that redirects all requests to piratewires.us.

Example: https://dolore-park.vercel.app/some/old/url will redirect to https://piratewires.us/some/old/url.

## Usage

To alias the domain:

- Go to domain registrar's DNS settings for dolorespark.pw (Google Domains)
- Create an ALIAS or ANNAME record pointing dolorespark.pw to the Vercel deployment URL
- Now traffic to dolorespark.pw will hit the Vercel serverless function first, and get redirected to https://piratewires.us/.

The function returns a 301 permanent redirect status.

## Customization

To customize the redirect logic, edit the api/index.js file.
