# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) presets for the homelab
repositories.

| Preset | Use in | Contents |
|---|---|---|
| `github>pixil98/renovate-config` | every homelab repository | `config:recommended` |
| `github>pixil98/renovate-config:kubernetes` | Flux and Kubernetes manifest repositories | The Flux, Kubernetes and CNPG `imageName` managers, image digest pinning, and one grouped PR for digest-only updates |

A repository's `renovate.json` extends the presets it needs and keeps only the
rules that are specific to it:

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": [
    "github>pixil98/renovate-config",
    "github>pixil98/renovate-config:kubernetes"
  ]
}
```

Renovate reads presets from this repository's default branch, so changes here
apply to every repository on its next run.
