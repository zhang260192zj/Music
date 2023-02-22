<script lang="ts" setup>
import {reactive} from 'vue'
import {Greet} from '../../wailsjs/go/main/App'

const data = reactive({
  name: "",
  resultText: "",
})

function greet() {
  Greet().then(result => {
    data.resultText = result
  })
}
greet()

</script>

<template>
<h1>{{data.resultText}}</h1>
</template>

<style scoped>

</style>
