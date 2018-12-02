<template>
    <div class="stage">
        <div class="world">
            <div class="terrain">
                <div class="field field--alt"></div>
                <div class="field ground">
                    <div class="field__texture field__texture--gradient"></div>
                    <div class="field__texture field__texture--grass"></div>
                    <div class="field__line field__line--goal"></div>
                    <div class="field__line field__line--goal field__line--goal--far"></div>
                    <div class="field__line field__line--outline"></div>
                    <div class="field__line field__line--penalty"></div>
                    <div class="field__line field__line--penalty-arc"></div>
                    <div class="field__line field__line--penalty-arc field__line--penalty-arc--far">
                    </div>
                    <div class="field__line field__line--mid"></div>
                    <div class="field__line field__line--circle"></div>
                    <div class="field__line field__line--penalty field__line--penalty--far"></div>
                </div>
            </div>
        </div>
        <Player rate="7,65" name="Szczesny" class="p1" />
        <Player rate="6,32" name="Rybus" class="p2" />
        <Player rate="6,4" name="Kamiński" class="p3" />
        <Player rate="6,1" name="Cionek" class="p4" />
        <Player rate="6,7" name="Bereszyński" class="p5" />
        <Player rate="6,4" name="Zieliński" class="p6"  />
        <Player rate="6,46" name="Krychowiak" class="p7"  />
        <Player rate="6,23" name="Klich" class="p8" />
        <Player rate="6,1" name="Grosicki" class="p9" />
        <Player rate="7,36" name="Piątek" class="p10" />
        <Player rate="7,25" name="Lewandowski" class="p11" />
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import Player from '@/components/Player.vue'; // @ is an alias to /src

@Component({
  components: {
    Player,
  },
})

export default class FootballPitch extends Vue {}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.stage {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  perspective-origin: 50% -300px;
  perspective: 1100px;
  z-index: 1;
  backface-visibility: hidden;
}
.world {
  position: absolute;
  top: 0;
  left: 50%;
  margin-left: -336px;
  width: 672px;
  height: 840px;
  transform: translateZ(-210px);
  transform-style: preserve-3d;
  z-index: 1;
  backface-visibility: hidden;
}
.terrain {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  transform-style: inherit;
}
.field {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: #eee;
  z-index: 2;
  transform: rotateX(90deg) translateZ(0);
  transform-origin: 50% 50%;
  box-sizing: content-box;
  backface-visibility: hidden;
}
.field--alt {
  display: block;
  width: 80%;
  left: 10%;
  transform: rotateX(90deg) translateZ(-20px);
  background: #000;
  opacity: 0.3;
  box-shadow: 0 0 40px 30px #000;
}
.field__texture {
  width: 100%;
  height: 100%;
  position: absolute;
  z-index: 3;
}
.field__texture.field__texture--gradient {
  background-image: linear-gradient(to top, rgba(0,0,0,0.2), transparent);
  z-index: 4;
}
.field__texture.field__texture--grass {
  background-image: url("http://textures101.com/textures/Nature/Grass/2012/1/15/tn1_4182507849028a2df3c2o_kkwbe.jpg");
  background-repeat: repeat;
  background-size: 100px 100px;
}
.field__line {
  position: absolute;
  width: 100%;
  height: 3px;
  z-index: 4;
}
.field__line--goal {
  width: 16%;
  height: 6%;
  border: solid 2px rgba(255,255,255,0.9);
  border-bottom: none;
  left: 0;
  right: 0;
  margin: auto;
  bottom: 4%;
}
.field__line--goal--far {
  top: 4%;
  bottom: auto;
  border: solid 2px rgba(255,255,255,0.9);
  border-top: none;
}
.field__line--penalty-arc {
  width: 20%;
  height: 20%;
  overflow: hidden;
  bottom: 20%;
  left: 0;
  right: 0;
  margin: auto;
}
.field__line--penalty-arc:after {
  position: absolute;
  top: 75%;
  width: 100%;
  height: 100%;
  left: 0;
  content: ' ';
  display: block;
  border-radius: 50% 50% 0 0;
  border: solid 2px rgba(255,255,255,0.9);
  border-bottom: none;
  box-sizing: border-box;
}
.field__line--penalty-arc--far {
  bottom: auto;
  top: 20%;
}
.field__line--penalty-arc--far:after {
  bottom: 75%;
  top: auto;
  border: solid 2px rgba(255,255,255,0.9);
  border-top: none;
  border-radius: 0 0 50% 50%;
}
.field__line--penalty {
  width: 44%;
  height: 16%;
  border: solid 2px rgba(255,255,255,0.9);
  border-bottom: none;
  left: 0;
  right: 0;
  margin: auto;
  bottom: 4%;
}
.field__line--penalty--far {
  top: 4%;
  bottom: auto;
  border: solid 2px rgba(255,255,255,0.9);
  border-top: none;
}
.field__line--outline {
  width: 92%;
  height: 92%;
  top: 4%;
  left: 4%;
  border: solid 2px rgba(255,255,255,0.9);
}
.field__line--mid {
  top: 50%;
  width: 92%;
  left: 4%;
  background-color: rgba(255,255,255,0.9);
}
.field__line--circle {
  width: 20%;
  height: 20%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  margin: auto;
  border: solid 2px rgba(255,255,255,0.9);
  border-radius: 50%;
}

.kit {
    transform: scale(0.44);
    position: absolute;
    z-index: 100;
}
.p1 {
    top: 420px;left: 410px;
}
.p2 {
    top: 350px;left: 180px;
}
.p3 {
    top: 350px;left: 320px;
}
.p4 {
    top: 350px;left: 490px;
}
.p5 {
    top: 350px;left: 640px;
}
.p6 {
    top: 220px;left: 180px;
}
.p7 {
    top: 220px;left: 320px;
}
.p8 {
    top: 220px;left: 490px;
}
.p9 {
    top: 220px;left: 640px;
}
.p10 {
    top: 90px;left: 320px;
}
.p11 {
    top: 90px;left: 490px;
}

</style>
