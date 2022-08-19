# 1️⃣ Aula 02 - Primeiro Algoritmo

<br>

> Lembrando: Durante todo este curso, será utilizado o **visualg** (visualizador de algoritmos) para poder desenvolver e executar os algoritmos em **Portugol**.

<br>

> Nessa aula, veremos conceitos fundamentais para o universo da programação. Entendendo bem esses conceito
> será fácil desenvolvermos nosso primeiro algoritmo. 😉

<br>

## 🏛 **Estrutura Básica de um Algoritmo no Visualg**

<br>

- No visualg, a estrutura básica de um algoritmo é formada por quatro **palavras reservadas**:

  - **"algoritmo"** : Define a existência e o início de um algoritmo. É necessário colocar um nome para o algoritmo.

  - **"var"** : Define a sessão de declaração de variáveis (conceito que vamos entender melhor mais adiante).

  - **"inicio"** : Define a sessão de comandos (conceito que vamos entender melhor mais adiante).

  - **"fimalgoritmo"** : Define o fim de um algoritmo.

<br>

````
algoritmo "nome do algoritmo"

var
  // Sessão de Declaração Variáveis

inicio
  // Sessão de Comandos

fimalgoritmo
````

<br>

> No visualg, você pode digitar "!", apertar "CTRL + ESPAÇO" e o próprio visualg formará essa estrutura básica.

<br>

## 💬 **Comentários**

<br>

- São trechos de códigos não executáveis.

- Utilizados normalmente para organização/explicação do código.

<br>

````
algoritmo "Comentários" 

var

inicio
  // isto é um comentário
  Escreva("Olá, Mundo!")

fimalgoritmo
````

<br>

## 📤 **Comandos de Saída de Dados (Output)**

<br>

- São comandos que, quando executados, mostrarão algo na tela.

- São responsáveis pela saída de dados.

<br>

````
algoritmo "Comandos de Saída de Dados (Output)"

var

inicio
  Escreva("Olá, Mundo!")    // escreverá "Olá, Mundo!" na tela
  EscrevaL("Olá, Mundo!")   // escreverá "Olá, Mundo!" na tela e pulará uma linha

fimalgoritmo
````

<br>

## 🗄 **Variáveis**

<br>

- Para entender o conceito de variáveis pense na seguinte analogia:
a memória do computador é um **"armário"** gigante com várias **espaços** vazios.

- Essas espaços são as *variáveis*, elas **servem para armazenar valores (dados)**.

- Cada espaço desse precisa ser identificado, por isso, cada um possui um "adesivo" com seu nome.

<br>

> **Exemplo**: na memória do computador ("armário"), eu quero reservar dois espaços (variáveis):
> um pra colocar uma bola (que é um tipo de brinquedo), e outro pra colocar um par de sapatos 
> (que é um tipo de calçado).

<br>

<img align="center" src="./images/variaveis.png">

<br>

> Se eu tiver outra bola a qual queria guardar no mesmo espaço, eu preciso tirar a primeira para
> poder colocar a segunda. 

<br>

<img align="center" src="./images/variaveis.gif">

<br>

> **Em uma variável simples, só podemos armarzenar um valor.**

<br>

### 🔠 **Nome de variáveis**

<br>

- Todos os nomes de variáveis seguem um padrão: **nome da variável + tipo de dado armazenado**

- Existem algumas **regras** que devemos seguir ao nomear uma variável:

  [x] Deve começar com uma letra

  [x] Não pode utilizar acentos

  [x] Não pode utilizar símbolos, exceto _ (underline)

  [x] Não pode ter espaços em branco

  [x] Não pode ser uma plavra reservada

<br>

````
// Exemplos:

✅ Nota1     ❌ Média
❌ 9idade    ✅ inicio_algoritmo
✅ media     ❌ Salário Bruto
❌ var       ✅ salarioBruto 
````

<br>

## 🎲 **Tipos de Dados**

<br>

- Inicialmente, vamos abordar só os tipos de dados **primitivos**:

  - **Inteiro**

    - Ex: 1, 3, -5, 198, 0

  - **Real**

    - Ex: 0.5, 5.0, 9.8, -77.3, 3.1415

    - na programação, utilizamos "." e não ","

  - **Caractere**

    - Ex: "Elias", "Neto", "Algoritmo", "123"

    - *String é um conjunto de carcteres*

  - **Lógico**

    - Ex: verdadeiro, falso

<br>

## **Exemplo de um algoritmo utilizando os conceitos que vimos até agora:**

<br>

````
algoritmo "Exemplo"

var
  msg1, msg2: caractere // declarando duas variáveis do tipo caractere

inicio
  msg1 <- "Olá,"        // msg1 recebe "Olá"      - atribuindo um valor à variável msg1
  msg2 <- " Mundo!"     // msg2 recebe "Mundo!"   - atribuindo um valor à variável msg2
  Escreva(msg1, msg2)   // comando de saída       - exibirá na tela os valores dentro das variáveis msg1 e msg2

fimalgoritmo
````

<br><br>

<p align="center"> Desenvolvido com 💙 por Elias de Araújo Ferreira Neto 👋 <p>
