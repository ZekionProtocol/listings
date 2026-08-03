# Zekion Listings

Public registry for **third-party Tokens** and **DApps** on Zekion.

Do **not** open listing requests on `monorepo` or other product repos. Use this repository only.

## Required application fields

| Token | DApp |
|-------|------|
| Website | Website / homepage |
| Description | Description |
| Token display name + symbol | **App display name** |
| Contract address(es) per chain | Web app URL |
| **Token icon** (HTTPS logo URL) | **App icon** (HTTPS logo URL) |

Optional extras (contacts, security email, test notes, deep links) are still collected in the Issue forms.

## How to apply

| What | Open an Issue |
|------|----------------|
| List a **Token** | [Token listing template](https://github.com/ZekionProtocol/listings/issues/new?template=listing-token.yml) |
| List a **DApp** (Discover whitelist) | [DApp listing template](https://github.com/ZekionProtocol/listings/issues/new?template=listing-dapp.yml) |

### After approval

1. Open a **Pull Request** that only changes files under `tokens/` or `discover/`.
2. Link the Issue (`Closes #N`).
3. Maintainers merge the catalog, run on-chain `configureToken` when needed, and sync into the wallet release.

Merging a PR **does not** by itself enable an asset on-chain. Token support requires operator configuration on Vault / HubConfig.

## Layout

```text
discover/whitelist.json   # Discover tiles shown in the Zekion wallet
tokens/                   # Approved token metadata (added via PR)
docs/MAINTAINER.md        # Maintainer checklist
```

## Docs

Product documentation (deeplinks, full walkthroughs) lives in the Zekion docs site. This repo is intake + catalog only.

## License

Catalog metadata contributed here is licensed under MIT (see `LICENSE`).
