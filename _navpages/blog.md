---
title: Blog
layout: page
idname: blog
---

Here's where I post what I've been up to lately. These are sometimes but not always research updates. Other things I post about include things I've been working on for fun, personal project interests, musings and other things I think might be helpful to share.

<div id="toc container" margin="0 auto;">
  <b> Contents: </b>
  <table style="text-align:left">
 {% for post in site.posts %}
  <tr>
   <td>{{ post.date | date_to_string: "ordinal", "US" }} | <a href="{{ post.url }}">{{ post.title }}</a></td>
  </tr>
 {% endfor %}
  </table>
</div>

***
{% for post in site.posts %}
  <h2>{{ post.title }}</h2>

  {{ post.excerpt }}<input type="button" onclick="location.href='{{ post.url }}';" value="Read More">
{% endfor %}
