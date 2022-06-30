<template>
  <h3>模拟</h3>
  <div>info:{{ info }}</div>
  <ul>
    <li v-for="m in mock" :key="m">{{ m }}</li>
  </ul>
</template>
<script lang="ts">
import { defineComponent, ref } from "vue";
import { useStore } from "vuex";
import { key, State } from "../store";
export default defineComponent({
  asyncData({ store, route }: any) {
    return store.dispatch("mockData");
  },
  setup(props, context) {
    const { mock } = useStore<State>(key).state;
    const info = ref('')
    setTimeout(()=>{
      info.value = '3'
    },3000)

    return {
      mock,
      info
    };
  },
});
</script>
<style lang="scss"></style>
