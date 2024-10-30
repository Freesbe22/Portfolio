<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import { useForm } from '@inertiajs/vue3'
import ActivityListItem from '@/Components/Dashboard/Activity/ActivityListItem.vue'

var form = useForm({
    addedQuantity: 1,
})

defineProps({ activities: Object })
</script>

<template>
        <div :id="activitees" class="">
        </div>
</template>
