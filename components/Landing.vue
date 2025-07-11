<script setup lang="ts">
const images = [
  '/img/youth.jpg',
  '/img/landing2.png',
  '/img/workshops.jpg'
]

const actionWords = [
  { text: 'thrive', color: 'text-sky-500' },
  { text: 'succeed', color: 'text-emerald-500' },
  { text: 'flourish', color: 'text-amber-500' }
]

const currentIndex = ref(0)

onMounted(() => {
  const interval = setInterval(() => {
    currentIndex.value = (currentIndex.value + 1) % images.length
  }, 6000)
  
  onUnmounted(() => clearInterval(interval))
})
</script>

<template>
  <div class="py-28">
    <div class="grid lg:grid-cols-2 gap-8">
      <div class="relative h-full min-h-[400px]">
        <Transition name="fade" mode="out-in">
          <NuxtImg 
            :key="images[currentIndex]" 
            :src="images[currentIndex]" 
            class="rounded-2xl shadow-amber-400 absolute inset-0 w-full h-full object-cover"
            alt="Youth programs"
          />
        </Transition>
      </div>
      <div>
        <div class="text-6xl font-bold text-blue-900 mb-4">
          Creating pathways for youth to 
          <Transition name="fade" mode="out-in">
            <span :key="actionWords[currentIndex].text" :class="actionWords[currentIndex].color">
              {{ actionWords[currentIndex].text }}
            </span>
          </Transition>
          in a rapidly changing world.
        </div>
        <div class="text-lg text-gray-700 mb-6">
          Education, Skills Training, Entrepreneurship and Social Enterprises that connect youth in Zimbabwe to employment opportunities. In turn, we're kick-starting a hyperlocal community ecosystem
        </div>
        <div class="flex justify-end">
          <UButton to="/programs" size="xl">
            <div class="font-bold">Sign Up</div> 
          </UButton>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 1.5s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

/* Ensure container maintains size during transition */
.min-h-[400px] {
  min-height: 400px;
}

/* Smooth color transitions */
span {
  transition: color 1.5s ease;
}
</style>