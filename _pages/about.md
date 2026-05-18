---
permalink: /
title: "Home"
author_profile: true
stylesheets:
  - /assets/css/home.css
redirect_from:
  - /about/
  - /about.html
---
{% assign home = site.data.home %}

<section id="about" class="wow-hero">
  <p class="section-kicker">{% include inline-markdown.html text=home.hero.eyebrow %}</p>
  <h1 class="main-heading">{% include inline-markdown.html text=home.hero.greeting %} <img src="{{ '/images/Hi.gif' | relative_url }}" width="40px" alt="Hi"> Welcome to my Homepage!</h1>
  <h2 class="hero-name">{% include inline-markdown.html text=home.hero.heading %}</h2>
  <div class="hero-intro rich-text">{{ home.hero.intro | markdownify }}</div>
  {% if home.hero.actions %}
    <div class="action-row">
      {% for action in home.hero.actions %}
        {% capture action_class %}wow-button{% if action.type == 'primary' %} wow-button-primary{% endif %}{% endcapture %}
        {% include smart-link.html label=action.label url=action.url external=action.external class_name=action_class %}
      {% endfor %}
    </div>
  {% endif %}
</section>

{% if home.focus_cards %}
<section class="profile-grid focus-grid" aria-label="Current focus">
  {% for card in home.focus_cards %}
    <div class="profile-card">
      <strong>{% include inline-markdown.html text=card.title %}</strong>
      <div class="rich-text">{{ card.text | markdownify }}</div>
      {% if card.links %}
        <div class="inline-link-row">
          {% for link in card.links %}{% include smart-link.html label=link.label url=link.url external=link.external %}{% endfor %}
        </div>
      {% endif %}
    </div>
  {% endfor %}
</section>
{% endif %}

{% if home.news %}
<section id="news" class="home-block">
  <h2>News</h2>
  <div class="news-box">
    <ul class="news-list">
      {% for item in home.news %}
        <li><span class="news-date"><em>{% include inline-markdown.html text=item.date %}</em></span> {% include inline-markdown.html text=item.text %}
          {% if item.links %}
            <span class="inline-link-row compact">
              {% for link in item.links %}{% include smart-link.html label=link.label url=link.url external=link.external %}{% endfor %}
            </span>
          {% endif %}
        </li>
      {% endfor %}
    </ul>
  </div>
</section>
{% endif %}

{% if home.experience %}
<section id="experience" class="home-block">
  <h2>Experience</h2>
  <div class="experience-container">
    {% for exp in home.experience %}
      <div class="experience-card">
        {% if exp.logo %}<img src="{{ exp.logo | relative_url }}" alt="{{ exp.logo_alt | default: exp.institution }}" class="experience-logo">{% endif %}
        <div class="experience-info">
          <strong>{% include inline-markdown.html text=exp.institution %}</strong><br>
          <em>{% include inline-markdown.html text=exp.period %}</em><br>
          {% include inline-markdown.html text=exp.role %}<br>
          <span class="muted-text">{% include inline-markdown.html text=exp.description %}</span>
          {% if exp.links %}
            <div class="inline-link-row">
              {% for link in exp.links %}{% include smart-link.html label=link.label url=link.url external=link.external %}{% endfor %}
            </div>
          {% endif %}
        </div>
      </div>
    {% endfor %}
  </div>
</section>
{% endif %}

{% if home.learning %}
<section id="learning" class="home-block">
  <h2>{% include inline-markdown.html text=home.learning.title %}</h2>
  <div class="rich-text">{{ home.learning.subtitle | markdownify }}</div>
  <div class="profile-grid three-col">
    {% for group in home.learning.groups %}
      <div class="profile-card">
        <strong>{% include inline-markdown.html text=group.title %}</strong>
        <ul>
          {% for item in group.items %}
            <li>{% include inline-markdown.html text=item %}</li>
          {% endfor %}
        </ul>
        {% if group.links %}
          <div class="inline-link-row">
            {% for link in group.links %}{% include smart-link.html label=link.label url=link.url external=link.external %}{% endfor %}
          </div>
        {% endif %}
      </div>
    {% endfor %}
  </div>
</section>
{% endif %}

