<template>
  <q-page class="q-pa-md home-page">
    <!-- Banner -->
    <div class="banner-container q-mb-md">
      <q-img
        src="https://assets.ggwp.id/2022/05/Beli-Diamond-Mobile-Legend-featured-640x360.jpg" 
        alt="Home Banner"
        class="banner-image"
      >
        <div class="banner-text">
          <h1>Selamat Datang di Dindra Shop</h1>
          <p>Temukan produk terbaik dengan harga terbaik hanya di Dindra Shop!</p>
        </div>
      </q-img>
    </div>

    <!-- Konten -->
    <div class="content-container q-mt-lg">
      <div class="section">
        <h2 class="section-title">Produk Unggulan</h2>
        <p class="section-description">Lihat koleksi produk unggulan kami yang paling diminati pelanggan.</p>
        <Carousel />
      </div>

      <div class="section q-mt-lg">
        <h2 class="section-title">Tentang Kami</h2>
        <p class="section-description">Dindra Shop adalah toko online terpercaya yang menyediakan berbagai macam produk berkualitas tinggi dengan harga terjangkau.</p>
      </div>

      <div class="section q-mt-lg">
        <h2 class="section-title">Kontak Kami</h2>
        <p class="section-description">Butuh bantuan? Hubungi kami kapan saja melalui halaman kontak kami.</p>
        <q-btn flat color="primary" @click="$router.push('/contact')">Hubungi Kami</q-btn>
      </div>
    </div>
  </q-page>
</template>

<script>
import Carousel from '../components/Carousel.vue'

export default {
  components: {
    Carousel
  }
}
</script>

<style scoped>
/* General styling for home page */
.home-page {
  font-family: 'Roboto', sans-serif;
}

/* Banner styling */
.banner-container {
  position: relative;
  border-radius: 8px;
  overflow: hidden;
}

.banner-image {
  height: 400px;
}

.banner-text {
  position: absolute;
  bottom: 20px;
  left: 20px;
  color: white;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.6);
}

.banner-text h1 {
  font-size: 36px;
  margin: 0;
}

.banner-text p {
  font-size: 18px;
  margin: 5px 0 0;
}

/* Content styling */
.content-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
  background-color: #ffffff;
  border-radius: 8px;
}

.section {
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.section-title {
  font-size: 24px;
  font-weight: bold;
  color: #007bff;
  margin-bottom: 10px;
}

.section-description {
  font-size: 16px;
  color: #333;
  margin-bottom: 20px;
}
</style>
