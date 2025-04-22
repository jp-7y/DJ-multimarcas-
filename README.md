<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>eBook - Como Crescer nas Redes Sociais</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      color: #333;
      padding: 20px;
    }
    .ebook-container {
      width: 80%;
      margin: 50px auto;
      background: #fff;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      padding: 30px;
      border-radius: 10px;
    }
    .title {
      text-align: center;
      font-size: 2.5em;
      color: #fdd835;
      margin-bottom: 20px;
    }
    .content {
      font-size: 1.1em;
      line-height: 1.8;
      color: #444;
    }
    .page {
      display: none;
    }
    .page.active {
      display: block;
    }
    .pagination {
      text-align: center;
      margin-top: 30px;
    }
    .pagination button {
      background-color: #fdd835;
      color: black;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 1.1em;
    }
    .pagination button:hover {
      background-color: #fbc02d;
    }
    .testimonial-container {
      display: flex;
      align-items: center;
      margin-top: 20px;
    }
    .testimonial-container img {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      margin-right: 20px;
    }
    .testimonial-container p {
      font-size: 1.1em;
    }
  </style>
</head>
<body>

  <div class="ebook-container">
    <div class="title">Como Crescer nas Redes Sociais</div>

    <div class="content">

      <!-- Page 1 -->
      <div class="page active" id="page-1">
        <h2>Introdução</h2>
        <p>Bem-vindo ao nosso eBook sobre como crescer nas redes sociais. Neste eBook, você aprenderá as estratégias que os influenciadores usam para aumentar seu engajamento e atrair mais seguidores.</p>
      </div>

      <!-- Page 2 -->
      <div class="page" id="page-2">
        <h2>Capítulo 1: Entendendo o Algoritmo</h2>
        <p>Os algoritmos das redes sociais determinam como seu conteúdo é exibido para os seguidores. Aprender como eles funcionam é fundamental para otimizar seu conteúdo e alcançar mais pessoas.</p>
      </div>

      <!-- Page 3 -->
      <div class="page" id="page-3">
        <h2>Capítulo 2: Criando Conteúdo Atraente</h2>
        <p>Agora que você entende os algoritmos, é hora de aprender a criar conteúdo que os algoritmos vão adorar. Use imagens de alta qualidade, textos interessantes e vídeos envolventes.</p>
      </div>

      <!-- Depoimentos -->
      <section class="testimonial-container">
        <h3>O que estão dizendo sobre o eBook:</h3>
        <div class="testimonial-container">
          <img src="https://via.placeholder.com/50" alt="Rafael T.">
          <p>"Comprei sem muitas expectativas, mas fiquei impressionado! Em poucos dias meu perfil explodiu de interações." <br><strong>– Rafael T.</strong></p>
        </div>
        <div class="testimonial-container">
          <img src="https://via.placeholder.com/50" alt="Juliana L.">
          <p>"As dicas são muito práticas e funcionam de verdade. Já indiquei para vários amigos!" <br><strong>– Juliana L.</strong></p>
        </div>
      </section>

      <!-- Pagination -->
      <div class="pagination">
        <button id="prev" onclick="changePage('prev')">Página Anterior</button>
        <button id="next" onclick="changePage('next')">Próxima Página</button>
      </div>
    </div>
  </div>

  <script>
    let currentPage = 1;
    const pages = document.querySelectorAll('.page');

    function showPage(pageNumber) {
      pages.forEach((page, index) => {
        page.classList.remove('active');
        if (index + 1 === pageNumber) {
          page.classList.add('active');
        }
      });
    }

    function changePage(direction) {
      if (direction === 'next') {
        currentPage = currentPage < pages.length ? currentPage + 1 : currentPage;
      } else if (direction === 'prev') {
        currentPage = currentPage > 1 ? currentPage - 1 : currentPage;
      }
      showPage(currentPage);
    }

    // Initial page setup
    showPage(currentPage);
  </script>

</body>
</html>
