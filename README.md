<div align="center">

# what-is-apache-kafka

The best single-resource explanation of Apache Kafka out there. (34 minute read / ~11,244 tokens)

<br>

| Action | Link |
| --- | --- |
| What is this? | [The What](#the-what) |
| Read the book | [Chapters](#chapters) |
| Install with NPX | [NPX Install](#npx-install) |
| Install in Claude Code | [Claude Install](#install-in-claude-code) |
| Install in Codex as a raw skill | [Codex Skill Install](#install-in-openai-codex-as-a-raw-skill) |
| Install in Codex as a plugin | [Codex Plugin Install](#install-as-a-codex-plugin) |

<br>

</div>

# The What

There are a thousand "What is Kafka" explanations out there, but very few are good, and almost none are thorough enough. The very thorough ones are whole books consisting of ~487 pages (~190k tokens / 600 minute / 10 hour reads), which is too much for 90% of people out there.

This repo is a simple markdown-friendly chapterized version of the article [*What is Apache Kafka and how does it work?*](https://stanislavkozlovski.medium.com/what-is-apache-kafka-and-how-does-it-work-16023aa2efee).

# Chapters

1. [Introduction](chapters/00-intro.md) — why Kafka exists, history, the data integration problem
2. [The Basics](chapters/01-basics.md) — log data structure, records, topics, partitions, producer/consumer API, message order
3. [Kafka as a Distributed System](chapters/02-distributed-system.md) — brokers, replication, leaders/followers, scalability
4. [Metadata & Controllers](chapters/03-metadata-and-controllers.md) — `__cluster_metadata`, controller quorum, KRaft consensus
5. [Storage Features](chapters/04-storage-features.md) — retention, replayability, tiered storage to S3
6. [Consumer Groups](chapters/05-consumer-groups.md) — read parallelization, group coordinator, `__consumer_offsets`
7. [Transactions & Exactly-Once Processing](chapters/06-transactions.md) — atomic multi-partition writes, idempotency, edge cases
8. [Other Kafka Components](chapters/07-other-components.md) — Streams, Schema Registry, Connect
9. [Conclusion](chapters/08-conclusion.md) — when to use Kafka, when not to, the wider ecosystem

# Install as an Agent Skill

The repo root *is* the skill folder — same `SKILL.md` works for both Claude Code and OpenAI Codex; only the install path differs. Explicit mention name: `$ak`.

## NPX Install

If you use [skills.sh](https://skills.sh/), install it with:

```sh
npx skills add stanislavkozlovski/what-is-apache-kafka
```

## Install in Claude Code

Symlink (or clone) into `~/.claude/skills/`:

```sh
ln -s "$(pwd)" ~/.claude/skills/apache-kafka
```
or:
```sh
git clone https://github.com/stanislavkozlovski/what-is-apache-kafka.git ~/.claude/skills/apache-kafka
```

## Install in OpenAI Codex

Choose one path:

- Want `$ak` available directly in Codex: use the skill install path below
- Want to install it as a Codex plugin: use the plugin path below

### Option A: Direct Skill Install

Symlink (or clone) into `~/.agents/skills/`:

```sh
ln -s "$(pwd)" ~/.agents/skills/apache-kafka
```
or:

```sh
git clone https://github.com/stanislavkozlovski/what-is-apache-kafka.git  ~/.agents/skills/apache-kafka
```

or:

```sh
# inside Codex
$skill-installer stanislavkozlovski/what-is-apache-kafka
```

This path is the simplest one if your goal is just to use `$ak`.

The skill triggers on Kafka questions — internals (brokers, partitions, KRaft, replication, consumer groups, transactions, tiered storage), components (Streams, Connect, Schema Registry), or fit assessment ("is Kafka right for X?"). On trigger, the agent reads the relevant chapter and answers from it instead of guessing.

Try it with:

```text
$ak explain Kafka consumer groups
```

### Option B: Codex Plugin Install

We also have a Codex plugin scaffold:

- marketplace: `.agents/plugins/marketplace.json`
- plugin: `plugins/apache-kafka/`
- bundled skill name: `$ak`

Step 1: add the marketplace from GitHub:

```sh
codex plugin marketplace add stanislavkozlovski/what-is-apache-kafka --ref main --sparse .agents/plugins --sparse plugins
```

Step 2: inside Codex, install the plugin from the plugin browser:

```text
/plugins
```

Then open the `what-is-apache-kafka` marketplace, open `Apache Kafka`, and select `Install plugin`.

Important: step 1 only adds the marketplace. It does not install the plugin, and it does not make `$ak` available by itself.

If your goal is only to get `$ak`, use Option A instead:

```sh
# inside Codex
$skill-installer stanislavkozlovski/what-is-apache-kafka
```

## License And Policies

- License: [Apache 2.0](LICENSE)
- Privacy: [PRIVACY.md](PRIVACY.md)
- Terms: [TERMS.md](TERMS.md)
