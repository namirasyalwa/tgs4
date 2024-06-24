<template>
  <div>
    <h1>Parent Component</h1>
    <child-component @send-to-parent="handleDataFromChild"></child-component>
    <p>{{ parentData }}</p>
    <slot></slot>
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';

export default {
  components: {
    ChildComponent
  },
  data() {
    return {
      parentData: ''
    }
  },
  methods: {
    handleDataFromChild(data) {
      this.parentData = data;
    }
  }
}
</script>
