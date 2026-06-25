---
layout: default
title: Our Story
permalink: /ourstory/
timeline:
  - month: July 2023
    icon: 🌱
    title: The Spark
    description: A small research initiative started to revolutionise Education Design.

  - month: October 2024
    icon: 🪔
    title: DLED is Born
    description: On Vijayadasami, the lab was formally named — Dhananjaya Lab for Education Design (DLED) at IIT Ropar.

  - month: December 2024
    icon: 💡
    title: The CBPAI Journey Begins
    description: CBPAI (Chalkboards to Chatbots, Pedagogy and AI), supported by UGC MMTTP, marked the lab's first major funding and enabled its national rollout.

  - month: February 2025
    icon: 🧑‍🏫
    title: GuruSetu Launched
    description: GuruSetu is launched as a re-envisioned ARPIT initiative, built on nine thematic pillars. It focuses on creating video content that departs from conventional formats—bringing in insights from experts rooted in real classroom experience, that resonates with educators.

  - month: July 2025
    icon: 🚀
    title: ViBe Unveiled at ABSS
    description: Our AI-enabled asynchronous learning platform was launched at Akhil Bharatiya Shiksha Samagam (ABSS) on the 5th anniversary of NEP 2020 by the Hon'ble Minister of Education—featuring mastery-based progression and attention-aware learning, delivered at an accessible cost of ₹7 per learner per hour.

  - month: October 2025
    split:
      - icon: ✨
        title: DLED Evolves into Vicharanashala
        description: DLED is renamed Vicharanashala Lab for Education Design, marking a new chapter in innovative, practice-driven educational research and development.
      - icon: 🫀
        title: Spandan Takes Identity
        description: Spandan enables real-time classroom interaction by generating contextual polls from live lectures—helping instructors gauge understanding and keep students actively engaged.

  - month: December 2025
    split:
      - icon: 🎓
        title: Vinternship Launch
        description: NPTEL Winter cohort launched — 423 learners enrolled under one Professor, 99.7% avg. progress of learners who were active in the cohort, 246,378 quiz attempts. Internship at national scale begins.
      - icon: 🖼️
        title: ViSlides — The First Show
        description: The First show of ViSlides, our tool where the audience steer the session, was staged for the first time in the ICPE Conference 2025.

  - month: January 2026
    split:
      - icon: 🌍
        title: VLED Global Speaker Series
        description: The Global Speaker Series brings educators together to exchange ideas, explore diverse perspectives, and foster collaborative learning on teaching practices, education systems, and emerging technologies.
      - icon: 🎙️
        title: "ViTalks: Conversations, Not Slides"
        description: ViTalks replace traditional webinars with interactive dialogue. The speaker sparks the idea, and participants drive the discussion. No scripts, no waiting until the end for questions—the conversation itself is the event, fostering reflection, inquiry, and insight beyond the classroom.

  - month: February 2026
    icon: 🪞
    title: "Vi-Chintan: Reflections in Action"
    description: Vi-Chintan offers fresh, human perspectives on education and AI through reflections, experiences, and insights—moving beyond recycled content to spark curiosity and thoughtful discussion.

  - month: March 2026
    icon: 🌾
    title: Fundamentals of AI with Agriculture Dataset
    description: Launched in March 2026, this course introduces AI concepts using real-world agriculture datasets, enabling learners to apply machine learning techniques to practical problems and gain hands-on experience in data-driven agriculture solutions.
---

<div class="story-intro">
  <p class="story-label"><i class="ph ph-book-open"></i> Our Story</p>
  <h1 class="story-h">From one conviction<br>to a national mission.</h1>
  <div class="story-cols">
    <p class="story-lead">Vicharanashala began in July 2023 as a small research initiative at IIT Ropar — a conviction that education could be designed more intentionally, more humanely, and at scale. What started as a single lab has grown into a national effort touching 10,000+ learners, 35+ faculty, and sending over 2,000 internship offer letters across India.</p>
    <p class="story-lead">The name says it all. <em>Vichara</em> means thought, inquiry, reflection. <em>Shala</em> means a hall — a place of gathering. Vicharanashala: a house of thinking where education isn't just delivered, but designed, questioned, and rebuilt from the ground up.</p>
  </div>
</div>

<div class="story-space">
  <p class="story-label"><i class="ph ph-map-pin"></i> The Space</p>
  <h2 class="story-section-h">Where thinking becomes practice.</h2>
  <div class="story-space-grid">
    <div class="story-space-text">
      <p>The lab is based at IIT Ropar in Punjab — one of India's newer IITs, set along the Sutlej in the Shivalik foothills. It's a campus still finding its shape, which suits us: we're building things here too.</p>
      <p>The physical lab is a workspace where whiteboards fill faster than they can be erased, a small team asks large questions, and the gap between research and real classrooms is taken seriously. Ideas don't leave here until they've been tried somewhere.</p>
    </div>
    <div class="story-space-img">
      <div class="story-space-placeholder">
        <i class="ph ph-image"></i>
        <span>Lab photo coming soon</span>
      </div>
    </div>
  </div>
