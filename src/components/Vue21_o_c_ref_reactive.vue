<!-- <template>
  <h1>Difference Coposition API and Options API</h1>
  <button @click="count++">count is: {{count}}</button>
</template>

<script>
export default {
  data() {
    return {
      count : 0
    }
  }
}
</script>
<template>
  <h1>Difference Composition API and Options API</h1>
  <button @click="addOne">Add</button>
  <span ref="result">count is:</span>
</template>

<script>
export default {
  data() {
    return {
      count : 0
    },
    methods: {
      addOne = function() {
        this.$refs.result.textContent = `count is: ${++this.count}`
      }
    }
  }
} 
</script>
<template>
  <h1>Composition Options API ref</h1>
  <button @click="addOne">Add</button>
  <span ref="result">count is:</span>
</template>

<script>
import { ref } from '@vue/reactivity';
export default {
  setup() {
    // state data
    const count = ref(0) // count 변수를 0으로 초기화

    // refs
    const result = ref(null) // null로 초기화 후 return하면서 span객체로 돌려줌

    // methods
    function addOne() {
      result.value.textContent = `count is: ${++count.value}`
    }
    return {
      count, result, addOne
    }
    </script> -->
<template>
  <h1>Composition Options API ref</h1>
  <button @click="addOne">Add</button>
  <span ref="result">count is:</span>
</template>

<script>
import { reactive, ref } from '@vue/reactivity';
export default {
  setup() {
    // 복수개의 변수를 하나의 변수로 하고자 할 때
    const state = reactive({
      count : ref(0)
    })

    const result = ref(null)

    function addOne() {
      result.value.textContent = `count is: ${++state.count}`
    }
    return {
      state, result, addOne
    }
  }
}

</script> -->

<style>

</style>