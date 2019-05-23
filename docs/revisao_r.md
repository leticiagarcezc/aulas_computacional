# Exercícios para uma revisão da linguagem R 

Mesmo que você se considere um programador razoável de [**R**](https://www.r-project.org/about.html), aconselho que venha resolver a lista de exercícios apresentada adiante. É comum que venhamos esquecer de alguns conceitos da linguagem. Esses exercícios é uma oportunidade que você irá ter de revisar lógica de programação utilizando a linguagem [**R**](https://www.r-project.org/about.html) e consequentemente revisar alguns conceitos importantes da linguagem. Tente fazer esses exercícos após um olhar detalhado das [sugestões][Sugestões de passos para revisão da linguagem R] apresentadas. 

As [sugestões de revisão][Sugestões de passos para revisão da linguagem R] sugerem temas bastante simples para quem já programa  um pouco na linguagem [**R**](https://www.r-project.org/about.html). Tais sugestões aliadas com as resoluções desses exercício irá lapidar os conhecimentos necessários e fará com que você necessariamente revise outros conceitos.

**Observação**:

\BeginKnitrBlock{rmdobservation}<div class="rmdobservation"><div class=text-justify>
A google disponibilizou um [guia de estilo](https://google.github.io/styleguide/Rguide.xml) de programação em [**R**](https://www.r-project.org/about.html). Trata-se de um guia de boas práticas de programação no que diz respeito à escrita do código. Esse guia **não** trata de boas práticas de programação para a obtenção de melhorias de desempenho da linuguagem [**R**](https://www.r-project.org/about.html).
</div></div>\EndKnitrBlock{rmdobservation}

## Exercícios propostos {-}

-----

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

3. Sem utilizar o R, o que você espera como retorno de `c(1, c(2, c(3, 4)))`?


4. O que signicica `NA`, `NaN`, `Inf` e `-Inf`? Liste algumas das situações em que utilizando-se das operações básicas `+`, `-`, `*` e `/` é possível ter como retorno `NaN`.

5. 


-----
