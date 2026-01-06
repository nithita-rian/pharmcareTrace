<!-- components/TraceInformation.vue -->
<template>
    <div class="bg-white rounded-lg shadow-lg p-8">
        <div class="grid grid-cols-1 md:grid-cols-12 gap-16">

            <ProductImages class="md:col-span-5" :images="images" />

            <div class="md:col-span-7">
                <h2 class="text-xl font-bold underline mb-4 text-gray-900">สรุปการตรวจสอบย้อนกลับ</h2>

                <div v-if="product" class="space-y-2 text-base">
                    <div class="grid grid-cols-3">
                        <span class="font-bold">สินค้า :</span>
                        <span class="col-span-2 text-gray-600">{{ product.name }}</span>
                    </div>
                    <div class="grid grid-cols-3">
                        <span class="font-bold">ผลิตโดย :</span>
                        <span class="col-span-2 text-gray-600">{{ product.produced }}</span>
                    </div>
                    <div class="grid grid-cols-3">
                        <span class="font-bold">รหัสสินค้า :</span>
                        <span class="col-span-2 text-gray-600">{{ product.productCode }}</span>
                    </div>
                    <div class="grid grid-cols-3">
                        <span class="font-bold">รหัสบรรจุภัณฑ์ :</span>
                        <span class="col-span-2 text-gray-600">{{ product.packageId }}</span>
                    </div>
                    <div class="grid grid-cols-3">
                        <span class="font-bold">รหัสการขนส่ง :</span>
                        <span class="col-span-2 text-gray-600">{{ product.transportId }}</span>
                    </div>
                    <div class="grid grid-cols-3">
                        <span class="font-bold">วันที่ผลิต :</span>
                        <span class="col-span-2 text-gray-600">{{ product.produceDate }}</span>
                    </div>
                    <div class="grid grid-cols-3">
                        <span class="font-bold">ผู้จัดจำหน่าย :</span>
                        <span class="col-span-2 text-gray-600">{{ product.distributor }}</span>
                    </div>
                    <div class="grid grid-cols-3">
                        <span class="font-bold">วันที่บรรจุ :</span>
                        <span class="col-span-2 text-gray-600">{{ product.packDate }}</span>
                    </div>
                    <div class="grid grid-cols-3">
                        <span class="font-bold">วันที่จัดส่ง :</span>
                        <span class="col-span-2 text-gray-600">{{ product.shipDate }}</span>
                    </div>
                    <div class="grid grid-cols-3">
                        <span class="font-bold">ประเภทการขนส่ง :</span>
                        <span class="col-span-2 text-gray-600">{{ product.transportType }}</span>
                    </div>
                    <div class="grid grid-cols-3">
                        <span class="font-bold">หมายเลขตู้คอนเทนเนอร์ :</span>
                        <span class="col-span-2 text-green-800 font-bold">{{ product.containerNo }}</span>
                    </div>
                    <div class="grid grid-cols-3">
                        <span class="font-bold">หมายเลขติดตาม :</span>
                        <span class="col-span-2 text-gray-600">{{ product.trackingNo }}</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>

const props = defineProps({
    product: Object,
    images: {
        type: Array,
        default: () => []
    }
});
</script>

<style></style>