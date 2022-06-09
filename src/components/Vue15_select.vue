<template>
  <h1>form element select</h1>
  select의 option에 value 값을 넣지 않으면 text의 값이 value가 됨<br>
  <select v-model="selected">
    <option value="" disabled>Please select one</option>
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>
  <span>{{selected}}</span><br><br>
  <select v-model="arrSelect">
    <option value="" disabled>Please select one</option>
    <option v-for="(item, i) in arrObj" :key="i" v-bind:value="item.value">{{item.text}}</option>
  </select>
</template>
  
<script>
export default {
  data() {
    return {
      selected: "A",
      arrSelect: ["C", "A"],
      arrObj: [{text:'One', value:'A'}, {text:'Two', value:'B'},
      {text:'Three', value:'C'}, {text:'Four', value:'D'}],
      arrString: ['A', 'B', 'C', 'D']
    }
  }
}
</script>

<style>

</style>