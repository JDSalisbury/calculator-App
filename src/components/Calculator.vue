<template>
    <div class="calculator">
        <div class="display">{{current || '0'}}</div>
        <div @click="clear" class="btn">Clear</div>
        <div @click="sign" class="btn">+/-</div>
        <div @click="percent" class="btn">%</div>
        <div class="btn operator">/</div>
        <div @click="append(7)" class="btn">7</div>
        <div @click="append(8)" class="btn">8</div>
        <div @click="append(9)" class="btn">9</div>
        <div class="btn operator">x</div>
        <div @click="append(4)" class="btn">4</div>
        <div @click="append(5)" class="btn">5</div>
        <div @click="append(6)" class="btn">6</div>
        <div class="btn operator">-</div>
        <div @click="append(1)" class="btn">1</div>
        <div @click="append(2)" class="btn">2</div>
        <div @click="append(3)" class="btn">3</div>
        <div class="btn operator">+</div>
        <div @click="append(0)" class="zero btn">0</div>
        <div class="btn">.</div>
        <div class="btn operator">=</div>


    </div>
</template>

<script>
export default {
  data() {
    return {
      current: ""
    }; 
  },
  methods: {
    clear() {
      this.current = "";
    },
    sign() {
        this.current = this.current.charAt(0) === "-" ?
        this.current.slice(1) : `-${this.current}`;
    },
    percent() {
        this.current = `${parseFloat(this.current) / 100}`
    },
    append(number) {
        this.current = `${this.current}${number}`
    }
  }
};
</script>

<style scoped>
.calculator {
  width: 400px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: minmax(50px, auto);
}
.display {
  display: flex;
  align-items: flex-end;
  justify-content: flex-end;
  grid-column: 1/-1;
  background-color: rgb(182, 196, 211);
  border: 1px solid black;
}

.zero {
  grid-column: 1/3;
}

.btn {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #eee;
  border: 1px solid black;
}

.operator {
  background-color: orange;
  color: white;
}
</style>