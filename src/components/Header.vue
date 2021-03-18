<template>
  <div class="row">
    <div class="col-sm-12">
      <div class="progress">
        <div
          class="progress-bar bg-info"
          role="progressbar"
          :style="{width: (itemsCount/maxItems) *100 + '%'}"
          aria-valuenow="50"
          aria-valuemin="0"
          aria-valuemax="100"
        ></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props: {
    maxItems:Number,
    itemsCount:Number
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style>
</style>