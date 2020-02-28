<template>
  <label class="flex flex-col">
    <div v-if="label" v-text="label" class="mb-1 text-sm font-semibold"></div>

    <input
      :type="type"
      :value="value"
      v-bind="$attrs"
      @input="$emit('input', $event.target.value)"
      class="form-input"
    />

    <p v-if="message" v-text="message" class="mt-1 text-sm text-gray-600"></p>
  </label>
</template>

<script>
export default {
  inheritAttrs: true,

  props: {
    value: null,
    type: {
      type: String,
      default: "text"
    },
    label: {
      type: String
    },
    message: {
      type: String
    }
  }
};
</script>
