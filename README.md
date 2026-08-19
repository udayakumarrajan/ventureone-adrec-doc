# VentureOne · ADREC API Reference

Mintlify documentation of the APIs and data fields VentureOne requires from **ADREC** (Abu Dhabi Real Estate Centre) to verify ownership, check eligibility, transfer title into an SPV, and keep a tokenized offering in sync with the registry.

## Run locally

```bash
cd adrec-api-docs
npx mintlify dev
```

Then open http://localhost:3000.

## Structure

| Path | Contents |
| --- | --- |
| `docs.json` | Mintlify config, navigation, black-and-white theme |
| `introduction/` | Overview, scope & reconciliation, conventions, security & encryption |
| `endpoints/` | The 19 endpoints + change webhook |
| `models/` | Shared schemas, enumerations, `assets`/`offering` mapping |

## Notes

- **Scope** is reconciled from three sources — the API checklist (`ADREC APIs.xlsx`), the earlier property-only draft, and the platform data model. See `introduction/scope-and-reconciliation.mdx` for consolidations, conflicts, and open gaps.
- **Encryption**: PII payloads use asymmetric JWE (`RSA-OAEP-256` + `A256GCM`); whole-payload by default. See `introduction/security.mdx`.
- Endpoint paths, auth, and certificates are **placeholders pending ADREC's contract**.
