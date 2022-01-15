<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <button @click="handleClick">Go to About</button>
  </div>
</template>

<script lang="ts">
// @ is an alias to /src
import HelloWorld from '../components/HelloWorld.vue'
import { defineComponent } from "vue";
import router from "../router";

export default defineComponent({
  name: 'Home',

  components: {
    HelloWorld
  },

  setup() {
    const handleClick = () => {
      router.push('/about');
    };

    return {
      handleClick,
    }
  }
});
</script>
