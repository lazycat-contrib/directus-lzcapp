# Directus (LazyCat LPK)

Headless CMS and data platform.

- Upstream: https://github.com/directus/directus
- Image: `directus/directus:12.6.0` (Docker Hub, mirror mode, digest-matched)
- License: MSCL-1.0-GPL (full text in `content/licenses/LICENSE`)
- Containers: Directus + PostgreSQL 16

## License note

The repo reports NOASSERTION because MSCL-1.0-GPL is a bespoke licence. Reading `license` in full:

- **License Grant** explicitly grants the right to display and **redistribute** the Software
  for any Permitted Purpose.
- **Permitted Purpose** covers own use, non-commercial education/research, and professional
  services deploying or hosting the Software for a licensee.
- **Redistribution** permits redistribution provided you (A) include the licence terms and keep
  copyright notices, and (B) impose no further restrictions or fees on the granted rights.
- **Limitations** forbid circumventing the licence-key functionality.

Redistributing to individual users running it on their own devices falls under these terms, so
the licence ships unmodified. This package does not touch Directus' licence-key mechanism.

## Notes

- Admin is seeded from `ADMIN_EMAIL` / `ADMIN_PASSWORD` on first init; `KEY` and `SECRET` come
  from platform stable secrets.
- Port 8055, user `node`. `PUBLIC_URL` set to the app domain so generated links resolve.
- Uploads and extensions persist on `/lzcapp/var/{uploads,extensions}`.
- No mail service configured.
- Not yet verified on a real device.
