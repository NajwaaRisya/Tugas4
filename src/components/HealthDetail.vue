<template>
    <div class="health-detail">
      <p>{{ info }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HealthDetail',
    props: {
      info: String
    }
  };
  </script>
  
  <style>
  .health-detail {
    background-color: lightcoral;
    padding: 10px;
    border-radius: 5px;
    margin-top: 10px;
  }
  </style>
  