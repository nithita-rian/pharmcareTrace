<template>
  <div class="min-h-screen">
    <header>header</header>
    <main class="mx-auto px-4 py-8 min-h-screen bg-white">
      <slot />
    </main>
    <footer class="bg-gray-100 inset-shadow-sm sticky bottom-0">
      <div class="px-4 py-4 flex items-center space-x-2 md:px-8 md:py-6">
        <Icon name="mdi:copyright" class="w-4 h-4 md:w-6 md:h-6 text-gray-400" />
        <span class="text-sm text-gray-600 md:text-base"> 2025 All Rights Reserved</span>
      </div>
    </footer>
  </div>
</template>

<script setup>

</script>

<style>

</style>