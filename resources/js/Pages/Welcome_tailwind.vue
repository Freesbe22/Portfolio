<script setup>
import { Head, Link } from '@inertiajs/vue3';
import Navbar from '@/Components/Tailwind/Welcome/Navbar.vue';
import Home from '@/Components/Tailwind/Welcome/Sections/Home.vue';
import Activities from '@/Components/Tailwind/Welcome/Sections/Activities.vue';
import Competences from '@/Components/Tailwind/Welcome/Sections/Competences.vue';
import '../bootstrap';
import '../../css/app_tailwind.css';

defineProps({
    activities: Object,
});
</script >

<template>
    <Head title="MIDEY Baptiste" />

    <div
        class="relative min-h-screen bg-dots-darker bg-center bg-gray-100 dark:bg-dots-lighter dark:bg-gray-900 selection:bg-red-500 selection:text-white transition-[margin] duration-300">
        <!-- <div
            class="relative sm:flex sm:justify-center sm:items-center min-h-screen bg-dots-darker bg-center bg-gray-100 dark:bg-dots-lighter dark:bg-gray-900 selection:bg-red-500 selection:text-white transition-[margin] duration-300"> -->
        <Navbar />

        <Home />

        <div class="overflow-hidden relative block w-full">
            <section class="h-40 w-full flex items-center justify-center"
                style="background-size: auto auto;
background-color: rgba(250, 204, 21, 1);
background-image: repeating-linear-gradient(125deg, transparent, transparent 40px, rgba(0, 0, 0, 1) 40px, rgba(0, 0, 0, 1) 85px );">
                <h1 class="text-8xl text-black uppercase font-extrabold font-sans bg-yellow-400 py-1 px-2">
                    Site en
                    construction
                </h1>
            </section>
            <Competences />
        </div>
    </div>
</template>

<style>
.bg-dots-darker {
    background-image: url("data:image/svg+xml,%3Csvg width='30' height='30' viewBox='0 0 30 30' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1.22676 0C1.91374 0 2.45351 0.539773 2.45351 1.22676C2.45351 1.91374 1.91374 2.45351 1.22676 2.45351C0.539773 2.45351 0 1.91374 0 1.22676C0 0.539773 0.539773 0 1.22676 0Z' fill='rgba(0,0,0,0.2)'/%3E%3C/svg%3E");
}

@media (prefers-color-scheme: dark) {
    .dark\:bg-dots-lighter {
        background-image: url("data:image/svg+xml,%3Csvg width='30' height='30' viewBox='0 0 30 30' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1.22676 0C1.91374 0 2.45351 0.539773 2.45351 1.22676C2.45351 1.91374 1.91374 2.45351 1.22676 2.45351C0.539773 2.45351 0 1.91374 0 1.22676C0 0.539773 0.539773 0 1.22676 0Z' fill='rgba(255,255,255,0.07)'/%3E%3C/svg%3E");
    }
}
</style>
