<!-- index.vue -->
<template>
    <div class="space-y-8 md:mx-10">
        <TraceInformation :product="trace" :images="images" />
        <!-- <ProductInformation :product="product" /> -->
        <div class="mb-6">
            <nav class="flex -mb-px space-x-4" aria-label="Tabs">

                <button @click="activeTab = 1" :class="getTabClass(1)">
                    <span class="flex items-center justify-center gap-2">
                        <Icon name="mdi:information-outline" class="h-5 w-5" />
                        ข้อมูลผลิตภัณฑ์
                    </span>
                </button>

                <button @click="activeTab = 2" :class="getTabClass(2)">
                    <span class="flex items-center justify-center gap-2">
                        <Icon name="mdi:file-table-outline" class="h-5 w-5" />
                        ใบรับรอง
                    </span>
                </button>

                <button @click="activeTab = 3" :class="getTabClass(3)">
                    <span class="flex items-center justify-center gap-2">
                        อื่นๆ
                    </span>
                </button>

            </nav>
        </div>

        <div class="rounded-lg min-h-75">

            <div v-if="activeTab === 1">
                <ProductInformation :product="product" />
            </div>

            <div v-if="activeTab === 2">
                <CertificateInformation :images="Certs" />
            </div>

            <div v-if="activeTab === 3">
                <OtherInformation :images="others"/>
            </div>

        </div>
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
    exp: '19/05/2026',
    lotNumber: 'FP28325017',
    barcode: '8858994701425',
    ingredients: 'ผลสมอไทย (Terminalia chebula), ผลสมอพิเภก (Terminalia bellerica), ผลมะขามป้อม (Phyllatus emblica)',
    size: '280',
    unit: 'มิลลิลิตร',
    properties: 'น้ำตรีผลาถูกพัฒนามาจากยาตรีผลา ให้เป็นเครื่องดื่มที่สามารถดื่มได้ทั่วไป ทุกเพศ ทุกวัย เป็นเครื่องดื่มที่อุดมไปด้วยสารฟีนอลิก ซึ่งมีฤทธิ์ต้านอนุมูลอิสระ ช่วยบำรุงร่างกาย',
});

const images = [
    "/img/tripala.jpg",
    "/img/tripala2.jpg",
    "/img/tripala3.jpg",
    "/img/tripala4.jpg",
    "/img/tripala5.jpg"
];

const activeTab = ref(1);
// ฟังก์ชันสำหรับเลือก Class ของปุ่ม Tab (เพื่อให้โค้ดใน Template สะอาด)
const getTabClass = (tabIndex) => {
    const baseClass = "flex py-2 px-2 md:p-4 text-center border-b-2 font-medium text-sm md:text-base cursor-pointer transition-colors duration-300 focus:outline-none";
    const activeClass = "border-green-600 text-green-700 bg-green-50";
    const inactiveClass = "border-transparent text-gray-500 hover:text-gray-700 hover:border-gray-300";

    return activeTab.value === tabIndex
        ? `${baseClass} ${activeClass}`
        : `${baseClass} ${inactiveClass}`;
};

const Certs = [
    "/img/Cert (1).jpg",
    "/img/Cert (2).jpg",
    "/img/Cert (3).jpg",
    "/img/Cert (4).jpg",
    "/img/Cert (5).jpg"
];

const others = [
    "/img/other (1).jpg",
    "/img/other (2).jpg",
];
</script>

<style></style>