<script>
  import { onMount } from "svelte";
  export let buscador
  let datosApi;

  onMount(async () => {
    const response = await fetch(
      "https://rickandmortyapi.com/api/character" + buscador
    );
    if (!response.ok) {
      throw new Error(`Error API ${response.status}`);
    }
    datosApi = await response.json();
  });
</script>
