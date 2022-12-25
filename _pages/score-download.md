---
layout: download-page
title:  "Download ossia score"

permalink: /score/download.html
category: site-score
---

<h2> Support us </h2>
We sell score on the Microsoft store as a way to get financial support to ensure continued development so please consider buying it there, or funding us through <a href="https://opencollective.com/ossia">OpenCollective</a> or <a href="https://github.com/sponsors/jcelerier">Github Sponsors</a>!

## Download ossia score v{{site.score_version}}
### Released on {{site.score_released_date}}
<p class="download-page-layout" align="center">
<a id="winstore" href="https://apps.microsoft.com/store/detail/ossia-score/9NGT21X5XB19" target="_blank" class="page-button download-page"><img src="../assets/microsoft-store.svg" height="80px"/> Microsoft Store</a>
<a id="win" href="https://github.com/ossia/score/releases/download/v{{site.score_version}}/ossia.score-{{site.score_version}}-win64.exe" class="page-button download-page"><img src="../assets/windows_logo_2012-Black.svg" height="80px"/> Windows</a>
<a id="osx" href="https://github.com/ossia/score/releases/download/v{{site.score_version}}/ossia.score-{{site.score_version}}-macOS.dmg" class="page-button download-page" ><img src="../assets/apple_logo_black.svg" height="60px"/>macOS 10.13 and later</a>
<a id="linux" href="https://github.com/ossia/score/releases/download/v{{site.score_version}}/ossia.score-{{site.score_version}}-linux-amd64.AppImage" class="page-button download-page"><img src="../assets/Linux_Platform.svg" height="80px"/>Linux</a>
<a id="pi" href="https://github.com/ossia/score/releases/download/v{{site.score_version}}/ossia.score-{{site.score_version}}-rpi-aarch32.tar.gz" class="page-button download-page"><img src="../assets/Pi_Platform.svg" height="80px"/>Raspberry Pi</a>
</p>


Take a look at the <a href="https://github.com/ossia/score/releases/latest" target="_blank">change log</a> for the latest release information !

## All Supported platforms

The releases are 64-bit on all desktop operating systems, 32-bit for Raspberry Pi. There are no native M1 macOS builds yet but score has been tested to work in Rosetta.

<h2 type="button" class="collapsible" > All platforms </h2>
<div class="collapsible-content">
<p class="download-page-layout" align="center">
<a href="https://apps.microsoft.com/store/detail/ossia-score/9NGT21X5XB19" target="_blank" class="page-button download-page"><img src="../assets/microsoft-store.svg" height="80px"/>Microsoft Store</a>
<a href="https://github.com/ossia/score/releases/download/v{{site.score_version}}/ossia.score-{{site.score_version}}-macOS.dmg" class="page-button download-page" ><img src="../assets/apple_logo_black.svg" height="80px"/>macOS</a>
<a href="https://github.com/ossia/score/releases/download/v{{site.score_version}}/ossia.score-{{site.score_version}}-linux-amd64.AppImage" class="page-button download-page"><img src="../assets/Linux_Platform.svg" height="80px"/>Linux</a>
<a href="https://github.com/ossia/score/releases/download/v{{site.score_version}}/ossia.score-{{site.score_version}}-rpi-aarch32.tar.gz" class="page-button download-page"><img src="../assets/Pi_Platform.svg" height="80px"/>Raspberry Pi</a>
<a href="https://github.com/ossia/score/releases/download/v{{site.score_version}}/ossia.score-{{site.score_version}}-win64.exe" class="page-button download-page"><img src="../assets/windows_logo_2012-Black.svg" height="80px"/>Windows</a>
<a href="https://ossia.io/score-web" target="_blank" class="page-button download-page"><img src="../assets/web.png" height="80px"/>WebAssembly</a>
</p>

<p style="display: flex; justify-content: center;align-content:space-evenly;" align="center">

</p>
</div>

<h2 type="button" class="collapsible" > Minimal requirements </h2>
<div class="collapsible-content">
<ul>
<li> 800 MHz CPU, 512MB of RAM (but you won't make very large scores). </li>
<li> For graphics, a GPU which supports at least OpenGL 3.2, Vulkan, Direct3D11 or Metal. </li>
</ul>
</div>

<h2 type="button" class="collapsible" > Windows </h2>
<div class="collapsible-content">
<ul>
<li> Recommended: Windows 10. Must be at least Windows 7 with all system updates installed. </li>
<li> <i>score</i> and *libossia* use Bonjour for the OSCQuery automatic discovery feature.
  This means that on Windows, you must install the <a href="https://support.apple.com/kb/dl999?locale=en_US">Bonjour Print Services</a> for this to work. </li>
</ul>
</div>

<h2 type="button" class="collapsible" > macOS </h2>
<div class="collapsible-content">
Must be at least High Sierra (10.13).
</div>

<h2 type="button" class="collapsible" > Linux (Desktop) </h2>
<div class="collapsible-content">

<p> To integrate the AppImage into your system, please follow: <br>
&nbsp;&nbsp;&nbsp;&nbsp;<a>https://github.com/AppImage/awesome-appimage/#desktop-integration</a>
</p>

All Linux distributions from at least mid-2018 should be supported:
<ul>
<li>The packages are built on CentOS 8.</li>
<li>Ubuntu 18.10+ </li>
<li>Debian Buster (10) / Bullseye (11) / ...  </li>
<li>Fedora 29+</li>
<li>Your system must have at least glibc-2.28, as well as X11, ALSA, libGL, librt, libdbus, libGL, libEGL. Those packages are present on any relevant desktop distribution ; if you use Debian, Ubuntu, Fedora, OpenSUSE, ArchLinux or anything like those it will work fine.</li>
<li>Either JACK or Pipewire for audio, and Avahi for Bonjour support are recommended.</li>
<li>libbluez may be necessary to use Wiimotes (which go through Bluetooth).</li>
<li>Wayland support is still experimental, in particular on GNOME-based desktops.</li>
</ul>
</div>

<h2 type="button" class="collapsible" > Ubuntu Jammy (22.04)</h2>
<div class="collapsible-content">
Important note for Ubuntu Jammy (22.04): *libfuse2* must be installed as it is necessary for running AppImages:

<pre>
sudo add-apt-repository universe
sudo apt install libfuse2
</pre>
</div>

<h2 type="button" class="collapsible" > Linux (Raspberry Pi, embedded...) </h2>
<div class="collapsible-content">
Read the <a href="https://ossia.io/score-docs/in-depth/embedded.html">documentation</a> before running score on a Pi.
</div>

## Source code

The source code for the latest release can be downloaded from here:
* Latest release's <a href="https://github.com/ossia/score/releases/download/v{{site.score_version}}/ossia.score-{{site.score_version}}-src.tar.xz">source code</a>
* Latest release's <a href="https://github.com/ossia/score/releases/download/v{{site.score_version}}/ossia.score-{{site.score_version}}-src.tar.xz.asc">source code signature</a>
* Alternatively, you can fetch the latest source code <a href="https://github.com/ossia/score">directly from Github</a>



<script src="/js/collapsible.js"></script>
