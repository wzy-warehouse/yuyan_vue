<template>
  <div style="width: 100%; margin: 0; padding: 20px; overflow: auto; min-height: 100vh;box-sizing: border-box;background: #f5f7fa">
    <vue-office-docx
      :src="docxUrl"
      @rendered="renderedHandler"
      @error="errorHandler"
      style="width: 100%;"
    />
    <Foot />
  </div>
</template>

<script setup>
import { computed } from "vue";
import VueOfficeDocx from "@vue-office/docx";
import "@vue-office/docx/lib/index.css";
import { useRoute } from "vue-router";
import Foot from "@/components/foot.vue";
const route = useRoute();

const docId = computed(() => {
  return parseInt(route.params.id) || 1;
});

const docxUrl = computed(() => {
  return `/docx/技术装备前沿/${docId.value}.docx`;
});

const errorHandler = (err) => {
  console.error("文档加载失败", err);
};
</script>

<style scoped>
:deep(.docx-wrapper) {
  background: #FFF !important;
  padding: 0 !important;
}
:deep(.docx) {
  width: 98% !important;
  box-shadow: none !important;
}

:deep(.docx-wrapper) {
  overflow: visible !important;
  height: auto !important;   
}

:deep(.docx) {
  height: auto !important;
  min-height: auto !important;
  padding: 20px !important;
}
</style>