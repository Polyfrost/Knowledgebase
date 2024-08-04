# Screen not appearing / White background

## TL;DR

* Disable Fast Render
* Do not use "PojavLauncher"

## Disable 'Fast Render' or 'Anti Aliasing'

Although this should be fixed, issues may still occur while using these features. This is because NanoVG (the tool we use for rendering our GUIs) use "framebuffers", which these features disable.

<figure><img src="../.gitbook/assets/Fast Render Screenshot.png" alt=""><figcaption><p>Located in "Options -> Video Settings -> Performance." To disable, click the "Fast Render" button.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Anti-Aliasing Screenshot.png" alt=""><figcaption><p>Located in "Options -> Video Settings -> Quality." To disable, drag "Antialiasing" to the left and <strong>restart your game</strong>.</p></figcaption></figure>

## Do not use PojavLauncher

PojavLauncher is a launcher for Android and iOS phones. This will not work with OneConfig, although a fix is in the works with the developers.
