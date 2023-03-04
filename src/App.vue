<script setup>
import TheHeader from "@/components/TheHeader.vue";
</script>

<template>
  <div class="container mx-auto mt-8">
    <TheHeader />
    <RouterView />
    <scroll-to-top />
  </div>
</template>
