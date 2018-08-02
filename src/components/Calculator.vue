<template>
    <div class="calculator">
        <div class="display">display</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>
        <div>area1</div>

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
    grid-column: 1/-1;
}
</style>