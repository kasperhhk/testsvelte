<script lang="ts">
  import { getState, setState } from '$lib/state';
  
  let state = getState();
  let value: string;

  function onclick() {
    setState(value);
    state = getState();
  } 
</script>

<h1>State: {state}</h1>
<input bind:value={value} /><button on:click={onclick}>Change state</button>
<br/>
<a href="/basic">Go to basic</a>