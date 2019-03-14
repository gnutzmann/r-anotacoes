# function **`help.start()`**

> Abre o indice da documentação da linguagem

## Sintaxe 

`help.start()`

## Exemplo

`help.start()`

Abre o indice da documentação da linguagem

---
# function **`help()`**

> Retorna a documentação do termo passado como parametro 

## Sintaxe 

`help("termo")`

## Exemplo

`help("search")`

Retorna a documentação da função search.

    Utilize o caracter "?" como forma abreviada do comando help() Ex.: ?search

---

# **function  `apropos()`**

> Retorna os termos que contém a palavra digitada

## Sintaxe

`apropos(palavra)`

## Exemplo

`apropos("sear")`

Retorna todos os termos que contém "sear"

---

# **function  `args()`**

> Retorna a assinatura da função passada como parametro, ou seja a lista de argumentos

## Sintaxe

`args("funcao")`

## Exemplo

`getwd("sd")`

Retorna a lista de argumentos da função "sd"

    Ao digitar somente o nome da função, ou seja sem os (), é retornado o código fonte em C da mesma.

---

# **function  `getwd()`**

> Retorna o diretório de trabalho atual

## Sintaxe

`getwd()`

## Exemplo

`getwd()`

Retorna o diretório de trabalho atual

---

# **function `setwd()`**

> Seta um diretório de trabalho passado como parametro

## Sintaxe

`setwd(path)`

## Exemplo

`setwd("/home/diogo/work/R")`

Seta o diretório de trabalhado para a caminho "/home/diogo/work/R"

---

# **function  `dir()`**

> Retorna a lista de arquivos do diretório padrão

## Sintaxe

`dir()`

## Exemplo

`dir()`

Retorna a lista de arquivos do diretório padrão

---

# **function  `save.image()`**

> Salva os estado da sessão de trabalho

## Sintaxe

`save.image("nome-do-arquivo")`

## Exemplo

`save.image("projeto-teste.RData")`

Grava no arquivo "projeto-teste.RData" o estado atual da sessão de trabalho.

---

# **function  `load()`**

> Carrega a sessão de trabalho salva no arquivo passado como parametro

## Sintaxe

`load(file="nome-do-arquivo")`

## Exemplo

`load(file="projeto-teste.RData")`

Carrega o arquivo "projeto-teste.RData".

---

# function **`install.packages()`**

> Instala os pacotes passados como parametros

## Sintaxe 

`install.packages(pacote,pacote,..., dependencies = TRUE|FALSE)`

## Exemplo

`install.packages("ggplot2", dependencies = TRUE)`

Instala o pacote ggplot2 com todas suas dependências devido a passagem o parametro dependencies = TRUE.

---

# function **`remove.packages()`**

> Remove os pacotes passados como parametros

## Sintaxe 

`remove.packages(pacote,pacote,...)`

## Exemplo

`remove.packages("ggplot2")`

Remove o pacote ggplot2. 

---

# function **`installed.packages()`**

> Retornar todos pacotes instalados na máquina

## Sintaxe 

`installed.packages()`

## Exemplo

`installed.packages()`

Retorna os pacotes instalados

---

# function **`library()`**

> Carrega para o uso os pacotes passados como parametros

## Sintaxe

`libray(pacote)`

## Exemplo

`library(ggplot2)`

Carrega para o uso o pacote ggplot2

---

# function **`detach()`**

> Descarrega da memória o pacote passado como parametro

## Sintaxe

`detach("package:nome-do-pacote")`

## Exemplo

`detach("package:ggplot2")`

Descarrega da memória o pacote ggplot2

---

# function **`search()`**

> Mostra todos pacotes carregados na memória

## Sintaxe 

`search()`

## Exemplo

`search()`

Mostra os pacotes carregados.

---

# functions `getOption() e setOption`

> Cada função retorna o valor de uma configuração passada como parametro e seta um configuração respectivamente

## Sintaxe

`getOption("opcao") e setOption("opcao")`

## Exemplo

`getOption("OutDec") e setOption(OutDec=",")`

Retorna o separador decimal e seta o separador decimal respectivamente.

### Lista de configurações

* **OutDec** => Separdor decimal
* **defaultPackages** => Retorna os pacotes padrões carregados na memória

Importante:

    A `help("options")` retorna a lista completa de opções de confiração na documentação

----

# **TIPOS DE DADOS**

* Caracter
* Numérico
* Inteiro
* Fator
* Data    

    **NA** representa o valor não disponível, ou seja, **NOT AVALIABLE**

## Variáveis 

    No R toda variável é tratada como um vetor. Ex.: a = 10 é um vetor com uma posição númerica.

### Simbolos de atribuição de valores 

* =
    * `a = 10`    
* ->
    * `a -> 10`    
* <-
    * `10 <- a`    

### Verificando o tipo das variáveis

`class(variavel)`

### Verificando o tipo pai das variáveis

`typeof(variavel)`

### Teste de tipos de dados

`is.numeric(variavel)`
`is.character(variavel)`
`is.integer(variavel)`

### Definir tipo de dados implicitamente

### Tipo inteiro (integer)

`idade = 35L`
ou
`idade = as.integer(35)`

    O "as" pode ser usado com outros tipos.

