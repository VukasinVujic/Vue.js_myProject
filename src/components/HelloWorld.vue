<template>
  <div v-bind:id="randomId">
    <div>{{ name }}</div>
    <div>{{ randomId * 100 }}</div>
    <div>{{ animals[0] }}</div>
    <div>{{ name.split('').reverse().join('') }}</div>
    <div>{{ randomId % 2 === 0 ? 'Deljiv' : 'Nije deljiv' }}</div>

    <div v-if="name === 'Ala' ">hello , {{ name }}</div>
    <div v-else>MEGA HAOS</div>

    <button @click="handleClick">click me</button>
    
    <a :href="link">Link</a>

    <form @submit.prevent="handleSubmit">
      <button type="submit">submit</button>
    </form>

    <div :class="{ 'blue' : isBlue}">I am blue</div>

    <ul>
      <li v-for="(color, index) in colors" :key="color">{{ color }} {{ index }}</li>
    </ul>

    <div>
      <input type="text" v-model="name222">
    </div>

    <button @click="handleClick_2">Greet</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Ala",
      name222: " ",
      randomId: Math.random(),
      animals: ["dog", "cat"],
      link: "https://www.google.rs/",
      isBlue: true,
      colors: ["red", "green", "blue"]
    };
  },

  methods: {
    handleClick() {
      console.log("CLICKED MEGA MEGA MEGA", event);
    },

    handleSubmit() {
      event.preventDefault();
      console.log("submitted");
    },
    handleClick_2() {
      alert(`hello,  ${this.name222} `);
    }
  }
};
</script>

<style>
.blue {
  background-color: blueviolet;
}
</style>
