<!--
 * @file: parents.
 * @authors: dawangf (dawangf@sina.com).
 * @createDate: 2020/10/13.
 * @version: 1.0.
 * @copyright © 2020 新和兴 All rights reserved.
 -->

<template>
  <div class="father">
    我是儿子，我的父亲叫: {{name}}
    <son/>
  </div>
</template>

<script lang="ts">
import { defineComponent, inject } from 'vue';
import son from './son.vue';

export default defineComponent({
  name: 'father',
  components: {
    son
  },
  setup() {
    const name = inject('name');
    return {
      name
    }
  }
});
</script>

<style scoped>
.father {
  padding: 20px;
  border: 1px solid #eeeeee;
  background: #a4da89;
}
</style>
