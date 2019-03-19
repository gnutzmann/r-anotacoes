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

> Instala os pacotes passados como parâmetros

## Sintaxe 

`install.packages(pacote,pacote,..., dependencies = TRUE|FALSE)`

## Exemplo

`install.packages("ggplot2", dependencies = TRUE)`

Instala o pacote ggplot2 com todas suas dependências devido a passagem o parametro dependencies = TRUE.

---

# function **`remove.packages()`**

> Remove os pacotes passados como parâmetros

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

> Carrega para o uso os pacotes passados como parâmetros

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

# **CONVERSÃO DE TIPOS DE DADOS**

> Converter um tipo em outro 

## Sintaxe
`as.tipo-dado(dados)`

## Exemplo

`n1 = "10";` <br>
`class(n1);` # Retorna character  <br>
`n1 = as.numeric(n1)` <br>
`class(n1);` # Retorna numeric <br>

    Pode-se utilizar com outros tipo como data.frame, list, integer.

---

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

---

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

---

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

---

# **DATA FRAME**

> Data frames se assemelham a tabelas, ou seja, podem trazer dados de tipos diferentes em suas colunas.

* Criando um data frame
    * `id = c(1,2,3)`
    * `nome = c("Diogo","Maria","João")`
    * `idade = c(39L,25L,53L)`
    * `cadastro_ativo = c(T,T,F)`
    * `limite_credito = c(5000.00,10550.50,0)` 
    * `clientes = data.frame(id,nome,idade,cadastro_ativo,limite_credito)`
* Verificando o tipo de uma coluna do data frame
    * `class(clientes$idade)`
* Alterando os dados de um data frame via R Editor
    * `fix(clientes)`
* Abrindo o R Editor para alterar os dados do data frame e atribuindo o resultado alterado à outra variável
    * `clientes_edit = edit(clientes)`

--- 

# **SÉRIE TEMPORAL**

> Coleção de observações feitas sequencialmente ao longo do tempo

* Criando uma série temporal
    * `serie_temp = ts(c(1:60), start=c(2010,1), end=c(2014,12), frequency = 12 )`

--- 

# **FATOR**

> Fatores são vetores de elementos numerados.

* Criando um fator de meses do ano
    * ` meses = factor(c(1:12), labels = c('jan','fev','mar','abr','mai','jun','jul','ago','set','out','nov','dez'), ordered = TRUE)`

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

# **function `c()`**

> combina os valores passados como parâmetros em um vetor ou lista

## Sintaxe

`c(....)`

## Exemplo

`c(1,10,15,20,25)`

Gera um vetor [1,10,15,20,25]

`c(T,F,T,T,F)`

Gera um vetor [TRUE,FALSE,TRUE,TRUE,FALSE]

`c(1:100)`

Gera um vetor com número de 1 a 100

---

# **function `seq()`**

> Gera um vetor com um sequencia de valores.

## Sintaxe

`seq(from=num-ini,to=num-fim,by=intervalo)`

## Exemplo

s1 = seq(from=1, to=1000, by=10)

Gera um vetor com numeros sequenciais de 1 a 1000 em intervalos de 10 ([10,20,30,40,....,1000])

--- 

# **function `scan()`**

> Abre um prompt para digitação de valores que irão compor um vetor

## Sintaxe

`scan()`

## Exemplo

`v1 = scan()`

Abre um prompt para digitar valores do tipo numeric que irão compor v1.

`v2 = scan(what="character")`

Abre um prompt para digitar valores do tipo character que irão compor o v2.

---

# **function `sample()`**

> Gera uma amostra de dados aleatórios baseados nos parâmetros informados

## Sintaxe 

`sample(x, size, replace = FALSE, prob = NULL)`

## Exemplo

`sample(c(0,1), 10, replace = TRUE, prob = c(0.5,0.5))`

Gera um vetor (amostra) de tamanho 10 contendo valores 0,1 aleatorios cuja probabilidade de ocorrer 0 é de 50% e 1 também de 50% e os dados não podem se repetir

    set.seed(numero) gera uma seed de geração de números aleatórios fixa, passada como parâmetro.

----

# **functions `attach(), detach() e with()`**

> **attach** coloca um conjunto de dados (data frame, list...) no "search path" do R e **detach** retira. Já o **with** utiliza o conjunto de dados passsado como primeira parametro para as expressões passadas no parametro seguinte.

## Sintaxe

- `attach(conj-dados)`
- `detach(conj-dados)`
- `with(conj-dados,expressao)`

## Exemplo

`attach(cars);` # Adiciona cars no search path <br>
`mean(speed);` # utiliza a coluna speed sem precisar declarar cars$speed <br>
`detach(cars);` # Retira do search path. <br>
`with(cars,mean(speed))` # Utiliza cars na expressão mean(speed)<br>

---

# **IMPORTANTO ARQUIVOS**

## Sintaxe
`read.table(arquivo,sep = char-separador,dec = "separador-decimal",header = T|F)`

## Exemplo

 `tab = read.table("arquivo.csv",sep = ";",dec = ".",header = T)`

Importa o arquivo de nome "arquivo.csv com separador de campos sendo ponto e virgula, usando ponto como separador decimal e considerando a primeira linha como cabeçalho

`tab = read.table(file.choose(),sep = ";",dec = ".",header = T)`

Executa a mesma tarefa do exemplo anterior porem utiliza a função file.choose() para abrir uma caixa de dialogo para seleção do arquivo.

---

