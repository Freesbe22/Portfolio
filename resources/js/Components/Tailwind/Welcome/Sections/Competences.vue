<script setup>
import CompetenceProgress from '@/Components/Tailwind/Welcome/Sections/Competences/CompetenceProgress.vue'
</script>

<template>
    <div id="competences"
        class="py-24 bg-white dark:bg-slate-800 text-base pt-12 text-gray-400 dark:text-zinc-300 block pb-28">
        <div class="container mx-auto table">
            <div class="mb-16 block">
                <h2 class="text-6xl font-semibold text-center uppercase text-black dark:text-white">
                    Mes compétences
                </h2>
                <h3 class="text-4xl text-center">
                    Des compétences à votre service
                </h3>
            </div>
            <div class="flex mx-auto w-full flex-row flex-wrap">
                <div class="w-full sm:w-1/2 px-4">
                    <h4 class="my-2 text-2xl font-medium">Compétences en développement</h4>
                    <ul class="mt-4">
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
                            <abbr title="Interface graphique qui est incluse dans le framework .NET">Windows Forms</abbr>
                        </CompetenceProgress>
                        <CompetenceProgress :percentLevel="35">
                            <abbr title="Langage de programmation de haut niveau orienté objet">Java</abbr>
                        </CompetenceProgress>
                    </ul>
                </div>
                <div class="w-full sm:w-1/2 px-4">
                    <h4 class="my-2 text-2xl font-medium">Compétences en administrateur système </h4>
                    <ul class="mt-4">
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
                <div class="w-full px-4">
                    <h4 class="my-2 text-2xl font-medium">Domaines de compétences</h4>
                    <ul class="pt-3 flex flex-row flex-wrap">
                        <li class="relative pl-7">
                            <font-awesome-icon :icon="['fas', 'check-circle']" class="top-0 left-2 absolute text-red-400" />
                            <h5 class="font-bold text-sm">Applications spécifiques et Interface d'administration</h5>
                            <em>PHP - MySQL - AJAX / ASP.NET - C# - SQL</em>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>
