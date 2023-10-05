<template>
  <section class="home-section">
    <div class="intro">
      <h1>Welcome to My Portfolio</h1>
      <p>
        Hey There! My name is Akhundzada Danyal and i am a Cyber Security Major. 
      This is a web page that I build Hope you like it.
      </p>
    </div>
    <div class="cta">
      <router-link to="/projects">
        <button class="cta-button">View Projects</button>
      </router-link>
    </div>
  </section>
</template>

<style scoped>
.home-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 70vh; /* Adjust the height as needed */
  text-align: center;
}

.intro {
  margin-bottom: 20px;
}

h1 {
  font-size: 2.5em;
  color: #3498db;
}

p {
  font-size: 1.2em;
  color: #555;
  max-width: 600px;
  margin: 0 auto;
}

.cta {
  margin-top: 20px;
}

.cta-button {
  padding: 10px 20px;
  font-size: 1em;
  background-color: #3498db;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.cta-button:hover {
  background-color: #2980b9;
}
</style>