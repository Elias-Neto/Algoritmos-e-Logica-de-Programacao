# 🛠 Aula 13 - Funções

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver e executar os algoritmos em **Portugol**.

<br>

## **Rotina (Parte 02) - Funções**

<br>

**Relembrando**

- rotina é um procedimento repetitivo

- rotinas são utéis para evitarmos repetição de código

<br>

**Procedimento x Função**

- Nos ***Procedimentos*** não se retorna um valor, neles ocorre simplesmente a execução de
um bloco de código

- Nas ***Funções*** se retorna um valor, nelas um bloco de código é executado mas o objetivo
é retornar um valor ao final da função.

<br>

**Sintaxe da Estrutura**

````
Funcao nomeDaFuncao(): tipoDaFuncao
inicio
  Bloco
  Retorne()
FimFuncao
````

<br>

**Exemplo - Somar Dois Números (Procedimento x Função) :**

````
algoritmo "somar dois números com PROCEDIMENTO"

var
  numero1, numero2: Inteiro
  
  Procedimento Soma(A, B: Inteiro)
  Inicio
     Escreval("A soma entre ", A, " e ", B, " é igual a ", A+B)
  FimProcedimento

inicio
  Escreva("Digite o primeiro valor: ")
  Leia(numero1)
  Escreva("Digite o segundo valor: ")
  Leia(numero2)
  Soma(numero1, numero2)

fimalgoritmo
````

````
algoritmo "somar dois números com FUNÇÃO"

var
  numero1, numero2, soma: Inteiro
  
  Funcao Soma(A, B: Inteiro): Inteiro
  Inicio
    Retorne(A+B)
  FimFuncao

inicio
  Escreva("Digite o primeiro valor: ")
  Leia(numero1)
  Escreva("Digite o segundo valor: ")
  Leia(numero2)
  soma <- Soma(numero1, numero2)
  Escreval("A soma entre ", numero1, " e ", numero2, " é igual a ", soma)

fimalgoritmo
````

## **Passagem de Parâmetro**

- Assim como nos procedimentos, em funções você tamném pode utilizar parâmetros.

- O funcionamento e o tipo de passagens de parâmetros dos procedimentos é o mesmo para as funções.

<br>

**Relembrando**

- Parâmetros são variáveis que estão recebem alguma coisa como referência.

<br>

## **Passagem de Parâmetro Por Valor**

<br>

**Relembrando**

- É um tipo de passagem na qual os parâmetros do procedimento recebem valores como referência

- OBS❕ Não use o mesmo nome da variável referência no parâmetro.

<br>

### 🏋️‍♂️ **Exercício Prático - Verificador Par/Ímpar :**

- Desenvolva um algoritmo que leia um número, verifique e informe se ele é par ou ímpar.

- Utilize uma função para realizar essa verificação.

````
algoritmo "VERIFICADOR PAR/ÍMPAR"
var
  numero: Inteiro
  retorno: Caractere
   
Funcao ParOuImpar(N: Inteiro): Caractere
Inicio
  Se (N%2 = 0) entao
    Retorne("PAR")
  senao
    Retorne("ÍMPAR")
  FimSe
FimFuncao

inicio
  Escreva("Digite um número: ")
  Leia(numero)
  retorno <- ParOuImpar(numero)
  EscrevaL("O número ", numero, " é um valor ", retorno)
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Fatorial de Um Número :**

- Crie um algoritmo que leia um número, calcule e informe o fatorial desse número.

- Utilize uma função para realizar essa cálculo.

````
algoritmo "FATORIAL DE UM NÚMERO"
var
  numero, F: Inteiro

Funcao Fatorial(N:Inteiro): Inteiro
var
  contador, resultado: Inteiro
Inicio
  Resultado <- 1
  Para Contador <- 1 ate N faca
    resultado <- resultado * Contador
  FimPara
  Retorne resultado
FimFuncao

