<template>
  <div>
    <p>{{ a.old_data }}</p>
    <button @click="click">渲染</button>
    <p>{{ a.new_data }}</p>
  </div>
</template>

<script setup>
import {reactive} from "vue";

var a = reactive({
  old_data: 1,

})

// eslint-disable-next-line no-unused-vars
function click() {
  a = reactive({
    new_data: 2,
    old_data: 2
  });

  console.log(a);
}


// eslint-disable-next-line no-unused-vars
function click2() {
  a.new_data = 2;
  a.old_data = 2;
  console.log(a);
}


</script>
<script>

export default {
  name: 'App',
}
</script>

<style>
</style>
