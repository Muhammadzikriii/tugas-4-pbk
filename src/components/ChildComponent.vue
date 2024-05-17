<!-- ChildComponent.vue -->
<template>
  <div class="child-container">
    <h2 class="title">Child Component</h2>
    <button class="button" @click="emitData">Send Data to Parent</button>
  </div>
</template>

<script>
export default {
  methods: {
    emitData() {
      const dataToSend = 'Data from child component';
      this.$emit('data-updated', dataToSend);
    }
  }
};
</script>

<style scoped>
.child-container {
  margin-top: 20px;
}

.title {
  font-size: 20px;
  color: #555;
}

.button {
  padding: 10px 20px;
  font-size: 16px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.button:hover {
  background-color: #0056b3;
}
</style>
