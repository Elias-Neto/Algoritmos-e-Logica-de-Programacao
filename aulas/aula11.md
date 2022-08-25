# 🔁 Aula 11 - Estruturas de Repetição (Parte 03)

<br>

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver algoritmos em **Portugol**.

<br>

> 🖖 Essas anotações foram feitas a partir das aulas do professor **Gustavo Guanabara**. <br>
> 👉 Link para acessar as vídeo-aulas e os materiais do curso: https://www.cursoemvideo.com/curso/curso-de-algoritmo/
 
 <br>

## **Estrutura de Repetição - "Para"**

- É uma estrutura que gira em torno de **uma condição**.

- Nessa estrutura, *o teste lógico é feito no __início__*.

- Portanto, é utilizada quando se sabe quantas vezes vai se repetir o loop.

- É uma estrutura que utiliza **menos linhas** do que as outras (Enquanto e Repita).

- Também chamada de estrutura de repetição com **variável de controle**.

<br>

### Sintaxe da Estrutura

- Você consegue numa única linha: referenciar uma variável (chamada de variável de controle), definir o início, o fim e o salto da contagem.

````
Para (variavel) <- (inicio) ate (fim) passo (salto) faca
  Bloco
FimPara
````

Exemplo:

````
// contar de 1 ate 10

Para contador <- 1 ate 10 passo 1 faca
  EscrevaL(contador)
FimPara

// contar de 10 ate 1 

Para contador <- 10 ate 1 passo -1 faca
  EscrevaL(contador)
FimPara
````

<br>

### 🏋️‍♂️ **Exercício Prático - Contagem Regressiva Com Números Pares :**

<br>

- Crie um algoritmo que leia um número e faça a contagem regressiva até zero utilizando apenas números pares.

````
algoritmo "Contagem Regressiva Com Números Pares"

var
  contador, numero: Inteiro
  
inicio
  Escreva("Digite um número: ")
  Leia(numero)
  
  Se  (numero % 2 = 1) entao
    numero <- numero -1
  FimSe
  
  Para numero <- valor ate 0 passo -2 faca
    Escreval(numero)
  FimPara
  
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Quantos Valores Estão Entre 0 e 10? :**

<br>

- Desenvolva um programa que leia seis números e informe quantos estão entre 0 e 10.

````
algoritmo "Quantos Valores Estão Entre 0 e 10?"

var
  contador, numero, de0ate10: Inteiro
  
inicio
  Para contador <- 1 ate 6 faca
    Escreva("Digite um número: ")
    Leia(numero)
    
    Se (numero >= 0) e (numero <= 10) entao
      de0ate10 <- de0ate10 + 1
    FimSe
  FimPara
  
  EscrevaL()
  Escreval("Ao todo foram ", de0ate10, " valores entre 0 e 10 ")
  
fimalgoritmo
````

- **ADICIONAL**: Exbir a soma dos números ímpares digitados.

````
algoritmo "Quantos Valores Estão Entre 0 e 10?"

var
  contador, numero, de0ate10, somaImpares: Inteiro
  
inicio
  Para contador <- 1 ate 6 faca
    Escreva("Digite um número: ")
    Leia(numero)

    Se (numero >= 0) e (numero <= 10) entao
      de0ate10 <- de0ate10 + 1
    FimSe

    Se (numero % 2 = 1) entao
      somaImpares <- somaImpares + numero
    FimSe
  FimPara
  
  EscrevaL()
  Escreval("Ao todo foram ", de0ate10, " valores entre 0 e 10 ")
  Escreval("A soma dos números ímpares digitados é igual a ", somaImpares)
  
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Combinações (Aninhando Estruturas de Repetição) :**

<br>

- Desenvolva um programa que combine três números (1, 2 e 3), agrupados dois a dois:

1,1 ... 2,1 ... 3,1
 
1,2 ... 2,2 ... 3,2

1,3 ... 2,3 ... 3,3


````
algoritmo "Combinações"

var
  contador1, contador2: Inteiro
  
inicio
  Para contador1 <- 1 ate 3 faca
    Para contador2 <- 1 ate 3 faca
      Escreval(contador1, contador2)
    FimPara
    EscrevaL()
  FimPara
  
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Sequência de Fibonacci :**

<br>

- Desenvolva um algoritmo que calcule e exiba os 15 primeiros termos da sequência de fibonacci.

- A sequência de fibonacci consiste numa sequência de números na qual o primeiro e o segundo elemento
são igual a 1 e os elementos seguintes são originados pela soma de seus dois antecessores, observe:

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

### 🏋️‍♂️ **Exercício Prático - Analisador de Números :**

<br>

- Faça um programa que leia cinco números e:

  - Calcule e informe a soma de todos os numeros;

  - Calcule e informe a média entre todos os numeros;

  - Calcule e informe a soma de todos os numeros pares;
  
  - Detecte e informe quantos numeros são divisíveis por cinco;

  - Detecte e informe quantos numeros são nulos;

````
algoritmo "Analisador de Números"

var
  contador, numero, soma, divisiveisPor5, numerosNulo, somaPar: Inteiro
  media: Real

inicio
  Para contador <- 1 ate 5 faca
    Escreva("Digite o ", contador, "° numero: ")
    Leia(numero)

    soma <- soma + numero

    media <- soma/5

    Se (numero % 5 = 0) entao
      divisiveisPor5 <- divisiveisPor5 + 1
    FimSe

    Se (numero = 0) entao
      numerosNulo <- numerosNulo + 1
    FimSe

    Se (numero % 2 = 0) entao
      somaPar <- somaPar + numero
    FimSe
  FimPara
  
  EscrevaL()
  Escreval("A soma entre os números digitados é ", soma)
  Escreval("A média entre os números digitados é ", media:5:2)
  Escreval("A quantidade de numeros divisíveis por cinco que digitados é ", divisiveisPor5)
  Escreval("A quantidade de números nulos digitados é ", numerosNulo)
  Escreval("A soma dos números pares digitados é ", somaPar)

fimalgoritmo
````

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>

<br>

<a href="../README.md">Voltar</a>