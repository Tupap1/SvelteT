<script>
  export let buscador;
  import { onMount } from "svelte";
  let datosApi;

  onMount(async () => {
    const response = await fetch(
      "https://rickandmortyapi.com/api/location" + buscador,
    );
    if (!response.ok) {
      throw new Error(`Error API ${response.status}`);
    }
    datosApi = await response.json();
  });
</script>
