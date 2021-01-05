<template>
  <main class="content">
    <p v-if="isLoading">Loading...</p>
    <div v-if="data">
      <Chart />
      <pre>{{ JSON.stringify(data, null, 2) }}</pre>
    </div>
    <p v-if="error">{{ error }}</p>
  </main>
</template>

<script>
import { onMounted, ref } from 'vue'
import db from '../../db.json'
import Chart from './Chart.vue'

export default {
  components: {
    Chart,
  },
  setup() {
    const data = ref(null)
    const isLoading = ref(false)
    const error = ref(null)

    const fetchData = async () => {
      isLoading.value = true

      try {
        // const placeholder = 'http://jsonplaceholder.typicode.com/posts'
        // const production = 'https://mu-ceb-api.herokuapp.com/'
        // const res = await fetch(production)
        // console.log(res)
        // const d = await res.json()
        // data.value = await res.json()

        console.log({ db })
        data.value = db
      } catch (err) {
        console.error(err)
        error.value = err
      }

      isLoading.value = false
    }

    onMounted(() => {
      fetchData()
    })

    return {
      data,
      isLoading,
      error,
    }
  },
}
</script>

<style lang="scss" scoped>
@import '../styles/variables.scss';

.content {
  border-right: 1px solid rgba(255, 255, 255, 0.5);
  flex: 1;
}
</style>
