<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Territórios da Semana</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background: #f4f6f9;
    }

    header {
      background: #4a6fa5;
      color: #fff;
      padding: 18px;
      text-align: center;
      font-size: 22px;
      font-weight: bold;
    }

    .botoes, .grupos {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin: 30px 10px;
    }

    button {
      background: #fff;
      border: 1px solid #4a6fa5;
      color: #4a6fa5;
      padding: 10px 22px;
      border-radius: 22px;
      font-size: 14px;
      cursor: pointer;
      white-space: nowrap;
    }

    button:hover {
      background: #4a6fa5;
      color: #fff;
    }

    .feriado {
      border-color: #d4a017;
      color: #d4a017;
      font-weight: bold;
    }

    .feriado:hover {
      background: #d4a017;
      color: #fff;
    }

    footer {
      text-align: center;
      font-size: 12px;
      color: #777;
      margin-top: 40px;
    }

    .hidden {
      display: none;
    }

    h2 {
      text-align: center;
      color: #4a6fa5;
    }
  </style>
</head>

<body>

<header>Territórios da Semana</header>

<!-- BOTÕES PRINCIPAIS -->
<div id="menu" class="botoes">
  <button onclick="abrirDia('segunda')">Segunda</button>
  <button onclick="abrirDia('terca')">Terça</button>
  <button onclick="abrirDia('quarta')">Quarta</button>
  <button onclick="abrirDia('quinta')">Quinta</button>
  <button onclick="abrirDia('sexta')">Sexta</button>
  <button onclick="mostrarGrupos()">Domingo</button>
  <button onclick="abrirDia('rural')">Campo Rural</button>
  <button class="feriado" onclick="abrirDia('feriado')">Feriado</button>
</div>

<!-- SELEÇÃO DE GRUPOS (DOMINGO) -->
<div id="grupos" class="hidden">
  <h2>Selecione seu grupo</h2>
  <div class="grupos">
    <button onclick="abrirGrupo('grupo1')">Grupo 1</button>
    <button onclick="abrirGrupo('grupo2')">Grupo 2</button>
    <button onclick="abrirGrupo('grupo3')">Grupo 3</button>
  </div>

  <div class="botoes">
    <button onclick="voltar()">⬅ Voltar</button>
  </div>
</div>

<footer>
  Organização de Territórios – Congregação Bela Vista
</footer>

<script>
  function abrirDia(pagina) {
    window.location.href = pagina + ".html";
  }

  function mostrarGrupos() {
    document.getElementById("menu").classList.add("hidden");
    document.getElementById("grupos").classList.remove("hidden");
  }

  function voltar() {
    document.getElementById("grupos").classList.add("hidden");
    document.getElementById("menu").classList.remove("hidden");
  }

  function abrirGrupo(grupo) {
    window.location.href = "domingo-" + grupo + ".html";
  }
</script>

</body>
</html>
