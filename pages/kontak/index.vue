<template>
  <div class="container mt-5">
    <div class="row">
      <!-- Contact Form Column -->
      <div class="col-12 col-md-6 mb-4 d-flex">
        <div class="card flex-fill shadow">
          <div class="card-body">
            <form @submit.prevent="submitForm">
              <div class="mb-3">
                <label for="name" class="form-label">Nama Lengkap:</label>
                <input type="text" class="form-control" id="name" v-model="name" required />
              </div>

              <div class="mb-3">
                <label for="email" class="form-label">Email:</label>
                <input type="email" class="form-control" id="email" v-model="email" required />
              </div>

              <div class="mb-3">
                <label for="message" class="form-label">Pesan:</label>
                <textarea class="form-control" id="message" rows="4" v-model="message" required></textarea>
              </div>

              <div class="text-center">
                <button type="submit" class="btn btn-primary">Kirim Pesan</button>
              </div>
            </form>
          </div>
        </div>
      </div>

      <!-- School Info Column -->
      <div class="col-12 col-md-6 mb-4 d-flex">
        <div class="card flex-fill shadow">
          <div class="card-body">
            <h5 class="card-title">Informasi Sekolah</h5>
            <ul class="list-unstyled">
              <li>
                <strong>Alamat:</strong><br />
                Jl. Contoh No.123, Tasikmalaya, Jawa Barat
              </li>
              <li>
                <strong>Email:</strong><br />
                info@smkn4tasikmalaya.sch.id
              </li>
              <li>
                <strong>Telepon:</strong><br />
                (0265) 1234567
              </li>
              <li>
                <strong>Jam Operasional:</strong><br />
                Senin - Jumat, 08:00 - 16:00
              </li>
            </ul>
            <!-- <h6 class="mt-4">Media Sosial</h6>
            <div>
              <a href="https://facebook.com/smkn4tasikmalaya" target="_blank" class="btn btn-primary btn-sm me-2">
                <i class="fab fa-facebook-f"></i> Facebook
              </a>
              <a href="https://instagram.com/smkn4tasikmalaya" target="_blank" class="btn btn-danger btn-sm me-2">
                <i class="fab fa-instagram"></i> Instagram
              </a>
              <a href="https://twitter.com/smkn4tasikmalaya" target="_blank" class="btn btn-info btn-sm">
                <i class="fab fa-twitter"></i> Twitter
              </a>
            </div> -->
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const name = ref('');
const email = ref('');
const message = ref('');

const submitForm = () => {
  alert(`Pesan dari ${name.value} telah dikirim!`);
  name.value = '';
  email.value = '';
  message.value = '';
};
</script>

<style scoped>
.container {
  max-width: 100%;
  margin-bottom: 50px;
}

/* Adjust margin for small screens */
@media (max-width: 768px) {
  .mb-4 {
    margin-bottom: 15px;
  }
}
</style>