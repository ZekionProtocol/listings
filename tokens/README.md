# Token catalog

Approved token metadata lands here **after** an Issue is labeled `approved`.

## Entry shape (v1)

One JSON file per `tokenKey` (stable across chains), e.g. `USDT.json`:

```json
{
  "tokenKey": "USDT",
  "symbol": "USDT",
  "name": "Tether USD",
  "decimals": 6,
  "description": "USD-pegged stablecoin …",
  "logoURI": "https://…/usdt.png",
  "website": "https://…",
  "deployments": [
    {
      "chain": "bsc",
      "slip44": 714,
      "address": "0x…"
    }
  ],
  "listingIssue": 1
}
```

Required for a complete listing: `name`, `symbol`, `tokenKey`, `decimals`, `logoURI`, `website`, at least one `deployments[].address`, and `listingIssue`.

Field notes:

- `tokenKey` must match the on-chain HubConfig / Vault key operators will configure.
- `decimals` must match the ERC-20/TRC-20 contract.
- `logoURI` must be a publicly reachable HTTPS image (square PNG preferred).
- `listingIssue` is the GitHub Issue number in this repo.

Do not invent keys that collide with existing protocol assets without maintainer approval.
