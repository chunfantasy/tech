---
layout: post
title: Spring TestContext Framework Configuration
description: "This note is about the configuration of testing environment with Spring."
modified: 2010-08-10
tags: [Framework]
comments: true
---

This note is about the configuration of testing environment with Spring.

# Dependency with Maven

{% highlight xml %}
<dependency>
	<groupId>org.springframework</groupId>
	<artifactId>spring-test</artifactId>
	<version>{$version}</version>
</dependency>
{% endhighlight %}

# Annotations above class

{% highlight java %}
@RunWith(SpringJUnit4ClassRunner.class)
@ContextConfiguration(locations = {
        "classpath*:*.xml"
})
@Transactional
{% endhighlight %}

# Rollback

The test rolls back transaction for test context after testing.
So do not worry when see nothing happens in database.