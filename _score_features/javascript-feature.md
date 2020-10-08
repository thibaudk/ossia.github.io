---
layout: score-feature
title:  "Javascript"

permalink: /score/features/javascript.html
category: "site-score"

image: /assets/features/js.png
description: "Writing JavaScript processes"

tag: "Scripting"
visible: true
---

## Scripting in Javascript / QML.
ES7; https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference
qml : property real, etc.

https://doc.qt.io/qt-5/qmlreference.html

setting the path to a file is possible

## Editing code
if there are compilation errors, the edited script *won't* be saved.

## Example of a value mapper

{% highlight qml %}
// Necessary for the Script object. 
// It is also possible to import QtQml 2.15
import Score 1.0

// Create our script object
Script {
  // Define the inputs & outputs - they are sub-objects of the script object
  ValueInlet { id: in1 }
  ValueOutlet { id: out1 }
  FloatSlider { id: slider; min: 10; max: 100; }

  // QML syntax for defining a floating-point constant
  readonly property real my_constant: 1.234

  // This function is called on each tick.
  tick: function(token, state) {
    // has a message been received ? 
    if (typeof in1.value !== 'undefined') {
      // print it in the console
      console.log(in1.value);

      // transform it with some math operations.
      var newValue = in1.value + slider.value * Math.random() + my_constant;

      // write it in the output
      out1.value = newValue;
    }
  }

  start: function() { console.log("I am called on start"); }
  stop: function() { console.log("I am called on stop"); }
  pause: function() { console.log("I am called on pause"); }
  resume: function() { console.log("I am called on resume"); }
}
{% endhighlight %}

Note: it is also possible to access the list of messages with their precise timing, with `values`.

## Example of an audio generator

{% highlight qml %}
import Score 1.0

Script {
  // Declare our inputs & outputs
  FloatSlider { id: in1; min: 20; max: 800; init: 440; objectName: "Frequency" }
  AudioOutlet { id: out1 }
  
  // Index to keep track of the phase
  property int idx: 0;

  tick: function(token, state) {
    var arr = [ ];

    // How many samples we must write
    var n = token.physical_write_duration(state.model_to_samples);
    
    if(n > 0) {
      // Computer the sin() coefficient
      var freq = in1.value;

      // Notice how we get sample_rate from state.
      var phi = 2 * Math.PI * freq / state.sample_rate;

      // Where we must start to write samples
      var i0 = token.physical_start(state.model_to_samples);

      // Fill our array
      for(var s = 0; s < n; s++) {
        var sample = Math.sin(phi * (idx++));
        sample = freq > 0 ? sample : 0;
        arr[i0 + s] = 0.3 * sample;
      }
    }

    // Write two audio channels, which will give stereo output by default in score.
    out1.setChannel(0, arr);
    out1.setChannel(1, arr);
  }
}

{% endhighlight %}

## Example of a MIDI transposer

See the user library: Presets/JS/transpose.qml

## Port types 
## Properties common to all ports
{% highlight qml %}
FloatSlider {
    id: myVariableName  // <- how you refer to it in the javascript Code
    objectName: "The name shown in the score UI"
    address: "foo:/bar/baz" // <- default address used when the object is created
}
{% endhighlight %}

## Audio
Create an audio input: 
{% highlight qml %}
AudioInlet { 
    id: in    
}

...

var left = in.channel(0);
var right = in.channel(1);

console.log(left[0]); // print the first sample of the first channel 

for (var value in left) { ... }
{% endhighlight %}

Create an audio output:

{% highlight qml %}
AudioOutlet { 
    id: out
}

...
// set the data of channel 0 to the following: 
out.setChannel(0, [0.1, 0.0, 0.2, 0.0, -0.1, 0.0]);

{% endhighlight %}

## MIDI
Create a MIDI input: 
{% highlight qml %}
MidiInlet { 
    id: in    
}

...

var messages = in.messages();
for (var message in messages) { 
    // Print the MIDI bytes
    console.log(message[0], message[1], message[2]);
}
{% endhighlight %}

Create a MIDI output: 

{% highlight qml %}
MidiOutlet { 
    id: out
}

...
// push a new message
out.add([144, 64, 127]);

// set & replace all the messages to be pushed
out.setMessages([ 
    [144, 64, 127], 
    [144, 68, 127], 
    [127, 30, 0]
]);
{% endhighlight %}


## Messages
Receiving:
{% highlight qml %}
ValueInlet {
    id: in
}

...

// Print the latest message received
console.log(in.value());

// Iterate through all the messages received for this tick, with their timestamp
for (var message in in.values) { 
    console.log(message.timestamp, message.value);
}
{% endhighlight %}

Sending:
{% highlight qml %}
ValueOutlet { 
    id: out
}

...
// Use either
out.setValue(1.234);

// or 
out.addValue(timestamp, 1.234);
{% endhighlight %}

## Controls
Controls behave exactly like ValueInlet but show up as actual UI 
controls. They have as such relevant properties: min, max, etc.
{% highlight qml %}
FloatSlider { 
    min: 0.0
    max: 1.0
    init: 0.5
}
{% endhighlight %}

{% highlight qml %}
IntSlider { 
    min: 0 
    max: 127
    init: 0
}
{% endhighlight %}

{% highlight qml %}
Enum { 
    choices: ["foo", "bar", "baz"]
    index: 2
}
{% endhighlight %}

{% highlight qml %}
Toggle { 
    checked: true
}
{% endhighlight %}

{% highlight qml %}
LineEdit { 
    text: "Hello world"
}
{% endhighlight %}


<!--
{% highlight qml %}
ControlInlet { }
{% endhighlight %}
{% highlight qml %}
ControlOutlet { }
{% endhighlight %}
-->