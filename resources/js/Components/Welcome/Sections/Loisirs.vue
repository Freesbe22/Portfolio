<script setup>

import LoisirBloc from '@/Components/Welcome/Sections/LoisirBloc.vue';


// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Navigation } from 'vue3-carousel'

const config = {
    wrapAround: true,
    transition: 300,
    autoplay: 5000,
    pauseAutoplayOnHover: true,
    breakpoints: {
        576: {
            itemsToShow: 1,
            snapAlign: 'center',
        },
        768: {
            itemsToShow: 2,
            snapAlign: 'start',
        },
        992: {
            itemsToShow: 3,
            snapAlign: 'start',
        },
        1400: {
            itemsToShow: 4,
            snapAlign: 'start',
        },
    },
}
</script>

<template>
    <section id="Loisirs" class="text-light container-fluid pt-4">
        <div class="row mx-5">
            <h1 class="text-light-emphasis mx-5 mt-5">Mes loisirs</h1>
        </div>
        <div class="row mx-5 p-3 mh-100">
            <Carousel v-bind="config">
                <Slide>
                    <LoisirBloc imgLink="../../../../../../resources/images/Loisirs/switchwire.webp"
                        imgAlt="Switchwire">
                        <template #Title>
                            Impression 3D
                        </template>
                        <template #Content>
                            D’une Ender 3 acheté en 2020 à une Voron Switchwire construite en 2024, mon imprimante a pu
                            créer de nombreux projets et outils/décorations aux seins de mes differents loisirs
                        </template>
                        <template #Quantite>
                            2600 Heures
                        </template>
                    </LoisirBloc>
                </Slide>
                <Slide>
                    <LoisirBloc imgLink="../../../../../../resources/images/Loisirs/homeserver.webp"
                        imgAlt="Mon Home Server">
                        <template #Title>
                            Home Server
                        </template>
                        <template #Content>
                            Un Home Server créer à partir d’un vieux PC, puis améliorer au fil du temps. Il est utilisé
                            pour différentes activités tel-que les jeux vidéo, le monitoring du réseau, ou bien pour
                            mettre en service des projets web ou applicatif
                        </template>
                        <template #Quantite>
                            1000 Heures
                        </template>
                    </LoisirBloc>
                </Slide>
                <Slide>
                    <LoisirBloc imgLink="../../../../../../resources/images/Loisirs/moto.jpg" imgAlt="Ma moto">
                        <template #Title>
                            Moto
                        </template>
                        <template #Content>
                            Depuis tout petit la moto me fascine, des courses de moto cross au championnat mondiaux, ou
                            encore le motoGP. C’est en 2022 que j’ai décidé de passer le permis et d’acheter une Suzuki
                            Bandit de 1995
                        </template>
                        <template #Quantite>
                            5800 km
                        </template>
                    </LoisirBloc>
                </Slide>
                <Slide>
                    <LoisirBloc imgLink="../../../../../../resources/images/Loisirs/airsoft.jpg" imgAlt="Mon loadout">
                        <template #Title>
                            Airsoft
                        </template>
                        <template #Content>
                            Depuis quelques années je pratique l'airsoft en association. J'ai pu y faire mes debuts et évoluer 
                            jusqu'à mon equipement actuel. Et tout cela en aidant les autres pratiquant de l'association, que ce 
                            soit pour leurs materiels ou bien sur la façon de tirer parti au mieux de leurs equipement actuel.
                        </template>
                        <template #Quantite>
                            5800 km
                        </template>
                    </LoisirBloc>
                </Slide>

                <template #addons>
                    <Navigation />
                </template>
            </Carousel>
        </div>
    </section>
</template>
