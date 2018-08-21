<template>
  <div>
    <button @click="isShown = !isShown">Toggle</button>
    <p v-if="isShown">Use V-If</p>
    <p v-else>Use Else If</p>
    <hr>
    <p v-show="isShown">Use V-Show</p>
    <p v-show="!isShown">Use V-Show Opposite</p>
    <hr>
    <ul>
      <li v-for="(fruit,index) in fruits">{{ index }} {{ fruit }}</li>
    </ul>
    <hr>
    <ul>
      <ol v-for="(value,keyName, index) in library">{{ value }} - {{ keyName }} - {{ index }}</ol>
    </ul>
    <hr>
    <ul>
      <li v-for="value in dataObj">
        {{ value }}
        <hr>
        <template v-if="Array.isArray(value)">
          <div v-for="element in value">{{ element }}</div>
        </template>
        <template v-else>{{ value }}</template>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isShown: true,
      fruits: ['mango','durian','barimbing','pisang'],
      library: {
        title: 'Lord Of The Rings',
        author: 'JRR Tolkiens',
        books: 3
      },
      dataObj: {
        name: 'Test Object',
        id: 10,
        data: [1.67, 1.33, 0.98, 2.21]
      }
    }
  },
  methods: {

  },
  computed: {

  },
  watch: {

  }
}
</script>

<style>

</style>
