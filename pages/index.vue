<template>
  <div>
    <Head>
      <Title>Mesfin Tsegaye - Software Engineering Lead</Title>
      <Meta
        name="description"
        content="Mesfin Tsegaye is passionate full-stack developer with over five years of industry expertise, specializing in remote-based roles across multiple global locations."
      />
    </Head>
    <section class="w-full mx-auto max-w-[90%] h-full py-16">
      <div class="md:flex justify-evenly md:space-x-10 items-center">
        <div class="w-full md:w-1/2">
          <img
            src="~/assets/pics/i1.jpeg"
            class="object-contain h-full w-full max-h-[500px]"
            alt="Mesfin"
          />
        </div>
        <div class="py-10 w-full md:w-1/2">
          <h1 class="text-4xl md:text-6xl">Greetings, I am</h1>
          <h1 class="text-4xl py-3 brand md:text-6xl font-extrabold">
            Abdela Ahmed
          </h1>
          <h1 class="text-2xl py-2 md:text-3xl brand">
            Teacher Development Program Coordinator at Oromia Education Bureau
          </h1>

          <p class="py-5">
            I stand as a devoted education enthusiast, boasting a formidable
            history of advancing teacher capabilities, spearheading meticulous
            monitoring and evaluation endeavors, and exhibiting resolute
            leadership in the realm of education. Across a wealth of
            undertakings, I have adeptly orchestrated training initiatives,
            meticulously upheld regulatory standards, and adeptly overseen
            data-centric procedures. My unwavering commitment revolves around
            nurturing conducive learning milieus and propelling the frontiers of
            educational distinction. My adeptness encompasses a trilingual
            proficiency in English, Amharic, and Afan Oromo, further amplifying
            my prowess in effective communication and seamless collaboration.
          </p>
          <h1 class="text-lg md:text-3xl py-5 pb-1">Get in touch with me</h1>
          <div class="py-5">
            <div
              v-for="(item, i) in items"
              :key="i"
              class="flex md:space-x-3 py-1 border-b border-gray-100"
            >
              <p class="w-1/4">{{ item.title }}</p>
              <NuxtLink
                :href="item.href"
                target="_blank"
                class="w-full md:pl-5 text-green-600"
                >{{ item.value }}
              </NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const items = [
  {
    title: "Phone Number",
    value: "+251 91 176 9390",
    href: "tel:+251911769390",
  },
  {
    title: "Email",
    value: "abdellahmed99@gmail.com",
    href: "mailto:abdellahmed99@gmail.com",
  },
  {
    title: "Alternative Email",
    value: "abdellaahmedmuhamed@gmail.com",
    href: "mailto:abdellaahmedmuhamed@gmail.com",
  },

  {
    title: "X (Twitter)",
    value: "@abdella47639275",
    href: "https://twitter.com/abdella47639275",
  },
  {
    title: "Facebook",
    value: "Abdela Ahmed",
    href: "https://www.facebook.com/profile.php?id=100005999175443&mibextid=ZbWKwL",
  },
  
  {
    title: "Telegram",
    value: "@ahm0911",
    href: "https://t.me/ahm0911",
  },
  {
    title: "Address",
    value: "Addis Ababa, Ethiopia",
    href: "https://en.wikipedia.org/wiki/Addis_Ababa",
  },
];
</script>
