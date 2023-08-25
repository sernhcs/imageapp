<template>
  <v-app>
    <!-- sidebar -->
    <Sidebar @selectOption="onSelectOption"></Sidebar>
    <v-main>
      <!-- cards -->
      <ImageGallery :isWithColor="isWithColor"></ImageGallery>
    </v-main>
  </v-app>
</template>

<script setup>
import Sidebar from './components/Sidebar.vue';
import ImageGallery from './components/ImageGallery.vue';
import { ref } from 'vue';

const isWithColor = ref(true);
const onSelectOption =(isColor)=>{
  isWithColor.value=isColor
}
</script>
