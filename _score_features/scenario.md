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

### Features

- Intervals: Muting intervals

- Triggers: see [the relevant page](triggers.html)
- Conditions: see [the relevant page](conditions.html)
- Comment blocks


### Execution
- Putting stuff on the top start state for it to run with Reinitialize
- Putting stuff on the top end state for it to run when stop is pressed.

### Keyboard shortcuts

- In a scenario with the navigation keys ( {% include shortcut.html content="↑" %}, {% include shortcut.html content="↓" %}, {% include shortcut.html content="→" %}, {% include shortcut.html content="←" %}).
- To the parent scenario with {% include shortcut.html content="Ctrl+Alt+↑" %}.

- Unroll all intervals' racks in a scenario {% include shortcut.html content="Ctrl+Alt+U" %} 
- Fold all intervals' racks in a scenario {% include shortcut.html content="Ctrl+Alt+F" %} 

### Speed control

Speed sliders appear on intervals while playing. To reset it:  {% include shortcut.html content="Ctrl+Right Click" %} 

### List of drag'n'drops possible 

#### On intervals
- Drop from the device explorer to an interval: create an automatoin curve.
- Drop from the library explorer to an interval: create a process.
- Drop a media from the library or the system to an interval: create a process.
- Drop from the object list into a slot or in the interval
  
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


#### From states
- It is possible to select messages in a state and drop them either in the scenario, or on another state