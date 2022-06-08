<template>
  <div id="app">
    <Header />
    <main>
      <Sidebar />
      <ShipsContainer />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Sidebar from "./components/Sidebar.vue";
import ShipsContainer from "./components/ShipsContainer.vue";

export default {
  name: "App",
  components: {
    Header,
    Footer,
    Sidebar,
    ShipsContainer,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:wght@300&family=Rajdhani:wght@300&display=swap");
#app {
  font-family: Rajdhani, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;

  display: flex;
  min-height: 100vh;
  flex-direction: column;
}

* {
  box-sizing: border-box;
}

body,
ul,
li,
h1,
h2,
p {
  padding: 0;
  margin: 0;
}

h2 {
  font-family: "IBM Plex Sans", Helvetica, Arial, sans-serif;
}
ul {
  list-style: none;
}
body {
  font-family: Arial, Helvetica, sans-serif;
  color: rgba(255, 255, 255, 0.4);
  background: linear-gradient(rgba(51, 10, 80, 0.6), black),
    url("./assets/background-body.jpg");
  background-position: 150px -30px;
  background-size: cover;
}
a {
  color: rgba(255, 255, 255, 0.4);
  text-decoration: none;
}
img {
  max-width: 100%;
  display: block;
}

main {
  display: flex;
  padding: 100px 200px 0;
  gap: 100px;
}

li,
a,
button,
input[type="checkbox"] {
  cursor: pointer;
}
</style>
