---
description: How to do a binary search (aka a thanos search)
---

# Binary search

One useful way to identify the cause of a crash is to perform what's known as a "binary search" (you may also know it as thanos searching). The idea is to halve your mod count to identify the issue faster than testing mods one by one.\
This is a great way to figure out the cause of the crash even if the log isn't helpful.

<details>

<summary>How to binary search</summary>

1. Remove all your mods. If it still crashes, this is possibly an issue with Minecraft itself, in which case inform this to your support person.
2. If it works, add back half of your original mod count.
3. If it works, swap to the other half. If it doesn't work, halve the mod count again and test.
4. Repeat step 3 until the problem no longer exists/you have identified the problematic mod.

</details>
