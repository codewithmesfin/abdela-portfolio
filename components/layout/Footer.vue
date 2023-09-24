<template>
  <div>
    <div class="bg-blue-600">
      <div class="mx-auto md:w-[90%] py-4">
        <h1 class="text-sm text-center text-gray-200">
        Powered by
              <NuxtLink
                class="text-white font-extrabold"
                href="https://bizenforce.com"
                target="_blank"
                >Bizenforce</NuxtLink
              > - 2023
            </h1>
      </div>
    </div>
  </div>
</template>

<script setup>
const links = [
  { title: "AI", href: "/learn/ai", current: false },
  { title: "ML", href: "/learn/ml", current: false },
  { title: "Web3", href: "/learn/web3", current: false },
  { title: "Blockchain", href: "/learn/blockchain", current: false },
  { title: "Marketing", href: "/learn/dm", current: false },
  { title: "CRM", href: "/learn/crm", current: false },
];
const socials = [
  {
    title: "Facebook",
    href: "https://www.facebook.com/bizenforce",
  },
  {
    title: "Linkedin",
    href: "https://linkedin.com/in/mesfin-tsegaye",
  },
  {
    title: "Github",
    href: "https://github.com/sciemesfin",
  },
];
</script>

<style></style>
