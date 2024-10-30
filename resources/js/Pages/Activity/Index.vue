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
    <AppLayout title="Activities">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 dark:text-gray-200 leading-tight">
                Activities
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="overflow-hidden shadow-xl">
                    <div class="fixed right-4 bottom-4">
                        <a type="button"
                            class="h-12 w-12 inline-flex text-center items-center justify-center px-4 py-2 bg-green-600 border border-transparent rounded-full font-bold text-4xl text-white uppercase tracking-widest hover:bg-green-500 active:bg-green-700 focus:outline-none focus:ring-2 focus:ring-green-500 focus:ring-offset-2 dark:focus:ring-offset-gray-800 transition ease-in-out duration-150"
                                :href="route('activity.create')">
                            +
                        </a>
                    </div>

                    <ul class="gap-y-2 grid">
                        <li v-for="activity in activities"
                            class="odd:bg-sky-950 even:bg-indigo-950  sm:rounded-lg p-2 flex flex-row">
                            <ActivityListItem :activity="activity"></ActivityListItem>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </AppLayout>
</template>
