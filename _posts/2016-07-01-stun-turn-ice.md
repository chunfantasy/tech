---
layout: post
title: STUN TURN and ICE Server Note
description: "This post contains the note about how to solve the problem happened when using STUN TURN and ICE Server."
modified: 2016-07-01
tags: [Server]
comments: true
---

# TURN




# STUN

# ICE

# Install

{% highlight bash %}
$ sudo apt-get update
$ sudo apt-get install coturn
{% endhighlight %}


# Configuration

By default, turn server port is 3478 and stun server is 3479.

https://www.webrtc-experiment.com/docs/TURN-server-installation-guide.html

# Run

{% highlight bash %}
$ sudo turnserver
{% endhighlight %}
