🧠 Sistema de Classificação de Heróis (JavaScript)

Este repositório contém dois scripts em JavaScript que simulam sistemas de classificação de heróis com base em:

🏆 Número de vitórias e derrotas
⚡ Pontos de experiência (XP)
📌 1. Classificação por Vitórias
📖 Descrição

A função calcularRank recebe o número de vitórias e derrotas de um herói e:

Calcula o saldo de vitórias
Define o nível do herói com base nas vitórias
🧮 Lógica de Classificação
Vitórias	Nível
< 10	Ferro
11 – 20	Bronze
21 – 50	Prata
51 – 80	Ouro
81 – 90	Diamante
91 – 100	Lendário
≥ 101	Imortal
💻 Código
function calcularRank(vitorias, derrotas) { 
    let saldoVitorias = vitorias - derrotas;
    let nivel = " ";

    if (vitorias < 10) {
        nivel = "Ferro";
    } else if (vitorias >= 11 && vitorias <= 20) {
        nivel = "Bronze";
    } else if (vitorias >= 21 && vitorias <= 50) {
        nivel = "Prata";
    } else if (vitorias >= 51 && vitorias <= 80) {
        nivel = "Ouro";
    } else if (vitorias >= 81 && vitorias <= 90) {
        nivel = "Diamante";
    } else if (vitorias >= 91 && vitorias <= 100) {
        nivel = "Lendário";
    } else if (vitorias >= 101) {
        nivel = "Imortal";
    }

    return `O Herói tem de saldo de ${saldoVitorias} está no nível de ${nivel}`;
}

// Exemplo de uso:
let vitorias = 25;
let derrotas = 10;
console.log(calcularRank(vitorias, derrotas));
⚡ 2. Classificação por XP (Experiência)
📖 Descrição

Este script:

Gera um valor aleatório de XP
Classifica o herói com base nesse valor
🎯 Lógica de Classificação
XP	Nível
≤ 1000	Ferro
≤ 2000	Bronze
≤ 5000	Prata
≤ 8000	Ouro
≤ 9000	Ascendente
≤ 10000	Imortal
≤ 10001	Radiante
💻 Código
const hero = "nego brutus"

function randint(min, max) {
    return Math.floor(Math.random()* (max - min +1)) + min;
} 

let xp = randint(1, 13000);
const classificacao = (`O herói ${hero} está no nível  `)

switch (true) {
    case xp <= 1000:
        console.log(classificacao + "Ferro")
        break

    case xp <= 2000:
        console.log(classificacao + "Bronze")
        break

    case xp <= 5000:
        console.log(classificacao + "Prata")
        break

    case xp <= 8000:
        console.log(classificacao + "Ouro")
        break

    case xp <= 9000:
        console.log(classificacao + "Ascendente")
        break

    case xp <= 10000:
        console.log(classificacao + "Imortal")
        break

    case xp <= 10001:
        console.log(classificacao + "Radiante")
        break
}
🚀 Como Executar
Instale o Node.js (se ainda não tiver)
Salve os arquivos .js
Execute no terminal:
node nome-do-arquivo.js
🧩 Melhorias Futuras
 Transformar em API (Node + Express)
 Criar interface web (HTML/CSS/JS)
 Persistência de dados (banco de dados)
 Testes automatizados
📌 Observações Técnicas
Uso de estruturas condicionais (if/else e switch)
Geração de números aleatórios
Interpolação de strings (template literals)
Lógica de classificação baseada em regras
