<template>
  <header class="flex justify-between bg-slate-900 p-4 md:p-6 lg:p-8 text-zinc-500 min-w-screen">
    <nav v-if="dipositivo='Desktop'" class ="flex flex-wrap justify-center items-center gap-3 lg:gap-8 font-bold text-sm lg:text-lg">
      <img src="../assets/logo.svg" class="w-20 md:w-30 lg:w-40 hover:scale-[1.05] duration-300">
      <a href="" class="hover:scale-[1.05] hover:text-zinc-300 duration-300">Features</a>
      <a href="" class="hover:scale-[1.05] hover:text-zinc-300 duration-300">Solutions</a>
      <a href="" class="hover:scale-[1.05] hover:text-zinc-300 duration-300">Team</a>
      <a href="" class="hover:scale-[1.05] hover:text-zinc-300 duration-300">Pricing</a>
    </nav>
    <div class="grid grid-cols-2 items-center">
      <router-link to="/" class="font-bold text-sm lg:text-lg hover:scale-[1.05] hover:text-zinc-300 duration-300" >Sign in</router-link>
      <router-link to="/" class="py-2 px-2 lg:py-3 lg:px-4 bg-white text-slate-900 text-sm lg:text-md font-semibold rounded-lg hover:shadow-sm shadow-slate-200 duration-300">Get started!</router-link>
    </div>
  </header>

</template>

<script setup>
import { ref, onMounted } from 'vue'

const dispositivo = ref('')

function tamanhotela(){
  const largura = window.innerWidth;

  if(largura <= 768){
    const dispositvo = 'Mobile'
  } else if (768 < largura >= 1024){
    const dispositivo = 'Tablet'
  } else {
    dispositivo = 'Desktop'
  }
}
</script>