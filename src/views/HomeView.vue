<script setup lang="ts">
import MilkdownEditorWrapper from '../components/MilkdownEditorWrapper.vue'
</script>

<template>
  <div class="editor-page">
    <div class="page-header">
      <div class="header-content">
        <h1>文档编辑器</h1>
        <p class="header-subtitle">使用 Milkdown 创建和编辑您的文档</p>
      </div>
    </div>
    <div class="editor-container">
      <MilkdownEditorWrapper />
    </div>
  </div>
</template>

<style scoped>
.editor-page {
  height: 100%;
  display: flex;
  flex-direction: column;
}

.page-header {
  padding: 20px 30px;
  border-bottom: 1px solid var(--color-border);
  background: linear-gradient(to right, var(--color-background-soft), var(--color-background));
}

.header-content h1 {
  margin: 0 0 5px 0;
  color: var(--color-heading);
  font-size: 1.8rem;
}

.header-subtitle {
  margin: 0;
  color: var(--color-text);
  opacity: 0.8;
  font-size: 0.9rem;
}

.editor-container {
  flex: 1;
  padding: 20px 30px;
  overflow: auto;
  background-color: var(--color-background);
}

.editor-container :deep(.milkdown) {
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  overflow: hidden;
}
</style>