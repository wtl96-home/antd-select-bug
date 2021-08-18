<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3 in CodeSandbox!" />
    <a-modal v-model:visible="dyData.visible" title="Basic Modal" @ok="handleOk">
     <div class="modal" style="height:200px;">
    <p v-for="item in 50" :key="item">{{item}}</p>
           <a-select
      ref="select"
      v-model:value="dyData.value1"
      style="width: 120px"
    > 
      <a-select-option value="jack">Jack</a-select-option>
      <a-select-option value="lucy">Lucy</a-select-option>
      <a-select-option value="disabled" disabled>Disabled</a-select-option>
      <a-select-option value="Yiminghe">yiminghe</a-select-option>
    </a-select>
     </div>
    </a-modal>
</template>

<script>
import { reactive } from 'vue';
import HelloWorldVue from "./components/HelloWorld.vue";
export default {
  name: "App",
  components: {
    HelloWorld: HelloWorldVue,
  },
  setup(){
    console.log(111);
    const dyData = reactive({
      visible:true,
      value1:''
    })
    return {
      dyData
    }
  }
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
.modal{
  height:200px;
  overflow:scroll;
}
</style>
