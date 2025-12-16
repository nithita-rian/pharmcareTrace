<!-- layouts/default.vue -->
<template>
    <div class="min-h-screen">
        <header>
            <div class="bg-[#468775] px-4 rounded-t-lg flex justify-end items-center gap-4">
                <h2 class="text-lg font-bold text-white">PharmCare Pharmaceutical</h2>
                <!-- <h2 class="text-blue-800">NECTEC</h2> -->
                <img src="/Logo_of_NECTEC.svg" alt="Logo of NECTEC" class="h-24 w-24"/>
            </div>
        </header>
        <main class="mx-auto px-4 py-8 min-h-screen bg-white">
            <slot></slot>
        </main>
        <footer class="bg-gray-100 inset-shadow-sm sticky bottom-0">
            <div class="px-4 py-4 flex items-center space-x-2 md:px-8 md:py-6">
                <Icon name="mdi:copyright" class="w-4 h-4 text-gray-400" />
                <span class="text-xs text-gray-600 md:text-sm"> 2025 All Rights Reserved</span>
            </div>
        </footer>
    </div>
</template>

<script setup>

</script>

<style></style>