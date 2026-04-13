<script setup>
import { ref } from 'vue';
import Header from './components/Header.vue';
import PortfolioHero from './components/PortfolioHero.vue';
import AssetTable from './components/AssetTable.vue';
import WalletModal from './components/WalletModal.vue';

const isWalletModalOpen = ref(false);

const openWalletModal = () => {
  isWalletModalOpen.value = true;
};

const closeWalletModal = () => {
  isWalletModalOpen.value = false;
};
</script>

<template>
  <div class="flex flex-col min-h-screen">
    <Header @connect="openWalletModal" />
    <main class="flex-1 pb-16">
      <div class="max-w-[1200px] mx-auto px-6 w-full">
        <PortfolioHero @connect="openWalletModal" />
        <AssetTable />
      </div>
    </main>
    <footer class="py-8 md:py-10 border-t border-border-hover text-text-muted text-sm">
      <div class="max-w-[1200px] mx-auto px-6 w-full flex flex-col md:flex-row justify-between items-center gap-4 md:gap-0">
        <div class="flex gap-4 md:gap-6">
          <a href="#" class="hover:text-text-secondary transition-colors duration-200">Support</a>
          <a href="#" class="hover:text-text-secondary transition-colors duration-200">Terms of Service</a>
          <a href="#" class="hover:text-text-secondary transition-colors duration-200">Privacy Policy</a>
        </div>
        <div class="text-center md:text-left">
          &copy; 2026 Leap Wallet. All rights reserved.
        </div>
      </div>
    </footer>

    <WalletModal :isOpen="isWalletModalOpen" @close="closeWalletModal" />
  </div>
</template>

<style scoped>
/* Scoped styles removed as they are now handled by Tailwind classes */
</style>
