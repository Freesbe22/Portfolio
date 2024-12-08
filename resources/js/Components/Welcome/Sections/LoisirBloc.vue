<script setup>
defineProps({ imgLink: String   , imgAlt: String })
function getImageUrl(name) {
    return new URL(`${name}`, import.meta.url).href
}
</script>

<template>
    <div class="col-11">
        <div class="card text-light card-has-bg click-col"
            :style="{ 'background-image': 'url(' +getImageUrl(imgLink)+')'}">
            <img class="card-img d-none" :src="imgLink"
                :alt="imgAlt">
            <div class="card-img-overlay d-flex flex-column">
                <div class="card-body">
                    <h4 class="card-title mt-0 ">
                        <slot name="Title"></slot>
                    </h4>
                    <small><i class="far fa-clock"></i> 600 H</small>
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
