<template>
    <div class="calculator">
        <div class="display">display</div>
        <div class="btn">Clear</div>
        <div class="btn">+/-</div>
        <div class="btn">%</div>
        <div class="btn operator">/</div>
        <div class="btn">7</div>
        <div class="btn">8</div>
        <div class="btn">9</div>
        <div class="btn operator">x</div>
        <div class="btn">4</div>
        <div class="btn">5</div>
        <div class="btn">6</div>
        <div class="btn operator">-</div>
        <div class="btn">1</div>
        <div class="btn">2</div>
        <div class="btn">3</div>
        <div class="btn operator">+</div>
        <div class="zero btn">0</div>
        <div class="btn">.</div>
        <div class="btn operator">=</div>


    </div>
</template>

<script>
export default {};
</script>

<style scoped>

.calculator {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(50px, auto);
}
.display{
    display: flex;
    align-items: flex-end;
    justify-content: flex-end;
    grid-column: 1/-1;
    background-color: rgb(182, 196, 211);
    border: 1px solid black;
}

.zero{
    grid-column: 1/3;
}

.btn{
    display:flex;
    align-items: center;
    justify-content: center;
    background-color:  #eee;
    border: 1px solid black;
}

.operator{
    background-color:orange;
    color: white
}
</style>