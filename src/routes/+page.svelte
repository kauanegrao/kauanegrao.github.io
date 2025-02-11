<script>
  import { onMount } from 'svelte';
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
    background: #0056b3;
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
  .content {
    padding: 20px;
  }
  h1 {
    color: #0056b3;
  }
  footer {
    background: #0056b3;
    color: white;
    text-align: center;
    padding: 10px;
    margin-top: 20px;
  }
  .social-icons {
    margin-top: 10px;
  }
  .social-icons a {
    margin: 0 10px;
    color: white;
    font-size: 24px;
    text-decoration: none;
  }
</style>

<nav>
  <a on:click={() => currentPage = 'home'}>Início</a>
  <a on:click={() => currentPage = 'sobre'}>Sobre</a>
  <a on:click={() => currentPage = 'contato'}>Contato</a>
</nav>

<div class="container">
  {#if currentPage === 'home'}
    <div class="content">
      <h1>KAUÃ RODRIGUES NEGRÃO</h1>
      <p><strong>Localização:</strong> Três Lagoas - MS</p>
      <p><strong>Telefone:</strong> (67) 99204-9293</p>
      <p><strong>Email:</strong> kauarodriguesnegrao@gmail.com</p>
      <p><strong>Data de Nascimento:</strong> 22/05/2006</p>
    </div>
  {:else if currentPage === 'sobre'}
    <div class="content">
      <h1>Resumo Profissional</h1>
      <p>Tenho experiência como atendente em restaurantes e também trabalho com higienização de ar-condicionados. Essas atividades me deram conhecimento em atendimento ao cliente e habilidades técnicas básicas.</p>
      <p>Tenho experiência em manutenção, higienização e instalação de ar-condicionados, adquirida através de trabalhos realizados junto ao meu pai. Tenho também conhecimento na área de elétrica, o que amplia minhas competências técnicas e práticas.</p>
      <p>Atualmente, estou cursando Tecnologia da Informação (TI), o que me permite integrar conhecimentos técnicos e tecnológicos, proporcionando uma abordagem abrangente e inovadora em minhas atividades profissionais.</p>
    </div>
  {:else if currentPage === 'contato'}
    <div class="content">
      <h1>Contato</h1>
      <p>Entre em contato comigo pelos seguintes meios:</p>
      <p><strong>Telefone:</strong> (67) 99204-9293</p>
      <p><strong>Email:</strong> kauarodriguesnegrao@gmail.com</p>
    </div>
  {/if}
</div>

<footer>
  <p>Minhas Redes Sociais:</p>
  <div class="social-icons">
    <a href="https://www.instagram.com/seu_perfil" target="_blank">📷</a>
    <a href="https://www.linkedin.com/in/seu_perfil" target="_blank">💼</a>
    <a href="https://wa.me/seu_numero" target="_blank">📱</a>
  </div>
</footer>
