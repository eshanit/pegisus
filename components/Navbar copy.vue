<script setup lang="ts">
import { ref } from 'vue'
import { NuxtImg } from '#components'
import Reports from './Reports.vue'


const showPrograms = ref(false)
const showAbout = ref(false)
const showTag = ref(false)
const showNews = ref(false)
const showReports = ref(false)

const isMenuOpen = ref(false)
const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value
}
</script>

<template>
    <nav class="bg-white py-14">
        <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
            <div class="flex h-20 items-center justify-between">
                <!-- Logo and desktop menu -->
                <div class="flex items-center py-5">
                    <div class="flex-shrink-0">
                        <NuxtImg class="h-36 w-auto" src="/img/pegi_logo.png" alt="pegisus" />
                    </div>
                </div>

                <!-- Desktop right menu -->
                <div class=" items-center gap-8 ">
                    <!-- Social media icons with animations -->
                    <div class="flex items-center space-x-4">
                        <UButton class="" size="xl">
                            Donate
                        </UButton>

                        <a href="https://www.facebook.com/ymcas" aria-label="World YMCA Facebook Link" title="Facebook"
                            class="social-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30"
                                fill="currentColor">
                                <path
                                    d="M22 16l1-5h-5V7c0-1.544.784-2 3-2h2V0h-4c-4.072 0-7 2.435-7 7v4H7v5h5v14h6V16h4z" />
                            </svg>
                        </a>
                        <a href="https://www.instagram.com/worldymca/" aria-label="World YMCA Instagram Link"
                            title="Instagram" class="social-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30"
                                fill="currentColor">
                                <path
                                    d="M15 11.014A3.986 3.986 0 0118.986 15 3.986 3.986 0 0115 18.986 3.986 3.986 0 0111.014 15 3.986 3.986 0 0115 11.014M15 9a6 6 0 00-6 6 6 6 0 006 6 6 6 0 006-6 6 6 0 00-6-6z" />
                                <path
                                    d="M21.723 5H8.277C6.527 5 5 6.527 5 8.277v13.446C5 23.473 6.527 25 8.277 25h13.446C23.473 25 25 23.473 25 21.723V8.277C25 6.527 23.473 5 21.723 5m-.724 16.5a.75.75 0 01-.75.75H9.75a.75.75 0 01-.75-.75V9.75a.75.75 0 01.75-.75h10.5a.75.75 0 01.75.75v10.5z" />
                                <circle cx="21.5" cy="8.5" r="1.5" />
                            </svg>
                        </a>
                        <a href="https://www.linkedin.com/company/worldymca/" aria-label="World YMCA LinkedIn Link"
                            title="LinkedIn" class="social-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30"
                                fill="currentColor">
                                <path
                                    d="M24 4H6a2 2 0 00-2 2v18a2 2 0 002 2h18a2 2 0 002-2V6a2 2 0 00-2-2zM10.954 22h-2.95v-9.492h2.95V22zM9.449 11.151a1.72 1.72 0 11-.001-3.439 1.72 1.72 0 01.001 3.439zM22 22h-2.948v-4.616c0-1.101-.02-2.517-1.533-2.517-1.535 0-1.771 1.199-1.771 2.437V22h-2.948v-9.492h2.83v1.297h.04c.394-.746 1.356-1.533 2.791-1.533 2.987 0 3.539 1.966 3.539 4.522V22z" />
                            </svg>
                        </a>
                        <a href="https://www.youtube.com/user/ymcaworld" aria-label="World YMCA YouTube Link"
                            title="YouTube" class="social-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30"
                                fill="currentColor">
                                <path
                                    d="M27.687 8.471a3.634 3.634 0 00-2.56-2.56C22.665 5 15 5 15 5s-7.665 0-10.127.911a3.634 3.634 0 00-2.56 2.56C1.5 10.934 1.5 15 1.5 15s0 4.066.911 6.529a3.634 3.634 0 002.56 2.56C7.335 25 15 25 15 25s7.665 0 10.127-.911a3.634 3.634 0 002.56-2.56C28.5 19.066 28.5 15 28.5 15s0-4.066-.813-6.529zM12.818 19.318V10.682L19.636 15l-6.818 4.318z" />
                            </svg>
                        </a>
                        <a href="https://www.flickr.com/photos/ymcaworld/albums" aria-label="World YMCA Flickr Link"
                            title="Flickr" class="social-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30"
                                fill="currentColor">
                                <circle cx="9" cy="15" r="6" />
                                <circle cx="21" cy="15" r="6" />
                            </svg>
                        </a>
                    </div>

                    <div class=" py-5" />

                    <div class="items-center gap-8">

                        <div class="ml-10 flex items-baseline space-x-6">
                            <!-- About Dropdown -->
                                  <a href="#"
                                class="rounded-md px-3 py-2 text-lg font-extrabold text-gray-700 hover:bg-gray-100 hover:text-gray-900 cursor-pointer"
                                @mouseover="showAbout = true">About</a>

                            <!-- Other menu items... -->
                            <a href="#"
                                class="rounded-md px-3 py-2 text-lg font-extrabold text-gray-700 hover:bg-gray-100 hover:text-gray-900 cursor-pointer"
                                @mouseover="showPrograms = true">Programs</a>
                            <a href=" #"
                                class="rounded-md px-3 py-2 text-lg font-extrabold text-gray-700 hover:bg-gray-100 hover:text-gray-900">TAG</a>
                            <a href="#"
                                class="rounded-md px-3 py-2 text-lg font-extrabold text-gray-700 hover:bg-gray-100 hover:text-gray-900">News</a>
                            <a href="#"
                                class="rounded-md px-3 py-2 text-lg font-extrabold text-gray-700 hover:bg-gray-100 hover:text-gray-900">Reports</a>
                            <UButton
                                class="bg-red-500 text-white hover:bg-red-600 px-4 py-2 rounded-md text-lg font-semibold"
                                size="xl">
                                Take Action !
                            </UButton>
                        </div>
                    </div>
                </div>

                <!-- Mobile menu button -->
                <div class="-mr-2 flex md:hidden">
                    <button @click="toggleMenu" type="button"
                        class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-700 hover:bg-gray-100 hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
                        aria-controls="mobile-menu" aria-expanded="false">
                        <span class="absolute -inset-0.5"></span>
                        <span class="sr-only">Open main menu</span>
                        <svg class="block h-8 w-8" :class="{ 'hidden': isMenuOpen, 'block': !isMenuOpen }" fill="none"
                            viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
                        </svg>
                        <svg class="block h-8 w-8" :class="{ 'hidden': !isMenuOpen, 'block': isMenuOpen }" fill="none"
                            viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                        </svg>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile menu -->
        <div class="md:hidden" id="mobile-menu" v-show="isMenuOpen">
            <div class="space-y-1 px-2 pb-3 pt-2 sm:px-3">
                <a href="#" class="block rounded-md bg-indigo-50 px-3 py-3 text-xl font-semibold text-indigo-600"
                    aria-current="page">Dashboard</a>
                <a href="#"
                    class="block rounded-md px-3 py-3 text-xl font-medium text-gray-700 hover:bg-gray-100 hover:text-gray-900">Programs</a>
                <a href="#"
                    class="block rounded-md px-3 py-3 text-xl font-medium text-gray-700 hover:bg-gray-100 hover:text-gray-900">TAG</a>
                <a href="#"
                    class="block rounded-md px-3 py-3 text-xl font-medium text-gray-700 hover:bg-gray-100 hover:text-gray-900">News</a>
                <a href="#"
                    class="block rounded-md px-3 py-3 text-xl font-medium text-gray-700 hover:bg-gray-100 hover:text-gray-900">Reports</a>
            </div>
            <div class="border-t border-gray-200 pb-3 pt-4">
                <div class="flex items-center px-5">
                    <div class="flex-shrink-0">
                        <img class="h-10 w-10 rounded-full"
                            src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                            alt="">
                    </div>
                    <div class="ml-3">
                        <div class="text-lg font-medium text-gray-800">John Doe</div>
                        <div class="text-sm font-medium text-gray-500">john@example.com</div>
                    </div>
                    <button type="button"
                        class="relative ml-auto flex-shrink-0 rounded-full bg-white p-1 text-gray-600 hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2">
                        <span class="absolute -inset-1.5"></span>
                        <span class="sr-only">View notifications</span>
                        <svg class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
                            aria-hidden="true">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M14.857 17.082a23.848 23.848 0 0 0 5.454-1.31A8.967 8.967 0 0 1 18 9.75V9A6 6 0 0 0 6 9v.75a8.967 8.967 0 0 1-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 0 1-5.714 0m5.714 0a3 3 0 1 1-5.714 0" />
                        </svg>
                    </button>
                </div>
                <div class="mt-3 space-y-1 px-2">
                    <div class="flex justify-center space-x-4 py-4">
                        <a href="https://www.facebook.com/ymcas" aria-label="World YMCA Facebook Link" title="Facebook"
                            class="social-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30"
                                fill="currentColor">
                                <path
                                    d="M22 16l1-5h-5V7c0-1.544.784-2 3-2h2V0h-4c-4.072 0-7 2.435-7 7v4H7v5h5v14h6V16h4z" />
                            </svg>
                        </a>
                        <a href="https://www.instagram.com/worldymca/" aria-label="World YMCA Instagram Link"
                            title="Instagram" class="social-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30"
                                fill="currentColor">
                                <path
                                    d="M15 11.014A3.986 3.986 0 0118.986 15 3.986 3.986 0 0115 18.986 3.986 3.986 0 0111.014 15 3.986 3.986 0 0115 11.014M15 9a6 6 0 00-6 6 6 6 0 006 6 6 6 0 006-6 6 6 0 00-6-6z" />
                                <path
                                    d="M21.723 5H8.277C6.527 5 5 6.527 5 8.277v13.446C5 23.473 6.527 25 8.277 25h13.446C23.473 25 25 23.473 25 21.723V8.277C25 6.527 23.473 5 21.723 5m-.724 16.5a.75.75 0 01-.75.75H9.75a.75.75 0 01-.75-.75V9.75a.75.75 0 01.75-.75h10.5a.75.75 0 01.75.75v10.5z" />
                                <circle cx="21.5" cy="8.5" r="1.5" />
                            </svg>
                        </a>
                        <a href="https://www.linkedin.com/company/worldymca/" aria-label="World YMCA LinkedIn Link"
                            title="LinkedIn" class="social-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30"
                                fill="currentColor">
                                <path
                                    d="M24 4H6a2 2 0 00-2 2v18a2 2 0 002 2h18a2 2 0 002-2V6a2 2 0 00-2-2zM10.954 22h-2.95v-9.492h2.95V22zM9.449 11.151a1.72 1.72 0 11-.001-3.439 1.72 1.72 0 01.001 3.439zM22 22h-2.948v-4.616c0-1.101-.02-2.517-1.533-2.517-1.535 0-1.771 1.199-1.771 2.437V22h-2.948v-9.492h2.83v1.297h.04c.394-.746 1.356-1.533 2.791-1.533 2.987 0 3.539 1.966 3.539 4.522V22z" />
                            </svg>
                        </a>
                        <a href="https://www.youtube.com/user/ymcaworld" aria-label="World YMCA YouTube Link"
                            title="YouTube" class="social-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30"
                                fill="currentColor">
                                <path
                                    d="M27.687 8.471a3.634 3.634 0 00-2.56-2.56C22.665 5 15 5 15 5s-7.665 0-10.127.911a3.634 3.634 0 00-2.56 2.56C1.5 10.934 1.5 15 1.5 15s0 4.066.911 6.529a3.634 3.634 0 002.56 2.56C7.335 25 15 25 15 25s7.665 0 10.127-.911a3.634 3.634 0 002.56-2.56C28.5 19.066 28.5 15 28.5 15s0-4.066-.813-6.529zM12.818 19.318V10.682L19.636 15l-6.818 4.318z" />
                            </svg>
                        </a>
                        <a href="https://www.flickr.com/photos/ymcaworld/albums" aria-label="World YMCA Flickr Link"
                            title="Flickr" class="social-icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30"
                                fill="currentColor">
                                <circle cx="9" cy="15" r="6" />
                                <circle cx="21" cy="15" r="6" />
                            </svg>
                        </a>
                    </div>
                    <a href="#"
                        class="block rounded-md px-3 py-2 text-lg font-medium text-gray-700 hover:bg-gray-100 hover:text-gray-900">Your
                        Profile</a>
                    <a href="#"
                        class="block rounded-md px-3 py-2 text-lg font-medium text-gray-700 hover:bg-gray-100 hover:text-gray-900">Settings</a>
                    <a href="#"
                        class="block rounded-md px-3 py-2 text-lg font-medium text-gray-700 hover:bg-gray-100 hover:text-gray-900">Sign
                        out</a>
                </div>
            </div>
        </div>
    </nav>
    <Transition>
        <div v-if="showPrograms" @mouseenter="showPrograms = true" @mouseleave="showPrograms = false"
            class="absolute z-10 w-full max-w-full">
            <Programs />
        </div>
    </Transition>
    <Transition>
        <div v-if="showAbout" @mouseenter="showAbout = true" @mouseleave="showAbout = false"
            class="absolute z-10 w-full max-w-full">
            <About />
        </div>
    </Transition>
  <Transition>
        <div v-if="showTag" @mouseenter="showTag = true" @mouseleave="showTag = false"
            class="absolute z-10 w-full max-w-full">
            <Tag />
        </div>
    </Transition>
  <Transition>
        <div v-if="showReports" @mouseenter="showReports = true" @mouseleave="showReports = false"
            class="absolute z-10 w-full max-w-full">
            <Reports />
        </div>
    </Transition>
     <Transition>
        <div v-if="showNews" @mouseenter="showNews = true" @mouseleave="showNews = false"
            class="absolute z-10 w-full max-w-full">
            <News />
        </div>
    </Transition>
</template>

<style>
.v-enter-active,
.v-leave-active {
    transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
    opacity: 0;
}

.social-icon:hover {
    animation: bounce 0.5s ease;
    transform: translateY(-5px);
}

/* Individual colors for each social icon */
.social-icon:nth-child(1) {
    color: #3b5998;
}

/* Facebook blue */
.social-icon:nth-child(2) {
    color: #E1306C;
}

/* Instagram pink */
.social-icon:nth-child(3) {
    color: #0077B5;
}

/* LinkedIn blue */
.social-icon:nth-child(4) {
    color: #FF0000;
}

/* YouTube red */
.social-icon:nth-child(5) {
    color: #FF0084;
}

/* Flickr pink */

@keyframes bounce {

    0%,
    100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-10px);
    }
}

[data-headlessui-state~="open"] [data-headlessui-popover] {
    width: 100vw;
    left: 0;
    right: 0;
    background-color: #f3f4f6;
    /* Tailwind's bg-gray-100 */
    z-index: 10;
}

[data-headlessui-state~="open"] [data-headlessui-popover]>div {
    margin: 0 auto;
    max-width: 80rem;
    padding: 0.75rem 1rem;
}
</style>