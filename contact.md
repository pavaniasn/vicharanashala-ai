---
layout: page
title: Contact
parent: Others
permalink: /contact/
---

<div class="contact-grid">
  <div class="contact-details">
    <div class="contact-block">
      <span class="contact-label">Address</span>
      <p>VLED — Vicharanashala Lab for Education Design<br>
      Lab No. C-101, Super Academic Block<br>
      Indian Institute of Technology, Ropar<br>
      Rupnagar, Punjab 140001</p>
    </div>

    <div class="contact-block">
      <span class="contact-label">Email</span>
      <p><a href="mailto:dled@iitrpr.ac.in">dled@iitrpr.ac.in</a></p>
    </div>

    <div class="contact-block">
      <span class="contact-label">Phone</span>
      <p>+91-1881-242175</p>
    </div>

    <div class="contact-block">
      <span class="contact-label">LinkedIn</span>
      <p><a href="https://www.linkedin.com/company/vicharanashala" target="_blank" rel="noopener">linkedin.com/company/vicharanashala</a></p>
    </div>
  </div>

  <div class="contact-map">
    <iframe
      src="https://maps.google.com/maps?q=Indian+Institute+of+Technology+Ropar+Rupnagar+Punjab&output=embed"
      width="100%"
      height="100%"
      style="border:0; min-height: 300px;"
      allowfullscreen=""
      loading="lazy"
      referrerpolicy="no-referrer-when-downgrade"
      title="IIT Ropar location on Google Maps">
    </iframe>
  </div>
</div>

<style>
.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2.5rem;
  margin-top: 1.5rem;
  align-items: start;
}

.contact-details {
  display: flex;
  flex-direction: column;
  gap: 1.75rem;
}

.contact-label {
  display: block;
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #767676;
  margin-bottom: 0.4rem;
}

.contact-block p {
  margin: 0;
  line-height: 1.65;
  color: #1a1a1a;
}

.contact-block a {
  color: #1a1a1a;
  text-decoration: underline;
  text-underline-offset: 3px;
}

.contact-map {
  border-radius: 8px;
  overflow: hidden;
  border: 1px solid #e2e2de;
  height: 380px;
}

.contact-map iframe {
  display: block;
  width: 100%;
  height: 100%;
}

@media (max-width: 640px) {
  .contact-grid {
    grid-template-columns: 1fr;
  }
  .contact-map {
    height: 280px;
  }
}
</style>
