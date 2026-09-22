<template>
  <Header />

  <main class="min-h-screen bg-slate-950 flex flex-col gap-16 md:gap-24 lg:gap-32 pb-20">

    <!-- Seção Hero (Apresentação Principal) -->
    <section
      class="relative flex flex-col mx-auto mt-16 md:mt-24 lg:mt-32 items-center gap-8 px-4"
    >
      <!-- Brilho azul atrás do texto -->
      <div
        class="absolute -z-0 w-96 h-36 bg-sky-100/20 rounded-full blur-3xl"
      ></div>

      <h1 class="relative z-10 text-white font-bold text-2xl md:text-4xl lg:text-6xl text-center">
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

      <div class="rounded-2xl overflow-hidden shadow-2xl border border-zinc-800">
        <img src="../assets/dashboard.png" class="max-w-4xl w-full">
      </div>
    </section>

    <!-- Nova Seção: Cards Indicadores Reutilizáveis -->
    <section class="max-w-7xl mx-auto w-full px-4 md:px-8">
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
        <CardIndicador 
          titulo="Dados Processados" 
          valor="1.482.000" 
          variacao="+18.2%" 
          tipo-variacao="positivo" 
        />
        <CardIndicador 
          titulo="Taxa de Precisão" 
          valor="99.4%" 
          variacao="+0.5%" 
          tipo-variacao="positivo" 
        />
        <CardIndicador 
          titulo="Anomalias Detectadas" 
          valor="12" 
          variacao="-3.1%" 
          tipo-variacao="negativo" 
        />
        <CardIndicador 
          titulo="Empresas Mapeadas" 
          valor="8.540" 
          variacao="+12.4%" 
          tipo-variacao="positivo" 
        />
      </div>
    </section>

  </main>
</template>

<script setup>
import Header from '../components/Header.vue'
import CardIndicador from '../components/CardIndicador.vue' // Importando o seu card
</script>