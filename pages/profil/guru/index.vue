<template>
  <div class="container mt-5">
    <h1 class="text-center mb-4">Daftar Guru</h1>
    <div class="card-body">
      <div class="row gap-5">
        <div v-for="(guru, index) in displayedGuruList" :key="index" class="card guru-card mx-3">
          <div class="card-body">
            <img :src="guru.foto" class="card-img-top" alt="Foto Guru" />
            <h5 class="card-title">{{ guru.nama }}</h5>
            <p class="card-text">{{ guru.mapel }}</p>
          </div>
        </div>
      </div>
    </div>
    <div class="text-center mt-4" v-if="displayedGuruList.length < guruList.length">
      <button @click="loadMore" class="btn btn-primary">Lainnya</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

import guru1 from "@/assets/guru/deni.jpg";
import guru2 from "@/assets/guru/arip.jpg";
import guru3 from "@/assets/guru/gandi.jpg";
import guru4 from "@/assets/guru/zul.jpg";
import guru5 from "@/assets/guru/taufik.jpg";
import guru6 from "@/assets/guru/andi.jpg";
import guru7 from "@/assets/guru/adi.jpg";
import guru8 from "@/assets/guru/lisye.jpg";
import guru9 from "@/assets/guru/vina.jpg";
import guru10 from "@/assets/guru/tini.jpg";
import guru11 from "@/assets/guru/sri.jpg";
import guru12 from "@/assets/guru/lisna.jpg";
import guru13 from "@/assets/guru/joy.jpg";
import guru14 from "@/assets/guru/suminar.jpg";


const guruList = [
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru1 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru2 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru3 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru4 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru5 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru6 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru7 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru8 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru9 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru10 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru11 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru12 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru13 },
  { nama: "Yuda Apriana Salam ", mapel: "B . Inggris", foto: guru14 },
];


const displayedGuruList = ref(guruList.slice(0, 4)); 

const loadMore = () => {
  const currentLength = displayedGuruList.value.length;
  const nextGuruList = guruList.slice(currentLength, currentLength + 4);
  displayedGuruList.value.push(...nextGuruList);
};
</script>

<style scoped>
.container {
  margin-bottom: 70px;
}

.guru-card {
  min-width: 262px;
  max-width: 230px;
  flex: 0 0 auto;
  border: 1px solid #ddd;
  border-radius: 5px;
}

.card-img-top {
  width: 100%;
  height: 220px;
  object-fit: cover;
}

.card-body {
  text-align: center;
}
</style>