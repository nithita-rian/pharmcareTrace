<!-- index.vue -->
<template>
    <div class="space-y-8">
        <TraceInformation :product="trace" />
        <ProductInformation :product="product" />
        <Map />
    </div>
</template>
<script setup>
// Mock Data based on the image
const trace = reactive({
    name: 'น้ำตรีผลา สูตร LOWSUGAR',
    productCode: '44-2-01055-2-0001',
    produced: 'บริษัท ภูเชียงกา เฮิร์มแลนด์ จำกัด',
    distributor: 'โรงงานฟาร์มแคร์ ฟาร์มาซูติคอล คณะเภสัชศาสตร์ มหาวิทยาลัยมหาสารคาม',
    packageId: '16011557416009',
    transportId: '16660115576873730',
    produceDate: '2025-12-07',
    packDate: '2025-12-08',
    shipDate: '2025-12-09',
    transportType: 'Truck',
    containerNo: '123456789',
    trackingNo: 'UFQHFY'
});

const product = reactive({
    name: 'น้ำตรีผลา สูตร LOWSUGAR',
    productCode: '44-2-01055-2-0001',
    ingredients: 'ผลสมอไทย (Terminalia chebula), ผลสมอพิเภก (Terminalia bellerica), ผลมะขามป้อม (Phyllatus emblica)',
    size:'280',
    unit:'มิลลิลิตร',
    properties:'น้ำตรีผลาถูกพัฒนามาจากยาตรีผลา ให้เป็นเครื่องดื่มที่สามารถดื่มได้ทั่วไป ทุกเพศ ทุกวัย เป็นเครื่องดื่มที่อุดมไปด้วยสารฟีนอลิก ซึ่งมีฤทธิ์ต้านอนุมูลอิสระ ช่วยบำรุงร่างกาย',
});
</script>

<style></style>