---
permalink: /grandmaster/
title: "GrandMaster"
author_profile: true
stylesheets:
  - /assets/css/home.css
redirect_from:
  - /grandmaster.html
---
{% assign gm = site.data.grandmaster %}

<section class="wow-hero compact">
  <p class="section-kicker">{% include inline-markdown.html text=gm.hero.eyebrow %}</p>
  <h1 class="main-heading">{% include inline-markdown.html text=gm.hero.title %}</h1>
  <div class="hero-intro rich-text">{{ gm.hero.intro | markdownify }}</div>
  {% if gm.hero.actions %}
    <div class="action-row">
      {% for action in gm.hero.actions %}
        {% capture action_class %}wow-button{% if action.type == 'primary' %} wow-button-primary{% endif %}{% endcapture %}
        {% include smart-link.html label=action.label url=action.url external=action.external class_name=action_class %}
      {% endfor %}
    </div>
  {% endif %}
</section>

<section id="overview" class="home-block">
  <p class="section-kicker">{% include inline-markdown.html text=gm.overview.kicker %}</p>
  <h2>{% include inline-markdown.html text=gm.overview.title %}</h2>
  <div class="rich-text">{{ gm.overview.subtitle | markdownify }}</div>
  <div class="profile-grid two-col">
    {% for card in gm.overview.cards %}
      <div class="profile-card">
        <strong>{% include inline-markdown.html text=card.title %}</strong>
        <div class="rich-text">{{ card.text | markdownify }}</div>
        {% if card.links %}<div class="inline-link-row">{% for link in card.links %}{% include smart-link.html label=link.label url=link.url external=link.external %}{% endfor %}</div>{% endif %}
      </div>
    {% endfor %}
  </div>
</section>

<section id="questions" class="home-block">
  <p class="section-kicker">{% include inline-markdown.html text=gm.research_questions.kicker %}</p>
  <h2>{% include inline-markdown.html text=gm.research_questions.title %}</h2>
  <div class="rich-text">{{ gm.research_questions.subtitle | markdownify }}</div>
  <div class="profile-grid two-col">
    {% for item in gm.research_questions.items %}
      <div class="profile-card">
        <strong>{% include inline-markdown.html text=item.title %}</strong>
        <div class="rich-text">{{ item.text | markdownify }}</div>
        {% if item.links %}<div class="inline-link-row">{% for link in item.links %}{% include smart-link.html label=link.label url=link.url external=link.external %}{% endfor %}</div>{% endif %}
      </div>
    {% endfor %}
  </div>
</section>

<section id="architecture" class="home-block">
  <p class="section-kicker">{% include inline-markdown.html text=gm.architecture.kicker %}</p>
  <h2>{% include inline-markdown.html text=gm.architecture.title %}</h2>
  <div class="rich-text">{{ gm.architecture.subtitle | markdownify }}</div>
  <div class="profile-grid two-col">
    {% for card in gm.architecture.cards %}
      <div class="profile-card">
        <strong>{% include inline-markdown.html text=card.title %}</strong>
        <ul>
          {% for bullet in card.bullets %}<li>{% include inline-markdown.html text=bullet %}</li>{% endfor %}
        </ul>
        {% if card.links %}<div class="inline-link-row">{% for link in card.links %}{% include smart-link.html label=link.label url=link.url external=link.external %}{% endfor %}</div>{% endif %}
      </div>
    {% endfor %}
  </div>
</section>

<section id="lifecycle" class="home-block">
  <p class="section-kicker">{% include inline-markdown.html text=gm.lifecycle.kicker %}</p>
  <h2>{% include inline-markdown.html text=gm.lifecycle.title %}</h2>
  <div class="rich-text">{{ gm.lifecycle.subtitle | markdownify }}</div>
  <div class="timeline-card compact-list">
    {% for item in gm.lifecycle.items %}
      <div><strong>{% include inline-markdown.html text=item.title %}</strong><div class="rich-text">{{ item.text | markdownify }}</div></div>
    {% endfor %}
  </div>
