<script setup>
import { Head, Link } from '@inertiajs/vue3';
import Developpeur from '@/Components/Welcome/Sections/Developpeur.vue';
import Reseaux from '@/Components/Welcome/Sections/Reseaux.vue';
import Apropos from '@/Components/Welcome/Sections/Apropos.vue';
import Parcours from '@/Components/Welcome/Sections/Parcours.vue';
import Technologies from '@/Components/Welcome/Sections/Technologies.vue';
import Loisirs from '@/Components/Welcome/Sections/Loisirs.vue';
import '../../css/app.scss';

defineProps({
    activities: Object,
});
</script>

<template>

    <Head title="MIDEY Baptiste" />

    <div class="vw-100 vh-100">
        <Developpeur />
        <Reseaux />
        <Apropos />
        <Parcours />
        <Technologies />
        <Loisirs />
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
