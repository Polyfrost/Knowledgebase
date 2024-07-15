# Failed to download

## TL;DR

* Check the [status page](https://status.polyfrost.cc/)
* Try using [OneConfig Bootstrap](https://modrinth.com/mod/oneconfig?hl=en-US)
* Check for any conflicting mods
* Check your antivirus
* Use a VPN

## Check Polyfrost status

While rare, our backend systems may be undergoing maintenance or experiencing an outage. Check the [status page](https://status.polyfrost.cc/) for any updates.

{% embed url="https://status.polyfrost.cc/" %}

## Launch bootstrap alone

Make sure none of your other mods are causing any incompatibilities by downloading & running [OneConfig Bootstrap](https://modrinth.com/mod/oneconfig?hl=en-US) by itself. This is an empty OneConfig install that doesn't depend on anything, and will only download OneConfig.

{% embed url="https://modrinth.com/mod/oneconfig?hl=en-US" %}

## Check for any conflicting mods

Some mods, including "Feather Client" and "Oringo," will not work with OneConfig's loader system. If using only the Bootstrap fixes the issue, check for those conflicting mods.

## Check antivirus

Since OneConfig downloads its core files from another server, some antiviruses will detect it as a form of malware & block it. McAfee, for example, used to detect our servers as a PUP.&#x20;

* Make sure all antivirus software is up-to-date
* Check that your antivirus isn't blocking OneConfig or other Polyfrost services

## Using a VPN

Occasionally, your ISP (internet service provider) or country may block access to certain websites such as GitHub or our own services. Using a [VPN](https://1.1.1.1/dns/) can allow you, to some extent circumvent these issues.

<details>

<summary>Countries known to cause issues</summary>

India

Iran

North Korea

China

</details>

## Download OneConfig directly

If you are still unable to download OneConfig, you may want to download it manually. Start by opening [this](https://api.polyfrost.org/oneconfig/1.8.9-forge). Here, highlight the first link (do not highlight the quotation marks), right click and press "go to https://...." ![image](https://github.com/user-attachments/assets/7b8bfd4f-0ab3-493e-ac32-fffec7a32dfb)
Upon clicking this, it will download a file, when that file is finished downloading, move it to `<your minecraft folder>/OneConfig`, if this folder does not exist create it. Once relocated, rename the jar file that you downloaded from the link to `OneConfig (1.8.9-forge).jar`. You can then try launching the game to see if OneConfig is present.
