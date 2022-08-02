# Aula 08 - Estruturas Condicionais (Parte 02) 🔀

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver e executar os algoritmos em **Portugol**.

<br>

## 🔱 **Estrutura Condicional Aninhada**

- é uma estrutura que gira em torno de mais de uma condição 
- possui três caminhos ou mais

Sintaxe da estrutura: 

- se ***acontecer essa coisa*** então ***faça isso*** senão se ***acontecer aquela coisa*** 
entao ***faça aquilo*** senao ***faça isto***

````
  Se (expressao A) entao
    BlocoX
  senao
    Se (exprssao B) entao
      BlocoY
    senao
      BlocoZ
    FimSe
  FimSe
````

Exemplo:

* Se ***eu tiver dinheiro*** então ***vou viajar para Disney*** senão se 
***eu tiver uma graninha*** então ***vou visitar minha cidade natal*** senao
***vou ficar em casa***

````
algoritmo "condicional aninhada"
var
  dinheiro: Real
inicio
  Escreva("Quanto dinheiro eu tenho? R$")
  Leia(dinheiro)
  Se (dinheiro >= 10000) entao
    EscrevaL("Partiu Disney!")
  senao
    Se (dinheiro >= 5000) e (dinheiro < 10000) entao
      Escreva("Visitar família")
    senao
      EscrevaL("#chateado")
    FimSe
  FimSe
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Aluno Aprovador, Reprovado ou Em Recuperação :**

- Construa um algoritmo que leia duas notas de um aluno(a), calcule a média, exiba a média,
detecte e informe se o aluno(a) foi aprovado(a), reprovado(a) ou está em recuperação.

````
algoritmo "Aluno"
var
   nota1, nota2, media: Real
inicio
   Escreva("Primeira Nota: ")
   Leia(nota1)
   Escreva("Segunda Nota: ")
   Leia(nota2)
   media <- (nota1 + nota2) / 2
   EscrevaL("A media do aluno(a) foi ", media:4:2)
   Se (media >= 7) entao
      EscrevaL("Aluno(a) APROVADO(A)")
   senao
      Se (media >= 5) e (media <7) entao
         EscrevaL ("Aluno(a) em RECUPERACAO(A)")
      senao
         EscrevaL ("Aluno(a) REPROVADO(A)")
      FimSe
   FimSe
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exércicio Prático - Cálculo do IMC :**

- Crie um algoritmo que leia a massa e altua do usuário, calcule o IMC dele, e informe
se em qual faixa de peso ele está.

- Cálculo de IMC: massa/(altura^2)

- Faixas de peso:

IMC | Faixa de Peso
---|---
abaixo de 17 | Muito abaixo do peso
entre 17 e 18.5 | Abaixo do peso
de 18.5 a 25 | Peso ideal
de 25 a 30 | Sobrepeso
de 30 a 35 | Obesidade
de 35 a 40 | Obesidade Severa
40 ou mais | Obesidade Mórbida

````
algoritmo "CalculoIMC"
var
   massa, altura, IMC: Real
inicio
   Escreva("Massa (Kg): ")
   Leia(massa)
   Escreva("Altura (m): ")
   Leia(altura)
   IMC <- massa / (altura ^ 2)
   EscrevaL("IMC: ", IMC:5:2)
   Se (IMC < 17) entao
      EscrevaL ("Muito abaixo do Peso")
   senao
      Se (IMC >= 17) e (IMC < 18.5) entao
         EscrevaL ("Abaixo so Peso")
      senao
         Se (IMC >= 18.5) e (IMC < 25) entao
            EscrevaL ("Peso ideal")
         senao
            Se (IMC >= 25) e (IMC < 30) entao
               EscrevaL ("Sobrepeso")
            senao
               Se (IMC >= 30) e (IMC < 35) entao
                  EscrevaL ("Obesidade")
               senao
                  Se (IMC >= 35) e (IMC < 40) entao
                     EscrevaL ("Obesidade Severa")
                  senao
                     EscrevaL ("Obesidade Morbida")
                  FimSe
               FimSe
            FimSe
         FimSe
      FimSe
   FimSe
fimalgoritmo
````

<br>

## 🔱 **Estrutura Condicional "Escolha Caso"**

- é uma estrutura que gira em torno de mais de uma condição 

- possui três caminhos ou mais

- não serve para testar faixas de valores (>, <, >=, <=)

- é mais simpes do que a estrutura condicional aninhada

- usar em casos de muitos testes com valores numéricos simples

Sintaxe da estrutura: 

````
  Escolha (variável)
    Caso valor
      Bloco A
    Caso valor
      Bloco B
    Caso valor
      Bloco C
    OutroCaso
      Bloco D
    FimEscolha
````

<br>

### 🏋️‍♂️ **Exércicio Prático - Criança Esperança :**

- Crie um programa que exiba opções de doações na tela, leia a opção escolhida pelo usuário e
mostre uma mensagem confirmando o valor doado e agradecendo.

````
algoritmo "CriancaEsperanca"
var
   opcao : Inteiro
   valor: Real
