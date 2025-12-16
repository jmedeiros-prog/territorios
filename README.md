<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Territórios de Pregação</title>

<style>
body{
  font-family:Arial,Helvetica,sans-serif;
  background:#f4f6f8;
  margin:0;
}
header{
  background:#1f3a5f;
  color:#fff;
  padding:20px;
  text-align:center;
}
.container{
  max-width:900px;
  margin:30px auto;
  padding:20px;
}
.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(140px,1fr));
  gap:15px;
}
a.button{
  display:flex;
  align-items:center;
  justify-content:center;
  padding:18px;
  text-decoration:none;
  background:#ffffff;
  border-radius:12px;
  box-shadow:0 4px 10px rgba(0,0,0,0.1);
  color:#1f3a5f;
  font-weight:bold;
  font-size:18px;
}
a.button:active{
  background:#e8f0fe;
}
.special{
  background:#1f3a5f;
  color:#fff;
}
footer{
  text-align:center;
  margin-top:40px;
  font-size:14px;
  color:#777;
}
</style>

<script>
function toggleSunday(){
  const menu = document.getElementById('domingo');
  menu.style.display = menu.style.display === 'none' ? 'block' : 'none';
}
</script>
</head>

<body>

<header>
  <h1>Territórios de Pregação</h1>
  <p>Selecione o dia</p>
</header>

<div class="container">

  <!-- DIAS DA SEMANA -->
  <div class="grid">
    <a class="button" href="segunda.html">Segunda</a>
    <a class="button" href="terca.html">Terça</a>
    <a class="button" href="quarta.html">Quarta</a>
    <a class="button" href="quinta.html">Quinta</a>
    <a class="button" href="sexta.html">Sexta</a>
    <a class="button" href="sabado.html">Sábado</a>
    <a class="button" href="javascript:void(0)" onclick="toggleSunday()">Domingo</a>
  </div>

  <!-- DOMINGO - GRUPOS -->
  <div id="domingo" style="display:none;margin-top:20px">
    <div class="grid">
      <a class="button" href="domingo-bv1.html">Bela Vista 1 (Edson Reis)</a>
      <a class="button" href="domingo-bv2.html">Bela Vista 2 (George Moura)</a>
      <a class="button" href="domingo-caxambu.html">Caxambu (Willian)</a>
      <a class="button" href="domingo-meireles.html">Meireles (Edson Ornagui)</a>
    </div>
  </div>

  <!-- ESPECIAIS -->
  <h2 style="margin-top:40px;text-align:center">Especiais</h2>
  <div class="grid">
    <a class="button special" href="feriados.html">Feriados</a>
    <a class="button special" href="rural.html">Campo Rural</a>
  </div>

</div>

<footer>
  <p>Uso interno – Organização de Territórios</p>
</footer>

</body>
</html>
