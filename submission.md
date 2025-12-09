---
layout: default
title: "Paper Submission"
permalink: /submission/
---

<h2 class="section-title">Call for Papers</h2>
<p>We invite extended abstracts (2–4 pages) and full papers on topics including but not limited to:
<ul>
  <li>Decentralized Finance protocols and smart contracts;</li>
  <li>Decentralized Exchanges and Automated Market Makers;</li>
  <li>Liquidity provision, slippage, and Maximal Extractable Value;</li>
  <li>Risk modeling and systemic risk in Decentralized Finance;</li>
  <li>Market microstructure of crypto exchanges (Centralized/Decentralized Exchanges);</li>
  <li>Agent-based modeling, econophysics, complexity science, and network effects in crypto ecosystems;</li>
  <li>Token economics, governance, NFTs, and digital assets;</li>
  <li>Blockchain economics;</li>
  <li>Interaction between regulatory authorities, cryptocurrencies, and stablecoins.</li>
</ul>
<p> The workshop does not have formal proceedings. Therefore, submissions of papers that have already been published or are under review elsewhere are welcome.
  
  All submissions will undergo peer review by the Scientific Committee. At least one author of accepted papers must register.</p>
  
<p> Please submit your work via the conference email: <a href="mailto:sns.defi@gmail.com">sns.defi@gmail.com</a>

<h2 class="section-title">Important Dates</h2>
{% assign homepage_deadlines = site.data.deadlines | default: empty %}
{% if homepage_deadlines and homepage_deadlines != empty %}
  <ul class="deadlines-list">
    {% for deadline in homepage_deadlines %}
      <li>
        {% if deadline.prev %}
          {{ deadline.name }}: <del>{{deadline.prev}}</del> <strong>{{ deadline.date }}</strong>
        {% else %}
          {{ deadline.name }}: <strong>{{ deadline.date }}</strong>
        {% endif %}
      </li>
    {% endfor %}
      <!--<li>Paper/Extended Abstract Submission Deadline: <strong>2025-12-01</strong></li>-->
    <!--<li><strong>Submission site:</strong> <a href="#" target="_blank" rel="noopener">EasyChair (coming soon)</a></li>-->
  </ul>
{% else %}
  <p class="text-muted">Deadlines lineup coming soon.</p>
{% endif %}


<!--
<h3>Templates</h3>
<ul>
  <li><a href="#" download>LaTeX Template (coming soon)</a></li>
  <li><a href="#" download>Word Template (coming soon)</a></li>
</ul>
-->
