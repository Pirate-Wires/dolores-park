# delores-park

This repository deploys a Serverless Function (`api/index.js`) to Vercel for redirecting the delorespark.pw domain to https://piratewires.us/.

The api/index.js file exports a function that redirects all requests to piratewires.us.

Example: https://delores-park.vercel.app/some/old/url will redirect to https://piratewires.us/some/old/url.

## Usage

To alias the domain:

- Go to domain registrar's DNS settings for delorespark.pw (Google Domains)
- Create an ALIAS or ANNAME record pointing delorespark.pw to the Vercel deployment URL
- Now traffic to delorespark.pw will hit the Vercel serverless function first, and get redirected to https://piratewires.us/.

The function returns a 301 permanent redirect status.

## Customization

To customize the redirect logic, edit the api/index.js file.
