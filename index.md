---
layout: default
title: "Homepage"
---

<div class="p-4 p-md-5 mb-4 hero">
  <div class="container py-4">
    <div class="row align-items-center">
      <div class="col-lg-8">
        <span class="badge text-bg-primary">Conference</span>
        <!-- <span class="badge badge-accent ms-2 text-white">DeFi · Crypto</span> -->
        <h1 class="display-5 fw-bold mt-3">Decentralized Finance & Crypto Workshop @ Scuola Normale Superiore</h1>
        <p class="lead">A Workshop on Decentralized Finance and Crypto at the Intersection of Academia and Industry.</p>
        <ul class="list-unstyled">
          <li><strong>Date:</strong> <em>26/01/2026 - 28/01/2026</em></li>
          <li><strong>Location:</strong> Scuola Normale Superiore, Pisa (Italy)</li>
        </ul>
        <div class="d-flex gap-2 mt-3">
          <a class="btn btn-primary btn-lg" href="{{ '/registration/' | relative_url }}">Register</a>
          <a class="btn btn-outline-primary btn-lg" href="{{ '/submission/' | relative_url }}">Submit a Paper</a>
          <!--<a class="btn btn-outline-secondary btn-lg" href="{{ '/program/' | relative_url }}">See Program</a>-->
        </div>
      </div>
      <div class="col-lg-4 mt-4 mt-lg-0">
        <div class="text-center">
          <img
            src="{{ '/assets/img/sns_defi_logo.png' | relative_url }}"
            alt="Conference logo"
            class="img-fluid mb-3"
            style="max-height: 180px; object-fit: contain;">
          <h2 class="h5 mb-3">Important Dates</h2>
          <ul class="list-unstyled mb-0">
            <li><strong>Paper submission opens:</strong> <em>TBD</em></li>
            <li><strong>Submission deadline:</strong> <em>TBD</em></li>
            <li><strong>Notification to authors:</strong> <em>TBD</em></li>
            <li><strong>Registration deadline:</strong> <em>TBD</em></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</div>

<section>
  <h2 class="section-title">About</h2>
  <p>
    The Scuola Normale Superiore is proud to host this premier event about Decentralized Finance (DeFi) and Crypto. Our goal is to foster collaboration and spur innovation in this rapidly evolving field, bringing together experts from both academia and industry.
  </p>
</section>

<section class="mt-4">
  <h2 class="section-title">Topics of Interest</h2>
  <div class="topics-grid">
    <div class="topic-item">AMMs, liquidity provision, slippage and MEV</div>
    <div class="topic-item">Risk modeling and systemic risk in DeFi</div>
    <div class="topic-item">Market microstructure of crypto exchanges (CEX/DEX)</div>
    <div class="topic-item">Price discovery and volatility</div>
    <div class="topic-item">Token economics, governance, NFTs and digital assets</div>
    <div class="topic-item">Stablecoins and payment rails</div>
    <div class="topic-item">Agent-based modeling, econophysics, complexity science, and network effects in crypto ecosystems</div>
  </div>
</section>

<section class="mt-5">
  <h2 class="section-title">Sponsors</h2>
  <p class="text-muted">Logos coming soon&mdash;placeholders shown below.</p>
  <div class="sponsor-logos d-flex flex-wrap align-items-center gap-4">
    <span class="sponsor-placeholder">Sponsor logo placeholder</span>
    <span class="sponsor-placeholder">Sponsor logo placeholder</span>
    <span class="sponsor-placeholder">Sponsor logo placeholder</span>
  </div>
</section>

<section class="mt-5">
  <h2 class="section-title">Invited Speakers</h2>
  {% assign homepage_speakers = site.data.speakers | default: empty %}
  {% if homepage_speakers and homepage_speakers != empty %}
    <ul class="invited-speakers-list">
      {% for speaker in homepage_speakers %}
        <li>
          <strong>{{ speaker.name }}</strong>{% if speaker.affiliation %}, {{ speaker.affiliation }}{% endif %}
        </li>
      {% endfor %}
    </ul>
  {% else %}
    <p class="text-muted">Speaker lineup coming soon.</p>
  {% endif %}
</section>
