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
          <h1 class="text-4xl md:text-4xl font-bold py-2">Experience</h1>
          <div v-for="(item, i) in experiences" :key="i">
            <div class="p-5 my-5 card rounded h-full">
              <h1 class="font-bold">
                {{ item.title }}
              </h1>
              <div class="flex justify-between items-center py-1">
                <div>
                  <p class="font-bold text-sm py-1">
                    {{ item.company }}
                  </p>
                  <p class="text-xs">
                    {{ item.location }}
                  </p>
                </div>
                <p v-if="item.endDate !== 'active'" class="text-sm">
                  {{ item.startDate }} - {{ item.endDate }}
                </p>
                <p v-else class="text-xs">
                  {{ item.startDate }} -
                  <span>{{ "Currently working here" }}</span>
                </p>
              </div>
              <div class="pt-3">
                <p class="font-bold text-sm">Description</p>
                <div
                  v-for="(x, i) in item.description"
                  :key="i"
                  class="flex items-center py-1 ml-3"
                >
                  <div class=" text-green-600">
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
                  <span class="pl-2 text-sm">{{ x }}</span>
                </div>
              </div>
            </div>
          </div>
        </section>
      </div>
    </div>
  </div>
</template>

<script setup>
const experiences = [
  {
    location: "Addis Ababa, Ethiopia",
    title: "Teacher Development Program Coordinator",
    company: "Oromia Education Bureau",
    startDate: "February 2010",
    endDate: "Present",
    description: [
      `Led and coordinated teacher and school director training across the Oromia region.`,
      `Collaborated with staff and the Read II project (USAID) for monitoring and reporting compliance.`,
      `Managed data collection, tracking of indicators, and ensured M&E systems' functionality.`,
      `Oversaw partners' reporting of monitoring data for timely submission and consolidation.`,
      `Identified and reported changes to indicators, milestones, and targets.`,
      `Facilitated sharing of learning opportunities to enhance teacher and school leader performance.`,
      `Conducted routine monitoring visits to ensure high-quality implementation.`,
    ],
  },
  {
   
    location: "Asella, Arsi, Oromia, Ethiopia",
    title: "Teacher Development Expert",
    company: "Arsi Zone Education Office",
    startDate: "September 2009",
    endDate: "February 2010",
    description: [
     `Managed and coordinated training in 26 Woredas.`,
     `Designed, collected, and analyzed survey data, disseminating quality reports.`,
     `Conducted project monitoring visits and provided technical support.`,
     `Provided capacity-building training for staff, identified skill gaps, and conducted quality benchmarking.`,
     `Supported Woreda teams through orientations, training, and coaching.`,
     `Conducted routine monitoring visits to ensure effective M&E implementation.`
    ],
  },
  {

    location: "Arsi, Oromia, Ethiopia",
    title: "School Director",
    company: "",
    startDate: "2002",
    endDate: "2008 EC",
    description: [
     `Lead overall school system in teaching learning process`,
     `Lead the design and implementation of M&E performance plan, log frames and tools for ongoing monitoring , and learning activities.`,
     `Develop and oversee the implementation of program-wide mechanisms to measure, analyze, and report progress against set indicators.`,
     `With inclusive participations of staff I prepare strategic and school improvement plan`,
     `Managed, organized, facilitated and provided MEAL training for staff at all level`,
     `Ensured data quality and the quality of Weekly, monthly, quarterly & annual reports`,
     `Designed survey questionnaires, collecting data, analyzing and disseminating quality reports,`,
     `Conducted monitoring visit and providing technical support for staff where needed, conducted different project learning including success stories and lessons and researches`,
     `Identified staff skill gaps and provided capacity building trainings & supported staff`,
     `Provided on-going feedback on the Performance Management Plan and database management, to enhance measuring the impact of the program against objectives and indicators`,
     `Conducted lesson learnt and success stories of project for future improvements`
    ],
  },

  {

    location: "Addis Ababa, Ethiopia",
    title: "Teacher",
    company: "",
    startDate: "1997",
    endDate: "2001 EC",
    description: [
     `Managed teaching and learning activities in the classroom and school`,
     `Monitored student development and reported to school directors`,
     `Mentored newly deployed teachers, supported data management and analysis`,
     `Delivered multiple trainings, including qualitative data collection and gender mainstreaming`
    ],
  },

];
</script>