</div>

<div class="story-reach">
  <p class="story-label"><i class="ph ph-map-pin"></i> Our Reach</p>
  <h2 class="story-section-h">Across India, city by city.</h2>
  <p class="story-reach-desc">Faculty reached through CBPAI and GuruSetu programs — {{ site.data.reach_cities | size }} cities across 28 states and union territories.</p>
  <div class="story-reach-legend">
    <span class="reach-legend-item"><span class="reach-dot reach-dot-faculty"></span> Faculty</span>
    <span class="reach-legend-item"><span class="reach-dot reach-dot-student"></span> Students</span>
  </div>
  <div id="reach-map"></div>
</div>

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"/>
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

<script>
var cities = [
  {% for city in site.data.reach_cities %}
  { name: "{{ city.city }}", state: "{{ city.state }}", lat: {{ city.lat }}, lng: {{ city.lng }}, type: "{{ city.type }}" }{% unless forloop.last %},{% endunless %}
  {% endfor %}
];

var map = L.map('reach-map', {
  center: [22.5, 82.0],
  zoom: 5,
  scrollWheelZoom: false,
  zoomControl: true
});

L.tileLayer('https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png', {
  attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> &copy; <a href="https://carto.com/">CARTO</a>',
  subdomains: 'abcd',
  maxZoom: 19
}).addTo(map);

var facultyStyle = { radius: 4, fillColor: '#e07020', color: '#fff', weight: 1, opacity: 1, fillOpacity: 0.85 };
var studentStyle = { radius: 4, fillColor: '#3ab7bf', color: '#fff', weight: 1, opacity: 1, fillOpacity: 0.85 };
var bothStyle    = { radius: 5, fillColor: '#8a5ab7', color: '#fff', weight: 1, opacity: 1, fillOpacity: 0.85 };

cities.forEach(function(c) {
  var style = c.type === 'student' ? studentStyle : c.type === 'both' ? bothStyle : facultyStyle;
  L.circleMarker([c.lat, c.lng], style)
    .bindTooltip('<strong>' + c.name + '</strong><br>' + c.state, { direction: 'top', offset: [0, -6] })
    .addTo(map);
});
</script>

<div class="story-timeline-intro">
  <p class="story-label"><i class="ph ph-clock-counter-clockwise"></i> The Timeline</p>
  <h2 class="story-section-h">How we got here.</h2>
</div>

{% include timeline.html %}

<style>
.story-intro {
  padding: 3rem 0 3.5rem;
  border-bottom: 1px solid #e2e2de;
  margin-bottom: 3.5rem;
}

.story-label {
  font-size: 0.72rem;
  font-weight: 500;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: #767676;
  margin-bottom: 1rem;
  display: flex;
  align-items: center;
  gap: 0.4rem;
}

.story-h {
  font-size: clamp(1.8rem, 4vw, 2.6rem);
  font-weight: 600;
  letter-spacing: -0.03em;
  line-height: 1.12;
  margin: 0 0 2rem 0;
}

.story-cols {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2.5rem;
}

.story-lead {
  font-size: 1rem;
  line-height: 1.78;
  color: #444;
  margin: 0;
}

/* Lab space */
.story-space {
  padding: 3rem 0;
  border-bottom: 1px solid #e2e2de;
  margin-bottom: 3.5rem;
}

.story-section-h {
  font-size: 1.4rem;
  font-weight: 600;
  letter-spacing: -0.02em;
  line-height: 1.25;
  margin: 0 0 2rem 0;
}

.story-space-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  align-items: start;
}

.story-space-text p {
  font-size: 0.95rem;
  line-height: 1.78;
  color: #444;
  margin: 0 0 1rem 0;
}

.story-space-text p:last-child { margin-bottom: 0; }

.story-space-img { border-radius: 6px; overflow: hidden; }

.story-space-placeholder {
  background: #efefec;
  border: 1px solid #e2e2de;
  border-radius: 6px;
  min-height: 220px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 0.6rem;
  color: #767676;
  font-size: 0.82rem;
}

.story-space-placeholder i { font-size: 2rem; }

/* Timeline intro */
.story-timeline-intro { margin-bottom: 0.5rem; }

@media (max-width: 600px) {
  .story-cols,
  .story-space-grid {
    grid-template-columns: 1fr;
    gap: 1.4rem;
  }
}
</style>
