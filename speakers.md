---
layout: default
title: "Invited Speakers"
permalink: /speakers/
---

<h2 class="section-title">Invited Speakers</h2>

<div class="row row-cols-1 row-cols-lg-2 g-4">
  {% assign speakers = site.data.speakers | default: empty %}
  {% if speakers and speakers != empty %}
    {% for s in speakers %}
      <div class="col">
        <div class="card h-100 shadow-sm">
          <div class="row g-0 align-items-center">
            <div class="col-auto p-3">
              {% assign img = s.image | default: '/assets/img/speakers/placeholder.png' %}
              <img
                src="{{ img | relative_url }}"
                alt="{{ s.name }}"
                class="speaker-avatar rounded-circle border"
                loading="lazy">
            </div>
            <div class="col">
              <div class="card-body">
                <h3 class="h5 mb-1">{{ s.name }}</h3>
                {% if s.affiliation %}<p class="text-muted mb-2">{{ s.affiliation }}</p>{% endif %}
                {% if s.bio %}<p class="mb-3">{{ s.bio }}</p>{% endif %}
                <div class="d-flex gap-2 flex-wrap">
                  {% if s.email %}
                    <a class="btn btn-outline-primary btn-sm"
                       href="mailto:{{ s.email | uri_escape }}">Email</a>
                  {% endif %}
                  {% if s.website %}
                    <a class="btn btn-outline-secondary btn-sm"
                       href="{{ s.website }}" target="_blank" rel="noopener">Website</a>
                  {% endif %}
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    {% endfor %}
  {% else %}
    <div class="col">
      <div class="alert alert-secondary" role="alert">
        Speaker list coming soon.
      </div>
    </div>
  {% endif %}
</div>
