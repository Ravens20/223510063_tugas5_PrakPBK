<template>
  <q-header class="bg-blue-10 text-yellow-4">
    <q-toolbar>
      <q-toolbar-title class="text-yellow-4">
        Dindra Shop
      </q-toolbar-title>
      <!-- Navigation links -->
      <q-btn flat class="nav-btn" to="/">Home</q-btn>
      <q-btn flat class="nav-btn" to="/products">Products</q-btn>
      <q-btn flat class="nav-btn" to="/about">About</q-btn>
      <q-btn flat class="nav-btn" to="/contact">Contact</q-btn>
      <!-- Add a button to toggle the cart -->
    </q-toolbar>
  </q-header>
</template>

<script>
export default {
  methods: {
    toggleCart() {
      // Emit event untuk menampilkan atau menyembunyikan keranjang belanja
      this.$emit('toggle-cart');
    },
    closeCart() {
      // Emit event untuk menutup keranjang belanja
      this.$emit('close-cart');
    }
  }
}
</script>
<style scoped>
.nav-btn {
  color: #ffeb3b; /* Yellow color */
}
</style>
