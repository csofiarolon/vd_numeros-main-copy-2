<script>
  import Waffles from "./lib/Waffles.svelte";
  import * as d3 from "d3";

  let numbers = [24, 33, 42, 54, 63, 71, 77, 87, 92, 98];

  let decenas = [2, 3, 4, 5, 6, 7, 7, 8, 9, 9];
  let unidades = [4, 3, 2, 4, 3, 1, 7, 7, 2, 8];

  /* Verificamos no haber salteado ningun número (que los largos sean iguales)
  console.log(decenas.length, unidades.length, numbers.length)
  */
</script>


<!-- <header> 
  <a href=#historia> Historia </a>
  <a href=#Rebelion> Rebelión Zombie </a>
  </header> -->

<main class="container">
  <div class="cuadraditos_container">
    <Waffles {numbers} title="Visualizar un conjunto de números" />
  </div>

  <!-- {#each decenas as decena }
  <div class="cuadrado">{decena}</div>
  {/each} -->
  <!-- {#each numbers as number, i}
    {#each d3.range(0, number) as n}
      <div class="cuadrado">{decenas[i]}</div>
      <div class="circulo">{unidades[i]}</div>
    {/each}
  {/each}  -->
</main>

<style>
  .container {
    /* max-width: 1280px; */
    margin: 0 auto;
    padding: 2rem;
  }
  :global(.headline) {
    /* margin: 5px; */
    font-family: "Rubik Glitch", system-ui;
    font-weight: 400;
    font-style: normal;
    font-size: 45px;
    text-align: center;
    color: rgb(62, 16, 16);
  }
</style>