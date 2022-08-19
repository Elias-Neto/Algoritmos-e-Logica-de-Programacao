# 🧠 Aula 04 - Operadores Lógicos e Relacionais 

<br>

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver e executar os algoritmos em **Portugol**.

<br>

> 🖖 Essas anotações foram feitas a partir das aulas do professor Gustavo Guanabara. <br>
> 👉 Link para acessar as vídeo-aulas e os materiais do curso: https://www.cursoemvideo.com/curso/curso-de-algoritmo/

<br>

## ↔ **Operadores Relacionais**

- Servem para criar uma **relaçãos de comparação** entre dois **valores numéricos**.

- Ao final da operação, **retornam** um valor  do tipo **lógico** (verdadeiro ou falso).



Operador  | Significado
--------- | ------
_>_       | Maior que 
_<_       | Menor que
_>=_      | Maior ou igual a
_<=_      | Menor ou igual a
_=_       | igual a
_<>_      | diferente de

<br>

### 🏋️‍♂️ **Exercício Prático - Operações Relacionais :**

<br>

- Crie três variáveis, atribua valores a elas e faça operações relacionais.

````
algoritmo "Operações Relacionais"

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

- Servem para criar uma **relaçãos de comparação** entre dois **valores lógicos**.

- Ao final da operação, **retornam** um valor  do tipo **lógico** (verdadeiro ou falso).

<br> 

### *Operador Lógico **"E"***

<br>

- p E q precisam ser verdadeiros para que a operação resulte num valor verdadeiro, caso contrário, resultará num valor falso.

p | q | p E q
:--------- | :------: | -------:
V | V | V
V | F | F
F | V | F
F | F | F

<br>

> Analogia para entender melhor, vamos considerar que "p" representa Paula e "q" representa Quésia, duas pessoas. 

<br>

- Para que eu fique feliz, Paula **E** Quésia precisam estarem felizes. Caso contrário, irei ficar triste.

Paula | Quésia | Eu
:--------- | :------: | -------:
😄 | 😄 | 😄
😄 | 😥 | 😥
😥 | 😄 | 😥
😥 | 😥 | 😥

<br>

### *Operador Lógico **"OU"***

<br>

- p OU q precisam ser verdadeiros para que a operação resulte num valor verdadeiro, caso contrário, resultará num valor falso.

p | q | p OU q
:--------- | :------: | -------:
V | V | V
V | F | V
F | V | V
F | F | F

<br>

> Vamos utilizar novamente a analogia de Paula e Quésia.

<br>

- Para que eu fique feliz, Paula **OU** Quésia precisam estarem felizes. Caso contrário, irei ficar triste.


Paula | Quésia | Eu
:--------- | :------: | -------:
😄 | 😄 | 😄
😄 | 😥 | 😄
😥 | 😄 | 😄
😥 | 😥 | 😥

<br>

### *Operador Lógico **"NÃO"***

<br>

- Esse operador faz a **inversão lógica** de um valor. Ou seja, o que é verdadeiro fica falso e o que é falso fica verdadeiro.

p | NÃO p
--------- | ------
V | F
F | V

<br>

> Novamente, vamos utilizar a analogia de Paula e Quésia.

<br>

- Paula está feliz 😄. Portanto, O inverso lógico é: Paula está triste 😥.

- Paula está triste 😥. Portanto, o inverso lógico é: Paula está feliz 😄.

<br>

### 🏋️‍♂️ **Exercício Prático - Operações Lógicas :**

<br>

- Crie três variáveis, atribua valores a elas e faça operações lógicas.

````
algoritmo "Operações Lógicas"

var
  a, b, c: Inteiro
  
inicio
  a <- 2
  b <- 3
  c <- 5
  EscrevaL ((a = b) ou (a >= 2))     // verdadeiro
  EscrevaL ((b <> 3) ou (a > b))     // falso
  EscrevaL ((c >= a+b) e (c < b^2))  // verdadeiro
  EscrevaL ((c <> a) e (a > c))      // falso
  EscrevaL (nao(c = 0))              // verdadeiro
  EscrevaL (nao(c = 5))              // falso
  
fimalgoritmo
````

<br>

## ❕ **Ordem de Precedência Geral**

Ordem | Tipo de Operadores 
--------- | ------
1° | Operadores Aritméticos 
2° | Operadores Relacionais
3° | Operadores Lógicos

<br>

### 🏋️‍♂️ **Exercício Prático - Triângulos :**

<br>

- Peça ao usuário a medida de três lados de um triângulo, confira se pode ser um triângulo e
qual o tipo do triângulo (isósceles, equilátero ou escaleno).

  - É triângulo quando a soma de dois lados é maior do que o outro lado.
  
  - É triângulo isósceles quando tem dois lados iguais.

  - É triângulo equilátero quando tem todos os lados iguais.

  - É triângulo escaleno quando não tem nenhum lado igual.

````
algoritmo "Triângulos"

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
