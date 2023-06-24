# Challenge-CubosAcademy-iFOOD-
Challenge-CubosAcademy-iFOOD 

//Desafio 05/05: Acesso ao chefão
// Iniciante-Difícil

// VIA EXPLICADA / DETALHADA:

// 01 - ARRAYS DE STRINGS PARA TESTES - PANORAMAS POSSÍVEIS DE FALHA:
//*retirar as "//OK" do início da Array de teste.

let itensColetados = ["capa", "arco", "flecha", "machado", "escudo", "comida", "sapato", "capacete"]; //Modelo do exercício com várias opções
//OKlet itensColetados = ["capa","espada", "arco", "flecha", "machado", "escudo", "comida","espada", "sapato", "capacete"]; //Modelo com Muitas opções e Item Necessário2 Repetido
//OKlet itensColetados = ["machado", "espada", "sapato"]; // Apenas Todos Obrigatórios.
//OKlet itensColetados = ["machado", "oculos"]; // Só dois ítens Obrigatórios.
//OKlet itensColetados = ["machado", "espada"]; // Só um item obrigatório e um não obrigatório.
//OKlet itensColetados = ["machado", "espada", "sapato", "corda"]; // Todos Obrigatórios em ordem + 1.
//ERROlet itensColetados = ["machado", "espada", "SAPATO", "corda"]; //Todos Obrigatórios em ordem + 1 e um com caixa alta.
//OKlet itensColetados = ["machado", "corda", "espada", "escada", "sapato"]; / /Obrigatórios e Vários Extras.
//OKlet itensColetados = ["corda", "espada", "escada", "sapato"]; // Apenas dois Obrigatórios.
//OKlet itensColetados = ["espada", "escada", "sapato", "corda", "oculos"]; // Apenas dois Obrigatórios.
console.log("Itens Coletados:", itensColetados)

// 02 - VARIÁVEIS DE STRINGS:
let itemNecessario1 = "machado";
console.log("Item Necessário 1:", itemNecessario1)

let itemNecessario2 = "espada";
console.log("Item Necessário 2:", itemNecessario2)

let itemNecessario3 = "sapato";
console.log("Item Necessário 3:", itemNecessario3)

// 03 - RESOLUÇÃO DO CÓDIGO:
//Obs.: Esse código está com falha se a palavra for escrita com Caixa Alta, porém não foi exigido no desafio esse reparo:

// Variáveis Contadoras dos Ítens (um pra cada):
let contadorItemNecessario1 = 0; 
let contadorItemNecessario2 = 0;
let contadorItemNecessario3 = 0;

// Usando FOR e contador .length (para fazer correr a array):
for (let item = 0; item < itensColetados.length; item++) {
  let itemEscrito = itensColetados[item];
  
  if (itemEscrito === itemNecessario1) {
    contadorItemNecessario1++;
    console.log(contadorItemNecessario1) // Para mostrar a parcial do contador 1
    
  } else if (itemEscrito === itemNecessario2) {
    contadorItemNecessario2++;
    console.log(contadorItemNecessario2) // Para mostrar a parcial do contador 2
    
  } else if (itemEscrito === itemNecessario3) {
    contadorItemNecessario3++;
    console.log(contadorItemNecessario3) // Para mostrar a parcial do contador 3
  }
}

// Para mostrar o total dos contadores:
console.log("Contador Item Necessário 1: " + contadorItemNecessario1);
console.log("Contador Item Necessário 2: " + contadorItemNecessario2);
console.log("Contador Item Necessário 3: " + contadorItemNecessario3);

// Criado Contador Geral para verificar se temos os 3 ítens obrigatórios:
let contadorGeral = contadorItemNecessario1 + contadorItemNecessario2 + contadorItemNecessario3
console.log("Contador Geral:", contadorGeral) // Para mostrar a parcial do contador geral

// Se houver itens obrigatórios repetidos, o jogador também poderá enfrentar!
if (contadorGeral >= 3) {
  console.log("PODE ENFRENTAR")
} else {
  console.log("NAO PODE ENFRENTAR")
}

/////////////////////////////////////////////////////////////////////
//VIA RESUMIDA:
/*
let itensColetados = ["capa", "arco", "flecha", "machado", "escudo", "comida", "sapato", "capacete"];

let itemNecessario1 = "machado";
let itemNecessario2 = "espada";
let itemNecessario3 = "sapato";

let contadorItemNecessario1 = 0; 
let contadorItemNecessario2 = 0;
let contadorItemNecessario3 = 0;

for (let item = 0; item < itensColetados.length; item++) {
  let itemEscrito = itensColetados[item];
  
  if (itemEscrito === itemNecessario1) {
    contadorItemNecessario1++;
  } else if (itemEscrito === itemNecessario2) {
    contadorItemNecessario2++;
  } else if (itemEscrito === itemNecessario3) {
    contadorItemNecessario3++;
  }
}

let contadorGeralItensNecessarios = contadorItemNecessario1 + contadorItemNecessario2 + contadorItemNecessario3

if (contadorGeralItensNecessarios >= 3) {
  console.log("PODE ENFRENTAR")
} else {
  console.log("NAO PODE ENFRENTAR")
}
*/

