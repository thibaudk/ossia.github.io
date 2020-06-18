---
layout: score-page
title:  "Download"

permalink: /score/download.html
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

Download the latest release __ossia score v3.0.0__:
<p style="display: flex; justify-content: center;align-content:space-evenly;" align="center">
<a id="windows" href="https://github.com/OSSIA/score/releases/latest"  target="_blank" class="page-button download-page"><img src="../assets/windows_logo_2012-Black.svg" height="80px"/>Windows 10</a>
<a id="osx" href="https://github.com/OSSIA/score/releases/latest"  target="_blank" class="page-button download-page" ><img src="../assets/apple_logo_black.svg" height="80px"/>Mac OS<br/>10.14, 10.15</a>
<a id="linux" target="_blank" class="page-button download-page"><img src="../assets/Linux_Platform.svg" height="80px"/>Linux <br/>details below</a>
</p>
The <a href="https://github.com/OSSIA/score/releases/latest"  target="_blank">change log</a> for the latest release.

<h2>Additional information</h2>

The releases are 64-bit on all operating systems.
Due to the limitations of the continuous integration service, most Mac OS releases will only work on the latest Mac OS version.
However, score can be built from source in order to work on 10.9 for instance.

<h2>Linux supported distribution</h2>
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
