---
layout: page
title: "topics"
permalink: /topics/
---

<div>

  <!-- testing things-->
  {% for category in site.categories %}
    {% capture category_name %}{{ category | first }}{% endcapture %}
    {% capture category_link %}/_category/{{ category_name | slugify }}.md{% endcapture %}
    <p>slugify: {{ category_name | slugify }} # name: {{ category_name }} # link: {{ category_link }}</p>
  {% endfor %}
</div>

<h1>Many of these links are currently nonexistent. Tx for your patience!</h1>

<div id="archives">
  {% for category in site.categories %}
  <div>
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <h3><a href="{{ site.baseurl }}/topics/{{ category_name | slugify}}">{{ category_name }}</a></h3>
  </div>
  {% endfor %}
</div>

<!-- Old code that lists categories with posts repeated: -->
<!-- {% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>

    <h3 class="category-head">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
    {% endfor %}
  </div>
{% endfor %} -->
