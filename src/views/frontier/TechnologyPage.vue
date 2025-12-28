<template>
  <div style="width: 100%; height: 100vh; margin: 0; padding: 0; overflow: auto;">
    <vue-office-docx
      :src="docxUrl"
      @rendered="renderedHandler"
      @error="errorHandler"
      style="width: 100%; height: 100%;"
    />
  </div>
</template>

<script setup>
import { computed } from 'vue'
import VueOfficeDocx from '@vue-office/docx'
import '@vue-office/docx/lib/index.css'
import { useRoute } from 'vue-router';

const route = useRoute();

const docId = computed(() => {
  return parseInt(route.params.id) || 1;
});

const docxUrl = computed(() => {
  return `/docx/技术装备前沿/${docId.value}.docx`
});
</script>
<style scoped>
</style>