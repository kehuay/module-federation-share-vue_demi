<script setup lang="ts">
import { loadRemote } from "@module-federation/enhanced/runtime";
import { defineAsyncComponent } from 'vue'

const RemoteApp = defineAsyncComponent(() => loadRemote("remote/App"))
</script>

<template>
  <div class="text-40px">Host</div>
  <div>
    <RemoteApp />
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
