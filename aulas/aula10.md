# 🔁 Aula 10 - Estruturas de Repetição (Parte 02)

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver e executar os algoritmos em **Portugol**.

<br>

## **Estrutura de Repetição "Repita"**

- gira em torno de uma condição
- *o teste lógico é feito no **fim** da estrutura*
- é utilizado quando não se sabe quantas vezes vai repetir o loop

Sintaxe da Estrutura:

- repita tal coisa até que tal condição seja verdadeira

````
Repita
  Bloco
Ate (expressão)
````

Exemplo:

- Está de castigo até arrumar seu quarto

````
Repita
  castigo
Ate (arrumar quarto)
liberado
````

<br>

### ***Enquanto x Repita***

- No "Enquanto" o teste lógico é feito no início, no "Repita" é feito no final.
   
   - Quando não se sabe quantas vezes vai repetir o loop, utiliza o repita

   - Quando se sabe quantas vezes vai repetir o loop, utiliza o enquanto

- O uso da expressão lógica (a condição) de uma é o inverso do da outra:
  
  - No "enquanto" foi utilizado: **não arrumar o quarto**
  
  - No "repita" foi utilizado: **arrumar o quarto**

- É uma relação inclusive de construção frasal:
  
  - "Você vai ficar de **castigo** enquanto **não arrumar o quarto**
  
  - "Você vai ficar de **castigo** até **arrumar seu quarto**

<br>

### 🏋️‍♂️ **Exercício Prático - Contar de 1 Até 10 :**

- Crie um algoritmo que conte de 1 até 10

````
algoritmo "contar de 1 até 10"
var
  contador: Inteiro
inicio
  Repita
    contador <- contador + 1
    Escreval(contador)
  Ate (contador = 10)
fimalgoritmo
````

- **adiconal:** exibir a tabuada de um número qualquer

````
algoritmo "tabuada"
var
  contador, numero, resultado: Inteiro
inicio
  Escreva("Quer ver a tabuada de qual número? ")
  Leia(numero)
  Repita
    contador <- contador + 1
    resultado <- numero * contador
    Escreval(numero, " x ", contador, " = ", resultado)
  Ate (contador = 10)
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Quantos Números São Negativos :**

- Crie um algoritmo que leia cinco números e, no final, mostre quantos são negativos

````
algoritmo "quantos numeros sao negativos"
var
  numero, contador, totalNegativos: Inteiro
inicio
  contador <- 1
  Repita
    Escreva("Digite um nùmero: ")
    Leia(numero)
    contador <- contador + 1
    Se (numero < 0) entao
      totalNegativos <- totalNegativos + 1
    FimSe
  Ate (contador > 5)
  Escreval("Foram digitado ", totalNegativos, " valores negativos")
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Fatorial de Um Número :**

- Desenvolva um programa que leia um número, calcule e exiba o faturial desse número.

- Fatorial é basicamente o número multiplicado por seus antecessores:
  - 3! = 3 x 2 x 1 = 6
  - 5! = 5 x 4 x 3 x 2 x 1 = 120

````
algoritmo "fatorial de um numero"
var
  contador, numero, fatorial: Inteiro
inicio
  Escreva("Digite um nùmero: ")
  Leia(numero)
  contador <- numero
  fatorial <- 1
  Repita
    fatorial <- fatorial * contador
    contador <- contador - 1
  Ate (contador < 1)
  Escreval("O valor do fatorial de ", numero, " é igual a ", fatorial)
fimalgoritmo
````

- **adicional:** fazer acontecer várias vezes

````
algoritmo "fatorial de um numero"
var
 contador, numero, fatorial: Inteiro
 resposta: Caractere
inicio
   Repita
      Escreva("Digite um número: ")
      Leia(numero)
      contador <- numero
      fatorial <- 1
      Repita
         fatorial <- fatorial * contador
         contador <- contador - 1
      Ate (contador = 1)
      Escreval("O valor do fatorial de ", numero, " é igual a ", fatorial)
      Escreva("Quer continuar? [S/N] ")
      Leia(resposta)
   Ate (resposta = "N")
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - É Um Número Primo? :**

- Desenvolvaa um algoritmo que lei um número, detecte e informe se esse número
é ou não primo

