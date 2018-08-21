<template>
  <div>
    <div>
      <p>Current Value : {{ value }}</p>
      <button @click="value += 5">Add 5</button>
      <button @click="value += 1">Add 1</button>
      <input type="text" placeholder="Set Timer" v-model="timer">
      <p>{{ checkValue }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value: 0,
      timer: 0
    }
  },
  computed: {
    checkValue() {
      return this.value == 37 ? 'Done' : 'Not Yet'
    }
  },
  watch: {
    checkValue() {
      setTimeout(() => {
        this.value = 0
      }, this.timer)
    }
  }
}
</script>

<style>
</style>
