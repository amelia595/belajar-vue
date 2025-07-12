<template>
  <section class="text-center space-y-4 my-28">
  <!-- Rectangle abu-abu untuk “Testimonial Section” -->
  <div class="inline-block bg-[#f3f3f3] px-4 py-1 rounded-md mb-4">
    <span class="text-orange-500 font-semibold">Testimonial Section</span>
  </div>

  <!-- Judul besar -->
  <h2 class="text-3xl font-bold">What Our Customer Say</h2>

  <!-- Deskripsi -->
  <p class="text-gray-500 max-w-xl mx-auto">
    Lorem Ipsum is simply dummy text of the printing and typesetting industry.
  </p>

  <!-- Tambahan testimonial cards (yang kamu udah punya) -->

    <div class="grid md:grid-cols-3 gap-8 px-4 md:px-20 pt-7">
      <div
        v-for="(item, index) in testimonials"
        :key="index"
        class="bg-gray-100 p-6 rounded shadow-md"
      >
        <p class="text-4xl text-blue-500 mb-4">“</p>
        <p class="text-gray-700 mb-6">{{ item.quote }}</p>
        <div class="flex items-center gap-3">
          <img :src="item.image" alt="avatar" class="w-10 h-10 rounded-full" />
          <div>
            <p class="font-medium">{{ item.name }}</p>
            <p class="text-orange-400 text-sm">★★★★★</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    name: 'Ikhsan Mahendra',
    quote:
      'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
    image: 'src/assets/image/conan.jpg',
  },
  {
    name: 'Amelia Putri',
    quote:
      'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
    image: 'src/assets/image/haibara.jpeg',
  },
  {
    name: 'Pratomo Bowo',
    quote:
      'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
    image: 'src/assets/image/mouri.jpeg',
  },
]
</script>

<style scoped>
</style>
