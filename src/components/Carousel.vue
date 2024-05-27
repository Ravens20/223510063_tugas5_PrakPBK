<template>
    <q-carousel v-model="slide" swipeable animated infinite>
      <q-carousel-slide
        v-for="(slide, index) in slides"
        :key="index"
        :name="index"
        :img-src="slide.img"
      >
        <div class="absolute-bottom text-subtitle1 text-center">
          <q-btn color="white" icon="info" round />
          <span class="text-h5">{{ slide.label }}</span>
        </div>
      </q-carousel-slide>
    </q-carousel>
  </template>
  
  <script>
  export default {
    data() {
      return {
        slide: 0,
        slides: [
          {
            img: 'https://cms.disway.id/uploads/7bd53df9033507f011fdba75c0054156.jpg',
            label: 'First Slide'
          },
          {
            img: 'https://cdn.medcom.id/dynamic/content/2023/09/13/1612651/WGpXhEM8Ct.jpg?w=700',
            label: 'Second Slide'
          },
          {
            img: 'https://gambar.sgp1.digitaloceanspaces.com/wp-content/uploads/2020/07/1-68.jpg',
            label: 'Third Slide'
          }
        ]
      }
    }
  }
  </script>
  