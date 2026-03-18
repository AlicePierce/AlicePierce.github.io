---
layout: page
title: Science Art Portfolio
---

I combine my love of plants and biology with illustration. Click any image to view it full size.

<div class="art-grid">

  <figure class="art-item" onclick="openLightbox(0)" tabindex="0" role="button" aria-label="View Arabidopsis illustration">
    <img src="/art-1.jpg" alt="Illustration of Arabidopsis thaliana">
    <figcaption>Arabidopsis</figcaption>
  </figure>

  <figure class="art-item" onclick="openLightbox(1)" tabindex="0" role="button" aria-label="View Rose illustration">
    <img src="/art-2.jpg" alt="Illustration of a rose">
    <figcaption>Rose</figcaption>
  </figure>

  <figure class="art-item" onclick="openLightbox(2)" tabindex="0" role="button" aria-label="View Hydrangea illustration">
    <img src="/art-3.jpg" alt="Illustration of a hydrangea">
    <figcaption>Hydrangea</figcaption>
  </figure>

</div>

<dialog id="lightbox" aria-modal="true" aria-label="Image viewer">
  <button class="lightbox-close" onclick="closeLightbox()" aria-label="Close image viewer">&times;</button>
  <button class="lightbox-nav lightbox-prev" onclick="shiftLightbox(-1)" aria-label="Previous image">&#8249;</button>
  <img id="lightbox-img" src="" alt="">
  <figcaption id="lightbox-caption"></figcaption>
  <button class="lightbox-nav lightbox-next" onclick="shiftLightbox(1)" aria-label="Next image">&#8250;</button>
</dialog>

<script>
const artItems = [
  { src: '/art-1.jpg', alt: 'Illustration of Arabidopsis thaliana', caption: 'Arabidopsis' },
  { src: '/art-2.jpg', alt: 'Illustration of a rose', caption: 'Rose' },
  { src: '/art-3.jpg', alt: 'Illustration of a hydrangea', caption: 'Hydrangea' },
];
let currentIndex = 0;
const dialog = document.getElementById('lightbox');

function openLightbox(index) {
  currentIndex = index;
  updateLightbox();
  dialog.showModal();
}

function closeLightbox() {
  dialog.close();
}

function shiftLightbox(direction) {
  currentIndex = (currentIndex + direction + artItems.length) % artItems.length;
  updateLightbox();
}

function updateLightbox() {
  const item = artItems[currentIndex];
  document.getElementById('lightbox-img').src = item.src;
  document.getElementById('lightbox-img').alt = item.alt;
  document.getElementById('lightbox-caption').textContent = item.caption;
}

// Close on backdrop click
dialog.addEventListener('click', function(e) {
  if (e.target === dialog) closeLightbox();
});

// Keyboard navigation
dialog.addEventListener('keydown', function(e) {
  if (e.key === 'ArrowRight') shiftLightbox(1);
  if (e.key === 'ArrowLeft') shiftLightbox(-1);
});

// Keyboard activation for grid items
document.querySelectorAll('.art-item').forEach(function(item, i) {
  item.addEventListener('keydown', function(e) {
    if (e.key === 'Enter' || e.key === ' ') {
      e.preventDefault();
      openLightbox(i);
    }
  });
});
</script>

<hr class="section-divider">

### See more on my [Instagram](https://www.instagram.com/alice.pipettes)
