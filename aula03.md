# Aula 03 - Comandos de Entrada e Operadores Aritméticos 1 🔢

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver algoritmos em **Portugol**.

<br>

## 📥 **Comandos de Entrada de Dados**

- são comandos que, quando executados, aguardarão uma resposta
- responsáveis pela entrada de dados

````
algoritmo "apresentação"
var
   nome: caractere
inicio
      Escreva("Digite seu nome: ")     // comando de saída de dados
      Leia(nome)                       // comando de ENTRADA de dados
      Escreva("Muito prazer ", nome)   // comando de saída de dados
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Somar Dois Números :**

* Faça um programa que solicite dois números ao usuário, calcule e mostre a soma entre eles.

````
algoritmo "soma"
var
   N1, N2, S: Real
inicio
      Escreva("Informe um número: ")
      Leia(N1)
      Escreva("Informe outro número: ")
      Leia(N2)
      S <- N1 + N2
      Escreva("A soma entre ", N1, " e ", N2, " é ", S)
fimalgoritmo
````

<br>

## ➗ **Operadores Aritméticos**

* ( + ) Adição
* ( - ) Subtração
* ( * ) Multiplicação
* ( / ) Divisão
* ( \ ) Divisão Inteira
* ( ^ ) Exponenciação
* ( % ) Módulo

<br>

### ❕ **Ordem de precedência**

ordem de precedência indica a ordem que os operadores serão considerados 
dentro de uma mesma expressão

1. ( )  parênteses
2.  ^   exponenciação
3. _*_ /  multiplicação/divisão
4. _+_ _-_  soma/subtração

<br>

### 🏋️‍♂️ **Exercício Prático - Média de Dois Números :**

* Faça um programa que solicite dois números ao usuário, calcule e mostre a média entre eles.

````
algoritmo "media"
var
   N1, N2: Inteiro
   M: Real
inicio
      Escreva("Informe um número: ")
      Leia(N1)
      Escreva("Indorme um número: ")
      Leia(N2)
      M <- (N1+N2)/2
      Escreva("A média entre ", N1, " e ", N2, " é ", M)
fimalgoritmo
````

<br>

## 🛠 Funções Aritméticas

Função | O que é | Exemplo
:--------- | :------: | -------:
Abs | valor absoluto | Abs(-10)  <span style="color:green">10</span>
Exp | exponenciação | Exp(3, 2)  <span style="color:green">9</span>
Int | valor inteiro | Int(3.9)  <span style="color:green">3</span>
RaizQ | raiz quadrada | Int(25)  <span style="color:green">5</span>
Pi | retorna Pi | Pi  <span style="color:green">3.14...</span>
Sen | Sen(rad) | Sen(0.523)  <span style="color:green">0.5</span>
Cos | Coseno(rad) | Cos(0.523)  <span style="color:green">0.86</span>
Tan | Tangente(rad) | Tan(0.523)  <span style="color:green">0.57</span>
GrauRad | Graus para rad | GraupRad(30)  <span style="color:green">0.52</span>

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>