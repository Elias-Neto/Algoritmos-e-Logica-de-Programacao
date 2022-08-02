# 🛠 Aula 12 - Procedimentos

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver e executar os algoritmos em **Portugol**.

<br>

## **Rotina - parte 1**

- rotina é um procedimento repetitivo
- são utéis para evitarmos repetição de código

**Sintaxe da Estrutura**

````
Procedimento nomeDoProcedimento()
Inicio
  Bloco
FimProcedimento
````

**Exemplo - Fazer Vitamina de Banana :**

- Se quiser fazer uma vitamina de banana, siga o procedimento abaixo:
- Procedimento para fazer uma vitamina de banana:
  - Pegar  2 bananas
  - Pegar 500ml de água
  - Pegar 50g de leite
  - Coloca tudo no Liquidificador
  - Bate tudo com o Liquidificador por 05min

````
algoritmo "Fazer Vitamina de Banana"

var
  resposta: Caractere

  Procedimento fazerVitaminaDeBanana()
  Inicio
    EscrevaL("- Pegar 2 bananas")
    EscrevaL("- Pegar 500ml de água")
    EscrevaL("- Pegar 50g de leite")
    EscrevaL("- Colocar tudo no Liquidificador")
    EscrevaL("- Bater tudo com o Liquidificador por 05min")
  FimProcedimento

inicio
  Escreva("Quer fazer uma vitamina de banana [S/N]? ")
  Leia(resposta)
  Se (resposta = "s") entao
    fazerVitaminaDeBanana()
  FimSe

fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Detector de Pesado :**

- Crie um programa que leia o nome e o peso de cinco pessoas, compare e detecte qual foi o maior
peso até o momento informe-o durante toda execução, ao final, informe o nome e o peso da pessoa mais
pesada cadastrada.

````
// SEM UTILIZAR PROCEDIMENTOS
// MUITA REPETIÇÃO DE CÓDIGO (CÓDIGO SUJO)

algoritmo "DETECTOR DE PESADO (SEM UTILIZAR PROCEDIMENTOS)"

var
  contador: Inteiro
  nome, pesado: Caractere
  peso, maiorPeso: Real

inicio
  LimpaTela
  Escreval("----------------------------------")
  Escreval(" D E T E C T O R  DE  P E S A D O ")
  Escreval(" Maior Peso até agora: ", maiorPeso, "kg")
  Escreval("----------------------------------")
  Para contador <- 1 ate 5 faca
    Escreva("Digite o nome: ")
    Leia(nome)
    Escreva("Digite o peso de ", nome, ": ")
    Leia(peso)
    Se (peso > maiorPeso) entao
      maiorPeso <- peso
      pesado <- nome
    FimSe
    LimpaTela
    Escreval("_---------------------------------")
    Escreval(" D E T E C T O R  DE  P E S A D O ")
    Escreval(" Maior Peso até agora: ", maiorPeso, "kg")
    Escreval("----------------------------------")
  FimPara
  LimpaTela
  Escreval("_---------------------------------")
  Escreval(" D E T E C T O R  DE  P E S A D O ")
  Escreval(" Maior Peso até agora: ", maiorPeso, "kg")
  Escreval("----------------------------------")
  Escreval("A pessoa mais pesado foi ", pesado, ", com ", maiorPeso, " quilos. ")

fimalgoritmo
````

````
// UTILIZANDO PROCEDIMENTOS
// MENOS REPETIÇÃO DE CÓDIGO (CÓDIGO LIMPO)

algoritmo "PRÁTICA 01 - DETECTOR DE PESADO (com Procedimento)"

var
  contador: Inteiro
  nome, pesado: Caractere
  peso, maiorPeso: Real

  Procedimento Topo()
  Inicio
    LimpaTela
    Escreval("----------------------------------")
    Escreval(" D E T E C T O R  DE  P E S A D O ")
    Escreval(" Maior Peso até agora: ", maiorPeso, "kg")
    Escreval("----------------------------------")
  FimProcedimento

