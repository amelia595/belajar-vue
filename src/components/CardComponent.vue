<template>
  <div class="bg-white w-[290px] m-2 rounded-md">
    <!-- Gambar Produk -->
    <div class="bg-gray-100 rounded-t-md">
      <img :src="gambar" alt="gambar-produk" class="object-cover w-full h-64 p-4" />
    </div>

    <!-- Tombol Add to Cart -->
    <div class="flex justify-center py-4 space-x-2">
      <Cart class="text-orange-600" />
      <h1 class="text-orange-600 font-medium">Add cart</h1>
    </div>

    <!-- Title & Harga -->
    <div class="text-left px-4 pb-4">
      <h1 class="text-gray-800 text-base font-semibold">{{ props.title }}</h1>
      <h1 class="text-black font-bold text-md">${{ props.harga }}</h1>
    </div>
  </div>
</template>

<script setup>
import { Cart } from './icons'

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  harga: {
    type: Number,
    required: true,
  },
  gambar: {
    type: String,
    required: true,
  },
})
</script>