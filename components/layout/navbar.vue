<template>
  <div class="sticky py-2 z-10 top-0 bg-green-600">
    <div class="mx-auto md:max-w-[90%]">
      <div class="flex items-center justify-between">
        <div class="flex items-center justify-between md:justify-start w-full">
          <NuxtLink
            href="/"
            class="text-xl flex items-center text-white font-bold lg:ml-2.5"
          >
            <img
              class="ml-3 w-8 h-8 rounded-full ring-2 ring-gray-300 dark:ring-gray-500"
              src="~/assets/abdela.png"
              alt="Bordered avatar"
            />
            <span class="self-center pl-2 whitespace-nowrap">Abdella Ahmed</span>
          </NuxtLink>
          <button
            @click="toggleSidebar"
            aria-expanded="true"
            aria-controls="sidebar"
            class="lg:hidden mr-2 text-white cursor-pointer p-2"
          >
            <Icon path="menu" />
          </button>
        </div>
        <div class="hidden md:flex items-center md:space-x-10 w-full">
          <div
            class="items-center md:space-x-8 justify-items-start md:justify-items-center md:flex md:pt-2 w-full left-0 top-10 px-5"
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
          </div>
        </div>
      </div>
    </div>
    <div class="flex md:hidden overflow-hidden sidebar">
      <aside
        id="sidebar"
        :class="{
          'hidden lg:flex': sidebarCollapsed,
          'lg:flex': !sidebarCollapsed,
        }"
        class="fixed z-20 h-full border-r top-0 left-0 flex lg:flex flex-shrink-0 flex-col w-64 transition-width duration-75"
        aria-label="Sidebar"
      >
        <div class="relative flex-1 flex flex-col min-h-0 sidebar pt-0">
          <div class="flex-1 flex flex-col pt-5 pb-4 overflow-y-auto">
            <div class="flex-1 px-3 sidebar divide-y space-y-1">
              <ul class="space-y-2 pb-2 w-full">
                <li class="flex justify-between items-center">
                  <NuxtLink
                    href="/"
                    class="text-xl brand font-bold lg:ml-2.5"
                  >
                    
                    <span class="self-center pl-3 t whitespace-nowrap"
                      >Abdella Ahmed</span
                    >
                  </NuxtLink>
                  <button
                    @click="toggleSidebar"
                    aria-expanded="true"
                    aria-controls="sidebar"
                    class="lg:hidden m-2 text-gray-600 hover:text-gray-900 cursor-pointer p-2 hover:bg-gray-100 focus:bg-gray-100 focus:ring-2 focus:ring-gray-100 rounded"
                  >
                    <Icon path="close" fill="red" stroke-color="red" />
                  </button>
                </li>
                <li v-for="item in navigation" :key="item.name">
                  <nuxt-link
                    :href="item.href"
                    @click="toggleSidebar"
                    :target="item.name === 'Curriculum Vitae' ? '_blank' : ''"
                    class="text-base font-normal rounded-lg flex items-center p-2 group"
                  >
                    <span class="ml-3">{{ item.name }} </span>
                  </nuxt-link>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </aside>
    </div>
  </div>
</template>

<script setup>
import Icon from "~~/components/icon.vue";

import { ref } from "vue";

const sidebarCollapsed = ref(true);

const toggleSidebar = () => {
  sidebarCollapsed.value = !sidebarCollapsed.value;
};
const navigation = [
  { name: "Home", href: "/", current: false },
  { name: "Experiences", href: "/experiences", current: false },
  { name: "Skills", href: "/skills", current: false },
  { name: "Education", href: "/education", current: false },
  { name: "Gallery", href: "/gallery", current: false },
  { name: "Curriculum Vitae", href: "/resume.pdf", current: false },
];
</script>
