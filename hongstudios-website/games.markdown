---
layout: default
title: 我们的游戏作品
permalink: /games/
---
{% for game in site.games %}
  <div class="game-card">
    <img src="{{ game.icon }}" alt="{{ game.title }}">
    <h3>{{ game.title }}</h3>
    <p>{{ game.description }}</p>
    <div class="screenshots">
      {% for screenshot in game.screenshots limit:3 %}
        <img src="{{ screenshot }}" alt="游戏截图">
      {% endfor %}
    </div>
    <div class="download-links">
      <a href="{{ game.appstore }}" class="btn">App Store</a>
      <a href="{{ game.googleplay }}" class="btn">Google Play</a>
    </div>
  </div>
{% endfor %}