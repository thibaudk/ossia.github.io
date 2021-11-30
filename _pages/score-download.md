---
layout: page
title:  "Download ossia score"

permalink: /score/download.html
category: site-score
score_version: 3.0.0-rc5
---

Download the latest beta release __ossia score v{{page.score_version}}__:
<p style="display: flex; justify-content: center;align-content:space-evenly;" align="center">
<a href="https://github.com/ossia/score/releases/download/v{{page.score_version}}/ossia.score-{{page.score_version}}-win64.exe" target="_blank" class="page-button download-page"><img src="../assets/windows_logo_2012-Black.svg" height="80px"/>Windows 10</a>
<a href="https://github.com/ossia/score/releases/download/v{{page.score_version}}/ossia.score-{{page.score_version}}-macOS.dmg"  target="_blank" class="page-button download-page" ><img src="../assets/apple_logo_black.svg" height="80px"/>Mac OS<br/>10.14 and later</a>
<a href="https://github.com/ossia/score/releases/download/v{{page.score_version}}/ossia.score-{{page.score_version}}-linux-amd64.AppImage" target="_blank" class="page-button download-page"><img src="../assets/Linux_Platform.svg" height="80px"/>Linux</a>
</p>
See the <a href="https://github.com/ossia/score/releases/latest" target="_blank">change log</a> for the latest release.

## Supported platforms

The releases are 64-bit on all desktop operating systems.

### Windows

* Must be at least Windows 10.
* *score* and *libossia* use Bonjour for the OSCQuery automatic discovery feature.
  This means that on Windows, you must install the [Bonjour Print Services](https://support.apple.com/kb/dl999?locale=en_US) for this to work.

### macOS

* macOS: must be at least Mojave (10.14).

### Linux (Desktop)

* All Linux distributions from at least 2015-era should be supported.
  * The packages are built on CentOS 7.
  * Your system must have at least glibc-2.17, as well as X11, ALSA, libGL, librt, libdbus.
  * Either JACK or Pipewire for audio, and Avahi for Bonjour support are recommended.
  * libbluez may be necessary to use Wiimotes (which go through Bluetooth).
  * Wayland support is still experimental.

* To integrate the AppImage into your system, please follow
  https://github.com/AppImage/awesome-appimage/#desktop-integration

### Linux (Raspberry Pi, embedded...)

* Raspberry Pi 3/4 (experimental, AArch32 build): [available here](https://github.com/ossia/score/releases/download/v3.0.0-rc5/ossia.score-3.0.0-rc5-rpi-aarch32.zip)!

* Read the [documentation](https://ossia.io/score-docs/in-depth/embedded.html) before running score on a Pi.

### Web

* Check out our experimental WebAssembly build: [right here](https://ossia.io/score-web)!

## Source code

The source code for the latest release can be downloaded from here:
* Latest release's <a href="https://github.com/ossia/score/releases/download/v{{page.score_version}}/ossia.score-{{page.score_version}}-src.tar.xz">source code</a>
* Latest release's <a href="https://github.com/ossia/score/releases/download/v{{page.score_version}}/ossia.score-{{page.score_version}}-src.tar.xz.asc">source code signature</a>
* Alternatively, you can fetch the latest source code <a href="https://github.com/ossia/score">directly from Github</a>
