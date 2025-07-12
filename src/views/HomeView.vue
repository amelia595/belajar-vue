<script setup>
import { IconKacamataPembesar, IconAll, IconStar, IconBag, IconClock } from '@/components/icons'
import { CardComponent } from '@/components'
import TestimonialSection from '@/components/TestimonialSection.vue'
import GallerySection from '@/components/GallerySection.vue'

import {
  g1, g2, g3, g4, g5, g6, g7, g8, g9, g10, g11, g12, g13, g14, g15,
  logo1, logo2, logo3, logo4, logo5
} from '@/assets/image'

const images = [g1, g2, g3, g4, g1, g2]
const logos = [logo1, logo2, logo3, logo4, logo5]
const galleryImages = [g6, g7, g8, g9, g10, g11]

const promoCards = [
  {
    title: 'Wooden Chair',
    image: g12,
    bg: 'bg-[#f8f8f8]',
  },
  {
    title: 'Bookcase',
    image: g13,
    bg: 'bg-[#efedfe]',
  },
  {
    title: 'Single Sofa',
    image: g14,
    bg: 'bg-[#fef1e8]',
  },
]

const barang = [
  {
    title: 'LifeStyle Green Chair',
    harga: 105.0,
    gambar: g1,
  },
  {
    title: 'LifeStyle Cupboard',
    harga: 185.0,
    gambar: g2,
  },
  {
    title: 'LifeStyle Desk',
    harga: 205.0,
    gambar: g3,
  },
  {
    title: 'LifeStyle Green Chair',
    harga: 105.0,
    gambar: g4,
  },
  {
    title: 'LifeStyle Cupboard',
    harga: 185.0,
    gambar: g5,
  },
  {
    title: 'LifeStyle Desk',
    harga: 205.0,
    gambar: g1,
  },
]

const galleryIcons = {
  IconAll,
  IconStar,
  IconBag,
  IconClock
}
</script>

<template>
  <main>
    <!-- Hero Section -->
    <section id="sectionHero" class="space-y-20">
      <div class="space-y-[27px]">
        <h1 class="text-7xl text-black font-medium text-center mt-60 mx-60">
          Transform your space, Elevate your style.
        </h1>
        <h2 class="text-xl text-center mx-60">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex error veritatis tempore quae
          magni in temporibus, maiores vel. Nobis, dolore quod. Excepturi, molestiae aliquam vel
          explicabo laborum autem velit nesciunt!
        </h2>
      </div>

      <div class="flex justify-center w-full">
        <div class="flex justify-center w-[667px] py-4 pr-4 pl-6 bg-gray-200">
          <IconKacamataPembesar class="m-4" />
          <input
            class="bg-gray-200 outline-none border border-gray-200 w-full"
            placeholder="Search your property"
          />
          <button class="bg-orange-600 p-3 text-white">Search</button>
        </div>
      </div>

      <!-- Images horizontal -->
      <div class="flex space-x-10">
        <div class="overflow-x-auto" v-for="gambar in images" :key="gambar">
          <img :src="gambar" alt="gambar" class="object-cover h-80 w-80" />
        </div>
      </div>

      <!-- Logo section -->
      <div class="flex justify-between">
        <div class="mx-4" v-for="logo in logos" :key="logo">
          <img :src="logo" alt="logo" class="object-cover" />
        </div>
      </div>
    </section>

   <!-- Product Card Section -->
<section id="card" class="my-20 w-full px-25">
  <!-- Bagian Heading -->
  <div class="text-center space-y-2 mb-12">
    <div class="inline-block bg-[#f3f3f3] px-4 py-1 rounded-md">
      <span class="text-orange-500 font-semibold">Check Our Product</span>
    </div>
    <h2 class="text-3xl font-bold pt-2">Crafted with excellent material</h2>
    <p class="text-gray-500 pt-2">
      Lorem Ipsum is simply dummy text of the printing and typesetting industry.
    </p>
  </div>

  <!-- Grid Produk -->
  <div class="w-full grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-10 ">
    <CardComponent
      v-for="(product, index) in barang"
      :key="index"
      :title="product.title"
      :harga="product.harga"
      :gambar="product.gambar"
    />
  </div>
</section>

    <!-- Testimonial -->
    <TestimonialSection />

    <!-- Gallery (with promoCards & icons) -->
    <GallerySection
      :gallery-images="galleryImages"
      :promo-cards="promoCards"
      :icons="galleryIcons"/>
  </main>
</template>