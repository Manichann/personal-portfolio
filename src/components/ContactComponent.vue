<script setup lang="ts">
import {ref} from 'vue'

interface ContactList {
    img: string
    alt: string
    tool: string
    account: string
}

const contacts = ref<ContactList[]>([
    {
        img: "",
        alt: "email",
        tool: "Email Address",
        account: "manichanh2002@gmail.com"
    },
    {
        img: "",
        alt: "phone",
        tool: "Phone",
        account: "+856 20 56430019"
    },
    {
        img: "",
        alt: "address",
        tool: "Address",
        account: "Vangvieng, Vientiane, Laos"
    },
    {
        img: "",
        alt: "",
        tool: "Facebook",
        account: "Manichanh Siboribane"
    },
    {
        img: "",
        alt: "",
        tool: "Whatsapp",
        account: "+856 20 77667426"
    },
    {
        img: "",
        alt: "",
        tool: "Github",
        account: "manichann"
    },
])


</script>

<template>
    <div id="contact" class="bg-white px-10">
        <h2 class="text-[#749BC2] text-lg min-[390px]:text-2xl sm:text-3xl lg:text-5xl font-bold py-4 lg:py-10 flex justify-center">Contact Info</h2>
        <hr class="w-full h-[2px] md:h-1 bg-[#749BC2]">
        <div class="flex justify-center items-center py-8 lg:py-16">
            <ul class="grid grid-cols-2 gap-x-5 min-[390px]:gap-x-8 sm:gap-x-14 lg:gap-x-32">
            <li v-for="(contact, idx) in contacts" :key="idx" class="py-1">
                <h3 class="text-[#749BC2] text-[9px] min-[390px]:text-[10px] sm:text-sm lg:text-lg font-bold">{{ contact.tool }}</h3>
                <p class="text-[#749BC2] text-[9px] min-[390px]:text-[10px] sm:text-sm lg:text-lg pb-2 ">{{ contact.account }}</p>
            </li>
        </ul>
        </div>
        <div class="footer footer-center">
            <p class="text-[#749BC2] text-[7px] min-[390px]:text-[9px] sm:text-xs lg:text-sm py-2">Copyright © 2023 - All right reserved by MANICHANH</p>
        </div>
        
    </div>
</template>

