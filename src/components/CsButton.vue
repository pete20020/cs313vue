<template>
  <div>
    <button v-on:click="upFunction" class="btn btn-info mr-3" >{{lable}}LIKE</button>
    <button v-on:click="downFunction" class="btn btn-info mr-3" >{{lable}}LOVE</button>
    <button v-on:click="LoveFunction" class="btn btn-info mr-3">{{lable}}UNLIKE</button>
    <button v-on:click="ResetFunction" class="btn btn-info mr-4">{{lable}}RESET</button>
  </div>
</template>

<script>
export default {
  name: "Soda",
  props: {
    label: String,
  },
  data: function () {
    return {
      counter: 0,
      fsize : 50 ,
    };
  },
  
  methods : {
    upFunction : function(){
      this.counter += 1
      this.$emit('cc',this.counter)
    },
    downFunction : function(){
      this.counter += 5
      this.$emit('cc',this.counter)
    },
    LoveFunction: function () {
      this.counter -= 10
      this.$emit("cc", this.counter);
    },
    ResetFunction: function () {
      this.counter = 0
      this.$emit("cc", this.counter);
    },
  },
};
</script>

<style>
</style>