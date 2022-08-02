<template>
  <slot>
    <select name="" id="">
      <option disabled selected>Choose an option</option>
      <option v-for="item in items" @click="someMethod(item.id)">{{ item.name }}</option>
    </select>
  </slot>
</template>

<script lang="ts">
import { defineComponent, computed, ref } from 'vue';

export default
  defineComponent({
    name: 'MySelect',
    props: {
      items: {
        type: [Object]
      },
      id: {
        type: Number
      },
      isVisible: {
        type: Number
      }
    },
    setup(props, { emit }) {

      const currentValue = computed({
        get: () => props.id,
        set: (e) => emit("update:isVisible", e)
      });

      const someMethod = (id: Number) => {
        emit("update:isVisible", id)
        console.log('123')
      }
      return {
        someMethod
      }
    }
  });
</script>

<style lang="scss" scoped>
</style>