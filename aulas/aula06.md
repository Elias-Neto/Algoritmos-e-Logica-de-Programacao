# Aula 06 - Exercícios de Algoritmos Resolvidos 🏋️‍♂️

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver e executar os algoritmos em **Portugol**.

> Nessa aula iremos ajudar uma moça muito bacana, a Creuza 👩‍🦱

<br>

## 🎂 **Exercício 01 - Creuza vai fazer aniverário :**

* Está chegando o aniversário da Creuza e ela não sabe quantas velinhas colocar em cima do bolo.

* Faça um programa que pergunte ao usuário qual é o ano atual, qual ano ele nasceu, calcule
a idade do usuário e mostre na tela quantos anos ele tem.

````
algoritmo "exercicio 01"
var
   anoAtual, anoNasc, idade: Inteiro
inicio
      Escreva("Em que ano nós estamos? ")
      Leia(anoAtual)
      Escreva("Em que ano você nasceu? ")
      Leia(anoNasc)
      idade <- ano_atual - ano_nasc
      Escreva("-> Você tem ", idade, " anos de idade")
fimalgoritmo
````

<br>

## 💵 **Exercício 02 - Creuza vai viajar e prcisa comprar dólares :**

* Agora que Creuza completou ano, ela quer se presentar com uma viagem para os Estados Unidos.
Além da passagem, ela precisa comprar dólares. Ele tem uma certa quantidade de dinheiro em reias
e quer saber quantos dólares essa quantidade vale.

* Faça um programa que leia quantos reais a pessoa têm, calcule quanto vale essa quantidade me dólar e
mostre na tela o resultado desse cálculo.

````
algoritmo "exercicio 02"
var
   reais, dolares: Real
inicio
      Escreva("Quantos reais você tem? R$")
      Leia(reais)
      dolares <- reais/5.2
      Escreva("Essa quantidade de reais vale U$", dolares:2:2)
fimalgoritmo
````

<br>

## 🌡️ **Exercpicio 03 - Creuza não sabe a temperatura :**

* Creuza já chegou nos Estados Unidos mas quando foi ver a temperatura estava em 100°, ela ficou
desesperada. Fazendo uma pesquisa, ela percebeu que nos Estados Unidos a temperatura é medida
em Fahrenheit e não em Celcius. O problema é que ela não sabe fazer a conversão de um para o outro.

* Crie um programa que pergunte ao usuário qual é a temperatura em Fahrenheit, faça a 
conversão para Celcius e exiba o resultado na tela.

````
algoritmo "exercicio 03"
var
   C, F: Real
inicio
      Escreva("Qual é a temperatura em Fahrenheit (°F)? ")
      Leia(F)
      C <- (F-32)/1.8
      Escreva("Em Celcius, essa temperatura equivale a ", C:4:1, "°C")
fimalgoritmo
````

<br>

## 🛒 **Exercício 04 - Creuza comprou várias coisas :**

* Durante a viagem, Creuza comprou muitas coisas e agora vai precisar pegar imposto assim 
que chegar no Brasil.

* Faça um programa que leia o valor de um porduto, calcule o imposto sobre esse produto e
exiba na tela o resultado. (considere o imposto de 60%)

````
algoritmo "exercicio 04"
var
    preco, imposto: Real
inicio
      Escreva("Qual o valor do produto? R$")
      Leia(preco)
      imposto <- (preco*60)/100
      Escreva("O imposto será de R$", imposto:5:2)
fimalgoritmo
````

<br>

## 💸 **Exercício 05 - Creuza teve que pegar um empréstimo no banco :**

* Após gastar para pagar os impostos, Creuza está sem grana e precisará pegar um 
empréstimo no banco.

* Faça um programa que leia qual o valor do empréstimo, quantas parcelas haverão, calcule
o valor final com juros de 20%, o preço das parcelas e exiba na tela esses valores.

````
algoritmo "exercicio 05"
var
   emprestimo, parcelas, valorFinal, valorParcela: Real
inicio
      Escreva("Qual o valor do empréstimo? R$")
      Leia(emprestimo)
      Escreva("Quantas parcelas? ")
      Leia(parcelas)
       valorFinal <- (emprestimo*120)/100
       valorParcela <- valorFinal/parcelas
      EscrevaL("-> Você irá pagar ", parcelas, " de R$", valorParcela)
      EscrevaL("-> O valor final a se pagar será de R$", valorFinal)
fimalgoritmo

````

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>