<script setup lang="ts"></script>

<template>
  <div class="flex flex-col lg:flex-row gap-2 my-12px">
    <slot />
  </div>
</template>

<style scoped lang="scss">
div :deep(> *) {
  flex-grow: 1;
  margin: 0 !important;
}
</style>
