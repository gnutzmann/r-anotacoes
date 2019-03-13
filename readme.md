# function `dim()`

> Retorna ou seta as dimensões de um objeto

## Sintaxe
`dim(x)`

## Exemplo
`x = 1:12; dim(x) = c(3,4); dim(x);` 

X recebe 12 valores aleatorios de 1 a 12, em seguida transforma-se esse vetor em uma matriz de 3 linha e 4 colunas. Por fim retorna o as dimensões da matriz gerada.

---

# function `c()`

> combina os valores passados como parametros em um vetor ou lista

## Sintaxe

`c(....)`

## Exemplo

`c(1,10,15,20,25)`

Gera um vetor [1,10,15,20,25]

---

# function `sample()`

> Gera uma amostra de dados baseados nos parametros informados

## Sintaxe 
`sample(x, size, replace = FALSE, prob = NULL)`

## Exemplo

`sample(c(0,1), 10, replace = TRUE, prob = c(0.5,0.5))`

Gera um vetor (amostra) de tamanho 10 contendo valores 0,1 aleatorios cuja probabilidade de ocorrer 0 é de 50% e 1 também de 50%

----
