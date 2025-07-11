<script setup lang="ts">
const stories = [
  {
    id: 1,
    name: "Tendai M.",
    age: 19,
    location: "Harare",
    role: "Tech Apprentice",
    quote: "The coding skills I learned changed my life. I now develop apps for local businesses.",
    image: "/img/tech_story.jpg",
    tags: ["#Technology", "#Entrepreneurship"]
  },
  {
    id: 2,
    name: "Rumbidzai C.",
    age: 21,
    location: "Bulawayo",
    role: "Community Health Worker",
    quote: "I'm helping fight substance abuse in my community through peer education.",
    image: "/img/utsanana_story.jpg",
    tags: ["#Health", "#Leadership"]
  },
  {
    id: 3,
    name: "Tinashe K.",
    age: 24,
    location: "Masvingo",
    role: "Sustainable Farmer",
    quote: "The agricultural training helped me turn barren land into a thriving organic farm.",
    image: "/img/farmer_story.jpg",
    tags: ["#Agriculture", "#Sustainability"]
  }
]
</script>

<template>
  <section class="py-20 bg-gradient-to-b from-gray-50 to-white">
    <div class="max-w-7xl mx-auto px-6">
      <!-- Section Header -->
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold text-blue-900 mb-4">
          Youth <span class="text-sky-500">Success Stories</span>
        </h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto">
          Real transformations from young people across Zimbabwe
        </p>
      </div>

      <!-- Stories Grid -->
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Story Card -->
        <div v-for="story in stories" :key="story.id" 
             class="bg-white rounded-2xl overflow-hidden shadow-lg hover:shadow-xl transition-all duration-300 group">
          <!-- Image -->
          <div class="relative h-64 overflow-hidden">
            <NuxtImg 
              :src="story.image" 
              :alt="`${story.name}'s story`"
              class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105"
            />
            <div class="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent"></div>
            <div class="absolute bottom-4 left-4">
              <span class="inline-block px-3 py-1 bg-sky-500 text-white rounded-full text-sm font-bold">
                {{ story.location }}
              </span>
            </div>
          </div>
          
          <!-- Content -->
          <div class="p-6">
            <div class="flex items-center mb-3">
              <h3 class="text-xl font-bold text-gray-900">{{ story.name }}, {{ story.age }}</h3>
            </div>
            <p class="text-gray-600 font-medium mb-2">{{ story.role }}</p>
            <p class="text-gray-700 mb-4 italic">"{{ story.quote }}"</p>
            
            <!-- Tags -->
            <div class="flex flex-wrap gap-2 mt-4">
              <span v-for="(tag, index) in story.tags" :key="index"
                    class="px-2 py-1 bg-gray-100 text-gray-700 text-xs font-medium rounded-full">
                {{ tag }}
              </span>
            </div>
          </div>
        </div>
      </div>

      <!-- CTA -->
      <div class="text-center mt-16">
        <UButton size="xl" color="sky" variant="solid" class="px-8">
          <span class="font-bold">Share Your Story</span>
          <UIcon name="i-heroicons-arrow-right" class="ml-2 w-5 h-5" />
        </UButton>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Smooth hover effects */
.group:hover .group-hover\:scale-105 {
  transform: scale(1.05);
}
</style>