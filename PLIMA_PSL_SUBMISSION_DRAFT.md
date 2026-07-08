# Plima / plima.site — PSL submission draft (finalize later)

Internal prep file. Do NOT open a PR until the two blockers below are cleared. When they are, copy the "PR body" section into the description of a new Pull Request (using the official PSL template), update the PR number in the _psl record, then submit.

## Blockers to clear before resubmitting

1. Distinct-user count. The PSL only considers requests at roughly 2000 to 3000 distinct users using subdomains of plima.site. Current status: 0. Resubmit once the threshold is reached.
2. Registration term. The domain must keep more than 2 years remaining. Current status: about 1 year. Action: renew plima.site for 2 years or more.

## To do at resubmission time

- Renew plima.site (>= 2 years).
- Verify or recreate the _psl.plima.site TXT record pointing to the new PR: dig +short TXT _psl.plima.site must return the new PR URL.
- Confirm the abuse-contact URL is accessible on the site.

## PR body (answers already gathered)

Organization Website: https://www.plima.ai/

Description of Organization: Plima is a product operated by Check Company S.A.S.U., a French company (SIREN 830789376, based in La Ciotat, France), which also operates Checksub. Plima provides businesses with AI-managed websites, each hosted on its own dedicated subdomain of plima.site (for example customer.plima.site). I am Florian Stegre, CEO of Check Company S.A.S.U., submitting on behalf of the company. The bare domain plima.site only redirects to our organization website and sets no cookies.

Reason for PSL Inclusion: Each customer site is served from its own subdomain of plima.site and must be treated as an independent origin. Listing plima.site in the PRIVATE section lets browsers and other PSL consumers isolate cookies between customer subdomains (no shared cookie scope on the parent domain) and assign separate Safe Browsing and search reputation per customer site. We use Cloudflare for DNS and TLS across all sites, so this request is not intended to work around any third-party certificate issuance or rate limits. We confirm plima.site will hold more than 2 years of registration and maintain more than 1 year remaining to stay listed.

Number of THOUSANDS of distinct users: TO COMPLETE once the ~2 to 3 thousand threshold is reached. Currently below it.

Role-based email (section and template): team@plima.ai
Abuse contact: team@plima.ai (confirm the abuse page URL on the site)

## Entry for public_suffix_list.dat (PRIVATE section)

// Plima : https://www.plima.ai/
// Submitted by Florian Stegre <team@plima.ai>
plima.site

Placement: alphabetically within the block, between pley.games (Pley) and onporter.run (Porter). Note: the current entry on this branch still uses florian@checksub.com; switch it to team@plima.ai before resubmitting.
