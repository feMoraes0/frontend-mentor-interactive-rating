<script lang="ts" setup>
defineProps({
  isActive: { type: Boolean, default: false }
})
</script>

<template>
  <button :class="{ 'active': isActive }" class="text-preset-3">
    <slot />
  </button>
</template>

<style lang="scss" scoped>
@import '@/scss/styles';

button {
  border-radius: 100%;
  width: 51px;
  height: 51px;
  border: none;
  background-color: $grey-900;
  cursor: pointer;
  color: $grey-500;

  &.active {
    background-color: $orange-500;
    color: $grey-900
  }

  &:hover {
    background-color: $white;
    color: $grey-900
  }
}
</style>