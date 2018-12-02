<template>
  <div class="home">
    <div class="header">
      <div class="hamburger">
        <div class="spinner"></div>
        <div class="spinner"></div>
        <div class="spinner"></div>
      </div>
      <div class="logo">topeleven.pl <span>...the best by the numbers</span></div>
    </div>
    <div class="lead">
      <h1>Nasza najlepsza jedenastka</h1>
      <p>Według not, rankingów oraz opinii zebranych z
        dziesiątek serwisów branzowych, opinii influencerów, for fanclubów</p>
      <a href="#">Dowiedz się jak zbieramy infmoracje</a>
      <p class="subs">Chcesz otrzymywac powiadomienie mailowe po
        kazdej aktualizacji rankingu? zapisz sie juz teraz.</p>
        <div>
           <input type="text">
           <button type="submit">Zapisz mnie</button>
        </div>
    </div>
    <FootballPitch style="width:60%;padding: 0 50px; right: 0" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import FootballPitch from '@/components/FootballPitch.vue'; // @ is an alias to /src

@Component({
  components: {
    FootballPitch,
  },
})
export default class Home extends Vue {}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.lead {
  position: absolute;
  max-width: 500px;
  top: 100px;
  left: 45px;
  text-align: left;
  h1 {
    font-size: 50px;
  }
  p {
    line-height: 26px;
    font-size: 16px;
    margin-top: -15px;
  }
  a {
    background: darkgreen;
    padding: 15px;
    border-radius: 3px;
    margin: 10px 0;
    display: block;
    max-width: 350px;
    color: #fff;
    text-align: center;
    text-decoration: none;
  }
  .subs {
    margin-top: 20px;
    font-size: 13px;
    line-height: 22px;
    color: #777;
  }
}
.logo {
  float: left;
  margin-left: 30px;
    font-size: 30px;
    font-weight: bold;
    span {
      font-size: 12px;
      font-weight: normal;
    }
}
.header {
  clear: both;
  overflow: hidden;
  position: relative;
  z-index: 100;
  padding: 20px;
}
.hamburger {
    height: 40px;
    width: 33px;
    margin: 0 0 0 44px;
    cursor: pointer;
    float: left;
    position: relative;
     left: -20px;
    .spinner {
    margin: 8px 0 0;
    height: 2px;
    width: 100%;
    background: #000;
    -webkit-transition: background .3s;
    transition: background .3s;
    }
}
.nav {
  float: right;
  margin-right: 20px;
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
</style>
