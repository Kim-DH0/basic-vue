<template>
  <h1>form element checkbox</h1>
  <form action="">
      <input placeholder="edit me" v-model="message">
      <p>Message is {{message}}</p>
      <label for="checkbox">체크 유무: {{state}}</label>
      <input type="checkbox" id="checkbox" v-model="checked" v-on:change="checkIt"><br>

      <label for="banana">바나나: </label>
      <input type="checkbox" id="banana" v-model="selFruit" value="banana" name="fruits">
      <label for="apple">사과: </label>
      <input type="checkbox" id="apple" v-model="selFruit" value="apple" name="fruits">
      <label for="pine-apple">파인애플: </label>
      <input type="checkbox" id="pine-apple" v-model="selFruit" value=pine-apple name="fruits"><br>
      <span>Multiline message :</span>
      <p style="white-space: pre-line">{{multiline}}</p>
      <textarea v-model="multiline" cols="30" rows="5"></textarea>
      <!-- <textarea cols="30" rows="10">{{multiline}}</textarea> vue3에서는 적용 안 됨 -->
  </form>
</template>

<script>
export default {
  data() {
    return {
    message : "저자의 머릿속에는 마구니가 가득하다. 그 마구니를 때려 죽여라.", multiline: "여러 줄을 작성합니다.\n\n",
    checked : true, state: "동의함", selFruit: ['pine-apple', 'banana'],
    }
  },
  methods: {
    checkIt() {
      this.state = (this.checked)? "동의함" : "동의 안 함"
    }
  }
}
</script>

<style>

</style>