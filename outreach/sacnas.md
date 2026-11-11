---
layout: page
title: SACNAS
permalink: /outreach/sacnas/
---

[← Back to Outreach](/outreach)

<div class="gallery-header" aria-roledescription="carousel" aria-label="SACNAS photo gallery">
  <button class="gallery-nav gallery-prev" type="button" aria-label="Previous photos">&#8249;</button>
  <div class="gallery-track" tabindex="0">
{% for photo in site.data.sacnas_gallery %}    <figure class="gallery-slide" tabindex="0" role="button" aria-label="Enlarge photo">
      <img src="{{ photo.src }}" alt="{{ photo.alt }}"{% if forloop.first %}{% else %} loading="lazy"{% endif %}>
      {% if photo.caption != "" and photo.caption %}<figcaption>{{ photo.caption }}</figcaption>{% endif %}
    </figure>
{% endfor %}  </div>
  <button class="gallery-nav gallery-next" type="button" aria-label="Next photos">&#8250;</button>
</div>

**SACNAS** (Society for Advancement of Chicanos/Hispanics and Native Americans in Science) fosters the success of underrepresented students and scientists, from college students to professionals, through mentorship, community, and professional development. Its annual SACNAS conference brings thousands of students and researchers together each year.

I am the **Past President of the Graduate Student and Postdoctoral (GSPD) SACNAS Chapter at UC Davis**. During my time as president, we led outreach from middle school through undergrad across the Sacramento Valley, all led and facilitated by graduate students and postdocs. Some highlights include computer science workshops and environmental science lectures for high school students, round table discussions for community college students in collaboration with the MESA program, and participating in the [Avanza Rising Scholars Conference](https://excellence.ucdavis.edu/avanza-conference). We also hosted professional development events, like a [workshop on how to make a personal website using GitHub](/assets/files/personal-website-workshop-gspd-sacnas.pdf).

<dialog id="lightbox" aria-modal="true" aria-label="Photo viewer">
  <button class="lightbox-close" onclick="closeLightbox()" aria-label="Close photo viewer">&times;</button>
  <button class="lightbox-nav lightbox-prev" onclick="shiftLightbox(-1)" aria-label="Previous photo">&#8249;</button>
  <img id="lightbox-img" src="" alt="">
  <figcaption id="lightbox-caption"></figcaption>
  <button class="lightbox-nav lightbox-next" onclick="shiftLightbox(1)" aria-label="Next photo">&#8250;</button>
</dialog>

<script>
(function () {
  var wrap = document.querySelector('.gallery-header');
  var track = wrap.querySelector('.gallery-track');
  function by(dir) { track.scrollBy({ left: dir * track.clientWidth * 0.8, behavior: 'smooth' }); }
  wrap.querySelector('.gallery-prev').addEventListener('click', function () { by(-1); });
  wrap.querySelector('.gallery-next').addEventListener('click', function () { by(1); });
  track.addEventListener('keydown', function (e) {
    if (e.target !== track) return;
    if (e.key === 'ArrowRight') { e.preventDefault(); by(1); }
    if (e.key === 'ArrowLeft') { e.preventDefault(); by(-1); }
  });

  // ---- Enlarge on click ----
  var slides = Array.prototype.slice.call(track.querySelectorAll('.gallery-slide'));
  var dialog = document.getElementById('lightbox');
  var lbImg = document.getElementById('lightbox-img');
  var lbCap = document.getElementById('lightbox-caption');
  var current = 0;

  function show(i) {
    current = (i + slides.length) % slides.length;
    var img = slides[current].querySelector('img');
    var cap = slides[current].querySelector('figcaption');
    lbImg.src = img.currentSrc || img.src;
    lbImg.alt = img.alt;
    lbCap.textContent = cap ? cap.textContent : '';
  }
  window.closeLightbox = function () { dialog.close(); };
  window.shiftLightbox = function (d) { show(current + d); };

  slides.forEach(function (slide, i) {
    slide.addEventListener('click', function () { show(i); dialog.showModal(); });
    slide.addEventListener('keydown', function (e) {
      if (e.key === 'Enter' || e.key === ' ') { e.preventDefault(); show(i); dialog.showModal(); }
    });
  });
  dialog.addEventListener('click', function (e) { if (e.target === dialog) dialog.close(); });
  dialog.addEventListener('keydown', function (e) {
    if (e.key === 'ArrowRight') shiftLightbox(1);
    if (e.key === 'ArrowLeft') shiftLightbox(-1);
  });
  dialog.addEventListener('close', function () {
    // keep the gallery in step with the photo that was last viewed
    slides[current].scrollIntoView({ behavior: 'smooth', block: 'nearest', inline: 'center' });
  });
})();
</script>


## Honors &amp; Awards

<div class="awards-grid">

<div class="award-card">
<p class="award-name">Graduate Student Oral Presentation Award, Plant Sciences/Botany</p>
<p class="award-detail">SACNAS, National Diversity in STEM Conference, 2025 · <a href="https://www.sacnas.org/diversity-news/stem-students-honored-for-excellence-in-research-and-presentation-at-the-2025-ndistem-conference" target="_blank" rel="noopener">Read the announcement</a></p>
</div>

<div class="award-card">
<p class="award-name">Chapter Officer Leadership Retreat (COLOR) Participant Travel Award</p>
<p class="award-detail">SACNAS, National Diversity in STEM Conference, 2025</p>
</div>

<div class="award-card">
<p class="award-name">Chapter Officer Leadership Retreat (COLOR) Participant Travel Award</p>
<p class="award-detail">SACNAS, National Diversity in STEM Conference, 2024</p>
</div>

<div class="award-card">
<p class="award-name">Travel Scholarship Award</p>
<p class="award-detail">SACNAS, National Diversity in STEM Conference, 2023</p>
</div>

<div class="award-card">
<p class="award-name">General Member Award for Outstanding High School Outreach</p>
<p class="award-detail">Grad and Postdoc SACNAS Chapter at UC Davis, 2022–2023</p>
</div>

</div>

<hr class="section-divider">

## UC Davis Chapter

<div class="resource-stack">

  <div class="resource-item">
    <span class="res-icon">🌵</span>
    <div class="res-info">
      <p class="res-title">Graduate Student &amp; Postdoctoral SACNAS Chapter at UC Davis</p>
      <p class="res-desc">Our chapter's website, with events, mentorship, and professional development opportunities.</p>
    </div>
    <div class="res-action">
      <a class="explore-btn" href="https://gspdsacnasatucd.weebly.com/" target="_blank" rel="noopener">
        <span class="btn-icon">→</span> Visit Website
      </a>
    </div>
  </div>

</div>

<hr class="section-divider">

## National SACNAS

<div class="resource-stack">

  <div class="resource-item">
    <span class="res-icon">🌎</span>
    <div class="res-info">
      <p class="res-title">SACNAS National Website</p>
      <p class="res-desc">Society for Advancement of Chicanos/Hispanics and Native Americans in Science.</p>
    </div>
    <div class="res-action">
      <a class="explore-btn" href="https://www.sacnas.org/" target="_blank" rel="noopener">
        <span class="btn-icon">→</span> Visit Website
      </a>
    </div>
  </div>

  <div class="resource-item">
    <span class="res-icon">📍</span>
    <div class="res-info">
      <p class="res-title">Find Your Local Chapter</p>
      <p class="res-desc">Browse the SACNAS chapter directory to find a chapter near you.</p>
    </div>
    <div class="res-action">
      <a class="explore-btn" href="https://www.sacnas.org/chapters/chapter-directory" target="_blank" rel="noopener">
        <span class="btn-icon">→</span> Chapter Directory
      </a>
    </div>
  </div>

</div>
