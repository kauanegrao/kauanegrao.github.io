<script>
    let currentPage = 'home';
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
    }
    nav {
      display: flex;
      justify-content: space-around;
      padding: 15px;
      background: #28a745;
      color: white;
      border-radius: 10px 10px 0 0;
    }
    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
    }
    nav a:hover {
      text-decoration: underline;
    }
    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      gap: 20px;
      padding: 20px;
    }
    .card {
      background: white;
      padding: 15px;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
      text-align: center;
    }
    .card h3 {
      color: #28a745;
    }
  </style>
  
  <nav>
    <a href="curriculo.html">Currículo</a>
  </nav>
  
  <div class="container">
    <h1>Meus Gostos</h1>
    <div class="cards">
      <div class="card"><h3>Comida</h3><p>Açaí, pastel de queijo, coxinha, chocolate, cookies, morango, uva sem caroço, melancia, purê de batata, hambúrguer.</p></div>
      <div class="card"><h3>Filmes, Séries e Animes</h3><p>Hunter x Hunter, One Piece, Ratatouille, O Incrível Mundo de Gumball, Sonic, Carros, Vinland Saga, Dinossauro Rei, Bob Esponja, Hora de Aventura.</p></div>
      <div class="card"><h3>Gostos Gerais</h3><p>Vôlei, basquete, rock, o número 7, motos antigas, carros de luxo, Super Choque, Pokémon, God of War.</p></div>
    </div>
  </div>
  