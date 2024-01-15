<template>
  <AppHeader />
  <HeroSection />

  <ProductSection title="Trending T-Shirts" :products="products" />
  <ProductSection title="Featured Products" :products="newProducts" />
  <img src="https://placehold.co/1920x600" loading="lazy" />
  <ProductSection title="New Products" :products="newProducts" />
  <ProductSection title="Best Selling Products" :products="newProducts" />
  <AppFooter />
</template>

<script setup>
import AppHeader from '@/components/AppHeader.vue'
import HeroSection from '@/components/HeroSection.vue'
import ProductSection from '@/components/ProductSection.vue'
import AppFooter from '@/components/AppFooter.vue'
import { products, newProducts } from '@/data/products'
</script>
