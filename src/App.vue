<template>
  <div class="app">
    <h1>Informasi Kesehatan</h1>
    <health-info @show-detail="displayDetail">
      <template #additional-content>
        <p>Kondisi Jantung Anda Saat Ini Normal.</p>
      </template>
    </health-info>
    <div v-if="detail" class="detail-section">
      <h2>Detail Informasi</h2>
      <p>{{ detail }}</p>
    </div>
  </div>
</template>

<script>
import HealthInfo from './components/HealthInfo.vue';

export default {
  name: 'App',
  components: {
    HealthInfo
  },
  data() {
    return {
      detail: ''
    };
  },
  methods: {
    displayDetail(data) {
      this.detail = data;
    }
  }
};
</script>

<style>
.app {
  background-color: pink;
  padding: 20px;
  text-align: center;
}

.detail-section {
  margin-top: 20px;
}
</style>