inicio
  Escreva("Digite um número: ")
  Leia(numero)
  F <- Fatorial(numero)
  Escreval("O valor de ", numero, "! è igual a ", F)
fimalgoritmo
````

<br>

## **Passagem de Parâmetro Por Referência**

<br>

**Relembrando**

- Nesse tipo de passagem, os parâmetros receberão a própria variável como referência.

- Podemos fazer uma analogia e dizer que os parâmetros receberão o 'endereço' da variável 
como referência.

<br>

### 🏋️‍♂️ **Exercício Prático - Sequência de Fibonacci :**

- Desenvolva um algoritmo que calcule e exiba na tela os 15 primeiros números da sequência de fibonacci.

- Utilize uma função para realizar esse cálculo.

````
algoritmo "SEQUÊNCIA DE FIBONACCI"
var
  contador, valor1, valor2, valor3: Inteiro

Funcao ProximoFibonacci(var V1, V2: Inteiro):Inteiro
var
  V3: Inteiro
Inicio
  V3 <- V1 + V2
  V1 <- V2
  V2 <- V3
  Retorne(V3)
FimFuncao

inicio
  Escreva(valor1)
  valor2 <- 1
  Escreva(valor2)
  Para contador <- 3 ate 15 faca
    valor3 <- ProximoFibonacci(valor1, valor2)
    Escreva(valor3)
  FimPara
fimalgoritmo
````

<br>

## **Funções do Visualg - valor carctere**

<br>

 **site <- "CursoEmVideo"**

 <br>

Função | Retorno | O que faz?
:--------- | :------: | -------:
Compr(site) | 12 | Retorna o comprimento de uma string
Copia(site, 6, 2) | Em | Retorna a copia de uma string contando a partir de um intervalo (string, inicioDoIntervalo, quantidadeDeLetras)
Maiusc(site) | CURSOEMVIDEO | Coloca todas as letras de uma string em maiúsculas
Minusc(site) | cursoemvideo | Coloca todas as letras de uma string em minúsculas
Pos("Video", site) | 8 | Retorna a posição de uma determinada string ou letra dentro de uma string maior
Asc("C") | 67 | Retorna o código específico de uma letra
Carac("67") | C | Retorna a letra específica de um código

<br>

### 🏋️‍♂️ **Exercício Prático - Analisador de Nomes :**

- Desenvolva um algoritmo, utilizando as funções do visualg, que leia o nome do usuário e:
  
  - Informe o total de letras do nome
  
  - Exiba o nome em letras maiúsculas
  
  - Exiba o nome em letras minúsculas
  
  - Informe a primeira letra do nome
  
  - Informe a última letra do nome
  
  - Informe a posição da letra "A" no nome
  
  - Informe a código correspondente a letra "A"
  
  - Informe a a letra correspondnete ao código 65

  - Monte e exiba na tela o nome do usuário ao contrário

````
algoritmo "ANALISADOR DE NOMES"
var
  nome: Caractere
  Contador: Inteiro
inicio
  Escreva("Digite seu nome: ")
  Leia(nome)
  Escreval("Total de letras do seu nome é ", Compr(nome))
  Escreval("Seu nome em maiúsculas ", Maiusc(nome))
  Escreval("Seu nome em minúsculas é ", Minusc(nome))
  Escreval("A primeira letra do seu nome é ", Copia(Maiusc(nome), 1, 1))
  Escreval("A última letra do seu nome é ", Copia(Maiusc(nome), Compr(nome), 1))
  Escreval("Seu nome tem a letra A na posição ", Pos("A", Maiusc(nome)))
  Escreval("O código da letra A é ", Asc("A"))
  Escreval("A letra de código 65 é ", Carac(65))
  Escreva("Seu nome ao contrário é ")
  Para Contador <- Compr(nome) ate 1 passo -1 faca
    Escreva(Copia(Maiusc(nome), Contador, 1))
  FimPara
fimalgoritmo
````

<br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>