# **SALVANDO ARQUIVO NO FORMATO RDATA**

# Sintaxe
`save(dados,file="nome-arquivo.rdata")`

# Exemplo

`v1 = seq(from=1,to=1000,by=5)`
`save(v1, file="vetor.rdata")`

Salva o vetor gerado em um arquivo no formato binário.

---

# **CARREGANDO ARQUIVOS NO FORMATO RDATA**

## Sintaxe

`load(nome-arquivo)`

## Exemplo

`load("vetor.rdata")`

Carrega os dados do arquivo passado como parametro.

---

# **function `list.files()`**

> Lista os arquivos e pastas de um diretório

## Sintaxe 
`list.files()`

## Exemplo 

`list.files()`

Lista os arquivos do diretório de trabalho

`list.files("/home/user/")`

Lista os arquivos do diretório /home/user/

---

# **function `head() e tail()`**

> Respectivamente mostram as primeiras e as ultimas linha de um conjunto de dados

## Sintaxe
`head(dados)`
`tail(dados)`

# Exemplo
`head(t1)` # Retorna as primeiras linha de t1 <br>
`tail(data1,n=4L)` # Retorna as últimas 4 linhas de data1 <br>

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

# **function `colnames() e rownames()`**

> Retornam, respectivamente, o nome das colunas e das linhas de um conjunto de dados

## Sintaxe 

`colnames(dados)`
`rownames(dados)`

## Exemplo

`colnames(iris)` # Retorna o nome das colunas de iris <br>
`rownames(iris)` # Retorna o nome das linhas de iris <br>

---

# **function `mean()`**

> Retorna a média de um conjunto de valores.

## Sintaxe 

`mean(dados)`

## Exemplo

`mean(c(1,2,3,4))`

Retorna a média dos valores passados como parâmetros

----

# **function `sd()`**

> Retorna o desvio padrão de um conjunto de valores.

## Sintaxe 

`sd(dados)`

## Exemplo

`sd(c(1,2,3,4))`

Retorna o desvio padrão do conjunto de valores passados como parâmetros

----

# **function `var()`**

> Retorna o variância de um conjunto de valores.

## Sintaxe 

`var(dados)`

## Exemplo

`var(c(1,2,3,4))`

Retorna o desvio padrão do conjunto de valores passados como parâmetros

----

# **function `rnorm()`**

> Gera uma distribuição normal baseada nos parâmetros passados. 

## Sintaxe 

`rnorm(qtde-valores, mean = media, sd = desvio-padrao)`

## Exemplo

`rnorm(10, mean = 20, sd = 3)`

Gera uma distribuição normal com 10 valores cuja média é 20 e o desvio padrão é 3.

----

# **function `rpois()`**

> Gera uma distribuição de Poisson baseada nos parâmetros passados. 

## Sintaxe 

`rpois(qtde-valores,lambda=valor)`

## Exemplo

`rpois(10, lambda=4)`

Gera uma distribuição de Poisson com 10 valores cuja lambda é 4.

----

# **function `rbinom()`**

> Gera uma distribuição binomial baseada nos parâmetros passados. 

## Sintaxe 

`rbinom(dados,size=tamanho, prob=probabilidade)`

## Exemplo

`rpois(10, lambda=4)`

Gera uma distribuição binomial.

----

# **function `shapiro.test()`**

> Verifica se um conjunto de dados de uma dada variável aleatória é uma distribuição normal.

## Sintaxe 

`shapiro.test(dados)`

## Exemplo

`shapiro.test(rnorm(10, mean = 20, sd = 3))`

Verifica se o resultado da função rnorm retornou uma distribuição normal.

----

# **function `cor()`**

> Verifica se existe uma correlação entre os valores passados como parâmetros. Retorna um valor entre -1 e 1 para indicar a correlação. 

## Sintaxe 

`cor(dados1,dados2)`

## Exemplo

`cor(women$height,women$weight)`

Verifica se existe uma correlação entre os valores de women$height e women$weight

---

# **function `lm()`**

> Retorna um modelo de regressão linear.

## Sintaxe 

`lm(formula-modelo)`

## Exemplo

`lm(women$height ~ women$weight)`

Gera um modelo de regressão linear de women$height e women$weight

---

# **function `cumsum(), cumprod(), cummax(), cummin()`**

> Retorna os valores acumulados somados, o produto, máximo ou mínimo respectivamente.

## Sintaxe 
`cumsum(x)`
`cumprod(x)`
`cummax(x)`
`cummin(x)`

## Exemplo

`cumsum(c(1,2,3,4))` # retorna [1,3,6,10] <br>

Retorna cumulativamente somadas do vetor passado.

----

# **function `apply()`**

> Aplica, linha a linha ou coluna a coluna um função passada como parametro em um conjunto de dados. 

## Sintaxe 

`apply(dados,1|2|nome-coluna|nome-linha,funcao)`

## Exemplo

`apply(USPersonalExpenditure,1,median)` # Retorna média das linhas <br> 
`apply(USPersonalExpenditure,2,median)` # Retorna média das colunas <br> 
`apply(USPersonalExpenditure,2,sum)` # Retorna somatório das colunas <br> 
`apply(USPersonalExpenditure,1,sum)` # Retorna somatório das linhas <br> 

----

# **function `table()`**

> Cria uma tabela de contingência baseada nos colunas passadas como parâmetros.

## Sintaxe 

`table(col1,col2)`

## Exemplo

`table(infert$education,infert$induced)`

Retorna os dados tabulados das colunas indicadas.

----