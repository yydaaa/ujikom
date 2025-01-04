<template>
  <div class="container mt-4">
    <!-- Header -->
    <div class="card mb-4">
      <div class="card-body">
        <h2 class="mb-4 text-center">Data Statistik</h2>
      </div>
    </div>

    <!-- Statistik -->
    <div class="row">
      <div v-for="(stat, index) in statistics" :key="index" class="col-md-3 mb-4">
        <div class="card">
          <div class="card-body text-center">
            <h6 class="mb-1">{{ stat.title }}</h6>
            <h3 class="font-weight-bold">{{ stat.value }}</h3>
          </div>
        </div>
      </div>
    </div>

    <!-- Diagram Lingkaran dalam Card -->
    <div class="row justify-content-center mt-4">
      <div class="col-md-3 mb-4">
        <div class="card">
          <div class="card-header text-center bg-primary text-white">
            Rekap Jenis Kelamin Siswa
          </div>
          <div class="card-body text-center">
            <canvas id="genderChart"></canvas>
          </div>
        </div>
      </div>

      <div class="col-md-3 mb-4">
        <div class="card">
          <div class="card-header text-center bg-success text-white">
            Rekap Status Kepegawaian Guru
          </div>
          <div class="card-body text-center">
            <canvas id="teacherChart"></canvas>
          </div>
        </div>
      </div>

      <div class="col-md-5 mb-4">
        <div class="card">
          <div class="card-header text-center bg-warning text-white">
            Rekap Siswa Per Jurusan
          </div>
          <div class="card-body text-center">
            <canvas id="adminChart"></canvas>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted } from "vue";
import Chart from "chart.js/auto";

console.log('Komponen Data dimuat');
// Data statistik
const statistics = [
  { title: "Jumlah Siswa", value: 1116 },
  { title: "Jumlah Rombel", value: 34 },
  { title: "Jumlah Guru", value: 60 },
  { title: "Jumlah Tenaga Administrasi", value: 10 },
];


onMounted(() => {
  const genderCtx = document.getElementById("genderChart").getContext("2d");
  new Chart(genderCtx, {
    type: "pie",
    data: {
      labels: ["Laki-laki", "Perempuan"],
      datasets: [
        {
          data: [662, 448],
          backgroundColor: ["#42A5F5", "#FF6384"],
        },
      ],
    },
    options: {
      responsive: true,
      plugins: {
        legend: {
          position: "bottom",
        },
      },
    },
  });


  const teacherCtx = document.getElementById("teacherChart").getContext("2d");
  new Chart(teacherCtx, {
    type: "pie",
    data: {
      labels: ["PNS", "NON PNS"],
      datasets: [
        {
          data: [35, 25],
          backgroundColor: ["#8E24AA", "#FF7043",],
        },
      ],
    },
    options: {
      responsive: true,
      plugins: {
        legend: {
          position: "bottom",
        },
      },
    },
  });

  const adminCtx = document.getElementById("adminChart").getContext("2d");
  new Chart(adminCtx, {
    type: "bar",
    data: {
      labels: ["TKJT", "PPLG", "TBSM", "DKV", "TOI"],
      datasets: [
        {
          data: [129, 123, 110, 52, 32],
          backgroundColor: ["#0000FF", " #008000", "#FF0000", "#FF5722", "#808080"],
        },
      ],
    },
    options: {
      responsive: true,
      scales: {
        x: {
          beginAtZero: true,
        },
        y: {
          beginAtZero: true,
        },
      },
      plugins: {
        legend: {
          display: false,
        },
      },
    },
  });
});
</script>

<style scoped>
.container {
  margin-bottom: 100px;
}

.font-weight-bold {
  font-weight: 700 !important;
}


.card {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  border-radius: 10px;

}

.card-header {
  font-weight: 600;
}


canvas {
  max-width: 100%;
  height: 250px;
}
</style>