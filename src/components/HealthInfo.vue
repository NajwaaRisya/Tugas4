<template>
    <div class="health-info">
      <h2>{{ title }}</h2>
      <health-button @clicked="handleClick">Lihat Detail</health-button>
      <health-detail v-if="showDetail" :info="info" />
      <slot name="additional-content"></slot>
    </div>
  </template>
  
  <script>
  import HealthButton from './HealthButton.vue';
  import HealthDetail from './HealthDetail.vue';
  
  export default {
    name: 'HealthInfo',
    components: {
      HealthButton,
      HealthDetail
    },
    data() {
      return {
        title: 'Kesehatan Jantung',
        info: 'Informasi mengenai kesehatan jantung.',
        showDetail: false
      };
    },
    methods: {
      handleClick() {
        this.showDetail = !this.showDetail;
        this.$emit('show-detail', this.info);
      }
    }
  };
  </script>
  
  <style>
  .health-info {
    background-color: white;
    padding: 15px;
    border-radius: 10px;
    margin: 10px auto;
    width: 80%;
  }
  </style>
  