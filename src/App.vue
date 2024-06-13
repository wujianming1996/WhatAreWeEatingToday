<template>
  <div id="app">
    <MyButton />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import MyButton from './views/HomeView.vue';
import 'element-plus/dist/index.css';

export default defineComponent({
  name: 'App',
  components: {
    MyButton
  }
});
</script>

