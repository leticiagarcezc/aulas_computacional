# Revisão básica da linguagem R

Mesmo que você se considere um programador razoável de [**R**](https://www.r-project.org/about.html), aconselho que venha resolver a lista de exercícios apresentada adiante. É comum que venhamos esquecer de alguns conceitos de linguagens em que programamos. Esses exercícios é uma oportunidade que você irá ter de revisar lógica de programação utilizando a linguagem [**R**](https://www.r-project.org/about.html) e consequentemente revisar alguns conceitos importantes, porém básicos, da linguagem. Tente resolver esses exercícos após um olhar detalhado das [sugestões][Sugestões de passos para revisão da linguagem R] apresentadas. 

A [lista de assuntos para revisão][Sugestões de passos para revisão da linguagem R] sugerem temas bastante simples para quem já programa  um pouco na linguagem [**R**](https://www.r-project.org/about.html). Tais sugestões aliadas com as resoluções desses exercício irão lapidar os conhecimentos necessários e fará com que você necessariamente revise outros assuntos inseridos nos exercícios. Estes assuntos/exercícios também são simples e não envolverão conceitos avançados da linguagem [**R**](https://www.r-project.org/about.html). Conceitos mais avançados serão abordados no decorrer do curso de **Estatística Computacional** e exercícios estarão disponíveis no decorrer de outros capítulos, à medida que forem necessários.



**Observação**:

\BeginKnitrBlock{rmdobservation}<div class="rmdobservation"><div class=text-justify>
A google disponibilizou um [guia de estilo](https://google.github.io/styleguide/Rguide.xml) de programação em [**R**](https://www.r-project.org/about.html). Trata-se de um guia de boas práticas de programação, no que diz respeito à escrita do código. Esse guia **não** trata de boas práticas de programação para a obtenção de melhorias de desempenho da linuguagem [**R**](https://www.r-project.org/about.html).

**Você não é obrigado adotar essas normas. Porém, segui-las tornará o seu código mais legível.**

</div></div>\EndKnitrBlock{rmdobservation}


-----

## Exercícios propostos {-}

1. Descreva o funcionamento e as diferenças de um compilador para um interpretador. Liste exemplos de linguagens de programação compiladas e interpretadas.


2. Responda os itens abaixo:



    1. Descreva os principais tipos de dados da linguagem R.
    2. Descreva as principais estruturas de dados da linguagem R.
    3. Disserte sobre as diferenças entre tipos de dados e estruturas de dados.
    4. Descreva quais estruturas de dados são homogêneas e quais estruturas são heterogêneas.</br></br>


3. Explique o por quê das saídas abaixo:

    
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

4. Sem utilizar o R, o que você espera como retorno de `x <- c(1, c(2, c(3, 4))); x`. Qual a estrutura de dados de `x`?


5. Irá ocorrer erro ao tentar criar um vetor atômico (vetor) com objetos de tipos diferentes? Como o interpretador de R trata essas situações. Explique detalhadamente.

6. O que signicica `NA`, `NaN`, `Inf` e `-Inf`, em R? Liste algumas das situações em que utilizando-se das operações básicas `+`, `-`, `*` e `/` poderemos ter `NaN` como retorno.

7. Considere `vetor <- c(2, 7, 10, 8)`. Qual o tipo de dados do objeto `vetor`? Crie os objetos `vetor_int`, `vetor_character` e `vetor_logical`. **Dica**: crie esses objetos utilizando funções para conversão dos tripos dos elementos do objeto `vetor`.


8. O que faz o código abaixo? Explique detalhadamente o que cada função faz.

    ```r
    objects(grep("bas", search()))
    ```

9. Qual o retorno do código abaixo? Explique detalhadamente o código.

    ```r
    search()[(grep("gr", search()))]
    ```

10. Forneça o código que acessa o caracter `"a"` de `l`, em que `l <- c(list(c(3, 2), "a"), c(1,2))`. Depois, converta `l` em um vetor atômico.

11. Sem executar  os códigos abaixo, descreva as saídas esperadas:

    1. Qual a saída esperada para os códigos `c(1, FALSE)`, `c("a", 1)`, `c(list(1), "a")`, `c(TRUE, 1L)`?
  
    2. Por que `1 == "1"` retornará `TRUE`? Explique.
  
    3. Por que `-1 < FALSE` retornará `TRUE`? Explique.
  
12. Considere o objeto `vetor <- 1:25`. Com o objeto `vetor`, construa uma matriz de ordem 5x5 usando a função `matrix()` e depois utilizando a função `dim()`.

13. Crie a matriz `M`, de ordem 50x50, com elementos de 1 à 2500 preenchidos por linha. Atribua nomes às linhas (**l_1** à **l_50**) e colunas (**c_1** à **c_50**) de `M`. **Dica**: certamente você percebeu que não será nada interessante digitar os nomes das linhas e colunas de `M`. Tente utilizar as funções `paste()` e  `rep()`como soluções para esse problema.

14. Remova os nomes das linhas e colunas da matriz `M` criada no exercício anterior.

15. Sejam `V1 <- matrix(1:12, ncol = 4, nrow = 3)` e `W1 <- matrix(1:8, ncol = 4, nrow = 2)`. Crie a matriz `M1`que é o resultado da concatenação, por linha, de `V1` e `W1`.

16. Considere os objetos `V2 <- matrix(1:12, ncol = 2, nrow = 4)` e `W2 <- matrix(1:12, ncol = 3, nrow = 4)`. Cria a matriz `M2`como resultados da concatenação, por coluna, de `V2` e `W2`.

17. Considere `obj <- list(1:3, "a" , TRUE, 1.0)`. Construa uma matriz de ordem 2x2 a partir de `obj`. O que de interessante você observa?

18. Construa a matriz `A` (matriz de avaliações), de ordem 30x2, em que a primeira coluna são os nomes dos alunos (**Aluno_1** à **Aluno_30**) e a segunda coluna são as notas de 3 avaliações, por aluno. **Dica**: para facilitar, gere as avaliações dos alunos de forma aleatória.

19. O que a função `dim()` retorna quando aplicada à um vetor?

20. Se `is.matrix(x)` retorna `TRUE`, o que irá retornar de `is.array(x)`? Explique.

21. Descreva os objetos objetos `x1`, `x2` e `x3` construídos na forma apresentada abaixo:
    
    ```r
    x1 <- array(1:5, c(1, 1, 5))
    x2 <- array(1:5, c(1, 5, 1))
    x3 <- array(1:5, c(5, 1, 1))
    ```

22. Considere o código apresentado abaixo:

    
    ```r
    df <- data.frame(x = 1:3, y = c("a", "b", "c"))
    df$y
    ```
    
    ```
    ## [1] a b c
    ## Levels: a b c
    ```
    Qual a estrutura de dados de `df$y`? Como poderemos alterar o comportamento do data frame `df` para que `df$y` retorne um vetor atômico com elementos do tipo **character**?

23. Ao tentar criar um data frame com o código abaixo obteremos um erro. Corrija o código:

    
    ```r
    data.frame(x = 1:3, y = list(1:2, 1:3, 1:4))
    ```
    
    ```
    ## Error in (function (..., row.names = NULL, check.rows = FALSE, check.names = TRUE, : arguments imply differing number of rows: 2, 3, 4
    ```

24. Considere a lista abaixo:

    ```r
    notas <- list(c(7.1, 3.2, NA), c(2.7, 8.8, 10.0),
                  c(0.0, NA, NA), c(7.7, 8.4, 6.3),
                  c(3.6, 6.6, 8.1), c(NA, NA, NA),
                  c(7.4, 7.1, 7.3), c(10.0, NA, 7.0),
                  c(1.6, 3.2, 5.3), c(8.8, 9.2, 8.0))
    ```

    Responta os itens abaixo:


    1. Atribua nomes (**Aluno_1** à **Aluno_10**) à cada elemento de `notas`.
  
    2. Crie o vetor `status` contendo o status dos dez alunos. Considere: **A** (aprovado), **REP** (reprovado), **F** (final). **Dica**: construa o vetor `status` atribuindo literalmente as categorias **A**, **REP** ou **F** para cada aluno, ou seja, não é preciso criar uma função para fazer isso automaticamente. Considere **A** para os alunos com média no intervalo $[7, 10]$, **R** para os alunos com média no intervalo $[0, 4)$ e **F** para os alunos com média no intervalo $[4, 7)$.
  
    3. Crie o vetor `alunos` com os nomes dos alunos. Obtenha esse vetor por meio do objeto `notas`.
  
    4. Construa o data frame `historico` com as variáveis **nomes**, **notas** e **status**. 
  
    5. Com base no data frame `historico`, construa o data frame `aprovados` com os alunos aprovados. De forma análoga, construa um data frame para cada um dos demais status, respectivamente. 
  
    6. Suponha que o professor está interessado em saber quais alunos foram ou tem alguma chance de assumir o status de aprovado. Construa o data frame `bons_alunos` com estes alunos.
  
    7. Modifique os nomes das linhas do data frame `historico` colocando **id_1** na primeira linha e respectivamente, no mesmo padrão, para as demais linhas. 
  
    8. Obtenha por meio do data frame `historico` um novo data frame (`historico_na`) com os alunos que deixaram ao menos uma prova para repor.
  
    9. Apenas para os alunos que fizeram as três avaliações, obtenha a média aritmética das avaliações. Acrescente a variável de nome **media** como última coluna do data frame `historico`.
  
25. Consideremos o conjunto de dados `state.x77` do pacote **datasets** (pacote padrão de R). A base  `state.x77` refere-se à um objeto de ordem 50x8, em que cada linha refere-se à um dos 50 estados dos EUA. Consulte a documentação (`help(state.x77)`) para obter maiores informações.

    Responda os itens abaixo:


    1. Qual a estrutura de dados do objeto `state.x77`?
    
    2. Construa o data frame `dados` utilizando `state.x77`.

    3. Obtenha o data frame de nome `dados_1` com os estados estadunidenses que possuem população maior que 4246 (quatro milhões duzentos e quarenta e seis mil). 
  
    4. Obtenha o data frame `dados_2` com os estatdos estadunidenses que possuem população maior que 4246 e menor que 8 milhões, isto é, menor que 8000.
  
    5. Obtenha o vetor `vetor_est` com os nomes dos estados que obedecem os critérios do item 3.
  
    6. Construa o data frame `dados_3` com os estados estadunidenses que possuem população maior que 1.5 vezes a média dos 50 estados considerados. Obtenha um vetor com o nome dos estados que obedecem essa restrição.

    7. Construa o data frame `dados_4` com os estados estadunidenses que possuem população maior que duas vezes a mediana dos 50 estados e que tenha uma população com expectativa de vida maior que 71.84 anos.
  
    8. Obtenha o data frame `dados_5` com os estados estadunidenses cuja população possuem renda maior que a média nacional e expectativa de vida maior que 72 anos.
  
    9. Adicione ao data frame `dados` duas linhas com as médias e variâncias de todas as variáveis, respectivamente.

26. Escreva um programa que retorne a saída baixo:

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

27. Escreva uma função que retorne o imposto pago por mulheres e por homens, sabendo que as mulheres pagam $10\%$ e que os homens pagam $5\%$ a mais do que as mulheres.

28. Resolva o exercício anterior utilizando a função `switch()`.

29. Implemente a função `tab(num, inicio, fim)` que é responsável por escrever no prompt de commando a tabuada de um número passado como argumento à `num`. **Nota**: os argumentos `inicio` e `fim` referem-se ao início e fim da tabuada, ou seja, `tab(num = 1, inicio = 7, fim = 12)` deverá escrever no prompt:

    ```
    1 x 7 = 7
    1 x 8 = 8
    1 x 9 = 9
    1 x 10 = 10
    1 x 11 = 11
    1 x 12 = 12
    
    ```
    Implemente `tab()` utilizando as diferentes escruturas de repetição da linguagem R (`for`, `while` e `repeat`).
    
    
30. Escreva a função `celtofar()` que converte um vetor de temperaturas em graus Celsius para graus Fahrenheit. Considere:

    $$F = 1.8 \times C + 32,$$
    em que $C$ é a temperatura em graus Celsius e $F$ é a temperatura em graus Fahrenheit. 

31. Melhore a função `celtofar()` para que critique valores não válidos de temperaturas.

32. Modifique a função `celtofar()` para que funcione também para conversões no sentido oposto, isto é, para que converta de graus Fahrenheit para graus Celsius.

33. Construa a função `imc()` que calcula o IMC (Índice de Massa Corporal) de uma pessoa. A função deverá retornar o IMC e um status. Observe que: 

    $$\mathrm{IMC} = \frac{\mathrm{peso}}{\mathrm{altura}^2},$$
    em que $\mathrm{peso}$ é dado em $kg$ e a $\mathrm{altura}$ é fornecida em $cm$.

    Alem disso, considere:

    -------------------------------------------------
    IMC               Status        
    ---------------   -------------------------------
    $< 17.0$          Muito abaixo do peso

    $[17.0, 18.5)$    Abaixo do peso

    $[18.5, 25.0)$    Peso normal

    $[25.0, 30.0)$    Acima do peso

    $[30.0, 35.0)$    Obesidade nível I

    $[35.0, 40.0)$    Obesidade nível II (severa)

    $\geq 40.0$       Obesidade nível III (mórbida)
    -------------------------------------------------

    **Dica**: Uma função robusta deverá tratar problema(s) com a(s) entrada(s), isto é, deverá criticar informações inconsistentes passadas como argumento.

34. Utilizando a instrução de repetição `for` construa um pequeno programa que com base em um vetor de valores no intervalo
$[0, 1]$, some apenas os valores maiores que 0.7. **Dica**: para economizar tempo, considere `vetor <- runif(n = 1e5, min = 0, max = 1)`.

35. Resolva o exercício anterior sem utilizar nenhuma instrução de repetição.

36. Avalie o custo computacional dos exercícios anteriores (exercícios 34 e 35) utilizando a função `Sys.time()`. Discuta o resultado.

37. Construa a função `central(x)` que recebe como argumeto um vetor passado à `x` e retorna algumas medidas de tendência central. A função `central()` deverá retornar:

    1. Média aritmética (média amostral): $\overline{x} = n^{-1}\sum_{i = 1}^n x_i.$
    
    2. Média geométrica: $G = (\prod_{i=1}^n x_i)^{\frac{1}{n}}.$
    
    3. Média harmônica: $H = \frac{n}{\frac{1}{x_1} + \cdots + \frac{1}{x_n}}.$

    Algumas exigências a respeito do funcionamento da função `central()` encontram-se enumeradas abaixo:
    
    1 - A função deverá retornar todas as três medidas de tendência central ou apenas uma das estatísticas, a depender do interesse do usuário.
    
    2 - Observações **Not Availables** `NA` serão eleminadas do cálculo. Porém, uma mensagem de aviso ao usuário da função deverá ser emitida informando-o a repseito do número de observações eliminadas e em quais posições encontravam-se estas observações.
    
    3 - A função deverá alertar o usuário se uma estrutura/tipo de dados não suportado por `central()` for passado como argumento à `x`. A função deverá alertar qual estrutura/tipo de dados foi passado, avinsando assim que essa estrutura/tipo de dados não poderá vir a ser processado(a). 

     **Nota**: Não utilize a vetorização da linguagem R. Nesse exercício desejamos treinar o uso das estruturas de repetições da linguagem. Não utilizar vetorização da linguagem quer dizer que você não poderá aplicar uma função à todos elementos de um vetor. Por exemplo, se `x` é um vetor, você não poderá fazer `x^2`, `sqrt(x)`, `mean(x)`, `length()`, etc. Aplique a função a cada posição do vetor utilizando estruturas de repetições. Em seus projetos reais, utilize a capacidade de vetorização da linguagem e evite o quanto der as estruturas de repetições. Isso fará com que os seus códigos sejam mais eficientes. Aqui apenas queremos exercitar o uso das estruturas de repetições. Além disso, `central()` poderá ter outros argumentos além de `x`.
    
38. Sem utilizar a capacidade de vetorização da linguagem R, nas formas do exercício anterior, implemente a função `myvar(x)` que retorna a variância amostral de um vetor passado como argumetno à `x`. 

    Algumas exigências a respeito do funcionamento da função `myvar()` encontram-se enumeradas abaixo:
    
    1 - A função deverá retornar todas as três medidas de dispersão ou apenas uma das estatísticas, a depender do interesse do usuário.
    
    2 -  Observações **Not Availables** `NA` serão eleminadas do cálculo. Porém, uma mensagem de aviso ao usuário deverá ser passada informando o número de observações eliminadas e em quais posições encontravam-se. 
    
    3 - A função deverá alertar o usuário se uma estrutura ou tipo de dados não coerente com o interesse da função for passado como argumento à `x`.

     **Nota**: Não utilize a vetorização da linguagem R. Nesse exercício desejamos treinar o uso das estruturas de repetições da linguagem. Não utilizar vetorização da linguagem quer dizer que você não poderá aplicar uma função à todos elementos de um vetor. Por exemplo, se `x` é um vetor, você não poderá fazer `x^2`, `sqrt(x)`, `mean(x)`, `length()`, etc. Aplique a função a cada posição do vetor utilizando estruturas de repetições. Em seus projetos reais, utilize a capacidade de vetorização da linguagem e evite o quanto der as estruturas de repetições. Isso fará com que os seus códigos sejam mais eficientes. Aqui apenas queremos exercitar o uso das estruturas de repetições. Além disso, `myvar()` poderá ter outros argumentos além de `x`.

39. Se `x`, na função `myvar()`, for um vetor não numérico? E se `x` for um vetor de caracteres numéricos? E se `x` for uma string numérica como `"1,2,3"` que desejamos tratar como sendo o `c(1, 2, 3)`? Modifique a função `myvar()` para que venham tratar/considerar essas situações. 

40. Implemente a função `disp(x)` que deverá retornar uma das medidas de dispersão listadas logo abaixo:

    - Amplitude: $A = x_{\mathrm{max}} - x_{\mathrm{min}}.$
    - Variância amostral: $S^2 = \frac{\sum_{i=1}^{n}(x_i - \overline{x})^2}{n-1}.$
    - Desvio padrão amostral: $S = \sqrt{S^2}.$
    - Coeficiente de variação: $CV = \frac{100 \times S}{\overline{x}}.$
    
    Algumas exigências a respeito do funcionamento da função `disp()` encontram-se enumeradas abaixo:
    
     1 - A função deverá retornar todas as quatro estatísticas ou apenas uma das estatísticas, a depender do interesse do usuário.
     
     2 - Observações **Not Availables** `NA` serão eleminadas do cálculo. Porém, uma mensagem de aviso ao usuário deverá ser passada informando o número de observações eliminadas e em quais posições encontravam-se. 
     
     3 - A função deverá alertar o usuário se uma estrutura ou tipo de dados não coerente com o interesse da função for passado como argumento à `x`.
     
     **Nota**: Não utilize a vetorização da linguagem. Nesse momento também desejamos treinar o uso das estruturas de repetições da linguagem.

41. Implemente a função `mycor(x, y, pearson = TRUE, rm.na = TRUE)` que deverá receber como argumentos dois vetores passados para `x` e `y`, respectivamente. A função `mycor()` deverá retornar o coeficiente de [correlação de Pearson](https://pt.wikipedia.org/wiki/Coeficiente_de_correla%C3%A7%C3%A3o_de_Pearson) se `pearson = TRUE`, caso contrário, retornará o coeficiente de [correlação de Spearman](https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient). Além disso, se `rm.na = TRUE`, a função `mycor()` deverá eliminar os **Not Availables** `NA` dos respectivos vetores. Por exemplo, se `x <- c(1, 8, -1, NA, NA)` e `y <- c(NA, 7, -2, 10, 5)` forem passados para `mycor()`, esta deverá eliminará as duas últimas observações de `x` e `y`, bem como a primeira observação de `x` e `y`, resultando, nesse exemplo, em `x <- c(8, -1)` e `y <- c(7, -2)`, respectivamente. A função deverá alertar a respeito das eliminações e informar quais as posições eliminadas dos vetores.
    
    Algumas outras exigências a respeito do funcionamento da função `mycor()` encontram-se enumeradas abaixo:
    
      1 - A função deverá parar e alertar o usuário nas situações em que os vetores não tenham os mesmos comprimentos.
      
      2 - A função deverá retornar dois objetos, `rho` e `level`, em que `rho` ($\rho$) é o valor da correlação e `level` informa o nível dessa correlação. Os níveis possível a ser retornados são: **desprezível** se $\rho \in [0, 0.3)$, **fraca** se $\rho \in [0.3, 0.5)$, **moderada** se $\rho \in [0.5, 0.7)$, **forte** se $\rho \in [0.7, 0.9)$ e **fortíssima** se $\rho \in [0.9, 1]$. 

    **Dica**: A função `warning()` pode ser útil para emitir uma mensagem de aviso (alerta) ao usuário da função `mycor()`.

42. Construa duas funções, `tree1()` e `tree2()`, que escrevam, no prompt de comando, as imagens abaixo, respectivamente. O programa deverá utilizar instruções de repetições para resolver o problema.

    **A primeira função deverá imprimir**:

    ```
    **********
    *********
    ********
    *******
    ******
    *****
    ****
    ***
    **
    *
    ```

    **A segunda função deverá imprimir**: 

    ```
    *-*-*-*-*-
    *-*-*-*-*
    *-*-*-*-
    *-*-*-*
    *-*-*-
    *-*-*
    *-*-
    *-*
    *-
    *
    ```
    Implemente as funções utilizando as estruturas de repetições `for`, `while` e `repeat`.
    
43. Escreva a função `tree3()`, utilizando instruções de repetições, de modo a fornecer as seguintes estruturas, adepender do valor de `n`.


    Para $n = 1$:

        
        *            
        

    Para $n = 2$:

        
        * 
        **
        

    Para $n = 3$:

        
        *
        **
        ***
        
    e assim por diante para outros valores de $n$. Implemente `tree3()` utilizando as estruturas de repetições `for`, `while` e `repeat`.

44. Melhore as funções `tree1()`, `tree2()` e `tree3()` de modo que estas possam considerar caracteres distintos e não somento o caracter asterisco.

45. Modifique a função `tree1()`, de tal forma que a estrutura obtida seja:

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
    e assim por diante para outros valores de $n$. **Dica**: Note que $n \leq 26$. Assim, retorne uma mensagem de advertência se um valor de $n$ inapropriado for informado. **Dica**: utilize a função `stop()`.

46. Implemente a função `aprox_e()` que retorna uma aproximação para $\mathrm{e}^x$, em que:

    $$\mathrm{e}^x = \sum_{n = 0}^{\infty} \frac{x^n}{n!}.$$
    **Dica**: A função `aprox_e()` deverá receber como argumento o número de somas a serem consideradas.

47. Crie a função `aprox_pi()`, fazendo uso de instruções de repetição, que forneça uma aproximação para o valor da constante $\pi$. Essa aproximação deverá considerar:

    $$\pi = 4 - \frac{4}{3} + \frac{4}{5} - \frac{4}{7} + \frac{4}{9} - \frac{4}{11} + \dots$$

    **Dica**: Premita que o usuário de sua função forneça a quantidade de termos a serem somados. Além disso, faça com que sua função critique valores indevidos para a quantidade de termos somados. 

48. Implemente a função `fib()`, utilizando instruções de repetição, que retorna o Fibonacci de um número. Lembre-se, a sequência de Fibonacci é dada por $1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, \ldots$ . Note que Fibonacci de $n$ é dado por $F_n = F_{n-1} + F_{n-2},\, n > 2$, com $F_1 = 1$ e $F_2 = 1$. Por exemplo, Fibonacci de 5 é dado por $F_5 = F_{4} + F_{3} = 3 + 2 = 5$.

49. Implemente o exercício anterior usando funções recursivas. **Lembre-se**: chamamos de funções recursivas as funçãos que chamam a si mesma.

    **Um esboço de função recursiva**:

    ```r
    func_f <- function(...){
        
       # Ué? ...
       # Sim! Estamos chamando a função que estamos criando. ;)
       func_f(...)
        
       # Será preciso parar em algum momento
       # somos finitos :)
       if (contition) break 
    }
    ```

50. Implemente a função `aprox_pi()` de forma recursiva.

51. Implemente a função `nachange(df)`, em que `df` recebe um data frame/matriz. A função `nachange()` deverá trocar `NA` pelo character "?". **Dica**: Em caso de `df` não possuir nenhum elemento `NA`, a função `nachange()` deverá retornar o objeto passado à `df`. 

52. Construa a função `searchindf(df, value)`, em que `df` é um data frame/matriz e `value` é um vetor de uma única posição. A função `searchindf()`deverá retorna **TRUE** se o valor passado para `value` é encontrado em alguma posição do data frame/matriz passado(a) para `df` e **FALSE** caso contrário. **Dica**: tente construir a função da forma mais robusta possível. Por exemplo, considere criticar os argumentos, caso estes não tenham a estrutura de dados adequada ao objetivo da função.

53. Construa a função `namecolsort(df)`, em que `df` receberá como argumento um(a) data frame/matriz. A função `namecolsort()` deverá retorna o(a) data frame/matriz com as colunas ordenadas. **Dica**: ordene as colunas considerando o primeiro caracter que compõe o nome da coluna (variável).
    
54. Escreva a função `exclusive(df)`, em que `df` receberá como argumento um(a) data frame/matriz. A função `exclusive()` deverá retornar a posição das linhas exclusivas, ou seja, as linhas que não possuem elementos repetidos.

55. Escreva uma função `extremeindex(df, max = NULL)`, em que `df` receberá como primeiro argumento um(a) data frame/matriz. A função `maxindex()` deverá retornar a posição (linha, coluna) do valor máximo contido no objeto passado para `df`, caso `max = TRUE`. Em caso de `max = FALSE`,  a função `maxindex()` deverá retornar a posição (linha, coluna) do valor mínimo contido no objeto passado à `df`. Para o caso de `max = NULL` (caso padrão), a função `maxindex()` deverá retornar uma matriz de ordem 2x2, em que cada linha deverá retornar a posição do elemento mínimo e máximo, respectivamente, contidos no objeto passado à `df`.

56. Implemente a função `myt(df)`, em que `df`recebe como argumento um(a) data frame/matriz. A função `myt()` deverá "girar", em 90 graus, a(o) matriz/data frame passado à `df`. **Dica**: não utilize a função `t()` para transpor a matriz.

57. Crie a função `anagram(x, y)` que recebe dois argumentos (duas strings). A função `anagram()` deverá retornar **TRUE** se uma palavra (string) é anagrama da outra e **FALSE** em situação contrária. A função deverá considerar que ambas as strings possuem a mesma quantidade de caracteres. Caso a quantidade de caracteres não seja igual, em ambas as strings, a função deverá parar e advertir o usuário. **Dica**: você poderá utilizar a função `strsplit()`. 

58. Implemente a função `strposition(x)`, em que dado uma palavra (string) fromada por letras do alfabeto Romano e passada como argumento para `x`, retorna a posição das letras em um vetor. Por exemplo, a string (palavra) **cada** passada para a função fará com que `strposition()` retorne o vetor formados pelos elementos 3, 1, 4 e 1. **Dica**: a função **não** poderá aceitar strings que são formadas por pelo menos um caracter que não seja uma letra do alfabeto Romano.

59. Altere a função `strposition(x)` para que em situação da string (palavra) possuir um ou mais caracteres não pertencentes ao alfabeto Romano, o retono seja `NA`, nas respectivas posições destes caracteres.