{% if home.projects %}
<section id="projects" class="home-block">
  {% assign projects_title = home.projects_intro.title | default: 'Projects' %}
  <h2>{% include inline-markdown.html text=projects_title %}</h2>
  <div class="rich-text">{{ home.projects_intro.subtitle | markdownify }}</div>
  {% for project in home.projects %}
    <div class="project-card {% if project.featured %}featured{% endif %}" data-category="project">
      <div class="project-card-inner">
        {% if project.image %}
          <div class="pub-media-rotator project-media" data-interval="4000">
            <img src="{{ project.image | relative_url }}" alt="{{ project.image_alt | default: project.title }}">
          </div>
        {% endif %}
        <div class="project-main">
          <div class="project-topline">
            <div>
              <strong>{% include inline-markdown.html text=project.title %}</strong><br>
              <i>{% include inline-markdown.html text=project.subtitle %}</i>
            </div>
            {% if project.links %}
              <div class="project-links">
                {% for link in project.links %}
                  {% include smart-link.html label=link.label url=link.url external=link.external %}
                {% endfor %}
              </div>
            {% endif %}
          </div>
          <div class="rich-text">{{ project.description | markdownify }}</div>
          {% if project.tags %}
            <div class="tag-row">
              {% for tag in project.tags %}<span>{% include inline-markdown.html text=tag %}</span>{% endfor %}
            </div>
          {% endif %}
          {% if project.bullets %}
            <ul>
              {% for bullet in project.bullets %}<li>{% include inline-markdown.html text=bullet %}</li>{% endfor %}
            </ul>
          {% endif %}
        </div>
      </div>
    </div>
  {% endfor %}
</section>
{% endif %}

{% if home.preparation %}
<section id="preparation" class="home-block">
  <h2>{% include inline-markdown.html text=home.preparation.title %}</h2>
  <div class="rich-text">{{ home.preparation.subtitle | markdownify }}</div>
  <div class="profile-grid two-col">
    {% for card in home.preparation.cards %}
      <div class="profile-card">
        <strong>{% include inline-markdown.html text=card.title %}</strong>
        <div class="rich-text">{{ card.text | markdownify }}</div>
        {% if card.links %}
          <div class="inline-link-row">
            {% for link in card.links %}{% include smart-link.html label=link.label url=link.url external=link.external %}{% endfor %}
          </div>
        {% endif %}
      </div>
    {% endfor %}
  </div>
</section>
{% endif %}

{% if home.extra_sections %}
  {% for section in home.extra_sections %}
    <section id="{{ section.id | default: section.title | slugify }}" class="home-block">
      {% if section.kicker %}<p class="section-kicker">{% include inline-markdown.html text=section.kicker %}</p>{% endif %}
      {% if section.title %}<h2>{% include inline-markdown.html text=section.title %}</h2>{% endif %}
      {% if section.subtitle %}<div class="rich-text">{{ section.subtitle | markdownify }}</div>{% endif %}
      {% if section.content %}<div class="rich-text">{{ section.content | markdownify }}</div>{% endif %}
      {% if section.items %}
        <ul>
          {% for item in section.items %}<li>{% include inline-markdown.html text=item %}</li>{% endfor %}
        </ul>
      {% endif %}
      {% if section.cards %}
        <div class="profile-grid {% if section.columns == 3 %}three-col{% else %}two-col{% endif %}">
          {% for card in section.cards %}
            <div class="profile-card">
              {% if card.title %}<strong>{% include inline-markdown.html text=card.title %}</strong>{% endif %}
              {% if card.text %}<div class="rich-text">{{ card.text | markdownify }}</div>{% endif %}
              {% if card.items %}
                <ul>{% for item in card.items %}<li>{% include inline-markdown.html text=item %}</li>{% endfor %}</ul>
              {% endif %}
              {% if card.links %}
                <div class="inline-link-row">
                  {% for link in card.links %}{% include smart-link.html label=link.label url=link.url external=link.external %}{% endfor %}
                </div>
              {% endif %}
            </div>
          {% endfor %}
        </div>
      {% endif %}
      {% if section.links %}
        <div class="action-row">
          {% for link in section.links %}
            {% capture link_class %}wow-button{% if link.type == 'primary' %} wow-button-primary{% endif %}{% endcapture %}
            {% include smart-link.html label=link.label url=link.url external=link.external class_name=link_class %}
          {% endfor %}
        </div>
      {% endif %}
    </section>
  {% endfor %}
{% endif %}

{% if home.contact %}
<section id="contact" class="home-block contact-panel">
  <p class="section-kicker">Contact</p>
  <h2>{% include inline-markdown.html text=home.contact.title %}</h2>
  <div class="rich-text">{{ home.contact.text | markdownify }}</div>
  {% if home.contact.email %}<p><a href="mailto:{{ home.contact.email }}">{{ home.contact.email }}</a></p>{% endif %}
  {% if home.contact.links %}
    <div class="action-row">
      {% for link in home.contact.links %}
        {% capture contact_class %}wow-button{% if link.type == 'primary' %} wow-button-primary{% endif %}{% endcapture %}
        {% include smart-link.html label=link.label url=link.url external=link.external class_name=contact_class %}
      {% endfor %}
    </div>
  {% endif %}
</section>
{% endif %}
