<!-- components/ProductInformation.vue -->
<template>
    <div class="bg-white rounded-lg shadow-lg px-12 py-6">
        <h1 class="py-2 text-xl text-green-800 font-bold underline">
            ข้อมูลผลิตภัณฑ์
        </h1>
        <div v-if="product" class="space-y-2 text-base">
            <h2 class="text-lg font-bold">{{ product.name }}</h2>
            <div class="grid grid-cols-5">
                <span class="font-bold">เลขทะเบียน :</span>
                <span class="col-span-4 text-gray-600">{{ product.productCode }}</span>
            </div>
            <div class="grid grid-cols-5">
                <span class="font-bold">ส่วนประกอบ :</span>
                <span class="col-span-4 text-gray-600">{{ product.ingredients }}</span>
            </div>
            <div class="grid grid-cols-5">
                <span class="font-bold">ขนาดบรรจุ :</span>
                <span class="col-span-4 text-gray-600">{{ product.size }} {{ product.unit }}</span>
            </div>
            <div class="grid grid-cols-5">
                <span class="font-bold">คุณสมบัติ :</span>
                <span class="col-span-4 text-gray-600">{{ product.properties }}</span>
            </div>
        </div>
    </div>
</template>

<script setup>
const props = defineProps({
    product: Object,
});
</script>

<style></style>