<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <OrderItem msg="Welcome to Your Vue.js App" />
    <OrderList />
    <Button @click="increment"> Click me </Button>
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import OrderItem from "./components/OrderItem.vue";
import OrderList from "./components/OrderList.vue";

import Button from "./components/Button.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    OrderItem,
    OrderList,
    Button,
  },
  data() {
    return {
      amountClicks: 0,
    };
  },
  computed: {
    title() {
      return `amoumt of clicks ${this.amountClicks}`;
    },
  },
  methods: {
    increment() {
      this.amountClicks += 1;
    },
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
