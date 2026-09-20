---
permalink: /
title: ""
author_profile: false
stylesheets:
  - /assets/css/home.css
redirect_from:
  - /about/
  - /about.html
---
{% assign home = site.data.home %}

<div class="research-home">
  <section id="about" class="home-hero">
    <div class="hero-photo">
      <img src="{{ '/images/avatar-photo.jpg' | relative_url }}" alt="He Jipei">
    </div>

    <div class="hero-main">
      <p class="hero-eyebrow">{{ home.hero.eyebrow }}</p>
      <h1>{{ home.hero.name }}</h1>
      <p class="hero-role">{{ home.hero.role }}</p>

      <div class="hero-copy">
        {% for paragraph in home.hero.intro %}
          {{ paragraph | markdownify }}
        {% endfor %}
      </div>

      <div class="hero-links" aria-label="Profile links">
        {% for link in home.hero.links %}
          <a href="{{ link.url }}"{% if link.external %} target="_blank" rel="noopener"{% endif %}>{{ link.label }}</a>
        {% endfor %}
      </div>
    </div>
  </section>

  <section id="research" class="home-section">
    <div class="section-heading">
      <p class="section-label">Research</p>
      <h2>Research interests</h2>
    </div>

    <div class="research-list">
      {% for item in home.research %}
        <article class="research-item">
          <h3>{{ item.title }}</h3>
          <p>{{ item.text }}</p>
        </article>
      {% endfor %}
    </div>
  </section>

  <section id="updates" class="home-section updates-section">
    <div class="section-heading">
      <p class="section-label">Updates</p>
      <h2>Recent</h2>
    </div>

    <div class="updates-list">
      {% for item in home.updates %}
        <div class="update-item">
          <time>{{ item.date }}</time>
          <p>{{ item.text }}</p>
        </div>
      {% endfor %}
    </div>
  </section>
</div>
