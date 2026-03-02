<h1 align="center">Nault Pro</h1>

<h3 align="center">Nano.to's Nault Fork</h3>

<p align="center">
  <img src="https://github.com/fwd/nault/raw/master/.github/screen.png" alt="Nault Promo" />
</p>

Nault Pro is a non-custodial Nano wallet experience that can run fully local, or be self-hosted on Cloudflare for cloud-enabled features.

## Why Nault Pro Cloud (without giving up custody)

- **Non-custodial by design**: your wallet backup is stored as encrypted wallet data, not as plaintext keys.
- **Cloud convenience**: sync profile settings, access cloud-backed wallet data, and use API keys for programmatic actions.
- **Self-hosted control**: run your own Cloudflare Worker + D1 database so you control infrastructure and policy.
- **Local-first still supported**: if you prefer, use Nault Pro as a local wallet with browser storage and no cloud backup.

## Self-hosting on Cloudflare

The repository includes `cloud-wallet-worker` for running Nault Pro cloud services on Cloudflare Workers + D1.

1. Install worker dependencies:

```bash
cd cloud-wallet-worker
npm install
```

2. Create and wire a D1 database in `cloud-wallet-worker/wrangler.toml`.
3. Apply schema:

```bash
npm run db:migrate
```

4. Set required secret:

```bash
npx wrangler secret put JWT_SECRET
```

5. (Optional) Set `CORS_ORIGIN` and `RPC_URL` in `wrangler.toml`/Worker vars for your environment.
6. Deploy:

```bash
npm run deploy
```

## Changes

- ✅ Redesigned UI/UX
- ✅ Add Nano.to Usernames to send page.
- ✅ Add Nano.to Usernames to transactions.
- ✅ Add seamless OpenAI into Nault
- 🟨 Add Community Funding Page
- 🟨 Add eCommerce into Nault.Pro
- 🟨 Professional Security Audit
- 🟨 Nault.Pro Code Freeze & Formal Release

### License 

**MIT**

## Nano.to Support

- Email: support@nano.to
- Twitter: [@nano2dev](https://twitter.com/nano2dev)
- Mastodon: [Xno.Social](https://xno.social/@nano2dev) 
