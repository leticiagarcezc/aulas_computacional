# Prefácio {-}


Esse material sempre tentará se adequar à ementa da disciplina de Estatística Computacional, sendo esta uma disciplina obrigatória do curso de bacharelado em estatística do Departamento de Estatística da UFPB. Dessa forma, trata-se de um material destinado à alunos do Departamento de Estatística da UFPB. Porém, esse material poderá vir a despertar interesse à outras pessoas que não alunos da instituição.

A ementa do curso de **Estatística Computacional** que compõe a estrutura do curso como disciplina obrigatória poderá ser obtida no [**link**](http://www.de.ufpb.br/graduacao/obrigatorias/EstatisticaComputacional.pdf). Como pode-se observar, a disciplina é dividida no uso de tecnologias (linguagem de marcação e linguagem de programação) e alguns aspectos teóricos que envolvem a teoria da estatística computacional. O bom uso dos conceitos abordados no curso estará alinhado ao perfeito entendimento das tecnologias e teorias apresentadas.


\BeginKnitrBlock{rmdimportant}<div class="rmdimportant"><div class=text-justify>
O tópico referente à tipografia científica em [**LaTeX**](https://www.latex-project.org/) não será abordado, visto que esse assunto atualmente está sendo apresentado na disciplina de Metodologia do Trabalho Científico no início do curso. Além disso, o tópico referente à programação em [**R**](https://www.r-project.org/) abordará aspectos mais avançados da linguagem, uma vez que a essa altura do curso, os alunos entendem os conceitos básicos da linguagem [**R**](https://www.r-project.org/).

Sendo assim, esse não é o material adequado para você, caso o seu enteresse seja aprender a linguagem de programação [**R**](https://www.r-project.org/). Em um futuro próximo, quando este material estiver concluído e caso você já considere um usuário avançado de [**R**](https://www.r-project.org/), talvez pular para os assuntos referentes à estatística computacional venha ser mais produtivo para o seu aprendizado.
</div></div>\EndKnitrBlock{rmdimportant}

## Tecnologias abordadas no curso {-}

1. Uso de [**git**](https://git-scm.com/) e [**GitHub**](https://github.com/prdm0/aulas_computacional) para versionamento de projetos;

2. Linguagem de programação [**R**](https://www.r-project.org/) sob um olhar mais avançado:
  - Orientação à objeto utilizando funções genéricas (sistema S3 de orientação à objeto);
  - Sistema R6 de orientação à objeto;
  - Expressões regulares (**regex**);
  - Uso de funcionais. Nessa parte será revisado os funcionais do **base r** bem como serão apresentados novos funcionais;
  - Construção de pacotes em R;
  - Uso de pacotes que incorporam características novas à linguagem R, entre eles, alguns dos pacotes da comunidade do [**RStudio**](https://www.rstudio.com/);
  - Conceitos de metaprogramação.
  
3. ~~Linguagem de marcação: [**LaTeX**](https://www.latex-project.org/)~~;

4. Linguagem de marcação: [**markdown**](https://en.wikipedia.org/wiki/Markdown);

5. Checando a peformance do código e identificando gargalos;

6. Closures;

7. Paralelismo em R [(**OpenMP**)](https://pt.wikipedia.org/wiki/OpenMP).

Em substituição ao item 2, trataremos do [**rmardkown**](https://rmarkdown.rstudio.com/), em especial, do uso do pacote [**bookdown**](https://bookdown.org/) para a construção de relatórios e livros dinâmicos utilizando a linguagem de marcação [**markdown**](https://en.wikipedia.org/wiki/Markdown). Por exemplo, esse material foi construído utilizando essas ferramentas.

**Nota**:

\BeginKnitrBlock{rmdnote}<div class="rmdnote"><div class=text-justify>
Um bom material em lingua portuguesa sobre o [**LaTeX**](https://www.latex-project.org/) poderá ser obtido no [**link**](http://www.mat.ufpb.br/lenimar/textos/breve21pdf.zip).
</div>  </div>\EndKnitrBlock{rmdnote}

## Teorias abordadas no curso {-}

1. Geração de números pseudo-aleatórios:
  - Método da inversão;
  - Método da aceitação-rejeição;
  - Método da transformação.

2. Métodos de Monte Carlo;

3. Métodos de reamostragem:
  - Jackknife;
  - Bootstrap: para estimação de erro-padrão de um estimador, correção de viés, construção de intervalos aleatórios, testes de hipóteses, bootstrap de Wu (bootstrap selvagem). Algumas dessas metodologias serão apresentadas em esquemas simples (um nível de bootstrap) e duplo (dois níveis de bootstrap).

4. Métodos de otimização não-linear em estatística: métodos de Newton e quasi-Newton.

## Sugestões de passos para revisão da linguagem R {-} 

\BeginKnitrBlock{rmdimportant}<div class="rmdimportant"><div class=text-justify>
É aconselhado que antes de prosseguir nesse material o leitor faça uma revisão básica da linguagem R. Entre os princiapis conceitos necessários para uma boa progressão nesse curso, destacam-se:

1. Entenda as diferenças de funcionamento de um compilador para um interpretador. Lembre-se, **R é uma linguagem interpretada**;

2. Revise os principais tipo de dados: **character**, **double**, **integer** e **logical**. Lembre-se que por regra de coerção, os tipos mais flexíveis em R seguem a seguinte regra de flexibilidade: **character > double > integer > lógico**. Isso quer dizer, por exemplo, que `a` é um vetor que possui elemtendos do tipo character e double, então todos os elementos do vetor serão coagidos para o tipo mais flexível, nesse caso o tipo character. **Exemplo**: `a <- c(1, letters[1:5]); is.character(a[1])` retornará `TRUE`.

3. Lembre-se que R não possui constantes. Constantes são tratadas como vetores atômicos de comprimento 1. Esses são chamados de atômicos por se a estrutura básica da linguagem, uma vez que R é uma linguagem vetorial;

4. Por falar em vetores atômicos / vetores, revise as principais **estruturas de dados** em: vetores atômicos (`c()`), fatores (`factor()`), listas (`list()`), matrizes (`matrix()`), sequência de matrizes (`arrays()`), tabelas (`data.frames()`). Note que uma matriz é um array de comprimento 1. Não confunda estrutura de dados com tipo de dados. Estruturas de dados refere-se ao mecanismo de organização de dados, já o tipo de dados refere-se ao tipo básico das informações que são organizadas nas estruturas de dados;

5. Entenda o uso das funções `is.troque()` e `as.troque()`, em que `troque` poderá ser ser substituido por: 
  
     - **Um Estrutura de dados**: `vector`, `factor`, `list`, `numeric`, `data.frame`, `matrix`, `array`.  

     - **Um Tipos de dados**: `integer`, `double`, `numeric`, `character` e `logical`.
  
6. Revise os operadores relacionais e lógicos:
  
    - **Operadores Relacionais**: `==`(igual), `<` (menor), `<=` (menor ou igual), `>` (maior), `>=` (maior ou igual), `!=` (diferente);
    - **Operadores Lógicos**: `||` (**OU** lógico), `&&` (**E** lógico), `!` (**NÃO** lógico). Esses são operadores não vetorizados. Versões vetorizadas serão abordadas no decorrer do curso.</br></br>
  

7. Revise as estruturas de condições: `if`, `else`, `switch`, `ifelse`. A função `ifelse` equivale à estrutura `(condição) ? retorno 1 : retorno 2` das linguagens C/C++; 

8. Revise as estruturas de repetições: `while`, `for` e `repeat`. Entenda o uso das instruções `break` e `next` quando utilizadas dentro dessas estruturas.

9. Revise a construção de funções em R. Tente entender a flexibilidade embutida em funções que retornam uma lista. 

10. Se achar necessário, revise algumas funções úteis: `ls()`, `rm()`, `length()`, `sum()`, `abs()`, `mean()`, `median()`, `var()`, `sd()`, `cor()`, `summary()`, `sqrt()`, `exp()`, `expm1()` (fornece uma boa proximação para `exp(x) - 1`, quando `x` é pequeno), `log()`, `log10()`, `log1p()` (fornece uma boa aproximação para `log(x+1)` quando `x` é pequeno), `round()`, `union()`, `intersect()`, `choose()`, `factorial()`, `dim()`, `ncol()`, `nrow()`, `diag()`, `%*%`, `t()`, `solve()`, `det()`, `eigen()`, `print()`, `cat()`, `paste()`, `paste0()`, `substring()`,`str()`, `sort()`, `quantile()`, `match()` e `%in%`. Lembre-se que quando os operadores `+`, `-`, `*`, `/`, `%%` (módulo / resto da divisão) e `^` são aplicados ente matrizes, ou entre matrizes e vetores de comprimento 1 ("constantes"), as operações serão realizadas elemento à elemento.
</div></div>\EndKnitrBlock{rmdimportant}
Diversas outras características da linguagem R são importantes e serão lembradas aos poucos na medida que for necessário. Ficará a cargo do leitor fazer as sugestões de revisões acima.

O capítulo que inicia esse material é dedicado à apresentação de exercício em que o leitor deverá resolver. Trata-se de um capítulo em que os exercícios envolvem as sugestões de revisão da linguagem R apresentadas acima. Os exercícios para serem resolvidos poderão exigir revisões de outros conceitos que não foram listados na proposta de revisão acima. No entanto, se esses exercícios forem bem resolvidos, utilizando-se de boas práticas de programação em R, a leitura desse material será a mais agradável possível.

-----