---

# **Manipulação de dados do tipo data (Date)**

> Para criar uma variavel com conteúdo do tipo Date é necessário passar em formato de caracter e converter para date.

## Exemplo

`data = as.Date("1979-07-10")`

> Para saber a diferença entre duas datas basta fazer um subtração entre os dois valores.

## Exemplo

`nasc = as.Date("1979-07-10"); hoje = Sys.Date(); dif = hoje - nasc;dif;`

O resultado é **"Time difference of 14491 days"**

## Formatação de tipos data

## Sintaxe

`format(data,format="mascara")`

## Exemplo

`format(data,format="%d/%m/%Y")`

Retorna o formato d/mm/aaaa

`format(Sys.time(),format="%d/%m/%Y %H:%M:%S")`

Retorna a data e hora atual no formato especificado.

---

# **function `paste()`**

> Concatena duas ou mais strings 

## Sintaxe 

`paste(string1, string2, stringN, sep="separador")`

## Exemplo

`frase = paste("O cachorro","latiu",sep=" ")`

Retorna "O cachorro latiu" para a variavel "frase".

---

# **function `objects()`**

> Lista todas variáveis em memória

## Sintaxe

`objects()`

## Exemplo

`objects()`

Retorna a lista de objetos na memória

---

# **function `rm()`**

> Remove objetos da memória

## Sintaxe

`rm(variavel)`

## Exemplo

`rm(list=objects())`

Remove todo objetos da memória

---

# **function `data()`**

> Retorna todos grupos de dados carregados no R

## Sintaxe

`data()`

## Exemplo

`data()`
`data(package = .packages(all.avaliable=TRUE))`

Retorna lista de grupos de dados instalados

---


# **function `dim()`**

> Retorna ou seta as dimensões de uma matriz

## Sintaxe

`dim(x)`

## Exemplo

`x = 1:12; dim(x) = c(3,4); dim(x);` 

X recebe 12 valores aleatorios de 1 a 12, em seguida transforma-se esse vetor em uma matriz de 3 linha e 4 colunas. Por fim retorna o as dimensões da matriz gerada.

---

# **function `summary()`**

> Sumariza um objeto passado como argumento

## Sintaxe 

`summary(object)`

## Exemplo

`summary(iris)`

Retorna um sumário de informações sobre a base de dados que acompanha a linguagem R denominada "iris".

---

# **function `c()`**

> combina os valores passados como parametros em um vetor ou lista

## Sintaxe

`c(....)`

## Exemplo

`c(1,10,15,20,25)`

Gera um vetor [1,10,15,20,25]

`c(T,F,T,T,F)`

Gera um vetor [TRUE,FALSE,TRUE,TRUE,FALSE]

---

# **function `sample()`**

> Gera uma amostra de dados baseados nos parametros informados

## Sintaxe 

`sample(x, size, replace = FALSE, prob = NULL)`

## Exemplo

`sample(c(0,1), 10, replace = TRUE, prob = c(0.5,0.5))`

Gera um vetor (amostra) de tamanho 10 contendo valores 0,1 aleatorios cuja probabilidade de ocorrer 0 é de 50% e 1 também de 50%

----

# **VETORES**

* Criando um vetor
    * `vet = c(1,2,3,4,5,6)`
* Ordenando um vetor
    * `sort(vet)`
* Retornando o maior e menor valor de um vetor
    * `max(vet);min(vet)`
* Filtrando dados do vetor
    * `vet[vet>3]` 
* Mostrando a ordem dos valores no vetor
    * `order(vet)`
* Somando os valores de dois vetores
    * `vet + vet`
* Somando um valor a cada item do vetor
    * `vet = vet + 5`
* Retornando o tamanho do vetor
    * `length(vet)`
* Alterando o tamanho do vetor                
    * `length(vet) = 12`
* Alterando valores em um indice especifico do vetor 
    * `vet[c(11,12)] = c(6,6)`

# **MATRIZES**

* Criando uma matriz com dados distribuidos por linha (byrow=T)
    * `matr = matrix(c(1,2,3,4,5,6), nrow=2,ncol=3,byrow=T)`
* Criando uma matriz com dados distribuidos por coluna (byrow=F)
    * `matr = matrix(c(1,2,3,4,5,6), nrow=2,ncol=3,byrow=F)`
* Nomeando as linhas e colunas de uma matriz
    * `dimanmes(matr) = list(c("L1","L2","L3"),c("C1","C2","C3"))`
* Alterando um valor especifico da matriz
    * `matr[1,2] = 0`
* Retornando dimensões da matriz
    * `dim(matr)`

# **LISTAS**

> Lista são conjuntos de objetos de classe que podem ser diferentes, por exemplo matrizes, vetores e outras listas.

* Criando uma lista
    * `lista = list(USPersonalExpenditure, ability.cov$center, c(1,2,3,4,5), "Frase frase")` 
* Colocando nome nos objetos de um lista de 4 itens
    * `names(lista) = c("Matriz","VetZero","Vet12345","Texto")`        
* Acessando o segundo objeto da lista
    * `lista[[2]]`
* Forma alternativa caso os itens da lista estejam nomeados
    * `lista$nome-item`         