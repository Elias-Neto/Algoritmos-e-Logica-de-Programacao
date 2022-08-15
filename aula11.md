# 🔁 Aula 11 - Estruturas de Repetição (Parte 03)

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver e executar os algoritmos em **Portugol**.

<br>

## **Estrutura de Repetição "Para"**

- gira em torno de uma condição
- *o teste lógico é feito no **início** da estrutura*
- é utilizado quando se sabe quantas vezes vai se repetir o loop
- utiliza poucas linhas (ja vem com a atribuição e o incremento incluido)
- também chamada de estrutura de repetição com variável de controle

Sintaxe da Estrutura

````
Para (variavel) <- (inicio) ate (fim) passo (salto) faca
  Bloco
FimPara
````

Exemplo:

````
// contar de 1 ate 10

Para contador <- 1 ate 10 passo 1 faca
  EscrevaL(C)
FimPara

// contar de 10 ate 1 

Para contador <- 10 ate 1 passo -1 faca
  EscrevaL(C)
FimPara
````

<br>

### 🏋️‍♂️ **Exercício Prático - Contagem Regressiva Com Números Pares :**

- Crie um algoritmo que leia um número e faça a contagem regressiva desse número até zero
utilizando apenas números pares.

````
algoritmo "Contagem Regressiva Com Números Pares"
var
  contador, valor: Inteiro
inicio
  Escreva("Digite um número: ")
  Leia(valor)
  Se  (valor % 2 = 1) entao
    valor <- valor -1
  FimSe
  Para contador <- valor ate 0 passo -2 faca
    Escreval(contador)
  FimPara
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Quantos Valores Estão Entre 0 e 10? :**

- Desenvolva um programa que leia seis números e, no final, informe quantos números estão
entre 0 e 10.

````
algoritmo "quantos valores estão entre 0 e 10"
var
  contador, valor, de0ate10: Inteiro
inicio
  Para contador <- 1 ate 6 faca
    Escreva("Digite um valor: ")
    Leia(valor)
    Se (valor >= 0) e (valor <= 10) entao
      de0ate10 <- de0ate10 + 1
    FimSe
  FimPara
  Escreval("Ao todo foram ", de0ate10, " valores entre 0 e 10 ")
fimalgoritmo
````

- **adicional:** exebir a soma dos números ímpares

````
algoritmo "quantos valores estão entre 0 e 10"
var
  contador, valor, de0ate10, somaImpares: Inteiro
inicio
  Para contador <- 1 ate 6 faca
    Escreva("Digite um valor: ")
    Leia(valor)
    Se (valor >= 0) e (valor <= 10) entao
      de0ate10 <- de0ate10 + 1
    FimSe
    Se (valor % 2 = 1) entao
      somaImpares <- somaImpares + valor
    FimSe
  FimPara
  Escreval("Ao todo foram ", de0ate10, " valores entre 0 e 10 ")
  Escreval("Nesse intervalo, a soma de impares foi ", somaImpares)
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Combinações (Aninhando Estruturas de Repetição) :**

- Desenvolva um programa que combine três números, agrupados dois a dois.

- Exemplo utilizando os números 1, 2 e 3 :

1,1 ... 2,1 ... 3,1
 
1,2 ... 2,2 ... 3,2

1,3 ... 2,3 ... 3,3


````
algoritmo "combinações"
var
  contador1, contador2: Inteiro
inicio
  Para contador1 <- 1 ate 3 faca
    Para contador2 <- 1 ate 3 faca
      Escreval(contador1, contador2)
    FimPara
  FimPara
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Sequência de Fibonacci :**

- Desenvolva um algoritmo que calcule e exiba os 15 primeiros termos da sequência de fibonacci.

- A sequência de fibonacci consiste em uma sequência de números na qual o primeiro e segundo elemento
é o 1 e o e os elementos seguintes são originados pela soma de seus dois antecessores, observe:

  - 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 987, 1597, 2584, 4181...

````
algoritmo "Sequência de Fibonacci"
var
  contador, valor1, valor2, valor3: Inteiro
inicio
  valor1 <- 1
  Escreva(valor1)
  valor2 <- 1
  Escreva(valor2)
  Para contador <- 3 ate 15 faca
    valor3 <- valor1 + valor2
    Escreva(valor3)
    valor1 <- valor2
    valor2 <- valor3
  FimPara
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Analisador de Valores :**

- Faça um programa que leia cinco números e:
  - calcule e informe a soma de todos os valores
  - calcule e informe a média entre todos os valores
  - detecte e informe quantos valores são divisíveis por cinco
  - detecte e informe quantos valores são nulos
  - calcule e informe a soma de todos os valores pares

````
algoritmo "Analisador de Valores"
var
  contador, valor, soma, divisiveisPor5, valoresNulo, valoresPar: Inteiro
  media: Real
inicio
  Para contador <- 1 ate 5 faca
    Escreva("Digite o ", contador, "° Valor: ")
    Leia(valor)
    soma <- soma + valor
    media <- soma/5
    Se (valor % 5 = 0) entao
      divisiveisPor5 <- divisiveisPor5 + 1
    FimSe
    Se (valor = 0) entao
      valoresNulo <- valoresNulo + 1
    FimSe
    Se (valor % 2 = 0) entao
      valoresPar <- valoresPar + valor
    FimSe
  FimPara
  Escreval("A soma entre os valores é ", soma)
  Escreval("A média entre os valores é ", media)
  Escreval("Valores divisíveis por cinco: ", divisiveisPor5)
  Escreval("Valores nulos: ", valoresNulo)
  Escreval("A soma dos valores pares é ", valoresPar)
fimalgoritmo
````

<br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>