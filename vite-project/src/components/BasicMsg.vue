<template>
<div v-bind:style="style">
  {{msg}} 
  <div :class="cls">哈哈</div>
  <input type="text" v-model="message">
  {{message}}
</div>

</template>

<script setup lang="ts">
import {ref} from 'vue'
defineProps<{ msg: string }>()

type Style={
  color:string,
  height:string
}
const style:Style={
  color:"blue",
  height:"50px"
}

type Cls = {
  a:boolean,
  b:boolean
}
const cls:Cls={
  a:true,
  b:true
}
// const message:string = "test";
const message = ref("test")
</script>

<style scoped>
.a{
  color: red;
}
.b{
  border:1px solid blue;
}
</style>
