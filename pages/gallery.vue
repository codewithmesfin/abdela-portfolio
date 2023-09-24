<template>
  <div class="h-full">
    <Head>
      <Title>Abdella Ahmed </Title>
      <Meta
        name="description"
        content="Teacher Development Program Coordinator at Oromia Education Bureau"
      />
    </Head>
    <div
      class="mx-auto md:max-w-[90%] h-full w-[100%] px-2 py-10 sm:px-6 lg:px-8"
    >
      <section class="w-full h-full p-2 md:px-10">
        <h1 class="text-4xl md:text-4xl text-center font-bold my-10">Gallery</h1>
        <div class="grid grid-cols-2 md:grid-cols-4 gap-4 pt-16 items-center">
          <div
            v-for="(item, i) in pictures"
            :key="i"
            class="bg-gray-400"
          >
        
              <img :src="item" alt="" class="rounded h-fill w-full max-w-[300px] max-h-[300px] object-contain" />
          
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script setup>
import i1 from "~/assets/pics/i1.jpeg";
import i2 from "~/assets/pics/i2.jpeg";
import i3 from "~/assets/pics/i3.jpeg";
import i4 from "~/assets/pics/i4.jpeg";
import i5 from "~/assets/pics/i5.jpeg";
import i6 from "~/assets/pics/i6.jpeg";

import i7 from "~/assets/pics/i7.jpeg";
import i8 from "~/assets/pics/i8.jpeg";
import i9 from "~/assets/pics/i9.jpeg";
import i10 from "~/assets/pics/i10.jpeg";
import i11 from "~/assets/pics/i11.jpeg";
import i12 from "~/assets/pics/i12.jpeg";

import i13 from "~/assets/pics/i13.jpeg";
import i14 from "~/assets/pics/i14.jpeg";

const pictures = [i6,i1, i2,i3,i4,i5,
i7,i8,i9,i10,i11,i12,i13,i14
];
</script>
