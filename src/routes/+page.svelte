
<script>
    import { onMount } from 'svelte';
    let currentPage = 'home';
  </script>
  
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
      color: #333;
    }
    .container {
      max-width: 800px;
      margin: 50px auto;
      padding: 20px;
      background: white;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    nav {
      display: flex;
      justify-content: space-around;
      padding: 10px;
      background: #007BFF;
      color: white;
    }
    nav a {
      color: white;
      text-decoration: none;
      cursor: pointer;
    }
    .content {
      padding: 20px;
    }
  </style>
  
  <nav>
    <a on:click={() => currentPage = 'home'}>Home</a>
    <a on:click={() => currentPage = 'sobre'}>Sobre</a>
    <a on:click={() => currentPage = 'contato'}>Contato</a>
  </nav>
  
  <div class="container">
    {#if currentPage === 'home'}
      <div class="content">
        <h1>Bem-vindo ao Meu Currículo</h1>
        <p>Confira minhas informações profissionais.</p>
      </div>
    {:else if currentPage === 'sobre'}
      <div class="content">
        <h1>Sobre Mim</h1>
        <p>Aqui você pode adicionar informações sobre você.</p>
      </div>
    {:else if currentPage === 'contato'}
      <div class="content">
        <h1>Contato</h1>
        <p>Me encontre através dos seguintes meios.</p>
      </div>
    {/if}
  </div>
  