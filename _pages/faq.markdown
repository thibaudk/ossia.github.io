---
layout: learn-page
title:  "FAQ"

permalink: /faq.html
category: site-learn
---
    
<h3 class="faq">Basics</h3>
<p type="button" class="collapsible" > What is ossia score ?</p>
<div class="collapsible-content">
<p align="center" style="margin: 5px;">
<iframe width="854" height="480" src="https://www.youtube.com/embed/LSifHFbuky0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>
</div>

<p type="button" class="collapsible"> Playing a sound</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible"> Creating an interactive trigger</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible"> Creating a temporal condition</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible"> Creating a nested score</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Showing a video</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Automating a parameter</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible"> Making a loop</p>
<div class="collapsible-content">
</div>

<h3 class="faq">Intermediate</h3>
<p type="button" class="collapsible">  Mapping a parameter</p>
<div id="intermediate-mapping" class="collapsible-content">
</div>

<p type="button" class="collapsible">  Writing & playing MIDI through a software synthesizer</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Modulating with LFOs, step sequencers and others</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible"> Saving and loading presets</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Switching between musical and real-time mode</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Recording OSC messages and automations</p>
<div class="collapsible-content">
</div>

<h3 class="faq">Advanced features</h3>
<p type="button" class="collapsible">  Nesting scores</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Creating complex graphs of effects</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Multi-channel audio output and sound spatialization</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Scripting with JavaScript</p>
<div class="collapsible-content">
</div>

<p type="button"  class="collapsible">  Writing audio effects with Faust</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Writing advanced mappings with math expressions</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Writing graphics effects with ISF</p>
<div class="collapsible-content">
</div>

<p type="button"  class="collapsible"> Creating a control surface for external parameters</p>
<div class="collapsible-content">
</div>

<h3 class="faq">Working with other software</h3>

<p type="button" class="collapsible">  Connecting to Processing</p>
<div class="collapsible-content">
</div>

<p type="button"  class="collapsible">  Connecting to OpenRNDR</p>
<div class="collapsible-content">
</div>

<p type="button"  class="collapsible"> Connecting to Max/MSP</p>
<div class="collapsible-content">
</div>

<p type="button"  class="collapsible"> Connecting to PureData</p>
<div class="collapsible-content">
</div>

<p type="button"  class="collapsible">  Connecting to Unreal Engine</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Connecting to Unity3D</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible"> Connecting to OpenFrameworks</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Connecting to Qt / QML</p>
<div class="collapsible-content">
</div>

<p type="button"  class="collapsible">  Connecting to a generic OSC software</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible"> Connecting to a generic OSCQuery software</p>
<div class="collapsible-content">
</div>

<h3 class="faq">Working with hardware</h3>

<p type="button" class="collapsible"> Getting data from a MIDI device</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible">  Sending data to an external MIDI device</p>
<div class="collapsible-content">
</div>

<p type="button"  class="collapsible">  Sending data to ArtNet nodes</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible"> Communicating with a serial device (Arduino, etc)</p>
<div class="collapsible-content">
</div>

<p type="button" class="collapsible"> Communicating with a gamepad or Wiimote</p>
<div class="collapsible-content">
</div>

<h3 class="faq">Troubleshooting</h3>

<p type="button" class="collapsible">  The playback does not start</p>
<div class="collapsible-content">
     Most of the time, this is due to incorrect sound settings.
</div>

<p type="button" class="collapsible"> The minimap is hard to use on a Mac</p>
<div class="collapsible-content">
     You are likely encountering <a href="https://stackoverflow.com/questions/61843481/macos-simulated-mouse-event-only-works-when-launching-binary-not-application-b">this macOS issue</a>. <br/> 
    As a workaround, you can try to open score by right-clicking on Score.app, selection "Open contents", navigating to "Score.app/Contents/MacOS" and running the "score" binary from there.
</div>

<p type="button"  class="collapsible">  I have crashes</p>
<div class="collapsible-content">
    Please report them on the <a href="https://github.com/OSSIA/score/issues">issue tracker</a> if you have time. Thanks in advance !
</div>


<br/>

<br/>

<p align="center">
<a href="http://forum.ossia.io/" class="page-button"  target="_blank" >If your question is not here, ask us in the forum ! </a>
</p>


<script>
var coll = document.getElementsByClassName("collapsible");
var i;

for (i = 0; i < coll.length; i++) {
  coll[i].addEventListener("click", function() {
  
    var coll = document.getElementsByClassName("collapsible");
    var i;
    for (i = 0; i < coll.length; i++) {
        coll[i].classList.remove("active");
        coll[i].nextElementSibling.style.display = "none";
    }
    
    this.classList.toggle("active");
    var content = this.nextElementSibling;
    content.style.display = "block";
  });
}
</script>
