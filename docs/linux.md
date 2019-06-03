# Evangelizando para o uso do GNU/Linux

Nesse capítulo tentarei o convencer, sem imposições, que o uso de alguma distribuição GNU/Linux poderá ser um caminho coerente e que trará facilidades para quem deseja um sistema operacional flexível, fácil de manter e livre. Tentarei aqui expressar minhas experiências no uso do linux de uma forma geral e na estatística. Ao final, irei sugerir distribuições GNU/Linux que considero interessantes e elencarei os motivos.

<img src="images/linux_class.jpg" width="90%" style="display: block; margin: auto;" />

</br>**Observação**:

\BeginKnitrBlock{rmdobservation}<div class="rmdobservation"><div class=text-justify>
Você é livre para escolher o sistema operacional (SO) ao qual deseja trabalhar. Porém, em situações em que seja necessário dissertar sobre alguma configuração específica do sistema (**não serão muitas**), as explicações apresentadas levarão em consideração apenas sistemas GNU/Linux.
</div></div>\EndKnitrBlock{rmdobservation}

## Um breve histórico

Em meados de 1970, o Unix foi e nos dias de hoje ainda é um dos sistemas operacionais mais amplamente utilizados em [**mainframes**](https://pt.wikipedia.org/wiki/Mainframe) devido à sua ampla confiabilidade, distribuição e suporte. Muitos desses sistemas Unix se tratavam de sistemas proprietários. Entre os sistemas Unix mais populares e livres estava o **Berkley Software Distribution** (**BSD**) cujo desenvolvimento (1977 e 1995) era realizado pela **Computer Systems Research Group** (**CSRG**), vinculado à Universidade da Califórnia em Berkely. 

**Nota**:

\BeginKnitrBlock{rmdnote}<div class="rmdnote"><div class=text-justify>
Nos dias de hoje, o termo **BSD** é utilizado para designar qualquer sistema operacional do tipo Unix (sistemas **Unix-like**). Muitas vezes o termo **Unix-like** é substituído por **UN\*X** ou **\*nix**. Tratam-se de sistemas operacionais baseados em Unix mas que não necessariamente estão de acordo com a especificação [**Single UNIX**](http://www.unix.org/what_is_unix/single_unix_specification.html).
</div></div>\EndKnitrBlock{rmdnote}

O sistema Linux (**kernel**) foi baseado no Unix, sendo este o sistema  **Unix-like** mais popular dentre diversos outros que são razoavelmente conhecidos pelo público em geral e bastante conhecidos por profissionais que tem alguma afinidade com a computação.

A maioria dos sistemas BSD's disponíveis na atualidade possuem o código fonte aberto, porém fazem o uso da licença [**BSD**](https://opensource.org/licenses/bsd-license.html) que é menos restritiva, permitindo a distribuição somente dos arquivos binários. Trata-se de uma licença atraente para aplicativos embarcados, em que empresas não estão obrigadas a disponibilizar o código fonte das aplicações, quando estes forem solicitados. 

Devido a licença [**BSD**](https://opensource.org/licenses/bsd-license.html) ser menos restritivas que a licença [**GNU General Public License**](https://www.gnu.org/licenses/gpl-3.0.html), utilizada pelo Linux, alguns sistemas BSD's conhecidos possuem código proprietário. Muito provavelmente se você solicitar os códigos às empresas que os construíram o seu pedido não será atendido. Entre os sistemas operacionais proprietários mais conhecidos, destacam-se dois:

1 - O [**Solaris**](https://pt.wikipedia.org/wiki/Solaris), nas suas primeiras versões chamado de **SunOS** e desenvolvido pela [**Sun Microsystems**](https://pt.wikipedia.org/wiki/Sun_Microsystems) que em 2009 foi adquirida pela [**Oracle Corporation**](https://www.oracle.com/br/corporate/). Detalhes a respeito do sistema Solaris podem ser encontrados no site da [**Oracle**](https://www.oracle.com/solaris/).
    
2 - O [**Mac OS X**](https://www.apple.com/macos/server/), sistema operacional produzido pela empresa [**Apple**](https://www.apple.com/). Muito provavelmente o [**Mac OS X**](https://www.apple.com/macos/server/) é o **\*nix** mais amplamente utilizado em PCs. Porém, o [**Mac OS X**](https://www.apple.com/macos/server/) está longe de ser o sistema **\*nix** mais amplamente utilizados em super computadores.

Saindo do território dos sistemas BSD's proprietários, abaixo listo alguns dos mais conhecidos sistemas BSD's em que os códigos dos projetos são abertos, isto é, com [**iniciativas Open Source**](https://opensource.org/):

1 - [**FreeBSD**](https://www.freebsd.org/): Trata-se de um sistema moderno e livre bastante utilizado em servidores, desktops e plataformas embarcadas. O FreeBSD é talvez o sistema BSD, de código livre, que é mais amplamente utilizado entre os sistemas dessa lista. A melhor forma de acompanhar as novidades do FreeBSD é acompanhar o [**FreeBSD Journal**](https://www.freebsdfoundation.org/journal/), um jornal livre dos desenvolvedores do FreeBSD. Seu mascote genérico é o [**BSD daemon**](https://en.wikipedia.org/wiki/BSD_Daemon), apelidado de **Beastie**.  

2 - [**NetBSD**](https://www.netbsd.org/): Trata-se de uma derivação do sistema 4.4BSD da Universidade da California, Berkley e do 386BSD, às vezes chamado de Jolix. Assim como o FreeBSD, o NetBSD é um sistema que pode rodar em diversas arquiteturas de computadores. O seu logo é uma [**bandeirola**](https://www.netbsd.org/gallery/logos.html).

3 - [**OpenBSD**](https://www.openbsd.org/): Trata-se de um projeto baseado no sistema 4.4BSD. O projeto OpenBSD desenvolveu aplicações como o [**OpenSSH**](https://www.openssh.com/) que é a principal ferramenta de conectividade para login remoto utilizando o protocolo [**Secure Shell (SSH)**]("https://pt.wikipedia.org/wiki/Secure_Shell"). O seu mascote é o [**Puffy**](https://en.wikipedia.org/wiki/OpenBSD).

4 - [**DragonFly BSD**](https://www.dragonflybsd.org/): Os seus desenvolvedores afirmam que trata-se de um sistema operacional pertencente à mesma classe de outros sistemas baseados em BSD e Linux, incluindo recursos que o diferenciam de outros sistemas operacionais da mesma classe. Por exemplo, o [**DragonFly BSD**](https://www.dragonflybsd.org/) é o HAMMER, um moderno sistema de arquivos de alta peformance descata-se como a mais proeminente diferença. O mascote do projeto é uma [**libélula**](https://www.dragonflybsd.org/images/).

**Observação**:

\BeginKnitrBlock{rmdobservation}<div class="rmdobservation"><div class=text-justify>
Linux é uma marca registrada de Linus Torvalds. Você poderá ver essa informação [**aqui**](https://www.freebsd.org/doc/pt_BR.ISO8859-1/articles/explaining-bsd/article.html). Além disso, Linux é um **\*nix**, **UN\*X** ou **Unix-like** (como queira chamar) mas Linux não é um BSD nem um BSD é um Linux. Por exemplo, a biblioteca C do BSD é baseada nos códigos de Berkeley e não na [**GNU C Library**](https://pt.wikipedia.org/wiki/GNU_C_Library). Dessa forma, diferentemente dos diversos sistemas BSD's, o Linux  utiliza-se de alguns recursos fornecidos do [**GNU C**](https://gcc.gnu.org/). 
</div></div>\EndKnitrBlock{rmdobservation}

O sistema operacional Linux foi inicialmente desenvolvido pelo engenheiro de software [**Linus Torvalds**](https://github.com/torvalds) em 1991 e o nome Linux não é difícil adivinhar o por quê.


<div class="figure" style="text-align: center">
<img src="images/linus_torvalds.jpg" alt="Linus Torvalds em uma conferência para o [**TED**](https://pt.wikipedia.org/wiki/TED_(confer%C3%AAncia)) intitulada [**A mente por trás do Linux**](https://www.ted.com/talks/linus_torvalds_the_mind_behind_linux?language=pt-br), 2016." width="70%" />
<p class="caption">(\#fig:unnamed-chunk-5)Linus Torvalds em uma conferência para o [**TED**](https://pt.wikipedia.org/wiki/TED_(confer%C3%AAncia)) intitulada [**A mente por trás do Linux**](https://www.ted.com/talks/linus_torvalds_the_mind_behind_linux?language=pt-br), 2016.</p>
</div>

Nessa época, inícios dos anos 90, [**Linus Torvalds**](https://github.com/torvalds) era discente na Universidade de Helsinque, Finlândia como estudante de ciência da computação. Sua dissertação de mestrado intitulada [**Linux: a Portable Operating System**](https://www.cs.helsinki.fi/u/kutvonen/index_files/linus.pdf) (56 páginas) foi defendida no Departamento de Ciência da Computação da Universidade de Helsinque, em 31 de janeiro de 1997. A dissertação introduz problemas de protabilidade do kernel Linux em diferentes arquiteturas de computadores. O autor comenta que quem acompanhou os primórdios do desenvolvimento do kernel Linux, o título de sua dissertação poderia soar como ironia, uma vez que o projeto original do Linux não estava realmente preocupado com a portabilidade do sistema em diversas arquiteturas de processadores. À época, a preocupação maior do projeto era com a execução do Linux em computadores com processadores Motorola 68k [**Amiga**](https://pt.wikipedia.org/wiki/Amiga) e [**Atari**](https://pt.wikipedia.org/wiki/Motorola_680x0), ambos de 32 bits. Isso restringia o uso de Linux em algumas arquiteturas de PCs doméstricos da época.

Segundo [**Torvalds**](https://www.cs.helsinki.fi/u/kutvonen/index_files/linus.pdf), a implementação do Linux foi baseada em três questões principais. São elas:

1 - **Simplicidade**: Muito embora o kernel de um sistema operacional é algo complexo, e isso não é diferente no Linux, a implementação mais simples possível é um dos pilares do projeto.

2 - **Eficiência**: Uma vez que o kernel está envolvido com quase todas as atividades de uma máquina (PCs, mainframes, entre outros), a implementação do kernel Linux busca a eficiência, ou seja, o kernel nunca poderá ser visto como uma restrição de desempenho.

3 - **Compatibilidade**: O que está ocorrendo por baixo do kernel de um sistema operacional poderá ser de interesse para pesquisadores na área de sistemas operacionais. Dessa forma, um sistema operacional não poderá impor "surpresas" ao usuário comum ou mesmo um programador. O Linux é um sistema operacional robusto e disponível para funcionar em diversas arquiteturas e sem "surpresas".

> "Embora o projeto Linux tenha sido intimamente associado a mim pessoalmente, em parte devido ao nome, gostaria de deixar         bem   claro que o sistema operacional Linux é um grande projeto feito cooperativamente por muitas pessoas em todo o             mundo. Mesmo se você desconsiderar todos os programas em nível de usuário que são parte integrante de qualquer sistema Linux,    apenas o kernel contém código de centenas de pessoas ao redor do mundo. Obrigado a todos vocês."

>

> --- Linus Torvalds, [**Linux: a Portable Operating System**](https://www.cs.helsinki.fi/u/kutvonen/index_files/linus.pdf), página 3. 

A todo momento, nessa nossa conversa, a expressão **kernel** foi utilizada junto com o termo Linux. Isso normalmente é feito para deixar claro que o Linux é um programa que gerencia os seus hardwares e o funcionamento dos programas que você utiliza no seu dia a dia, caso você esteja utilizando uma distribuição Linux, é claro. Porém, se você ainda não está utilizando o Linux nesse momento, saiba que o seu sistema operacional possui um kernel, sendo este a parte mais importante do sistema.

Para que um sistema operacional venha ser utilizado pela maioria das pessoas, em que nesse grupo nos incluímos, este deverá conter diversos outros programas e recursos além do kernel propriamente dito. Para nós que trabalhamos com estatístca, por exemplo, precisamos de ter a nossa disposição outras linguagens de programação além de C, como R, C++, Java e Python, IDEs (**Integrated Development Environment**) para desenvolvimento dos nossos programas, softwares para escrita de relatórios, sistemas de gerenciamento de banco de dados, entre outros programas de interesse. 

Atualmente o desenvolvimento do kernel Linux possuem colaborações de diversos programadores ao redor do mundo, em que [**Linus Torvalds**](https://github.com/torvalds) é o pricipal desenvolvedor e gerencia o rumo em que o projeto deverá seguir.

\BeginKnitrBlock{rmdnote}<div class="rmdnote"><div class=text-justify>
[**Aqui**](https://github.com/torvalds) você poderá acessar a conta oficial do Linus Torvalds no [**GitHub**](https://pt.wikipedia.org/wiki/GitHub). Você poderá acompanhar todas as modificações e quando estas foram incluídas no projeto Linux. Mais adiante nesse material trataremos a respeito do uso do [**git**](https://git-scm.com/)/[**GitHub**](https://pt.wikipedia.org/wiki/GitHub). Por sinal, o [**git**](https://git-scm.com/) foi criado pelo Linus Torvalds.
</div></div>\EndKnitrBlock{rmdnote}




## Vantagens em utilizar GNU/Linux

## Algumas distribuições

### Uma sugestão pessoal

## Equivalência de progamas entre diferentes SO

