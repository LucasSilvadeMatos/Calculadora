# Calculadora
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=, initial-scale=1.0" />
    <title>sem titulo</title>
    <link rel="stylesheet" href="CSS BASICO/stilecalculadora.css" />
  </head>
  <body>
    <div class="box">
      <h1>Calculadora</h1>
      <div class="tela"></div>
      <table>
        <tr>
          <td><button onclick="clean()" ('C')">C</button></td>
          <td><button onclick="back()"><</button></td>
          <td><button onclick="inserir('/')">/</button></td>
          <td><button onclick="inserir('*')">x</button></td>
        </tr>
        <tr>
          <td><button onclick="inserir('7')">7</button></td>
          <td><button onclick="inserir('8')">8</button></td>
          <td><button onclick="inserir('9')">9</button></td>
          <td><button onclick="inserir('-')">-</button></td>
        </tr>
        <tr>
          <td><button onclick="inserir('4')">4</button></td>
          <td><button onclick="inserir('5')">5</button></td>
          <td><button onclick="inserir('6')">6</button></td>
          <td><button onclick="inserir('+')">+</button></td>
        </tr>
        <tr>
          <td><button onclick="inserir('1')">1</button></td>
          <td><button onclick="inserir('2')">2</button></td>
          <td><button onclick="inserir('3')">3</button></td>
          <td rowspan="2">
            <button
              style="height: 102px; background-color: #ff7300" onclick="somar()"
              onclick="inserir('=')"
            >
              =
            </button>
          </td>
        </tr>
        <tr>
          <td colspan="2">
            <button style="width: 102px" onclick="inserir('0')">0</button>
          </td>
          <td><button onclick="inserir('.')">.</button></td>
        </tr>
      </table>
      <span>&copy;lucasdev</span>
    </div>
  </body>
  <script src="calculadora.js"></script>
</html>
            
            CSS
            
const primeiroNome = prompt("Informe o primeiro nome do recruta:?");
const sobrenome = prompt("Informe o sobrenome do recruta:?");
const anoDeNascimento = prompt("Informe o ano de nascimento do recruta:?");

alert(
  "Recruta cadastrado com sucesso!\n" +
    "\nNome completo:" +
    primeiroNome +
    " " +
    sobrenome +
    "\nIdade: " +
    (2023 - anoDeNascimento)
);

function inserir(num) {
  document.querySelector(".tela").innerHTML += num;
}

function clean() {
  document.querySelector(".tela").innerHTML = "";
}

function back() {
  let tela = document.querySelector(".tela").innerHTML;
  document.querySelector(".tela").innerHTML = tela.substring(
    0,
    tela.length - 1
  );
}

function somar() {
  let tela = document.querySelector(".tela").innerHTML;
  document.querySelector(".tela").innerHTML = eval(tela);
  if (tela) {
    document.querySelector(".tela").innerHTML = eval(tela);
  } else {
    document.querySelector(".tela").innerHTML = "nenhum comando...";
  }
}
