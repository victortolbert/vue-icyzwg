<script>
export default {
  props: {
    list: Array,
  },
  data() {
    return {
      reversed: false,
    };
  },
  computed: {
    reversedList() {
      if (this.reversed) {
        return this.list.reverse();
      } else {
        return this.list;
      }
    },
  },
  methods: {
    toggleReversed() {
      this.reversed = !this.reversed;
    },
  },
};
</script>

<template>
  <div>
    <button @click="toggleReversed">Toggle</button>
    <ul>
      <li v-for="item in reversedList" :key="item">{{ item }}</li>
    </ul>
  </div>
</template>
