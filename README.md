# Spanish Intake Skill — Claude Desktop Plugin

A Claude Desktop plugin for solo and small-firm attorneys. One skill (`/spanish-intake`): Conducts bilingual (English/Spanish) client intake and communication: turns Spanish-language intake notes or a voicemail transcript into a structured English intake summary for the file, and turns an English draft communication into a natural Spanish version — flagging any ambiguous translation for the attorney's confirmation rather than guessing.

Distributed free by [Protomated](https://protomated.com).

---

## Repo layout

```text
plugin/           Installable plugin (packaged into .zip)
  .claude-plugin/plugin.json   Identity manifest
  .mcp.json                    Empty — no connector required
  skills/spanish-intake/
    SKILL.md                   The single skill

scripts/
  validate-plugin.mjs          Validates plugin/ structure before packing

.github/workflows/
  validate.yml     Runs on every push/PR — validates plugin structure
  release.yml      Runs on vX.Y.Z tags — builds, checksums, and publishes a GitHub Release
```

---

## Skill

| Skill | What it does |
|---|---|
| `/spanish-intake` | Conducts bilingual (English/Spanish) client intake and communication: turns Spanish-language intake notes or a voicemail transcript into a structured English intake summary for the file, and turns an English draft communication into a natural Spanish version — flagging any ambiguous translation for the attorney's confirmation rather than guessing. |

---

## Development

```bash
npm run validate   # validate plugin/ structure
npm run build      # validate → pack → checksum
npm run release    # build + gh release create (requires gh CLI + repo write access)
```

---

## Part of the Protomated Plugin Marketplace

This plugin also ships via the [Protomated plugin marketplace](https://github.com/protomated/protomated-plugins-official) (git-native install, no zip needed) — install this repo's zip release if you want a pinned version instead.

## License

Apache 2.0. See [LICENSE](LICENSE).
