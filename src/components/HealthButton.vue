<template>
    <button @click="buttonClick">
      <slot></slot>
    </button>
  </template>
  
  <script>
  export default {
    name: 'HealthButton',
    methods: {
      buttonClick() {
        this.$emit('clicked');
      }
    }
  };
  </script>
  
  <style>
  button {
    background-color: darkred;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
  }
  </style>
  