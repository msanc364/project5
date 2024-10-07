<script setup>
import { faker } from '@faker-js/faker'








const dish = faker.food.dish()
const description = faker.food.description()
const ethnicCategory = faker.food.ethnicCategory()

</script>

<template>

    <!-- {{ fullname }} <br /> -->
      

      
      <div class="border border-gray-400 rounded-lg shadow bg-gray-200 h-full">
        <img :src="faker.image.urlLoremFlickr({width: 640, height: 480, category:'food'})" class="rounded-t-xl"/>
        <div class="p-4">
            <p class="mb-2 text-2xl font-bold">{{ dish }}</p>
            <p class="mb-3 font-normal text-gray-700">{{ ethnicCategory }}</p>
            <p class="mb-3 font-normal text-gray-700">{{ description }}</p>
        </div>
      </div>
    

</template>