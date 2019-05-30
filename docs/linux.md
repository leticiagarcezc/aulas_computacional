# Evangelizando para o uso do GNU/Linux

Nesse capítulo tentarei o convencer, sem imposições, que o uso de alguma distribuição GNU/Linux poderá ser um caminho coerente e que tratá facilidades para quem deseja um sistema operacional flexível, fácil de manter e livre. Tentarei aqui expressar minhas experiências no uso do linux na estatística e irei sugerir distribuições GNU/Linux que considero interessantes.


**Observação**:

\BeginKnitrBlock{rmdobservation}<div class="rmdobservation"><div class=text-justify>
Você é livre para escolher o sistema operacional (SO) ao qual deseja trabalhar. Porém, em situações em que seja necessário dissertar sobre alguma configuração específica do SO (**não serão muitas**), as explicações apresentadas levarão em consideração apenas sistemas GNU/Linux.
</div></div>\EndKnitrBlock{rmdobservation}

## Um breve histórico

Em meados de 1970, o Unix foi e nos dias de hoje ainda é um dos sistemas operacionais mais amplamente utilizados em [**mainframes**](https://pt.wikipedia.org/wiki/Mainframe) devido à sua ampla confiabilidade, distribuição e suporte. Muitos desses sistemas Unix se tratavam de sistemas proprietários. Entre os sistemas Unix mais populares e livres estava o **Berkley Software Distribution** (**BSD**) cujo desenvolvimento (1977 e 1995) era realizado pela **Computer Systems Research Group** (**CSRG**) vinculado à Universidade da Califórnia em Berkely. 

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

1 - [**FreeBSD**](https://www.freebsd.org/):

2 - [**OpenBSD**](https://www.openbsd.org/):

3 - [**NetBSD**](https://www.netbsd.org/):

4 - [**DragonFly BSD**](https://www.dragonflybsd.org/):

**Observação**:

\BeginKnitrBlock{rmdobservation}<div class="rmdobservation"><div class=text-justify>
Linux é uma marca registrada de Linus Torvalds. Você poderá ver essa informação [**aqui**](https://www.freebsd.org/doc/pt_BR.ISO8859-1/articles/explaining-bsd/article.html).
</div></div>\EndKnitrBlock{rmdobservation}

O sistema operacional Linux foi inicialmente desenvolvido pelo engenheiro de software [**Linus Torvalds**](https://github.com/torvalds) em 1991. Nessa época, [**Linus Torvalds**](https://github.com/torvalds) era discente na Universidade de Helsinque, Finlândia como estudante de ciência da computação. Sua dissertação de mestrado intitulada [**Linux: a Portable Operating System**](https://www.cs.helsinki.fi/u/kutvonen/index_files/linus.pdf) (56 páginas) foi defendida no Departamento de Ciência da Computação da Universidade de Helsinque, em 31 de janeiro de 1997. A dissertação introduz problemas de protabilidade do kernel Linux em diferentes arquiteturas de computadores. O autor comenta que quem acompanhou os primórdios do desenvolvimento do kernel Linux, o título de sua dissertação poderia soar como ironia, uma vez que o projeto original do Linux não estava realmente preocupado com a portabilidade do sistema em diversas arquiteturas de processadores. À época, a preocupação maior do projeto era com a execução do Linux em computadores com processadores Motorola 68k [**Amiga**](https://pt.wikipedia.org/wiki/Amiga) e [**Atari**](https://pt.wikipedia.org/wiki/Motorola_680x0), ambos de 32 bits. Isso restringia o uso de Linux em algumas arquiteturas de PCs doméstricos da época.


Atualmente o desenvolvimento do kernel Linux possuem colaborações de diversos programadores ao redor do mundo, em que [**Linus Torvalds**](https://github.com/torvalds) é o pricipal desenvolvedor e gerencia o rumo em que o projeto deverá seguir.

\BeginKnitrBlock{rmdnote}<div class="rmdnote"><div class=text-justify>
[**Aqui**](https://github.com/torvalds) você poderá acessar a conta oficial do Linus Torvalds no [**GitHub**](https://pt.wikipedia.org/wiki/GitHub). Você poderá acompanhar todas as modificações e quando estas foram incluídas no projeto Linux. Mais adiante nesse material trataremos a respeito do uso do [**git**](https://git-scm.com/)/[**GitHub**](https://pt.wikipedia.org/wiki/GitHub). Por sinal, o [**git**](https://git-scm.com/) foi criado pelo Linus Torvalds.
</div></div>\EndKnitrBlock{rmdnote}




## Vantagens em utilizar GNU/Linux

## Algumas distribuições

### Uma sugestão pessoal

## Equivalência de progamas entre diferentes SO

