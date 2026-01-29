---
layout: default
title: "Homepage"
permalink: /
---

<div class="p-4 p-md-5 mb-4 hero">
  <div class="container py-4">
    <div class="row align-items-center">
      <div class="col-lg-8">
        <!-- <span class="badge text-bg-primary">Conference</span> -->
        <!-- <span class="badge badge-accent ms-2 text-white">DeFi · Crypto</span> -->
        <h1 class="display-5 fw-bold mt-3">Decentralized Finance & Crypto Workshop @ Scuola Normale Superiore</h1>
        <p class="lead">A Workshop on Decentralized Finance and Crypto at the Intersection of Academia and Industry.</p>
        <ul class="list-unstyled">
          <li><strong>Date:</strong> <em>26/01/2026 - 28/01/2026</em></li>
          <li><strong>Location:</strong> Scuola Normale Superiore, Pisa (Italy)</li>
        </ul>
        <div class="d-flex gap-2 mt-3">
          <a class="btn btn-primary btn-lg" href="{{ '/registration/' | relative_url }}">Register</a>
          <a class="btn btn-primary btn-lg" href="{{ '/submission/' | relative_url }}">Submit a Paper</a>
          <!-- <a class="btn btn-outline-primary btn-lg" href="{{ '/submission/' | relative_url }}">Submit a Paper</a> -->
          <!--<a class="btn btn-outline-secondary btn-lg" href="{{ '/program/' | relative_url }}">See Program</a>-->
        </div>
      </div>
      <div class="col-lg-4 mt-4 mt-lg-0">
        <div class="text-center">
          <img
            src="{{ '/assets/img/sns_defi_logo_2.png' | relative_url }}"
            alt="Conference logo"
            class="img-fluid mb-3"
            style="max-height: 180px; object-fit: contain;">
          <h2 class="h5 mb-3">Important Dates</h2>
          <ul class="list-unstyled mb-0">
          {% assign homepage_deadlines = site.data.deadlines | default: empty %}
          {% if homepage_deadlines and homepage_deadlines != empty %}
            <ul class="deadlines-list">
              {% for deadline in homepage_deadlines %}
                <li>
                  {% if deadline.text %}
                  <strong>{{ deadline.name }}</strong>: {{deadline.text}}
                  {% else %}
                    {% if deadline.prev %}
                    <strong>{{ deadline.name }}</strong>: <del>{{deadline.prev}}</del>   {{ deadline.date }}
                    {% else %}
                    <strong>{{ deadline.name }}</strong>: {{ deadline.date }}
                    {% endif %}
                  {% endif %}
                </li>
              {% endfor %}
            </ul>
          {% else %}
            <p class="text-muted">Deadlines lineup coming soon.</p>
          {% endif %}
            <!-- <li><strong>Paper submission opens:</strong> 2025-11-01</li>
            <li><strong>Submission deadline:</strong> 2025-12-01</li>
            <li><strong>Notification to authors:</strong> 2025-12-15</li>
            <li><strong>Registration deadline:</strong> 2026-01-15</li> -->
          </ul>
        </div>
      </div>
    </div>
  </div>
</div>

<section>
  <h2 class="section-title">About</h2>
  <p>
    The Scuola Normale Superiore is proud to host this premier event dedicated to Decentralized Finance (DeFi) and Crypto, bringing together leading voices from academia and industry to foster collaboration and spark innovation. Alongside discussions on the policy, technology, and market forces shaping the crypto ecosystem, the workshop shines a light on topics such as automated market makers, liquidity provision, and MEV; risk modeling and systemic fragility in DeFi; microstructure of centralized and decentralized exchanges; price discovery and volatility; token governance, NFTs and digital assets; stablecoins and emerging payment rails; and agent-based modeling, econophysics, and network effects in complex crypto systems.
  </p>
  Conference email: <p>Email: <a href="mailto:sns.defi@gmail.com">sns.defi@gmail.com</a></p>
</section>

