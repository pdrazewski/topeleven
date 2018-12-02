<template>
    <div class="kit">
        <span class="front">
            <span class="neck"></span>
            <span class="neck_overlay"></span>
            <span class="pattern"></span>
            <span class="badge"></span>
            <span class="rate"> {{ rate }} </span>
        </span>
        <span class="sleeve sleeve-r"></span>
        <span class="sleeve sleeve-l"></span>
        <span class="name">{{ name }}</span>
    </div>
</template>
<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Player extends Vue {
  @Prop() private name!: string;
  
  @Prop() private rate!: string;
}
</script>
<style scoped lang="scss">

$kit-width: 180px;
$kit-height: 200px;

.kit {
    width: $kit-width;
    height: $kit-height;
    margin: 10px 5px;
    position: relative;
    overflow: hidden;
    display: inline-block;
    &:after {
        display: block;
        content: "";
        width: 100px;
        height: 20px;
        box-shadow: 11px 20px 50px rgba(0, 0, 0, 0.3);
        position: absolute;
        bottom: 54px;
        left: 36px;
    }
}
.rate {
    position: absolute;
    top: 60px;
    width: 100%;
    text-align: center;
    font-size: 30px;
    letter-spacing: -0.5px;
    font-weight: bold;
    z-index: 4;
}
.front {
    width: $kit-width/2;
    height: ($kit-height)-50;
    left: 45px;
    z-index: 2;
    overflow: hidden;
    border-radius: 0 5px 5px;
    background-color: #f6f6f6;
}
span {
    display: block;
    position: absolute;
    box-sizing: border-box;
}
.neck {
    width: 0;
    height: 0;
    border-left: 20px solid transparent;
    border-right: 20px solid transparent;
    border-top: 16px solid #ccac00;
    top: 0px;
    left: 25px;
    border-top-color: red;
    position: relative;
}
.pattern {
    width: 0;
    height: 0;
    border-left: 145px solid transparent;
    border-bottom: 186px solid #ececec;
    top: 10px;
    right: 0;
    position: absolute;
    z-index: 1;
}
.badge {
    width: 15px;
    height: 15px;
    background-color: red;
    right: 10px;
    opacity: 0.5;
    z-index: 2;
    position: absolute;
    top: 25px;
}
.neck_overlay {
    width: 0;
    height: 0;
    border-left: 20px solid transparent;
    border-right: 20px solid transparent;
    border-top: 16px solid #ccac00;
    top: -20px;
    left: 25px;
    border-top-color: #f6f6f6;
    position: relative;
}
.sleeve-r {
    left: 108px;
    transform: rotate(-55deg);
    border-right: 4px solid transparent;
}

.sleeve {
    width: 50px;
    height: 60px;
    background: #f6f6f6;
    z-index: 1;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
.sleeve-l {
    left: 20px;
    transform: rotate(55deg);
    border-left: 4px solid transparent;
}
.name {
    position: absolute;
    bottom: 0;
    width: 100%;
    text-align: center;
    text-transform: capitalize;
    font-size: 28px;
    color: #fff;
}
</style>
