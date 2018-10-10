---
layout: page
title:  Ketä kysytty mukaan?
---

Listaus organisaatioista, joita kysytty mukaan vähentämään yksinäisyyttä.


<p> Yritykset:</p>

<ul>
  {% for post in site.categories.yritys %}
    {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a> <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time></li>
    {% endif %}
  {% endfor %}
</ul>

<p> Yritykset, jotka on mukana: </p>

<ul>
  {% for post in site.categories.yritys %}
    {% if post.categories contains "mukana" %}
      {% if post.url %}
          <li><a href="{{ post.url }}">{{ post.title }}</a> <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time></li>
      {% endif %}
    {% endif %}
  {% endfor %}
</ul>



