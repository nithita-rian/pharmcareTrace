<template>
    <div>
        <TraceInformation :product="product"/>
    </div>
</template>
<script setup>
// Mock Data based on the image
const product = reactive({
    name: 'น้ำตรีผลา สูตร LOWSUGAR',
    productCode: '44-2-01055-2-0001',
    produced: 'โรงงานฟาร์มแคร์ ฟาร์มาซูติคอล คณะเภสัชศาสตร์ มหาวิทยาลัยมหาสารคาม',
    processingAddress: 'โรงงานฟาร์มแคร์ ฟาร์มาซูติคอล คณะเภสัชศาสตร์ มหาวิทยาลัยมหาสารคาม',
    packageId: '16011557416009',
    transportId: '16660115576873730',
    produceDate: '2025-12-07',
    packDate: '2025-12-08',
    shipDate: '2025-12-09',
    transportType: 'Truck',
    containerNo: '123456789',
    trackingNo: 'UFQHFY'
});
</script>

<style></style>