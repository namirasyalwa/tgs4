<template>
    <div>
      <button @click="sendData">click me</button>
    </div>
    
  </template>
  
  <script>
  export default {
    methods: {
      sendData() {
        this.$emit('send-to-child', 'hola! ini data dari grandchild');
      }
    }
  }
  </script>
  