inicio
   EscrevaL ("---------------------------")
   EscrevaL ("     CRIANCA ESPERANCA     ")
   EscrevaL ("---------------------------")
   Escreval (" Muito obrigado por ajudar ")
   Escreval (" [1] para doar R$10 ")
   Escreval (" [2] para doar R$25 ")
   Escreval (" [3] para doar R$50 ")
   Escreval (" [4] para doar outros valores ")
   Escreval (" [5] para cancelar ")
   Leia (opcao)
   Escolha opcao
      Caso 1
            valor <- 10
      Caso 2
            valor <- 25
      Caso 3
            valor <- 50
      Caso 4
            Escreva ("Qual o valor da doacao? R$")
            Leia (valor)
      Caso 5
            valor <- 0
   FimEscolha
   Escreval ("------------------------")
   Escreval (" SUA DOACAO FOI DE R$", Valor)
   Escreval (" MUITO OBRIGADO!")
   Escreval ("------------------------")
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Quantidade de Dependentes de um Funcionário :**

- Crie uma aplicação que leia o nome do(a) funcionário(a), o salário dele(a), a quatidade
de dependentes dessa pessoa e calcule o novo salário dela de acordo com essa quantidade

- Aumento de 5% caso não tenha dependentes

- Aumento de 10% caso tenha 1, 2 ou 3 dependentes

- Aumento de 15% caso tenha 4, 5, ou 6 dependentes
 
- Aumento de 18% caso tenha mais de 6 dependentes

````
algoritmo "DependentesFuncionario"
var
   nome: Caractere
   salario, novoSalario : Real
   dependentes : Inteiro
inicio
   Escreva ("Qual o nome do Funcionário(a)? ")
   Leia (nome)
   Escreva ("Qual o salario do Funcionario(a)? R$")
   Leia (salario)
   Escreva ("Qual e a quantidade de dependentes? ")
   Leia (dependentes)
   Escolha dependentes
      Caso 0
            novoSalario <- salario + (salario*5/100)
      Caso 1, 2, 3
            novoSalario <- salario + (salario*10/100)
      Caso 4, 5, 6
            novoSalario <- salario + (salario*15/100)
      OutroCaso
            novoSalario <- salario + (salario*18/100)
   FimEscolha
   EscrevaL ("O novo salario de ", nome, " sera de R$", novoSalario:5:2)
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Aproveitamento de um Aluno(a) :**

- Cronstrua um algoritmo que leia duas notas de uma aluno(a), calcule a média, 
detecte e informe qual foi o aproveitamento.

Média | Aproveitamento
---|---
9.0 - 10.0 | A
8.0 - 8.9 | B
7.0 - 7.9 | C
6.0 - 6.9 | D
5.0 - 5.9 | E
0.0 - 5.0 | F


````
algoritmo "SituacaoAluno"
var
   nota1, nota2, media: Real
inicio
   EscrevaL("-----------------------")
   EscrevaL(" ESCOLA JAVALI CANSADO ")
   EscrevaL("-----------------------")
   Escreva("Primeira Nota: ")
   Leia(nota1)
   Escreva("Segunda Nota: ")
   Leia(nota2)
   media <- (nota1 + nota2)/2
   EscrevaL("-----------------------")
   EscrevaL(" MEDIA: ", media:3:1)
   Se (media >=9) e (media <= 10) entao
      EscrevaL(" APROVEITAMENTO: A ")
   senao
      Se (media >= 8) e (media < 9) entao
         EscrevaL (" APROVEITAMENTO: B ")
      senao
         Se (media >= 7) e (media < 8) entao
            EscrevaL (" APROVEITAMENTO: C ")
         senao
            Se (media >= 6) e (media < 7) entao
               EscrevaL (" APROVEITAMENTO: D ")
            senao
               Se (media >= 5) e (media < 6) entao
                  EscrevaL (" APROVEITAMENTO: E ")
               senao
                  EscrevaL(" APROVEITAMENTO: F ")
               FimSe
            FimSe
         FimSe
      FimSe
   FimSe
   EscrevaL("-----------------------")
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Partida de Futebol :**

- Crie uma aplicação que leia quantos gols um time A e um time B fizeram em uma partida,
calcule e exiba a diferença de gols, detecte e informe o status da partida.

Diferença | Status
---|---
0 | Empate
1, 2, 3 | Partida Normal
4, 5, 6, 7 | Goleada
8 ou mais | Incomum

````
algoritmo "PartidaFutebol"
var
   golsTimeA, golsTimeB, diferenca: Real
inicio
   EscrevaL("---------------------")
   EscrevaL("   TIME A x TIME B   ")
   EscrevaL("---------------------")
   Escreva("Quantos gols do TIME A? ")
   Leia(golsTimeA)
   Escreva("Quantos gols do TIME B? ")
   Leia(golsTimeB)
   Se (golsTimeA > golsTimeB) entao
      diferenca <- golsTimeA - golsTimeB
   senao
      diferenca <- golsTimeB - golsTimeA
   FimSe
   EscrevaL("-----------------------")
   EscrevaL(" DIFERENCA: ", diferenca)
   Escolha diferenca
      Caso 0
            EscrevaL(" STATUS: EMPATE ")
      Caso 1, 2, 3
            EscrevaL(" STATUS: PARTIDA NORMAL ")
      Caso 4, 5, 6, 7
            EscrevaL(" STATUS: GOLEADA ")
      OutroCaso
            EscrevaL(" STATUS: ALGO INCOMUM. ")
            EscrevaL(" Voce digitou os dados corretos? ")
   FimEscolha
   EscrevaL("-----------------------")
fimalgoritmo
````