<template>
  <div id="app">
    <ParentComponent />
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';
import ChildComponent from './components/ChildComponent.vue';

export default {
  components: {
    ParentComponent
  }
};
</script>