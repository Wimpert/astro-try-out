<script>
  import { count } from "../stores/counter.store";
</script>

<div>
  <span> count: </span>
  {$count}
  <button on:click={count.increment}>+</button>
</div>
