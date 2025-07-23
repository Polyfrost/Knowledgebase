---
description: Learn how to log performance issues using Spark.
---

# Spark logs

Spark is a mod designed to record performance issues when playing Minecraft. It is able to track statistics like FPS, TPS, ping, and other stats that would affect your game performance, as well as track processes that Minecraft is using. This can be extremely helpful in narrowing down root causes of issues like stuttering, freezes, etc...

## Generating a Spark log

To generate a Spark log, you must download and install Spark as a mod. For versions 1.16.5-1.21, the official mod can be found [here](https://modrinth.com/mod/spark). For 1.8.9, there is no official Spark mod, but you may use [this fork made by nea89o](https://jitpack.io/com/github/romangraef/spark/spark-forge189/bde4ce2ff/spark-forge189-bde4ce2ff-mod.jar).

For performance stuff (memory issues might also show here):

Run `/sparkc profiler start` and do activites that would cause the performance issue. Once finished you may stop logging with `/sparkc profiler stop` and share the link in chat to the person helping you.

For memory stuff :

Do the same, except use `/sparkc heapsummary` instead.

## Before reading it:

Remember that:

* In the game of improving FPS, we are looking into micro-optimizations. Keep in mind that a single frame is expected to take mere milliseconds.&#x20;
* However, sometimes, calls are necessary. We can't not draw anything, although it would increase FPS infinitely, or else the user wouldn't see anything (obviously).
* If you don't know Java, the chances that you misinterpret the log is SUPER high, so please be respectful to any mod authors you report to!

## Reading it

Get the link and open it. Click on the "flat" view, this will allow you to see the spark log sorted from taking up the most time to taking up the least time.

![](<../.gitbook/assets/Screenshot 2025-07-24 at 2.49.40 AM.png>)

You can also tweak the `Sort Mode` if you like, it could declutter the tree for you. Setting it to `Self Time` will order it according to "the time spent executing code within the method," which can be more useful.

<figure><img src="../.gitbook/assets/Screenshot 2025-07-24 at 2.54.37 AM.png" alt=""><figcaption></figcaption></figure>

From there, expand the tree on the bottom of the page:

<figure><img src="../.gitbook/assets/Screenshot 2025-07-24 at 2.53.39 AM.png" alt=""><figcaption></figcaption></figure>

And you'll see this tree.

<figure><img src="../.gitbook/assets/Screenshot 2025-07-24 at 2.54.21 AM.png" alt=""><figcaption></figcaption></figure>

As a general rule, you can ignore any typical method stemming from `sun.reflect`, `java` (both are java-internal packages), `org.lwjgl`, `net.minecraft(forge)`, `net.fabricmc`, etc. These are very widely used libraries and if there was a blatant performance issue in them, we have a much bigger problem at hand.

To find performance issues, you're more likely to find them in actual mods, like SkyHanni in that particular log, taking up a lot of percentage points. You can click on them to expand their trees and look at what methods they're calling from within the method to have such a high impact on performance.

<figure><img src="../.gitbook/assets/Screenshot 2025-07-24 at 3.02.52 AM.png" alt=""><figcaption></figcaption></figure>

Continuously expanding the tree leads to this. What is going on here??? To a person unfamiliar with Java, this is very jarring.

In this particular case, a spam of does not indicate it is a problem, rather we need to look into each one and see what actual calls are causing issues.

In this case, the lambda spam is actually SkyHanni dynamically calling methods via MethodHandles. Theoretically, it should be as fast as normal calls, so there's nothing to worry about. It just looks a bit weird to look at.

**TLDR;** if you see anything weird like this just continue searching and expand the top option to see what's happening.

<figure><img src="../.gitbook/assets/Screenshot 2025-07-24 at 3.07.14 AM.png" alt=""><figcaption></figcaption></figure>

Expanding until we have nothing else to expand, we find that 2.38% of the thread is being taken up by this single call to `String`. Keep in mind, the thread runs tens of thousands of methods every frame, and so a _single_ call taking up this much is crazy.

You can either tell the person to reproduce without it or just directly go to the mod author about the issue.
