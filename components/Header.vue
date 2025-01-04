<template>
  <div class="container-fluid">
    <div class="header row p-3">
      <div class="col-4 col-lg-1">
        <img src="../assets/img/Logo.png" alt="Logo SMKN 4 Tasikmalaya" class="img-fluid rounded">
      </div>
      <div class="col-8 col-lg-10">
        <h1 class="mb-0">SMKN 4 Tasikmalaya</h1>
        <address class="mb-0">
          Jl. Depok, Sukamenak, Purbaratu
        </address>
      </div>
    </div>

    <div class="p-2 nav-bar row">
      <div class="col-12">
        <ul class="d-flex list-unstyled mb-0 menu justify-content-end">
          <li class="me-3">
            <NuxtLink to="/" class="nav-link">Beranda</NuxtLink>
          </li>
          <li class="me-3 dropdown">
            <a href="#" class="btn dropdown-toggle">Profil Sekolah</a>
            <ul class="dropdown-menu">
              <li>
                <NuxtLink to="/profil/sejarah" class="dropdown-item">Sejarah</NuxtLink>
              </li>
              <li>
                <NuxtLink to="/profil/identitas" class="dropdown-item">Identitas Sekolah</NuxtLink>
              </li>
              <li>
                <NuxtLink to="/profil/visi" class="dropdown-item">Visi dan Misi</NuxtLink>
              </li>
              <li>
                <NuxtLink to="/profil/guru" class="dropdown-item">Guru dan Staff</NuxtLink>
              </li>
              <!-- <li>
                <NuxtLink to="/profil/data" class="dropdown-item">Data</NuxtLink>
              </li> -->
            </ul>
          </li>
          <li class="me-3">
            <NuxtLink to="/berita" class="nav-link">Berita</NuxtLink>
          </li>
          <li class="me-3">
            <NuxtLink to="/galeri" class="nav-link">Galeri</NuxtLink>
          </li>
          <li class="me-3 dropdown">
            <a href="#" class="btn dropdown-toggle">Siswa</a>
            <ul class="dropdown-menu">
              <li>
                <NuxtLink to="/siswa/eks" class="dropdown-item">Ekstrakurikuler</NuxtLink>
              </li>
              <li>
                <NuxtLink to="/siswa/kejuruan" class="dropdown-item">Kejuruan</NuxtLink>
              </li>
            </ul>
          </li>
          <li class="me-3">
            <NuxtLink to="/kontak" class="nav-link">Hubungi kami</NuxtLink>
          </li>
        </ul>
      </div>
    </div>
  </div>


</template>

<script setup>

</script>

<style scoped>
.container-fluid {
  background-color: #003366;
  color: white;
}

.nav-bar {
  background-color: #00509E;
}

.nav-link,
.btn {
  color: white;
  text-decoration: none;
  padding: 7px 20px;
}

.nav-link:hover,
.dropdown-item:hover,
.btn:hover {
  background-color: #004080;
  color: white;
  border-radius: 5px;
}

.dropdown-menu {
  display: none;
  position: absolute;
  margin-top: 0;
  padding: 0;
  background-color: #00509E;
}

.dropdown:hover .dropdown-menu {
  display: block;

}

.dropdown-menu .dropdown-item {
  color: white;
  background-color: #00509E;
  padding: 10px;
}

.dropdown-menu .dropdown-item:hover {
  background-color: #004080;
  color: white;
}
</style>