<script>
  import { onMount } from 'svelte';
  let currentPage = 'home';
</script>

<style>
  body {
      font-family: 'Poppins', sans-serif;
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
      text-align: left;
  }
  h1 {
      color: #0056b3;
      text-align: center;
  }
  .section {
      margin-top: 20px;
  }
  footer {
      background: #0056b3;
      color: white;
      text-align: center;
      padding: 10px;
      position: fixed;
      bottom: 0;
      width: 100%;
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
  .social-icons img {
      width: 30px;
      height: 30px;
  }

  /* Responsividade */
  @media (max-width: 768px) {
      .container {
          margin: 20px;
          padding: 20px;
      }
      nav {
          flex-direction: column;
      }
      .social-icons a {
          margin: 0 5px;
      }
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
      <h1>Kauã Rodrigues Negrão</h1>
      <p><strong>Idade:</strong> 18 anos</p>
      <p><strong>Localização:</strong> Jardim Novo Aeroporto, Três Lagoas - MS</p>
      <p><strong>Telefone:</strong> (67) 99204-9293</p>
      <p><strong>Email:</strong> kauarodriguesnegrao@gmail.com</p>
    </div>
  {:else if currentPage === 'sobre'}
    <div class="content">
      <h1>Sobre Mim</h1>
      <p>Sou estudante de Ensino Médio e Técnico em Informática no Instituto Federal do Mato Grosso do Sul (IFMS), com conclusão prevista para dezembro de 2025. Tenho interesse em estagiar na área da informática e busco adquirir experiência para aplicar meus conhecimentos técnicos.</p>
      <div class="section">
        <h2>Objetivo</h2>
        <p>Estágio na área da informática, com foco no desenvolvimento de soluções e no aprimoramento das minhas habilidades técnicas.</p>
      </div>
      <div class="section">
        <h2>Formação Acadêmica</h2>
        <p><strong>Ensino Médio:</strong> Instituto Federal do Mato Grosso do Sul (Conclusão em Dezembro de 2025)</p>
        <p><strong>Técnico em Informática:</strong> Instituto Federal do Mato Grosso do Sul (Conclusão em Dezembro de 2025)</p>
      </div>
      <div class="section">
        <h2>Habilidades</h2>
        <ul>
          <li>Conhecimento do pacote Office</li>
          <li>Conhecimento em elétrica</li>
          <li>Comunicação eficaz</li>
          <li>Adaptabilidade</li>
          <li>Inovação e criatividade</li>
        </ul>
      </div>
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
    <a href="https://www.instagram.com/seu_perfil" target="_blank">
      <img src="https://cdn-icons-png.flaticon.com/512/174/174855.png" alt="Instagram">
    </a>
    <a href="https://www.linkedin.com/in/seu_perfil" target="_blank">
      <img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="LinkedIn">
    </a>
    <a href="https://wa.me/seu_numero" target="_blank">
      <img src="https://cdn-icons-png.flaticon.com/512/733/733585.png" alt="WhatsApp">
    </a>
  </div>
</footer>
