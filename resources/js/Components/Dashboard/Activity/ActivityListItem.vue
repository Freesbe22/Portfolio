<script setup>
import { useForm, Link } from '@inertiajs/vue3'

var form = useForm({
    addedQuantity: 1,
})

defineProps({ activity: Object })
</script>

<template>
    <div class="basis-2/3 flex flex-col">
        <h1 class="text-xl font-bold text-gray-800 dark:text-gray-200">
            {{ activity.name }} : {{ activity.quantity }}
        </h1>
        <div class="text-gray-500">
            {{ activity.complement }}
        </div>
    </div>
    <div class="basis-1/3 flex flex-row items-center">
        <form @submit.prevent="form.post(route('activity.quickAdd', activity))" class="basis-3/4 flex flex-row">
            <input v-model="form.addedQuantity" class="h-10 w-32 mx-4 outline-none focus:outline-none text-center w-full bg-gray-300 font-semibold text-md hover:text-black focus:text-black  md:text-basecursor-default flex items-center text-gray-700  outline-none" type="number" />
            <button type="submit"
                class="bg-green-600 border border-transparent rounded-md w-12 font-bold text-4xl text-center content-center text-white uppercase tracking-widest hover:bg-green-500 active:bg-green-700 focus:outline-none focus:ring-2 focus:ring-green-500 focus:ring-offset-2 dark:focus:ring-offset-gray-800 transition ease-in-out duration-150">
                +
            </button>
        </form>
        <div class="basis-1/4 text-center">
            <Link :href="route('activity.edit',activity)" class=" font-bold text-4xl text-white">></Link>
        </div>
    </div>
</template>
