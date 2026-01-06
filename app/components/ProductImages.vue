<template>
    <div>
        <!-- <div class="md:col-span-5 flex flex-col items-center justify-center">
            <div class="w-full p-2 bg-gray-50 flex items-center justify-center border rounded-lg mb-4">
                <img src="~/assets/img/tripala.jpg" alt="tripala">
            </div>
        </div> -->


        <div class="grid gap-4" v-if="images.length > 0">
            <div>
                <img class="h-auto max-h-full max-w-full rounded-lg w-full object-contain aspect-4/3 transition-all duration-300"
                    :src="activeImage" alt="Selected product image">
            </div>

            <div class="grid grid-cols-5 gap-4">
                <div v-for="(img, index) in images" :key="index" @click="activeImage = img" class="cursor-pointer">
                    <img class="h-full md:h-24 w-40 rounded-lg hover:opacity-75 transition-opacity"
                        :class="{ 'ring-2 ring-[#468775] ring-offset-2': activeImage === img }" :src="img"
                        alt="Thumbnail">
                </div>
            </div>
        </div>
        <div v-else class="text-center my-20">
            <p>No images available.</p>

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

// const activeImage = ref(props.images?.[0]) || null;

const activeImage = ref(null);

// เมื่อข้อมูลมาถึง หรือมีการเปลี่ยนแปลง ให้ set รูปแรกเป็น active ทันที
watch(() => props.images, (newImages) => {
    if (newImages && newImages.length > 0) {
        activeImage.value = newImages[0];
    }
}, { immediate: true });

</script>

<style></style>