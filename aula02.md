# Aula 02 - Primeiro Algoritmo 1️⃣

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver e executar os algoritmos em **Portugol**.

<br>

<br>

## 💬 **Comentários**

- são trechos de códigos não executáveis
- utilizados normalmente para organização/explicação do código

````
algoritmo "comemtarios" 
var

inicio
      // isto é um comentário
      Escreva("Olá, Mundo!")
fimalgoritmo
````

<br>

## 📤 **Comandos de Saída de Dados (Output)**

- são comandos que, quando executados, mostrarão algo na tela
- responsáveis pela saída de dados

````
algoritmo "comandos de saida"
var

inicio
      Escreva("Olá, Mundo!")    // escreverá "Olá, Mundo!" na tela
      EscrevaL("Olá, Mundo!")   // escreverá "Olá, Mundo!" na tela e pulará uma linha
fimalgoritmo
````

<br>

## 🗄 **Variáveis**

- para entender o conceito de variáveis pense na seguinte analogia:
a memória do computador é um **armário** gigante com várias **gavetas**

- essas gavetas são as variáveis, elas tem o poder de guardar coisas (dados)

- cada gaveta dessa possui um adesivo com seu nome

- todos esses nomes seguem um padrão: "nome escolhido" + tipo da coisa (dado) armazenada

- em uma variável simples só é possível armazenar 1 valor (se quiser colocar outro valor, tem que tirar o primeiro)

### 🔠 **Nome de variáveis**

[x] Deve começar com uma letra

[x] Não pode utilizar acentos

[x] Não pode utilizar símbolos, exceto _ (underline)

[x] Não pode ter espaços em branco

[x] Não pode ser uma plavra reserva

````
  // Exemplos:
  
  ✅ Nota1     ❌ Média
  ❌ 9idade    ✅ inicio_algoritmo
  ✅ media     ❌ Salário Bruto
  ❌ var       ✅ salarioBruto 
````

<br>

## 🎲 **Tipos de Dados**

Inicialmente, vamos abordar só os tipos de dados primitivos:

- Inteiro - (1, 3, -5, 198, 0)
- Real - (0.5, 5.0, 9.8, -77.3, 3.1415)
  - na programação, utilizamos "." e não ","
- Caractere - ("Elias", "Neto", "Algoritmo", "123") 
  - String é um conjunto de carcteres
- Lógico - (verdadeiro, falso)

<br>

Exemplo de um algoritmo utilizando os conceitos que vimos até agora:
````
  algoritmo "apanhado do que vimos"
  var
    msg1, msg2: caractere
  inicio
        msg1 <- "Olá,"        // msg1 recebe "Olá"      - atribuição de valor
        msg2 <- " Mundo!"     // msg2 recebe "Mundo!"   - atribuição de valor
        Escreva(msg1, msg2) 
  fimalgoritmo
````

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>