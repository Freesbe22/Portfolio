<script setup>
import { computed } from 'vue'
const props = defineProps({ imgLink: String, imgAlt: String })
// const imageUrl = computed(
//     //() => new URL(`@/assets/images/Loisirs/${props.imgLink}`, import.meta.url).href
//     () => new URL(`@/assets/images/Loisirs/airsoft.jpg`, import.meta.url).href
// );
const imageUrl = new URL(`../../../../images/Loisirs/${props.imgLink}`, import.meta.url).href
</script>

<template>
    <div class="col-11">
        <div class="card text-light card-has-bg click-col" :style="{ 'background-image': 'url(' + imageUrl + ')' }">
            <img class="card-img d-none" :src="imageUrl" :alt="imgAlt">
            <div class="card-img-overlay d-flex flex-column">
                <div class="card-body">
                    <h4 class="card-title mt-0 ">
                        <slot name="Title"></slot>
                    </h4>
                    <small><i class="far fa-clock"></i>
                        <slot name="Quantite"></slot>
                    </small>
                </div>
                <div class="card-footer">
                    <div class="media">

                        <slot name="Content"></slot>
                    </div>
                </div>
            </div>
        </div>
    </div>

</template>
