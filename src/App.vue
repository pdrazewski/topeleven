<template>
  <div id="app">
    <div class="header">
      <div class="header_wrapper">
        <div class="logo"><router-link to="/">topeleven.pl</router-link></div>
        <div class="nav">
          <router-link to="/about">Jak to działa?</router-link>
          <router-link to="/selection">Selekcja</router-link>
          <router-link to="/subscribe">Subskrybuj</router-link>
        </div>
      </div>
    </div>
    <div class="content">
      <router-view/>
    </div>
    <div class="footer">
      © Copyright 2018.  <br>
        Noty podawane na stronie są wypadkową informacji zbieranych
        przez nas zespół z wielu źródeł oraz autorskiego systemu, który bierze pod uwagę
        między innymi przeliczania w oparciu o oficjalne ratio lig europejskich.
        <br>Zdajemy sobie sprawe ze `Nasza najlepsza jedenstka`` jest zebrana jedynie w oparciu o liczby i nie bierze pod uwagę
        wielu aspektów które sa tak istotne w profesjonalnym futbolu jak morale, umiejętnosci miekkie, 
        zaangazowanie, komunikacja, doswiadczenie zawodnikow, umiejetnosc realizacji zalozen taktycznych i inne.
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

export default class App extends Vue {
  sidenav: boolean = false

  toggleMenu() {
    // Correctly update the expected property.
    this.sidenav = !this.sidenav;
  }
}
</script>

<style lang="scss">
body {
  background: #fafafa;
  font-family: -apple-system, BlinkMacSystemFont, “Segoe UI”, Roboto, Helvetica, Arial, sans-serif
}
.logo {
  float: left;
    font-size: 30px;
    font-weight: bold;
    a {
      text-decoration: none;
      color: #000;
    }
    span {
      font-size: 12px;
      font-weight: normal;
    }
}
.header {
  position: relative;
  z-index: 2;
  &_wrapper {
    max-width: 1360px;
    margin: 0 auto;
    padding: 20px 0;
    overflow: hidden;
    clear: both;
    z-index: 10;
  }
}
.nav {
  float: right;
  padding: 9px 10px;
    a {
    font-weight: bold;
    color: #2c3e50;
    text-decoration: none;
    margin-left: 30px;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
.content {
  max-width: 1360px;
  clear: both;
  margin: 0 auto;
}
.footer {
  max-width: 1360px;
  margin: 0 auto;
  padding: 20px 100px;
  text-align: center;
  font-size: 12px;
  line-height: 21px;
  color: #777;
  clear: both;
  background: transparent;
}
</style>
