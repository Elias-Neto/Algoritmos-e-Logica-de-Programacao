# 🛠 Aula 13 - Funções

<br>

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver algoritmos em **Portugol**.

<br>

> 🖖 Essas anotações foram feitas a partir das aulas do professor **Gustavo Guanabara**. <br>
> 👉 Link para acessar as vídeo-aulas e os materiais do curso: https://www.cursoemvideo.com/curso/curso-de-algoritmo/

<br>

## **O que são Funções?**

- De maneira pragmática, funções são procedimentos que, ao final da estrutura, **retornam um valor**.

- Portanto, os conceitos que valem para os procedimentos também são válidos para as funções:

  - Ambos são **blocos de código** que se **repetem** com certa frequência, por isso são importantíssimos para a construção de um **código limpo**.

  - Possuem sintaxes bem semelhantes:

  ````
  Funcao nomeDaFuncao(): tipoDaFuncao           Procedimento nomeDoProcedimento()
  inicio                                        Inicio
    Bloco                                         Bloco
    Retorne()                                   FimProcedimento
  FimFuncao
  ````

  - Ambos podem utilizar as passagens de parâmetros (tanto por valor como por referência). 

  - Por esses motivos giram em torno dos mesmo conceitos: Escopo, Argumentos, Parâmetros, etc...

<br>

## **Procedimento x Função - Quais são as diferenças?**

- Como foi dito no início: "funções são procedimentos que, ao final da estrutura, **retornam um valor**.".

- Nos ***Procedimentos*** não retorna-se um valor, neles ocorre simplesmente a execução de um bloco de código

- Já nas ***Funções*** retorna-se um valor, nelas um bloco de código é executado mas o objetivo é retornar um valor ao final da função.

<br>

**Exemplo - Somar Dois Números (Procedimento x Função) :**

````
algoritmo "Somar Dois Números (utilizando PROCEDIMENTO)"

var
  numero1, numero2: Inteiro
  
  Procedimento Soma(A, B: Inteiro)
  Inicio
     Escreval("A soma entre ", A, " e ", B, " é igual a ", A+B)
  FimProcedimento

inicio
  Escreva("Digite o primeiro valor: ")
  Leia(numero1)
  Escreva("Digite o segundo valor: ")
  Leia(numero2)
  
  Soma(numero1, numero2)

fimalgoritmo
````

````
algoritmo "Somar Dois Números (utilizando FUNÇÃO)"

var
  numero1, numero2, soma: Inteiro
  
  // Ao declarar uma função, é necessário definir o tipo de dado que ela irá retornar
  
  Funcao Soma(A, B: Inteiro): Inteiro 
  Inicio
    Retorne(A+B)
  FimFuncao

inicio
  Escreva("Digite o primeiro valor: ")
  Leia(numero1)
  Escreva("Digite o segundo valor: ")
  Leia(numero2)
  
  soma <- Soma(numero1, numero2)
  
  Escreval("A soma entre ", numero1, " e ", numero2, " é igual a ", soma)

fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Verificador Par/Ímpar :**

<br>

- Desenvolva um algoritmo que leia um número, verifique e informe se ele é par ou ímpar.

- Utilize uma função para realizar essa verificação.

````
algoritmo "Verificador Par/Ímpar"

var
  numero: Inteiro
  retorno: Caractere
   
Funcao ParOuImpar(N: Inteiro): Caractere
Inicio
  Se (N%2 = 0) entao
    Retorne("PAR")
  senao
    Retorne("ÍMPAR")
  FimSe
FimFuncao

inicio
  Escreva("Digite um número: ")
  Leia(numero)
  
  retorno <- ParOuImpar(numero)
  
  EscrevaL("O número ", numero, " é um valor ", retorno)
  
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Fatorial de Um Número :**

<br>

- Crie um algoritmo que leia um número, calcule e informe o fatorial desse número.

- Utilize uma função para realizar essa cálculo.

````
algoritmo "Fatorial de Um Número"

var
  numero, F: Inteiro

Funcao Fatorial(N:Inteiro): Inteiro
var
  contador, resultado: Inteiro
Inicio
  resultado <- 1
  
  Para contador <- 1 ate N faca
    resultado <- resultado * contador
  FimPara
  
  Retorne resultado
