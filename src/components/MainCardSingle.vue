<script setup>
import { faker } from '@faker-js/faker'

const firstname = faker.person.firstName()

const lastname = faker.person.lastName()
const fullname = faker.person.fullName({firstName: firstname, lastName:lastname})
const job_title = faker.person.jobTitle()
const bio = faker.lorem.lines(2)
const username = faker.internet.userName({ firstName: firstname, lastName: lastname }).toLowerCase()
const dish = faker.food.dish()
const description = faker.food.description()
const ingredient = faker.food.ingredient()

</script>

<template>

    <!-- {{ fullname }} <br /> -->
      <RouterLink :to="{name: 'CardDetails', params: {id: username}}">

      
      <div class="border border-gray-400 rounded-lg shadow bg-gray-200 h-full">
        <img :src="faker.image.urlLoremFlickr({width: 640, height: 480, category:'food'})" class="rounded-t-xl"/>
        <div class="p-4">
            <p class="mb-2 text-2xl font-bold">{{ dish }}</p>
            <p class="mb-3 font-normal text-gray-700">{{ ingredient }}</p>
            <p class="mb-3 font-normal text-gray-700">{{ description }}</p>
        </div>
      </div>
    </RouterLink>

</template>