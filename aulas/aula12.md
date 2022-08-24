# 🛠 Aula 12 - Procedimentos

<br>

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver algoritmos em **Portugol**.

<br>

> 🖖 Essas anotações foram feitas a partir das aulas do professor **Gustavo Guanabara**. <br>
> 👉 Link para acessar as vídeo-aulas e os materiais do curso: https://www.cursoemvideo.com/curso/curso-de-algoritmo/

<br>

## **O que são Procedimentos?**

- Procedimentos são **blocos de código** que se **repetem** com certa frequência. 

- Eles são muito úteis para escrevermos um código mais organizado (mais **limpo**), pois elas ***evitam a repetição desnecessária de código***.

<br>

### **Sintaxe da Estrutura**

````
Procedimento nomeDoProcedimento()
Inicio
  Bloco
FimProcedimento
````

<br>

**Exemplo - Fazer Vitamina de Banana :**

- Toda vez que eu for fazer uma vitamina de banana eu posso, simplesmente, seguir um procedimento padrão:

  [x] Pegar  2 bananas
  
  [x] Pegar 500ml de água

  [x] Pegar 50g de leite

  [x] Coloca tudo no Liquidificador

  [x] Bate tudo no Liquidificador por 5min
  
- Logo, quando eu quiser fazer uma vitamina de banana eu só preciso repetir um procedimento já definido previamente.

````
algoritmo "Fazer Vitamina de Banana"

var
  resposta: Caractere

  Procedimento fazerVitaminaDeBanana()
  Inicio
    EscrevaL("[x] Pegar 2 bananas")
    EscrevaL("[x] Pegar 500ml de água")
    EscrevaL("[x] Pegar 50g de leite")
    EscrevaL("[x] Colocar tudo no Liquidificador")
    EscrevaL("[x] Bater tudo no Liquidificador por 5min")
  FimProcedimento

inicio
  Escreva("Quer fazer uma vitamina de banana [S/N]? ")
  Leia(resposta)
  
  EscrevaL()
  Se (resposta = "s") entao
    fazerVitaminaDeBanana()
  FimSe

fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Detector de Pesado :**

<br>

- Crie um programa que leia o nome e o peso de cinco pessoas e informe durante toda execução qual foi o maior
peso até o momento. Ao final, exiba o nome e o peso da pessoa mais pesada que foi cadastrada.

````
// ❌ SEM UTILIZAR PROCEDIMENTOS                                                         
// 👎 MUITA REPETIÇÃO DE CÓDIGO (CÓDIGO SUJO)                                            
  
algoritmo "Detector de Pesado (SEM UTILIZAR PROCEDIMENTOS)"                              

var                                                                                    
  contador: Inteiro                                                                              
  nome, pesado: Caractere
  peso, maiorPeso: Real

inicio
  Para contador <- 1 ate 5 faca
    LimpaTela
    Escreval("_---------------------------------")
    Escreval(" D E T E C T O R  DE  P E S A D O ")
    Escreval(" Maior Peso até agora: ", maiorPeso, "kg")
    Escreval("----------------------------------")
  
    Escreva("Digite o nome: ")
    Leia(nome)
    Escreva("Digite o peso de ", nome, ": ")
    Leia(peso)
    
    Se (peso > maiorPeso) entao
      maiorPeso <- peso
      pesado <- nome
    FimSe
    
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
// ✅ UTILIZANDO PROCEDIMENTOS
// 👍 MENOS REPETIÇÃO DE CÓDIGO (CÓDIGO LIMPO)

algoritmo "DETECTOR DE PESADO (UTILIZANDO PROCEDIMENTOS)"

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
  Para contador <- 1 ate 5 faca
    Topo()
    
    Escreva("Digite o nome: ")
    Leia(nome)
    Escreva("Digite o peso de ", nome, ": ")
    Leia(peso)
    
    Se (peso > maiorPeso) entao
      maiorPeso <- peso
      pesado <- nome
    FimSe
  FimPara
  
  Topo()
  Escreval("A pessoa mais pesado foi ", pesado, ", com ", maiorPeso, " quilos. ")

fimalgoritmo
````

<br>

## **Procedimentos com Passagem de Parâmetros**

- Parâmetro é uma palavra que utilizamos, normalmente, para estabelecer uma **relação de comparação**.

  - Por exemplo: "Muitos deliverys utilizam o IFood como parâmetro." 

  - Nessa frase, "utilizar o IFood como parâmetro" significa que muitos deliverys utilizam o IFood como **REFERÊNCIA** de negócio.

  - Na programação, a ideia é semelhante...

