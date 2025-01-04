<template>
  <!-- Carousel Section -->
  <div id="carouselExample" class="carousel slide" data-bs-ride="carousel" data-bs-interval="2000">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="@/assets/img/s.jpg" class="d-block w-100 img-overlay" alt="Slide 1" />
        <div class="carousel-caption">
          <h3>Selamat Datang di SMKN 4 Tasikmalaya</h3>
          <p>Generasi unggul dan berprestasi</p>
        </div>
      </div>
      <div class="carousel-item">
        <img src="@/assets/img/d.jpg" class="d-block w-100 img-overlay" alt="Slide 2" />
        <div class="carousel-caption">
          <h3>Fasilitas Modern</h3>
          <p>Kenyamanan belajar dengan fasilitas lengkap</p>
        </div>
      </div>
      <div class="carousel-item">
        <img src="@/assets/img/k.jpg" class="d-block w-100 img-overlay" alt="Slide 3" />
        <div class="carousel-caption">
          <h3>Kompetensi Terbaik</h3>
          <p>Mempersiapkan siswa untuk masa depan</p>
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

  <!-- Berita Terbaru Section -->
  <div class="container mt-5">
    <h1 class="text-center mb-4">Berita Terbaru</h1>
    <div class="row">
      <!-- Berita pertama di kiri -->
      <div class="col-md-6">
        <div v-for="(berita, index) in beritaListKiri" :key="index" class="mb-3 shadow-sm berita-card hover-effect">
          <a :href="berita.link" target="_blank" class="card-link-wrapper">
            <div class="card">
              <div class="row no-gutters">
                <div class="col-md-4">
                  <img :src="berita.foto" class="card-img" alt="Gambar Berita" />
                </div>
                <div class="col-md-8">
                  <div class="card-body">
                    <h5 class="card-title">{{ berita.judul }}</h5>
                    <h6 class="card-subtitle mb-2 text-muted">{{ berita.tanggal }}</h6>
                    <p class="card-text">{{ berita.deskripsi }}</p>
                  </div>
                </div>
              </div>
            </div>
          </a>
        </div>
      </div>

      <!-- Berita kedua di kanan -->
      <div class="col-md-6">
        <div v-for="(berita, index) in beritaListKanan" :key="'right-' + index"
          class="mb-3 shadow-sm berita-card hover-effect">
          <a :href="berita.link" target="_blank" class="card-link-wrapper">
            <div class="card">
              <div class="row no-gutters">
                <div class="col-md-4">
                  <img :src="berita.foto" class="card-img" alt="Gambar Berita" />
                </div>
                <div class="col-md-8">
                  <div class="card-body">
                    <h5 class="card-title">{{ berita.judul }}</h5>
                    <h6 class="card-subtitle mb-2 text-muted">{{ berita.tanggal }}</h6>
                    <p class="card-text">{{ berita.deskripsi }}</p>
                  </div>
                </div>
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>

  <!-- Sambutan Kepala Sekolah Section -->
  <section id="about" class="pt-5">
    <div class="mb-3 pb-5">
      <div class="row g-0">
        <div class="col-md-3 text-center">
          <img src="@/assets/img/kpl.png" class="img-fluid" alt="Kepala Sekolah" />
          <h2>Kepala Sekolah</h2>
          <h5>Kurniawan, S.Pd, M.Pd.</h5>
        </div>
        <div class="col-md-8">
          <div class="card-body">
            <h2 class="text-center">Sambutan Kepala Sekolah</h2>
            <p>Assalamu’alaikum warahmatullahi wabarakatuh,</p>
            <p>Salam sejahtera bagi kita semua. Puji syukur kita panjatkan ke hadirat Allah SWT atas segala limpahan
              rahmat dan karunia-Nya. Dengan penuh rasa bangga, saya menyampaikan sambutan hangat kepada seluruh
              pengunjung website resmi SMKN 4 Tasikmalaya.</p>
            <p>Website ini kami hadirkan sebagai media informasi, komunikasi, dan edukasi yang dapat diakses oleh siswa,
              orang tua, guru, serta masyarakat luas. Di sini, Anda dapat menemukan berbagai informasi terkait kegiatan
              sekolah, prestasi siswa, program unggulan, serta berita terbaru yang menjadi bagian dari perjalanan kami
              di dunia pendidikan.</p>
            <p>Kami berkomitmen untuk terus memberikan pelayanan terbaik demi mencetak generasi unggul, berkarakter, dan
              siap menghadapi tantangan masa depan. Harapan kami, kehadiran website ini dapat semakin mempererat
              hubungan antara sekolah, orang tua, dan masyarakat.</p>
            <p>Terima kasih atas kunjungan Anda. Jangan ragu untuk memberikan saran dan masukan demi pengembangan
              sekolah yang lebih baik.</p>
            <p>Wassalamu’alaikum warahmatullahi wabarakatuh.</p>
            <p>Hormat saya,</p>
            <p><strong>SMKN 4 Tasikmalaya</strong></p>
            <p>Kurniawan, S.Pd, M.Pd.</p>
          </div>
        </div>
      </div>
    </div>
  </section>


  <div class="page-container">
    
    <galeri />
    <dataa />

  </div>
</template>

<script setup>
import galeri from '~/pages/galeri/index.vue';
import dataa from '~/pages/data/index.vue';


import foto1 from '@/assets/berita/astra.jpg';
import foto2 from '@/assets/berita/gur.jpeg';
import foto3 from '@/assets/berita/jo.jpg';

const beritaListKiri = [
  {
    judul: 'SMKN 4 Tasikmalaya Gelar Job Fair 2023, Harapkan Angka Pengangguran di Tasikmalaya Berkurang',
    tanggal: '12/10/2024',
    foto: foto3,
    link: 'https://ruangatas.com/smkn-4-tasikmalaya-gelar-job-fair-2023-harapkan-angka-pengangguran-di-tasikmalaya-berkurang/'
  },
  {
    judul: 'Sinkronisasi Kurikulum SMKN 4 Tasikmalaya dengan Inovindo',
    tanggal: '09/07/2024',
    foto: foto2,
    link: 'https://inovindoacademy.com/berita/sinkronisasi-kurikulum-smkn-4-tasikmalaya-dengan-inovindo'
  },
  {
    judul: 'Astra Honda Resmikan Safety Riding Lab ke-7 di SMKN 4 Tasikmalaya, Kampanye Keselamatan Berkendara',
    tanggal: '20/05/2024',
    foto: foto1,
    link: 'https://inovindoacademy.com/berita/sinkronisasi-kurikulum-smkn-4-tasikmalaya-dengan-inovindo'
  }
];

const beritaListKanan = [...beritaListKiri];
</script>

<style scoped>

.img-overlay {
  opacity: 0.5;
  object-fit: cover;
}


.carousel-inner img {
  max-height: 70vh;
}

/* Styling untuk teks overlay */
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

/* Container utama */
.page-container {
  padding: 20px;
}

/* Gaya umum untuk setiap section */
.section {
  margin-bottom: 40px;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* Efek hover untuk card */
.hover-effect {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.hover-effect:hover {
  transform: scale(1.02);
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
}

.card-link-wrapper {
  text-decoration: none;
  color: inherit;
}

.card-link-wrapper:hover {
  text-decoration: none;
}
</style>
