<template>
  <div>
    <div>
      <button @click="startEffect">Start Effect</button>
      <br><br>
      <div id="effect" :class="effectClasses"></div>
    </div>
    <hr>
    <div :class="[]">I got no class :(</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      effectClasses:{
        highlight: false,
        shrink: true
      }
    }
  },
  methods: {
    startEffect() {
      setInterval(() => {
        this.effectClasses.highlight = !this.effectClasses.highlight
        this.effectClasses.shrink = !this.effectClasses.shrink
      },1000)
    }
  },
  computed: {

  },
  watch: {

  }
}
</script>

<style>
  #effect {
    width: 100px;
    height: 100px;
    border: 1px solid black;
  }
  .highlight {
    background-color: red;
    width: 200px !important;
  }
  .shrink {
      background-color: grey;
      width: 50px !important;
  }
  .blue {
    background-color: blue;
  }
  .float {
    float: right;
  }
  .text-color {
    color: yellow;
  }
</style>
