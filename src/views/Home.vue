<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
     
    <form id="search">
      Search <input name="query" v-model="searchQuery" />
    </form>
    <Grid
      :heroes="gridData"
      :columns="gridColumns"
      :filter-key="searchQuery"
    >
    </Grid>
    
  </div>
</template>

<script>
// @ is an alias to /src
import Grid from '@/components/Grid.vue'

export default {
  name: 'Home',
  data: function (){
    return {
    searchQuery: "",
    gridColumns: ["name", "power"],
    gridData: [
      { name: "Chuck Norris", power: Infinity },
      { name: "Bruce Lee", power: 9000 },
      { name: "Jackie Chan", power: 7000 },
      { name: "Jet Li", power: 8000 }
    ]
    }
  },
  components: {
    Grid
  }
}
</script>
