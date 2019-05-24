# Exercícios para uma revisão da linguagem R 

Mesmo que você se considere um programador razoável de [**R**](https://www.r-project.org/about.html), aconselho que venha resolver a lista de exercícios apresentada adiante. É comum que venhamos esquecer de alguns conceitos da linguagem. Esses exercícios é uma oportunidade que você irá ter de revisar lógica de programação utilizando a linguagem [**R**](https://www.r-project.org/about.html) e consequentemente revisar alguns conceitos importantes da linguagem. Tente fazer esses exercícos após um olhar detalhado das [sugestões][Sugestões de passos para revisão da linguagem R] apresentadas. 

As [sugestões de revisão][Sugestões de passos para revisão da linguagem R] sugerem temas bastante simples para quem já programa  um pouco na linguagem [**R**](https://www.r-project.org/about.html). Tais sugestões aliadas com as resoluções desses exercício irão lapidar os conhecimentos necessários e fará com que você necessariamente revise outros assuntos.

**Observação**:

\BeginKnitrBlock{rmdobservation}<div class="rmdobservation"><div class=text-justify>
A google disponibilizou um [guia de estilo](https://google.github.io/styleguide/Rguide.xml) de programação em [**R**](https://www.r-project.org/about.html). Trata-se de um guia de boas práticas de programação no que diz respeito à escrita do código. Esse guia **não** trata de boas práticas de programação para a obtenção de melhorias de desempenho da linuguagem [**R**](https://www.r-project.org/about.html).
</div></div>\EndKnitrBlock{rmdobservation}


-----

## Exercícios propostos {-}

1. Responda os itens abaixo:

  - Descreva os principais tipos de dados de R.
  - Descreva os principais estruturas de dados de R.
  - Disserte sobre as diferenças entre tipos de dados e estruturas de dados.
  - Descreva quais estruturas de dados são homogêneas e quais estruturas são heterogêneas.

2. Explique o por quê das saídas abaixo:


```r
x <- c(7.1, 2.3, 3L, TRUE)
x
```

```
## [1] 7.1 2.3 3.0 1.0
```

```r
y <- c(TRUE, letters[1:3])
y
```

```
## [1] "TRUE" "a"    "b"    "c"
```

```r
z <- c(1.0, 5, 7, 0L)
z
```

```
## [1] 1 5 7 0
```

3. Sem utilizar o R, o que você espera como retorno de `x <- c(1, c(2, c(3, 4))); x`. Qual a estrutura de dados de `x`?


4. Irá ocorrer erro ao tentar criar um vetor atômico (vetor) com objetos de tipos diferentes? Como o interpretador de R trata essas situações. Explique detalhadamente.

5. O que signicica `NA`, `NaN`, `Inf` e `-Inf`, em R? Liste algumas das situações em que utilizando-se das operações básicas `+`, `-`, `*` e `/` é possível ter como retorno `NaN`.

6. Considere `vetor <- c(2, 7, 10, 8)`. Qual o tipo de dados do objeto `vetor`? Crie os objetos `vetor_int`, `vetor_character` e `vetor_logical`. (**Dica**: Crie esses objetos fazendo a conversão do objeto `vetor`).


7. O que faz o código abaixo? Explique detalhadamente o que cada função faz.

```r
objects(grep("bas", search()))
```

8. Explique passo a passo a sintaxe abaixo:

```r
search()[(grep("gr", search()))]
```

9. Forneça o código que acessa o caracter `"a"` de `l`, em que `l <- c(list(c(3, 2), "a"), c(1,2))`. Depois, converta `l` em um vetor atômico.

10. Sem correr os códigos abaixo, descreva as saídas obtidas:

  - Qual a saída esperada para os códigos c(1, FALSE), c("a", 1), c(list(1), "a"), c(TRUE, 1L)?
  
  - Por que `1 == "1"` é igual à `TRUE`?
  
  - Por que `-1 < FALSE` é igual à `TRUE`?
  
11. Considere `vetor <- 1:25`. Com no objeto `vetor`, construa uma matriz de dimensão 5x5 usando a função `matrix()` e dois utilizando a função `dim()`.

12. Crie a matriz `M`, de dimensão 50x50, com elementos de 1 à 2500 preenchidos por linha. Atribua nomes às linhas (**l_1** à **l_50**) e colunas (**c_1** à **c_50**) da matriz. (**Dica**: certamente você percebeu que não é nada interessante digitar elemento por elemento para as linhas e colunas da matriz. Tente utilizar as funções `paste()` e  `rep()`como soluções para o problema).

13. Remova os nomes das linhas e colunas da matriz `M` criada no exercício anterior.

14. Sejam `V1 <- matrix(1:12, ncol = 4, nrow = 3)` e `W1 <- matrix(1:8, ncol = 4, nrow = 2)`. Crie a matriz `M1`que é o resultado da concatenação por linha de `V1` e `W1`.

15. Considere os objetos `V2 <- matrix(1:12, ncol = 2, nrow = 4)` e `W2 <- matrix(1:12, ncol = 3, nrow = 4)`. Cria a matriz `M2`como resultados da concatenação por coluna de `V2` e `W2`.

16. Considere `obj <- list(1:3, "a" , TRUE, 1.0)`. Construa uma matriz de dimensão 2x2 a partir de `obj`.

17. Construa uma matriz de avaliações `A` a de dimensão 30x2, em que a primeira coluna são os nomes dos alunos (**Aluno_1** à **Aluno_30**) e a segunda coluna são as notas de 3 avaliações, por aluno. (**Dica**: para facilitar, gere as avaliações dos alunos de forma aleatória).

18. O que a função `dim()` retorna quando aplicada à um vetor?

19. Se `is.matrix(x)` retorna `TRUE`, o que irá retornar de `is.array(x)`?

20. Descreva os objetos objetos `x1`, `x2` e `x3`. 
    
```r
x1 <- array(1:5, c(1, 1, 5))
x2 <- array(1:5, c(1, 5, 1))
x3 <- array(1:5, c(5, 1, 1))
```

21. Considere o código código abaixo:


```r
df <- data.frame(x = 1:3, y = c("a", "b", "c"))
df$y
```

```
## [1] a b c
## Levels: a b c
```
Como podemos observar, `df$y` retorna um fator com os níveis construídos das strings que compõe a variável `y`. Como podemos alterar o comportamento do data frame `df` para que `df$y` retorne um vetor atômico do tipo character?

22. Corrija o código abaixo de modo a que venha funcionar:


```r
data.frame(x = 1:3, y = list(1:2, 1:3, 1:4))
```

```
## Error in (function (..., row.names = NULL, check.rows = FALSE, check.names = TRUE, : arguments imply differing number of rows: 2, 3, 4
```

23. Considere a lista abaixo:


```r
notas <- list(c(7.1, 3.2, NA), c(2.7, 8.8, 10.0),
              c(0.0, NA, NA), c(7.7, 8.4, 6.3),
              c(3.6, 6.6, 8.1), c(NA, NA, NA),
              c(7.4, 7.1, 7.3), c(10.0, NA, 7.0),
              c(1.6, 3.2, 5.3), c(8.8, 9.2, 8.0))
```

Responta os itens abaixo:

---

  1. Atribua nomes (**Aluno_1** à **Aluno_10**) à cada elemento de `notas`.
  
  2. Crie o vetor `status` contendo o status dos dez alunos. Considere: **A** (aprovado), **REP** (reprovado), **F** (final). (**Dica**: Construa o vetor `status` atribuindo literalmente as categorias **A**, **REP** ou **F** para cada aluno, ou seja, não é preciso criar uma função para fazer isso automaticamente. Considere **A** para os alunos com média no intervalo $[7, 10]$, **R** para os alunos com média no intervalo $[0, 4)$ e **F** para os alunos com média no intervalo $[4, 7)$).
  
  3. Crie o vetor `alunos` com os nomes dos alunos.
  
  4. Construa o data frame `historico` com as variáveis **nomes**, **notas** e **status**. 
  
  5. Com base no data frame `historico`, construa o data frame `aprovados` com os alunos aprovados. De forma análoga para os demais status. 
  
  6. Suponha que o professor está interessado em saber quais alunos foram ou tem alguma chance de assumir o status de aprovado. Construa o data frame `bons_alunos` com estes alunos.
  
  7. Modifique os nomes das linhas do data frame historico colocando **id_1** na primeira linha e respectivamente, no mesmo padrão, para as demais linhas. 
  
  8. Obtenha por meio do data frame `historico` um novo data frame (`historico_na`) com os alunos que deixaram ao menos uma prova para repor.
  
  9. Apenas para os alunos que fizeram as três avaliações, obtenha uma média aritmética das avaliações. Acrescente a variável de nome **media** no data frame `historico`.
  
---

24. Consideremos o conjunto de dados `state.x77` do pacote **datasets** (pacote padrão de R). A base  `state.x77` refere-se à uma matriz de dimensão 50x8 em que cada linha refere-se à um dos 50 estados dos EUA. Consulte as documentações para obter maiores informações.

Responda os itens abaixo:

-----

  1. Construa o data frame `dados` utilizando `state.x77`.

  2. Obtenha um data frame de nome `dados_1` com as observações de dados que possua população maior que 4246, isto é, com os estados estadunidenses que possua uma população maior que 4246 (quatro milhões duzentos e quarenta e seis mil). 
  
  3. Obtenha o data frame `dados_2` com as observações população maior que 4246 e menores que 8 milhões, isto é, menor que 8000.
  
  4. Obtenha o vetor `vetor_est` com os nomes dos estados que obedecem os critérios do item 3.
  
  5. Construa o data frame `dados_3` com os estados estadunidenses com população maior que 1.5 vezes a média dos 50 estados considerados. Obtenha o vetor com o nome dos estados que obedecem essa regra.

  6. Construa o data frame `dados_4` com os estados estadunidenses com população maior que duas vezes a mediana dos 50 estados e que tenha uma população com expectativa de vida maior que 71.84 anos.
  
  7. Obtenha o data frame `dados_5` com os estados estadunidenses com renda maior que a média nacional, expectativa de vida maior que 72 anos.
  
  8. Adicione ao data frame dados duas linhas com a média de todas as variáveis e variâncias, respectivamente.
  
-----

25. Escreva uma função que retorne o imposto pago por mulheres e por homens, sabendo que as mulheres pagam $10%$ e que os homens pagam $5%$ a mais do que as mulheres.

26. Resolva o exercício anterior utilizando a função `switch()`.

27. Escreva um programa que retorne a saída baixo:

```r
i1 = 1
i2 = 2
i3 = 3
i4 = 4
i5 = 5
i6 = 6
i7 = 7
```

**Dica**: Resolva esse simples exercício de três formas diferentes (usando `while`, `for` e `repeat`).

28. Utilizando a instrução de repetição `for` construa um pequeno programa que com base em um vetor de valores no intervalo
$[0, 1]$, some apenas os valores maiores que 0.7. **Dica**: Para economizar tempo, faça `vetor <- runif(n = 1e5, min = 0, max = 1)` para gerar o objeto `vetor`.

29. Resolva o exercício 28 sem utilizar nenhuma instrução de repetição.

30. Avalie o custo computacional dos exercícios anteriores (exercícios 28 e 29) utilizando a função `Sys.time()`. Discuta o resultado.

31. Escreva um programa em R, utilizando as instruções de loop vistas anteriormente, de modo a fornecer as seguintes estruturas, adepender do valor de `n`.


Para $n = 1$:

```
*            
```

Para $n = 2$:

```
* 
**
```

Para $n = 3$:

```
*
**
***
```
e assim por diante para outros valores de $n$. **Dica**: crie uma função `tree()` que tenha `n` como argumento.

32. Resolva o exercício anterior acrescentando mais um argumento à função `tree()` para que seja possível especificar outro caracter além de `*`. 

33. Modifique o programa da solução do exercício 31, de tal forma que a estrutura obtida seja:

Para $n = 1$:

```
A            
```

Para $n = 2$:

```
A 
BB
```

Para $n = 3$:

```
A
BB
CCC
```
e assim por diante para outros valores de $n$. **Dica**: Note que $n \leq 26$. Assim, retorne uma mensagem de advertência se um valor de $n$ inapropriado for informado. Por exemplo, utilize a função `stop()`.
