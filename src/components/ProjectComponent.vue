<script setup lang="ts">
import {ref} from 'vue'

interface Project {
  img: string
  alt: string
  title: string
  content: string
  link: string
}

const projects = ref<Project[]>([
  {
    img: "/src/assets/images/HandSign.png",
    alt: "hand_sign",
    title: "Hand Sign Language Recognition",
    content: "is a real-time hand sign language recognition for deaf person.",
    link: "https://github.com/Manichann/Hand-Sign-Language-Recognition"
  },
  {
    img: "/src/assets/images/pandaGame2.png",
    alt: "panda",
    title: "Panda Climbing Bamboo",
    content: "panda game is to avoid panda from hitting the obstacles.",
    link: "https://github.com/AOI-SK/Panda-climbing-bamboo-game"
  },
  {
    img: "/src/assets/images/tulip-background.jpg",
    alt: "flower shop",
    title: "Flower-Shop Website",
    content: "is a online flower delivery service for any occasion.",
    link: "https://github.com/Manichann/Flower-Shop"
  },
])
</script>

<template>
  <div id="project" class="bg-white px-10 sm:px-14 py-10">
    <h1 class="text-[#749BC2] text-xl min-[390px]:text-2xl sm:text-4xl lg:text-5xl font-bold text-center py-4 lg:py-10">Projects</h1>
    <div class="flex flex-col items-center">
      <div class="card w-60 min-[390px]:w-72 md:w-[38rem] lg:w-[50rem] md:card-side bg-white shadow-xl my-10" v-for="(project,idx) in projects" :key="idx">
        <figure>
          <img :src="`${project.img}`" :alt="project.alt" class="w-[15rem] h-[12rem] min-[390px]:w-[18rem] min-[390px]:h-[15rem] sm:w-[18rem] sm:h-[16rem] lg:w-[20rem] lg:h-[18rem]" />
        </figure>
        <div class="card-body p-5">
          <h2 class="card-title text-[#749BC2] text-sm min-[390px]:text-base sm:text-lg lg:text-2xl font-bold">{{project.title}}</h2>
          <p class="text-[#749BC2] text-xs min-[390px]:text-sm sm:text-base lg:text-lg mb-4">{{project.content}}</p>
          <div class="card-actions justify-end">
            <a
              :href="`${project.link}`"
              target="_blank"
              class="btn btn-sm sm:btn-sm lg:btn-md w-28 rounded-3xl border-none bg-[#F4D160] text-white text-[8px] min-[390px]:text-[10px] sm:text-xs lg:text-sm"
              >View</a
            >
          </div>
        </div>
      </div>
      <a
        href="https://github.com/Manichann?tab=repositories"
        target="_blank"
        class="btn btn-ghost text-[#F4D160] text-[8px] min-[390px]:text-[10px] sm:text-xs lg:text-sm font-bold mt-0 md:mt-10"
        >View More</a
      >
    </div>
  </div>
</template>
