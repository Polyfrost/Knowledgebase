---
description: Learn how to log performance issues using Spark.
---

# Profile a Spark log

Spark is a mod designed to record performance issues when playing Minecraft. It is able to track statistics like FPS, TPS, ping, and other stats that would affect your game performance, as well as track processes that Minecraft is using. This can be extremely helpful in narrowing down root causes of issues like stuttering, freezes, etc...

## Generating a Spark log

To generate a Spark log, you must download and install Spark as a mod. For versions 1.16.5-1.21, the official mod can be found [here](https://modrinth.com/mod/spark). For versions 1.8.9 and 1.12.2, there is no official Spark mod, but you may use [this fork made by nea89o](https://jitpack.io/com/github/romangraef/spark/spark-forge189/bde4ce2ff/spark-forge189-bde4ce2ff-mod.jar) for 1.8.9 and [this fork made by fonnymunkey](https://modrinth.com/mod/spark-unforged) for 1.12.2.

Then, run `/sparkc profiler start` and do activites that would cause the performance issue. Once finished you may stop logging with `/sparkc profiler stop` and share the link in chat to the person helping you.
