---
layout: default
---

<section class="hero" id="top">
  <div class="hero-inner">
    <p class="hero-eyebrow">IEEE GRSS · QUEST QC4EO Working Group</p>
    <h1>{{ site.event.full_title }}</h1>
    <div class="hero-meta">
      <div><strong>Dates</strong><span>{{ site.event.dates_display }}</span></div>
      <div><strong>Venue</strong><span>{{ site.event.venue_name }}, {{ site.event.venue_city }}</span></div>
      <div><strong>Format</strong><span>Invited talks · Poster session · Social dinner</span></div>
    </div>
    <div class="hero-actions">
      <a href="{{ site.event.registration_url }}" class="btn-primary" target="_blank" rel="noopener">Register now</a>
      <a href="#agenda" class="btn-secondary">View agenda</a>
    </div>
  </div>
</section>

<section id="about">
  <div class="section-inner">
    <p class="section-label">About</p>
    <div class="prose">
      <p>{{ site.event.acronym }} is organized by the <strong>QC4EO Working Group</strong>, part of the IEEE Geoscience and Remote Sensing Society (GRSS) <a href="https://www.grss-ieee.org/technical-committees/quantum-earth-science-and-technology-quest/" target="_blank" rel="noopener">QUEST</a> technical committee.</p>
      <p>The workshop focuses on quantum computing and quantum machine learning for Earth Observation. Its goal is to introduce students and early-career researchers to this rapidly growing field, encourage their involvement in research activities, and give an overview of the main international organizations and initiatives in quantum technologies — with a particular focus on future directions.</p>
      <p>The program includes invited talks of approximately one hour, a poster session, and a social dinner, designed to foster discussion and exchange among invited speakers, students, and early-career researchers.</p>
    </div>
  </div>
</section>

<section id="topics">
  <div class="section-inner">
    <p class="section-label">Covered Topics</p>
    <h2 class="section-title">What we'll cover</h2>
    <ul class="topics-list">
      {% for t in site.topics %}
        <li>{{ t }}</li>
      {% endfor %}
    </ul>
  </div>
</section>

<section id="agenda">
  <div class="section-inner">
    <p class="section-label">Agenda</p>
    <h2 class="section-title">Program</h2>

    <table class="agenda-table">
      <caption>Sunday, October 25 — Welcome</caption>
      <thead><tr><th>Time</th><th>Session</th></tr></thead>
      <tbody>
        <tr><td class="time">Afternoon</td><td>Welcome reception &amp; registration</td></tr>
      </tbody>
    </table>

    <table class="agenda-table">
      <caption>Scientific Program</caption>
      <thead>
        <tr><th>26 October 2026</th><th></th><th>27 October 2026</th><th></th></tr>
      </thead>
      <tbody>
        <tr><td class="time">9:00–9:30</td><td>Introduction</td><td class="time"></td><td></td></tr>
        <tr class="highlight"><td class="time">9:30–10:30</td><td>Keynote 1</td><td class="time">9:30–10:30</td><td>Keynote 4</td></tr>
        <tr class="break"><td class="time">10:30–11:00</td><td>Coffee Break</td><td class="time">10:30–11:00</td><td>Coffee Break</td></tr>
        <tr><td class="time">11:00–12:00</td><td>Keynote 2</td><td class="time">11:00–12:00</td><td>Keynote 5</td></tr>
        <tr class="highlight"><td class="time">12:00–13:00</td><td>Keynote 3</td><td class="time">12:00–13:00</td><td>Keynote 6</td></tr>
        <tr class="break"><td class="time">13:00–14:30</td><td>Lunch</td><td class="time">13:00–14:00</td><td>Lunch</td></tr>
        <tr><td class="time">14:30–17:00</td><td>Poster Session (+ coffee break at 15:30)</td><td class="time">14:00–15:00</td><td>Keynote 7</td></tr>
        <tr><td class="time">17:30–19:30</td><td>Walking together in Benevento</td><td class="time">15:00–16:00</td><td>Panel</td></tr>
        <tr><td class="time">20:00</td><td><strong>Gala Dinner</strong></td><td class="time">16:00–16:30</td><td>Closing Remarks</td></tr>
      </tbody>
    </table>

    <div class="callout">
      <h3>Poster session for students</h3>
      <p>Details on the award/prize for the best student poster — to be announced.</p>
    </div>
  </div>
</section>

<section id="speakers">
  <div class="section-inner">
    <p class="section-label">Speakers</p>
    <h2 class="section-title">Invited speakers</h2>
    <div class="people-grid">
      {% for s in site.speakers %}
        <div class="person-card">
          <img src="{{ s.photo | relative_url }}" alt="{{ s.name }}" class="person-photo">
          <p class="person-name">{{ s.name }}</p>
          <p class="person-affiliation">{{ s.affiliation }}</p>
          {% if s.talk_title %}<p class="person-bio"><em>{{ s.talk_title }}</em></p>{% endif %}
        </div>
      {% endfor %}
    </div>
  </div>
</section>

<section id="committee">
  <div class="section-inner">
    <p class="section-label">Organizing Committee</p>
    <h2 class="section-title">Committee</h2>
    <div class="people-grid">
      {% for o in site.organizers %}
        <div class="person-card">
          <img src="{{ o.photo | relative_url }}" alt="{{ o.name }}" class="person-photo">
          <p class="person-name">{{ o.name }}</p>
          <p class="person-web"><a href="{{ o.web }}" target="_blank" rel="noopener">About</a></p>
          <p class="person-affiliation">{{ o.affiliation }}</p>
          <p class="person-affiliation">{{ o.role }}</p>
          <p class="person-email"><a href="mailto:{{ o.email }}">{{ o.email }}</a></p>
        </div>
      {% endfor %}
    </div>
  </div>
</section>

<section id="venue">
  <div class="section-inner">
    <p class="section-label">Venue</p>
    <h2 class="section-title">{{ site.event.venue_name }}</h2>
    <div class="venue-grid">
      <div class="prose">
        <p>{{ site.event.venue_city }} — {{ site.event.venue_note }}.</p>
        <p>Accommodation list: <a href="#">[ACCOMMODATION_PDF_LINK]</a></p>
        <p>For any information, write to the committe emails provided above.</p>
      </div>
      <div class="venue-map">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3005.0978885099253!2d14.780158899999998!3d41.132388999999996!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x133a3a6dc20bbf77%3A0x8bf13fe91caf5c13!2sAuditorium%20Sant%27Agostino!5e0!3m2!1sen!2sen" loading="lazy"></iframe>
      </div>
    </div>
  </div>
</section>

<section id="gallery">
  <div class="section-inner">
    <p class="section-label">Gallery</p>
    <h2 class="section-title">Photos</h2>
    <div class="gallery-grid">
      <img src="{{ '/assets/img/gallery/placeholder1.jpg' | relative_url }}" alt="">
      <img src="{{ '/assets/img/gallery/placeholder2.jpg' | relative_url }}" alt="">
      <img src="{{ '/assets/img/gallery/placeholder3.jpg' | relative_url }}" alt="">
    </div>
  </div>
</section>