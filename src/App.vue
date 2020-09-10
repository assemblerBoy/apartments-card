<template>
  <div id="app">
      <v-app>
        <div class="app-wrapper d-flex flex-row justify-space-around flex-wrap">
          <ApartmentCard 
            :data="item" 
            v-for="item in items"  
            :key="item.id">
          </ApartmentCard>
        </div>
      </v-app>
  </div>
</template>

<script>
  import ApartmentCard from './components/ApartmentCard'

  export default {
      name: 'App',
      components: {
        ApartmentCard      
      },
      data() {
        return {
          items: []
        }
      },
      async mounted() {
        let data =  await this.axios.get('http://localhost:3000/response')
        this.items = data.data
      }
    }

</script>

<style scoped>
  .app-wrapper {
    padding-top: 50px;
  }
</style>
