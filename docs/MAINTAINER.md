# Maintainer checklist

## Triage

1. Verify contact and (for tokens) contract addresses on explorers.
2. Label `needs-info` / `approved` / `rejected`.
3. For tokens, schedule on-chain configure (Vault + HubConfig) — see contracts HubConfig ops docs in the monorepo / zekion-contracts.

## After approval

1. Ensure a catalog PR exists (`discover/whitelist.json` or `tokens/*.json`).
2. Merge PR.
3. Sync into product trees:
   - Wallet Discover: `zekion/wallet/packages/wallet-ui/src/discover/defaultWhitelist.json`
   - Token pickers / chain catalogs as applicable
4. Comment on the Issue with: catalog commit, configure tx/refs (if any), client release target.
5. Close when the client build that includes the catalog has shipped (or note “catalog merged; client pending”).

## Labels

Suggested: `listing`, `token`, `dapp`, `needs-triage`, `needs-info`, `approved`, `rejected`, `on-chain-pending`, `synced`.
