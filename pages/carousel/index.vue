<template>

  <div id="carouselExample" class="carousel slide" data-bs-ride="carousel" data-bs-interval="3000">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="@/assets/img/s.jpg" class="d-block w-100 img-overlay" alt="Slide 1" />
        <div class="carousel-caption">
          <h3>Selamat Datang di SMKN 4 Tasikmalaya</h3>
        </div>
      </div>
      <div class="carousel-item">
        <img src="@/assets/img/s.jpg" class="d-block w-100 img-overlay" alt="Slide 2" />
        <div class="carousel-caption">
          <h3>Selamat Datang di SMKN 4 Tasikmalaya</h3>
        </div>
      </div>
      <div class="carousel-item">
        <img src="@/assets/img/k.jpg" class="d-block w-100 img-overlay" alt="Slide 3" />
        <div class="carousel-caption">
          <h3>Selamat Datang di SMKN 4 Tasikmalaya</h3>
        </div>
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExample" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>

<script setup>
</script>

<style scoped>
.img-overlay {
  opacity: 0.5;
  object-fit: cover;
}

.carousel-inner img {
  max-height: 70vh;
}

.carousel-caption {
  position: absolute;
  bottom: 20%;
  left: 50%;
  transform: translateX(-50%);
  color: white;
  text-align: center;
  padding: 15px 20px;
  border-radius: 10px;
}

.carousel-caption h3 {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 10px;
}

.carousel-caption p {
  font-size: 1.2rem;
}
</style>