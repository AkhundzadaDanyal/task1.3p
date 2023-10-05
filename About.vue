<template>
  <section>
    <h2>Welcome to My Portfolio</h2>
    <p>
      Hey There! My name is Akhundzada Danyal and i am a Cyber Security Major. 
      This is a web page that I build Hope you like it.
    </p>
    <p>
      Please selcet from the given options.
      I have made a number game for you and a Joke roullete to lift up your mood.
    </p>

    <div>
      <h3>Guess the Number Game</h3>
      <p>Try to guess the correct number between 1 and 10.</p>
      <input v-model="userGuess" type="number" placeholder="Enter your guess" />
      <button @click="checkGuess">Submit Guess</button>
      <p v-if="feedback">{{ feedback }}</p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      correctNumber: Math.floor(Math.random() * 10) + 1,
      userGuess: null,
      attempts: 0,
      maxAttempts: 3,
      feedback: "",
    };
  },
  methods: {
    checkGuess() {
      this.attempts++;

      if (this.userGuess === this.correctNumber) {
        this.feedback = "Congratulations! You guessed the correct number.";
      } else if (this.attempts === this.maxAttempts) {
        this.feedback = `Sorry, you've reached the maximum attempts. The correct number was ${this.correctNumber}.`;
        alert("You failed!");
      } else {
        this.feedback =
          this.userGuess < this.correctNumber
            ? "Try a higher number."
            : "Try a lower number.";
      }
    },
  },
};
</script>

<style scoped>
section {
  text-align: center;
  margin: 20px;
}

h2 {
  color: #3498db;
}

p {
  margin-bottom: 15px;
}

div {
  margin-top: 30px;
  border: 1px solid #ddd;
  padding: 15px;
  border-radius: 5px;
}

h3 {
  color: #3498db;
}

input {
  margin-right: 10px;
}

button {
  background-color: #3498db;
  color: white;
  padding: 5px 10px;
  border: none;
  border-radius: 3px;
  cursor: pointer;
}

p[if] {
  color: red;
}
</style>