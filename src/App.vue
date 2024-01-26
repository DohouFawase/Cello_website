<script setup>
import Nav from './components/Nav.vue'
import { gsap } from "gsap";
import { createRouter } from 'vue-router'
import { Flip } from "gsap/Flip";
import { TextPlugin } from "gsap/TextPlugin";
import { ref,computed, onMounted,onUnmounted } from 'vue'


gsap.registerPlugin(Flip,TextPlugin);


const targetDate = ref('2024-03-31T23:59:59')
const now = ref(Date.now());
const intervalId = ref(null);
const remainingTime = computed(() => {
  const target = new Date(targetDate.value);
  const difference = target.getTime() - now.value;
  return difference > 0 ? difference / 1000 : 0;
});


const days = computed(() => Math.floor(remainingTime.value / 86400));
const hours = computed(() => Math.floor((remainingTime.value % 86400) / 3600));
const minutes = computed(() => Math.floor((remainingTime.value % 3600) / 60));
const seconds = computed(() => Math.floor(remainingTime.value % 60));

onMounted(() => {
  intervalId.value = setInterval(() => {
    now.value = Date.now();
  }, 1000);
});

onMounted(() => {
  intervalId.value = setInterval(() => {
    now.value = Date.now();
  }, 1000);
});

// Cleanup on unmount
onUnmounted(() => {
  clearInterval(intervalId.value);
});


const name = ref('');
const email = ref('');
const phone = ref('');
const date = ref('');
const time = ref('');
const message = ref('');

const onSubmit = () => {
  // Envoyez les données du formulaire au serveur
};
</script>

<template>
  <Nav  />
  <div class="py-12 px-12 text-white">
        <div class=" relative">
           
            <div class="text-center">
               <h1 class="font-black text-9xl">COMMING</h1>
               <h1 class="font-black text-9xl" >SOON</h1>
                <p class="text-4xl font-semibold py-5">FESTIVAL DU CHRIST</p>
            </div>
           
            
            <div class="timer pt-8 ">
                <div class="time flex space-x-8 rtl:space-x-revers items-center">
                    <div class="days text-center p-4">
                        <p class="text-2xl font-semibold">{{ days }}</p>
                        <p>Jours</p>
                    </div>

                    <div class="hours text-center p-4">
                        <p class="text-2xl font-semibold">{{ hours }}</p>
                        <p>Heurs</p>

                    </div>

                    <div class="minutes text-center p-4">
                        <p class="text-2xl font-semibold">{{ minutes }}</p>
                        <p>Minutes</p>

                    </div>

                    <div class="second text-center p-4">
                        <p class="text-2xl font-semibold">{{ seconds }}</p>
                        <p>Secondes</p>
                    </div>
                </div>
            </div>
        </div>

    <div class="about pt-12">
      <div class="container mx-auto flex flex-col md:flex-row ">
        <div class="">
            <h1 class="  text-blue-500 min-w-80 mb-6 text-5xl font-bold uppercase">Qui sommes Nous</h1>
            <p class="min-w-80 mb-6 w w-2/3 ">L'agence Cello est spécialisée dans la création d'événements. Nous nous engageons à créer des expériences uniques et inoubliables pour nos clients.

            Nous croyons que les événements sont l'occasion de créer des liens, de partager des émotions et de vivre des moments forts. C'est pourquoi nous nous attachons à concevoir des événements qui soient à la fois originaux et engageants.

        Notre équipe est composée de professionnels expérimentés et passionnés. Nous sommes à votre écoute pour comprendre vos besoins et vos objectifs. Nous vous accompagnerons tout au long du processus de création de votre événement, de la conception à la réalisation.
            </p>
            

            <a href="" class="bg-blue-500 p-3 rounded hover:bg-blue-800 shadow ">Explorez Nous</a>
        </div>

        <div class="">
            <img src="/imgs/5.jpg" alt="" class=" ">
        </div>
      </div>
    </div>


    <div class="event py-12">
      <div class="">
        <div class="">
            <div class="w-20" >
            <img src="/imgs/logo.jpg" alt="" class="w-full">
            </div>
            <p>Vous présente</p>
            <p class="ill pt-4"> ILLUMINIA 2K24</p>
        </div>
        <div class="container mx-auto pt-12">
  <div class="flex flex-wrap justify-content-center md:flex-row md:justify-content-between">
    <div class="w-full md:w-1/4 mt-4">
      <img src="/imgs/1.jpg" alt="" class="w-full h-full">
      <div class="text-center text-gray-500">
        <h6 class="mb-2">FESTIVAL DU CHRIST</h6>
        <p class="mb-1">31 MARS AU 1 AVRIL(PÂQUES)</p>
      </div>
    </div>
   
    <div class="w-full md:w-1/4 mt-4">
      <img src="/imgs/4.jpg" alt="" class="w-full h-full">
      <div class="text-center text-gray-500">
        <h6 class="mb-2">MOUSSE THE MOOD </h6>
        <p class="mb-1">Description de la carte 3</p>
      </div>
    </div>
    <div class="w-full md:w-1/4 mt-4">
      <img src="/imgs/3.jpg" alt="" class="w-full h-full">
      <div class="text-center text-gray-500">
        <h6 class="mb-2">MMATURE VIBES</h6>
        <p class="mb-1">Description de la carte 4</p>
      </div>
    </div>

    <div class="w-full md:w-1/4 mt-4">
      <img src="/imgs/2.jpg" alt="" class="w-full h-full">
      <div class="text-center text-gray-500">
        <h6 class="mb-2">100 MOOD IMPREVUE AFTER PARTY</h6>
        <p class="mb-1">TOUS LES JOURS EN DECEMBRE</p>
      </div>
    </div>
  </div>
</div>

      </div>
    </div>

    

    <div class="event py-12">
      <div class="">
        <div class="">
           
            <p class=""> Contactez Nous</p>
        </div>
          <div class=""></div>
      </div>
    </div>


    </div>


</template>


