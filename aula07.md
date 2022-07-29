# Aula 07 - Estruturas Condicionais (Parte 01) 🔀

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver algoritmos em **Portugol**.

> Nessa aula, a gente começa a se perguntar "e se acontecer tal coisa..."

<br>

## ➡ **Estrutura Condicional Simples**

* é uma estrutura que gira em torno de uma única condição 
* possui um único caminho: se a condição for verdadeira, execute o bloco

Sintaxe da estrutura: 

* se *acontecer tal coisa* então *faça aquilo*

````
  Se (expressao) entao
    Bloco
  FimSe
````

Exemplo:

* Se ***eu tiver dinheiro*** então ***vou viajar para Disney***

````
algoritmo "condicional simples"
var
  dinheiro: Real
inicio
  Escreva("Quanto dinheiro eu tenho? R$")
  Leia(dinheiro)
  Se (dinheiro >= 10000) entao
    EscrevaL("Partiu Disney!")
  FimSe
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Aprimorar o Algoritmo da Idade :**

* Faça um programa que pergunte em qua ano estamos e em quano o usuário nasceu (guarde 
esses valores dentro de variáveis), calcule a idade do usuário e exiba-a na tela. Se
a idade do usuário for maior que 21 anos, exiba uma mensagem informando que o usuário
já atingiu a maioridade. 

````
algoritmo "Cálculo Idade"
var
   anoAtual, anoNasc, idade: Real
inicio
     Escreva("Em que ano estamos? ")
     Leia(anoAtual)
     Escreva("Em que ano você nasceu? ")
     Leia(anoNasc)
     idade <- anoAtual - anoNasc
     Escreva("Atualmente, você tem ", idade, " anos")
     Se (idade >= 21) entao
        Escreval(" e já atingiu a maioridade")
     FimSe
fimalgoritmo
````

<br>

## 🔀 **Estrutura Condicional Composta**

* é uma estrutura que também gira em torno de uma única condição 
* possui dois caminhos: se a condição for verdadeira, execute bloco x, senão, 
execute o bloco y

Sintaxe da estrutura: 

* se *acontecer tal coisa* então *faça isso* senão *faça aquilo*

````
  Se (expressao) entao
    BlocoX
  senao
    BlocoY
  FimSe
````

Exemplo:

* Se ***eu tiver dinheiro*** então ***vou viajar para Disney*** senão ***vou ficar em casa***

````
algoritmo "condicional composta"
var
  dinheiro: Real
inicio
  Escreva("Quanto dinheiro eu tenho? R$")
  Leia(dinheiro)
  Se (dinheiro >= 10000) entao
    EscrevaL("Partiu Disney!")
  senao
    EscrevaL("#chateado")
  FimSe
fimalgoritmo
````

### 🏋️‍♂️ **Exercício Prático - Par ou Ímpar :**

* Construa um algoritmo que leia um número qualquer, detecte se ele é par ou ímpar e exiba
o resultado na tela.

````
algoritmo "Par Ou Ímpar"
var
   N: Inteiro
inicio
      Escreva("Digite um número qualquer: ")
      Leia(N)
      Se (N % 2 = 0) entao
         Escreval("O número ", N," é PAR")
      senao
           Escreval("O numero ", N," é ÍMPAR")
      FimSe
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Cálculo do IMC :**

* Crie um algoritmo que leia a massa e altua do usuário, calcule o IMC dele, e informe
se o usuário está na faixa de peso ideal ou não.
* Cálculo de IMC: massa/(altura^2)
* Faixa ideal de peso é quando o IMC está entre 18.5 e 25

````
algoritmo "Calculo IMC"
var
   massa, altura, IMC:Real
inicio
      Escreva("Massa(kg): ")
      Leia(massa)
      Escreva("Altura(m): ")
      Leia(altura)
      IMC <- massa/(altura^2)
      Escreval("IMC: ", IMC:5:2)
      Se (IMC >= 18.5) e (IMC < 25) entao
         Escreva("Parabéns! Você está no seu peso ideal.")
      senao
           Escreva("Você não está na faixa de peso idela")
      FimSe
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Está Apto a Dirigir? :**

* Faça um programa para o Departamento de Trânsito que solicite e leia o ano atual e 
o ano de nascimento do usuário, calcule a idade dele e, se ele tiver 18 ou mais anos
idade, informe que ele está apto a tirar carteira, senão, exiba que ele não está apto 
a tirar a carteira.

````
algoritmo "Esta Apto a Dirigir?"
var
   idade, anoAtual, anoNasc: Inteiro
inicio
      Escreval("--------------------------")
      Escreval(" DEPARTAMENTO DE TRÂNSITO ")
      Escreval("--------------------------")
      Escreva("Ano Atual (yyyy): ")
      Leia(anoAtual)
      Escreva("Ano de Nascimento (yyyy): ")
      Leia(anoNasc)
      Escreval("--------- STATUS ---------")
      idade <- anoAtual - anoNasc
      Escreval("IDADE: ", idade)
      Se (idade >= 18) entao
         Escreval("APTO A TIRAR CARTEIRA")
      senao
           Escreval("INAPTO A TIRAR CARTEIRA")
      FimSe
      Escreva("--------------------------")
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Aluno Aprovado ou Reprovado? :**

* Desenvolva uma aplicação para a Escola Javali Cansado que solicite e leia 2 notas,
calcule a média, e, se a média for maior ou igual a 7, informe que o aluno(a) foi
aprovado, senão, informe que o aluno foi reprovado.

````
algoritmo "Aluno aprovado ou reprovado?"
var
   Nota1, Nota2, media:Real
inicio
      Escreval("-----------------------")
      Escreval(" ESCOLA JAVALI CANSADO ")
      Escreval("-----------------------")
      Escreva("Primeira Nota: ")
      Leia(Nota1)
      Escreva("Segunda Nota: ")
      Leia(Nota2)
      Escreval("-----------------------")
      media <- (Nota1+Nota2)/2
      Escreval("MÉDIA: ", media:2:1)
      Se (media >= 7) entao
         Escreval("ALUNO(A) APROVADO")
      senao
           Escreval("ALUNO(A) REPROVADO")
      FimSe
      Escreva("------------------------")
fimalgoritmo
````

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>