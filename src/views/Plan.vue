<template>
  <div class="about">
    <div class="lead">
      <h1>Jak to działa?</h1>
      <p>
          - abonament 9,9 pln
            - trendy formy per zawodnik (najwiekszy skok not w gore, najwiekszy spadek)
            - trend formy kadry
            - dopasowania kadry - per liga / per wiek / per ustawienie
            - powiadomienia o zmianach
      </p>
      <p>
          - abonament 29,90 pln
            - dodawanie swoich zawodnikow
            - tworzenie wlasnej kadry
            - wlasne rankingi
            - udostepnianie rankingow / ocen po meczu
      </p>
    </div>
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
export default class Plan extends Vue {}
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
</style>
