<script setup>
import MobileMenuOpenIcon from "../components/icons/MobileMenuOpenIcon.vue";
import MobileMenuCloseIcon from "../components/icons/MobileMenuCloseIcon.vue";
import MainArticle from "../components/MainArticle.vue";
import SecondaryArticle from "../components/SecondaryArticle.vue";
import NewsCard from "../components/NewsCard.vue";
import { reactive } from "vue";
const NewsCardOptions = [
  {
    id: "01",
    title: "Reviving Retro PCs",
    description: "What happens when old PCs are given modern upgrades?",
    src: "/assets/images/image-retro-pcs.jpg",
    alt: "retro pc",
  },
  {
    id: "02",
    title: "Top 10 Laptops of 2022",
    description: "Our best picks for various needs and budgets",
    src: "/assets/images/image-top-laptops.jpg",
    alt: "gaming pc keyboard",
  },
  {
    id: "03",
    title: "The Growth of Gaming",
    description: "How the pandemic has sparked fresh opportunities",
    src: "/assets/images/image-gaming-growth.jpg",
    alt: "retro pc",
  },
];
const data = reactive({ isMenuOpen: false });
function handleCloseMenu() {
  data.isMenuOpen = false;
}
function handleClickOnMenuIcon() {
  console.log("click");
  data.isMenuOpen = !data.isMenuOpen;
}
</script>

<template>
  <div class="max-w-[1440px] mx-auto px-6">
    <header class="flex justify-between items-center py-4 mt-8 text-dark-grayish-blue">
      <img src="../../public/assets/images/logo.svg" alt="logo" />
      <ul class="items-center gap-12 hidden sm:flex">
        <li class="hover:cursor-pointer hover:text-soft-orange duration-300">Home</li>
        <li class="hover:cursor-pointer hover:text-soft-orange duration-300">News</li>
        <li class="hover:cursor-pointer hover:text-soft-orange duration-300">Popular</li>
        <li class="hover:cursor-pointer hover:text-soft-orange duration-300">Trending</li>
        <li class="hover:cursor-pointer hover:text-soft-orange duration-300">Categories</li>
      </ul>
      <div @click="handleClickOnMenuIcon()" class="block sm:hidden hover:cursor-pointer">
        <MobileMenuOpenIcon v-if="!data.isMenuOpen" />
      </div>
      <div class="fixed inset-0 z-[999] sm:hidden backdrop-brightness-50" v-if="data.isMenuOpen">
        <div
          class="absolute min-w-[280px] inset-y-0 right-0 bg-off-white transition-all duration-300"
        >
          <div class="text-right flex justify-end px-6 py-6" @click="handleCloseMenu()">
            <MobileMenuCloseIcon v-if="data.isMenuOpen" />
          </div>
          <ul class="text-2xl text-dark-grayish-blue capitalize mt-12">
            <li class="px-6 py-4">Home</li>
            <li class="px-6 py-4">News</li>
            <li class="px-6 py-4">Popular</li>
            <li class="px-6 py-4">Trending</li>
            <li class="px-6 py-4">Categories</li>
          </ul>
        </div>
      </div>
    </header>
    <main class="grid grid-cols-1 sm:grid-cols-3 gap-12">
      <section class="col-span-1 sm:col-span-2">
        <MainArticle />
      </section>
      <section class="col-span-1">
        <SecondaryArticle />
      </section>
      <NewsCard v-for="options in NewsCardOptions" :options="options" :key="options.id" />
    </main>
    <footer class="py-16">
      <div class="text-center text-dark-grayish-blue text-sm">
        &#169; 2023 A Random Frontend Mentor User
      </div>
    </footer>
  </div>
</template>
