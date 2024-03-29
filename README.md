1. Imagine que você está criando um sistema escolar para obter a média dos alunos da sala. Foram realizadas 3 avaliações com nota máxima de 10 pontos. Aline, tirou na primeira nota o total de 8 pontos, na segunda nota tirou 9 pontos e na terceira nota 7 pontos. 
**Escreva um programa que receba as notas, faça o cálculo da média e imprima o resultado final da média.**

``` js
// Função para calcular a média
function calcularMedia(numero1, numero2, numero3) {
    var soma = numero1 + numero2 + numero3;
    var media = soma / 3;
    return media;
}

// Pedindo ao usuário para digitar seu nome
var nome = prompt("Digite seu nome:");

// Pedindo ao usuário para digitar os três números separadamente
var numero1 = parseFloat(prompt("Olá, " + nome + "! Digite o primeiro número:"));
var numero2 = parseFloat(prompt("Agora digite o segundo número:"));
var numero3 = parseFloat(prompt("Por fim, digite o terceiro número:"));

// Calculando a média
var media = calcularMedia(numero1, numero2, numero3);

// Mostrando o resultado da média para o usuário
alert("Olá, " + nome + "! A média dos números digitados é: " + media);
```

2. Tais está participando de um sorteio na Loteria e recebeu uma lista de números aleatórios para poder apostar. Os números foram: 15, 8, 90, 75, 102, 6 e 2. Por ser bastante cautelosa, ela gostaria de saber qual é o menor número e qual é o maior número. 
**Ajude Tais e escreva um programa que faça a lógica de programação para organização dos números, receba os números da lista e imprima na tela o menor número digitado e o maior número digitado.**

``` js
// Função para encontrar o menor número em uma lista
function encontrarMenorNumero(lista) {
    var menor = lista[0];
    for (var i = 1; i < lista.length; i++) {
        if (lista[i] < menor) {
            menor = lista[i];
        }
    }
    return menor;
}

// Função para encontrar o maior número em uma lista
function encontrarMaiorNumero(lista) {
    var maior = lista[0];
    for (var i = 1; i < lista.length; i++) {
        if (lista[i] > maior) {
            maior = lista[i];
        }
    }
    return maior;
}

// Pedindo ao usuário que digite os números separados por vírgula
var numerosString = prompt("Digite os números separados por vírgula:");

// Convertendo a string de entrada em uma lista de números
var numeros = numerosString.split(",").map(function(item) {
    return parseInt(item.trim());
});

// Encontrando o menor e o maior número na lista
var menorNumero = encontrarMenorNumero(numeros);
var maiorNumero = encontrarMaiorNumero(numeros);

// Mostrando os resultados ao usuário
alert("O menor número digitado é: " + menorNumero + "\nO maior número digitado é: " + maiorNumero);
```
