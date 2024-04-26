<script>
  export let pais;
  let p;

  const paises = {
    Colombia: [
      "Colombia",
      "Bogota",
      "51,52 millones de habitantes",
      "Peso Colombiano",
      "1,142 Millones de Km",
      "https://upload.wikimedia.org/wikipedia/commons/thumb/2/21/Flag_of_Colombia.svg/800px-Flag_of_Colombia.svg.png",
    ],

    Venezuela: [
      "Venezuela",
      "Caracas",
      "28,435,928 habitantes (2023)",
      "Bolívar Fuerte (VEF)",
      "916,440 Km²",
      "https://upload.wikimedia.org/wikipedia/commons/0/06/Flag_of_Venezuela.svg",
    ],

    Peru: [
      "Peru",
      "Lima",
      "33,375,894 habitantes (2023)",
      "Sol Peruano (PEN)",
      "1,285,216 Km²",
      "https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Flag_of_Peru.svg/1280px-Flag_of_Peru.svg.png",
    ],

    Ecuador: [
      "Ecuador",
      "Quito",
      "18,140,133 habitantes (2023)",
      "Dólar Estadounidense (USD)",
      "283,561 Km²",
      "https://upload.wikimedia.org/wikipedia/commons/e/e8/Flag_of_Ecuador.svg",
    ],

    Brasil: [
      "Brasil",
      "Brasilia",
      "215,573,947 habitantes (2023)",
      "Real Brasileño (BRL)",
      "8,515,770 Km²",
      "https://upload.wikimedia.org/wikipedia/commons/0/05/Flag_of_Brazil.svg",
    ],

    Argentina: [
      "Argentina",
      "Buenos Aires",
      "46,289,813 habitantes (2023)",
      "Peso Argentino (ARS)",
      "2,780,400 Km²",
      "https://es.wikipedia.org/wiki/Bandera_de_la_Argentina",
    ],
    Bolivia: [
      "Bolivia",
      "Sucre (capital constitucional) y La Paz (sede de gobierno)",
      "12,062,185 habitantes (2023)",
      "Boliviano (BOB)",
      "1,098,581 Km²",
      "https://es.wikipedia.org/wiki/Bandera_de_Bolivia",
    ],
    Chile: [
      "Chile",
      "Santiago de Chile",
      "19,723,871 habitantes (2023)",
      "Peso Chileno (CLP)",
      "756,102 Km²",
      "https://es.wikipedia.org/wiki/Bandera_de_Chile",
    ],
    Guyana: [
      "Guyana",
      "Georgetown",
      "814,360 habitantes (2023)",
      "Dólar Guyanés (GYD)",
      "214,999 Km²",
      "https://es.wikipedia.org/wiki/Bandera_de_Guyana",
    ],
    Paraguay: [
      "Paraguay",
      "Asunción",
      "7,454,116 habitantes (2023)",
      "Guarani Paraguayo (PYG)",
      "406,752 Km²",
      "https://es.wikipedia.org/wiki/Bandera_de_Paraguay",
    ],
    Surinam: [
      "Surinam",
      "Paramaribo",
      "587,604 habitantes (2023)",
      "Dólar Surinamés (SRD)",
      "163,821 Km²",
      "https://es.wikipedia.org/wiki/Bandera_de_Surinam",
    ],
    Uruguay: [
      "Uruguay",
      "Montevideo",
      "3,517,248 habitantes (2023)",
      "Peso Uruguayo (UYU)",
      "176,214 Km²",
      "https://es.wikipedia.org/wiki/Bandera_de_Uruguay",
    ],
  };

  p = paises[pais];
</script>

<div class="main">
  <div class="col1">
    <img src={p[5]} alt="bandera de colombia" width="250" height="200" />
  </div>
  <div class="col2">
    <div class="linea"><strong>Pais:</strong> {p[0]}</div>
    <div class="linea"><strong>Capital:</strong> {p[1]}</div>
    <div class="linea"><strong>Poblacion:</strong> {p[2]}</div>
    <div class="linea"><strong>Moneda:</strong> {p[3]}</div>
    <div class="linea"><strong>Extension:</strong> {p[4]}</div>
  </div>
</div>

<style>
  .main {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 5px;
    grid-auto-rows: minmax(100px, auto);
    border-radius: 10px;
    border-style: solid;
    border-color: gold;
    border-width: 2px;
    margin: left;
    width: 600px;
    box-shadow: 5px 5px 5px black;
    margin-right: 5px;
    margin-bottom: 10px;
  }

  .col1 {
    grid-column: 1;
    grid-row: 1;
    margin: 5px;
    padding: 5px;
  }

  .col2 {
    grid-column: 2;
    grid-row: 1;
    margin: 5px;
    padding: 5px;
    border-color: black;
    width: max-content;
  }

  strong {
    color: blue;
    font-weight: bolder;
  }

  .linea {
    font-size: 15px;
    margin-bottom: 18px;
  }
</style>
