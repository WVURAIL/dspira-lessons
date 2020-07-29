---
layout: center
permalink: /tags/
---
![redwood house and laser name and trees and staaaaaars](/images/DspiraGalaxyPic2019.jpg)

  
{% for tag in site.tags %}
  {% capture tag_name %}{{ tag[0] }}{% endcapture %}
  <h3><a class="button" href="{{ site.baseurl }}/tags/{{ tag_name | slugify: "pretty" }}">{{ tag_name }}</a></h3> 
{% endfor %}

