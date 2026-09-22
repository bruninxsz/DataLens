<script setup>
// Definimos as propriedades (props) que o card vai receber para ser dinâmico
defineProps({
  titulo: {
    type: String,
    required: true
  },
  valor: {
    type: [String, Number],
    required: true
  },
  variacao: {
    type: String,
    default: ''
  },
  tipoVariacao: {
    type: String, // 'positivo' ou 'negativo'
    default: 'positivo'
  }
})
</script>

<template>
  <div class="bg-white dark:bg-slate-800 p-6 rounded-xl shadow-sm border border-slate-100 dark:border-slate-700 flex flex-col justify-between">
    <!-- Cabeçalho do Card -->
    <div class="flex items-center justify-between">
      <span class="text-sm font-medium text-slate-500 dark:text-slate-400">{{ titulo }}</span>
      <!-- Slot caso queira passar um ícone dinamicamente depois -->
      <slot name="icone"></slot>
    </div>

    <!-- Valor Principal -->
    <div class="mt-4 flex items-baseline justify-between">
      <h3 class="text-2xl font-bold text-slate-800 dark:text-white">{{ valor }}</h3>
      
      <!-- Tag opcional de variação (ex: +12% em relação ao mês passado) -->
      <span 
        v-if="variacao" 
        :class="[
          'text-xs font-semibold px-2 py-0.5 rounded-full',
          tipoVariacao === 'positivo' 
            ? 'bg-emerald-50 text-emerald-600 dark:bg-emerald-950/50 dark:text-emerald-400' 
            : 'bg-rose-50 text-rose-600 dark:bg-rose-950/50 dark:text-rose-400'
        ]"
      >
        {{ variacao }}
      </span>
    </div>
  </div>
</template>