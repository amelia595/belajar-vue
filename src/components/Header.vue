<template>
  <div class="border-b border-gray-200 shadow flex justify-between py-[27px] px-24 bg-white">
    <div id="logo" class="">
      <a href="#sectionHero">
        <img :src="logoHeader" alt="logoHeader" />
      </a>
    </div>

    <div id="menu" class="flex space-x-14">
      <h1 class="text-xl"><a href="#card">Product</a></h1>
      <h1 class="text-xl">Services</h1>
      <h1 class="text-xl">Article</h1>
      <h1 class="text-xl">About Us</h1>
    </div>

    <div id="user" class="flex space-x-4">
      <Cart class="text-black" />
      <User />
    </div>
  </div>
</template>

<script setup>
import { logoHeader } from '@/assets/image'
import { Cart, User } from './icons'
</script>
