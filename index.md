---
layout: default
title: SCM Backup
permalink: /
---

![{{ site.title}}](/img/logo64x64.png)

{{ site.description }}

At the moment, the following hosters are supported:

- [GitHub](https://github.com)
- [Bitbucket](https://bitbucket.org)


## News

{% for post in site.posts limit: 5 %}
- {{ post.date | date: "%b %d %Y" }} [{{ post.title | escape }}]({{ post.url | prepend: site.baseurl }})
{% endfor %}

[More news...](/news/)