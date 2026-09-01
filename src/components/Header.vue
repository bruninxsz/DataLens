<template>
  <header class="flex justify-between bg-slate-900 p-4 md:p-6 lg:p-8 text-zinc-500 min-w-screen border-b-1 border-white">
    <nav class ="flex flex-wrap justify-center items-center gap-3 lg:gap-8 font-bold text-sm lg:text-lg">
      <img src="../assets/logo.svg" class="w-25 md:w-35 lg:w-40 hover:scale-[1.05] duration-300">
      <a v-if="dispositivo === 'Desktop'" href="" class="hover:scale-[1.05] hover:text-zinc-300 duration-300">Features</a>
      <a v-if="dispositivo === 'Desktop'" href="" class="hover:scale-[1.05] hover:text-zinc-300 duration-300">Solutions</a>
      <a v-if="dispositivo === 'Desktop'" href="" class="hover:scale-[1.05] hover:text-zinc-300 duration-300">Team</a>
      <a v-if="dispositivo === 'Desktop'" href="" class="hover:scale-[1.05] hover:text-zinc-300 duration-300">Pricing</a>
    </nav>
    <div class="flex flex-wrap gap-4 md:gap-8 lg:gap-12 items-center">
      <router-link to="/" class="font-bold text-sm lg:text-lg hover:scale-[1.05] hover:text-zinc-300 duration-300" >Sign in</router-link>
      <router-link to="/" class="py-2 px-2 lg:py-3 lg:px-4 bg-white text-slate-900 text-xs md:text-sm lg:text-md font-semibold rounded-lg hover:shadow-sm shadow-slate-200 duration-300">Get started!</router-link>
    </div>
  </header>

</template> 

<script setup>
import { ref, onMounted } from 'vue'

const dispositivo = ref('')

function tamanhotela(){
  const largura = window.innerWidth;

  if(largura <= 768){
    dispositivo.value = 'Mobile'
  } else if (768 < largura && largura <= 1024){
    dispositivo.value = 'Tablet'
  } else {
    dispositivo.value = 'Desktop'
  }
}

onMounted(() => {
  tamanhotela()
})

</script>