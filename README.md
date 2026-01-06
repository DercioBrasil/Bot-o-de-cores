<html> 
  <head>
    <style>
      body {
        background-color: #f3f4f6;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        font-family: Arial, sans-serif;
        gap: 20px;
      }

      h1{
        cursor: pointer;
        font-size: 40px;
        padding: 18px;
        border-radius: 10px;
        transition: color 0.2s;
      }
  
      #resultado{
       font-size: 24px;
       padding: 10px 15px;
       border: 1px solid #ccc;
       border-radius: 8px;
       background: white;
      }

    </style>
  </head>
  <body>
    <h1 id="titulo">Clique em mim</h1>
    <div id="resultado">A cor escolhida vai aparecer aqui</div>

    <script>
      const titulo = document.getElementById('titulo');
      const resultado = document.getElementById('resultado');

      function corAleatoria() {
     return '#' + Math.floor(Math.random()*16777215).toString(16).padStart(6, '0');
      }

      titulo.addEventListener('click', () => {
        const corTexto = corAleatoria();
        const corFundo = corAleatoria();

        titulo.style.background = corFundo;
        titulo.style.color = corTexto;
        resultado.textContent = `Cor do texto: ${corTexto} | Cor de fundo: ${corFundo}`;
      });

    </script>
  </body>
</html>