</section>

<section id="implementation" class="home-block">
  <p class="section-kicker">{% include inline-markdown.html text=gm.implementation.kicker %}</p>
  <h2>{% include inline-markdown.html text=gm.implementation.title %}</h2>
  <div class="rich-text">{{ gm.implementation.subtitle | markdownify }}</div>
  <div class="profile-grid two-col">
    {% for card in gm.implementation.cards %}
      <div class="profile-card">
        <strong>{% include inline-markdown.html text=card.title %}</strong>
        <ul>
          {% for bullet in card.bullets %}<li>{% include inline-markdown.html text=bullet %}</li>{% endfor %}
        </ul>
        {% if card.links %}<div class="inline-link-row">{% for link in card.links %}{% include smart-link.html label=link.label url=link.url external=link.external %}{% endfor %}</div>{% endif %}
      </div>
    {% endfor %}
  </div>
  <div class="note-box rich-text">{{ gm.implementation.note | markdownify }}</div>
</section>

<section id="evaluation" class="home-block">
  <p class="section-kicker">{% include inline-markdown.html text=gm.evaluation.kicker %}</p>
  <h2>{% include inline-markdown.html text=gm.evaluation.title %}</h2>
  <div class="rich-text">{{ gm.evaluation.subtitle | markdownify }}</div>
  <div class="timeline-card compact-list">
    {% for item in gm.evaluation.items %}
      <div><strong>{% include inline-markdown.html text=item.title %}</strong><div class="rich-text">{{ item.text | markdownify }}</div></div>
    {% endfor %}
  </div>
  <div class="profile-grid two-col after-gap">
    {% for card in gm.evaluation.cards %}
      <div class="profile-card {% if card.warning %}warning{% endif %}">
        <strong>{% include inline-markdown.html text=card.title %}</strong>
        <div class="rich-text">{{ card.text | markdownify }}</div>
        {% if card.links %}<div class="inline-link-row">{% for link in card.links %}{% include smart-link.html label=link.label url=link.url external=link.external %}{% endfor %}</div>{% endif %}
      </div>
    {% endfor %}
  </div>
</section>

<section id="why" class="home-block">
  <p class="section-kicker">{% include inline-markdown.html text=gm.why_it_matters.kicker %}</p>
  <h2>{% include inline-markdown.html text=gm.why_it_matters.title %}</h2>
  <div class="rich-text">{{ gm.why_it_matters.subtitle | markdownify }}</div>
  <div class="profile-grid two-col">
    {% for item in gm.why_it_matters.items %}
      <div class="profile-card">
        <strong>{% include inline-markdown.html text=item.title %}</strong>
        <div class="rich-text">{{ item.text | markdownify }}</div>
        {% if item.links %}<div class="inline-link-row">{% for link in item.links %}{% include smart-link.html label=link.label url=link.url external=link.external %}{% endfor %}</div>{% endif %}
      </div>
    {% endfor %}
  </div>
</section>

<section id="links" class="home-block contact-panel">
  <p class="section-kicker">{% include inline-markdown.html text=gm.links.kicker %}</p>
  <h2>{% include inline-markdown.html text=gm.links.title %}</h2>
  <div class="rich-text">{{ gm.links.text | markdownify }}</div>
  {% if gm.links.actions %}
    <div class="action-row">
      {% for action in gm.links.actions %}
        {% capture action_class %}wow-button{% if action.type == 'primary' %} wow-button-primary{% endif %}{% endcapture %}
        {% include smart-link.html label=action.label url=action.url external=action.external class_name=action_class %}
      {% endfor %}
    </div>
  {% endif %}
  {% if gm.links.chips %}
    <div class="tag-row">
      {% for chip in gm.links.chips %}<span>{% include inline-markdown.html text=chip %}</span>{% endfor %}
    </div>
  {% endif %}
</section>
