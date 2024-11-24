<script setup>

import TechnologyBloc from '@/Components/Welcome/Sections/TechnologyBloc.vue';
</script>

<template>
    <section id="Technologies" class="text-light container-fluid pt-4">
        <div class="row mx-5">
            <h1 class="text-light-emphasis mx-5 mt-5">Les technologies utilisées</h1>
        </div>
        <div class="row mx-5 p-3 mh-100">
            <ul class="list-group">
                <TechnologyBloc>
                    <template #Image><img class="img-fluid" src="../../../../images/Technologies/csharp.jpg"
                            alt="Csharp logo">
                    </template>
                    <template #Title>
                        C# (Csharp)
                    </template>
                    <template #Content>
                        Brevet fédéral (2018 et 2020) - Alternance à DLM Soft (2021 et 2022) - DLM Soft (2022 à
                        2024)
                    </template>
                </TechnologyBloc>
                <TechnologyBloc>
                    <template #Image><img class="img-fluid" src="../../../../images/Technologies/postgresql.png"
                            alt="Csharp logo">
                    </template>
                    <template #Title>
                        PostgreSQL
                    </template>
                    <template #Content>
                        Licence Administrateur de Sytème d’Information (2021 à 2022) - DLM Soft (2022 à
                        2024)
                    </template>
                </TechnologyBloc>
                <TechnologyBloc>
                    <template #Image><img class="img-fluid" src="../../../../images/Technologies/oracle.png"
                            alt="Csharp logo">
                    </template>
                    <template #Title>
                        Oracle
                    </template>
                    <template #Content>
                        Brevet fédéral (2019 à 2020) - Licence Administrateur de Sytème d’Information (2020
                        à
                        2022)
                        - Alternance à DLM Soft (2020 à 2022) - DLM Soft (2022 à 2024)
                    </template>
                </TechnologyBloc>
                <TechnologyBloc>
                    <template #Image><img class="img-fluid" src="../../../../images/Technologies/vb6.jpg"
                            alt="Csharp logo">
                    </template>
                    <template #Title>
                        VB6 (Visual Basic 6)
                    </template>
                    <template #Content>
                        Alternance à DLM Soft (2020 à 2022) - DLM Soft (2022 à
                        2024)
                    </template>
                </TechnologyBloc>
                <TechnologyBloc>
                    <template #Image><img class="img-fluid" src="../../../../images/Technologies/blazor.png"
                            alt="Csharp logo">
                    </template>
                    <template #Title>
                        Blazor
                    </template>
                    <template #Content>
                        Alternance à DLM Soft (2021 à 2022) - DLM Soft (2022 à 2024)
                    </template>
                </TechnologyBloc>
                <TechnologyBloc>
                    <template #Image><img class="img-fluid" src="../../../../images/Technologies/laravel.png"
                            alt="Csharp logo">
                    </template>
                    <template #Title>
                        Laravel
                    </template>
                    <template #Content>
                        Brevet fédéral (2018 à 2020) - Licence Administrateur de Sytème d’Information (2020
                        à
                        2022) - Ce site web (2024)
                    </template>
                </TechnologyBloc>
            </ul>
        </div>
    </section>
</template>
