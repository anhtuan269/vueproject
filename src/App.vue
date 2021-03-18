<template>
  <div class="container">
    <p>xin chao</p>
    <Header :itemsCount="items.length" :maxItems="maxItems"></Header>
    <CreateItem @addItem="addItem" :items="items" ></CreateItem>
    <ItemsLayout :layoutItems="items" @removeItem="removeItem" />
  </div>
</template>

<script>
import ItemsLayout from "./components/ItemsLayout.vue";
import CreateItem from "./components/CreateItem.vue";
import Header from "./components/Header.vue";
export default {
  name: "App",
  components: {
    ItemsLayout,
    CreateItem,
    Header,
  },
  data() {
    return {
      items: ["No pain no gain"],
      maxItems: 10,
    };
  },
  methods: {
    addItem(item) {
      if(this.items.length > 9) {
        alert('Xóa bớt dữ liệu trước khi nhập thêm')
      } else {
      this.items.push(item);        
      }
    },
    removeItem(index) {
      this.items.splice(index, 1);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
