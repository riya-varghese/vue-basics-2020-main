<template>
  <div class="container">
    <h1> {{ student }}</h1>
    <button v-on:click="changeStudent">Heads or Tails</button>
    <h3>{{ animal }}</h3>
    <button @click="changeAnimal">Rock Paper Scissors</button>
    <ul>
      <li v-for="animal in animals" :key="animal">{{ animal }}</li>
    </ul>
    <h2 v-if="isLoggedIn">Not Riya </h2>
    <h2 v-else>Welcome Riya</h2>
    <button v-if="isLoggedIn" @click="logout">Begone Imposter</button>
    <button v-else @click="login">Login</button>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {},
  data() {
    return {
      student: ["Heads", "Tails"],
      animals: ["Rock", "Paper", "Scissors"],
      animal: "",
      isLoggedIn: false,
    };
  },
  methods: {
    changeStudent: function() {
      this.student = "Tails";
    },
    changeAnimal: function() {
      let number = Math.floor(Math.random() * 5);
      this.animal = this.animals[number];
    },
    login: function() {
      this.isLoggedIn = true;
    },
    logout: function() {
      this.isLoggedIn = false;
    },
  },
  created() {},
  mounted() {
    this.changeAnimal();
  },
  beforeCreate() {},
};
</script>

<style lang="scss" scoped>
h1 {
  font-size: 3rem;
}
button {
  font-size: 2rem;
}
</style>
