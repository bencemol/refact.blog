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
</style>

<div class="counter flex">
  <button on:click={subtract}>-</button>
  <div>{ count }</div>
  <button on:click={add}>+</button>
</div>
<div class="children">
  <slot />
</div>
