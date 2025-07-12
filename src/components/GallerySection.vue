<script setup>
// Props
defineProps({
  galleryImages: Array,
  promoCards: Array,
  icons: Object
})
</script>

<template>
  <section class="my-28 px-8">
    <!-- Section 3 Card Promo -->
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mt-10 mb-16">
      <div
        v-for="(card, index) in promoCards"
        :key="index"
        :class="`p-6 flex items-center justify-between rounded-md ${card.bg}`"
      >
        <div>
          <h3 class="text-lg font-semibold">{{ card.title }}</h3>
          <button class="mt-2 border border-black px-3 py-1 text-sm">Shop now</button>
        </div>
        <img :src="card.image" :alt="card.title" class="h-24" />
      </div>
    </div>

    <div class="text-center space-y-2 mb-12 pt-10px">
      <div class="inline-block bg-[#f3f3f3] px-4 py-1 rounded-md">
        <span class="text-orange-500 font-semibold">Check Our Collection</span>
      </div>
      <h2 class="text-3xl font-bold">Our Furniture Gallery</h2>
      <p class="text-gray-500">
        Lorem Ipsum is simply dummy text of the printing and typesetting industry.
      </p>

      <!-- Tombol filter dengan icon -->
      <div class="flex justify-center space-x-4 mt-6">
        <button class="border px-4 py-2 rounded-full text-purple-600 border-purple-600 flex items-center gap-2">
          <component :is="icons.IconAll" class="w-4 h-4" /> All
        </button>
        <button class="border px-4 py-2 rounded-full flex items-center gap-2">
          <component :is="icons.IconStar" class="w-4 h-4" /> Best Sellers
        </button>
        <button class="border px-4 py-2 rounded-full flex items-center gap-2">
          <component :is="icons.IconBag" class="w-4 h-4" /> New
        </button>
        <button class="border px-4 py-2 rounded-full flex items-center gap-2">
          <component :is="icons.IconClock" class="w-4 h-4" /> Up Coming
        </button>
      </div>
    </div>

    <!-- Gambar Gallery -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 px-4">
      <div v-for="(img, index) in galleryImages" :key="index">
        <img :src="img" alt="furniture" class="rounded-xl w-full h-[250px] object-cover" />
      </div>
    </div>
  </section>
</template>