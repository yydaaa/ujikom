<template>
  <div class="container py-5">
    <h1 class="text-center mb-4">Galeri</h1>
    <div class="row g-4">
      <div class="col-md-4" v-for="(image, index) in images" :key="index">
        <div class="card h-100 image-card shadow">
          <img :src="image.src" :alt="image.alt" class="card-img-top" />
          <div class="card-body">
            <h5 class="card-title">{{ image.title }}</h5>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import foto1 from '../assets/galeri/177.jpg';
import foto2 from '../assets/galeri/p.jpg';
import foto3 from '../assets/galeri/makan.jpg';
import foto4 from '../assets/galeri/mpls.jpg';
import foto5 from '../assets/galeri/b.jpg';
import foto6 from '../assets/galeri/p5.jpg';

const images = [
  { src: foto1, alt: 'Gambar 1', title: '17 Agustus 2024' },
  { src: foto2, alt: 'Gambar 2', title: 'Porseni 2024' },
  { src: foto5, alt: 'Gambar 3', title: 'Hari Guru' },
  { src: foto4, alt: 'Gambar 4', title: 'MPLS 2024' },
  { src: foto3, alt: 'Gambar 5', title: 'Makan Bersama' },
  { src: foto6, alt: 'Gambar 6', title: 'P5 tema "Kebekerjaan"' },
];
</script>



<style scoped>
.card-img-top {
  object-fit: cover;
  max-height: 250px;
}

.card-body {
  text-align: center;
}
</style>