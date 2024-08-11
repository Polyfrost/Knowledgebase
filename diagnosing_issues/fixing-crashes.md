---
description: Helpful information for diagnosing crashes.
---

# Fixing crashes

## TL;DR

* Locate the correct log to get help faster.
* Resend your log if you keep crashing.
* Not all mods in the stacktrace are the cause.
* Perform a binary search if logs are unclear.

***

## Exit codes

Different Minecraft exit codes have useful information located elsewhere. Click below to find the relevant log for your exit code.

<details>

<summary>Exit codes and their corresponding logs</summary>

* Long negative exit codes (e.g. -8679432150): These are usually JVM crashes. These logs should be located in `.minecraft/hs_err_pid_(random numbers).log`. If you just crashed and this log was made afterwards, DO NOT SEND THE ENTIRE LOG as it can contain information that could be used to hijack your Minecraft account. Instead, copy the lines at the beginning that start with `#`.
* Exit Code 0 (or any crash that doesn't have a `View Crash Log` button in the default launcher): The relevant log should be located at `.minecraft/logs/latest` or `.minecraft/logs/latest.log`.
* Any other crashes: The crash report should be located at `.minecraft/crash-reports/crash-(current date and time).log`.

Once the information has been copied, paste it into the [mclo.gs service](https://mclo.gs/) and give the link to the person helping you.

</details>

## Multiple crashes

If you are experiencing a crash, removed the suspected cause, and you are still crashing, you may now have a different issue.
This is usually indicated by the stacktrace in your crashlog looking different. In this case, you should always resend your crashlog to whoever is helping you! This way, they will be able to see the new log.

## Weird mods showing in crashes

Some mods load themselves into the game in a different way, such as Essential. This can cause them to appear inside every crashlog generated. If such a mod is present, then they should appear towards the bottom of the stacktrace if they aren't the cause of the crash. If they appear high up, they could be the (or a part of the) cause of the problem.