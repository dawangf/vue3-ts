<!--
 * @file: parents.
 * @authors: dawangf (dawangf@sina.com).
 * @createDate: 2020/10/13.
 * @version: 1.0.
 * @copyright © 2020 新和兴 All rights reserved.
 -->

<template>
  <div class="parents">
    <p>
      <b>Vue 依赖注入provide和inject的使用：</b>
    </p>
    我是爷爷叫: {{name}}
    <father/>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref, provide} from 'vue';
import father from './father.vue';

export default defineComponent({
  name: 'parents',
  components: {
    father
  },
  setup() {
    const name = ref('姓名');
    provide('name', name)
    const setName = () => {
      name.value = '随机数' + Math.random();
    }
    provide('setName', setName)
    return {
      name
    }
  }
});
</script>

<style scoped>
.parents {
  margin-top: 20px;
  padding: 20px;
  line-height: 50px;
  border: 1px solid #eeeeee;
  background: #b5b7d9;
}
</style>
