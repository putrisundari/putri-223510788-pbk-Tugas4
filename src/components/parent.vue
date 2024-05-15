<template>
    <div>
      <h2>Parent Component</h2>
      <p>Data from Child: {{ childData }}</p>
      <ChildOne @data-from-child="handleDataFromChild" />
      <ChildTwo @data-from-child="handleDataFromChild" />
    </div>
  </template>
  
  <script>
  import ChildOne from './childone.vue';
  import ChildTwo from './childtwo.vue';
  
  export default {
    name: 'Parent',
    components: {
      ChildOne,
      ChildTwo
    },
    data() {
      return {
        childData: ''
      };
    },
    methods: {
      handleDataFromChild(data) {
        this.childData = data;
      }
    }
  }
  </script>