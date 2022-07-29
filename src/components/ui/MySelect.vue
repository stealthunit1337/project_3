<template>
  <slot>
    <select name="" id="">
      <option disabled selected>Choose an option</option>
      <options v-for="option in options" value=""></options>
    </select>
  </slot>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'MySelect',
  props: {
    options: Array,
  },
});
</script>

<style lang="scss" scoped>
</style>