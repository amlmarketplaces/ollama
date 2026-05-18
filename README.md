# amlmarketplaces/ollama

Claude Code marketplace federating all `@amlplugins/ollama-*` plugins.

## Install

Add to your project's `.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "aml-ollama": {
      "source": { "source": "github", "repo": "amlmarketplaces/ollama" }
    }
  },
  "enabledPlugins": {
      "ollama-chat@aml-ollama": true,
      "ollama-embeddings@aml-ollama": true,
      "ollama-generate@aml-ollama": true,
      "ollama-models@aml-ollama": true
    }
}
```

Then launch Claude Code in the project. The marketplace is fetched from `amlmarketplaces/ollama`, cached under `~/.claude/plugins/cache/aml-ollama/`, and each enabled plugin is loaded from its `amlplugins` source repo.

## Plugins (4 total)

- `ollama-chat` — [@amlplugins/ollama-chat](https://github.com/amlplugins/ollama-chat)
- `ollama-embeddings` — [@amlplugins/ollama-embeddings](https://github.com/amlplugins/ollama-embeddings)
- `ollama-generate` — [@amlplugins/ollama-generate](https://github.com/amlplugins/ollama-generate)
- `ollama-models` — [@amlplugins/ollama-models](https://github.com/amlplugins/ollama-models)

## Related

- npm packages: `@amlplugins/ollama-*` published to GitHub Packages (`https://npm.pkg.github.com`).
- Aggregating parent: [`amlmarketplaces/aml`](https://github.com/amlmarketplaces/aml) — federates every `@amlplugins/*` plugin under a single marketplace.
- AML topology: see `.claude/rules/definitions/ageni.md` § "GitHub Topology" — this repository is a Tier-4 HUB-INSTANCE under the `amlmarketplaces/` Tier-3 HUB-ORGANIZATION.

> Built by `.claude/skills/aml/metateam/marketplace/test/cross-org-amlmarketplaces-batch.mjs`.
