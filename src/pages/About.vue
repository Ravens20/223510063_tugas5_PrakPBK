<template>
  <q-page class="q-pa-md">
    <!-- Banner -->
    <div class="banner-container q-mb-md">
      <q-img
        src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/6f7eaccb-10b8-4a0a-bddc-f09a7200aa36/dah41rb-52513dda-f244-4da9-9924-96656a272647.jpg/v1/fill/w_1024,h_576,q_75,strp/cod___youtube_banner_by_ambientflush_dah41rb-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzZmN2VhY2NiLTEwYjgtNGEwYS1iZGRjLWYwOWE3MjAwYWEzNlwvZGFoNDFyYi01MjUxM2RkYS1mMjQ0LTRkYTktOTkyNC05NjY1NmEyNzI2NDcuanBnIiwiaGVpZ2h0IjoiPD01NzYiLCJ3aWR0aCI6Ijw9MTAyNCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS53YXRlcm1hcmsiXSwid21rIjp7InBhdGgiOiJcL3dtXC82ZjdlYWNjYi0xMGI4LTRhMGEtYmRkYy1mMDlhNzIwMGFhMzZcL2FtYmllbnRmbHVzaC00LnBuZyIsIm9wYWNpdHkiOjk1LCJwcm9wb3J0aW9ucyI6MC40NSwiZ3Jhdml0eSI6ImNlbnRlciJ9fQ.WnHXq3pEBd1TxKO6Qpko9QgobKlvL8jmZof1-uXzOPA" 
        alt="Banner Image"
        class="banner-image"
      >
        <div class="banner-text">
          <h1>Selamat Datang di Dindra Shop</h1>
          <p>Belanja online terbaik dengan kualitas dan harga terbaik.</p>
        </div>
      </q-img>
    </div>

    <!-- Konten -->
    <div class="about-content">
      <!-- Paragraf 1: Tentang Dindra Shop -->
      <div class="about-section">
        <div class="about-box">
          <h2>Tentang Dindra Shop</h2>
          <p>
            Dindra Shop adalah destinasi belanja online terbaik untuk Anda. Kami menyediakan berbagai macam produk berkualitas dari berbagai kategori, mulai dari fashion hingga elektronik.
          </p>
        </div>
      </div>

      <!-- Paragraf 2: Kelebihan Dindra Shop -->
      <div class="about-section">
        <div class="about-box">
          <h2>Kelebihan Dindra Shop</h2>
          <p>
            Kelebihan Dindra Shop adalah kemudahan dan kenyamanan dalam berbelanja. Dengan antarmuka pengguna yang intuitif, pelanggan dapat dengan mudah menemukan produk yang mereka inginkan. Selain itu, kami menawarkan layanan pelanggan yang responsif untuk membantu pelanggan dalam setiap langkah dari proses pembelian.
          </p>
        </div>
      </div>

      <!-- Paragraf 3: Keamanan dan Keandalan -->
      <div class="about-section">
        <div class="about-box">
          <h2>Keamanan dan Keandalan</h2>
          <p>
            Kami juga bangga dengan keamanan dan keandalan transaksi di Dindra Shop. Kami menggunakan teknologi enkripsi terbaru untuk melindungi data pribadi pelanggan dan mengamankan setiap transaksi pembayaran. Dengan demikian, pelanggan dapat berbelanja dengan aman dan nyaman di platform kami.
          </p>
        </div>
      </div>

      <!-- Paragraf 4: Layanan dan Promosi -->
      <div class="about-section">
        <div class="about-box">
          <h2>Layanan dan Promosi</h2>
          <p>
            Kami menawarkan berbagai promosi dan diskon menarik serta program loyalitas untuk membalas kepercayaan pelanggan kami. Kami percaya bahwa kepuasan pelanggan adalah kunci kesuksesan kami, dan kami berkomitmen untuk terus meningkatkan layanan kami untuk memenuhi kebutuhan belanja online Anda.
          </p>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
}
</script>
<style scoped>
/* Gaya untuk banner */
.about-banner {
  position: relative;
  height: 300px;
  overflow: hidden;
}

.banner-container {
  position: relative;
}

.about-banner-image {
  width: 100%;
  height: auto;
  object-fit: cover;
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

.about-banner-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: rgba(0, 0, 0, 0.5); /* Overlay dengan opacity 0.5 */
  color: #fff; /* Warna teks putih */
  text-align: center;
}

.about-banner-title {
  font-size: 36px;
  font-weight: bold;
  margin-bottom: 10px;
}

.about-banner-subtitle {
  font-size: 24px;
}

/* Gaya untuk konten tentang */
.about-content {
  margin-top: 20px;
  font-size: 16px;
  line-height: 1.6;
  color: #333; /* Warna teks */
}
.about-content h2 {
  font-size: 24px;
  font-weight: bold;
  color: #007bff; /* Warna biru */
  margin-bottom: 20px;
}

.banner-text p {
  font-size: 18px;
  margin: 5px 0 0;
}

.about-content p {
  margin-bottom: 20px;
  text-align: justify; /* Ratakan teks ke kanan dan kiri */
}


.about-content p:last-child {
  margin-bottom: 0;
}

.about-content p::first-letter {
  font-size: 28px; /* Ukuran huruf kapital pertama */
  font-weight: bold; /* Tebal */
  color: #007bff; /* Warna biru */
  margin-right: 5px; /* Jarak antara huruf kapital dan teks lainnya */
}

.about-section {
  margin-bottom: 30px; /* Jarak antar bagian */
}


.about-box {
  border: 1px solid #ccc; /* Garis tepi */
  border-radius: 5px; /* Sudut bulat */
  padding: 20px; /* Ruang dalam kotak */
}

.about-box h2 {
  font-size: 24px;
  font-weight: bold;
  color: #007bff; /* Warna biru */
  margin-bottom: 10px; /* Jarak antara judul dan konten */
}

.about-box p {
  margin-bottom: 0; /* Hapus margin bawah */
}
</style>
