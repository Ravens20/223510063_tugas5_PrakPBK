<template>
  <div class="product-grid">
    <q-card
      v-for="product in products"
      :key="product.id"
      class="q-mb-md"
      style="width: 300px;"
      @mouseover="hoverEffect(product.id)"
      @mouseleave="resetEffect(product.id)"
    >
      <q-img :src="product.image" :alt="product.name" />
      <q-card-section>
        <div class="text-h6">{{ product.name }}</div>
        <div class="text-subtitle1">{{ product.price }}</div>
      </q-card-section>
      <q-card-actions align="right">
        <q-btn flat label="Add to Cart" color="primary" @click="addToCart(product)" />
      </q-card-actions>
    </q-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        { id: 1, name: 'Starlight', price: 'Rp.150.000', image: './image/diamond.webp' },
        { id: 2, name: 'Twilight Pass', price: 'Rp.79.000', image: 'path-to-your-image2.jpg' },
        { id: 3, name: '100DM', price: 'Rp.32.000', image: 'path-to-your-image3.jpg' },
        { id: 4, name: '130DM', price: 'Rp.40.000', image: 'path-to-your-image4.jpg' },
        { id: 5, name: '150DM + 30DM Bonus', price: 'Rp.50.000', image: 'path-to-your-image5.jpg' },
        { id: 6, name: '175DM + 30DM Bonus', price: 'Rp.60.000', image: 'path-to-your-image6.jpg' },
        { id: 7, name: '200DM + 30DM Bonus', price: 'Rp.70.000', image: 'path-to-your-image7.jpg' },
        { id: 8, name: '225DM + 30DM Bonus', price: 'Rp.80.000', image: 'path-to-your-image8.jpg' },
        { id: 9, name: '280DM + 30DM Bonus', price: 'Rp.90.000', image: 'path-to-your-image9.jpg' },
        { id: 10, name: '320DM + 30DM Bonus', price: 'Rp.100.000', image: 'path-to-your-image10.jpg' },
      ]
    };
  },
  methods: {
    addToCart(product) {
      // Emit event untuk menambahkan produk ke keranjang belanja
      this.$emit('add-to-cart', product);
    }
  }
}
</script>


<style scoped>
.q-card {
  width: 300px;
  margin-bottom: 20px;
  transition: transform 0.3s ease; /* Animasi perubahan ukuran */
}

.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px; /* Jarak antar kolom */
  justify-items: center;
}

/* Gaya tambahan jika diperlukan */
</style>
