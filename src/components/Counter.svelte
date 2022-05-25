<script lang="ts">
  import { count } from "../stores/counter.store";

  let countValue;

  $: countValue = $count;
</script>

<div class="counter">
  <button on:click={count.decrement}>-</button>
  <pre>{countValue}</pre>
  <button on:click={count.increment}>+</button>
</div>
<div class="message">
  <slot />
</div>

<style>
  .counter {
    display: grid;
    font-size: 2em;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    margin-top: 2em;
    place-items: center;
    height: 800px;
  }
  .message {
    text-align: center;
  }
</style>
