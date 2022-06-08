<template>
  <div>
      <h2>Ships</h2>            
      <div id="container">
        <div v-for="ship in ships" :key="ship.id">
          <Card :shipName="ship.shipName" 
          :owner="ship.owner" 
          :img="ship.img" 
          :level="ship.level" 
          :usprice="ship.usprice" 
          :spfy="ship.spfy"/>
        </div>
      </div>
  </div>
</template>

<script>
import ships from "../../public/ships.json"
import Card from "./Card.vue"
export default {
    name: "ShipsContainer",
    components: {
      Card
    },
    data(){
      return {
        ships: null
      }
    },
    created(){
      this.getShips()
    },
    methods: {
      getShips(){
        this.ships = ships
      }
    }
}
</script>

<style scoped>
  #container {
    min-width: 40vw;
    display: grid;
    gap: 50px;
    grid-template-columns: repeat(auto-fit, minmax(260px, auto));
  }

  h2 {
        text-align: left;
        color: #fff;
        margin-bottom: 15px;
        text-transform: uppercase;
    }
</style>