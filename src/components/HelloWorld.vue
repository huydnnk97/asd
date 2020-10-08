<template>
  <div class="hello">
    <!-- <h1>{{ msg }}</h1> -->
    <h2>Hello World</h2>
    <ul>
      <li v-for="n in 4">{{ themes[n - 1] }}</li>
    </ul>
    <form @submit.prevent="addSkill">
      <input type="text" placeholder="Enter a skill you have.." v-model="skill">
    </form>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      themes: ["HTML", "CSS", "JS", "Vue.js"],
      skills: ["Software", "Web", "Machine Learning"]
    };
  },
  methods: {
    addSkill() {
      this.skills.push({ skill: this.skill });
      this.skill = "";
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>