- Número Primo, quer dizer que da contagem de um até o número, ele só tem dois 
divisores (um e ele mesmo)

````
algoritmo "é um numero primo?"
var
  numero, contador, primo, divisivel: Inteiro
inicio
  contador <- 1
  Escreva("Digite um número: ")
  Leia(numero)
  Repita
    Se (numero % contador = 0) entao
      divisivel <- divisivel + 1
    FimSe
    contador <- contador + 1
  Ate (contador > numero)
  Se (divisivel > 2) entao
    Escreval(" O número ", numero, " não é primo! ")
  senao
    Escreval(" O número ", numero, " é primo! ")
  FimSe
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Super Contador :**

- Faça uma aplicação que dê ao usuário tês opções: 
  
  1. De 1 até 10 

  2. De 10 até 1 

  3. Sair

- caso ele escolha a primeira opção, o programa irá calcular e exebir uma contagem
de 1 até 10

- caso ele escolha a segunda opção, o programa irá calcular e exebir uma contagem
de 10 até 1

- caso ele escolha a terceira opção, o programa irá ser finalziado

````
algoritmo "super contador"
var
  contagem, contador: Inteiro
inicio
  Repita
    Escreval("")
    Escreval("")
    Escreval("=================")
    Escreval("     M E N U     ")
    Escreval("=================")
    Escreval(" [1] De 1 a 10 ")
    Escreval(" [2] De 10 a 1 ")
    Escreval(" [3] Sair ")
    Escreval("=================")
    Leia(contagem)
    Escolha (contagem)
      Caso 1
        contador <- 1
        Repita
          Escreva(" ", contador, "..")
          contador <- contador + 1
        Ate (contador > 10)
      Caso 2
        contador <- 10
        Repita
          Escreva(" ", contador, "..")
          contador <- contador - 1
        Ate (contador < 1)
      Caso 3
        Escreval("SAINDO...")
      OutroCaso
        Escreval("INVÁLIDO.")
    FimEscolha
  Ate (contagem = 3)
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Escolhendo Pessoas :**

- Faça um programa que leia o sexo, a idade e a cor de cabelo do usuário,
detcte e informe a quantidade de:

- homens, com mais de 18 anos e cabelos castanhos
- mulheres, entre 25 e 30 anos e cabelos loiros

- esse programa deve se repetir quantas vezes o usuário quiser

````
algoritmo "EXERCÍCIO 02 - ESCOLHENDO PESSOAS"
var
  sexo, resposta, cabelo: Caractere
  idade, tipo, quantM, quantF: Inteiro
inicio
  Repita
    LimpaTela
    Escreval("========================")
    Escreval("   SELETOR DE PESSOAS   ")
    Escreval("========================")
    Escreva("Qual o Sexo? [M/F] ")
    Leia(sexo)
    Escreva("Qual a idade? ")
    Leia(idade)
    Escreval("Qual a cor do Cabelo? ")
    Escreval("-------------------------")
    Escreval(" [1] Preto ")
    Escreval(" [2] Castanho ")
    Escreval(" [3] Loiro ")
    Escreval(" [4] Ruivo ")
    Leia(tipo)
    Escolha (tipo)
      Caso 1
        cabelo <- "Preto"
      Caso 2
        cabelo <- "Castanho"
      Caso 3
        cabelo <- "Loiro"
      Caso 4
        cabelo <- "Ruivo"
    FimEscolha
    Se (sexo = "M") e (idade >= 18) e (cabelo = "Castanho") entao
      quantM <- quantM + 1
    FimSe
    Se (sexo = "F") e (idade >= 25) e (idade <= 30) e (cabelo= "Loiro") entao
      quantF <- quantF + 1
    FimSe
    Escreva("Quer continuar? [S/N] ")
    Leia(resposta)
  Ate (resposta = "N")
  LimpaTela
  Escreval("--------------------")
  Escreval("  RESULTADO  FINAL  ")
  Escreval("--------------------")
  Escreval("Total de homens com mais de 18 anos e com cabelos castanhos é ", quantM)
  Escreval("Total de mulheres entre 25 e 30 anos e com cabelos loiros é ", quantF)
fimalgoritmo
````

<br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>