- Um procedimento pode utilizar o **valor** ou o **"endereço"** de uma variável como parâmetro (ou seja, como referência).

<br>

**Exemplo:**

- Faça um procedimento que possua dois parâmetros numéricos e realize a soma deles.

````
algoritmo "Passagem de Parâmetros"

var
  X, Y: Inteiro

  Procedimento Soma(A, B: Inteiro)
  Inicio
    Escreval("Recebi o valor ", A)   // A recebeu o valor da variável X como referência
    Escreval("Recebi o valor ", B)   // B recebeu o valor da variável Y como referência
    Escreval("A soma entre os dois é ", A + B)
  FimProcedimento

inicio
  X <- 5
  Y <- 3
  Soma(X, Y) 

fimalgoritmo
````

- Perceba que A e B funcionam normalmente como variáveis **dentro** da estrutura do procedimento.

  - É por isso que precisamos delcarar os parâmetros da mesma forma como declaramos variáveis ("nomeDoParâmetro" + tipo de dado que será armazenado).

- Na programação, muitas vezes há uma confusão entre o conceito de **PARÂMETROS** e de **ARGUMENTOS**:

  - PARÂMETROS são as variáveis que irão **receber** algo como referência dentro de um procedimento (no exmeplo acima, A e B).

  - ARGUMENTOS são aquilo que você **passa** como referência para os parâmetros de um procedimento (no exemplo acima, X e Y).

  - Ou seja, no exemplo acima, os *parâmetros* A e B do *procedimento* Soma() estão recebendo X e Y como *argumentos*.

<br>

## **Passagem de Parâmetro Por Valor**

- Como já foi dito: "Um procedimento pode utilizar o **valor** ou o **"endereço"** de uma variável como parâmetro (ou seja, como referência)". 

- No exemplo anterior, ocorre uma passagem de parâmetro por valor. 

  - A e B são parâmetros que recebem o **valor** dos argumentos X e Y como referência.

- ***OBS❕ Use sempre nomes diferentes para os argumentos e os parâmetros.***

<br>

### 🏋️‍♂️ **Exercício Prático - Verificador Par/Ímpar :**

<br>

- Desenvolva um algoritmo que leia um número, verifique e informe se ele é par ou ímpar.

````
algoritmo "Verificador Par/Ímpar"

var
  numero: Inteiro

  Procedimento ParOuImpar(N: Inteiro)  // O parâmetro N recebe o valor do seu argumento como referência
  Inicio
    Se (N%2 = 0) entao
      Escreval("O número ", N, " é PAR")
    senao
      Escreval("O nùmero ", N, " é ÍMPAR")
    FimSe
  FimProcedimento

inicio
  Escreva("Digite um número: ")
  Leia(numero)
  ParOuImpar(numero)  // Chamando o procedimento ParOuImpar() e Passando a variável número como Argumento
  
fimalgoritmo
````

<br>

## **Escopo**

- Escopo é um conceito crucial na programação.

- Ele representa o **local** onde uma determinada variável vai **funcionar**.

- Existem dois **tipos** de escopos:

  - **Escopo Global**, quando uma variável funciona em qualquer lugar do programa.

  - **Escopo Local**, quando uma variável só funciona num lugar específico do programa.

**Exemplo:**

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
    
    EscrevaL("Valor de N1: ", N1)     // NÃO vai dar ERRO
    EscrevaL("Valor de N2: ", N2)     // NÃO vai dar ERRO
    EscrevaL("Valor de A: ", A)       // NÃO vai dar ERRO
    EscrevaL("Valor de B: ", B)       // NÃO vai dar ERRO
    EscrevaL("Valor de X: ", X)       // NÃO vai dar ERRO
    EscrevaL("Valor de Y: ", Y)       // NÃO vai dar ERRO
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

- Nesse exemplo:
  
  -  Somente as variáveis N1 e N2 têm **escopo global**, logo, funcionam em qualquer parte do programa.

  -  Já as variáveis A e B são parâmetros do procedimento Rotina(), portanto, possuem **escopo local** (ou seja, funcionam somente dentro do procedimento Rotina()).

  -  Por fim, as variáveis X e Y são declaradas dentro do procedimento Rotina(), consequentemente, também possuem **escopo local** (ou seja, funcionam somente dentro do procedimento).

<br>

## **Passagem de Parâmetro Por Referência**

