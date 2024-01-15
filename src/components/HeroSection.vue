<template>
  <div>
    <img src="https://placehold.co/1920x600" loading="lazy" />

    <div class="flex items-center gap-5 py-16 px-16 justify-between">
      <div
        class="flex flex-col justify-center items-center"
        v-for="category in categories"
        :key="category.name"
      >
        <img
          class="rounded-full w-44"
          :src="category.img"
          alt=""
          loading="lazy"
        />
        <span class="text-lg font-semibold">{{ category.name }}</span>
      </div>
    </div>

    <div>
      <div class="flex items-center justify-between gap-4 px-16">
        <div class="w-1/2">
          <img loading="lazy" src="https://placehold.co/1920x1080" />
        </div>
        <div class="w-1/2">
          <img loading="lazy" src="https://placehold.co/1920x1080" />
        </div>
      </div>

      <div class="flex items-center justify-between gap-4 px-16 py-4">
        <div class="w-1/3">
          <img loading="lazy" src="https://placehold.co/1920x1080" />
        </div>
        <div class="w-1/3">
          <img loading="lazy" src="https://placehold.co/1920x1080" />
        </div>
        <div class="w-1/3">
          <img loading="lazy" src="https://placehold.co/1920x1080" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const categories = [
  {
    name: "Men's T-Shirts",
    img: 'https://placehold.co/300x300',
  },
  {
    name: "Women's Wear",
    img: 'https://placehold.co/300x300',
  },
  {
    name: 'Winter Collections',
    img: 'https://placehold.co/300x300',
  },
  {
    name: 'Hooded T-Shirts',
    img: 'https://placehold.co/300x300',
  },
  {
    name: 'Polo Neek T-Shirts',
    img: 'https://placehold.co/300x300',
  },
  {
    name: 'Full Sleeves T-Shirts',
    img: 'https://placehold.co/300x300',
  },
]
</script>
