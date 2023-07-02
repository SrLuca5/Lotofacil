<!DOCTYPE html>
<html>
<head>
  <title>Gerador de Sequência Lotofácil</title>
  <script>
    function gerarSequenciaLotofacil(numero) {
      var sequencia = [];

      for (var i = 1; i <= 15; i++) {
        var numeroSorteado = (numero + i) % 25 + 1;
        sequencia.push(numeroSorteado);
      }

      return sequencia;
    }

    function gerarSequencia() {
      var numeroEscolhido = parseInt(document.getElementById("numero").value);
      var sequenciaJogo = gerarSequenciaLotofacil(numeroEscolhido);
      document.getElementById("resultado").innerHTML = "Sequência do jogo da Lotofácil: " + sequenciaJogo.join(", ");
    }
  </script>
</head>
<body>
  <h1>Gerador de Sequência Lotofácil</h1>
  <label for="numero">Digite um número:</label>
  <input type="number" id="numero">
  <button onclick="gerarSequencia()">Gerar Sequência</button>
  <p id="resultado"></p>
</body>
</html>
