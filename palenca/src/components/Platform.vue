<template>
  <div class="w-5/6 mx-auto h-full">
    <section  class="mr-auto mb-8 relative text-center h-12 flex items-center text-lg">
        <img src="@/assets/Back.png" class="absolute left-0" alt="">
        <p>Select an app</p>
    </section>
    <div
        v-for="app in appOtions"
        :key="app.name"
        class="h-24"
        :style="{ backgroundColor: app.color }"
        >
        <img :src="app.icon" alt="">
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
              { 'name': 'Uber', 'color': 'black', icon: ''},
              { 'name': 'Rappi', 'color': '#E85B52', icon: ''},
              { 'name': 'Didi', 'color': '#EF8450', icon: ''},
              { 'name': 'Uber', 'color': 'black', icon: ''}
          ]
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
