<script setup lang="ts"></script>

<template>
  <div class="flex flex-col lg:flex-row gap-2 my-12px">
    <slot />
  </div>
</template>

<style scoped lang="scss">
div :deep(> *) {
  min-width: 50%;
  flex-grow: 1;
  flex-shrink: 1;
  margin: 0 !important;
}

div {
  :deep(code),
  :deep(pre) {
    margin-bottom: 0 !important;
  }
}
</style>
