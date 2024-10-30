<script setup>
import CompetenceProgress from '@/Components/Welcome/Sections/Competences/CompetenceProgress.vue';
import CompetenceCard from '@/Components/Welcome/Sections/Competences/Competence.vue';
</script>

<template>
    <section id="competences" class="pb-5 text-light-emphasis">
        <div class="container">
            <div class="row my-5 page-heading">
                <h2 class="h2 fw-semibold text-center text-uppercase text-light">
                    Mes compétences
                </h2>
                <h3 class="mb-5 h3 text-center">
                    Des compétences à votre service
                </h3>
            </div>
            <div class="row">
                <div class="col-xs-12 col-sm-6">
                    <h4 class="my-2 fs-4 fw-medium">Compétences en développement</h4>
                    <ul class="mt-4 progress-holder px-0">
                        <CompetenceProgress :percentLevel="85">
                            <abbr title="(eXtensible) HyperText Markup Language\">(X)HTML</abbr> - <abbr
                                title="Cascading Style Sheets">CSS</abbr>
                        </CompetenceProgress>
                        <CompetenceProgress :percentLevel="75">
                            <abbr title="HyperText Preprocessor">PHP</abbr>
                        </CompetenceProgress>
                        <CompetenceProgress :percentLevel="70">
                            <abbr title="My Structured Query Language">MySQL</abbr> - <abbr
                                title="Structured Query Language">SQL</abbr>
                        </CompetenceProgress>
                        <CompetenceProgress :percentLevel="60">
                            <abbr title="Langage de développement web orienté client">JavaScript</abbr> - <abbr
                                title="Asynchronous JavaScript and XML">AJAX</abbr>
                        </CompetenceProgress>
                        <CompetenceProgress :percentLevel="80">
                            <abbr title="Active Server Pages">ASP</abbr>.NET - <abbr title="C Sharp">C#</abbr>
                        </CompetenceProgress>
                        <CompetenceProgress :percentLevel="70">
                            <abbr title="Interface graphique qui est incluse dans le framework .NET">Windows
                                Forms</abbr>
                        </CompetenceProgress>
                        <CompetenceProgress :percentLevel="35">
                            <abbr title="Langage de programmation de haut niveau orienté objet">Java</abbr>
                        </CompetenceProgress>
                    </ul>
                </div>
                <div class="col-xs-12 col-sm-6">
                    <h4 class="my-2 fs-4 fw-medium">Compétences en administrateur système </h4>
                    <ul class="mt-4 progress-holder px-0">
                        <CompetenceProgress :percentLevel="50">
                            <a>Active Directory</a>
                        </CompetenceProgress>
                        <CompetenceProgress :percentLevel="65">
                            <a>Microsoft Exchange</a>
                        </CompetenceProgress>
                        <CompetenceProgress :percentLevel="75">
                            <a>Watchguard</a>
                        </CompetenceProgress>
                        <CompetenceProgress :percentLevel="35">
                            <a>Serveur Mail</a>
                        </CompetenceProgress>
                        <CompetenceProgress :percentLevel="30">
                            <a>Veeam</a>
                        </CompetenceProgress>
                    </ul>
                </div>
                <div class="col-12">
                    <h4 class="my-2 fs-4 fw-medium">Domaines de compétences</h4>
                    <ul class="pt-3 ps-1 flex flex-row flex-wrap list-unstyled">
                        <CompetenceCard>
                            <template v-slot:title>Applications spécifiques et Interface d'administration</template>
                            <template v-slot:content>PHP - MySQL - AJAX / ASP.NET - C# - SQL</template>
                        </CompetenceCard>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>

<style>
.progress-holder{
    margin: 14px 0 0 -2px;
    list-style: none;
}
.progress-holder li {
    height: 30px;
    margin: 0 0 20px;
    position: relative;
    background: --bs-primary;
}
.progress-holder .progress-bar-outer {
    background: #e74c3c;
    top: 0;
    left: 0;
    bottom: 0;
    height: 30px;
    display: block;
    position: absolute;
}
.progress-holder .text,
#work-filter li a:hover {
    background: #f47a6d;
}

.progress-holder .text {
    top: 0px;
    left: 0;
    height: 30px;
    padding: 5px 15px;
    color: white;
    position: absolute;
    letter-spacing: 2px;
    text-transform: uppercase;
    font: 600 12px/18px "Poppins", "Helvetica Neue", Helvetica, Arial, sans-serif;
}
</style>
