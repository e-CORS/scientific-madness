<template>
  <div
    :class="['tab-wrapper', { 'active-tab': isActive }]"
    @click="$emit('set-active-component', tabComponent)"
  >
    <span>{{ tabName }}</span>
  </div>
</template>

<script setup>
defineProps({
  tabName: String,
  isActive: Boolean,
  tabComponent: String,
});
</script>

<style scoped>
.tab-wrapper {
  padding: 10px;
  width: fit-content;
  height: 20px;
  border: 1px solid white;
  flex-grow: 1;
  border-top: none;
  border-right: none;
  background-color: #303030;
  cursor: pointer;
}
.tab-wrapper:first-child {
  border-left: none;
}
.active-tab {
  background-color: #1b1b1b;
}
</style>
