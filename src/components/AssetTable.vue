<template>
    <div class="mt-4">
        <div class="w-full">
            <div
                class="grid grid-cols-[2fr_1fr] md:grid-cols-[2fr_1fr_1fr] py-3 text-text-secondary text-xs font-medium border-b border-border-hover pb-3">
                <div>Token</div>
                <div class="text-right hidden md:block">Price</div>
                <div class="text-right">Balance</div>
            </div>

            <div class="table-body">
                <div class="py-[60px] text-center text-text-secondary" v-if="assets.length === 0">
                    <p>No holdings found. Connect your wallet to see your assets.</p>
                </div>
                <div v-for="asset in assets" :key="asset.name"
                    class="grid grid-cols-[2fr_1fr] md:grid-cols-[2fr_1fr_1fr] py-4 border-b border-border-hover items-center">
                    <div class="flex items-center gap-3 min-w-0">
                        <div class="w-8 h-8 rounded-full flex items-center justify-center font-bold text-sm shrink-0"
                            :style="{ backgroundColor: asset.color }">
                            {{ asset.symbol[0] }}
                        </div>
                        <div class="min-w-0">
                            <div class="font-semibold text-sm md:text-[15px] leading-tight truncate">{{ asset.name }}</div>
                            <div class="flex items-center gap-1 text-text-secondary text-xs">
                                <span>{{ asset.symbol }}</span>
                                <span class="md:hidden">• {{ asset.price }}</span>
                            </div>
                        </div>
                    </div>
                    <div class="text-right hidden md:block">
                        <div class="font-medium text-[15px]">{{ asset.price }}</div>
                    </div>
                    <div class="text-right shrink-0">
                        <div class="flex flex-col">
                            <div class="font-semibold text-sm md:text-[15px]">{{ asset.balance }}</div>
                            <div class="text-text-secondary text-xs">{{ asset.value }}</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const assets = [
    { name: 'Cosmos Hub', symbol: 'ATOM', balance: '0', price: '$8.45', value: '$0.00', color: '#2E3148' },
    { name: 'Osmosis', symbol: 'OSMO', balance: '0', price: '$0.85', value: '$0.00', color: '#750BBB' },
    { name: 'Celestia', symbol: 'TIA', balance: '0', price: '$12.20', value: '$0.00', color: '#7B2BF9' }
];
</script>

<style scoped>
/* Scoped styles removed as they are now handled by Tailwind classes */
</style>
