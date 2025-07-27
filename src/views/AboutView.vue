<script setup lang="ts">
import MilkdownEditorWrapper from '../components/MilkdownEditorWrapper.vue'
</script>

<template>
  <div class="about-page">
    <div class="page-header">
      <div class="header-content">
        <h1>关于</h1>
        <p class="header-subtitle">了解 CheeseDown 应用程序</p>
      </div>
    </div>
    <div class="content">
      <div class="card">
        <p>这是一个使用 Vue 3 + Tauri 构建的桌面应用程序，集成了 Milkdown 富文本编辑器。</p>

        <h2>功能特点</h2>
        <ul>
          <li>现代化的富文本编辑体验</li>
          <li>支持 Markdown 语法</li>
          <li>桌面应用程序，可离线使用</li>
          <li>响应式设计，适配不同屏幕尺寸</li>
        </ul>

        <h2>技术栈</h2>
        <ul>
          <li>Vue 3 Composition API</li>
          <li>Tauri 桌面应用框架</li>
          <li>Milkdown 富文本编辑器</li>
          <li>TypeScript</li>
          <li>Vite 构建工具</li>
        </ul>
      </div>

      <div class="card">
        <h2>试用编辑器</h2>
        <p>下面是一个 Milkdown 编辑器实例，您可以在这里试用编辑功能：</p>
        <div class="editor-wrapper">
          <MilkdownEditorWrapper />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.about-page {
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

.content {
  flex: 1;
  padding: 20px 30px;
  overflow: auto;
  background-color: var(--color-background);
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.card {
  background-color: var(--color-background-soft);
  border-radius: 8px;
  padding: 25px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
  border: 1px solid var(--color-border);
}

.card h2 {
  margin-top: 0;
  color: var(--color-heading);
  border-bottom: 1px solid var(--color-border);
  padding-bottom: 10px;
}

.content ul {
  padding-left: 20px;
}

.content li {
  margin-bottom: 10px;
}

.editor-wrapper {
  margin-top: 20px;
  border-radius: 8px;
  overflow: hidden;
}
</style>
