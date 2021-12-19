<template>
  <div id="app">
    <List :list="['apple', 'orange', 'banana', 'grape']" />
  </div>
</template>

<script>
import List from './components/List.vue';

export default {
  components: {
    List,
  },
};
</script>
