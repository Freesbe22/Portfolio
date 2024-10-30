<script setup>
defineProps({ percentLevel: Number })
</script>

<template>
    <li class="h-8 mb-5 relative bg-slate-100 dark:bg-slate-600">
        <div class="h-full w-full shadow-none overflow-visible float-left">
            <span class="bg-red-500  h-full absolute top-0 bottom-0 left-0" :style="{ 'width': percentLevel + '%' }"></span>
        </div>
        <span class="bg-red-400  h-full absolute top-0 bottom-0 left-0 text-white px-4 py-1">
            <slot></slot>
        </span>
    </li>
</template>
