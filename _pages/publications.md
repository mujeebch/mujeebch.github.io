---
layout: archive
title: "Selected Publications"
permalink: /publications/
author_profile: true
---
You can find my articles on [Google Scholar](https://scholar.google.com/citations?user=l_qJD3IAAAAJ&hl=en).
{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
