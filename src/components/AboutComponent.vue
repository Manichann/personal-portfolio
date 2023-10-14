<script setup lang="ts">
import { ref } from 'vue'

interface Interested {
  img: string
  alt: string
  tip: string
}

const interests = ref<Interested[]>([
  {
    img: 'https://cdn-icons-png.flaticon.com/128/3285/3285977.png',
    alt: 'psychology',
    tip: 'psychology'
  },
  {
    img: 'https://cdn-icons-png.flaticon.com/128/681/681560.png',
    alt: 'design',
    tip: 'design'
  },
  {
    img: 'https://cdn-icons-png.flaticon.com/128/7656/7656431.png',
    alt: 'analysis',
    tip: 'analysis'
  },
  {
    img: 'https://cdn-icons-png.flaticon.com/128/6062/6062646.png',
    alt: 'programing',
    tip: 'programing'
  }
])

interface HobbyList {
  img: string
  alt: string
  tip: string
}

const hobbies = ref<HobbyList[]>([
  {
    img: 'https://cdn-icons-png.flaticon.com/128/567/567829.png',
    alt: 'music',
    tip: 'music'
  },
  {
    img: 'https://cdn-icons-png.flaticon.com/128/167/167755.png',
    alt: 'reading',
    tip: 'reading'
  },
  {
    img: 'https://cdn-icons-png.flaticon.com/128/3184/3184254.png',
    alt: 'crochet',
    tip: 'crochet'
  },
  {
    img: 'https://img.icons8.com/color/2x/netflix.png',
    alt: 'series',
    tip: 'series'
  }
])

interface SkillList {
  img: string
  alt: string
  tip: string
}

const skills = ref<SkillList[]>([
  {
    img: 'https://cdn-icons-png.flaticon.com/128/732/732212.png',
    alt: 'html',
    tip: 'html'
  },
  {
    img: 'https://cdn-icons-png.flaticon.com/128/732/732190.png',
    alt: 'css',
    tip: 'css'
  },
  {
    img: 'https://cdn-icons-png.flaticon.com/128/5968/5968292.png',
    alt: 'javaScript',
    tip: 'javaScript'
  },
  {
    img: 'https://cdn-icons-png.flaticon.com/128/5968/5968381.png',
    alt: 'typeScript',
    tip: 'typeScript'
  },
  {
    img: 'https://img.icons8.com/FFFFFF/color/2x/vue-js.png',
    alt: 'vue',
    tip: 'vue'
  },
  {
    img: 'https://img.icons8.com/FFFFFF/fluent/2x/tailwind_css.png',
    alt: 'tailwind',
    tip: 'tailwind'
  },
  {
    img: 'https://cdn-icons-png.flaticon.com/128/5968/5968350.png',
    alt: 'python',
    tip: 'python'
  },
  {
    img: 'https://cdn-icons-png.flaticon.com/128/6132/6132221.png',
    alt: 'c#',
    tip: 'c#'
  },
  {
    img: 'https://img.icons8.com/FFFFFF/color/2x/microsoft-sql-server.png',
    alt: 'sql server',
    tip: 'sql server'
  }
])

</script>

<template>
  <div id="about" class="bg-white px-10 sm:px-14 py-10">
    <h1 class="text-[#749BC2] font-bold text-center text-lg min-[390px]:text-2xl sm:text-4xl lg:text-5xl py-4 lg:py-10">
      About Me
    </h1>
    <div class="flex flex-col sm:flex-row sm:justify-around items-center">
      <img
        src="https://i.pinimg.com/564x/53/83/c5/5383c54aa6dfb8cf3597e8c5731d05e0.jpg"
        alt="profile"
        class="w-24 h-24 min-[390px]:w-32 min-[390px]:h-32 sm:w-36 sm:h-36 lg:w-48 lg:h-48 rounded-full my-3"
      />
      <div class="card w-60 min-[390px]:w-72 sm:w-80 md:w-96 lg:w-[42rem] px-auto bg-white shadow-xl">
        <div class="grid lg:grid-cols-2 gap-x-0 lg:gap-x-16 p-6">
          <div>
            <p class="text-[#749BC2] text-xs min-[390px]:text-sm sm:text-base lg:text-lg">
              Hi, I’m Manichanh Siboribane, I’m 21 years old, I’m a year 3 computer science student
              at NUOL, and now I’m a internship as front-end developer at HAL Technology.
            </p>
          </div>
          <div class="my-4 lg:my-0">
            <p class="text-[#749BC2] font-semibold text-xs min-[390px]:text-sm sm:text-base lg:text-lg mb-3 lg:mb-0">
              Name: Manichanh Siboribane <br />
              Date of Birth: 28 Feb 2002 <br />
              MBTI: INFJ <br />
              Address: Vangvieng, Vientiane <br />
            </p>
          </div>

          <a
            href="#project"
            class="btn btn-sm sm:btn-md lg:btn-md w-28 rounded-3xl border-none bg-[#F4D160] text-white text-[8px] min-[390px]:text-[10px] sm:text-xs lg:text-sm mx-auto sm:mx-0 my-0 lg:my-5"
            >Project</a
          >
        </div>
      </div>
    </div>
    <div class="mt-10 md:mt-36 gap-x-0 md:gap-x-12 lg:gap-x-24 flex flex-col md:flex-row justify-center items-center md:items-start">
      <div class="my-3 lg:my-5">
        <p class="text-[#749BC2] text-base min-[390px]:text-lg md:text-xl lg:text-2xl font-bold text-center py-5">My interested</p>
        <div class="card bg-white shadow-xl gap-10 lg:gap-14 p-8 lg:p-10 grid grid-cols-2">
          <div
            class="tooltip flex justify-center"
            :data-tip="interest.tip"
            v-for="(interest, idx) in interests"
            :key="idx"
          >
            <img :src="interest.img" :alt="interest.alt" class="w-9 h-9 min-[390px]:w-10 min-[390px]:h-10 md:w-11 md:h-11 lg:w-12 lg:h-12" />
          </div>
        </div>
      </div>
      <div class="my-3 lg:my-5">
        <p class="text-[#749BC2] text-base min-[390px]:text-lg md:text-xl lg:text-2xl font-bold text-center py-5">My hobby</p>
        <div class="card bg-white shadow-xl gap-10 lg:gap-14 p-8 lg:p-10 grid grid-cols-2">
          <div
            class="tooltip flex justify-center"
            :data-tip="hobby.tip"
            v-for="(hobby, idx) in hobbies"
            :key="idx"
          >
            <img :src="hobby.img" :alt="hobby.alt" class="w-9 h-9 min-[390px]:w-10 min-[390px]:h-10 md:w-11 md:h-11 lg:w-12 lg:h-12" />
          </div>
        </div>
      </div>
      <div class="my-3 lg:my-5">
        <p class="text-[#749BC2] text-base min-[390px]:text-lg md:text-xl lg:text-2xl font-bold text-center py-5">My skill</p>
        <div class="card h-[12rem] lg:h-[15rem]  overflow-y-auto bg-white shadow-xl gap-10 lg:gap-14 p-8 lg:p-10 grid grid-cols-2">
          <div
            class="tooltip flex justify-center"
            :data-tip="skill.tip"
            v-for="(skill, idx) in skills"
            :key="idx"
          >
            <img :src="skill.img" :alt="skill.alt" class="w-9 h-9 min-[390px]:w-10 min-[390px]:h-10 md:w-11 md:h-11 lg:w-12 lg:h-12" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
