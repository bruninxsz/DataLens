<template>
  <Header />

  <main class="min-h-screen bg-slate-950 flex flex-col gap-16 md:gap-24 lg:gap-32">

    <section
      id=""
      class="relative flex flex-col mx-auto mt-16 md:mt-24 lg:mt-32 items-center gap-8"
    >

      <!-- Brilho azul atrás do texto -->
      <div
        class="absolute -z-0 w-96 h-36 bg-sky-100/20 rounded-full blur-3xl"
      ></div>

      <h1 class="relative z-10 text-white font-bold text-2xl md:text-4xl lg:text-6xl font-instrument text-center">
        <div>Transforme Dados em</div>

        <div
          class="bg-gradient-to-r from-sky-300 to-sky-700 bg-clip-text text-transparent"
        >
          Inteligência Comercial
        </div>
      </h1>
      <p class="relative z-10 text-zinc-400 max-w-xs md:max-w-lg lg:max-w-2xl text-center text-sm md:text-lg lg:text-xl">
        A plataforma definitiva para limpeza, análise e insights estratégicos de
        dados B2B. Acelere suas vendas com dados precisos.
      </p>
      <div class="rounded-2xl overflow-hidden"><img src="../assets/dashboard.png" class="max-w-xl w-full"></div>
    </section>
  </main>
</template>

<script setup>
import Header from '../components/Header.vue'
</script>