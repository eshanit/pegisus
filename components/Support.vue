<script setup lang="ts">
</script>

<template>
    <div class="text-4xl">
        <div> There are
            <span
                class="font-semibold bg-clip-text text-transparent bg-gradient-to-r from-green-600 to-blue-600 dark:from-green-400 dark:to-blue-400">20
                million young people aged 15-24 <br /> in Southern Africa</span>
        </div>
    </div>
    <div class="text-2xl mt-4">This is how we support them, and their communities</div>

    <div class="py-8" />

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
        <!-- Community Well Being -->
        <div class="group relative h-80 w-full overflow-hidden shadow-lg transition-all duration-300 bg-gray-50 rounded-xl">
            <!-- Default Content -->
            <div class="absolute inset-0 flex flex-col group-hover:opacity-0 group-hover:scale-90 transition-all duration-300 p-6">
                <h3 class="text-xl font-bold mb-4">Community Well Being</h3>
                <p class="text-base font-semibold mb-4">We nurture young people in body, mind and spirit.</p>
                <div class="mt-auto">
                    <NuxtImg src="/img/youth1.jpg" alt="Health Icon" class="w-full h-40 object-cover rounded-lg" />
                </div>
            </div>

            <!-- Hover Content -->
            <div class="absolute inset-0 bg-gradient-to-br from-green-600 to-blue-500 p-6 flex flex-col justify-between text-white opacity-0 scale-90 group-hover:opacity-100 group-hover:scale-100 transition-all duration-300 rounded-xl">
                <div>
                    <h3 class="text-xl font-bold mb-2">This matters because...</h3>
                    <p class="text-center text-2xl font-semibold">1 in 7</p>
                    <USeparator size="md" class="my-4" />
                    <p class="text-base">Young people aged 5 - 19 experiences some form of mental health disorder</p>
                    <p class="text-xs font-bold mt-2">UN/WHO</p>
                </div>

                <div class="footer bg-gradient-to-r from-green-700 to-blue-700 py-3 px-4 rounded-b-lg -mx-6 -mb-6">
                    <div class="flex justify-between items-center">
                        <span class="text-xs font-medium">Learn more</span>
                        <UIcon name="i-heroicons-arrow-right" class="w-4 h-4" />
                    </div>
                </div>
            </div>
        </div>

        <!-- Meaningful Work -->
        <div class="group relative h-80 w-full overflow-hidden shadow-lg transition-all duration-300 bg-gray-50 rounded-xl">
            <!-- Default Content -->
            <div class="absolute inset-0 flex flex-col group-hover:opacity-0 group-hover:scale-90 transition-all duration-300 p-6">
                <h3 class="text-xl font-bold mb-4">Meaningful Work</h3>
                <p class="text-base font-semibold mb-4">We support worthwhile jobs and sustainable livelihoods</p>
                <div class="mt-auto">
                    <NuxtImg src="/img/electricity.jpeg" alt="Work Icon" class="w-full h-40 object-cover rounded-lg" />
                </div>
            </div>

            <!-- Hover Content -->
            <div class="absolute inset-0 bg-gradient-to-br from-green-600 to-blue-500 p-6 flex flex-col justify-between text-white opacity-0 scale-90 group-hover:opacity-100 group-hover:scale-100 transition-all duration-300 rounded-xl">
                <div>
                    <h3 class="text-xl font-bold mb-2">This matters because...</h3>
                    <p class="text-center text-2xl font-semibold">264 million</p>
                    <USeparator size="md" class="my-4" />
                    <p class="text-base">Young people aged 15 - 24 are not in education, employment or training</p>
                    <p class="text-xs font-bold mt-2">UN/ILO</p>
                </div>

                <div class="footer bg-gradient-to-r from-green-700 to-blue-700 py-3 px-4 rounded-b-lg -mx-6 -mb-6">
                    <div class="flex justify-between items-center">
                        <span class="text-xs font-medium">Learn more</span>
                        <UIcon name="i-heroicons-arrow-right" class="w-4 h-4" />
                    </div>
                </div>
            </div>
        </div>

        <!-- Drug Free -->
        <div class="group relative h-80 w-full overflow-hidden shadow-lg transition-all duration-300 bg-gray-50 rounded-xl">
            <!-- Default Content -->
            <div class="absolute inset-0 flex flex-col group-hover:opacity-0 group-hover:scale-90 transition-all duration-300 p-6">
                <h3 class="text-xl font-bold mb-4">Zero drug and substance abuse</h3>
                <p class="text-base font-semibold mb-4">Thriving towards a clean, drug free youth</p>
                <div class="mt-auto">
                    <NuxtImg src="/img/drugfree.png" alt="Drug Free Icon" class="w-full h-40 object-cover rounded-lg" />
                </div>
            </div>

            <!-- Hover Content -->
            <div class="absolute inset-0 bg-gradient-to-br from-green-600 to-blue-500 p-6 flex flex-col justify-between text-white opacity-0 scale-90 group-hover:opacity-100 group-hover:scale-100 transition-all duration-300 rounded-xl">
                <div>
                    <h3 class="text-xl font-bold mb-2">This matters because...</h3>
                    <p class="text-center text-2xl font-semibold">78 million</p>
                    <USeparator size="md" class="my-4" />
                    <p class="text-base">Young people aged 12 - 24 are affected by substance abuse worldwide</p>
                    <p class="text-xs font-bold mt-2">UN/ILO</p>
                </div>

                <div class="footer bg-gradient-to-r from-green-700 to-blue-700 py-3 px-4 rounded-b-lg -mx-6 -mb-6">
                    <div class="flex justify-between items-center">
                        <span class="text-xs font-medium">Learn more</span>
                        <UIcon name="i-heroicons-arrow-right" class="w-4 h-4" />
                    </div>
                </div>
            </div>
        </div>

        <!-- Equality and Justice -->
        <div class="group relative h-80 w-full overflow-hidden shadow-lg transition-all duration-300 bg-gray-50 rounded-xl">
            <!-- Default Content -->
            <div class="absolute inset-0 flex flex-col group-hover:opacity-0 group-hover:scale-90 transition-all duration-300 p-6">
                <h3 class="text-xl font-bold mb-4">Equality and Justice</h3>
                <p class="text-base font-semibold mb-4">We help amplify youth voices and actions in the community</p>
                <div class="mt-auto">
                    <NuxtImg src="/img/justice.jpg" alt="Justice Icon" class="w-full h-40 object-cover rounded-lg" />
                </div>
            </div>

            <!-- Hover Content -->
            <div class="absolute inset-0 bg-gradient-to-br from-green-600 to-blue-500 p-6 flex flex-col justify-between text-white opacity-0 scale-90 group-hover:opacity-100 group-hover:scale-100 transition-all duration-300 rounded-xl">
                <div>
                    <h3 class="text-xl font-bold mb-2">This matters because...</h3>
                    <p class="text-center text-2xl font-semibold">400 million</p>
                    <USeparator size="md" class="my-4" />
                    <p class="text-base">Young people face discrimination because of their ethnicity and religion</p>
                    <p class="text-xs font-bold mt-2">UN/ILO</p>
                </div>

                <div class="footer bg-gradient-to-r from-green-700 to-blue-700 py-3 px-4 rounded-b-lg -mx-6 -mb-6">
                    <div class="flex justify-between items-center">
                        <span class="text-xs font-medium">Learn more</span>
                        <UIcon name="i-heroicons-arrow-right" class="w-4 h-4" />
                    </div>
                </div>
            </div>
        </div>
    </div>
        <div class="py-8" />
</template>

<style scoped>
.footer {
    transition: all 0.3s ease;
}

.group:hover .footer {
    background: linear-gradient(to right, #047857, #1d4ed8);
}
</style>