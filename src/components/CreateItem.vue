<template>
  <div class="row">
    <form action="">
      <div class="col-sm-8 offset-sm-2 col-md-6 offset-md-3 form-group">
        <label for=""> U can saying...</label>
        <textarea class="form-group" v-model=" item" name="" id="" cols="30" rows="10"></textarea>
        <button class="btn btn-success" @click.prevent="createNew"> Add</button>
      </div>
    </form>
  </div>
  
</template>

<script>
export default {
  props : {
    items:Array 
  },
  data() {
    return {
      item: ''
    };
  },
  methods: {
    createNew(){
     if(this.item == '') {
       return false
     } else if (this.items.includes(this.item)){
       return alert('Item đã tồn tại ')
     } else {
       this.$emit('addItem', this.item);
       this.item = '';
     }
    }
  }
};
</script>

<style>
label {
  display: block;
  margin-bottom:30px;
}
button.btn {
  display: block;
  margin: 10px auto;

}
textarea {
  width: 100%;
  resize: none;
}

</style>