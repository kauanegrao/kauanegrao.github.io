

<script>
  import { sortable } from "svelte-sortable";
  let currentTab = "comida";

  let comida = [
    { nome: "Açaí", img: "./images/acai.jpg" },
    { nome: "Pastel de queijo", img: "./images/pastel.jpg" },
    { nome: "Coxinha", img: "./images/coxinha.jpg" },
    { nome: "Chocolate", img: "./images/chocolate.jpg" },
    { nome: "Cookies", img: "./images/cookies.jpg" },
    { nome: "Morango", img: "./images/morango.jpg" },
    { nome: "Uva sem caroço", img: "./images/uva.jpg" },
    { nome: "Melancia", img: "./images/melancia.jpg" },
    { nome: "Purê de batata", img: "./images/pure.jpg" },
    { nome: "Hambúrguer", img: "./images/hamburguer.jpg" }
  ];

  let filmesSeriesAnimes = [
    { nome: "Hunter x Hunter", img: "./images/hxh.jpg" },
    { nome: "One Piece", img: "./images/onepiece.jpg" },
    { nome: "Ratatouille", img: "./images/ratatouille.jpg" },
    { nome: "O Incrível Mundo de Gumball", img: "./images/gumball.jpg" },
    { nome: "Sonic", img: "./images/sonic.jpg" },
    { nome: "Carros", img: "./images/carros.jpg" },
    { nome: "Vinland Saga", img: "./images/vinland.jpg" },
    { nome: "Dinossauro Rei", img: "./images/dino.jpg" },
    { nome: "Bob Esponja", img: "./images/bobesponja.jpg" },
    { nome: "Hora de Aventura", img: "./images/hora.jpg" }
  ];

  let gostosGerais = [
    { nome: "Vôlei", img: "./images/volei.jpg" },
    { nome: "Basquete", img: "./images/basquete.jpg" },
    { nome: "Rock", img: "./images/rock.jpg" },
    { nome: "Número 7", img: "./images/7.jpg" },
    { nome: "Motos Antigas", img: "./images/motos.jpg" },
    { nome: "Carros de Luxo", img: "./images/carrosluxo.jpg" },
    { nome: "Super Choque", img: "./images/superchoque.jpg" },
    { nome: "Pokémon", img: "./images/pokemon.jpg" },
    { nome: "God of War", img: "./images/gow.jpg" }
  ];
</script>

<style>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #eef2f3;
    color: #333;
  }
  .container {
    max-width: 900px;
    margin: 50px auto;
    padding: 30px;
    background: white;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
    text-align: center;
  }
  .tabs button {
    padding: 10px 20px;
    margin: 5px;
    border: none;
    background: #28a745;
    color: white;
    cursor: pointer;
    border-radius: 5px;
  }
  .tabs button:hover {
    background: #218838;
  }
  .cards {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 20px;
    padding: 20px;
  }
  .card {
    background: white;
    padding: 15px;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
    cursor: grab;
  }
  .card img {
    width: 100%;
    height: 150px;
    object-fit: cover;
    border-radius: 8px;
  }
  h1, h2 {
    color: #28a745;
  }
</style>

<nav>
  <a href="curriculo.html">Currículo</a>
</nav>

<div class="container">
  <h1>Meus Gostos - Ranking</h1>

  <div class="tabs">
    <button on:click={() => currentTab = "comida"}>Comida</button>
    <button on:click={() => currentTab = "filmes"}>Filmes, Séries e Animes</button>
    <button on:click={() => currentTab = "gostos"}>Gostos Gerais</button>
  </div>

  {#if currentTab === "comida"}
    <div class="cards" use:sortable={{ items: comida }}>
      {#each comida as item (item.nome)}
        <div class="card">
          <img src={item.img} alt={item.nome}>
          <h3>{item.nome}</h3>
        </div>
      {/each}
    </div>
  {/if}

  {#if currentTab === "filmes"}
    <div class="cards" use:sortable={{ items: filmesSeriesAnimes }}>
      {#each filmesSeriesAnimes as item (item.nome)}
        <div class="card">
          <img src={item.img} alt={item.nome}>
          <h3>{item.nome}</h3>
        </div>
      {/each}
    </div>
  {/if}

  {#if currentTab === "gostos"}
    <div class="cards" use:sortable={{ items: gostosGerais }}>
      {#each gostosGerais as item (item.nome)}
        <div class="card">
          <img src={item.img} alt={item.nome}>
          <h3>{item.nome}</h3>
        </div>
      {/each}
    </div>
  {/if}
</div>
