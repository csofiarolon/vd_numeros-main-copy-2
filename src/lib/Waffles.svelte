<script>
  import * as d3 from "d3";
  let numbers = [24, 33, 42, 54, 63, 71, 77, 87, 92, 98];

  let unidades = [23, 35, 45, 56, 50, 43, 38, 32, 28, 25];

  let title = "La guerra de los cerebros podridos";

  let años = [2014, 2015, 2016, 2017, 2018, 2019, 2020, 2021, 2022, 2023];
</script>

<head>
  <style>
    @import url("https://fonts.googleapis.com/css2?family=Rubik+Glitch&display=swap");
    @import url("https://fonts.googleapis.com/css2?family=Moderustic:wght@500&display=swap");
  </style></head
>

<main>
  <h3 class="headline">{title}</h3>
  <!-- <p id="bajada"> La guerra que cambió cómo vemos a los zombies  </p> -->

  <p id="primer_texto">
    Desde 2014, una aldea de Haití utiliza un ritual de creación de zombies, con
    la ayuda de una entidad, para obtener una mano de obra superfuerte y capaz.
    Este proceso se dio pacíficamente hasta el año 2017, en donde ocurre una
    rebelión y se desata la Guerra de los cerebros podridos, una guerra de
    recursos y valores.
  </p>

  <h5>Evolución de territorio zombie y aldeano a lo largo de los años</h5>
  <h6>(medido en cantidad de hectáreas)</h6>
  <div class="waffles_container">
    <div class="nombre1">
      <p>Zombies</p>
    </div>
    {#each numbers as n, i}
      <div class="waffle_wrapper">
        <p class="number">{numbers[i]}</p>
        <div class="waffle">
          {#each d3.range(0, n) as number}
            <p class="cuad lleno">🧠</p>
          {/each}
        </div>
      </div>
    {/each}
  </div>
  <br />
  <hr />

  <div class="waffles_container">
    <div class="nombre2">
      <p>Aldeanos</p>
    </div>

    {#each unidades as n, i}
      <div class="waffle_wrapper">
        <p class="number">{unidades[i]}</p>
        <div class="waffle">
          {#each d3.range(0, n) as number}
            <p class="cuad lleno">🪵</p>
          {/each}
        </div>
      </div>
    {/each}
  </div>
  <br />
  <hr />

  <div class="años_container">
    <div class="nombre1">
      <!-- <p>años</p> -->
    </div>
    {#each años as n, i}
      <div class="añoswrapper">
        <p class="number">{años[i]}</p>
      </div>
    {/each}
  </div>
</main>

<br />

<p class="textos">
  Para 2015, un cuarto de la aldea era zombie. Estos convivían con las personas
  y sus capacidades evolucionaban día a día. Comenzaron a desarrollar facultades sobrehumanas como la superfuerza y la telepatía, y, además, podían
  reproducirse y negociar con los aldeanos.
</p>
<p class="textos">
  Los humanos vieron esto como una oportunidad para expandir su cantidad de
  recursos, y llegaron a un trato con ellos. Los zombies podían producir en más
  hectáreas y ser dueños de ellas, pero debían entregar todos los recursos que
  produjeran. Su evolución de capacidades continuó positivamente y seguían
  obedeciendo a los humanos, hasta que, una noche del 2017, la entidad tuvo
  suficiente con la situación y decidió que no iba a transcurrir un día más en
  el que sus criaturas sufrieran en manos de los humanos.
</p>

<!-- {#each unidades as n,i}
  <div class="waffle_wrapper">
    <div class="waffle">
      {#each d3.range(0, n) as number}
          <div id= "unidades"> </div>
      {/each}
    </div>
  </div>
  {/each} -->
<br />

<h5 id="cambios"> Conquista de territorios desde 2017 </h5>
<h6>(medido en cantidad de hectáreas)</h6>
<img src="./public/images/barras.png" alt="barras.png">
<p class="textos">
  Ese año se desató el caos. Los zombies se determinaron a conquistar el mundo
  usando sus dotes sobrehumanos para propagar su población y generar un pueblo
  nuevo que venere a su entidad tan amada, dando comienzo así a la guerra. A
  partir de entonces los recursos de la tribu bajaron bruscamente mientras que
  los de los zombies aumentaban exponencialmente, debido a que los zombies
  comenzaron a conquistar territorios y a convertir a más personas en parte de su
  ejército.
</p>
<br>

<h5 id="resumen"> Evolución del territorio antes, durante y después de la guerra</h5>
<h6>(medido en porcentaje de ocupación de la totalidad de hectáreas)</h6>
<img src="./public/images/donas.png" alt="donas.png" id="donas">
<p class="textos">
 Desde 2023, los zombies continuaron con su conquista y llegaron más allá de la aldea. Esto fue documentado de casualidad por un fotógrafo que se encontraba realizando un relevamiento de los daños causados por un devastador tornado que llegó a la isla en mayo de 2024.
</p>
<p class= "textos"> El hombre notó un comportamiento extraño en los haitianos, como si estuviesen constantemente en alerta, y terminó por descubrir el oscuro secreto que ocultaban los pueblos originarios de este lugar del Caribe.</p>







<style>
  .waffles_container {
    display: flex;
    /* flex-direction: column; */
    flex-direction: row;
    align-items: flex-end;
    justify-content: center;
    gap: 14px;
    /* margin-left: 1px; */
  }

  .waffle {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    grid-template-rows: repeat(3, 1fr);
    grid-auto-flow: column-reverse;
    transform: rotateX(180deg);
    width: 100%;
    height: 100%;
    gap: 1px;
    /* margin: 10px; */
    margin-left: 10px;
  }
  .cuad {
    font-size: 17px;
    width: 17px;
    height: 16px;
    margin-top: 1px;
    margin-bottom: 0px;
  }

  .lleno {
    transform: rotateX(180deg);
    /* background-color: white; */
    /* margin-top: 0.01px; */
  }
  .number {
    text-align: center;
    margin-top: 20px;
    margin-bottom: 1px;
    font-family: "Courier New", Courier, monospace;
  }

  /* #unidades {
    background-color: lightblue;
    width: 15px;
    height: 15px;
    border-radius: 100%;
  } */

  .nombre1 {
    justify-content: left;
    font-family: "Courier New", Courier, monospace;
  }

  .nombre2 {
    justify-content: left;
    font-family: "Courier New", Courier, monospace;
  }

  .años_container {
    display: flex;
    flex-direction: row;
    align-items: flex-end;
    justify-content: center;
    gap: 51px;
    margin-left: 8px;
    padding-left: 20px;
  }

  .añoswrapper {
    margin-left: 30px;
    justify-content: center;
    font-size: 14px;
    display: flex;
    flex-direction: row;
  }

  /* #bajada {
    font-family: Moderustic;
    font-size: 22px;
    text-align: center;
    margin-top: 1px;
  } */

  /* #historia{
  font-family: "Courier New", Courier, monospace;
 margin-left: 10%;
 margin-right: 10%;
} */

  .textos {
    font-family: "Courier New", Courier, monospace;
    margin-left: 10%;
    margin-right: 10%;
    margin-top: 2%;
  }

  #primer_texto {
    font-family: "Courier New", Courier, monospace;
    margin-left: 10%;
    margin-right: 10%;
    margin-top: 3%;
    margin-bottom: 5%;
  }

  img{
    margin-top: 0px;
  }

  #donas{
    margin-top: 3px;
  }

</style>