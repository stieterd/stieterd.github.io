---
layout: home
---

{% assign todays_date = site.time | date: '%Y%m%d' %}

<div style="position: absolute; left: 50%; top: 10%; transform: translateX(-43%);">
  <h2 style="white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">
    <a id="myLink" href="javascript:MyFunction();"><code><</code></a> Movies of today <a id="myLink" href="javascript:MyFunction();"><code>></code></a>
  </h2>
</div>

<div style="overflow-y:hidden;overflow: hidden;padding:1em;width:100%;">

<ul style="position: relative; top: 150%; left: 50%; transform: translate(-45%, 15%); list-style: none; padding: 0;">

{% assign sortedPosts = site.posts | sort: 'title' %}

{% for post in sortedPosts %}
  {% capture post_date %}{{post.date | date: "%Y%m%d"}}{% endcapture %}
  {% if post_date == todays_date %}
  <li style="display: block;">
      <p> <a href="{{ post.url }}"><code>< watch ></code></a> - {{ post.date | date: '%d/%m/%Y'}} - {{ post.title }}</p>
  </li>
  {% endif %}
{% endfor %}

</ul>

</div>