<section class="mt-5">
  <h2 class="section-title">Last Edition</h2>
  {% assign last_edition_photos = site.static_files | where_exp: "file", "file.path contains '/photo/'" | where_exp: "file", "file.extname == '.jpg' or file.extname == '.jpeg' or file.extname == '.png' or file.extname == '.webp' or file.extname == '.gif'" | sort: "path" %}
  {% if last_edition_photos and last_edition_photos != empty %}
    <div id="lastEditionCarousel" class="carousel slide last-edition-carousel" data-bs-ride="carousel">
      <div class="carousel-indicators">
        {% for photo in last_edition_photos %}
          <button
            type="button"
            data-bs-target="#lastEditionCarousel"
            data-bs-slide-to="{{ forloop.index0 }}"
            class="{% if forloop.first %}active{% endif %}"
            {% if forloop.first %}aria-current="true"{% endif %}
            aria-label="Slide {{ forloop.index }}"></button>
        {% endfor %}
      </div>
      <div class="carousel-inner">
        {% for photo in last_edition_photos %}
          {% assign photo_alt = photo.name | split: '.' | first | replace: '_', ' ' | replace: '-', ' ' %}
          <div class="carousel-item {% if forloop.first %}active{% endif %}">
            <img src="{{ photo.path | relative_url }}" class="d-block w-100" alt="{{ photo_alt | escape }}">
          </div>
        {% endfor %}
      </div>
      <button class="carousel-control-prev" type="button" data-bs-target="#lastEditionCarousel" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#lastEditionCarousel" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
  {% else %}
    <p class="text-muted">Photos coming soon.</p>
  {% endif %}
</section>

<section class="mt-5">
  <h2 class="section-title">Invited Speakers</h2>
  {% assign homepage_speakers = site.data.speakers | default: empty %}
  {% if homepage_speakers and homepage_speakers != empty %}
    <ul class="invited-speakers-list">
      {% for speaker in homepage_speakers %}
        <li>
          <strong>{{ speaker.name }}</strong>{% if speaker.affiliation %}, {{ speaker.affiliation }}{% endif %}{% if speaker.affiliation2 %} & {{ speaker.affiliation2 }}{% endif %}
        </li>
      {% endfor %}
    </ul>
  {% else %}
    <p class="text-muted">Speaker lineup coming soon.</p>
  {% endif %}
</section>

<section class="mt-5">
  <h2 class="section-title">Important Dates</h2>
  {% assign homepage_deadlines = site.data.deadlines | default: empty %}
  {% if homepage_deadlines and homepage_deadlines != empty %}
    <ul class="deadlines-list">
      {% for deadline in homepage_deadlines %}
        <li>
          {% if deadline.text %}
          {{ deadline.name }}: <strong>{{deadline.text}}</strong>
          {% else %}
            {% if deadline.prev %}
            {{ deadline.name }}: <del>{{deadline.prev}}</del>   <strong>{{ deadline.date }}</strong>
            {% else %}
            {{ deadline.name }}: <strong>{{ deadline.date }}</strong>
            {% endif %}
          {% endif %}
        </li>
      {% endfor %}
        <!--<li>Paper/Extended Abstract Submission Deadline: <strong>2025-12-01</strong></li>-->
      <!--<li><strong>Submission site:</strong> <a href="#" target="_blank" rel="noopener">EasyChair (coming soon)</a></li>-->
    </ul>
  {% else %}
    <p class="text-muted">Deadlines lineup coming soon.</p>
  {% endif %}
</section>

<section class="mt-5">
  <h2 class="section-title">Sponsors</h2>
  <p class="text-muted">We gratefully acknowledge the contribution of various sponsors for financial support. In particular, the Workshop is supported by:</p>
  <ul class="sponsors-list">
    <li>PRIN2022 DD N. 104 of February 2, 2022 ”Liquidity and systemic risks in centralized and decentralized markets”, codice proposta 20227TCX5W - CUP J53D23004130006 funded by the European Union NextGenerationEU through the Piano Nazionale di Ripresa e Resilienza (PNRR).</li>
    <li>SoBigData.it receives funding from European Union – NextGenerationEU – National Recovery and Resilience Plan (Piano Nazionale di Ripresa e Resilienza, PNRR) – Project: “SoBigData.it – Strengthening the Italian RI for Social Mining and Big Data Analytics” – CUP B53C22001760006 – Prot. IR0000013 – Avviso n. 3264 del 28/12/2021.</li>
  </ul>
  <div class="sponsor-logos d-flex flex-wrap align-items-center gap-4">
    <img
      src="{{ '/assets/img/Logo_SoBigData it.svg' | relative_url }}"
      alt="SoBigData"
      height="80"
      class="sponsor-logo">
    <img
      src="{{ '/assets/img/prin.png' | relative_url }}"
      alt="PRIN"
      height="100"
      class="sponsor-logo">
    <img
      src="{{ '/assets/img/logo_unibo.png' | relative_url }}"
      alt="University of Bologna"
      height="42"
      class="sponsor-logo">
    <img
      src="{{ '/assets/img/orizzontale colore.jpg' | relative_url }}"
      alt="Scuola Normale Superiore"
      height="42"
      class="sponsor-logo">
  </div>
</section>
