---
layout: page
title: gedanken
permalink: /gedanken/
---
> **der Gedanke** *(philosophisch betrachtet)* 
> Das Ergebnis eines inneren Prozesses; eine erwogene Meinung oder Ansicht.  

Hier sind meine aktuellen Gedanken:

<ul>
  {% for post in site.posts %}
    <li>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | downcase }}
        </a>
      </h3>
    </li>
  {% endfor %}
</ul>
