<template>
  <div>
    <!-- <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a> -->
  </div>
  <HelloWorld msg="Christmas Tree" />
</template>
<script>
import { defineComponent } from 'vue'
import HelloWorld from './components/tree.vue'

export default defineComponent({
  components: {
    HelloWorld
  },
  setup() {
    
  },
})
</script>



<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
