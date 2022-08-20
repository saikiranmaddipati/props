<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <propsExamples
      v-for="(value, index) in content"
      :key="index"
      v-bind:value="value"
      v-bind:index="index"
    />
    <slots-examples>
      <template v-slot:title>
        <h1>{{ heading }}</h1>
      </template>
      <p>{{ paragraph }}</p>
    </slots-examples>
  </div>
</template>

<script>
import propsExamples from "./components/PropsExamples.vue";
import slotsExamples from "./components/SlotsExamples.vue";

export default {
  name: "App",
  components: {
    propsExamples,
    "slots-examples": slotsExamples,
  },
  data() {
    return {
      content: [{ name: "sai" }, { name: "kiran" }, { name: "sunny" }],
      heading: "Hello Welcome to Slots",
      paragraph: "mutiple slots",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
