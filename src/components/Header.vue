<template>
  <header class="header">
    <div class="header-logo">
      <div class="logo-icon">
        <!-- SVG code here -->
      </div>
      <h2>Kerala Tourism</h2>
    </div>
    <div class="header-nav">
      <div class="nav-links">
        <a href="#" v-for="link in navLinks" :key="link">{{ link }}</a>
      </div>
      <button class="login-button">
        <span>Login</span>
      </button>
      <div class="user-avatar"></div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    navLinks: {
  type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  white-space: nowrap;
  border-bottom: 1px solid #f5f3f0;
  padding: 0.75rem 2.5rem;
}

.header-logo {
  display: flex;
  align-items: center;
  gap: 1rem;
  color: #181611;
}

.logo-icon {
  width: 1rem;
  height: 1rem;
}

.header-logo h2 {
  font-size: 1.125rem;
  font-weight: 700;
  line-height: 1.25;
  letter-spacing: -0.015em;
}

.header-nav {
  display: flex;
  flex: 1;
  justify-content: flex-end;
  gap: 2rem;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 2.25rem;
}

.nav-links a {
  color: #181611;
  font-size: 0.875rem;
  font-weight: 500;
  line-height: normal;
  text-decoration: none;
}

.login-button{
  display: flex;
  min-width: 84px;
  max-width: 480px;
  cursor: pointer;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  border-radius: 9999px;
  height: 2.5rem;
  padding: 0 1rem;
  font-size: 0.875rem;
  font-weight: 700;
  line-height: normal;
  letter-spacing: 0.015em;
}

.login-button {
  background-color: #f5f3f0;
  color: #181611;
}
.user-avatar {
  background-image: url("https://cdn.usegalileo.ai/stability/4a99dfc4-164a-4137-bdf8-5c09bdbca15e.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  border-radius: 9999px;
  width: 2.5rem;
  height: 2.5rem;
}
.main-content {
  padding: 1.25rem 10rem;
  display: flex;
  flex: 1;
  justify-content: center;
}

.layout-content-container {
  display: flex;
  flex-direction: column;
  max-width: 960px;
  flex: 1;
}

.nav-links a {
  position: relative;
}

.nav-links a::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -4px;
  left: 0;
  background-color: #f2a60d;
  transition: width 0.3s ease;
}

.nav-links a:hover::after {
  width: 100%;
}

.login-button:hover {
  background-color: #e5e3e0;
}

.user-avatar:hover {
  transform: scale(1.05);
}
</style>
