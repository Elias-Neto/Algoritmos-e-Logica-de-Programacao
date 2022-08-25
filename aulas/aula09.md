# 🔁 Aula 09 - Estruturas de Repetição (Parte 01)

<br>

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver algoritmos em **Portugol**.

<br>

> 🖖 Essas anotações foram feitas a partir das aulas do professor **Gustavo Guanabara**. <br>
> 👉 Link para acessar as vídeo-aulas e os materiais do curso: https://www.cursoemvideo.com/curso/curso-de-algoritmo/

<br>

## **Estrutura de Repetição - "Enquanto"**

- É uma estrutura que gira em torno de **uma condição**.
  
  - Percebemos anteriormente (com as estruturas condicionais), que "girar em torno de uma condição" significa que é uma estrutura na qual haverá uma expressão lógica que, se for verdadeira, então haverá a execução de um bloco de código.
  
  - Essa verificação da expressão lógica (para conferir se ela é verdadeira ou falasa) é o que chamamos de **Teste Lógico**.

- Na estrutura de repetição ENQUANTO, *o teste lógico é feito no **início** da estrutura*.

- Por esse motivo, essa estrutura é utilizada quando se sabe quantas repetições ocorrerão.

<br>

### Sintaxe da Estrutura:

- enquanto ***tal condição*** for verdadeira faça ***tal coisa***

````
Enquanto (expressão) faça
  Bloco
FimEnquanto
````

Exemplo:

- Enquanto ***não arrumar seu quarto*** está de ***castigo***

````
Enquanto (não arrumar quarto) faça
  castigo
FimEnquanto
liberado
````

- Nesse exemplo, enquanto a expressão "não arumar quarto" for verdadeira, o bloco de código "castigo" será executado (ou seja, haverá um **loop**, uma **repetição**). Isso ocorrerá enquanto a expressão for verdadeira, até ela se tornar falsa. Quando ela for falsa, o loop irá parar e a linha abaixo será executada (ou seja, a pessoa será liberada do castigo).

<br>

### 🏋️‍♂️ **Exercício Prático - Contar de 0 até 10 :**

<br>

- Crie um algoritmo que conte de 0 até 10.

````
algoritmo "Contar de 0 até 10"

var
  contador:Inteiro
   
inicio
  
  Enquanto (contador <= 10) faca
    Escreval(contador)
    contador <- contador + 1
  FimEnquanto
  
  EscrevaL()
  Escreval("Terminei de contar!")
   
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Contar de 10 até 0 :**

<br>

- Crie um algoritmo que conte de 10 até 0.

````
algoritmo "Contar de 10 até 0"

var
  contador:Inteiro
   
inicio
  contador <- 10
  
  Enquanto (contador >= 0) faca
    Escreval(contador)
    contador <- contador - 1
  FimEnquanto
  
  EscrevaL()
  Escreval("Terminei de contar!")
   
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Contar de 0 até onde o usuário quiser:**

<br>

- Crie um algoritmo que conte de 0 até onde o usuário quiser.

````
algoritmo "Contar de 0 até onde o usuário quiser"

var
  inici0, fim: Inteiro
   
inicio
  Escreva("Até onde o você quer contar? ")
  Leia(fim)
  
  EscrevaL()
  Enquanto (inici0 <= fim) faca
    Escreval(inici0)
    inici0 <- inici0 +  1
  FimEnquanto
  
  EscrevaL()
  Escreval("Terminei de contar!")
   
fimalgoritmo
````

- **ADICIONAL**: Pergunte ao usuário o valor do salto dessa conta.

````
algoritmo "Contar de 0 até onde o usuário quiser *ADICIONAL*"

var
  inici0, fim, salto: Inteiro
   
inicio
  Escreva("Até onde o você quer contar? ")
  Leia(fim)
  Escreva("Qual valor do salto? ")
  Leia(salto)
  
  EscrevaL()
  Enquanto (inici0 <= fim) faca
    Escreval(inici0)
    inici0 <- inici0 + salto
  FimEnquanto
  
  EscrevaL()
  Escreval("Terminei de contar!")
   
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Ler 5 números e somá-los :**

<br>

- Crie um algoritmo que leia 5 números e some-os.

````
algoritmo "Ler 5 números e somá-los"

var
  contador, numero, soma: Inteiro
   
inicio
  contador <- 1
  
  Enquanto (contador <= 5) faca
    Escreva("Digite o ", contador, "° número: ")
    Leia(numero)
    
    soma <- soma + numero
    
    contador <- contador + 1
  FimEnquanto
  
  EscrevaL()
  Escreval("A soma de todos os valores é ", soma)
   
