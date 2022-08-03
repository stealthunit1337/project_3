<template>
  <slot>
    <label for="" placeholder="label"></label>
    <input type="text">
  </slot>
</template>

<script lang="ts">
import { defineComponent, computed, ref } from 'vue';

export default
  defineComponent({
    name: 'MyInput',
    props: {
      label: {
        type: String
      },
      userName: {
        type: String
      },
      password: {
        type: String
      }
    },
    setup(props, { emit }) {
    }
  });
</script>

<style lang="scss" scoped>
</style>