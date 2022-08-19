# 🔢 Aula 03 - Comandos de Entrada e Operadores Aritméticos 1 

<br>

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver e executar os algoritmos em **Portugol**.

<br>

> 🖖 Essas anotações foram feitas a partir das aulas do professor Gustavo Guanabara. <br>
> 👉 Link para acessar as vídeo-aulas e os materiais do curso: https://www.cursoemvideo.com/curso/curso-de-algoritmo/

<br>

## 📥 **Comandos de Entrada de Dados**



- São comandos que, quando executados, aguardarão uma resposta.

- São responsáveis pela entrada de dados.



````
algoritmo "apresentação"

var
   nome: caractere

inicio
   Escreva("Digite seu nome: ")     // comando de saída de dados
   Leia(nome)                       // comando de ENTRADA de dados   - recebrá um valor digitado pelo usuário E atribuirá esse valor na variável nome
   Escreva("Muito prazer ", nome)   // comando de saída de dados

fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Somar Dois Números :**

<br>

- Faça um programa que solicite dois números ao usuário, calcule e mostre a soma entre eles.

````
algoritmo "Somar Dois Números"

var
   numero1, numero2, soma: Real

inicio
   Escreva("Informe um número: ")
   Leia(numero1)
   Escreva("Informe outro número: ")
   Leia(numero2)
   soma <- numero1 + numero2
   Escreva("A soma entre ", numero1, " e ", numero2, " é ", soma)
      
fimalgoritmo
````

<br>

## ➗ **Operadores Aritméticos**

- São utilizados para fazer operações aritméticas:

<br>

Símbolo   | Significado
--------- | ------
( + ) | Adição
( - ) | Subtração
( * ) | Multiplicação
( / ) | Divisão
( \ ) | Divisão Inteira
( ^ ) | Exponenciação
( % ) | Módulo

<br>

### ❕ **Ordem de precedência**

<br>

- A Ordem de precedência indica a ordem que os operadores serão considerados dentro de uma mesma expressão.

<br>

Ordem | Símbolo | Significado
:--------- | :------: | -------:
1° | ( ) | Parênteses
2° | ^ | Exponenciação
3° | _*_ / | Multiplicação/divisão
4° | _+_ _-_ | Soma/Subtração

<br>

### 🏋️‍♂️ **Exercício Prático - Média Entre Dois Números :**

<br>

- Faça um programa que solicite dois números ao usuário, calcule e mostre a média entre eles.

````
algoritmo "Média Entre Dois Números"

var
   numero1, numero2: Inteiro
   media: Real

inicio
   Escreva("Informe um número: ")
   Leia(numero1)
   Escreva("Indorme um número: ")
   Leia(numero2)
   media <- (numero1+numero2)/2
   Escreva("A média entre ", numero1, " e ", numero2, " é ", media)

fimalgoritmo
````

<br>

## 🛠 Funções Aritméticas

- São funcionalidades do próprio visualg que servem para realizar mais algumas operações aritméticas.

<br>

Função | O que é | Exemplo
:--------- | :------: | -------:
Abs | valor absoluto | Abs(-10) 10
Exp | exponenciação | Exp(3, 2) 9
Int | valor inteiro | Int(3.9) 3
RaizQ | raiz quadrada | Int(25) 5
Pi | retorna Pi | Pi 3.14...
Sen | Sen(rad) | Sen(0.523) 0.5
Cos | Coseno(rad) | Cos(0.523) 0.86
Tan | Tangente(rad) | Tan(0.523) 0.57
GrauRad | Graus para rad | GraupRad(30) 0.52

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>
