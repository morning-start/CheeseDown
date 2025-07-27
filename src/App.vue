<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="layout">
    <nav class="sidebar">
      <div class="logo">
        <h2>CheeseDown</h2>
        <p class="logo-subtitle">富文本编辑器</p>
      </div>
      <ul class="nav-links">
        <li>
          <RouterLink to="/" active-class="active" class="nav-link">
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" fill="currentColor" viewBox="0 0 16 16">
              <path d="M12.5 0H3.5A1.5 1.5 0 0 0 2 1.5v13A1.5 1.5 0 0 0 3.5 16h9a1.5 1.5 0 0 0 1.5-1.5v-13A1.5 1.5 0 0 0 12.5 0zM3.5 1a.5.5 0 0 1 .5.5v1a.5.5 0 0 1-.5.5H3v11h10V2h-.5a.5.5 0 0 1-.5-.5v-1a.5.5 0 0 1 .5-.5h9A.5.5 0 0 1 13 1.5v13a.5.5 0 0 1-.5.5h-9a.5.5 0 0 1-.5-.5v-13z"/>
              <path d="M4 3h8a1 1 0 0 1 1 1v1a1 1 0 0 1-1 1H4a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1zm0 4h8a1 1 0 0 1 1 1v1a1 1 0 0 1-1 1H4a1 1 0 0 1-1-1V8a1 1 0 0 1 1-1zm0 4h5a1 1 0 0 1 1 1v1a1 1 0 0 1-1 1H4a1 1 0 0 1-1-1v-1a1 1 0 0 1 1-1z"/>
            </svg>
            <span>编辑器</span>
          </RouterLink>
        </li>
        <li>
          <RouterLink to="/about" active-class="active" class="nav-link">
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" fill="currentColor" viewBox="0 0 16 16">
              <path d="M8 15A7 7 0 1 1 8 1a7 7 0 0 1 0 14zm0 1A8 8 0 1 0 8 0a8 8 0 0 0 0 16z"/>
              <path d="M8.93 6.588l-2.29.287-.082.38.45.083c.294.07.352.176.288.469l-.738 3.468c-.194.897.105 1.319.808 1.319.545 0 1.178-.252 1.465-.598l.088-.416c-.2.176-.493.246-.686.246-.275 0-.375-.193-.304-.533L8.93 6.588zM9 4.5a1 1 0 1 1-2 0 1 1 0 0 1 2 0z"/>
            </svg>
            <span>关于</span>
          </RouterLink>
        </li>
        <li>
          <RouterLink to="/settings" active-class="active" class="nav-link">
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" fill="currentColor" viewBox="0 0 16 16">
              <path d="M8 4.754a3.326 3.326 0 1 0 0 6.492 3.326 3.326 0 0 0 0-6.492zM5.326 8a2.674 2.674 0 1 1 5.348 0 2.674 2.674 0 0 1-5.348 0z"/>
              <path d="M9.254 8a1.254 1.254 0 1 0-2.508 0 1.254 1.254 0 0 0 2.508 0zM8 1.5A6.5 6.5 0 0 0 1.5 8a6.5 6.5 0 0 0 6.5 6.5 6.5 6.5 0 0 0 6.5-6.5A6.5 6.5 0 0 0 8 1.5zm0 12a5.5 5.5 0 1 1 0-11 5.5 5.5 0 0 1 0 11z"/>
              <path d="M8 16a8 8 0 1 0 0-16 8 8 0 0 0 0 16zM8 2a6 6 0 1 1 0 12A6 6 0 0 1 8 2z"/>
            </svg>
            <span>设置</span>
          </RouterLink>
        </li>
      </ul>
    </nav>

    <main class="main-content">
      <RouterView />
    </main>
  </div>
</template>

<style scoped>
.layout {
  display: flex;
  min-height: 100vh;
}

.sidebar {
  width: 250px;
  background: linear-gradient(180deg, var(--color-background-soft), var(--color-background-mute));
  padding: 20px 0;
  border-right: 1px solid var(--color-border);
  box-shadow: 3px 0 10px rgba(0, 0, 0, 0.05);
  display: flex;
  flex-direction: column;
}

.logo {
  padding: 0 20px 20px;
  border-bottom: 1px solid var(--color-border);
  margin-bottom: 20px;
}

.logo h2 {
  color: var(--color-heading);
  margin: 0;
  font-size: 1.5rem;
}

.logo-subtitle {
  color: var(--color-text);
  opacity: 0.7;
  font-size: 0.85rem;
  margin: 5px 0 0;
}

.nav-links {
  list-style: none;
  padding: 0;
  margin: 0;
  flex-grow: 1;
}

.nav-links li {
  margin-bottom: 5px;
}

.nav-link {
  display: flex;
  align-items: center;
  padding: 12px 20px;
  text-decoration: none;
  color: var(--color-text);
  transition: all 0.2s ease;
  border-left: 3px solid transparent;
  gap: 12px;
}

.nav-link:hover {
  background-color: var(--color-background);
  border-left: 3px solid #42b883;
}

.nav-link.active {
  background-color: var(--color-background);
  border-left: 3px solid #42b883;
  font-weight: 600;
}

.main-content {
  flex: 1;
  overflow-y: auto;
  background-color: var(--color-background);
}
</style>