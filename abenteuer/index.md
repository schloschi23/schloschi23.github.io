---
layout: page
title: abenteuer
permalink: /abenteuer/
---
mittelhochdeutsch ābentiure, āventiure < altfranzösisch aventure, über das
Vulgärlateinische zu lateinisch advenire: *mit einem außergewöhnlichen,
erregenden Geschehen verbundene gefahrvolle Situation, die jemand zu bestehen
hat*


<div class="adventure-grid">
  {% assign adventures = site.pages | where_exp: "item", "item.path contains 'abenteuer/'" %}
  
  {% for adventure in adventures %}
    {% unless adventure.url == page.url %} <a href="{{ adventure.url | relative_url }}" class="adventure-card">
        <div class="card-content">
          <h3>{{ adventure.title }}</h3>
          {% if adventure.description %}
            <p>{{ adventure.description }}</p>
          {% endif %}
          <span class="read-more">Ansehen &rarr;</span>
        </div>
      </a>

    {% endunless %}
  {% endfor %}
</div>

<style>
/* Container für das Grid */
.adventure-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); /* Automatische Spalten */
  gap: 20px; /* Abstand zwischen Kacheln */
  margin-top: 2rem;
}

/* Die einzelne Kachel */
.adventure-card {
  display: block;
  background: #f9f9f9; /* Helle Hintergrundfarbe */
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 20px;
  text-decoration: none; /* Kein Unterstrich beim Link */
  color: inherit;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

/* Hover-Effekt: Kachel hebt sich leicht */
.adventure-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  background: #fff;
}

.adventure-card h3 {
  margin-top: 0;
  margin-bottom: 0.5rem;
  color: #333; /* Deine Überschriftenfarbe */
}

.adventure-card p {
  font-size: 0.95rem;
  color: #666;
  line-height: 1.5;
}

.read-more {
  display: inline-block;
  margin-top: 10px;
  font-weight: bold;
  font-size: 0.9rem;
  color: #007bff; /* Deine Akzentfarbe anpassen */
}
</style>
