<template>
  <div id="app">
    <parent-component>
      <h4>Ini merupakan tugas 4 Praktikum PBK </h4>
    </parent-component>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  components: {
    ParentComponent
  }
}
</script>

<style>
@import './style.css';
</style>