fimalgoritmo
````

- **ADICIONAL**: Mostrar qual foi o maior e o menor número digitado.

````
algoritmo "*ADICIONAL* Ler 5 números e somá-los"

var
  contador, numero, soma, menor, maior: Inteiro
  
inicio
  contador <- 1
  
  Enquanto (contador <= 5) faca
    Escreva("Digite o ", contador, "°. valor: ")
    Leia(numero)
    
    Se (contador = 1) entao
      menor <- numero
    FimSe
    
    Se (numero > maior) entao
      maior <- numero
    FimSe
    
    Se (numero < menor) entao
      menor <- numero
    FimSe
    
    soma <- soma + numero
    
    contador <- contador + 1
  FimEnquanto
  
  EscrevaL()
  Escreval("A soma de todos os valores é ", soma)
  Escreval("O maior valor digitado foi ", maior)
  Escreval("O menor valor digitado foi ", menor)
   
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Fazer conversão de moedas 4 vezes :**

<br>

- Faça um algoritmo que solicite ao usuário um valor em reais e converta esse valor para dólar, faça com que isso se repita 4 vezes.

````
algoritmo "Fazer conversão de moedas 4 vezes"

var
  reais, dolar: Real
  contador: Inteiro
  
inicio
  contador <- 1
  
  Enquanto (contador <= 4) faca
    Escreva("Qual o valor em R$? ")
    Leia(reais)
    
    dolar <- reais / 5.2
    
    EscrevaL("O valor convertido: U$", dolar:5:2)
    
    contador <- contador + 1
    EscrevaL()
  FimEnquanto
   
fimalgoritmo
````

- **ADICIONAL**: Perguntar ao usuário quantas conversões serão realizadas.

````
algoritmo "Fazer conversão de moedas 4 vezes"

var
  reais, dolar: Real
  contador, conversoes: Inteiro
   
inicio
  contador <- 1

  Escreva("Deseja relaizar quantas conversões? ")
  Leia(conversoes)

  Enquanto (contador <= conversoes) faca
    EscrevaL()

    Escreva("Qual o valor em R$? ")
    Leia(reais)

    dolar <- reais / 5.2

    EscrevaL("O valor convertido: U$", dolar:5:2)
    
    contador <- contador + 1
  FimEnquanto
   
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Contador Inteligente :**

<br>

- Crie um programa que leia o início e o fim da contagem, detecte se ela é progressiva ou regressiva e realize a contagem.

````
algoritmo "EXERCÍCIO 01 - CONTAGEM INTELIGENTE "

var
   ini, fim: Inteiro
   
inicio
   Escreval("CONTAGEM INTELIGENTE")
   Escreval("--------------------")
   Escreva("Início: ")
   Leia(ini)
   Escreva("Fim: ")
   Leia(fim)
   
   Escreval("--------------------")
   Escreval("      CONTANDO      ")
   Escreval("--------------------")
   
   Se (fim > ini) entao
      Enquanto (ini <= fim) faca
         Escreva(ini, (".. "))
         ini <- ini + 1
      FimEnquanto
   senao
      Enquanto (fim <= ini) faca
         Escreva(ini, (".. "))
         ini <- ini -1
      FimEnquanto
   FimSe
   
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Melhor Aluno da Turma :**

<br>

- Desenvolva um programa que leia a quantidade de alunos em uma turma, o nome e a nota de cada aluno, detecte e informe qual foi o aluno(a) com o melhor aproveitamente e a sua respectiva nota.

````
algoritmo "Melhor Aluno da Turma"

var
  alunos, contador: Inteiro
  nome, melhorAproveitamento: Caractere
  nota, melhorNota: Real
  
inicio
  contador <- 1
  
  Escreval("------------------------")
  Escreval(" Escola Santa Paciência ")
  Escreval("------------------------")
  Escreva("Quantos alunos a turma tem? ")
  Leia(alunos)
  
  Enquanto (contador <= alunos) faca
    Escreval("-----------------")
    Escreval("ALUNO(A) ", contador)
    Escreva("Nome do aluno(a): ")
    Leia(nome)
    Escreva("Nota de ", nome, ": ")
    Leia(nota)
    
    Se (nota > melhorNota) entao
      melhorNota <- nota
      melhorAproveitamento <- nome
    FimSe
    
    contador <- contador + 1
  FimEnquanto
  
  Escreval("-----------------")
  Escreval("O melhor aproveitamento foi de ", melhorAproveitamento, " com a nota ", melhorNota:3:1)

fimalgoritmo
````

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>

<br>

<a href="../README.md">Voltar</a>