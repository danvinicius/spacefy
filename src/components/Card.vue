<template>
  <div class="card-container">
      <div class="title">
          <h3>{{shipName}}</h3>
          <div v-if="rarity" class="rarity">
              <span></span>
            <p>Rarity Item</p>
          </div>
      </div>
          
          <p id="owner">Owner: {{owner}}</p>
          <div class="card">
            <div class="upper-container">
              <div class="level-container">
                  <span class="level">LVL {{level}}</span>
              </div>
              <div class="img-container">
                <img :src="img" :alt="shipName">
              </div>
            </div>
            <div class="price-container">
                <p class="price">US$ {{usprice | useComma}}</p>
                <div class="diamond"></div>
                <span class="spfy">{{spfy | useSPFY}} SPFY</span>
              </div>
          </div>
        </div>
</template>

<script>

export default {
    props: {
        shipName: String,
        owner: String,
        img: String,
        level: Number,
        usprice: Number,
        spfy: Number,
        rarity: Boolean
    },
    filters: {
        useComma: function(number) {
            return number.toString().replace(".", ",")
        },
        useSPFY: function(number) {
            return number.toLocaleString("pt-br", {style: "currency", currency: "BRL", maximumSignificantDigits: 4}).replace("R$", "").replace(",",".")
        }
    }
}
</script>

<style scoped>
.card {
    background: #1E1827;
    border-radius: 10px;
    border: 1px solid rgba(255, 255, 255, .5);
}

.upper-container {
    background-image: linear-gradient(rgba(49, 26, 67, .4), rgba(49, 26, 67, .4)), url("../assets/nebula.png");
    background-position: center center;
    background-size: cover;
    border-radius: 11px;
    padding: 15px;
    display: flex;
    gap: 25px;
    border: 1px solid rgba(255, 255, 255, .5);
}

.img-container {
    transform: rotate(15deg);
}

.img-container img {
    max-width: 150px;
}


h3 {
    text-align: left;
    color: #fff;
    margin-bottom: 15px;
    text-transform: uppercase;
    position: relative;
}

h3::after, h3::before {
    content: '';
    height: 4px;
    width: 25px;
    background: #6D2CAE;
    position: absolute;
    left: 0;
}

h3::after {
    top: -10px;
}

h3::before {
    bottom: -10px;
}

.title {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.title .rarity p {
    text-align: left;
    margin: 20px 0;
    text-transform: uppercase;
    font-weight: bold;
}

.rarity {
    display: flex;
    align-items: center;
}

.rarity span {
    display: block;
    width: 15px;
    height: 15px;
    border: 2px solid transparent;
    border-top-color: rgb(139, 146, 247);
    border-left-color: rgb(139, 146, 247);
    transform: rotate(45deg);
    margin-right: 10px;
    margin-top: 10px;
    position: relative;
}

.rarity span::before {
    content: '';
    width: 3px;
    height: 3px;
    position: absolute;
    top: 30%;
    left: 30%;
    background: rgb(139, 146, 247);
    box-shadow: 0 0 3px rgb(139, 146, 247);
}

.level-container {
    height: 75px;
    width: 150px;
    background: linear-gradient(to right, rgba(211, 28, 227, .2), transparent);
    border-top: 1px solid #CCDFF6;
    border-left: 1px solid #CCDFF6;
    border-bottom: 1px solid #CCDFF6;
    text-align: left;
    margin-bottom: 15px;
    text-transform: uppercase;
    font-style: italic;
    font-weight: bold;
    padding: 10px 0 0 15px;
    font-family: 'IBM Plex Sans';
    position: relative;
}

.level-container::before {
    content: '';
    height: 0;
    width: 0;
    border: 5px solid transparent;
    border-bottom-color: #fff;
    position: absolute;
    top: -5px;
    left: -5px;
    transform: rotate(-45deg);
}


.price-container {
    padding: 15px 20px;
    text-align: left;
}

.price {
    color: rgba(255, 255, 255, .6);
    font-weight: bold;
}

.spfy {
    color: #fff;
    letter-spacing: 3px;
    font-size: 20px;
    font-weight: bold;
    display: inline-block;
    padding-left: 5px;
    padding-top: 5px;
}

.diamond {
    clip-path: polygon(0% 70%, 50% 0%, 100% 70%, 50% 100%); 
    height: 15px;
    width: 10px;
    background: linear-gradient(161.57deg, #7D24DD -8.33%, #D31CE3 92.71%);
    display: inline-block;
}


#owner {
    text-align: left;
    margin: 20px 0;
    text-transform: uppercase;
    font-weight: bold;
}

</style>