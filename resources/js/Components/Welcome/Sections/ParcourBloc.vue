<script setup>
</script>

<template>
    <li>
        <div class="timeline_content">
            <h3 class="text-light-emphasis">
                <slot name="Title"></slot>
            </h3>
            <a v-if="this.$slots['Content']">
                <slot name="Content"></slot>
            </a>
            <br v-if="this.$slots['Content']" />
            <a>
                <slot name="Date"></slot>
            </a>
        </div>
    </li>
</template>
