<template>
  <h1>{{ msg }}</h1>
  <button @click="state.count++">count is: {{ state.count }}</button>
  <p>
    Edit <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>
</template>

<script>
import { reactive } from 'vue'
export default {
  props: {
    msg: String,
  },
  setup() {
    const state = reactive({
      count: 0,
      name: 'josh mu',
    })

    return {
      state,
    }
  },
}
</script>
