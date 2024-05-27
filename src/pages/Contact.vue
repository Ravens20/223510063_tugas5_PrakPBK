<template>
  <q-page class="q-pa-md">
    <!-- Banner -->
    <div class="banner-container q-mb-md">
      <q-img
        src="https://i.pinimg.com/736x/8d/85/c4/8d85c4af3912d39f02923312f12f3832.jpg" 
        alt="Contact Us Banner"
        class="banner-image"
      >
        <div class="banner-text">
          <h1>Hubungi Kami</h1>
          <p>Butuh bantuan? Kami di sini untuk membantu Anda!</p>
        </div>
      </q-img>
    </div>

    <!-- Konten -->
    <div class="contact-content">
      <div class="contact-box">
        <h2>Kontak Kami</h2>
        <p>Silakan isi formulir di bawah ini dan kami akan menghubungi Anda sesegera mungkin.</p>
        
        <!-- Formulir Kontak -->
        <q-form @submit="onSubmit">
          <q-input filled v-model="name" label="Nama" class="q-mb-md" />
          <q-input filled v-model="email" label="Email" type="email" class="q-mb-md" />
          <q-input filled v-model="subject" label="Subjek" class="q-mb-md" />
          <q-input filled v-model="message" label="Pesan" type="textarea" autogrow class="q-mb-md" />
          <q-btn type="submit" label="Kirim" color="primary" />
        </q-form>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      email: '',
      subject: '',
      message: ''
    }
  },
  methods: {
    onSubmit() {
      // Lakukan sesuatu dengan data form, seperti mengirim ke server
      console.log('Form submitted', this.name, this.email, this.subject, this.message);
      // Reset form
      this.name = '';
      this.email = '';
      this.subject = '';
      this.message = '';
    }
  }
}
</script>

<style scoped>
.banner-container {
  position: relative;
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

.contact-content {
  margin-top: 20px;
  display: flex;
  justify-content: center;
}

.contact-box {
  width: 100%;
  max-width: 600px;
  border: 1px solid #ccc; /* Garis tepi */
  border-radius: 5px; /* Sudut bulat */
  padding: 20px; /* Ruang dalam kotak */
  background-color: #f9f9f9;
}

.contact-box h2 {
  font-size: 24px;
  font-weight: bold;
  color: #007bff; /* Warna biru */
  margin-bottom: 10px; /* Jarak antara judul dan konten */
}

.contact-box p {
  margin-bottom: 20px; /* Jarak bawah untuk paragraf */
}

.q-input {
  width: 100%;
}
</style>
