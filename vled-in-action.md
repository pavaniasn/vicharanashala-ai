---
layout: default
title: VLED in Action
permalink: /vled-in-action/
---

<div class="initiative-page-hero">
  <p class="home-label"><i class="ph ph-images"></i> &nbsp;GLIMPSES</p>
  <h1 class="initiative-page-h">VLED in Action</h1>
  <p class="initiative-page-tag">From people who walked into the lab to rooms we walked into — researchers, educators, and practitioners who've crossed paths with this work.</p>
</div>

<div class="moments-filter">
  <button class="moments-filter-btn active" data-filter="all">All</button>
  <button class="moments-filter-btn" data-filter="visit">Visits</button>
  <button class="moments-filter-btn" data-filter="conference">Conferences</button>
  <button class="moments-filter-btn" data-filter="event">Events</button>
</div>

<div class="moments-grid">
  {% for moment in site.data.moments %}
  <div class="moment-card" data-type="{{ moment.type }}">
    <div class="moment-img-wrap">
      <img src="{{ site.baseurl }}/assets/images/moments/{{ moment.image }}" alt="{{ moment.caption }}" class="moment-img" loading="lazy">
    </div>
    <div class="moment-body">
      <span class="moment-tag moment-tag--{{ moment.type }}">{{ moment.type }}</span>
      <p class="moment-caption">{{ moment.caption }}</p>
      <p class="moment-detail">{{ moment.detail }}</p>
      <p class="moment-date">{{ moment.date }}</p>
    </div>
  </div>
  {% endfor %}
</div>

<script>
  const btns = document.querySelectorAll('.moments-filter-btn');
  const cards = document.querySelectorAll('.moment-card');
  btns.forEach(btn => {
    btn.addEventListener('click', () => {
      btns.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;
      cards.forEach(card => {
        card.style.display = (filter === 'all' || card.dataset.type === filter) ? '' : 'none';
      });
    });
  });
</script>
