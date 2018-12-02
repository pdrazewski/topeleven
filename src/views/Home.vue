<template>
  <div class="home">
    <div class="lead">
      <h1>Nasza najlepsza jedenastka</h1>
      <p>Według not, rankingów oraz opinii zebranych z
        dziesiątek serwisów branzowych, opinii influencerów, for fanclubów</p>
      Dowiedz się jak zbieramy infmoracje
    </div>
    <FootballPitch class="footballPitch" />
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
  float: left;
  width: 40%;
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
.footballPitch {
  float: right;
  width: 60%;
}
</style>
