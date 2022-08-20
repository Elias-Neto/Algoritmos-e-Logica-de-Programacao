# 🔀 Aula 07 - Estruturas Condicionais (Parte 01) 

<br>

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver e executar os algoritmos em **Portugol**.

<br>

> 🖖 Essas anotações foram feitas a partir das aulas do professor **Gustavo Guanabara**. <br>
> 👉 Link para acessar as vídeo-aulas e os materiais do curso: https://www.cursoemvideo.com/curso/curso-de-algoritmo/

<br>

> Nessa aula, a gente começa a se perguntar **"e se acontecer tal coisa..."**

<br>

## ➡ **Estrutura Condicional Simples**

- É uma estrutura que gira em torno de **uma única condição**.

- Possui **um único caminho**: se a condição for verdadeira, execute o bloco.

<br>

### Sintaxe da Estrutura: 

- se ***acontecer tal coisa*** então ***faça aquilo***.

````
Se (expressao) entao
  Bloco
FimSe
````

Exemplo:

- Se ***eu tiver dinheiro*** então ***vou viajar para Disney***.

````
algoritmo "Estrutura Condicional Simples"

var
  dinheiro: Real
  
inicio
  Escreva("Quanto dinheiro eu tenho? R$")
  Leia(dinheiro)
  Se (dinheiro >= 10000) entao
    EscrevaL("Partiu Disney!")
  FimSe
  
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Atingiu a Maioridade? :**

<br>

- Faça um programa que pergunte o ano atual e o de nascimento do usuário (guarde 
esses valores dentro de variáveis), calcule a idade do usuário e exiba-a na tela. Se
a idade do usuário for maior que 21 anos, exiba uma mensagem informando que o usuário
já atingiu a maioridade. 

````
algoritmo "Atingiu a Maioridade?"

var
  anoAtual, anoNasc, idade: Real
   
inicio
   Escreva("Em que ano estamos? ")
   Leia(anoAtual)
   Escreva("Em que ano você nasceu? ")
   Leia(anoNasc)
   idade <- anoAtual - anoNasc
   Escreva("Atualmente, você tem ", idade, " anos")
   Se (idade >= 21) entao
      Escreval(" e já atingiu a maioridade")
   FimSe
     
fimalgoritmo
````

<br>

## 🔀 **Estrutura Condicional Composta**

- Assim como a condicional simples, a estrutura condicional composta também gira em torno de **uma única condição**. 

- Entretanto, a composta possui **dois caminhos**: se a condição for verdadeira, execute o bloco x, senão, 
execute o bloco y.

<br>

### Sintaxe da Estrutura: 

- se ***acontecer tal coisa*** então ***faça isso*** senão ***faça aquilo***.

````
Se (expressao) entao
  BlocoX
senao
  BlocoY
FimSe
````

Exemplo:

- Se ***eu tiver dinheiro*** então ***vou viajar para Disney*** senão ***vou ficar em casa***.

````
algoritmo "Estrutura Condicional Composta"

var
  dinheiro: Real
  
inicio
  Escreva("Quanto dinheiro eu tenho? R$")
  Leia(dinheiro)
  Se (dinheiro >= 10000) entao
    EscrevaL("Vou viajar para Disney! #PartiuDisney")
  senao
    EscrevaL("Vou ficar em Casa! #Chateado")
  FimSe
  
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Par ou Ímpar :**

<br>

- Construa um algoritmo que leia um número qualquer, detecte se ele é par ou ímpar e exiba
o resultado na tela.

````
algoritmo "Par Ou Ímpar"

var
 N: Inteiro
   
inicio
  Escreva("Digite um número qualquer: ")
  Leia(N)
  Se (N % 2 = 0) entao
    Escreval("O número ", N," é PAR")
  senao
    Escreval("O numero ", N," é ÍMPAR")
  FimSe
  
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Cálculo do IMC :**

<br>

- Crie um algoritmo que leia a massa e altua do usuário, calcule o IMC dele, e informe
se o usuário está na faixa de peso ideal ou não.

- Cálculo de IMC: massa/(altura^2)

- Faixa ideal de peso é quando o IMC está entre 18.5 e 25

````
algoritmo "Calculo IMC"

var
 massa, altura, IMC:Real
   
inicio
  Escreva("Massa(kg): ")
  Leia(massa)
  Escreva("Altura(m): ")
  Leia(altura)
  
  IMC <- massa/(altura^2)
  
  Escreval("IMC: ", IMC:5:2)   // IMC:5:2 é uma formatação do valor da variável IMC. Significa que eu quero um número com 5 casas decimais, sendo 2 delas depois da vírugula
  Se (IMC >= 18.5) e (IMC < 25) entao
     Escreva("Parabéns! Você está no seu peso ideal.")
  senao
       Escreva("Você não está na faixa de peso ideal")
  FimSe
  
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Está Apto a Dirigir? :**

<br>

- Faça um programa para o Departamento de Trânsito que solicite e leia o ano atual e 
o ano de nascimento do usuário, calcule a idade dele e, se ele tiver 18 anos ou mais
idade, informe que ele está apto para tirar a carteira, se não, exiba que ele inapto
para tirar a carteira.

````
algoritmo "Esta Apto a Dirigir?"

var
  idade, anoAtual, anoNasc: Inteiro
   
inicio
  Escreval("--------------------------")
  Escreval(" DEPARTAMENTO DE TRÂNSITO ")
  Escreval("--------------------------")
  Escreva("Ano Atual (yyyy): ")
  Leia(anoAtual)
  Escreva("Ano de Nascimento (yyyy): ")
  Leia(anoNasc)
  
  Escreval("--------- STATUS ---------")
  idade <- anoAtual - anoNasc
  Escreval("IDADE: ", idade)
  Se (idade >= 18) entao
     Escreval("APTO PARA TIRAR A CARTEIRA")
  senao
       Escreval("INAPTO PARA TIRAR A CARTEIRA")
  FimSe
  Escreva("--------------------------")
  
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Aluno Aprovado ou Reprovado? :**

<br>

- Desenvolva uma aplicação para a Escola Javali Cansado que solicite e leia 2 notas,
calcule a média, e, se a média for maior ou igual a 7, informe que o aluno(a) foi
aprovado, se não, informe que foi reprovado.

````
algoritmo "Aluno aprovado ou reprovado?"

var
  nota1, nota2, media:Real
   
inicio
  Escreval("-----------------------")
  Escreval(" ESCOLA JAVALI CANSADO ")
  Escreval("-----------------------")
  Escreva("Primeira Nota: ")
  Leia(nota1)
  Escreva("Segunda Nota: ")
  Leia(nota2)

  Escreval("-----------------------")
  media <- (nota1+nota2)/2
  Escreval("MÉDIA: ", media:2:1)
  Se (media >= 7) entao
    Escreval("ALUNO(A) APROVADO")
  senao
    Escreval("ALUNO(A) REPROVADO")
  FimSe
  Escreva("------------------------")
      
fimalgoritmo
````

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>
