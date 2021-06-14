# Tabela-classificacao
Tabela de clasIFICAÇÃO
COD HTML
<html>

<head>
    <title>
        Imersão Dev - Aula 06
    </title>
</head>

<body>
    <h1>Tabela de classificação</h1>

    <table style="width:100%">
        <thead>
            <tr>
                <th>Nome</th>
                <th>Vitórias</th>
                <th>Empates</th>
                <th>Derrotas</th>
                <th>Pontos</th>
                <th>Ações</th>
            </tr>
        </thead>
        <tbody id="tabelaJogadores">
              <tr>
    <td>Paulo</td>
    <td>2</td>
    <td>1</td>
    <td>1</td>
    <td>7</td>
    <td><button onClick="adicionarVitoria()">Vitória</button></td>
    <td><button onClick="adicionarEmpate()">Empate</button></td>
    <td><button onClick="adicionarDerrota()">Derrota</button></td>
  </tr>
  <tr>
    <td>Rafa</td>
    <td>1</td>
    <td>4</td>
    <td>2</td>
    <td>7</td>
    <td><button onClick="adicionarVitoria()">Vitória</button></td>
    <td><button onClick="adicionarEmpate()">Empate</button></td>
    <td><button onClick="adicionarDerrota()">Derrota</button></td>
  </tr>
        </tbody>
    </table>
</body>

</html>

COD CSS.
{
    text-align: center;
}

body {
    font-family: 'Roboto Mono', monospace;
    min-height: 400px;
    background-image: url('https://www.alura.com.br/assets/img/imersoes/dev-2021/tabela-classificacao-bg.png');
    background-color: #111;
    background-size: 100%;
    background-position: center;
    background-repeat: no-repeat;
}

.container {
    text-align: center;
    padding: 20px;
    height: 100vh;
}

.page-title {
    color: #ffffff;
    margin: 0 0 5px;
}

.page-subtitle {
    color: #ffffff;
    margin-top: 5px;
}

.page-logo {
    width: 200px;
}

.alura-logo {
    width: 40px;
    position: absolute;
    top: 10px;
    right: 10px;
}

table {
    border: 2px solid white;
    border-collapse: collapse;
}

h1 {
    color: white;
}

th, tr, td {
    border: solid 1px white;
    color: white;
}
COD JAVASCRIPT
var paulo = {
  nome: "Paulo",
    vitorias: 2, 
      empates: 5,
        derrotas: 1,
          pontos: 0
}
var rafa = {nome: "Rafa",
            vitorias: 3,
            empates: 5,
            derrotas: 2,
            pontos: 0
  
}
//console.log(paulo.vitorias)
//console.log(rafa)


rafa.pontos = calculaPontos(rafa)
paulo.pontos = calculaPontos(paulo)


function calculaPontos (jogador){
  var pontos = (jogador.vitorias * 3)  + jogador.empates
  return pontos
   
}

var jogadores = [rafa, paulo]

exibirJogadoresNaTela(jogadores)

function exibirJogadoresNaTela(jogadores){
  var html = ""
  for(var i = 0; i < jogadores.length; i++){
 html += "<tr><td>" + jogadores[i].nome + "</td>"
 html += "<td>" + jogadores[i].vitorias + "</td>" 
 html += "<td>" + jogadores[i].empates + "</td>"
 html += "<td>" + jogadores[i].derrotas + "</td>"
 html += "<td>" + jogadores[i].pontos + "</td>"
 html += "<td><button onClick='adicionarVitoria(" + i + ")'>Vitória</button></td>"
 html += "<td><button onClick='adicionarEmpate(" + i + ")'>Empate</button></td>"
 html += "<td><button onClick='adicionarDerrota(" + i + ")'>Derrota</button></td></tr>"
    
  }
  var tabelaJogadores = document.getElementById("tabelaJogadores")
  tabelaJogadores.innerHTML = html
}

function adicionarVitoria(i){
 var jogador = jogadores[i]
 jogador.vitorias++
 jogador.pontos = calculaPontos(jogador)
  exibirJogadoresNaTela(jogadores)
}

function adicionarEmpate(i){
  var jogador = jogadores[i]
  jogador.empates++
  jogador.pontos = calculaPontos(jogador)
  exibirJogadoresNaTela(jogadores)
}
  
function adicionarDerrota(i){
var jogador = jogadores[i]
jogador.derrotas++
  exibirJogadoresNaTela(jogadores)
  
  
  

}
