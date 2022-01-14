---
layout: page
title:  "Download ossia score"

permalink: /score/download.html
category: site-score
score_version: 3.0.1
---

Download the latest stable release __ossia score v{{page.score_version}}__:
<p style="display: flex; justify-content: center;align-content:space-evenly;" align="center">
<a href="https://github.com/ossia/score/releases/download/v{{page.score_version}}/ossia.score-{{page.score_version}}-win64.exe" target="_blank" class="page-button download-page"><img src="../assets/windows_logo_2012-Black.svg" height="80px"/>Windows 7/8/10/11</a>
<a href="https://github.com/ossia/score/releases/download/v{{page.score_version}}/ossia.score-{{page.score_version}}-macOS.dmg"  target="_blank" class="page-button download-page" ><img src="../assets/apple_logo_black.svg" height="80px"/>Mac OS<br/>10.14 and later</a>
<a href="https://github.com/ossia/score/releases/download/v{{page.score_version}}/ossia.score-{{page.score_version}}-linux-amd64.AppImage" target="_blank" class="page-button download-page"><img src="../assets/Linux_Platform.svg" height="80px"/>Linux</a>
<a href="https://github.com/ossia/score/releases/download/v{{page.score_version}}/ossia.score-{{page.score_version}}-rpi-aarch32.tar.gz" target="_blank" class="page-button download-page"><img src="../assets/Pi_Platform.svg" height="80px"/>Raspberry Pi</a>
</p>
See the <a href="https://github.com/ossia/score/releases/latest" target="_blank">change log</a> for the latest release.

## Supported platforms

The releases are 64-bit on all desktop operating systems, 32-bit for Raspberry Pi. There are no native M1 macOS builds yet but score has been tested to work in Rosetta.

### Minimal requirements

* 800 MHz CPU, 512MB of RAM (but you won't make very large scores).
* For graphics, a GPU which supports at least OpenGL 3.2, Vulkan, Direct3D11 or Metal.
  
### Windows

* Recommended: Windows 10. Must be at least Windows 7 with all system updates installed.
* *score* and *libossia* use Bonjour for the OSCQuery automatic discovery feature.
  This means that on Windows, you must install the [Bonjour Print Services](https://support.apple.com/kb/dl999?locale=en_US) for this to work.

### macOS

* macOS: must be at least Mojave (10.14).

### Linux (Desktop)

* All Linux distributions from at least mid-2018 should be supported.
  * The packages are built on CentOS 8.
  * Ubuntu 18.10+
  * Debian Buster (10) / Bullseye (11) / ...  
  * Fedora 29+
  * Your system must have at least glibc-2.28, as well as X11, ALSA, libGL, librt, libdbus, libGL, libEGL (those packages are present on any relevant desktop distribution ; if you use Debian, Ubuntu, Fedora, OpenSUSE, ArchLinux or anything like those it will work fine).
  * Either JACK or Pipewire for audio, and Avahi for Bonjour support are recommended.
  * libbluez may be necessary to use Wiimotes (which go through Bluetooth).
  * Wayland support is still experimental, in particular on GNOME-based desktops.

* To integrate the AppImage into your system, please follow
  https://github.com/AppImage/awesome-appimage/#desktop-integration

### Linux (Raspberry Pi, embedded...)

* Read the [documentation](https://ossia.io/score-docs/in-depth/embedded.html) before running score on a Pi.

### Web

* Check out our experimental WebAssembly build: [right here](https://ossia.io/score-web)!

## Source code

The source code for the latest release can be downloaded from here:
* Latest release's <a href="https://github.com/ossia/score/releases/download/v{{page.score_version}}/ossia.score-{{page.score_version}}-src.tar.xz">source code</a>
* Latest release's <a href="https://github.com/ossia/score/releases/download/v{{page.score_version}}/ossia.score-{{page.score_version}}-src.tar.xz.asc">source code signature</a>
* Alternatively, you can fetch the latest source code <a href="https://github.com/ossia/score">directly from Github</a>
