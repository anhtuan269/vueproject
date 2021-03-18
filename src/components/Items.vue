<template>
  <div class="col-sm-6 col-md4 col-lg-3">
    <div class="card">
      <div class="card-body item">
          <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style>
.item {
    cursor:pointer;
}
.item:hover {
    color: #dedede;
}
</style>