<template>
  <div>
    <div class="bg-blue-600">
      <div class="mx-auto md:w-[90%] py-4">
        <div class="md:flex md:justify-evenly">
          <div class="flex flex-wrap justify-center px-3">
            <div
              v-for="(nav, i) in navigation"
              :key="i"
              class="py-1 text-white"
            >
              <nuxt-link
                :href="nav.href"
                :target="nav.name === 'Curriculum Vitae' ? '_blank' : ''"
                class="p-3"
              >
                {{ nav.name }}
              </nuxt-link>
            </div>
          </div>
          <h1 class="text-sm text-center text-gray-200 p-3">
            Powered by
            <NuxtLink
              class="text-white font-extrabold"
              href="https://bizenforce.com"
              target="_blank"
              >Bizenforce</NuxtLink
            >
            - 2023
          </h1>
        </div>
        <!-- <div
            class=" grid grid-cols-2 md:grid-cols-4 gap-4"
          >
            <span
              v-for="(nav, i) in navigation"
              :key="i"
              class="py-1 text-white"
            >
              <nuxt-link
                :href="nav.href"
                :target="nav.name === 'Curriculum Vitae' ? '_blank' : ''"
                :class="
                  $route.path === nav.href
                    ? 'flex brand hover:text-blue-500 cursor-pointer transition-colors duration-300'
                    : 'flex cursor-pointer transition-colors duration-300'
                "
              >
                {{ nav.name }}
              </nuxt-link>
            </span>
          </div> -->
      </div>
    </div>
  </div>
</template>

<script setup>
const navigation = [
  { name: "Home", href: "/", current: false },
  { name: "Experiences", href: "/experiences", current: false },
  { name: "Skills", href: "/skills", current: false },
  { name: "Education", href: "/education", current: false },
  { name: "Gallery", href: "/gallery", current: false },
  { name: "Curriculum Vitae", href: "/resume.pdf", current: false },
];
</script>

<style></style>
