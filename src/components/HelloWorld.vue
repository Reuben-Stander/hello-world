<template>
  <v-container class="fill-height">
    <v-btn @click="doSomething">
  My Button
</v-btn>
{{ myAction }}
  </v-container>
</template>

<script setup>
import { ref } from 'vue'
const myAction = ref(null)
function doSomething(){
  myAction.value = "this works!"
}

</script>
