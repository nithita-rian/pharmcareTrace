<!-- TraceInformation.vue -->
<template>
    <div class="bg-white rounded-lg shadow-lg p-6">
        <div class="grid grid-cols-1 md:grid-cols-12 gap-8">

            <div class="md:col-span-5 flex flex-col items-center justify-center">
                <div class="w-full p-2 bg-gray-50 flex items-center justify-center border rounded-lg mb-4">
                    <img src="/tripala.jpg" alt="tripala">
                </div>
            </div>

            <div class="md:col-span-7">
                <h2 class="text-xl font-bold underline mb-4 text-gray-900">สรุปการตรวจสอบย้อนกลับ</h2>

                <div v-if="product" class="space-y-2 text-base">
                    <div class="grid grid-cols-3">
                        <span class="font-bold">สินค้า :</span>
                        <span class="col-span-2 text-gray-600">{{ product.name }}</span>
                    </div>
                    <div class="grid grid-cols-3">
                        <span class="font-bold">จาก :</span>
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
                        <span class="font-bold">แหล่งที่มาของการแปรรูป :</span>
                        <span class="col-span-2 text-gray-600">{{ product.processingAddress }}</span>
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
});
</script>

<style></style>