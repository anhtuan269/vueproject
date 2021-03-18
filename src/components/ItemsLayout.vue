<template>
  <div class="row">
    <app-Item
      v-for="(item, index) in layoutItems"
      :key="index"
      @click="removeItem(index)"
    >
    {{item}}
    </app-Item>
  </div>
</template>

<script>
import Items from "./Items.vue";
export default {
  props: {
    layoutItems: Array,
  },
  components: {
    appItem: Items,
  },
  methods: {
    removeItem(index) {
      this.$emit("removeItem", index);
    },
  },
};
</script>

<style>
</style>