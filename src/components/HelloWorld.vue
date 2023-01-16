<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
  <div class="tree">
    <svg class="tree__star" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 113.32 108.44" style="--delay: 50">
      <path d="M90.19 104.33L57.12 87.38 24.4 105l5.91-36.69L3.44 42.65l36.72-5.72 16.1-33.5L73.06 36.6l36.83 4.97-26.35 26.21z" fill="none" stroke-width="6.88" stroke-linecap="round" stroke-linejoin="round"></path>
    </svg>
  </div>
  <!-- <span>{{ msg }}</span> -->

  <!-- <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Install
    <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>
    in your IDE for a better DX
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p> -->
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
