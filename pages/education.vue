<template>
  <div class="h-full">
    <Head>
      <Title>Mesfin Tsegaye - Education</Title>
      <Meta
        name="description"
        content="Developed and deployed EtyopAI, an AI system utilizing ChatGPT models, to provide OpenAI Services in Africa"
      />
    </Head>
    <div
      class="mx-auto md:max-w-[90%] h-full w-[100%] px-2 py-10 sm:px-6 lg:px-8"
    >
      <div class="md:flex h-full">
        <section class="hidden md:block w-full md:w-1/2 md:p-10">
          <img
            class="h-8 w-8 md:h-32 md:w-32 rounded-full"
            src="~/assets/abdela.png"
            alt="Workflow"
          />
          <h1 class="text-xl md:text-4xl font-bold py-2">Bio</h1>
          <p>
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
        </section>
        <section class="w-full h-full md:border-l p-2 md:px-10">
          <h1 class="text-4xl md:text-4xl font-bold py-2">Education</h1>
          <div v-for="(item, i) in schools" :key="i" class="my-3 border-b border-gray-100 pb-3">
            <div class="flex items-center py-1 ml-3">
             
              <div class="text-green-600 hidden md:flex">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                  class="w-5 h-5"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M9 12.75L11.25 15 15 9.75M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
                  />
                </svg>
              </div>
              <div class="md:mx-10">
                <img :src="item.img" alt="" class="max-h-24 max-w-24">
              </div>
              <div>
                <h1 class="pl-2 font-semibold text-xl md:text-2xl">{{ item.title }}</h1>
                <p class="pl-2 text-lg md:text-xl">{{ item.subtitle }}</p>
                <p class="pl-2 text-sm">{{ item.time }}</p>
              </div>
            </div>
          </div>
        </section>
      </div>
    </div>
  </div>
</template>

<script setup>
import hu from '~/assets/hu.png'
import aru from '~/assets/aru.png'
import diploma from '~/assets/diploma.jpeg'
import cert from '~/assets/cert.png'
const schools = [
  {
    title: "Master of Art in School Leadership",
    subtitle: "Haramaya University",
    time: "Graduated in 2016",
    img:hu
  },
  {
    title: "Bachelor of Art in History",
    subtitle: "Arba Minch University",
    time: "Graduated in 2009",
    img:aru
  },
  {
    title: "Diploma in History",
    subtitle: "Adama Teachers College",
    time: "Graduated in 2004",
    img:diploma
  },
  {
    title: "Certificate(Grade 9 -12)",
    subtitle: "Dida Robe",
    time: "Graduated in 2002",
    img:cert
  },
];
</script>
