<script>
  /*   import buscador from "./lib/locations.svelte";
  import Characters from "./lib/characters.svelte";
  import Locations from "./lib/locations.svelte";
  import Episodes from "./lib/episodes.svelte"; */

  import { onMount } from "svelte";
  //export let buscador
  let datosApi;

  onMount(async () => {
    const response = await fetch("https://rickandmortyapi.com/api/");
    if (!response.ok) {
      throw new Error(`Error API ${response.status}`);
    }
    datosApi = await response.json();
    console.log(datosApi);
  });

  function personaje() {
    onMount(async () => {
      const response = await fetch("https://rickandmortyapi.com/api/character");
      if (!response.ok) {
        throw new Error(`Error API ${response.status}`);
      }
      datosApi = await response.json();
      console.log(datosApi);
    });
  }
</script>

<main>
  <div>
    <input
      id="buscador"
      type="text"
      value=""
      placeholder="Busca personajes, episodios y ubicaciones"

          />

          <div id="buscadores">
    <input
      id="personajes"
      type="button"
      value="Buscar personajes"
      onclick="personaje()"
    />
    <input
      id="personajes"
      type="button"
      value="Buscar Episodios"
      onclick=personaje()
    />
    <input
      id="personajes"
      type="button"
      value="Buscar Ubicaciones"
      onclick="personaje()"
    />
  </div>
  </div>

  <div></div>

  <p></p>
</main>
