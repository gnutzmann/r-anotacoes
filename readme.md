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

# **function `dim()`**

> Retorna ou seta as dimensões de um objeto

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

---

# **function `sample()`**

> Gera uma amostra de dados baseados nos parametros informados

## Sintaxe 

`sample(x, size, replace = FALSE, prob = NULL)`

## Exemplo

`sample(c(0,1), 10, replace = TRUE, prob = c(0.5,0.5))`

Gera um vetor (amostra) de tamanho 10 contendo valores 0,1 aleatorios cuja probabilidade de ocorrer 0 é de 50% e 1 também de 50%

----
