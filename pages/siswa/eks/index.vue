<template>
  <h1 class="text-center">
    <b>Ekstrakurikuler SMKN 4 TASIKMALAYA</b>
  </h1>
  <div class="eks-container">
    <div class="eks-grid">
      <div class="card">
        <img src="@/assets/eks/pra.jpg" alt="Pramuka" class="img" />
        <h2 class="title">Pramuka</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/paskib.jpg" alt="Paskibra" class="img" />
        <h2 class="title">Paskibra</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/pd.jpg" alt="Perisai Diri" class="img" />
        <h2 class="title">Perisai Diri</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/bola.jpg" alt="Sepak Bola" class="img" />
        <h2 class="title">Sepak Bola</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/fut.jpg" alt="Futsal" class="img" />
        <h2 class="title">Futsal</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/voly.jpg" alt="Voly" class="img" />
        <h2 class="title">Voly</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/srl.jpg" alt="Safety Riding" class="img" />
        <h2 class="title">Safety Riding</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/baskett.jpg" alt="Basket" class="img" />
        <h2 class="title">Basket</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/irmaa.jpg" alt="Rohis" class="img" />
        <h2 class="title">Rohis (IRMA)</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/ec.jpg" alt="ec" class="img" />
        <h2 class="title">Englih Club</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/pub.jpg" alt="pub" class="img" />
        <h2 class="title">Pasukan Upacara Bendera</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/pmr.jpg" alt="pmr" class="img" />
        <h2 class="title">Palang Merah Remaja</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/art.jpg" alt="art" class="img" />
        <h2 class="title">Dance Art</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/osis.jpg" alt="osis" class="img" />
        <h2 class="title">Osis</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/it.jpg" alt="it" class="img" />
        <h2 class="title">IT Club</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/plh.jpg" alt="Basket" class="img" />
        <h2 class="title">Pecinta Lingkungan Hidup</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/pks.jpg" alt="Basket" class="img" />
        <h2 class="title">Polisi Keamanan Sekolah</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/bulu.jpg" alt="Basket" class="img" />
        <h2 class="title">Persatuan Bulu Tangkis</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/glp.jpg" alt="Basket" class="img" />
        <h2 class="title">Gerakan Laskar Pustaka</h2>
      </div>
      <div class="card">
        <img src="@/assets/eks/gt.jpg" alt="Basket" class="img" />
        <h2 class="title">Gak tau</h2>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style scoped>
.eks-container {
  padding: 20px;
  font-family: Arial, sans-serif;
  text-align: center;
  margin-bottom: 50px;
}

.eks-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

.card {
  background: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: scale(1.05);
  box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2);
}

.img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.title {
  padding: 10px;
  font-size: 18px;
  color: #555;
  font-weight: bold;
}
</style>