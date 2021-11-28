<script>
  let count = 0;

  function add() {
    count += 1;
  }

  function subtract() {
    count -= 1;
  }
</script>

<style>
.counter {
  gap: 1ch;
}
button,
div {
  width: 4ch;
  text-align: center;
}
</style>

<div class="counter">
  <button on:mousedown={subtract}>-</button>
  <div>{ count }</div>
  <button on:mousedown={add}>+</button>
</div>
<div class="children">
  <slot />
</div>
