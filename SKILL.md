---
name: ak
description: Use when answering questions about Apache Kafka — internals (brokers, partitions, replication, KRaft, consumer groups, transactions, exactly-once, tiered storage), components (Kafka Streams, Connect, Schema Registry), or fit assessment ("is Kafka right for this use case?"). Backed by a chapterized end-to-end reference.
---

# Apache Kafka — End-to-End Reference

A chapterized version of Stanislav Kozlovski's *What is Apache Kafka and how does it work?*. When the user's question maps to one of the topics below, read just that chapter and answer from it. Each chapter is self-contained (~3–11kb).

## Index

| Topic | Chapter |
| --- | --- |
| Why Kafka exists, history, the data integration problem | [chapters/00-intro.md](chapters/00-intro.md) |
| Log structure, records, topics, partitions, producer/consumer API, message order | [chapters/01-basics.md](chapters/01-basics.md) |
| Brokers, replication, leaders/followers, scalability | [chapters/02-distributed-system.md](chapters/02-distributed-system.md) |
| `__cluster_metadata`, controller quorum, KRaft consensus | [chapters/03-metadata-and-controllers.md](chapters/03-metadata-and-controllers.md) |
| Retention, replayability, tiered storage to S3 | [chapters/04-storage-features.md](chapters/04-storage-features.md) |
| Consumer groups, group coordinator, `__consumer_offsets` | [chapters/05-consumer-groups.md](chapters/05-consumer-groups.md) |
| Transactions, idempotency, exactly-once processing, edge cases | [chapters/06-transactions.md](chapters/06-transactions.md) |
| Kafka Streams, Schema Registry, Kafka Connect | [chapters/07-other-components.md](chapters/07-other-components.md) |
| When to use Kafka, when not to, the wider ecosystem | [chapters/08-conclusion.md](chapters/08-conclusion.md) |

## Usage

1. Match the user's question to one (or two adjacent) chapters above.
2. Read just that chapter — do not load the whole book up front.
3. Synthesize from it; cite specifics rather than restating verbatim.
4. For broad "explain Kafka" questions, walk chapters in order rather than dumping all of them at once.
