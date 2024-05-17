<!-- ParentComponent.vue -->
<template>
  <div class="parent-container">
    <h1 class="title">Parent Component</h1>
    <div class="content-wrapper">
      <slot></slot> <!-- Menambahkan slot di sini -->
    </div>
    <ChildComponent @data-updated="updateData" />
    <p class="child-data">Data from Child: {{ childData }}</p>
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
      childData: ''
    };
  },
  methods: {
    updateData(data) {
      this.childData = data;
    }
  }
};
</script>

<style scoped>
.parent-container {
  max-width: 600px;
  margin: 20px auto;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  background-color: #000; /* Ubah warna latar belakang menjadi hitam */
  color: #fff; /* Ubah warna font menjadi putih */
}

.title {
  font-size: 28px;
  color: #fff;
  margin-bottom: 20px;
}

.content-wrapper {
  padding: 20px;
  border-radius: 8px;
  color: #000; /* Ubah warna font menjadi hitam */
}

.child-data {
  font-size: 18px;
  color: #fff; /* Ubah warna font menjadi putih */
  margin-top: 20px;
}
</style>
