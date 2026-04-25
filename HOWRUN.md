## Codex Direct Skill Install

```sh
$skill-installer stanislavkozlovski/what-is-apache-kafka
```

## Local Skill Install

```sh
ln -s "$(pwd)" ~/.agents/skills/apache-kafka
```

## Sync Plugin Bundle

```sh
./scripts/sync_codex_plugin.sh
```

## Local Plugin Test

```sh
codex plugin marketplace add .
```

## Published Plugin Install: Add Marketplace

```sh
codex plugin marketplace add stanislavkozlovski/what-is-apache-kafka --ref main --sparse .agents/plugins --sparse plugins
```

## Published Plugin Install: Install Plugin In Codex

```text
/plugins
```
