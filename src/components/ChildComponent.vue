<template>
  <div>
    <h2>Child Component</h2>
    <grand-child-component @send-to-child="handleDataFromGrandChild"></grand-child-component>
    <p>{{ childData }}</p>
  </div>
</template>

<script>
import GrandChildComponent from './GrandChildComponent.vue';

export default {
  components: {
    GrandChildComponent
  },
  data() {
    return {
      childData: ''
    }
  },
  methods: {
    handleDataFromGrandChild(data) {
      this.childData = data;
      this.$emit('send-to-parent', data);
    }
  }
}
</script>
