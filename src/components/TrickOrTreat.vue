<script setup>
import tots from "../data/trickOrTreat";
</script>
<template>
  <section id="trick-or-treat" class="py-32 flex flex-col items-center">
    <h2 class="mt-10 mb-28 text-white text-6xl font-bold">Trick Or Treat</h2>
    <div class="grid grid-cols-3 gap-10">
      <div
        v-for="(tot, i) of tots"
        :key="tot.title"
        class="text-white bg-gradient-to-b grid place-items-center text-center p-8 rounded-md"
        :class="
          i === 1
            ? 'from-primary-200 to-primary-100 -translate-y-10'
            : 'from-primary-200/20 to-primary-200/10'
        "
      >
        <img :src="tot.image" alt="" />
        <h3 class="font-bold text-2xl">{{ tot.title }}</h3>
        <p class="w-[90%]">{{ tot.desc }}</p>
      </div>
    </div>
  </section>
</template>
