<!--
 * @file: parents.
 * @authors: dawangf (dawangf@sina.com).
 * @createDate: 2020/10/13.
 * @version: 1.0.
 * @copyright © 2020 新和兴 All rights reserved.
 -->

<template>
  <div class="son">
    我是孙子，我的爷爷叫: {{name}}
    <button @click="setName">点我改变爷爷的名字</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, inject } from 'vue';

export default defineComponent({
  name: 'son',
  setup() {
    const name = inject('name');
    const setName = inject('setName')
    return {
      name,
      setName
    }
  }
});
</script>

<style scoped>
.son {
  padding: 20px;
  border: 1px solid #eeeeee;
  background: #dbcdb5;
}
</style>
