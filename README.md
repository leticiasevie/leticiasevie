<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Ubuntu:wght@400;700&family=Courgette&display=swap">
    <style>
        body {
            margin: 0;
            background-color: rgb(227, 227, 236);
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column; 
            height: 100vh;
            font-family: 'Ubuntu', sans-serif;
        }

        .constelacao-container {
            width: 600px;
            height: 200px;
            background-color: rgb(19, 19, 37);
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .estrela {
            width: 3px;
            height: 3px;
            background-color: rgb(255, 255, 255);
            position: absolute;
            border-radius: 50%;
        }

        .ponto {
            width: 1px;
            height: 1px;
            background-color: rgb(255, 255, 255);
            position: absolute;
            border-radius: 50%;
            animation: brilho 1.5s infinite; 
        }

        @keyframes brilho {
            0%, 100% {
                opacity: 0.4;
                transform: scale(1);
            }

            50% {
                opacity: 0.5;
                transform: scale(3.5); 
            }
        }

        
        .nome {
            font-family: 'Courgette', cursive;
            font-size: 28px;
            color: white;
            margin: 2px 0; 
            text-shadow: 5px 5px 5px rgb(0, 0, 0); 
        }

     
        .ola {
            font-size: 13px;
            color: white;
            margin: 2px 0;
            text-shadow:  7px 7px 7px rgb(0, 0, 0); 
        }
    </style>
</head>
<body>
    <div class="constelacao-container" id="constelacao">
        <p class="ola">👋🏻 Olá,eu sou a</p>
        <p class="nome">Letícia</p>
    </div>

    <script>
        function criarEstrela(numeroEstrela, quantidadePontos) {
            const constelacao = document.getElementById('constelacao');
            const estrela = document.createElement('div');
            estrela.classList.add('estrela');

            for (let i = 0; i < quantidadePontos; i++) {
                const ponto = document.createElement('div');
                ponto.classList.add('ponto');
                estrela.appendChild(ponto);
            }

            constelacao.appendChild(estrela);

            const left = Math.floor(Math.random() * (600 - 3));
            const top = Math.floor(Math.random() * (200 - 3));
            estrela.style.left = `${left}px`;
            estrela.style.top = `${top}px`;
        }

        for (let i = 0; i < 150; i++) {
            criarEstrela(i, 5);
        }
    </script>

- 🔭 Estudante no 3º ano de técnico em informática.
- 📫 leticiasvd@outlook.com
  
