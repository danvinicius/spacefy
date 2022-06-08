<template>
  <div id="sidebar">
      <h2>Filters</h2>
      <div>
          <form action="" id="owner">
            <input type="text" placeholder="Search by owner">
            <button><i class="fa-solid fa-paper-plane"></i></button>
      </form>
      </div>
      
      <div id="level">
          <h3>Level</h3>
          <div class="level-container">
              <div class="level-box">
              <p>1</p>
              </div>
              <div class="level-box">
              <p>2</p>
              </div>
              <div class="level-box">
              <p>3</p>
              </div>
              <div class="level-box">
              <p>4</p>
              </div>
              <div class="level-box">
              <p>5</p>
              </div>
          </div>
          
      </div>
      <div class="horizontal-line">
          <div></div>
          <div></div>
          <div></div>
          <div></div>
          <div></div>
      </div>
      <hr>
      <div id="listing">
          <h3>Listing</h3>
          <form action="">
              <div>
                  <label for="fixed-price">
                  <div class="checkbox">
                    <input type="checkbox" id="fixed-price" >
                    <span class="check"></span>
                  </div>
                    Fixed Price
                </label>
              </div>
              <div>
                  <label for="action">
                    <div class="checkbox">
                    <input type="checkbox" id="action">
                    <span class="check"></span>
                    </div>
                Action
                </label>
              </div>
          </form>
      </div>
      <hr>
      <div id="payment">
          <h3>Payment</h3>
          <form action="">
              <div>
                  <label for="spfy">
                    <div class="checkbox">
                    <input type="checkbox" id="spfy">
                    <span class="check"></span>
                    </div>
                    SPFY
              </label>
              </div>
              <div>
                  <label for="eth">
                    <div class="checkbox">
                        <input type="checkbox" id="eth">
                        <span class="check"></span>
                    </div>
                ETH
              </label>
              </div>
              
          </form>
      </div>
      <hr>
      <div id="type">
          <h3>Type</h3>
          <form action="">
              <div>
                  <label for="ship">
                    <div class="checkbox">
                        <input type="checkbox" id="ship">
                        <span class="check"></span>
                    </div>
                    Ship
              </label>
              </div>
              <div>
                  <label for="planet">
                    <div class="checkbox">
                        <input type="checkbox" id="planet">
                        <span class="check"></span>
                    </div>
                    Planet
              </label>
              </div>
              <div>
                  <label for="item">
                        <div class="checkbox">
                        <input type="checkbox" id="item">
                        <span class="check"></span>
                        </div>
                    Item
              </label>
              </div>
              
          </form>
      </div>
      <hr>
      <div id="class">
          <h3>Class</h3>
          <form action="">
              <div>
                  <label for="Jawoks">
                        <div class="checkbox">
                        <input type="checkbox" id="Jawoks">
                        <span class="check"></span>
                        </div>
                    Jawoks
              </label>
              </div>
              <div>
                  <label for="Vorgs">
                    <div class="checkbox">
                    <input type="checkbox" id="Vorgs">
                    <span class="check"></span>
                    </div>
                    Vorgs
              </label>
              </div>
              <div>
                  <label for="Tangarions">
                    <div class="checkbox">
                    <input type="checkbox" id="Tangarions">
                    <span class="check"></span>
                    </div>
                Tangarions
              </label>
              </div>
              
          </form>
      </div>
  </div>
</template>

<script>
export default {
    name: "SideBar"
}
</script>

<style scoped>
    #sidebar {
        background: rgba(121, 70, 240, 0.4);
        padding: 20px 0;
        border: 2px solid #fff;
        box-shadow: 2px 0 15px rgb(139, 146, 247);
    }

    #sidebar > div {
        text-align: left;
        padding: 10px 20px;
    }

    h2 {
        text-align: left;
        margin-left: 20px;
        color: #fff;
        margin-bottom: 15px;
        text-transform: uppercase;
    }

    h3 {
        text-transform: uppercase;
        background-image: linear-gradient(to bottom, #9E3FDF, #A736DD);
        background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    .level-container {
        display: flex;
        gap: 5px;
        justify-content: space-between;
        padding-left: 20px;
    }

    .level-container p {
        color: #fff;
    }

    .level-box {
        position: relative;
    }

    .level-box::before {
        content: '';
        position: absolute;
        left: -15px;
        bottom: 0;
        background: #E08CE6;
        height: 25px;
        width: 10px;
        transform: rotate(-15deg) skewY(15deg);
    }

    .horizontal-line {
        width: 80%;
        height: 2px;
        background: rgba(255, 255, 255, .5);
        padding: 0 !important;
        margin: 10px 20px 30px;
        display: flex;
        justify-content: space-around;
    }

    .horizontal-line > div {
        height: 10px;
        width: 10px;
        border-radius: 50%;
        background: #fff;
        position: relative;
        bottom: 4px;
    }

    form#owner {
        position: relative;
    }

    form#owner input {
        background: rgba(142, 78, 226, 0.2);
        border-radius: 43px;
        outline: none;
        border: none;
        color: #fff;
        font-family: Rajdhani;
        padding: 16px;
        padding-right: 50px;
    }

    form#owner input::placeholder {
        font-family: Rajdhani;
        color: rgba(255, 255, 255, .9);
        text-transform: uppercase;
    }

    form#owner button {
        position: absolute;
        bottom: 0;
        top: 0;
        right: 0;
        color: #fff;
        background: linear-gradient(to right, #8E4EE2, #AE2FDB);
        outline: none;
        border: none;
        border-top-right-radius: 43px;
        border-bottom-right-radius: 43px;
        cursor: pointer;
        padding: 16px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 14px;

    }

    form > div {
        margin-bottom: 10px;
    }

    .checkbox {
        display: inline;
        width: 10px;
        height: 40px;
        background: linear-gradient(86.26deg, #9746E1 -30.72%, #A637DD 227.34%);
        clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
        transform: rotate(90deg);
        cursor: pointer;
        margin-right: 5px;
        margin-bottom: 20px;
        position: relative;
    }

    .checkbox .check {
        width: 5px;
        height: 10px;
        border: 1px solid transparent;
        border-bottom-color: #fff;
        border-right-color: #fff;
        position: absolute;
        top: 3px;
        left: 8px;
        transform: rotate(45deg);
        display: none;
    }

    .checkbox input:checked + .check {
        display: block;
    }

    input[type="checkbox"] {
        opacity: 0;
        position: relative;
    }

    hr {
        height: 1px;
        border: 1px solid rgba(255, 255, 255, .5);
    }

</style>