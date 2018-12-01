<template>
  <div class="home">
    <img alt="Vue logo" class="logo" src="../assets/logo2.png">
    <FootballPitch msg="Welcome to Your Vue.js + TypeScript App"/>
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
.logo {
  position: absolute;
  top: 20px;
  left: 20px;
  max-width: 200px;
}
</style>
