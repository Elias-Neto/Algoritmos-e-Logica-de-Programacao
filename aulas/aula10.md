# 🔁 Aula 10 - Estruturas de Repetição (Parte 02)

<br>

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver algoritmos em **Portugol**.

<br>

> 🖖 Essas anotações foram feitas a partir das aulas do professor **Gustavo Guanabara**. <br>
> 👉 Link para acessar as vídeo-aulas e os materiais do curso: https://www.cursoemvideo.com/curso/curso-de-algoritmo/

<br>

## **Estrutura de Repetição - "Repita"**

- É uma estrutura que gira em torno de **uma condição**.

- Diferentemente da estrutura "Enquanto", na "Repita" *o teste lógico é feito no **fim** da estrutura* e não no início.

- Por esse motivo, a estrutura REPITA é utilizada quando não se sabe quantas vezes vai repetir o loop

<br>

### Sintaxe da Estrutura:

- repita ***tal coisa*** até que ***tal condição*** seja verdadeira

````
Repita
  Bloco
Ate (expressão)
````

Exemplo:

- Você está de castigo até arrumar seu quarto.

````
Repita
  castigo
Ate (arrumar quarto)
liberada
````

- Nesse exemplo, o bloco de código "castigo" será executado até que a expressão "arrumar quarto" seja falsa (ou seja, haverá um **loop**, uma **repetição**).
Quando a expressão "arrumar quarto" for falsa, o loop irá parar e a linha abaixo será executada (ou seja, a pessoa será liberada do castigo).

<br>

## ***Enquanto x Repita***

- É importante entendermos a relação entre essas duas estruturas.

- Lembra que ambas giram em torno de **uma condição**? Pois bem...

- A diferença entre elas está justamente nesse fato, *uma é o **complemento lógico** da outra*, perceba:

  - "**_ENQUANTO_ não arrumar seu quarto** você vai ficar de castigo."

  - "Você vai ficar de castigo **_ATÉ_ arrumar seu quarto**."

- E por que isso é importante? Bem, lembra que "girar em torno de uma condição" significa que a estrutura possui um **Teste Lógico**? Olha que interessante:

  - Na frase que utiliza o ***"Enquanto"***, a condição "não arrumar seu quarto" é verificada no início (ou seja, o **Teste Lógico é feito no início**).

  - Já na frase que utiliza o ***"Repita"***, a condição "arrumar seu quarto" é verificada no fim (ou seja, o **Teste Lógico é feito no fim**).

- Essa é a principal diferença entre essas estruturas de repetição, as suas **Sintaxes Lógicas** (suas Construções Lógicas):

```` 
✅ Teste Lógico Feito no INÍCIO                 ✅ Teste Lógico Feito no FIM

Enquanto (não arrumar quarto) faça               Repita
  castigo                                          castigo
FimEnquanto                                      Ate (arrumar quarto)
liberada                                         liberada
````

- Por isso que:
  
  - A estrutura de repetição **ENQUANTO** é utilizada quando se **sabe quantas repetições ocorrerão**. 

  - A estrutura de repetição **REPITA** é utilizada quando **não se sabe quantas repetições ocorrerão**.


<br>

### 🏋️‍♂️ **Exercício Prático - Contar de 1 Até 10 :**

<br>

- Crie um algoritmo que conte de 1 até 10.

````
algoritmo "Contar de 1 Até 10"

var
  contador: Inteiro

inicio
  Repita
    contador <- contador + 1
    Escreval(contador)
  Ate (contador = 10)

fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Gerador de Tabuada :**

<br>

- Desenvolva um algoritmo que leia um número, calcule e exiba a tabuada desse número.

````
algoritmo "Gerador de Tabuada"

var
  contador, numero, resultado: Inteiro
  
inicio
  EscrevaL(" GERADOR DE TABUADA  ")
  EscrevaL("---------------------")
  Escreva("Quer ver a tabuada de qual número? ")
  Leia(numero)
  EscrevaL()
  
  Repita
    contador <- contador + 1
    
    resultado <- numero * contador
    
    Escreval(numero, " x ", contador, " = ", resultado)
  Ate (contador = 10)
  
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Quantos Números São Negativos :**

<br>

- Crie um algoritmo que leia cinco números e, no final, mostre quantos são negativos.

````
algoritmo "Quantos Números São Negativos"

var
  numero, contador, totalNegativos: Inteiro
  
inicio
  contador <- 1
  
  Repita
    Escreva("Digite um número: ")
    Leia(numero)
    
    Se (numero < 0) entao
      totalNegativos <- totalNegativos + 1
    FimSe
    
    contador <- contador + 1
  Ate (contador > 5)
  
  Escreval("Foram digitado ", totalNegativos, " números negativos")
  
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - Fatorial de Um Número :**

<br>

- Desenvolva um programa que leia um número, calcule e exiba o faturial desse número.

- Fatorial é basicamente o número multiplicado por seus antecessores:
  - 3! = 3 x 2 x 1 = 6
  - 5! = 5 x 4 x 3 x 2 x 1 = 120

````
algoritmo "Fatorial de Um Número"

var
  numero, fatorial: Inteiro
  
inicio
  Escreva("Digite um nùmero: ")
  Leia(numero)
  
  fatorial <- 1
  Repita
    fatorial <- fatorial * numero
    numero <- numero - 1
  Ate (numero < 1)
  
  Escreval("O valor do fatorial de ", numero, " é igual a ", fatorial)
  
fimalgoritmo
````

- **ADICIONAL**: Permitir que o usuário execute o programa quantas vezes ele quiser.

````
algoritmo "Fatorial de Um Número"

var
 numero, fatorial: Inteiro
 resposta: Caractere
 
inicio
   Repita
      Escreva("Digite um número: ")
      Leia(numero)
      
      fatorial <- 1
      
      Repita
         fatorial <- fatorial * contador
         numero <- numero - 1
      Ate (numero = 1)
      
      Escreval("O valor do fatorial de ", numero, " é igual a ", fatorial)
      
      Escreva("Quer continuar? [S/N] ")
      Leia(resposta)
   Ate (resposta = "N")
   
fimalgoritmo
````

<br>

### 🏋️‍♂️ **Exercício Prático - É Um Número Primo? :**

<br>

- Desenvolva um algoritmo que leia um número, detecte e informe se esse número é ou não primo.

- Ser um Número Primo, significa que da contagem de um até o número, ele só tem dois divisores (um e ele mesmo).

````
algoritmo "É Um Número Primo?"

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

<br>

- Faça uma aplicação que dê ao usuário três opções de contagem: 
  
  - De 1 até 10 (Caso for escolhida, calcule e exiba a contagem).

  - De 10 até 1 (Caso for escolhida, calcule e exiba a contagem).

  - Sair (Caso for escolhida, finalize a aplicação).

````
algoritmo "Super Contador"

var
  contagem, contador: Inteiro
  
inicio
  Repita
    Escreval()
    Escreval()
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

<br>

- Faça um programa que leia o sexo, a idade e a cor de cabelo do usuário.

- O programa deve detctar e informar a quantidade de:

  - Homens, com mais de 18 anos e cabelos castanhos.
  
  - Mulheres, entre 25 e 30 anos e cabelos loiros.

- Esse programa deve se repetir quantas vezes o usuário quiser

````
algoritmo "Escolhendo Pessoas"

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

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>
