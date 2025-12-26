<template>
  <div
      class="document-body"
      :class="{ 'with-padding': padding }"
      :style="bodyStyle"
  >
    <!-- 主要内容插槽 -->
    <slot name="content">
      <!-- 默认内容 -->
      <p>请插入文档内容</p>
    </slot>

    <!-- 附加内容插槽（如图片、表格等） -->
    <slot name="additional"></slot>
  </div>
</template>

<script setup>
import { computed } from 'vue';

// 定义组件属性
const props = defineProps({
  padding: {
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

// 计算样式
const bodyStyle = computed(() => {
  return {
    '--line-height': props.lineHeight,
    '--font-size': props.fontSize
  };
});
</script>

<style scoped>
.document-body {
  font-family: "Microsoft YaHei", "SimHei", sans-serif;
  color: #333;
  line-height: var(--line-height, 1.8);
  font-size: var(--font-size, 16px);
}

.document-body.with-padding {
  padding: 20px;
  background-color: #ffffff;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
}

/* 嵌套样式 - 这些样式会作用于插槽内的内容 */
.document-body :deep(h1) {
  color: #1a5f7a;
  font-size: 28px;
  font-weight: 700;
  margin: 30px 0 20px;
  padding-bottom: 10px;
  border-bottom: 2px solid #1a5f7a;
  text-align: center;
}

.document-body :deep(h2) {
  color: #2a8fb8;
  font-size: 24px;
  font-weight: 600;
  margin: 25px 0 15px;
  padding-left: 10px;
  border-left: 4px solid #2a8fb8;
}

.document-body :deep(h3) {
  color: #3a9fc7;
  font-size: 20px;
  font-weight: 600;
  margin: 20px 0 12px;
}

.document-body :deep(p) {
  margin: 15px 0;
  text-align: justify;
  text-indent: 2em;
}

.document-body :deep(p:first-of-type) {
  text-indent: 0;
}

.document-body :deep(ul),
.document-body :deep(ol) {
  margin: 15px 0;
  padding-left: 30px;
}

.document-body :deep(li) {
  margin: 8px 0;
  line-height: 1.6;
}

.document-body :deep(strong),
.document-body :deep(b) {
  color: #1a5f7a;
  font-weight: 600;
}

.document-body :deep(.image-container) {
  text-align: center;
  margin: 25px 0;
  padding: 10px;
  background-color: #f8f9fa;
  border-radius: 6px;
  border: 1px solid #e9ecef;
}

.document-body :deep(.image-container img) {
  max-width: 100%;
  height: auto;
  border-radius: 4px;
}

.document-body :deep(table) {
  width: 100%;
  border-collapse: collapse;
  margin: 20px 0;
  font-size: 15px;
}

.document-body :deep(table th) {
  background-color: #f1f8ff;
  color: #1a5f7a;
  font-weight: 600;
  padding: 12px;
  border: 1px solid #dee2e6;
  text-align: center;
}

.document-body :deep(table td) {
  padding: 10px 12px;
  border: 1px solid #dee2e6;
  vertical-align: top;
}

.document-body :deep(table tr:nth-child(even)) {
  background-color: #f8f9fa;
}

.document-body :deep(.highlight) {
  background-color: #fff9c4;
  padding: 2px 4px;
  border-radius: 3px;
  font-weight: 500;
}

.document-body :deep(blockquote) {
  border-left: 4px solid #2a8fb8;
  background-color: #f1f8ff;
  padding: 15px 20px;
  margin: 20px 0;
  font-style: italic;
  border-radius: 0 6px 6px 0;
}

.document-body :deep(a) {
  color: #2a8fb8;
  text-decoration: none;
  border-bottom: 1px solid #2a8fb8;
  transition: all 0.2s;
}

.document-body :deep(a:hover) {
  color: #1a5f7a;
  border-bottom-width: 2px;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .document-body {
    font-size: 15px;
  }

  .document-body :deep(h1) {
    font-size: 24px;
    margin: 25px 0 15px;
  }

  .document-body :deep(h2) {
    font-size: 20px;
    margin: 20px 0 12px;
  }

  .document-body :deep(h3) {
    font-size: 18px;
    margin: 18px 0 10px;
  }

  .document-body.with-padding {
    padding: 15px;
  }
}

/* 打印样式 */
@media print {
  .document-body {
    color: #000;
    line-height: 1.5;
  }

  .document-body.with-padding {
    box-shadow: none;
    padding: 0;
    background-color: transparent;
  }

  .document-body :deep(a) {
    color: #000;
    text-decoration: underline;
    border-bottom: none;
  }

  .document-body :deep(.no-print) {
    display: none;
  }
}
</style>
