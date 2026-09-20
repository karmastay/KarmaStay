<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Karma Fest ID</title>
<style>
body {
  font-family: Arial;
  background: linear-gradient(#cfe3ff, #ffffff);
  text-align: center;
  padding: 20px;
}

input {
  margin: 5px;
  padding: 10px;
  border-radius: 10px;
  border: 1px solid #ccc;
}

button {
  padding: 10px 20px;
  border: none;
  background: #6fa8ff;
  color: white;
  border-radius: 10px;
  cursor: pointer;
}

.card {
  margin-top: 20px;
  width: 300px;
  padding: 20px;
  border-radius: 20px;
  background: white;
  box-shadow: 0 10px 30px rgba(0,0,0,0.1);
  display: none;
}

.title {
  font-weight: bold;
  margin-bottom: 10px;
}
</style>
</head>

<body>

<h2>🎟️ Karma Fest - Stay ID</h2>

<input id="nome" placeholder="Seu nome"><br>
<input id="utt" placeholder="Seu utt"><br>
<input id="local" placeholder="Seu local"><br>

<button onclick="gerar()">Gerar Carteirinha</button>

<div class="card" id="card">
  <div class="title">SKZ KARMA BRASIL</div>
  <p><strong id="nomeCard"></strong></p>
  <p>ID: SKZ-<span id="id"></span></p>
  <p>UTT: <span id="uttCard"></span></p>
  <p>LOCAL: <span id="localCard"></span></p>
  <p><b>KARMA FEST ACCESS PASS</b></p>
</div>

<script>
function gerar() {
  document.getElementById("card").style.display = "block";

  document.getElementById("nomeCard").innerText =
    document.getElementById("nome").value;

  document.getElementById("uttCard").innerText =
    document.getElementById("utt").value;

  document.getElementById("localCard").innerText =
    document.getElementById("local").value;

  document.getElementById("id").innerText =
    Math.floor(Math.random() * 9999);
}
</script>

</body>
</html>