FimFuncao

inicio
  Escreva("Digite um número: ")
  Leia(numero)
  
  F <- Fatorial(numero)
  
  EscrevaL()
  Escreval("O valor de ", numero, "! è igual a ", F)
  
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Sequência de Fibonacci :**

<br>

- Desenvolva um algoritmo que calcule e exiba na tela os 15 primeiros números da sequência de fibonacci.

- Utilize uma função para realizar esse cálculo.

````
algoritmo "Sequência de Fibonacci"

var
  contador, primeiroNumero, segundoNumero, terceiroNumero: Inteiro

Funcao ProximoFibonacci(var N1, N2: Inteiro):Inteiro
var
  N3: Inteiro
Inicio
  N3 <- N1 + N2
  N1 <- N2
  N2 <- N3

  Retorne(N3)
FimFuncao

inicio
  Escreva(primeiroNumero)

  segundoNumero <- 1
  Escreva(segundoNumero)

  Para contador <- 3 ate 15 faca
    terceiroNumero <- ProximoFibonacci(primeiroNumero, segundoNumero)
    
    Escreva(terceiroNumero)
  FimPara

fimalgoritmo
````

<br>

## **Funções do Visualg - Manipulação de Strings**

<br>

 **site <- "CursoEmVideo"**

<br>

Função | Retorno | O que faz?
:--------- | :------: | -------:
Compr(site) | 12 | Retorna o comprimento de uma string
Copia(site, 6, 2) | Em | Retorna a copia de uma string contando a partir de um intervalo (string, inicioDoIntervalo, quantidadeDeLetras)
Maiusc(site) | CURSOEMVIDEO | Coloca todas as letras de uma string em maiúsculas
Minusc(site) | cursoemvideo | Coloca todas as letras de uma string em minúsculas
Pos("Video", site) | 8 | Retorna a posição de uma determinada string ou letra dentro de uma string maior
Asc("C") | 67 | Retorna o código específico de uma letra
Carac("67") | C | Retorna a letra específica de um código

<br>

### 🏋️‍♂️ **Exercício Prático - Analisador de Nomes :**

<br>

- Desenvolva um algoritmo, utilizando as funções do visualg, que leia o nome do usuário e:
  
  - Informe o total de letras do nome;
  
  - Exiba o nome em letras maiúsculas;
  
  - Exiba o nome em letras minúsculas;
  
  - Informe a primeira letra do nome;
  
  - Informe a última letra do nome;
  
  - Informe a posição da letra "A" no nome;
  
  - Informe a código correspondente a letra "A";
  
  - Informe a a letra correspondnete ao código 65;

  - Monte e exiba na tela o nome do usuário ao contrário.

````
algoritmo "Analisador de Nomes"

var
  nome: Caractere
  Contador: Inteiro

inicio
  EscrevaL(" ANLISADOR DE NOMES ")
  EscrevaL("--------------------")

  Escreva("Digite seu nome: ")
  Leia(nome)

  EscrevaL()
  Escreval("-> Total de letras do seu nome é ", Compr(nome))

  EscrevaL()
  Escreval("-> Seu nome em maiúsculas ", Maiusc(nome))

  EscrevaL()
  Escreval("-> Seu nome em minúsculas é ", Minusc(nome))

  EscrevaL()
  Escreval("-> A primeira letra do seu nome é ", Copia(Maiusc(nome), 1, 1))

  EscrevaL()
  Escreval("-> A última letra do seu nome é ", Copia(Maiusc(nome), Compr(nome), 1))

  EscrevaL()
  Escreval("-> Seu nome tem a letra A na posição ", Pos("A", Maiusc(nome)))

  EscrevaL()
  Escreval("-> O código da letra A é ", Asc("A"))

  EscrevaL()
  Escreval("A letra de código 65 é ", Carac(65))

  EscrevaL()
  Escreva("-> Seu nome ao contrário é ")
  Para Contador <- Compr(nome) ate 1 passo -1 faca
    Escreva(Copia(Maiusc(nome), Contador, 1))
  FimPara

  EscrevaL()

fimalgoritmo
````

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>

<br>

<a href="../README.md">Voltar</a>
