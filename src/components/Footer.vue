<template>
  <footer>
      <div id="img-copyright">
          <img src="../assets/spacefy-logo.png" alt="">
          <p>2022 Spacefy Game. All rights reserved</p>
      </div>
      <div id="links">
          <h4>Links</h4>
          <ul>
              <li>Whitepaper</li>
              <li>Pickdeck</li>
          </ul>
      </div>
      <div id="sitemap">
          <h4>Sitemap</h4>
          <ul>
              <li>Marketplace</li>
              <li>Stake</li>
          </ul>
      </div>
      <div id="contact">
          <h4>Our community</h4>
          <ul>
              <li><div><i class="fa-brands fa-instagram"></i></div> </li>
              <li><div><i class="fa-brands fa-twitch"></i></div> </li>
              <li><div><i class="fa-brands fa-twitter"></i></div> </li>
              <li><div><i class="fa-brands fa-telegram"></i></div> </li>
              <li><div><i class="fa-solid fa-envelope"></i></div> </li>
          </ul>
      </div>
  </footer>
</template>

<script>
export default {
    name: "Footer"
}
</script>

<style scoped>
footer {
    display: flex;
    justify-content: space-around;
    padding: 50px 200px 50px 100px;
    position: relative;
    top: 210px;
    left: 0;
    width: 100%;
    background: linear-gradient(rgba(66, 13, 105, .4), rgba(66, 13, 105, .4)), url('../assets/footer-background.jpg');
}
    #img-copyright {
        display: flex;
        flex-direction: column;
        gap: 15px;
    }
    footer #img-copyright img {
        width: 150px;
    }

    footer div ul li {
        line-height: 3;
        font-weight: bold;
    }

    p, li, a {
        color: #fff;
    }
    #contact {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
    }
    #contact ul {
        display: flex;
        gap: 15px;
    }
    #contact ul li div {
        height: 40px;
        width: 40px;
        border-radius: 10px;
        background: rgba(70, 22, 110, .4);
        
    }
    footer::after {
        content: '';
        width: 1px;
        background: rgba(136, 131, 141, .28);
        position: absolute;
        top: 0;
        bottom: 0;
        left: 65%;
    }
    h4 {
        text-transform: uppercase;
    }
</style>