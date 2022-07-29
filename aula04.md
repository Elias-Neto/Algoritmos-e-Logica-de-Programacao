# Aula 04 - Operadores Lógicos e Relacionais 🧠

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver algoritmos em **Portugol**.

<br>

## ↔ **Operadores Relacionais**

- criam uma relaçãos de comparação entre dois valores numéricos
- retornam valor lógico (verdadeiro ou falso)

<br>

Operador  | Significado
--------- | ------
_>_       | Maior que 
_<_       | Menor que
_>=_      | Maior ou igual a
_<=_      | Menor ou igual a
_=_       | igual a
_<>_      | diferente de

<br>

### 🏋️‍♂️ **Exercício Prático:**

Comparar valores numéricos.

````
algoritmo "operadores relacionais"
var
  a, b, c: Inteiro
inicio
  a <- 2
  b <- 3
  c <- 5
  EscrevaL(a < b)     // verdadeiro
  EscrevaL(a > b)     // falso
  EscrevaL(c >= b^a)  // falso
  EscrevaL(c <= a+b)  // verdadeiro
  EscrevaL(1 = c%2)   // verdadeiro
  EscrevaL(a <> b)    // verdadeiro
fimalgoritmo
````

<br>

## 🧠 **Operadores Lógicos**

- compara somente valores lógicos
- retornam  valor lógico (verdadeiro ou falso)

<br> 

### *Operador Lógico **"E"***

* p E q precisam ser verdadeiros para que a operação seja verdadeira

p | q | p E q
:--------- | :------: | -------:
V | V | V
V | F | F
F | V | F
F | F | F

> Analogia para entender melhor, vamos considerar que "p" representa Paula e "q" representa Quésia, duas pessoas. 

* quero que Paula **e** Quésia estejam feliz


p | q | p E q
:--------- | :------: | -------:
😄 | 😄 | 😄
😄 | 😥 | 😥
😥 | 😄 | 😥
😥 | 😥 | 😥

<br>

### *Operador Lógico **"OU"***

* p OU q precisa ser verdadeiro para que a operação seja verdadeira

p | q | p OU q
:--------- | :------: | -------:
V | V | V
V | F | V
F | V | V
F | F | F

> Analogia para entender melhor, vamos considerar que "p" representa Paula e "q" representa Quésia, duas pessoas. 

* quero que Paula **e** Quésia estejam feliz


p | q | p E q
:--------- | :------: | -------:
😄 | 😄 | 😄
😄 | 😥 | 😄
😥 | 😄 | 😄
😥 | 😥 | 😥


<br>

### *Operador Lógico **"NÃO"***

* inversão lógica

p | NÃO p
--------- | ------
V | F
F | V

* quem tá feliz, fica triste.
* quem tá triste, fica feliz.

p | NÃO p
--------- | ------
😄 | 😥 
😥 | 😄 

<br>

### 🏋️‍♂️ **Exercício Prático:**

Comparar valores lógicos.

````
algoritmo "operadores relacionais"
var
  a, b, c: Inteiro
inicio
  a <- 2
  b <- 3
  c <- 5
  EscrevaL((a = b) ou (a >= 2))     // verdadeiro
  EscrevaL((b <> 3) ou (a > b))     // falso
  EscrevaL((c >= a+b) e (c < b^2))  // verdadeiro
  EscrevaL((c <> a) e (a > c))      // falso
  EscrevaL(nao(c = 0))              // verdadeiro
  EscrevaL(nao(c = 5))              // falso
fimalgoritmo
````

<br>

## ❕ **Ordem de Precedência Geral**

- 1° Operadores Aritméticos 
- 2° Operadores Relacionais
- 3° Operadores Lógicos

<br>

### 🏋️‍♂️ **Exercício Prático:**

Peça ao usuário a medida de três lados de um triângulo e confira se pode ser um triângulo
e, se sim, qual o tipo do triângulo (isósceles, equilátero ou escaleno).

````
algoritmo "triângulos"
var
   L1, L2, L3: Real
   IS, EQ, ES, TRI: Logico
inicio
      Escreva("Digite o primeiro lado: ")
      Leia(L1)
      Escreva("DIgite o segundo lado: ")
      Leia(L2)
      Escreva("Digite o terceiro lado: ")
      Leia(L3)
      TRI <- (L1 < L2 + L3) e (L2 < L3 + L1) e (L3 < L1 + L2)
      EQ <- (L1 = L2) e (L2 = L3)
      ES <- (L1 <> L2) e (L2 <> L3) e (L1 <> L3)
      IS <- ((L1 = L2) e (L1 <> L3)) ou ((L1 = L3) e (L1 <> L2)) 
      Escreval("Pode formar um TRIÂNGULO?", TRI)
      Escreval("O triangulo é EQUILÁTERO? ", EQ)
      Escreval("O triangulo é ESCALENO?", ES)
      Escreval("O triangulo é ISÓSCELES?", IS)
fimalgoritmo
````

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>