<template>
  <div class="h-full">
    <Head>
      <Title>Abdela Ahmed </Title>
      <Meta
        name="description"
        content="Teacher Development Program Coordinator at Oromia Education Bureau"
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
          <h1 class="text-4xl md:text-4xl font-bold py-2">My Skills</h1>
          <div v-for="(item, i) in skills" :key="i">
            <div class="flex items-center py-1 ml-3">
              <div class="text-green-600">
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
              <span class="pl-2 text-sm">{{ item }}</span>
            </div>
          </div>
          <h1 class="text-4xl md:text-4xl font-bold mt-10 py-2">
            Language Skills
          </h1>
          <div v-for="(item, i) in languages" :key="i">
            <div class="flex items-center py-1 ml-3">
              <div class="text-green-600">
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
              <span class="pl-2 text-sm">{{ item }}</span>
            </div>
          </div>
        </section>
      </div>
    </div>
  </div>
</template>

<script setup>
const skills = [
  "Leadership",
  `Strong commitment, energy, trustworthiness, and integrity to meet challenging goals.`,
  `Excellent teamwork and leadership skills gained from experience in government organizations.`,
  `Proven ability to work under pressure and take initiative.`,
  `Effective workload prioritization aligned with organizational values.`,
  `Exceptional communication skills, fostering open and transparent dialogue within teams.`,
  `Demonstrated adaptability to evolving situations and a continuous learning mindset.`,
  `Adept at conflict resolution, promoting harmony and productivity among team members.`,
  `Innovation-driven mindset, driving creativity and problem-solving within the organization.`,
  `Consistent track record of achieving and surpassing performance targets.`,
  `Strong ethical compass, ensuring all decisions align with organizational and societal values.`,
 ` Exceptional problem-solving abilities, with a history of resolving complex issues.`,
`Visionary leadership, guiding teams towards long-term strategic goals.`,
`Empowering leadership style, encouraging team members to reach their full potential.`,
`Skilled in stakeholder management and building strong relationships across diverse groups.`,
`High level of emotional intelligence, facilitating effective collaboration and conflict resolution.`
];
const languages = ["English", "Afan Oromo", "Amharic"];
</script>
