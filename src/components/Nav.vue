<script setup>
import { createRouter } from 'vue-router'
</script>

<template>
  <div class="bg-black text-white px-12  ">
    <div class="flex p-4 items-center justify-between"  >
        <div >
            <img src="/imgs/logo.jpg" alt="" class="w-20">
        </div>
        <div>
            <ul class="flex space-x-8 rtl:space-x-revers">
                <li><a href="">Home</a></li>
                <li><a href="">A propos</a></li>
                <li><a href="">Contact </a></li>
                <li><a href="">Comming Soon</a></li>
            </ul>
        </div>
        <div>
            <a class="py-2.5 px-5 me-2 mb-2 text-sm font-medium text-gray-900 focus:outline-none bg-white rounded-full border border-gray-200 hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:ring-4 focus:ring-gray-200 dark:focus:ring-gray-700 dark:bg-gray-800 dark:text-gray-400 dark:border-gray-600 dark:hover:text-white dark:hover:bg-gray-700">
                Réservation
            </a>
        </div>
    </div>
  </div>
</template>