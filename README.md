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


