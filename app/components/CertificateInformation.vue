<!-- components/ProductInformation.vue -->
<template>
    <div class="bg-white rounded-lg shadow-lg px-12 py-8 space-y-4">
        <h1 class="text-xl text-green-800 font-bold underline">
            ใบรับรอง (Certification)
        </h1>
        <div class="flex justify-center">
            <ProductImages class="md:col-span-5 w-full md:w-2/3" :images="images" />
        </div>
    </div>
</template>

<script setup>
const props = defineProps({
    images: {
        type: Array,
        default: () => []
    }
});
</script>

<style></style>