<script setup lang="ts">
import { differenceInDays, differenceInHours, differenceInMinutes, differenceInSeconds } from 'date-fns'

const targetDate = new Date(2025, 7, 4, 8, 0, 0) // August 4, 2025 8:00 AM

const days = ref(0)
const hours = ref(0)
const minutes = ref(0)
const seconds = ref(0)

const updateCountdown = () => {
  const now = new Date()
  days.value = differenceInDays(targetDate, now)
  hours.value = differenceInHours(targetDate, now) % 24
  minutes.value = differenceInMinutes(targetDate, now) % 60
  seconds.value = differenceInSeconds(targetDate, now) % 60
}

onMounted(() => {
  updateCountdown()
  const timer = setInterval(updateCountdown, 1000)
  onUnmounted(() => clearInterval(timer))
})
</script>

<template>
  <div class="grid lg:grid-cols-2 gap-12 items-center max-w-6xl mx-auto px-6 py-12">
    <!-- Workshop Info -->
    <div class="space-y-6">
      <div class="space-y-4">
        <span class="inline-block px-4 py-2 bg-orange-100 text-orange-600 rounded-full text-sm font-bold">
          4-6 August 2025
        </span>
        <h1 class="text-4xl md:text-5xl font-bold bg-gradient-to-r from-orange-600 to-sky-600 bg-clip-text text-transparent">
          Youth Against Drugs Annual Workshop
        </h1>
        <div class="flex items-center text-lg text-gray-600">
          <UIcon name="i-heroicons-map-pin" class="w-5 h-5 mr-2 text-sky-500" />
          <span class="font-medium text-sky-600">Masvingo, Zimbabwe</span>
        </div>
      </div>

      <p class="text-lg text-gray-700 leading-relaxed">
        Our team from southern Zimbabwe will host our much-anticipated annual workshop. 
        Prepare for an inspiring experience with leading experts and youth advocates.
      </p>

      <!-- Countdown -->
      <div class="space-y-3">
        <h3 class="text-sm font-semibold text-gray-500 uppercase tracking-wider">Countdown to Workshop</h3>
        <div class="grid grid-cols-4 gap-3">
          <div v-for="(value, unit) in { days, hours, minutes, seconds }" :key="unit" 
               class="bg-white p-4 rounded-xl shadow-sm border border-gray-100 text-center">
            <div class="text-3xl font-bold text-orange-600">{{ value }}</div>
            <div class="text-xs font-medium text-gray-500 uppercase mt-1 tracking-wider">{{ unit }}</div>
          </div>
        </div>
      </div>

      <UButton size="xl" class="mt-6" color="warning" variant="solid">
        <span class="font-bold">Book Your Seat Now</span>
        <UIcon name="i-heroicons-arrow-right" class="ml-2 w-5 h-5" />
      </UButton>
    </div>

    <!-- Speaker Section -->
    <div class="relative">
      <div class="relative z-10">
        <NuxtImg src="/img/linkedIn.jpg" 
                 class="rounded-2xl shadow-xl w-full h-auto aspect-square object-cover border-4 border-white" />
      </div>
      
      <!-- Speaker Info Card -->
      <div class="absolute -bottom-8 right-0 z-20 w-4/5 bg-white p-6 rounded-xl shadow-lg border border-gray-100">
        <div class="space-y-2">
          <h3 class="text-2xl font-bold text-gray-900">Eshanit Orongam</h3>
          <p class="text-gray-600">Pharmacology and Toxicants Inc President</p>
          <span class="inline-block px-3 py-1 bg-orange-100 text-orange-600 rounded-full text-sm font-bold">
            Guest Speaker
          </span>
        </div>
      </div>

      <!-- Polka Dots Background -->
      <div class="absolute -top-8 -left-8 -z-10 w-64 h-64 opacity-20">
        <div class="grid grid-cols-4 gap-1">
          <template v-for="row in 4" :key="row">
            <div v-for="col in 4" :key="col" class="text-teal-500 text-5xl">•</div>
          </template>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Smooth gradient text animation */
.bg-gradient-to-r {
  background-size: 200% auto;
  animation: gradient 3s ease infinite;
}

@keyframes gradient {
  0% { background-position: 0% center; }
  50% { background-position: 100% center; }
  100% { background-position: 0% center; }
}
</style>