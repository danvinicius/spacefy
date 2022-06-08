<template>
  <header>
      <nav id="nav">
        <div id="logo">
            <img src="../assets/spacefy-logo.png" alt="">
        </div>
          <ul>
              <li><a href="#">Play Game</a></li>
              <li class="active"><a href="#">Marketplace</a></li>
              <li><a href="#">Stake</a></li>
              <li><a href="#">Contact</a></li>
          </ul>
      </nav>
      <div id="connect-button">
          <a href="#">
              <img src="../assets/butaoroxo.png" alt="">
              <span>Connect Wallet</span>
          </a>
      </div>
  </header>
</template>

<script>
export default {
    name: "Header"
}
</script>

<style scoped>
    header {
        position: absolute;
        top: 0;
        width: 100%;
        display: flex;
        justify-content: space-between;
        padding: 0 200px;
        background-image: linear-gradient(to top, rgba(50, 12, 87, .6), rgba(8, 21, 30, .6));
    }

    header::after, header::before {
                
        content: '';
        height: 4px;
        width: 200px;
        background: #6D2CAE;
        position: absolute;
        bottom: 0;
    }

    header::after {
        right: 0;
    }

    header::before {
        left: 0;
    }

    nav {
        display: flex;
    }

    nav #logo {
        padding-top: 20px;
        padding-right: 50px;
    }

    nav #logo img {
        width: 100px;
    }

    nav ul {
        display: flex;
    }

    nav ul li {
        display: block;
        background: #34214C;
        padding: 40px 50px;
        transform: skew(-20deg);
        margin-right: 5px;
    }

    nav ul li a {
        transform: skew(20deg);
    }

    nav ul li:hover, .active {
        background: #130324;
    }

    nav ul li a {
        display: block;
        color: #fff;
        font-weight: bold;
        position: relative;
    }

    nav ul li:hover a::after, .active a::after {
        content: '';
        width: 30px;
        height: 4px;
        background: #6D2CAE;
        position: absolute;
        bottom: -10px;
        left: 50%;
        transform: translate(-50%, 0);
    }

    #connect-button {
        display: flex;
        align-items: center;
        position: relative;
    }

    #connect-button a img {
        width: 200px;
    }

    #connect-button a span {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        z-index: 10;
        color: #fff;
        text-transform: uppercase;
        font-weight: bold;
        font-size: 14px;
    }
</style>