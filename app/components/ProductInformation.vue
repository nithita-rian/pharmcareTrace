<!-- components/ProductInformation.vue -->
<template>
    <div class="bg-white rounded-lg shadow-lg px-8 md:px-12 py-8 space-y-4">
        <h1 class="text-xl text-green-800 font-bold underline">
            ข้อมูลผลิตภัณฑ์
        </h1>
        <div v-if="product" class="space-y-2 text-base">
            <h2 class="text-lg font-bold">{{ product.name }}</h2>
            <div class="grid grid-cols-2 md:grid-cols-5">
                <span class="font-bold">เลขทะเบียน :</span>
                <span class="md:col-span-4 text-gray-600">{{ product.productCode }}</span>
            </div>
            <div class="grid grid-cols-2 md:grid-cols-5">
                <span class="font-bold">เลขล็อต :</span>
                <span class="md:col-span-4 text-gray-600">{{ product.lotNumber }}</span>
            </div>
            <div class="grid grid-cols-2 md:grid-cols-5">
                <span class="font-bold">รหัสมาตรฐานสากล :</span>
                <span class="md:col-span-4 text-gray-600">{{ product.barcode }}</span>
            </div>
            <div class="grid grid-cols-2 md:grid-cols-5">
                <span class="font-bold">วันหมดอายุ :</span>
                <span class="md:col-span-4 text-gray-600">{{ product.exp }}</span>
            </div>
            <div class="grid grid-cols-2 md:grid-cols-5">
                <span class="font-bold">ส่วนประกอบ :</span>
                <span class="md:col-span-4 text-gray-600">{{ product.ingredients }}</span>
            </div>
            <div class="grid grid-cols-2 md:grid-cols-5">
                <span class="font-bold">ขนาดบรรจุ :</span>
                <span class="md:col-span-4 text-gray-600">{{ product.size }} {{ product.unit }}</span>
            </div>
            <div class="grid grid-cols-2 md:grid-cols-5">
                <span class="font-bold">คุณสมบัติ :</span>
                <span class="md:col-span-4 text-gray-600">{{ product.properties }}</span>
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