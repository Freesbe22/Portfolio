<script setup>

import ParcourBloc from '@/Components/Welcome/Sections/ParcourBloc.vue';
</script>

<template>
   <section id="Parcours" class="text-light container-fluid">
      <div class="row mx-5">
         <h1 class="text-light-emphasis mx-5 mt-5">Mon Parcours</h1>
      </div>
      <div class="row mx-5 pb-2">
         <div class="col-md-3 d-none d-md-block">

         </div>
         <div class="col-12 col-md-9">
            <ul class="timeline-list">
               <ParcourBloc>
                  <template #Title>
                     Brevet fédéral
                  </template>
                  <template #Content>
                     Equivalent : BTS Système Informatique aux Organisations
                  </template>
                  <template #Date>
                     (2018-2020)
                  </template>
               </ParcourBloc>
               <ParcourBloc>
                  <template #Title>
                     Stage et CDD
                  </template>
                  <template #Content>
                     Développeur applicatif chez Avea Concept
                  </template>
                  <template #Date>
                     (2019-2020)
                  </template>
               </ParcourBloc>
               <ParcourBloc>
                  <template #Title>
                     Licence Administrateur de Sytème d’Information
                  </template>
                  <template #Date>
                     (2020-2022)
                  </template>
               </ParcourBloc>
               <ParcourBloc>
                  <template #Title>
                     Alternance
                  </template>
                  <template #Content>
                     Développeur .NET chez DLM Soft
                  </template>
                  <template #Date>
                     (2020-2022)
                  </template>
               </ParcourBloc>
               <ParcourBloc>
                  <template #Title>
                     CDD puis CDI
                  </template>
                  <template #Content>
                     Développeur .NET chez DLM Soft
                  </template>
                  <template #Date>
                     (2022-2024)
                  </template>
               </ParcourBloc>
            </ul>
         </div>
      </div>
   </section>
</template>

<style>
ul.timeline-list {
    position: relative;
    margin: 0;
    padding: 0
}

ul.timeline-list:before {
    position: absolute;
    content: "";
    width: 2px;
    height: 100%;
    background-color: #ffffff;
    left: 50%;
    top: 0;
    -webkit-transform: translateX(-50%);
    transform: translateX(-50%);
}

ul.timeline-list li {
    position: relative;
    clear: both;
    display: table;
    width: 100%;
}

ul.timeline-list li .timeline_content {
    width: 45%;
    padding: 30px;
    float: right;
    text-align: left;
}

ul.timeline-list li:nth-child(2n) .timeline_content {
    float: left;
    text-align: left;
}

ul.timeline-list li:before {
    position: absolute;
    content: "";
    width: 25px;
    height: 25px;
    background-color: #ff3636;
    left: 50%;
    top: 50%;
    -webkit-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
    border-radius: 50%;
}
</style>
