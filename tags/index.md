---
layout: center
permalink: /tags/
---

{% for tag in site.tags %}
  {% capture tag_name %}{{ tag[0] }}{% endcapture %}
  <h3><a class="button" href="{{ site.baseurl }}/tags/{{ tag_name | slugify: "pretty" }}">{{ tag_name }}</a></h3> 
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
      
    {% endfor %}
  </ul>
{% endfor %}
