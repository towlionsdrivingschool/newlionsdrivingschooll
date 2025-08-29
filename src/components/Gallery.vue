<template>
    <div class="p-6 container">
        <h2 class="text-lg text-primary text-center mb-8 tracking-wider">
            Gallery
        </h2>

        <!-- Image Grid -->
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-4">
            <img v-for="(img, index) in images" :key="index" :src="img" alt="Gallery"
                class="rounded-sm shadow-md hover:scale-105 transition cursor-pointer" @click="openLightbox(index)" />
        </div>

        <!-- FsLightbox -->
        <FsLightbox :toggler="lightboxToggler" :sources="images" :slide="currentSlide" />
    </div>
</template>

<script setup>
import { ref } from 'vue'
import FsLightbox from 'fslightbox-vue'

// ✅ Local images using Vite-compatible import
const images = [
    new URL('@/assets/images/img1.jpg', import.meta.url).href,
    new URL('@/assets/images/img2.jpg', import.meta.url).href,
    new URL('@/assets/images/img4.jpg', import.meta.url).href,
    new URL('@/assets/images/img8.jpg', import.meta.url).href,
    new URL('@/assets/images/img6.jpg', import.meta.url).href,
    new URL('@/assets/images/img11.jpg', import.meta.url).href,
    new URL('@/assets/images/img9.jpg', import.meta.url).href,
    new URL('@/assets/images/img10.jpg', import.meta.url).href,
    new URL('@/assets/images/img13.jpg', import.meta.url).href,
    new URL('@/assets/images/img14.jpg', import.meta.url).href,
    new URL('@/assets/images/img15.jpg', import.meta.url).href,
    new URL('@/assets/images/img12.jpg', import.meta.url).href,
    new URL('@/assets/images/img18.jpg', import.meta.url).href,
]

const lightboxToggler = ref(false)
const currentSlide = ref(1)

function openLightbox(index) {
    currentSlide.value = index + 1
    lightboxToggler.value = !lightboxToggler.value
}
</script>

<style scoped>
/* Optional: Add styles for smooth image hover */
img {
    width: 100%;
    height: auto;
}

img {
    transition: transform 0.3s ease;
}
</style>
