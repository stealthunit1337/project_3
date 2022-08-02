<template>
  <div>
    <div v-if="isVisible == 1">qwe</div>
    <div v-if="isVisible == 2">zxc</div>
    <p>123213</p>
    <my-select v-model:isVisible="isVisible" :items="items"></my-select>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import MySelect from '@/components/ui/MySelect.vue';

export default defineComponent({
  name: 'MyView',
  components: {
    MySelect,
  },
  setup() {
    const items = [
      { name: "kappa", id: 1 },
      { name: "keepo", id: 2 },
    ]
    const isVisible = ref()
    return {
      items,
      isVisible
    }
  }
});

</script>

<style lang="scss" scoped >
</style>