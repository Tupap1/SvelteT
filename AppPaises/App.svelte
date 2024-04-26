<script>
  import Paises from "./lib/Paises.svelte";
  const lista = ["Colombia", "Venezuela", "Ecuador", "Peru", "Brasil", "Argentina", "Bolivia", "Chile", "Guayna", "Paraguay", "Surinam", "Uruguay"]
</script>

<div class="main">
  {#each lista as pais}

  <div>
    <Paises {pais}/>
  </div>

  {:else}
  no existen elementos
  {/each}
</div>

<svelte:head>
    <title>Paises de Suramerica</title> 
</svelte:head>

<style>
  .main {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-gap: 10px;
        grid-auto-rows: minmax(100px, auto);
        }
</style>