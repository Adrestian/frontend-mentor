<template>
  <div class="flex gap-6 h-36">
    <img :src="options.src" :alt="options.alt" class="aspect-[9/16]" />
    <div class="flex flex-col justify-between items-start">
      <h2 class="text-2xl sm:text-3xl font-extrabold text-grayish-blue">{{ options.id }}</h2>
      <h3 class="text-xl sm:text-2xl font-bold text-dark-blue">{{ options.title }}</h3>
      <p class="text-lg text-dark-grayish-blue">
        {{ options.description }}
      </p>
    </div>
  </div>
</template>
<script setup>
defineProps(["options"]);
</script>
