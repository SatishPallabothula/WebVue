<template>
  <div class="container">
    <HeaderTop Name="Car Rental Information" />

    <Box :Rental="Rental" />

</div>
</template>

<script>

import HeaderTop from './components/HeaderTop.vue'
import Box from './components/Box.vue'

export default {
  name: 'App',
  components: {    
    HeaderTop,
    Box
  },

  data(){
    return {
      Rental: []
    }

  },

methods: {

  // promises

    async fetchRental(){
      const res = await fetch('https://vuewebdatabase.herokuapp.com/api')
     //const res = await fetch('http://localhost:5959/Rental')
        const data= await res.json()
        console.log(data)
        return data.RENTAL
    }


},
async created(){
  this.Rental = await this.fetchRental()
}
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}

div{
  margin-bottom: 0.5em;
  padding:10px;
}

</style>