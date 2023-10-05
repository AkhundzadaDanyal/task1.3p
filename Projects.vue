<template>
  <section class="projects-section">
    <h2>Projects</h2>
    <div v-for="project in projects" :key="project.id" class="project-item">
      <h3>{{ project.title }}</h3>
      <a :href="project.link" target="_blank" class="project-link">{{
        project.description
      }}</a>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          title: "Akhundzada Danyal Dark Theme Page",
          description: "Task 1.1P - A website with a cute buffalo where you can Enter yout email and password.",
          link: "https://github.com/AkhundzadaDanyal/Task1.1",
        },
        {
          id: 2,
          title: "Awesome responsive web design",
          description: "creatively designed website to showcase the possibilities of responsive web design.",
          link: "https://github.com/AkhundzadaDanyal/task1.2p",
        },
      ],
    };
  },
};
</script>

<style scoped>
.projects-section {
  text-align: left;
  margin: 20px;
}

.project-item {
  margin-bottom: 20px;
}

.project-link {
  text-decoration: none;
  color: #3498db;
  font-weight: bold;
}

.project-link:hover {
  text-decoration: underline;
}
</style>