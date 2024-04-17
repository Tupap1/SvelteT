<script>
export let numero;
let resultado;
$: if (numero===0)
  resultado = "El numero es neutro"
else 
    if (numero%2===0)
      resultado = "El numero es par";
    else
      resultado = "El numero es impar";
</script>

<p>{resultado}</p>

<style>
  p{
    color: antiquewhite;
    font-family: sans-serif;
    font-size: 25px;
  }
</style>
