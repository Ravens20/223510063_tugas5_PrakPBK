<template>
  <div class="cart-container">
    <!-- Tombol keranjang untuk membuka dan menutup keranjang -->
    <q-btn
      class="cart-btn"
      color="primary"
      icon="shopping_cart"
      @click="toggleCart"
    />
    <!-- Konten keranjang belanja -->
    <q-drawer
      v-model="showCart"
      show-if-above
      side="right"
      width="300px"
    >
      <q-toolbar class="bg-blue-10 text-yellow-4">
        <q-toolbar-title>Cart</q-toolbar-title>
        <!-- Tambahkan tombol untuk menutup keranjang belanja -->
        <q-btn flat icon="close" @click="toggleCart" />
      </q-toolbar>
      <q-list>
        <!-- Daftar produk dalam keranjang belanja -->
        <q-item v-for="item in cartItems" :key="item.id">
          <q-item-section>{{ item.name }}</q-item-section>
          <q-item-section side="right">{{ item.price }}</q-item-section>
        </q-item>
      </q-list>
    </q-drawer>
  </div>
</template>

<script>
export default {
  props: {
    cartItems: {
      type: Array,
      required: true
    },
    modelValue: {
      type: Boolean,
      required: true
    }
  },
  data() {
    return {
      showCart: this.modelValue
    };
  },
  methods: {
    toggleCart() {
      // Toggle status tampilan keranjang
      this.showCart = !this.showCart;
    }
  }
}
</script>

<style scoped>
.cart-container {
  position: relative;
  z-index: 999;
}

/* Gaya untuk tombol keranjang */
.cart-btn {
  position: fixed;
  bottom: 70px; /* Sesuaikan dengan tinggi footer */
  right: 20px;
  z-index: 1000;
}
</style>
