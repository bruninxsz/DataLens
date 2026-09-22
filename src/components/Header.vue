<template>
  <header class="flex justify-between items-center bg-slate-950 p-4 md:p-6 lg:p-8 text-zinc-400 w-full border-b border-zinc-800 sticky top-0 z-50">
    <!-- Logo -->
    <div class="flex items-center">
      <img src="../assets/logo.svg" alt="Logo" class="w-24 md:w-32 lg:w-40 hover:scale-[1.05] duration-300">
    </div>

    <!-- Navegação Desktop (Visível apenas em telas grandes) -->
    <nav class="hidden md:flex items-center gap-6 lg:gap-8 font-bold text-sm lg:text-lg">
      <a href="#features" class="hover:scale-[1.05] hover:text-zinc-200 duration-300">Features</a>
      <a href="#solutions" class="hover:scale-[1.05] hover:text-zinc-200 duration-300">Solutions</a>
      <a href="#team" class="hover:scale-[1.05] hover:text-zinc-200 duration-300">Team</a>
      <a href="#pricing" class="hover:scale-[1.05] hover:text-zinc-200 duration-300">Pricing</a>
    </nav>

    <!-- Botões de Ação (Desktop) -->
    <div class="hidden md:flex gap-4 lg:gap-6 items-center">
      <router-link to="/login" class="font-bold text-sm lg:text-lg hover:scale-[1.05] hover:text-zinc-200 duration-300">
        Sign in
      </router-link>
      <router-link to="/get-started" class="py-2 px-3 lg:py-3 lg:px-4 bg-white text-slate-900 text-xs md:text-sm lg:text-base font-semibold rounded-lg hover:shadow-sm shadow-slate-200 duration-300 hover:scale-[1.02]">
        Get started!
      </router-link>
    </div>

    <!-- Botão do Menu Hambúrguer (Visível apenas em telas mobile) -->
    <button @click="toggleMenu" class="md:hidden text-zinc-300 focus:outline-none p-2">
      <svg class="w-7 h-7" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path v-if="!menuAberto" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
        <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
      </svg>
    </button>
  </header>

  <!-- Menu Mobile Suspenso (Abre quando clica no hambúrguer) -->
  <div v-if="menuAberto" class="md:hidden bg-slate-950 border-b border-zinc-800 px-6 py-6 flex flex-col gap-6 text-zinc-300 fixed w-full z-40 shadow-2xl transition-all">
    <nav class="flex flex-col gap-4 font-bold text-base">
      <a href="#features" @click="menuAberto = false" class="hover:text-white duration-200">Features</a>
      <a href="#solutions" @click="menuAberto = false" class="hover:text-white duration-200">Solutions</a>
      <a href="#team" @click="menuAberto = false" class="hover:text-white duration-200">Team</a>
      <a href="#pricing" @click="menuAberto = false" class="hover:text-white duration-200">Pricing</a>
    </nav>
    
    <hr class="border-zinc-800">

    <div class="flex flex-col gap-4">
      <router-link to="/login" @click="menuAberto = false" class="font-bold text-base hover:text-white duration-200">
        Sign in
      </router-link>
      <router-link to="/get-started" @click="menuAberto = false" class="py-3 text-center bg-white text-slate-900 text-sm font-semibold rounded-lg shadow-md duration-300">
        Get started!
      </router-link>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const menuAberto = ref(false)

function toggleMenu() {
  menuAberto.value = !menuAberto.value
}
</script>