<div align="center">

# what-is-apache-kafka

The best single-resource explanation of Apache Kafka out there. (34 minute read / ~11,244 tokens)

<br>

| Action | Link |
| --- | --- |
| What is this? | [The What](#the-what) |
| Read the book | [Chapters](#chapters) |
| Regenerate images | [Scripts](#scripts) |
| Original article | [Source](#source) |

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

