<template>
  <div v-if="statistics" class="flex gap-8">
    <div class="px-4 py-3 bg-bg-light rounded-lg min-w-[13em]">
      <h2 class="inline-block">{{ statistics.airdropped }}</h2>
      <span class="text-body ml-1">/{{ statistics.total || '?' }}</span>
      <p class="text-white">airdropped/available NFTs</p>
    </div>
    <div class="px-4 py-3 bg-bg-light rounded-lg min-w-[13em]">
      <h2>{{ statistics.unconfirmed }}</h2>
      unconfirmed
    </div>
    <div class="px-4 py-3 bg-bg-light rounded-lg min-w-[13em]">
      <h2>{{ statistics.pending }}</h2>
      pending
    </div>
    <div class="px-4 py-3 bg-bg-light rounded-lg min-w-[13em]">
      <h2>{{ statistics.threwError }}</h2>
      errors
    </div>
  </div>
</template>

<script lang="ts" setup>
import type { PropType } from 'vue';

defineProps({
  statistics: { type: Object as PropType<StatisticsInterface>, default: null },
});
</script>
