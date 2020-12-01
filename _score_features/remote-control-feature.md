---
layout: score-feature
title:  "Remote control"

permalink: /score/features/remote-control.html
category: "site-score"

image: /assets/features/missing.png
description: "Remote control through a web page"

tag: "Interoperability"
visible: true
---

## Description
Exposes some properties of the score over WebSockets:
* Transport.
* Viewing and controlling triggers.
* Sending & receiving messages through the Device Explorer.
* Executing JS code in the console.

## WebSocket API description

The message format is JSON.

### Score -> client

{% highlight js %}
{
    "Message": "DeviceTree"
}
{% endhighlight %}


#### When a trigger starts executing:
{% highlight js %}
{
    "Message": "TriggerAdded"
    "Path": "/path/to/the/trigger"
}
{% endhighlight %}

#### When a trigger has finished executing:
{% highlight js %}
{
    "Message": "TriggerRemoved"
    "Path": "/path/to/the/trigger"
}
{% endhighlight %}


### Client -> score

#### Transport messages:

{% highlight js %}
{ "Message": "Play" }
{ "Message": "Pause" }
{ "Message": "Stop" }
{% endhighlight %}

#### Console control:

See the [Console API](console.html) for the allowed operations.
{% highlight js %}
{
  "Message": "Console"
  "Code": "someJSCodeToExecute()"
}
{% endhighlight %}

#### To trigger a trigger:
{% highlight js %}
{
    "Message": "Trigger"
    "Path": "/path/to/the/trigger"
}
{% endhighlight %}

#### To send a control message:
{% highlight js %}
{
    "Message": "Message"
    "Address": "device:/foo/bar@[color.rgb.r]"
    "Value": {
        "Float": 1.23
    }
}
{% endhighlight %}

or, to showcase all possible types:
{% highlight js %}
{
    "Message": "Message"
    "Address": "device:/foo/bar"
    "Value": {
        "Tuple": [
            { "Int": 1 },
            { "Bool": true },
            { "Char": c },
            { "Vec2f": [0.0, 1.1] },
            { "Vec3f": [0.0, 1.1, 1.2] },
            { "Vec4f": [0.0, 1.1, 1.3, 1.4] },
            { "Float": 1.23 },
            { "String": "foo" },
            { "Impulse": null },
        ]
    }
}
{% endhighlight %}

#### To enable / disable listening

Listening to an address means that when an address's value changes, the
new value is forwarded to the remote client.

{% highlight js %}
{
    "Message": "EnableListening"
    "Address": "device:/foo/bar"
}
{% endhighlight %}

and

{% highlight js %}
{
    "Message": "DisableListening"
    "Address": "device:/foo/bar"
}
{% endhighlight %}