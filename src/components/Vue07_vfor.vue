<template>
  <h1>v-for</h1>
  <!-- <ul> -->
    <!-- <li v-for="(item, idx) in list" :key="idx">{{idx + 1}}. {{item}}</li> -->
  <!-- </ul> -->
    <ul v-for="item in 8" :key="item">
      <li v-for="item2 in 9" :key="item2">
      {{item + 1}} x {{item2}} = {{(item + 1) * item2}}</li>
  </ul>
</template>

<script>
  export default {
    data() {
      return {
        // list: [1, 2, 3, 4, 5, 6, 7, 8, 9]
        // list: ['Busan', 'Seoul', 'Changwon', 'Pohang', 'Incheon']
      }
    }
  }
</script>

<style>
  ul {
    text-align: center;
    list-style: none;
  }
</style>