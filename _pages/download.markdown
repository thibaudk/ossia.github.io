---
layout: score-page
title:  "Download"

permalink: /download.html
category: site-score
---
<script>
$(function(){
var tag = "v3.0.0-alpha5";
var version = "v3.0.0-a5";

   document.getElementById("linux").href = "https://github.com/OSSIA/score/releases/download/"+tag+"/score-"+version+"-Linux.AppImage" ;
   
   document.getElementById("windows").href = "https://github.com/OSSIA/score/releases/download/"+tag+"/score-"+version+"-win64.exe" ;
   
   document.getElementById("osx").href = "https://github.com/OSSIA/score/releases/download/"+tag+"/score-"+version+"-macOS.zip";

});
</script>

Download the latest stable release:
<p style="display: flex; justify-content: center;align-content:space-evenly;" align="center">
<a id="windows" href="https://github.com/OSSIA/score/releases/latest"  target="_blank" class="page-button download-page"><img src="assets/windows_logo_2012-Black.svg" width="80px"/>Windows</a>
<a id="osx" href="https://github.com/OSSIA/score/releases/latest"  target="_blank" class="page-button download-page" ><img src="assets/apple_logo_black.svg" width="80px"/>OS X</a>
<a id="linux" target="_blank" class="page-button download-page"><img src="assets/Linux_Platform.svg" width="80px"/>Linux</a>
</p>
The <a href="https://github.com/OSSIA/score/releases/latest"  target="_blank">change log</a> for the latest release.

<h2>Supported operating systems</h2>

* Windows 10
* Mac OS X 10.12, 10.13, 10.14
* Most recent desktop Linux distributions

<h2>Additional information</h2>

The releases are 64-bit on all operating systems.
Due to the limitations of the continuous integration service, most OS X releases will only work on the latest OS X version.
However, score can be built from source in order to work on 10.9 for instance.

For Linux, the AppImage should work on :
* CentOS >= 6.7
* Chromixium
* Fedora
* Kali
* Ubuntu, Kubuntu, Xubuntu, etc… >= 12.04
* Debian >= Jessie
* Suse >= 7.2
* ElementaryOS
* Arch Linux

It does not work currently on NixOS.
