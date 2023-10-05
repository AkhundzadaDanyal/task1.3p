<template>
  <header class="custom-header">
    <h1 class="header-title">Mr.Akhundzada Danyal</h1>
    <nav class="main-nav">
      <router-link to="/" class="nav-link">Home</router-link>
      <router-link to="/about" class="nav-link">About</router-link>
      <router-link to="/projects" class="nav-link">Projects</router-link>
      <router-link to="/contact" class="nav-link">Contact</router-link>
    </nav>
  </header>
</template>

<style scoped>
.custom-header {
  background-color: #333;
  padding: 20px;
  color: white;
  text-align: center;
}

.header-title {
  margin: 0;
  font-size: 24px;
}

.main-nav {
  margin-top: 20px;
}

.nav-link {
  margin-right: 20px;
  text-decoration: none;
  color: white;
  font-weight: bold;
  font-size: 18px;
}

.nav-link:hover {
  text-decoration: underline;
}
</style>