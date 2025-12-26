<template>
  <div class="document-template">
    <!-- 标题组件 -->
    <DocumentTitle
        :align="titleAlign"
        :show-divider="showTitleDivider"
    >
      <!-- 使用具名插槽 -->
      <template #title>
        <h1>{{ title }}</h1>
      </template>

      <template #subtitle v-if="subtitle">
        <h2>{{ subtitle }}</h2>
      </template>

      <template #meta v-if="meta">
        <div class="document-meta">
          {{ meta }}
        </div>
      </template>
    </DocumentTitle>

    <!-- 正文组件 -->
    <DocumentBody
        :padding="bodyPadding"
        :line-height="lineHeight"
        :font-size="fontSize"
    >
      <!-- 主要内容插槽，父组件可以传入HTML -->
      <template #content>
        <!-- 使用v-html渲染HTML内容 -->
        <div v-html="content"></div>
      </template>

      <!-- 附加内容插槽 -->
      <template #additional>
        <slot name="additional"></slot>
      </template>
    </DocumentBody>
    <Foot />
  </div>
</template>

<script setup>
import { defineProps } from 'vue';
import DocumentTitle from "@/components/title.vue";
import DocumentBody from "@/components/body.vue";
import Foot from "@/components/foot.vue"; // 修正导入路径

// 定义组件属性
const props = defineProps({
  // 标题相关
  title: {
    type: String,
    default: '文档标题'
  },
  subtitle: {
    type: String,
    default: ''
  },
  meta: {
    type: String,
    default: ''
  },
  titleAlign: {
    type: String,
    default: 'center'
  },
  showTitleDivider: {
    type: Boolean,
    default: true
  },

  // 正文相关
  content: {
    type: String,
    default: '<p>请提供文档内容</p>'
  },
  bodyPadding: {
    type: Boolean,
    default: true
  },
  lineHeight: {
    type: String,
    default: '1.8'
  },
  fontSize: {
    type: String,
    default: '16px'
  }
});
</script>

<style scoped>
.document-template {
  margin: 0 auto;
  padding: 20px;
}

.document-meta {
  color: #666;
  font-size: 14px;
  margin-top: 10px;
  font-style: italic;
}

@media (max-width: 768px) {
  .document-template {
    padding: 10px;
  }
}
</style>
