<template>
  <div class="cms about">
    <div class="cms_content">
      <h1 class="cms_title">
        Selekcja - czyli obserwowani gracze.
      </h1>
      <div class="cms_text">
        <h2>Kim jestesmy?</h2>
        Noty podawane na stronie są wypadkową informacji zbieranych przez nas zespół z wielu źródeł oraz autorskiego systemu, który bierze pod uwagę między innymi przeliczania w oparciu o oficjalne ratio lig europejskich. <br> <br>
Zdajemy sobie sprawe ze `Nasza najlepsza jedenstka`` jest zebrana jedynie w oparciu o liczby i nie bierze pod uwagę wielu aspektów które sa tak istotne w profesjonalnym futbolu jak morale, umiejętnosci miekkie, zaangazowanie, komunikacja, doswiadczenie zawodnikow, umiejetnosc realizacji zalozen taktycznych i inne.
      <h2>Skad pomysl?</h2>
        Noty podawane na stronie są wypadkową informacji zbieranych przez nas zespół z wielu źródeł oraz autorskiego systemu, który bierze pod uwagę między innymi przeliczania w oparciu o oficjalne ratio lig europejskich. <br> <br>
Zdajemy sobie sprawe ze `Nasza najlepsza jedenstka`` jest zebrana jedynie w oparciu o liczby i nie bierze pod uwagę wielu aspektów które sa tak istotne w profesjonalnym futbolu jak morale, umiejętnosci miekkie, zaangazowanie, komunikacja, doswiadczenie zawodnikow, umiejetnosc realizacji zalozen taktycznych i inne.
<h2>Skad czerpiemy skladowe oceny?</h2>
        Noty podawane na stronie są wypadkową informacji zbieranych przez nas zespół z wielu źródeł oraz autorskiego systemu, który bierze pod uwagę między innymi przeliczania w oparciu o oficjalne ratio lig europejskich. <br> <br>
Zdajemy sobie sprawe ze `Nasza najlepsza jedenstka`` jest zebrana jedynie w oparciu o liczby i nie bierze pod uwagę wielu aspektów które sa tak istotne w profesjonalnym futbolu jak morale, umiejętnosci miekkie, zaangazowanie, komunikacja, doswiadczenie zawodnikow, umiejetnosc realizacji zalozen taktycznych i inne.
      </div>
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
export default class Home extends Vue {}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.cms {
  max-width: 1360px;
  margin: 0 auto;
  &_content {
    max-width: 860px;
    margin: 20px auto;
    .cms_title {
      font-size: 34px;
      font-weight: bold;
      text-align: center;
      padding: 20px 0;
    }
    .cms_text {
      text-align: left;
      line-height: 26px;
      font-size: 16px;
      padding-bottom: 15px;
    }
  }
}
</style>