inicio
  Topo()
  Para contador <- 1 ate 5 faca
    Escreva("Digite o nome: ")
    Leia(nome)
    Escreva("Digite o peso de ", nome, ": ")
    Leia(peso)
    Se (peso > maiorPeso) entao
      maiorPeso <- peso
      pesado <- nome
    FimSe
    Topo()
  FimPara
  Topo()
  Escreval("A pessoa mais pesado foi ", pesado, ", com ", maiorPeso, " quilos. ")

fimalgoritmo
````

<br>

## **Passagem de Parâmetro**

- Em um procedimento você pode utilizar parâmetros

- Parâmetros são variáveis que estão recebem alguma coisa como referência

**Exemplo:**

- Faça um procedimento passando dois números como parâmetros para serem somados.

````
algoritmo "PASSAGEM DE PARÂMETRO POR VALOR"

var
  X, Y: Inteiro

  Procedimento Soma(A, B: Inteiro)
  Inicio
    Escreval("Recebi o valor ", A)   // A recebeu o valor de X como referência
    Escreval("Recebi o valor ", B)   // B recebeu o valor de Y como referência
    Escreval("A soma entre os dois é ", A + B)
  FimProcedimento

inicio
  X <- 5
  Y <- 3
  Soma(X, Y)

fimalgoritmo
````

<br>

## **Tipos de Passagem de Parâmetros: Passagem de Parâmetro Por Valor**

- É um tipo de passagem na qual os parâmetros do procedimento recebem valores como referência

- No exemplo acima ocorre uma passagem de parâmetro por valor 
(A e B são parâmetros que recebem o valor de X e Y como referência)

- OBS❕ Não use o mesmo nome da variável referência no parâmetro.

<br>

### 🏋️‍♂️ **Exercício Prático - Verificador Par/Ímpar :**

- Desenvolva um algoritmo que leia um número, verifique e informe se ele é par ou ímpar.

- Utilize procedimentos com passagem de parâmetro por valor.

````
algoritmo "VERIFICADOR PAR/ÍMPAR"

var
  numero: Inteiro

  Procedimento ParOuImpar(valor: Inteiro)
  Inicio
    Se (valor%2 = 0) entao
      Escreval("O número ", valor, " é PAR")
    senao
      Escreval("O nùmero ", valor, " é ÍMPAR")
    FimSe
  FimProcedimento

inicio
  Escreva("Digite um número: ")
  Leia(numero)
  ParOuImpar(numero)
fimalgoritmo
````

<br>

## **Escopo**

- escopo é o local onde uma determinada variável vai funcionar.

- existe o escopo global, quando uma variável funciona em todo o lugar do programa.

- exsite o escopo local, quando uma variável só funciona em um lugar específico.

**Exemplo:**

- nesse exemplo, somente as variáveis N1 e N2 tem o escopo global, logo, funcionam em qualquer
parte do programa.

- já as variáveis A e B, são parâmetros do procedimento 'Rotina', portanto, são de escopo local
e funcionam somente dentro do procedimento 'Rotina'.

- e as variáveis X e Y, são declaradas dentro do procedimento 'Rotina, logo, são de escopo local
e funcionam somente dentro do procedimento 'Rotina'.

````
algoritmo "ESCOPO"

var
  N1, N2: Inteiro

  Procedimento Rotina(A, B: Inteiro)
  var
    X, Y: Inteiro
  Inicio
    X <- A
    Y <- B
    EscrevaL("DENTRO DO PROCEDIMENTO 'ROTINA'")
    EscrevaL("Valor de N1: ", N1)
    EscrevaL("Valor de N2: ", N2)
    EscrevaL("Valor de A: ", A)
    EscrevaL("Valor de B: ", B)
    EscrevaL("Valor de X: ", X)
    EscrevaL("Valor de Y: ", Y)
  FimProcedimento

