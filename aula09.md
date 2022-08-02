# Aula 09 - Estruturas de Repetição (Parte 01) 🔁

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver algoritmos em **Portugol**.

<br>

## **Estrutura de Repetição "Enquanto"**

- gira em torno de uma condição
- *o teste lógico é feito no **início** da estrutura*

Sintaxe da Estrutura:

- enquanto tal condição for verdadeira faça tal coisa

````
Enquanto (expressão) faça
  Bloco
FimEnquanto
````

Exemplo:

- Enquanto não arrumar seu quarto está de castigo

````
Enquanto (não arrumar quarto) faça
  castigo
FimEnquanto
liberado
````

<br>

### 🏋️‍♂️ **Exercício Prático - Contar de 0 até 10 :**

- Crie um algoritmo que conte de 0 até 10

````
algoritmo "contar de 0 ate 10"
var
   contador:Inteiro
inicio
   contador <- 0
   Enquanto (contador <= 10) faca
      Escreval(contador)
      contador <- contador +  1
   FimEnquanto
   Escreval("Terminei de contar")
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Contar de 10 até 0 :**

- Crie um algoritmo que conte de 10 até 0

````
algoritmo "contar de 10 ate 0"
var
   contador:Inteiro
inicio
   contador <- 10
   Enquanto (contador >= 0) faca
      Escreval(contador)
      contador <- contador -  1
   FimEnquanto
   Escreval("Terminei de contar")
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Contar de 0 até onde o usuário quiser:**

- Crie um algoritmo que conte de 0 até onde o usuário quiser

````
algoritmo "contar de 0 ate onde o usuario quiser"
var
   inici0, fim: Inteiro
inicio
   Escreva("Até onde o você quer contar? ")
   Leia(fim)
   inici0 <- 0
   Enquanto (inici0 <= fim) faca
      Escreval(inici0)
      inici0 <- inici0 +  1
   FimEnquanto
   Escreval("Terminei de contar")
fimalgoritmo
````

- **adicional:** pergunte ao usuário o valor do salto dessa conta

````
algoritmo "contar de 0 ate onde o usuario quiser"
var
   inici0, fim, salto: Inteiro
inicio
   Escreva("Até onde o você quer contar? ")
   Leia(fim)
   Escreva("Qual valor do salto? ")
   Leia(salto)
   inici0 <- 0
   Enquanto (inici0 <= fim) faca
      Escreval(inici0)
      inici0 <- inici0 + salto
   FimEnquanto
   Escreval("Terminei de contar")
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Ler 10 números e somar-los :**

- Crie um algoritmo que leia 10 números e some-os

````
algoritmo "ler 10 numeros e soma-los"
var
   contador, numero, soma: Inteiro
inicio
   soma <- 0
   contador <- 1
   Enquanto (contador <= 5) faca
      Escreva("Digite o ", contador, "°. valor: ")
      Leia(numero)
      soma <- soma + numero
      contador <- contador + 1
   FimEnquanto
   Escreval("A soma de todos os valores é ", soma)
fimalgoritmo
````

- **adicional:** mostrar qual foi o maior e o menor número digitado

````
algoritmo "ler 10 numeros e soma-los"
var
   contador, numero, soma, menor, maior: Inteiro
inicio
   soma <- 0
   contador <- 1
   Enquanto (contador <= 5) faca
      Escreva("Digite o ", contador, "°. valor: ")
      Leia(numero)
      Se (contador = 1) entao
         menor <- numero
      FimSe
      Se (numero > maior) entao
         maior <- numero
      FimSe
      Se (numero < menor) entao
         menor <- numero
      FimSe
      soma <- soma + numero
      contador <- contador + 1
   FimEnquanto
   Escreval("A soma de todos os valores é ", soma)
   Escreval("O maior valor digitado foi ", maior)
   Escreval("O menor valor digitado foi ", menor)
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Fazer conversão de moedas 4x :**

- Faça um algoritmo que solicite ao usuário um valor em reais e converta esse valor para
dólar, faça com que isso se repita 4 vezes.

````
algoritmo "conversao de moeda 4x"
var
   reais, dolar: Real
   contador: Inteiro
inicio
   contador <- 1
   Enquanto (contador <= 4) faca
      Escreva("Qual o valor em R$? ")
      Leia(reais)
      dolar <- reais / 5.2
      EscrevaL("O valor connvertido em U$", dolar:5:2)
      contador <- contador + 1
   FimEnquanto
 fimalgoritmo
````

- **adicional:** perguntar ao usuário quantas conversões serão realizadas

````
algoritmo "conversao de moeda 4x"
var
   reais, dolar: Real
   contador, conversoes: Inteiro
inicio
   contador <- 1
   Escreva("Deseja relaizar quantas conversões? ")
   Leia(conversoes)
   Enquanto (contador <= conversoes) faca
      Escreva("Qual o valor em R$? ")
      Leia(reais)
      dolar <- reais / 5.2
      EscrevaL("O valor connvertido em U$", dolar:5:2)
      contador <- contador + 1
   FimEnquanto
 fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Contador Inteligente :**

- Crie um programa que leia o início e o fim da contagem, detecte se ela é progressiva ou
regressiva e realize a contagem.

````
algoritmo "EXERCÍCIO 01 - CONTAGEM INTELIGENTE "
var
   ini, fim: Inteiro
inicio
   Escreval("CONTAGEM INTELIGENTE")
   Escreval("--------------------")
   Escreva("Início: ")
   Leia(ini)
   Escreva("Fim: ")
   Leia(fim)
   Escreval("--------------------")
   Escreval("      CONTANDO      ")
   Escreval("--------------------")
   Se (fim > ini) entao
      Enquanto (ini <= fim) faca
         Escreva(ini, (".. "))
         ini <- ini + 1
      FimEnquanto
   senao
      Enquanto (fim <= ini) faca
         Escreva(ini, (".. "))
         ini <- ini -1
      FimEnquanto
   FimSe
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Melhor Aluno da Turma :**

- Desenvolva um programa que leia a quantidade de alunos em uma turma, o nome e a nota 
de cada aluno, detecte e informe qual foi o aluno(a) com o melhor aproveitamente e a sua 
nota.

````
algoritmo "melhor aluno da turma"
var
  alunos, contador: Inteiro
  nome, melhorAproveitamento: Caractere
  nota, melhorNota: Real
inicio
  contador <- 1
  Escreval("------------------------")
  Escreval(" Escola Santa Paciência ")
  Escreval("------------------------")
  Escreva("Quantos alunos a turma tem? ")
  Leia(alunos)
  Enquanto (contador <= alunos) faca
    Escreval("-----------------")
    Escreval("ALUNO(A) ", contador)
    Escreva("Nome do aluno(a): ")
    Leia(nome)
    Escreva("Nota de ", nome, ": ")
    Leia(nota)
    Se (nota > melhorNota) entao
        melhorNota <- nota
        melhorAproveitamento <- nome
    FimSe
    contador <- contador + 1
  FimEnquanto
  Escreval("-----------------")
  Escreval("O melhor aproveitamento foi de ", melhorAproveitamento, " com a nota ", melhorNota:3:1)
FimAlgoritmo
fimalgoritmo
````