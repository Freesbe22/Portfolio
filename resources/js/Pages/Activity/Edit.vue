<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import { useForm } from '@inertiajs/vue3'

const props = defineProps({ activity: Object })

var form = useForm({
    name: props.activity?.name,
    quantity: props.activity?.quantity,
    complement: props.activity?.complement,
})

const submit = () => {
    if(props.activity){
        form.post(route('activity.store'))
    }
    else{
        form.put(route('activity.update'))
    }
};
</script>

<template>
    <AppLayout title="Create activity">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 dark:text-gray-200 leading-tight">
                Create activity
            </h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="overflow-hidden shadow-xl">

                    <form @submit.prevent="submit" class="basis-3/4 flex flex-row">
                        <input type="text" v-model="form.name" class="">
                        <input v-model="form.quantity"
                            class="h-10 w-32 mx-4 outline-none focus:outline-none text-center w-full bg-gray-300 font-semibold text-md hover:text-black focus:text-black  md:text-basecursor-default flex items-center text-gray-700  outline-none"
                            type="number" />
                        <textarea type="text" v-model="form.name" class=""/>
                        <button type="submit" class="">
                            Ajouter
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </AppLayout>
</template>
