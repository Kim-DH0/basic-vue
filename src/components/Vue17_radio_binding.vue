<template>
  <h1>form element radio binding</h1>
  <label for="radioA">A</label>
  <input type="radio" name="radios" id="radioA" v-model="pick" v-bind:value="A">
  <label for="radioB">B</label>
  <input type="radio" name="radios" id="radioB" v-model="pick" v-bind:value="B">
  <label for="radioC">C</label>
  <input type="radio" name="radios" id="radioC" v-model="pick" v-bind:value="C">
  <br><span>{{pick}}</span>
  <input type="hidden" name="choice" v-text="pick">
</template>

<script>
export default {
  data: () => ({
    pick: "A", A: "A", B: "B", C: "C"
  })
}
</script>

<style>
  
</style>