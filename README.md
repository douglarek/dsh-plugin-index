# dsh-plugin-index

A custom [DSH plugin market](https://github.com/deepseek-ai/deepseek-harness) index.

Index URL:

```
https://raw.githubusercontent.com/douglarek/dsh-plugin-index/main/index.json
```

Current entries:

- `dsh-cpa-search-provider` — CPA Responses web search and fetch provider.
- `@douglarek/dsh-statistics` — token usage, cost, budget, and CPU statistics.
- `dsh-memory` — cross-session persistent memory.
- `@douglarek/dsh-subagent-agy` — Antigravity (agy) ACP subagent.

## Use it in DSH

1. Enable the **Custom plugin indexes** bundle (`@deepseek-ai/dsh-experimental-plugin-market-bundle`) in **Plugins**.
2. Open **Plugins → Discover**.
3. Paste the index URL above and click **Add**.
4. Install or update `dsh-cpa-search-provider` from the index.

## Update an entry

When a plugin publishes a new version, add a new object to `plugins[].versions` with:

- the exact `version`,
- its `publishTimestamp` in Unix seconds,
- a `source` pinned to the release commit (`type: "git"`, `url`, full 40-hex `commit`).

The index is validated against the format-1 schema by
`@deepseek-ai/dsh-plugin-market-index`.
