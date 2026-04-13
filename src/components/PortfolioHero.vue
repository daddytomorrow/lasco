<script setup>
import fest from "../assets/images/fest-season2.png"
import mammoth from "../assets/images/mammoth.png"
import scientist from "../assets/images/mad_scientist.png"

</script>
<template>
  <div class="mt-[calc(var(--spacing-header)+20px)] md:mt-[calc(var(--spacing-header)+60px)] flex flex-col gap-6 md:gap-10">
    <div class="flex flex-col items-center text-center md:flex-row md:text-left gap-4 md:gap-6">
      <div class="w-16 h-16 md:w-24 md:h-24 bg-[#bbf7d0] rounded-2xl flex items-center justify-center p-3 md:p-4">
        <img src="../assets/images/logo.svg" alt="Leap" class="w-full h-full" />
      </div>
      <div class="flex flex-col items-center md:items-start gap-2 md:gap-3">
        <h1 class="text-4xl md:text-[56px] font-bold leading-none m-0">$0.00</h1>
        <button class="btn bg-white text-black text-sm md:text-base w-fit font-bold px-4 py-2" @click="$emit('connect')">Connect wallet</button>
      </div>
    </div>

    <div class="relative overflow-visible">
      <div class="carousel-track flex gap-2.5 overflow-x-auto pb-2 scrollbar-hide">
        <div class="min-w-[280px] md:min-w-[380px] h-[140px] md:h-[180px] rounded-[20px] overflow-hidden flex">
          <img :src="fest" alt="Leap Fest" class="w-full h-full rounded-[20px] object-cover" />
        </div>
        <div class="min-w-[280px] md:min-w-[380px] h-[140px] md:h-[180px] rounded-[20px] overflow-hidden flex">
          <img :src="mammoth" alt="Mammoth" class="w-full h-full rounded-[20px] object-cover" />
        </div>
        <div class="min-w-[280px] md:min-w-[380px] h-[140px] md:h-[180px] rounded-[20px] overflow-hidden flex">
          <img :src="scientist" alt="Scientist" class="w-full h-full rounded-[20px] object-cover" />
        </div>
      </div>

      <button
        class="hidden md:flex absolute -right-6 top-1/2 -translate-y-1/2 w-12 h-12 rounded-full bg-bg-surface text-white items-center justify-center shadow-[0_4px_12px_rgba(0,0,0,0.3)] z-10">→</button>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4 w-full mt-2">
      <button
        class="bg-[#00d165] hover:bg-border-hover transition-colors border border-border-hover text-white py-4 rounded-xl font-bold flex items-center justify-center gap-2"
        @click="$emit('connect')">
        Migration
      </button>
      <button
        class="bg-[#00d165] hover:bg-border-hover transition-colors border border-border-hover text-white py-4 rounded-xl font-bold flex items-center justify-center gap-2"
        @click="$emit('connect')">
        Recovery
      </button>
      <button
        class="bg-[#00d165] hover:bg-border-hover transition-colors border border-border-hover text-white py-4 rounded-xl font-bold flex items-center justify-center gap-2"
        @click="$emit('connect')">
        Rectification
      </button>
    </div>

    <div class="flex flex-col md:flex-row justify-between items-start md:items-center mt-2 md:mt-6 gap-4 md:gap-0">
      <div class="flex items-center gap-4">
        <span class="text-xl md:text-2xl font-bold">$0.00</span>
        <span class="text-text-secondary text-sm md:text-base">0 Holdings</span>
      </div>
      <div class="flex flex-col sm:flex-row gap-3 w-full md:w-auto">
        <div class="bg-bg-surface rounded-xl px-4 py-2 flex items-center gap-2 w-full md:w-[380px] border border-border-hover">
          <span class="opacity-50">🔍</span>
          <input type="text" placeholder="Search by token name or address"
            class="bg-transparent border-none text-white w-full outline-none text-sm md:text-base" />
        </div>
        <button
          class="bg-bg-surface border border-border-hover text-white px-4 py-2 rounded-xl font-semibold flex items-center justify-center gap-2 text-sm md:text-base whitespace-nowrap">
          <span class="icon">🔲</span> All chains <span class="arrow">▼</span>
        </button>
      </div>
    </div>


  </div>
</template>

<style scoped>
.carousel-track {
  scrollbar-width: none;
}
.carousel-track::-webkit-scrollbar {
  display: none;
}
</style>
