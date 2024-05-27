<template>
    <q-drawer v-model="showSidebar" show-if-above side="right" width="300px">
      <q-toolbar class="bg-blue-10 text-yellow-4">
        <q-toolbar-title>Cart</q-toolbar-title>
      </q-toolbar>
      <q-list>
        <q-item v-for="item in cartItems" :key="item.id">
          <q-item-section>{{ item.name }}</q-item-section>
          <q-item-section side="right">{{ item.price }}</q-item-section>
        </q-item>
      </q-list>
    </q-drawer>
  </template>
  
  <script>
  export default {
    props: {
      cartItems: {
        type: Array,
        required: true
      },
      showSidebar: {
        type: Boolean,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  /* Gaya tambahan jika diperlukan */
  </style>
  