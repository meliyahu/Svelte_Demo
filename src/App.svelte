<script>
  let name = "Hout Kop";
  let points = 100;
  let showControls = false;
  const addPoint = () => points += 1;
  const removePoint = () => points -= 1;
  const toggleControls = () => ( showControls = !showControls);
</script>

<style>
  h1 {
    color: #204f6e;
  }
  
  h3 {
	  margin-bottom:10px;
	  }

</style>

<div class="container">
  <div class="card">
    <h1>{name}
	<button class="btn btn-sm" on:click={toggleControls}>+</button>
	</h1>
    <h3>{points}</h3>
	{#if showControls}
	<button class="btn" title="Add point" on:click={addPoint}>+1</button>
	<button class="btn btn-dark" title="Remove point" on:click={removePoint}>-1</button>
	<input type="number" bind:value={points}>
	{/if}
  </div>
</div>
