<script lang="ts" setup>
const emits = defineEmits(['onClick'])
const handleClick = () => {
  emits('onClick')
}
</script>

<template>
  <button @click="handleClick">
    <slot />
  </button>
</template>

<style lang="scss" scoped>
button {
  background-color: $orange-500;
  border: none;
  border-radius: 22.5px;
  padding: 12.5px;
  width: 100%;
  cursor: pointer;

  &:hover {
    background-color: $white;
  }
}
</style>