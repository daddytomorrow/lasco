<template>
  <div class="fixed top-0 left-0 right-0 z-[1000]">
    <header class="h-header bg-bg-primary border-b border-border-color flex items-center">
      <div class="container mx-auto px-6 flex justify-between items-center">
        <div class="flex items-center gap-3">
          <img src="../assets/images/logo.svg" alt="Leap" class="h-8 w-8" />
          <span class="text-xl font-bold tracking-tight">Leap</span>
        </div>

        <nav class="hidden md:flex bg-bg-surface p-1 rounded-full gap-1">
          <a href="#"
            class="px-4 py-2 rounded-full text-sm font-semibold transition-colors duration-200 bg-bg-surface-hover text-text-primary">Portfolio</a>
          <a href="#"
            class="px-4 py-2 rounded-full text-sm font-semibold transition-colors duration-200 text-text-secondary hover:text-text-primary">Staking</a>
          <div class="relative group">
            <a href="#"
              class="px-4 py-2 rounded-full text-sm font-semibold transition-colors duration-200 text-text-secondary hover:text-text-primary flex items-center gap-1.5">Trade
              <span class="text-[10px]">▼</span></a>
          </div>
          <a href="#"
            class="px-4 py-2 rounded-full text-sm font-semibold transition-colors duration-200 text-text-secondary hover:text-text-primary">Rewards</a>
          <a href="#"
            class="px-4 py-2 rounded-full text-sm font-semibold transition-colors duration-200 text-text-secondary hover:text-text-primary flex items-center gap-1.5">Leap
            Fest <span class="bg-accent-secondary text-white text-[10px] px-1.5 py-0.5 rounded font-bold">NEW</span></a>
        </nav>

        <div class="flex items-center gap-4">
          <button class="btn bg-white text-black" @click="$emit('connect')">Connect Wallet</button>
        </div>
      </div>
    </header>
  </div>
</template>

<style scoped>
/* Scoped styles removed as they are now handled by Tailwind classes */
</style>
