---
description: What type of log do I provide?
---

# Types of logs

## TL;DR

* latest.log is the record of what happens in the game.
* Crash reports are for when the game crashed.
* Spark logs are for if you experience performance issues.
* hs_err_pid logs are for when the JVM (Java Virtual Machine) crashes.
* Upload your logs to mclo.gs to have your personal info filtered out.

## latest.log

This log is the one that is generated every time the game is launched. This log basically records what happens in the game session, and is usually useful for non-crash related issues.

This log is found in `<your Minecraft folder>/logs/` and is the file literally named `latest` or `latest.log`. Any other file there is not usually helpful.

## Crash reports

This report is generated when a crash occurs (with certain exceptions). This is the most helpful log as it contains details that are very helpful in diagnosing the cause of the issue.

This log is generated in `<your Minecraft folder>/crash-reports` and is the file that is named `crash-(insert crash date and time here)`. Similar to above it may also have `.log` appended to it, both are the same.

## Spark logs

Spark logs, also known as Spark profiles, are logs that measure the performance of your game. This includes TPS, FPS, ping (ms) and more, as well as a breakdown of Minecraft processes that are being loaded. This log is helpful if you find that you are experiencing performance issues.

You can find instructions for using Spark [here](../diagnosing_issues/spark.md)

## hs_err_pid logs

These weird-looking log names are generated after a Java Virtual Machine (JVM) crash. This signals that something *could* be really wrong for it to crash like this. Because of this, it's good to do the following first:

* Check that your drivers are up-to-date.
* Check that your hardware isn't causing issues

If after doing that the JVM crash still occurs, locate the log in your Minecraft folder (it may also appear inside `logs` or `crash-reports`) and open it.

If you just crashed and the log appeared, __DO NOT SEND THE ENTIRE LOG!__ This log contains sensitive information about your account that someone could use to hijack your account. Instead, simply scroll to the top and send the lines that start with `#` to the person helping you. This portion is the safe part of your log for now and the rest of the log shouldn't be needed.

## Sending your logs

SkyAnswers, our own bot which handles crash logs, uploads your logs sent in the Polyfrost/SkyClient discords to [mclo.gs](https://mclo.gs/), a paste service designed for Minecraft logs and has a personal information filter, which should filter out computer usernames, IP addresses, and other information considered sensitive. Simply sending your logs in Discord in a private support channel should keep you safe from accidentally leaking your information.
