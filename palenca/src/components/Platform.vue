<template>
  <div class="w-5/6 mx-auto h-full">
    <section  class="mr-auto mb-8 relative text-center h-12 flex items-center text-lg">
        <img src="@/assets/Back.png" class="absolute left-0" alt="" @click="$emit('back')">
        <p class="w-full">Select an app</p>
    </section>
    <div
        v-for="app in appsOptions"
        :key="app.name"
        class="h-24 rounded-2xl my-4 text-white flex items-center font-bold px-4"
        :style="{ backgroundColor: app.color }"
        >
        <img :src="getImgUrl(app.icon)" alt="" class="mr-2">
        {{ app.name }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'Platform',
  data () {
      return {
          // this may be an endpoint answer
          appsOptions: [
              { 'name': 'Uber', 'color': 'black', icon: 'uber.png' },
              { 'name': 'Rappi', 'color': '#E85B52', icon: 'rappi.png' },
              { 'name': 'Didi', 'color': '#EF8450', icon: 'didi.png' },
              { 'name': 'McDonalds', 'color': '#D22D1F', icon: 'mcd.png' },
              { 'name': 'Starbucks', 'color': '#2A6245', icon: 'starbucks.png' }
          ]
      }
  },
  methods: {
      getImgUrl(pic) {
        return require('../assets/'+pic)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
  color: #2772F0;
}
</style>
