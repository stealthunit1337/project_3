<template lang="pug">
.wrapper
  my-select
  my-input
  my-input
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import MySelect from '@/components/ui/MySelect.vue';
import MyInput from '@/components/ui/MyInput.vue';

export default defineComponent({
  name: 'MyView',
  components: {
    MySelect, MyInput
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

<style lang="scss">
.wrapper {
  // @include mega
}
</style>