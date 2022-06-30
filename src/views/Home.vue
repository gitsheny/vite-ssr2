<template>
  <div class="home">
    <h1>HOME.</h1>
    <el-date-picker
        v-model="value1"
        type="date"
        placeholder="Pick a day"
    />
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  setup() {
    const value1 = ref('')
    return {
      value1
    }
  }
});
</script>
<style scoped>
.home {
  text-align: center;
}
</style>
