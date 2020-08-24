<template>
 <div id="app" >
    <HelloWorld msg="LIKE-UNLIKE" /><hr><br>
    <h1>{{total}}</h1>
    <div class="row">
      <div class="col-12">
        <img alt="Vue logo" src="./assets/1.jpg" width="490" /><br><br><hr>
      </div>
      <div class="col-12">
        <CsButton @cc="sum" />
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue"
import CsButton from "./components/CsButton.vue"

export default {
  name: "App",
  components: {
    HelloWorld,
    CsButton,
  },
  data: function(){
    return {
      total: 0,
    };
  },
  methods: {
    sum(counterValue) {
      this.total = counterValue;
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
