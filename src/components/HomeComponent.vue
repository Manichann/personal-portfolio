<script setup lang="ts">
import {ref} from 'vue'

interface SocialList {
  img: string
  alt: string
  link: string
}

const socials = ref<SocialList[]>([
  {
    img: "https://img.icons8.com/FFFFFF/m_rounded/2x/facebook-new.png",
    alt: "facebook",
    link: "https://www.facebook.com/manichanh.siboribane/"
  },
  {
    img: "https://img.icons8.com/FFFFFF/m_outlined/2x/whatsapp.png",
    alt: "whatsapp",
    link: "https://api.whatsapp.com/qr/4OZ2TRQX7YX7N1?autoload=1&app_absent=0"
  },
  {
    img: "https://img.icons8.com/FFFFFF/m_outlined/2x/instagram-new.png",
    alt: "instagram",
    link: "https://www.instagram.com/tanoy__pisces/"
  },
  {
    img: "https://img.icons8.com/FFFFFF/m_outlined/2x/github.png",
    alt: "github",
    link: "https://github.com/Manichann"
  }
])
</script>

<template>
  <div id="home" class="bg-[#749BC2] flex flex-col items-center gap-8 min-[390px]:gap-10 sm:gap-14 lg:gap-16 p-10 min-[390px]:p-14 sm:p-20 lg:p-28">
    <img
      src="https://i.pinimg.com/564x/53/83/c5/5383c54aa6dfb8cf3597e8c5731d05e0.jpg"
      alt="profile"
      class="w-20 h-20 min-[390px]:w-28 min-[390px]:h-28 sm:w-32 sm:h-32 lg:w-40 lg:h-40 rounded-full"
    />
    <h1 class="text-white font-extrabold text-center text-xl min-[390px]:text-[26px] sm:text-[40px] lg:text-5xl">Manichanh Siboribane</h1>
    <ul class="flex">
      <li class="mx-2 sm:mx-5" v-for="(social,idx) in socials" :key="idx">
        <a :href="`#${social.link}`">
          <img :src="social.img" :alt="social.alt" class="w-5 h-5 min-[390px]:w-6 min-[390px]:h-6 sm:w-8 sm:h-8 lg:w-9 lg:h-9"/>
        </a>
      </li>
    </ul>
    <a href="#about" class="btn btn-sm sm:btn-md w-28 rounded-3xl border-none bg-[#F4D160] text-white text-[8px] min-[390px]:text-[10px] sm:text-xs lg:text-sm ">About me</a>
  </div>
</template>
