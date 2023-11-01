<script setup>
import category1 from "../assets/images/category/category1-img.png";
import category2 from "../assets/images/category/category2-img.png";
import category3 from "../assets/images/category/category3-img.png";

const categories = [
  {
    title: "Ghost",
    image: category1,
    desc: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id id consequat, eu faucibus nulla. Ultrices mattis lacus, sed maecenas nascetur.",
  },
  {
    title: "Witch",
    image: category2,
    desc: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id id consequat, eu faucibus nulla. Ultrices mattis lacus, sed maecenas nascetur.",
  },
  {
    title: "Pumpkin",
    image: category3,
    desc: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id id consequat, eu faucibus nulla. Ultrices mattis lacus, sed maecenas nascetur.",
  },
];
</script>

<template>
  <section id="category" class="pt-30 flex flex-col items-center py-32">
    <h2 class="my-10 text-white text-6xl font-bold">Category</h2>
    <div class="grid grid-cols-3 place-items-center">
      <div v-for="category of categories" :key="category.title">
        <div class="grid place-items-center text-white text-center gap-5">
          <div :class="{ 'pt-14': category.title !== 'Witch' }">
            <img :src="category.image" alt="" />
          </div>
          <h3 class="text-3xl font-semibold">{{ category.title }}</h3>
          <div class="w-3/4">
            {{ category.desc }}
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="grid grid-flow-col grid-cols-2 gap-10 items-center">
    <div class="p-10">
      <img src="../assets/images/category2-img.png" alt="category2-img" />
    </div>

    <div class="translate-y-12" id="about">
      <h2 class="text-6xl font-bold text-white">What's that</h2>
      <div class="flex items-center gap-5">
        <h2 class="text-6xl font-bold text-white">Halloween</h2>
        <img src="../assets/images/head2-img.png" alt="head2-img" />
      </div>
      <p class="mt-12 text-lg text-white w-[60%]">
        Halloween or Hallowe'en, also known as Allhalloween, All Hallows' Eve,
        or All Saints' Eve, is a celebration observed in many countries on 31
        October, the eve of the Western Christian feast of All Hallows' Day.
      </p>
    </div>
  </section>
</template>
