<script setup>
import SlideOne from '@/Components/Tailwind/Welcome/Sections/Home/SlideOne.vue';
import SlideTwo from '@/Components/Tailwind/Welcome/Sections/Home/SlideTwo.vue';
import SlideThree from '@/Components/Tailwind/Welcome/Sections/Home/SlideThree.vue';

import { watchEffect } from 'vue'
import emblaCarouselVue from 'embla-carousel-vue';
import Autoplay from 'embla-carousel-autoplay';

const [emblaNode, emblaApi] = emblaCarouselVue({ loop: true }, [Autoplay()]);
watchEffect(() => {
    if (emblaApi.value) {
    }
});

function NextSlide() {
    if (emblaApi.value) {
        emblaApi.value.scrollNext();
    }
}
function PreviousSlide() {
    if (emblaApi.value) {
        emblaApi.value.scrollPrev();
    }
}
</script>

<template>
    <div :id="HomeSection" class=" relative embla w-full h-screen overflow-hidden" ref="emblaNode">
        <div class="h-full flex max-h-none relative w-full embla__container">
            <SlideOne />
            <SlideTwo />
            <!-- <SlideThree /> -->
        </div>
        <div class="embla__prev absolute inset-y-0 left-0 z-40 flex items-center">
            <button class="h-1/6 w-16 transition opacity-0 hover:opacity-50 bg-slate-500 text-slate-200 rounded-e-md" v-on:click="PreviousSlide()"
                type="button">
                <font-awesome-icon :icon="['fas', 'caret-left']" size="4x" />
            </button>
        </div>
        <div class="embla__next absolute inset-y-0 right-0 z-40 flex items-center">
            <button class="h-1/6 w-16 transition opacity-0 hover:opacity-80 bg-slate-500 text-slate-200 rounded-s-md" v-on:click="NextSlide()"
                type="button">
                <font-awesome-icon :icon="['fas', 'caret-right']" size="4x" />
            </button>
        </div>
    </div>
</template>

<style scoped src="../../../../../css/Tailwind/Welcome/Sections/Home.css"></style>
