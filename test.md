---
layout: page
title: test
permalink: /test/
author: dave
---
<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
      {{ post.excerpt }}
  </li>
{% endfor %}
</ul>
---
{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
  {% for post in tag[1] %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
  </ul>
{% endfor %}
---
{% for staff_member in site.staff_members %}
  <h2>{{ staff_member.name }} - {{ staff_member.position }}</h2>
  <p>{{ staff_member.content | markdownify }}</p>
{% endfor %}
---
{% for staff_member in site.staff_members %}
  <h2>
    <a href="{{ staff_member.url }}">
      {{ staff_member.name }} - {{ staff_member.position }}
    </a>
  </h2>
  <p>{{ staff_member.content | markdownify }}</p>
{% endfor %}
---
<ul>
{% for member in site.data.members %}
  <li>
    <a href="https://github.com/{{ member.github }}">
      {{ member.name }}
    </a>
  </li>
{% endfor %}
</ul>
---
<ul>
{% for org_hash in site.data.orgs %}
{% assign org = org_hash[1] %}
  <li>
    <a href="https://github.com/{{ org.username }}">
      {{ org.name }}
    </a>
    ({{ org.members | size }} members)
  </li>
{% endfor %}
</ul>
---
{% assign author = site.data.people[page.author] %}
<a rel="author"
  href="<https://twitter.com/{{ author.twitter }}>"
  title="{{ author.name }}">
    {{ author.name }}
</a>
---
{% assign image_files = site.static_files | where: "image", true %}
{% for myimage in image_files %}
  {{ myimage.path }}
{% endfor %}