- No início eu ressaltei que "Um procedimento pode utilizar o **valor** ou o **"endereço"** de uma variável como parâmetro (ou seja, como referência)."

- Diferentemente da passagem de parâmetro por valor, na passagem por referência, os parâmetos do procedimento estão **diretamente ligados** às variável que foram passadas como referências (ou seja, aos Argumentos).

- Isso quer dizer que: se eu passar um argumento X com valor 1 para um parâmetro A de um procedimento qualquer, por exemplo, e, dentro do procedimento, A tem seu valor reatribuido para 2, quando o procedimento chegar ao fim e retornar ao fluxo normal da aplicação, o valor de X também terá sido reatribuído para 2, pois na passagem de parâmetro por referência os Argumentos do procedimento estão diretamente ligados aos seus Parâmetros.

- É como se os parâmetros recebecem seus próprios argumentos como referência. Podemos fazer uma analogia e dizer que os parâmetros receberão o **"endereço"** de seus argumentos como referência, logo, o que é alterado naquele afeta diretamente esse.

<br>

### **Exemplo - Comparando Os Tipos de Passagem de Parâmetro (Por Valor x Por Referência) :**

````
algoritmo "Passagem de Parâmetros por REFERÊNCIA"

var
  X, Y: Inteiro

  // para passagem de parâmetro por referência, acrescente 'var' antes dos parâmetros
  
  Procedimento Soma (var A, B: Inteiro)  // A e B (Parâmetros do procedimento Soma) recebem os "ENDEREÇOS" de seus argumentos (X e Y, respectivamente) como referência
  Inicio
    A <- A + 1  // A tem seu valor reatribuído
    B <- B + 2  // B tem seu valor reatribuído
    
    Escreval("Valor de A = ", A)     // = 5
    Escreval("Valor de B = ", B)     // = 10
    Escreval("Soma A + B = ", A+B)   // = 15 
  FimProcedimento

inicio
  X <- 4
  Y <- 8
  
  Soma(X, Y)  // Chamando procedimento Soma() e Passando X e Y como argumentos
  
  Escreval("Valor de X = ", X)    // = 5   | O valor da variável X muda
  Escreval("Valor de Y = ", Y)    // = 10  | O valor da variável Y muda
  Escreval("Soma X + Y = ", X+Y)  // = 15
    
fimalgoritmo
````

````
algoritmo "Passagem de Parâmetros por VALOR"

var
  X, Y: Inteiro

  Procedimento Soma (A, B: Inteiro) // A e B (Parâmetros do procedimento Soma) recebem os VALORES de seus argumentos (X e Y, respectivamente) como referência
  Inicio
    A <- A + 1  // A tem seu valor reatribuído
    B <- B + 2  // B tem seu valor reatribuído
    
    Escreval("Valor de A = ", A)     // = 5
    Escreval("Valor de B = ", B)     // = 10
    Escreval("Soma A + B = ", A+B)   // = 15 
  FimProcedimento

inicio
  X <- 4
  Y <- 8
  
  Soma (X, Y)  // Chamando procedimento Soma() e Passando X e Y como argumentos
  
  Escreval("Valor de X = ", X)    // = 4  | O valor da variável X não muda
  Escreval("Valor de Y = ", Y)    // = 8  | O valor da variável Y não muda
  Escreval("Soma X + Y = ", X+Y)  // = 12
    
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Sequência de Fibonacci :**

<br>

- Utilizando procedimento, desenvolva um algoritmo que calcule e exiba os 15 primeiros termos da sequência de fibonacci.

- A sequência de fibonacci consiste em uma sequência de números na qual o primeiro e segundo elemento é o 1 e o e os elementos seguintes são originados pela soma de seus dois antecessores, observe:

  - 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 987, 1597, 2584, 4181...

````
algoritmo "Sequência de Fibonacci"

var
  contador, primeiroValor, segundoValor: Inteiro

  Procedimento ProximoFibonacci(var A, B: Inteiro)
  var
    terceiroValor: Inteiro
  Inicio
    terceiroValor <- A + B
    
    Escreva(terceiroValor)
    
    A <- B
    B <- terceiroValor
  FimProcedimento

inicio
  primeiroValor <- 1
  Escreva(primeiroValor)
  
  segundoValor <- 1
  Escreva(segundoValor)
  
  Para contador <- 3 ate 15 faca
    ProximoFibonacci(primeiroValor, segundoValor)
  FimPara
  
fimalgoritmo
````

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>
