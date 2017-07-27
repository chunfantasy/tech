---
layout: post
title: Hibernate Note
description: "This note is about the problems that I met while using Hibernate."
modified: 2013-04-01
tags: [Framework]
comments: true
image:
  feature: 2010-06-01-hibernate.png
---

This note is about the problems that I met while using Hibernate.

# Generated Value

{% highlight java %}
@Id
@GeneratedValue(generator = "uuid")
@GenericGenerator(name = "uuid", strategy = "uuid2")
{% endhighlight %}

# Mapping

{% highlight java %}
// One to one
@OneToOne(cascade = {CascadeType.PERSIST, CascadeType.REFRESH})
@JoinColumn(name = "memberId")
{% endhighlight %}

* CascadeType.PERSIST : means that save() or persist() operations cascade to related entities.
* CascadeType.MERGE : means that related entities are merged into managed state when the owning entity is merged.
* CascadeType.REFRESH : does the same thing for the refresh() operation.
* CascadeType.REMOVE : removes all related entities association with this setting when the owning entity is deleted.
* CascadeType.DETACH : detaches all related entities if a “manual detach” occurs.
* CascadeType.ALL : is shorthand for all of the above cascade operations.