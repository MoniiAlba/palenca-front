<template>
  <div id="app">
    <component
        :is="componentSelected"
        @nextStep="stepNumber = stepNumber + 1"
        />
  </div>
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    Home
  },
  data () {
      return {
          stepNumber: 0
      }
  },
  computed: {
      componentSelected () {
          if (this.stepNumber === 0) return () => import('@/components/Home.vue')
          if (this.stepNumber === 1) return () => import('@/components/Platform.vue')
          return () => import('@/components/Platform.vue')
      }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 16px;
}
</style>
