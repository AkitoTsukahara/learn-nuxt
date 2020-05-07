<template>
  <div class="container">
    <Counter></Counter>
    <hr>
    <Counter></Counter>
    <hr>
    <Counter></Counter>
    <hr>
  </div>
</template>

<script>
import Counter from '~/components/Counter.vue'

export default {
  components: {
    Counter
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: block;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
