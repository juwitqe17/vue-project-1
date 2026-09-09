<script setup>
const artworks = [
  { src: '/images/DSC_4801.jpg', alt: 'naik', class: 'petirtaan artwork-1' },
  { src: '/images/DSC_4821.jpg', alt: 'Okta nyatet', class: 'petirtaan artwork-2' },
  { src: '/images/DSC_4789.jpg', alt: 'Kawasan suci', class: 'petirtaan artwork-3' },
  { src: '/images/DSC_4832.jpg', alt: 'DH liat atas', class: 'petirtaan artwork-4' },
  { src: '/images/DSC_4833.jpg', alt: 'DH di depan Kala', class: 'petirtaan artwork-5' },
  { src: '/images/DSC_4849.jpg', alt: 'D bertanya', class: 'petirtaan artwork-6' },
  { src: '/images/DSC_4855.jpg', alt: 'Kala nelen rahu', class: 'petirtaan artwork-7' },
  { src: '/images/DSC_4865.jpg', alt: 'bapak melati', class: 'petirtaan artwork-8' },
  { src: '/images/DSC_4888.jpg', alt: 'tembok woi', class: 'petirtaan artwork-9' },
  { src: '/images/DSC_4914.jpg', alt: 'foto bareng', class: 'petirtaan artwork-10' },
]
</script>

<template>
  <main class="">
    <section class="">
      <div class="gallery">
        <img
          v-for="artwork in artworks"
          :key="artwork.src"
          :src="artwork.src"
          :alt="artwork.alt"
          :class="[artwork.class, 'rounded-xl shadow-md']"
        />

        <span class="dot dot-1 bg-sky-700"></span>
        <span class="dot dot-2 bg-sky-400"></span>
        <span class="dot dot-3 bg-sky-700"></span>
        <span class="dot dot-4 bg-blue-400"></span>

      </div>
    </section>
  </main>
</template>

<style scoped>

.gallery {
  position: relative;
  width: 100%;
  max-width: 500px;
  aspect-ratio: 1 / 1;
  margin: 0 auto;
}

.petirtaan {
  position: absolute;
  object-fit: cover;
  display: block;
}

.artwork-1 {
  width: 31%;
  height: 24%;
  left: 0;
  top: 43%;
}

.artwork-2 {
  width: 35%;
  height: 34%;
  left: 14%;
  top: 4%;
}

.artwork-3 {
  width: 23%;
  height: 19%;
  left: 28%;
  top: 72%;
}

.artwork-4 {
  width: 18%;
  height: 27%;
  left: 54%;
  top: 11%;
}

.artwork-5 {
  width: 15%;
  height: 11%;
  left: 35%;
  top: 48%;
}

.artwork-6 {
  width: 40%;
  height: 28%;
  left: 55%;
  top: 45%;
}

.artwork-7 {
  width: 23%;
  height: 14%;
  left: 87%;
  top: 27%;
}

.artwork-8 {
  width: 35%;
  height: 23%;
  left: 67%;
  top: 81%;
}

.artwork-9 {
  width: 30%;
  height: 23%;
  left: -7%;
  top: 76%;
}

.artwork-10 {
  width: 40%;
  height: 24%;
  left: 75%;
  top:-2%;
}

.dot {
  position: absolute;
  display: block;
  width: 4%;
  aspect-ratio: 1;
  border-radius: 9999px;
}

.dot-1 {
  left: 5%;
  top: 18%;
}

.dot-2 {
  left: 107%;
  top: 70%;
}

.dot-3 {
  left: 110%;
  top: 78%;
  width: 2.5%;
}

@media (max-width: 768px) {
  .gallery {
    max-width: 420px;
  }
}
</style>