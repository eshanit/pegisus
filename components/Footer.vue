<template>
  <footer class="bg-blue-900 text-white pt-16 pb-8">
    <div class="max-w-7xl mx-auto px-6">
      <!-- Main Footer Content -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12">
        <!-- About Section -->
        <div class="space-y-6">
          <h3 class="text-2xl font-bold">
            <span class="text-sky-400">Youth</span> Pegasis
          </h3>
          <p class="text-blue-100">
            Empowering young people in Southern Africa through education, skills development, and community building.
          </p>
          <div class="flex space-x-4">
            <a href="#" class="text-blue-200 hover:text-white transition-colors">
              <UIcon name="i-bxl-facebook" class="w-6 h-6" />
            </a>
            <a href="#" class="text-blue-200 hover:text-white transition-colors">
              <UIcon name="i-bxl-twitter" class="w-6 h-6" />
            </a>
            <a href="#" class="text-blue-200 hover:text-white transition-colors">
              <UIcon name="i-bxl-instagram" class="w-6 h-6" />
            </a>
            <a href="#" class="text-blue-200 hover:text-white transition-colors">
              <UIcon name="i-bxl-linkedin" class="w-6 h-6" />
            </a>
          </div>
        </div>

        <!-- Join Us Section -->
        <div class="space-y-6">
          <h4 class="text-lg font-semibold uppercase tracking-wider text-sky-400">Join Us</h4>
          <ul class="space-y-3">
            <li><a href="#" class="text-blue-100 hover:text-white transition-colors">For Students</a></li>
            <li><a href="#" class="text-blue-100 hover:text-white transition-colors">For Employers</a></li>
            <li><a href="#" class="text-blue-100 hover:text-white transition-colors">Volunteer</a></li>
            <li><a href="#" class="text-blue-100 hover:text-white transition-colors">Partner With Us</a></li>
            <li><a href="#" class="text-blue-100 hover:text-white transition-colors">Careers</a></li>
          </ul>
        </div>

        <!-- Contact Section -->
        <div class="space-y-6">
          <h4 class="text-lg font-semibold uppercase tracking-wider text-sky-400">Contact Us</h4>
          <address class="not-italic space-y-3 text-blue-100">
            <div class="flex items-start">
              <UIcon name="i-heroicons-map-pin" class="w-5 h-5 mt-0.5 mr-3 flex-shrink-0" />
              <span>123 Youth Avenue, Masvingo, Zimbabwe</span>
            </div>
            <div class="flex items-center">
              <UIcon name="i-heroicons-phone" class="w-5 h-5 mr-3 flex-shrink-0" />
              <span>+263 123 456 789</span>
            </div>
            <div class="flex items-center">
              <UIcon name="i-heroicons-envelope" class="w-5 h-5 mr-3 flex-shrink-0" />
              <span>info@youthpagisus.org</span>
            </div>
          </address>
        </div>

        <!-- Newsletter Section -->
        <div class="space-y-6">
          <h4 class="text-lg font-semibold uppercase tracking-wider text-sky-400">Stay Updated</h4>
          <p class="text-blue-100">
            Subscribe to our newsletter for the latest programs and success stories.
          </p>
          <form class="space-y-3">
            <input 
              type="email" 
              placeholder="Your email address" 
              class="w-full px-4 py-3 rounded-lg bg-blue-800 border border-blue-700 focus:outline-none focus:ring-2 focus:ring-sky-400 text-white placeholder-blue-300"
            >
            <UButton 
              type="submit" 
              color="sky" 
              size="md" 
              class="w-full justify-center"
            >
              Subscribe
            </UButton>
          </form>
        </div>
      </div>

      <!-- Divider -->
      <div class="border-t border-blue-800 my-12"></div>

      <!-- Bottom Footer -->
      <div class="flex flex-col md:flex-row justify-between items-center">
        <p class="text-blue-300 text-sm">
          © 2025 Youth Pegisus. All rights reserved.
        </p>
        <div class="flex space-x-6 mt-4 md:mt-0">
          <a href="#" class="text-blue-300 hover:text-white text-sm transition-colors">Privacy Policy</a>
          <a href="#" class="text-blue-300 hover:text-white text-sm transition-colors">Terms of Service</a>
          <a href="#" class="text-blue-300 hover:text-white text-sm transition-colors">Accessibility</a>
        </div>
      </div>
    </div>
  </footer>
</template>