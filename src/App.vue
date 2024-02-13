<template>
  <div>
    <button @click="handleClick">+</button>
    <p >{{ count }}</p>
    <button @click="handleClick1">-</button>

  </div>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0);

function handleClick() {
  
  if(count.value <= 10 ){
  count.value++;
  }
  else{
    console.log("Limit is reached");
  }
}
function handleClick1() {
  
  if(count.value >= 0){
  count.value--;
  }
}
</script>
