<script setup lang="ts">
import { differenceInDays, differenceInHours, differenceInMinutes, differenceInSeconds } from 'date-fns'

const targetDate = new Date(2025, 7, 4, 8, 0, 0) // August 4, 2025 8:00 AM (months are 0-indexed)

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
  <div class="grid lg:grid-cols-2 gap-5">
    <div id="workshop-info">
      <div class="text-orange-500 text-2xl font-bold mt-6">4-6 August 2025</div>
      <div class="text-4xl mt-4"> Youth against drugs and substance abuse annual workshop</div>
      <div class="text-lg">Location: <span class="text-sky-500">Masvingo, Zimbabwe</span></div>
      <div class="py-2.5" />
      <div>
        Our team from the southern part of Zimbabwe will be hosting our much awaited annual workshop.
        Be prepared to have a blast.
      </div>
      <div class="py-2.5" />
      <div class="w-1/2">
        <div class="grid grid-cols-4 gap-1">
          <div class="flex flex-col items-center">
            <div class="text-3xl font-semibold bg-clip-text">{{
              days }}</div>
            <div class="text-sm text-orange-600 uppercase mt-1">Days</div>
          </div>
          <div class="flex flex-col items-center">
            <div class="text-3xl font-semibold  bg-clip-text">{{
              hours }}</div>
            <div class="text-sm text-orange-600 uppercase mt-1">Hours</div>
          </div>
          <div class="flex flex-col items-center">
            <div class="text-3xl font-semibold  bg-clip-text">{{
              minutes }}</div>
            <div class="text-sm text-orange-600 uppercase mt-1">Minutes</div>
          </div>
          <div class="flex flex-col items-center">
            <div class="text-3xl font-semibold  bg-clip-text">{{
              seconds }}</div>
            <div class="text-sm text-orange-600 uppercase mt-1">Seconds</div>
          </div>
        </div>
      </div>
      <div class="flex justify-between py-2.5">
        <UButton size="xl">
          <span class="font-bold">Book a seat now</span>
        </UButton>
      </div>
    </div>
    <div id="workshop-guest">
      <div class="grid grid-cols-12 ">
        <div id="speaker" class="grid col-span-8">
          <NuxtImg src="/img/linkedIn.jpg" class="rounded-full shadow-amber-400" height="350" width="350" />
          <div id="speaker-info-card" class="bg-white shadow-lg rounded-lg p-5">
            <div class=" text-2xl text-black font-semibold">Eshanit Orongam</div>
            <div>Pharmacology and Toxicants Inc President</div>
            <div class="text-orange-500">Guest Speaker</div>
          </div>
        </div>
        <div id="polka-dots" class="grid col-span-4">
          <div>
            <div class="grid grid-cols-4 gap-2">
              <div class="text-teal-700 text-8xl">.</div>
              <div class="text-teal-700 text-8xl">.</div>
              <div class="text-teal-700 text-8xl">.</div>
              <div class="text-teal-700 text-8xl">.</div>
            </div>
            <div class="grid grid-cols-4 gap-2">
              <div class="text-teal-700 text-8xl">.</div>
              <div class="text-teal-700 text-8xl">.</div>
              <div class="text-teal-700 text-8xl">.</div>
              <div class="text-teal-700 text-8xl">.</div>
            </div>
            <div class="grid grid-cols-4 gap-2">
              <div class="text-teal-700 text-8xl">.</div>
              <div class="text-teal-700 text-8xl">.</div>
              <div class="text-teal-700 text-8xl">.</div>
              <div class="text-teal-700 text-8xl">.</div>
            </div>
            <div class="grid grid-cols-4 gap-2">
              <div class="text-teal-700 text-8xl">.</div>
              <div class="text-teal-700 text-8xl">.</div>
              <div class="text-teal-700 text-8xl">.</div>
              <div class="text-teal-700 text-8xl">.</div>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>
</template>
<style scoped></style>