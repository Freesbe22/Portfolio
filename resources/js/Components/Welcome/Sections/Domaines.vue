<script setup>
</script>

<template>
    <div class="container-fluid h-75 position-relative">
        <div class="row position-absolute start-50 top-0 translate-middle-x">
            <h1 class="fs-1 text-light fw-semibold">MIDEY Baptiste</h1>
        </div>
        <div class="row h-100">
            <div id="Dev" class="col-12 col-lg-6 text-light">
                <div class="row align-items-center h-100 text-center">
                    <div class="col">
                        <h1 class="fs-3 text-uppercase fw-semibold">
                            Développeur informatique
                        </h1>
                        <h1 class="fs-5 text-uppercase fw-semibold">
                            .NET (C#, Blazor, ...)
                        </h1>

                    </div>
                </div>
            </div>
            <div id="Infra" class="col-12 col-lg-6 text-light">
                <div class="row align-items-center h-100 text-center">
                    <div class="col">
                        <h1 class="fs-3 text-uppercase fw-semibold">
                            Adminstrateur Système
                        </h1>
                        <h2 class="fs-5 text-uppercase fw-semibold">
                            Gestion, maintenance, sécurisation d'une infrastructure informatique
                        </h2>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
#Dev {
    background: no-repeat;
    background-image: url('../../../../images/Dev.svg');
    background-size: cover;
}

#Infra {
    background: no-repeat;
    background-image: url('../../../../images/Infra.svg');
    background-size: cover;
}
</style>
