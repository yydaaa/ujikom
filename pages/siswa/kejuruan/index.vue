<template>
  <div>
    <h1 class="fw-bold text-center">Kejuruan</h1>
    <div class="container my-5">
      <div class="row g-4">
        <div class="col-md-4">
          <div class="card text-center shadow hover-card">
            <div class="card-body">
              <img src="~/assets/jurusan/tkjt.jpg" alt="Teknik Komputer dan Jaringan" class="img-fluid mb-3">
              <h5 class="card-title mt-3">Teknik Komputer Jaringan dan Telekomunikasi</h5>
            </div>
          </div>
        </div>


        <div class="col-md-4">
          <div class="card text-center shadow hover-card">
            <div class="card-body">
              <img src="~/assets/jurusan/pplg.jpg" alt="Rekayasa Perangkat Lunak" class="img-fluid mb-3">
              <h5 class="card-title mt-3">Perkembangan Perangkat Lunak dan Game</h5>
            </div>
          </div>
        </div>


        <div class="col-md-4">
          <div class="card text-center shadow hover-card">
            <div class="card-body">
              <img src="~/assets/jurusan/tbsm.jpg" alt="Teknik dan Bisnis Sepeda Motor" class="img-fluid mb-3">
              <h5 class="card-title mt-3">Teknik dan Bisnis Sepeda Motor</h5>
            </div>
          </div>
        </div>


        <div class="col-md-4">
          <div class="card text-center shadow hover-card">
            <div class="card-body">
              <img src="~/assets/jurusan/dkv.jpg" alt="Desain Komunikasi Visual" class="img-fluid mb-3">
              <h5 class="card-title mt-3">Desain Komunikasi Visual</h5>
            </div>
          </div>
        </div>


        <div class="col-md-4">
          <div class="card text-center shadow hover-card">
            <div class="card-body">
              <img src="~/assets/jurusan/toi.jpg" alt="Teknik Otomasi Industri" class="img-fluid mb-3">
              <h5 class="card-title mt-3">Teknik Otomasi Industri</h5>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.card-body {
  padding: 1.5rem;
}

.card {
  margin-bottom: 1.5rem;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  height: 220px;
  max-width: 270px;
  margin-left: auto;
  margin-right: auto;

}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.img-fluid {
  max-height: 90px;
  width: 70px;
  object-fit: cover;
  border-radius: 8px;
}

.hover-card:hover {
  transform: scale(1.05);
}
</style>