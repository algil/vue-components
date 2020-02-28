<template>
  <div class="container h-screen py-8 mx-auto">
    <section class="">
      <h2 class="mb-8 text-5xl text-gray-800">Input</h2>
      <base-input
        label="Name"
        v-model="demo"
        placeholder="Some placeholder"
      ></base-input>
    </section>
  </div>
</template>

<script>
import BaseInput from "./components/BaseInput";

export default {
  components: {
    BaseInput
  },

  data() {
    return {
      demo: ""
    };
  }
};
</script>
