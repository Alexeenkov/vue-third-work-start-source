<template>
  <div class="app_layout">
    <AppLayoutHeader />
    <slot></slot>
  </div>
</template>

<script setup>
import AppLayoutHeader from "@/layouts/AppLayoutHeader.vue";
</script>

<style lang="scss" scoped>
.app_layout {
  display: flex;
  flex-direction: column;
  height: 100vh;
}
</style>
