<script setup lang="ts">
import { ref } from 'vue'

interface MenuList {
  id: string
  menu: string
}

const menus = ref<MenuList[]>([
  {
    id: 'home',
    menu: 'Home'
  },
  {
    id: 'about',
    menu: 'About'
  },
  {
    id: 'project',
    menu: 'Project'
  },
  {
    id: 'contact',
    menu: 'Contact'
  }
])
</script>

<template>
  <div class="bg-[#749BC2] flex items-center justify-between h-10 sm:h-14 lg:h-16 px-10 shadow-xl">
    <div>
      <a href="#home" class="text-white text-xs min-[390px]:text-sm lg:text-xl font-bold"
        >MANICHANH</a
      >
    </div>
      <div class="dropdown dropdown-end sm:hidden">
        <label tabindex="0" class="btn btn-ghost">
          <img
            src="https://img.icons8.com/FFFFFF/m_rounded/2x/menu.png"
            alt="menu"
            class="w-5 h-5"
          />
        </label>
        <div class="dropdown-content menu rounded-box shadow bg-[#749BC2] w-32 z-[1] p-2">
          <ul>
            <li v-for="(menu, idx) in menus" :key="idx" tabindex="0">
              <a
                :href="`#${menu.id}`"
                class="text-white text-xs font-semibold hover:text-[#F4D160]"
                >{{ menu.menu }}</a
              >
            </li>
          </ul>
        </div>
      </div>
      <div class="hidden sm:flex">
        <ul class="menu menu-horizontal pl-5 lg:pl-14">
          <li v-for="(menu, idx) in menus" :key="idx">
            <a
              :href="`#${menu.id}`"
              class="text-white text-sm lg:text-lg font-semibold hover:text-[#F4D160]"
              >{{ menu.menu }}</a
            >
          </li>
        </ul>
      </div>
  </div>
</template>