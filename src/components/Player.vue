<template>
    <div class="kit">
        <span class="front">
            <span class="neck"></span>
            <span class="badge"></span>
            <span class="brand"></span>
            <span class="sponsor"></span>
        </span>
        <span class="sleeve sleeve-r"></span>
        <span class="sleeve sleeve-l"></span>
        <span class="name">Kowalski</span>
    </div>
</template>
<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Player extends Vue {
  @Prop() private msg!: string;
}
</script>
<style scoped lang="scss">
.kit {
    width: 180px;
    height: 200px;
    margin: 10px 5px;
    position: relative;
    overflow: hidden;
    display: inline-block;
}
.front {
    width: 90px;
    height: 150px;
    left: 45px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    z-index: 2;
    border-top: 8px solid transparent;
    border-bottom: 5px solid transparent;
    background-color: #f6f6f6;
    border-top: 2px solid #1e1e20;
    border-bottom: 5px solid rgba(221, 221, 221, 0.3);
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
.badge {
    width: 15px;
    height: 15px;
    background: gold;
    opacity: 0.5;
    background-color: white;
    right: 15px;
    top: 25px;
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
    border-color: #1e1e20;
    border-width: 2px;
    z-index: 1;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}
.sleeve:after {
    content: '';
    width: 100%;
    height: 10px;
    display: block;
    position: absolute;
    bottom: 0;
    border-bottom: 5px solid rgba(18, 18, 19, 0.15);
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
    font-size: 30px;
    font-family: arial;
    font-weight: bold;
    color: #fff;
}
</style>
