---
permalink: /
author_profile: true
stylesheets:
  - /assets/css/home.css
redirect_from:
  - /about/
  - /about.html
---

<span class="home-anchor" id="about"></span>

I am an undergraduate student at [Renmin University of China](https://www.ruc.edu.cn/). My research interests include **LLM reasoning, Transformer architecture optimization, post-training, and multimodal AI safety**.

Broadly, I am interested in how foundation models reason and how to make that process more effective and efficient. I also care about the safety and reliability of multimodal systems.

I am fortunate to work with Prof. [Ruihua Song](https://ai.ruc.edu.cn/GSAI_HOME/FACULTYn/RuihuaSong/698c41551ecb4629a3df64b648881b8d.htm), Prof. [Suyun Zhao](https://info.ruc.edu.cn/jsky/szdw/ajxjgcx/jsjkxyjsx1/js2/ee3b7633ab884b2596fc713137af091d.htm), and Prof. [Wenxuan Wang](https://jarviswang94.github.io/) at Renmin University of China.


<span class="home-anchor" id="publications"></span>

# Selected Publications

<div class="paper-card">
  <a class="paper-card-visual" href="https://arxiv.org/pdf/2609.39394" aria-label="Open paper PDF">
    <div class="paper-badge">arXiv 2026</div>
    <svg viewBox="0 0 720 420" role="img" aria-label="Visual summary of STAIR and historical computation reuse">
      <rect x="0" y="0" width="720" height="420" rx="18" fill="#fbfcfe"/>
      <text x="34" y="44" fill="#1f2937" font-size="22" font-weight="700">Can earlier computation help new reasoning?</text>
      <text x="34" y="72" fill="#667085" font-size="13">Continuous multi-problem reasoning</text>

      <g transform="translate(34,104)">
        <rect x="0" y="0" width="118" height="70" rx="10" fill="#ffffff" stroke="#cfd8e3"/>
        <text x="14" y="24" fill="#224b8d" font-size="14" font-weight="700">T1</text>
        <text x="14" y="46" fill="#596270" font-size="12">Problem A</text>

        <rect x="144" y="0" width="118" height="70" rx="10" fill="#ffffff" stroke="#cfd8e3"/>
        <text x="158" y="24" fill="#224b8d" font-size="14" font-weight="700">T2</text>
        <text x="158" y="46" fill="#596270" font-size="12">Problem B</text>

        <rect x="288" y="0" width="118" height="70" rx="10" fill="#ffffff" stroke="#cfd8e3"/>
        <text x="302" y="24" fill="#224b8d" font-size="14" font-weight="700">T3</text>
        <text x="302" y="46" fill="#596270" font-size="12">Problem C</text>

        <rect x="486" y="0" width="166" height="70" rx="10" fill="#eef4fb" stroke="#9fb4cc"/>
        <text x="500" y="24" fill="#224b8d" font-size="14" font-weight="700">T4</text>
        <text x="500" y="46" fill="#344054" font-size="12">New problem</text>

        <path d="M118 35 H144 M262 35 H288 M406 35 H486" stroke="#94a3b8" stroke-width="2.2"/>
        <path d="M479 30 L489 35 L479 40" fill="none" stroke="#94a3b8" stroke-width="2.2"/>
      </g>

      <g transform="translate(34,215)">
        <rect x="0" y="0" width="300" height="118" rx="12" fill="#ffffff" stroke="#d7dde6"/>
        <text x="18" y="28" fill="#344054" font-size="14" font-weight="700">Historical K/V bank</text>
        <rect x="18" y="48" width="72" height="36" rx="8" fill="#edf2f7"/>
        <rect x="102" y="48" width="72" height="36" rx="8" fill="#edf2f7"/>
        <rect x="186" y="48" width="72" height="36" rx="8" fill="#edf2f7"/>
        <text x="35" y="71" fill="#667085" font-size="11">T1 state</text>
        <text x="119" y="71" fill="#667085" font-size="11">T2 state</text>
        <text x="203" y="71" fill="#667085" font-size="11">T3 state</text>
        <text x="18" y="103" fill="#98a2b3" font-size="11">read-only historical computation</text>

        <rect x="374" y="0" width="278" height="118" rx="12" fill="#eef4fb" stroke="#9fb4cc"/>
        <text x="394" y="28" fill="#224b8d" font-size="14" font-weight="700">STAIR</text>
        <text x="394" y="52" fill="#475467" font-size="12">re-address current queries</text>
        <text x="394" y="73" fill="#475467" font-size="12">toward useful historical states</text>
        <rect x="394" y="88" width="104" height="16" rx="8" fill="#c8d8ea"/>
        <rect x="394" y="88" width="74" height="16" rx="8" fill="#224b8d"/>
        <text x="510" y="101" fill="#667085" font-size="10">lightweight</text>

        <path d="M334 59 H374" stroke="#224b8d" stroke-width="2.6"/>
        <path d="M365 53 L377 59 L365 65" fill="none" stroke="#224b8d" stroke-width="2.6"/>
      </g>

      <text x="34" y="378" fill="#344054" font-size="13" font-weight="700">Historical computation reuse for later-turn reasoning</text>
      <text x="34" y="400" fill="#7b8491" font-size="11">STAIR · frozen backbone · 12,288 trainable parameters</text>
    </svg>
  </a>

  <div class="paper-card-content">
    <div class="publication-title">
      <a href="https://arxiv.org/abs/2609.39394">Can Computation from Earlier Problems Help LLMs Solve New Ones?</a>
    </div>
    <div class="publication-authors">
      <strong>Jipei He</strong>, Wenhui Tan, Xiaoyi Yu, Enver Sangineto, Fiorenzo Parascandolo, Rita Cucchiara, Ruihua Song
    </div>
    <div class="publication-meta">arXiv, 2026</div>
    <p class="publication-summary">
      We study whether computation retained from earlier problems can help later reasoning, and introduce STAIR, a lightweight mechanism for reusing historical attention states.
    </p>
    <div class="publication-links">
      <a href="https://arxiv.org/abs/2609.39394">arXiv</a>
      <a href="https://arxiv.org/pdf/2609.39394">PDF</a>
      <a href="https://arxiv.org/html/2609.39394">HTML</a>
    </div>
  </div>
</div>

<span class="home-anchor" id="research"></span>

# Research Interests

- **LLM Reasoning** — reasoning mechanisms and inference-time computation.
- **Transformer Architecture Optimization** — efficient architectural design for large language and multimodal models.
- **Post-Training** — methods for improving reasoning and generalization after pretraining.
- **Multimodal AI Safety** — safety and robustness across modalities.
