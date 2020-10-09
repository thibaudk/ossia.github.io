---
layout: score-feature
title:  "Temporal workflow"

permalink: /score/features/temporal.html
category: "site-score"

image: /assets/features/temporal.png
description: "Creating and editing scenarios"

tag: "Structure"
visible: true
---

The main view in score.

# Features


### List of drag'n'drops possible 

#### On intervals
- Drop from the device explorer to an interval: create an automatoin curve.
- Drop from the library explorer to an interval: create a process.
- Drop a media from the library or the system to an interval: create a process.

#### Moving processes around
- Drag the little ☰ icon somewhere else in the timeline.
  - In the same interval: reorders
  - In another interval: moves the process
  - In a blank space: creates a new interval from there and moves the process
  
#### On processes
- Generally, dropping a media on a process changes the content of the process.
   * dropping a new sound file on a sound process
   * dropping a new address from the explorer on an automation
   * etc...
   * file bugs if you see a case not implemented !

#### On states
- Message list: add messages to the state
- .cues files (created by dropping a state into the library)
- .layer files