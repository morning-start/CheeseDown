<script setup lang="ts">
// 设置界面逻辑可以在这里添加
</script>

<template>
  <div class="settings">
    <div class="page-header">
      <div class="header-content">
        <h1>设置</h1>
        <p class="header-subtitle">配置应用程序选项</p>
      </div>
    </div>
    <div class="content">
      <div class="card">
        <h2>常规设置</h2>
        <div class="setting-item">
          <label for="theme">主题</label>
          <select id="theme" class="setting-select">
            <option value="light">明亮</option>
            <option value="dark">暗黑</option>
          </select>
        </div>

        <div class="setting-item">
          <label for="language">语言</label>
          <select id="language" class="setting-select">
            <option value="zh">中文</option>
            <option value="en">English</option>
          </select>
        </div>

        <div class="setting-item checkbox-item">
          <label for="autosave" class="checkbox-label">
            <input type="checkbox" id="autosave" class="setting-checkbox" />
            自动保存
          </label>
        </div>
      </div>

      <div class="card">
        <h2>编辑器设置</h2>
        <div class="setting-item">
          <label for="font-size">字体大小</label>
          <select id="font-size" class="setting-select">
            <option value="small">小</option>
            <option value="medium" selected>中</option>
            <option value="large">大</option>
          </select>
        </div>

        <div class="setting-item checkbox-item">
          <label for="line-numbers" class="checkbox-label">
            <input type="checkbox" id="line-numbers" class="setting-checkbox" />
            显示行号
          </label>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.settings {
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

.setting-item {
  margin-bottom: 20px;
  display: flex;
  align-items: center;
}

.setting-item label {
  flex: 1;
  margin-bottom: 0;
  color: var(--color-text);
  font-weight: 500;
}

.checkbox-item {
  display: flex;
  align-items: center;
}

.checkbox-label {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 0;
  cursor: pointer;
}

.setting-select {
  padding: 8px 12px;
  border-radius: 4px;
  border: 1px solid var(--color-border);
  background-color: var(--color-background);
  color: var(--color-text);
  min-width: 150px;
  font-size: 1rem;
}

.setting-checkbox {
  width: 18px;
  height: 18px;
  cursor: pointer;
}
</style>
