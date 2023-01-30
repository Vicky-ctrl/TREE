<template>
  <div class="tree">
    <svg class="tree__star" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 113.32 108.44" :style="{'--delay': LIGHTS}">
      <path d="M90.19 104.33L57.12 87.38 24.4 105l5.91-36.69L3.44 42.65l36.72-5.72 16.1-33.5L73.06 36.6l36.83 4.97-26.35 26.21z" fill="none" stroke-width="6.88" stroke-linecap="round" stroke-linejoin="round"></path>
    </svg>
    <div 
      v-for="(item, index) in lights" 
      :key="index" 
      class="tree__light"
      :style="{'--appear':item.appear, '--y': item.y, '--rotate':item.rotate, '--radius':item.radius, '--speed':item.speed,  '--delay':item.delay}"></div>
  </div>
</template>

<script>
import { 
    reactive,
    toRefs, 
    defineComponent,
    ref,
    onMounted,
    provide,
} from 'vue'
export default defineComponent({
    components: {
    },
    setup() {
        const state = reactive({
          lights: [],
        })
        const LIGHTS = ref(50)
        provide('LIGHTS', LIGHTS)
        onMounted(()=>{
          loadAll()
        })
        const loadAll = () => {
          var num = LIGHTS.value
          const genConfig = (index) => {
            return {
              rotate: 1440 / num * (num - index),
              radius: 12.5 / num * (num - index),
              y: 100 / num * index,
              speed: Math.random() * 10,
              delay: Math.random() * -10,
              appear: index,
            }
          }
          for (let i = 0; i < num; i++) {
            state.lights.push(genConfig(i))
          }
        }
        return {
            ...toRefs(state),
            loadAll,
            LIGHTS,
        };
    },
})
</script>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