inicio
  N1 <- 5
  N2 <- 3
  Rotina(N1, N2)
  EscrevaL()
  EscrevaL("FORA DO PROCEDIMENTO 'ROTINA'")
  EscrevaL("Valor de N1: ", N1)
  EscrevaL("Valor de N2: ", N2)
  EscrevaL("Valor de A: ", A)    // Vai dar ERRO: variável 'A' não foi encontrada
  EscrevaL("Valor de B: ", B)    // Vai dar ERRO: variável 'B' não foi encontrada
  EscrevaL("Valor de X: ", X)    // Vai dar ERRO: variável 'X' não foi encontrada 
  EscrevaL("Valor de Y: ", Y)    // Vai dar ERRO: variável 'Y' não foi encontrada 

fimalgoritmo
````

<br>

## **Tipos de Passagem de Parâmetros: Passagem de Parâmetro Por Referência**

- Nesse tipo de passagem, os parâmetros receberão a própria variável como referência

- Podemos fazer uma analogia e dizer que os parâmetros receberão o 'endereço' da variável 
como referência

<BR>

### **Exemplo - Comparando Os Tipos de Passagem de Parâmetro (Por Valor x Por Referência) :**

````
algoritmo "PASSAGEM DE PARÂMTRO POR VALOR"

var
  X, Y: Inteiro

  Procedimento Soma (A, B: Inteiro)
  Inicio
    A <- A + 1
    B <- B + 2
    Escreval("Valor de A = ", A)     // = 5  | A recebeu o valor da variável X como referência 
    Escreval("Valor de B = ", B)     // = 10 | B recebeu o valor da variável Y como referência
    Escreval("Soma A + B = ", A+B)   // = 15 
  FimProcedimento

inicio
  X <- 4
  Y <- 8
  Soma (X, Y)
  Escreval("Valor de X = ", X)    // = 4  | O valor da variável X não muda
  Escreval("Valor de Y = ", Y)    // = 8  | O valor da variável Y não muda
  Escreval("Soma X + Y = ", X+Y)  // = 12
    
fimalgoritmo
````

````
algoritmo "PASSAGEM DE PARÂMTRO POR REFERÊNCIA"

var
  X, Y: Inteiro

  Procedimento Soma (var A, B: Inteiro)  // para passagem de parâmetro por referência, acrescente 'var' antes dos parâmetros
  Inicio
    A <- A + 1
    B <- B + 2
    Escreval("Valor de A = ", A)     // = 5  | A recebeu a própria variável X como referência 
    Escreval("Valor de B = ", B)     // = 10 | B recebeu a própria variável Y como referência
    Escreval("Soma A + B = ", A+B)   // = 15 
  FimProcedimento

inicio
  X <- 4
  Y <- 8
  Soma (X, Y)
  Escreval("Valor de X = ", X)    // = 5  | O valor da variável X muda
  Escreval("Valor de Y = ", Y)    // = 10  | O valor da variável Y muda
  Escreval("Soma X + Y = ", X+Y)  // = 15
    
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Sequência de Fibonacci :**

- Utilizando procedimento e passagem de parâmetro, desenvolva um algoritmo que calcule e exiba 
os 15 primeiros termos da sequência de fibonacci.

- A sequência de fibonacci consiste em uma sequência de números na qual o primeiro e segundo elemento
é o 1 e o e os elementos seguintes são originados pela soma de seus dois antecessores, observe:

  - 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 987, 1597, 2584, 4181...

````
algoritmo "SEQUÊNCIA DE FIBONACCI"

var
  contador, valor1, valor2: Inteiro

  Procedimento ProximoFibonacci(var A, B: Inteiro)
  var
    valor3: Inteiro
  Inicio
    valor3 <- A + B
    Escreva(valor3)
    A <- B
    B <- valor3
  FimProcedimento

inicio
  valor1 <- 1
  Escreva(valor1)
  valor2 <- 1
  Escreva(valor2)
  Para contador <- 3 ate 15 faca
    ProximoFibonacci(valor1, valor2)
  FimPara
  
fimalgoritmo
````