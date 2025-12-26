<template>
  <div class="document-title" :class="{ 'no-divider': !showDivider }">
    <!-- 使用插槽接收标题内容 -->
    <slot name="title">
      <!-- 默认插槽内容，当父组件不提供时显示 -->
      <h1>文档标题</h1>
    </slot>

    <!-- 副标题插槽（可选） -->
    <slot name="subtitle"></slot>

    <!-- 元信息插槽（日期、地点等） -->
    <slot name="meta"></slot>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

// 定义组件属性
const props = defineProps({
  align: {
    type: String,
    default: 'center'
  },
  showDivider: {
    type: Boolean,
    default: true
  }
});
</script>

<style scoped>
.document-title {
  text-align: v-bind(align);
  margin-bottom: 30px;
  padding-bottom: 20px;
  position: relative;
}

/* 添加分割线样式 */
.document-title:not(.no-divider)::after {
  content: '';
  display: block;
  position: absolute;
  bottom: 0;
  left: 20%;
  width: 60%;
  height: 2px;
  background: linear-gradient(90deg, transparent, #1a5f7a, transparent);
  opacity: 0.6;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .document-title {
    margin-bottom: 20px;
    padding-bottom: 15px;
  }

  .document-title:not(.no-divider)::after {
    left: 10%;
    width: 80%;
  }
}

/* 打印样式 */
@media print {
  .document-title {
    break-inside: avoid;
    page-break-inside: avoid;
  }
}
</style>
