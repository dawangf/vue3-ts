<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
  <e-button>默认按钮</e-button>
  <e-button type="primary">主要按钮</e-button>
  <e-button type="success">成功按钮</e-button>
  <e-button type="info">信息按钮</e-button>
  <e-button type="warning">警告按钮</e-button>
  <e-button type="danger">危险按钮</e-button>
  <div>
    <parents/>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import eButton from './components/eButton.vue';
import parents from './views/provide/parents.vue';

export default defineComponent({
  name: 'App',
  components: {
    HelloWorld,
    eButton,
    parents
  },
  setup() {
    const handelFn = (e: object) => {
      console.log('ee:', e)
    }
    return {
      handelFn
    }
  }
});
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
