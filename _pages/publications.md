---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% if site.publications.size > 0 %}
  {% for post in site.publications reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% else %}
  Formal publications can be added later under the `_publications/` collection.
{% endif %}
