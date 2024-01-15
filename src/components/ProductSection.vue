<template>
  <Container>
    <div class="text-center text-4xl font-medium mb-7 pb-3 title relative">
      {{ title }}
    </div>

    <div
      class="grid grid-cols-2 xl:grid-cols-4 lg:grid-cols-3 items-center gap-x-4 gap-y-8 w-full"
    >
      <div
        class="flex flex-col group"
        v-for="(product, idx) in products"
        :key="idx"
      >
        <div class="relative w-full overflow-hidden">
          <img class="w-full" src="https://placehold.co/720x1080" alt="" />
          <div
            class="w-full grid place-items-center opacity-0 hover:opacity-100 h-full top-0 group-hover:backdrop-blur-sm transition-colors absolute z-10"
          >
            <div class="flex gap-3">
              <span
                class="cursor-pointer text-red-700 bg-white rounded-full p-2"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                  class="w-6 h-6"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z"
                  />
                </svg>
              </span>

              <span
                class="cursor-pointer text-red-700 bg-white rounded-full p-2"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                  class="w-6 h-6"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12z"
                  />
                </svg>
              </span>

              <span
                class="cursor-pointer text-red-700 bg-white rounded-full p-2"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                  class="w-6 h-6"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M7.217 10.907a2.25 2.25 0 100 2.186m0-2.186c.18.324.283.696.283 1.093s-.103.77-.283 1.093m0-2.186l9.566-5.314m-9.566 7.5l9.566 5.314m0 0a2.25 2.25 0 103.935 2.186 2.25 2.25 0 00-3.935-2.186zm0-12.814a2.25 2.25 0 103.933-2.185 2.25 2.25 0 00-3.933 2.185z"
                  />
                </svg>
              </span>
            </div>
          </div>
        </div>
        <span class="text-gray-600 text-center">{{ product.title }}</span>
        <div class="mx-auto">
          <span class="text-lg">${{ product.price }}</span>
          <span class="text-red-500 line-through">
            ${{ product.discount }}
          </span>
        </div>

        <div
          class="flex items-center gap-3 text-[10px] lg:text-xs mx-auto mt-2"
        >
          <div
            class="border px-3 py-1 rounded"
            v-for="size in product.sizes"
            :key="size"
          >
            {{ size }}
          </div>
        </div>
      </div>
    </div>

    <div class="flex w-full">
      <button class="bg-red-800 px-10 py-2 rounded mt-10 mx-auto text-white">
        View All
      </button>
    </div>
  </Container>
</template>

<script setup>
import Container from './Container.vue'

defineProps({
  title: String,
  products: Array,
})
</script>

<style scoped>
.title::after {
  @apply content-[''] absolute top-1/2 right-0 -translate-y-1/2 bg-gray-200 h-0.5 w-1/2;
}
.title::before {
  @apply content-[''] absolute top-1/2 left-0 -translate-y-1/2 bg-gray-200 h-0.5 w-1/2;
}
</style>
