---
permalink: /
layout: academic
redirect_from:
  - /about/
  - /about.html
---

<section class="profile" id="about" aria-labelledby="profile-name">
  <div class="profile-identity">
    <h1 id="profile-name">{{ site.author.name }}</h1>
    <p class="affiliation">Undergraduate at <a href="https://www.ruc.edu.cn/">Renmin University of China</a></p>
  </div>
  <img class="profile-photo" src="{{ site.author.avatar | prepend: '/images/' | relative_url }}"
       alt="Portrait of {{ site.author.name }}" width="576" height="768" fetchpriority="high">
  <div class="profile-intro">
    <p class="research-question">What should a language model compute now to reason better later?</p>
    <p>I started with latent reasoning. I now want to understand how pretraining can teach models to reuse their internal states, using looped Transformers to study when that reuse helps.</p>
    <ul class="link-row profile-links" aria-label="Contact and profiles">
      <li><a href="mailto:{{ site.author.email }}">Email</a></li>
      <li><a href="{{ site.author.googlescholar | escape }}">Google Scholar</a></li>
      <li><a href="https://github.com/{{ site.author.github }}">GitHub</a></li>
    </ul>
  </div>
</section>

<section class="home-section" id="publications" aria-labelledby="publications-heading">
  <h2 id="publications-heading">Selected Publications</h2>
  <article class="publication">
    <div class="publication-text">
      <p class="paper-meta">STAIR <span aria-hidden="true">&middot;</span> First author <span aria-hidden="true">&middot;</span> arXiv preprint, 2026</p>
      <h3><a href="https://arxiv.org/abs/2609.39394">Can Computation from Earlier Problems Help LLMs Solve New Ones?</a></h3>
      <p class="paper-authors"><strong>Jipei He</strong>, Wenhui Tan, Xiaoyi Yu, Enver Sangineto, Fiorenzo Parascandolo, Rita Cucchiara, Ruihua Song</p>
      <p>STAIR learns to read attention states saved from earlier answers, keeping the backbone and the saved states fixed.</p>
      <p>On AIME 2025 with Qwen3.5-4B, STAIR improves mean later-turn accuracy (Avg@4) by <strong>11.67 percentage points</strong> over the unmodified model with conversation history, using just <strong>12,288 trainable parameters</strong>.</p>
      <ul class="link-row paper-links" aria-label="Paper links">
        <li><a href="https://arxiv.org/abs/2609.39394">arXiv</a></li>
        <li><a href="https://arxiv.org/pdf/2609.39394">PDF</a></li>
        <li><a href="https://arxiv.org/html/2609.39394">HTML</a></li>
      </ul>
    </div>
    <figure class="paper-figure">
      <a href="https://arxiv.org/html/2609.39394v2#S1.F1" aria-label="View the STAIR figure in the paper">
        <img src="{{ '/images/publications/stair-v2-figure1.svg' | relative_url }}"
             alt="STAIR task switching, historical attention readout, and accuracy comparisons"
             width="548" height="378" loading="lazy">
      </a>
      <figcaption>STAIR method and results &middot; <a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a></figcaption>
    </figure>
  </article>
</section>

<section class="home-section" id="research" aria-labelledby="research-heading">
  <h2 id="research-heading">Research Direction</h2>
  <div class="research-description">
    <p><strong>Looped Transformers</strong> let us vary how much computation happens between tokens without changing the parameter count. I want to understand when an extra step helps later predictions, even when the immediate token choice stays the same.</p>
    <p>That puts the focus on <strong>pretraining</strong>: what kinds of dependencies in training data teach a model which intermediate states to keep and when to use them?</p>
  </div>
</section>

<section class="home-section" id="experience" aria-labelledby="experience-heading">
  <h2 id="experience-heading">Research Experience</h2>
  <dl class="experience-list">
    <div class="experience-entry">
      <dt><time datetime="2026-05">May 2026</time></dt>
      <dd>
        <p>Started collaborating with <a href="https://unimore.unifind.cineca.it/resource/person/245898?language=en_US">Prof. Enver Sangineto</a>.</p>
        <p class="experience-affiliation">University of Modena and Reggio Emilia</p>
      </dd>
    </div>
    <div class="experience-entry">
      <dt><time datetime="2026-04">Apr 2026</time></dt>
      <dd>
        <p>Joined <a href="https://ruc-aimind.github.io/">AIMIND Lab</a> as a research assistant, working with <a href="https://ai.ruc.edu.cn/GSAI_HOME/FACULTYn/RuihuaSong/698c41551ecb4629a3df64b648881b8d.htm">Prof. Ruihua Song</a>.</p>
        <p class="experience-affiliation">Gaoling School of Artificial Intelligence, Renmin University of China</p>
      </dd>
    </div>
    <div class="experience-entry">
      <dt><time datetime="2026-03">Mar 2026</time></dt>
      <dd>
        <p>Started collaborating with <a href="https://info.ruc.edu.cn/jsky/szdw/ajxjgcx/jsjkxyjsx1/js2/ee3b7633ab884b2596fc713137af091d.htm">Prof. Suyun Zhao</a>.</p>
        <p class="experience-affiliation">School of Information, Renmin University of China</p>
      </dd>
    </div>
  </dl>
</section>
