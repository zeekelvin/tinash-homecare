# Tinash Homecare Services

A custom Next.js website for Tinash Homecare Services in New Jersey, deployed through Vercel. WordPress is not required.

## Development

```sh
npm ci
npm run dev
npm run typecheck
npm run build
```

Requires Node.js 22 or newer. Source content is in `lib/content.ts`; website policy text is in `lib/legal.ts`. Shared presentation components are in `components/`.

## Features

- Cinematic home page with locally hosted films, manual pause/play controls, reduced-motion and data-saver support.
- Custom generated imagery, responsive design, manual image carousel, clear keyboard focus, and accessible navigation.
- Home care overview and six service pages, DDD information, care process, New Jersey service area, about, careers, and contact.
- Privacy, terms, HIPAA information, cookies, accessibility, and care rights pages.
- Email inquiry composer with separate family, professional referral, and career paths. It opens a reviewed draft in the visitor's email client; it does **not** silently submit to a server or claim successful delivery.
- Open Graph image, sitemap, robots controls, error page, security headers, and migration redirects.

## Deployment and domain migration

The GitHub repository is connected to Vercel. Keep deployment protection at its team default. Set `NEXT_PUBLIC_SITE_URL` to the final canonical origin when the custom domain is connected. Set `SITE_INDEXABLE=true` only for the approved production domain; previews default to noindex.

Existing URL mappings are in `next.config.ts`: `/mmd-care` -> `/ddd-care`, `/care-plans` -> `/how-care-works`, `/application` -> `/careers#apply`.

Before switching the live domain:

1. Confirm the exact business identity, service availability, credentials, hours, counties, and privacy contact.
2. Have the appropriate business/legal reviewer adopt the policy text. The HIPAA information page is not an adopted Notice of Privacy Practices or a compliance certification; add the agency's approved notice when available.
3. Review all media and their illustrative disclosure. Do not represent generated people as real clients, caregivers, or testimonials.
4. Back up the existing WordPress files, database, media, URL list, and DNS records.
5. Confirm redirects and email behavior. Keep Hostinger MX, SPF, DKIM, and DMARC records intact when changing website A/CNAME records.
6. If direct website form delivery is desired, configure a suitable mail transport and server-side validation/abuse controls. Clinical information needs a separately assessed intake workflow; do not add clinical fields to the general inquiry composer.
7. Review the production site on mobile and desktop and confirm crawl/index settings.

No advertising, analytics, session replay, remote-font, or embedded third-party video scripts are included. Fonts and media are served with the website. Hosting-level logs and protection features remain subject to the hosting provider's policies.

## Media

Custom cinematic assets were generated with Higgsfield (GPT Image 2.5 and Seedance 2.5). The files `care-team.jpg` and `home-care.png` are reused from Tinash's existing website. The site discloses illustrative/AI-generated imagery. All media should be reviewed by the owner before domain cutover.

## License

Public source visibility does not grant a license to reuse Tinash branding, content, or media. No open-source license is granted by this repository.
