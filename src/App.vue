<template>
  <h1 @click="increase">{{ count }}</h1>
  <div v-if="count > 4">4보다 큽니다</div>
  <ul>
    <Fruit v-for="fruit in fruits" :key="fruit" :name="fruit">{{
      fruit
    }}</Fruit>
  </ul>
</template>

<script>
import Fruit from "./components/Fruit.vue";
export default {
  data() {
    return {
      count: 0,
      fruits: ["Apple", "Banana", "Cherry"],
    };
  },
  components: {
    Fruit,
  },
  methods: {
    increase() {
      this.count += 1;
    },
  },
};
</script>

<style>
h1 {
  color: royalblue;
}
li {
  font-size: 40px;
}
</style>
