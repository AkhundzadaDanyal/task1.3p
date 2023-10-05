<template>
  <section class="contact-section">
    <h2>Contact</h2>
    <div class="contact-info">
      <div class="contact-item">
        <p class="contact-detail">
          Email:
          <a href="mailto:s223739913@deakin.edu" class="contact-link"
            >s223739913@deakin.edu</a
          >
        </p>
      </div>
      <div class="contact-item">
        <p class="contact-detail">
          Mobile: <a href="tel:+61406506XXX" class="contact-link">0406506XXX</a>
        </p>
      </div>
    </div>
  </section>
  <section class="funny-game">
    <h2>Super Funny Jokes Game</h2>
    <div class="joke-container">
      <p>{{ currentJoke }}</p>
      <button @click="getNewJoke">Get Another Joke</button>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      currentJoke: "",
    };
  },
  mounted() {
    this.getNewJoke();
  },
  methods: {
    async getNewJoke() {
      try {
        const response = await fetch("https://v2.jokeapi.dev/joke/Any");
        const jokeData = await response.json();
        this.currentJoke =
          jokeData.type === "twopart"
            ? `${jokeData.setup} ${jokeData.delivery}`
            : jokeData.joke;
      } catch (error) {
        console.error("Failed to fetch joke", error);
        this.currentJoke = "Error 404. Please try again.";
      }
    },
  },
};
</script>

<style scoped>
.funny-game {
  text-align: center;
  margin: 20px;
}

.joke-container {
  margin-top: 20px;
}

.contact-info {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
  margin-top: 20px;
}

.contact-item {
  display: flex;
  flex-direction: column;
}

.contact-link {
  color: #3498db;
  text-decoration: none;
  font-weight: bold;
}

.contact-link:hover {
  text-decoration: underline;
}

button {
  background-color: #3498db;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  margin-top: 10px;
}

button:hover {
  background-color: #2980b9;
}
</style>