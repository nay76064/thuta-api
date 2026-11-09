# Haven API

The API serves property search, listing details, accounts, owner listing management, and administrator review for the Haven marketplace. Its supported behavior is described in [SPEC.md](SPEC.md).

## Run locally

Requires Node.js 20 or later. Install dependencies, configure the environment, and start the service:

```sh
npm install
cp .env.example .env
npm run dev
```

The API listens on port 4001 and stores its SQLite database under `data/`. On first run it seeds illustrative homes and demo accounts. The demo password is `HavenDemo2026!`; email addresses are `owner@haven.demo`, `admin@haven.demo`, and `buyer@haven.demo`. These accounts and listings are for local use only.

Set a private `JWT_SECRET` before using accounts outside a local demo. Set `WEB_ORIGIN` to the permitted web client origin. Run `npm run build` to compile the service.
