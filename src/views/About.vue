<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button @click="handleClick">Go to Home</button>
  </div>
</template>

<script lang="ts">
// @ is an alias to /src
import { defineComponent } from "vue";
import router from "../router";

export default defineComponent({
  name: 'About',

  setup() {
    const handleClick = () => {
      router.push('/');
    };

    return {
      handleClick,
    }
  }
});
</script>
