<template>
    <div class="child">
      <h3>Child One</h3>
      <button @click="sendData">Klik Tombol Ini</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'childone',
    emits: ['data-from-child'],
    setup(props, { emit }) {
      const sendData = () => {
        emit('data-from-child', 'Data from child one');
      };
  
      return {
        sendData,
      };
    },
  };
  </script>
  
  <style scoped>
  .child {
    border: 1px solid rgb(123, 123, 185);
    padding: 10px;
    margin: 10px;
    text-align: center;
  }
  button {
    background-color: rgb(115, 115, 158);
    color: white;
    border: none;
    padding: 10px 20px;
    cursor: pointer;
  }
  button:hover {
    background-color: rgb(95,95,140);
  }
  </style>
  