<script>
  import ParImpar from "./lib/parImpar.svelte";
  let valor = 0 
  const listenInput = (event) => valor = event.target.value
</script>

<main>
  <ParImpar numero = {valor}/>

  <input type="number" value={valor} on:input={listenInput}> 

</main>
