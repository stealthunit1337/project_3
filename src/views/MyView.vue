<template>
  <div>
    <p>123213</p>
    <my-select></my-select>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import MySelect from '@/components/ui/MySelect.vue';

export default defineComponent({
  name: 'MyView',
  components: {
    MySelect,
  },
});
</script>

<style lang="scss" scoped >
</style>