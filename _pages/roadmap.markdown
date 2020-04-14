---
layout: about-page
title:  "Roadmap"

permalink: /roadmap.html
category: site-about
---

<p align="center">
<a href="https://github.com/OSSIA/score/releases/tag/v2.5.2" class="button special"  target="_blank" >Current stable version is 2.5.2</a>
</p>

<h2>Future plans</h2>

* JIT compilation support. [An addon has been started but has not been maintained](https://github.com/OSSIA/score-addon-jit){:target="_blank"}.
* Networked edition and execution. [These capabilities have been prototyped but not kept up to date with the rest of the software](https://github.com/OSSIA/iscore-addon-network){:target="_blank"}.
* Parametric processes. How to have parameters and variables used within the scope of a given box and changed easily across different instances of that box.
* Mixer panel : making mixing from within score more straightforward.
* WebAssembly support : experiments have been made a few years ago – most of the score engine and user interface builds for WebAssembly, but execution does not work yet in a web page.
* Spout, Syphon support.
* Better support for sequences.
* Support for MIDI 2.0.

<h2><a href="https://github.com/OSSIA/score/releases/tag/v3.0.0-alpha1"  target="_blank">ossia score v3 (release targeting mid-2020)</a></h2>

ossia score 3 fulfills the long-term goal of being a proper multi-media platform, by providing integrated video abilities, in sync with the rest of the score, as well as musical abilities with support for tempo, musical metrics and quantization. Finally, the core engine has been extended to allow cycles in scenarios with a new kind of connection. This allows to implement state-machine-like behaviours in scenarios.

* [Support for reading videos](https://twitter.com/jcelerie/status/1236809800727617537){:target="_blank"}, right now H264 and HAP. Implementation uses Vulkan, Metal, D3D or OpenGL depending on the platform for maximal performance. Multiple viewports are supported.
* Support for applying shader-based filters on these videos. Interactive shader format is supported.
* Support for tempo, musical bars, etc. It is now possible to sync the triggering of a timenode to the beginning of the following bar for instance. Polyrythmy is supported : each interval can have its own tempo and metrics timeline.
* [Support for cycles and loops](https://twitter.com/jcelerie/status/1245484342274646017){:target="_blank"} in the main scenario.
* [Preset mechanism](https://twitter.com/jcelerie/status/1241774333535666176){:target="_blank"} for built-in processes.
* Built-in looping for individual processes, to easily loop audio files.
* Intervals can now be viewed in nodal mode to easily interconnect their processes.
* Many small and useful new processes – signal visualization, pattern sequencer…

<h2><a href="https://github.com/OSSIA/score/releases/tag/v2.5.2"  target="_blank">ossia score v2.5 (release targeting mid-2020)</a></h2>

This version is a big update to 2.0, adding two new processes :

* Control surface : allows to have UIs to control remote parameters in the score
* Nodal : allows to layout processes in a graph interface, like many other famous visual programming languages. Temporal processes can be nested in nodal processes.
* RemoteControl : control your score through a simple WebSockets API.
* Tons of UI work

<h2><a href="https://github.com/OSSIA/score/releases/tag/v2.0.0-a1"  target="_blank">ossia score v2.0 (release targeting mid-2020)</a></h2>

The 2.0 version is a paradigm shift : it introduces data and audio processing in score. The name was changed to reflect the OSSIA project legacy. It is now possible to play sounds, apply sound effects, among many other changes. The main highlights are :

* Execution is now based on synchronous audio processing APIs
* Playback of sounds
* Support for LV2, VST effects and instruments
* Support for Faust effects. The Faust compiler is integrated directly to score.
* Support for many new protocols : OSCQuery, ArtNet…
* Many new processes: LFO, step sequencer, math expressions, etc
* Pattern matching
* Drag’n’drop in a lot of places
* Creation of a library panel and a [user library](https://github.com/OSSIA/score-user-library){:target="_blank"}
* A super cute new mascot, [Oscar](https://camo.githubusercontent.com/2d6bd98dd127261a5306d0d9c73acf28c63795f7/68747470733a2f2f692e696d6775722e636f6d2f327842574967392e706e67){:target="_blank"} !

The first release for the 2.0 version was released in April 2018.

<h2><a href="https://github.com/OSSIA/score/releases/tag/v1.0.0-b40"  target="_blank">i-score v1.0 (release targeting mid-2020)</a></h2>

The 1.0 version is the concretization of the last year of effort in the  OSSIA project.
Thanks to a from-scratch rewrite, the software has been highly modularized, and now offers the following features :

* Undo-redo
* Restore on crash
* Various plug-in APIs
* Loops, mappings, JavaScript processes
* Arbitrary hierarchy
* Complete conditional branching and triggering
* A new dark blue theme

The 1.0 version was released in 2016.

<h2>i-score v0.3</h2>

Thanks again to the OSSIA project, a research effort will be carried on from early-2014 to 2015 in order to implement logic scenarios in i-score. This will include:

* Support for looping boxes and (sub-)scenarios
* Better graphic support for the conditional branching
* Multi-user support
* Framework for the future support of “plug-in” boxes:
    * Mapping boxes (for several one-to-one mappings between remote parameters)
    * Generic boxes and SDK for third-party boxes (e.g. audio boxes using JamomaAudioGraph, video/openGL boxes using QuartzComposer, etc…)


<h2>i-score v0.2</h2>

Thanks to the OSSIA research project, some services of i-score have been improved by implementing the Jamoma Modular framework into libIscore, and a dedicated framework for Interactive scores management

This allows some new features and improvements :

* Better devices/namespace support, including:
    * better devices configuration and automatic discovery
    * devices’ parameters’ attributes support (including range, type, etc….)
    * better curve management
    * recording of performance actions as curves
    * declaration and management of i-score’s boxes parameters (such as speed, trigger points….)
* Initial support of the conditional branching

<h2>v0.1</h2>

Initial version, including (as of 0.1-alpha1 – December 2012):

* Linear edition (no loops, no branching)
* One static Minuit device only (MinuitDevice1)
* Simple curves (no range editing)
* Nested scenarios (hierarchy) support
* Simple playing (unfinished GOTO function)

Several incremental alpha versions, have been released along the way, including:

* Plain OSC support
* Minuit devices configuration
* Several interface improvements

