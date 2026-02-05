LINK ABSOLUTO: Usado para arquivos externos do site

Ex.: <a href="https://www.origamid.com/cursos/">Origamid</a>



LINK RELATIVO: Usado para arquivos internos do site

Ex.: <a href="/produto/bicicletas.html"></a>



##### CAMINHO RELATIVO:

**/index.html** -> Este arquivo esta no diretório raiz /.



**/produto/bibicletas.html** -> Arquivo bibicletas.html no diretório /produtos localizado na raiz.



**index.html ou ./index.html** -> Arquivo index.html no diretório atual ./



**../index.html** -> Arquivo index.html um diretório anterior ao atual ../



**../../index.html** -> Arquivo index.html dois diretórios anteriores ao atual.



---



#### **DISPLAY INLINE E BLOCK**

* INLINE: Respeita o fluxo da escrita sem iniciar uma nova linha, não é possível definir valores de width, height, margin (top/bottom) e etc. É o estilo padrão.
* BLOCK: Inicia uma nova linha e não permite que outros elementos sejam posicionados em sua linha. Aceita todas as propriedades do box model. Estilo inicial de elementos como h1, p, div e outros.



---



#### **IMAGENS**

* A estilização **max-width** 100% garante que imagem nunca fique maior que o seu elemento pai.
* PREFERENCIALMENTE UTILIZAR ARQUIVOS NO FORMATO .SVG, pois traz uma melhor resolução.
* Utilizar arquivos no formato .JPG ao invés de .JPEG por ter um tamanho menor e também ter o fundo transparente.



---



#### **GRID**

O elemento pai deve ser definido como display GRID e para alterar a disponibilização dos itens deve-se utilizar o 'grid-template-columns:'.

EX.:

.grid {

  display: grid;

  grid-template-columns: 220px 220px;

}



grid-template-columns: auto auto; -> Ao definir os atributos em 'auto' os elementos envelopados no grid, acabam ocupando o tamanha máximo permitido do elemento.



* JUSTIFY-CONTENT:

 	- CENTER: Alinha o grid ao centro da tela.

 	- START: Alinha o grid a esquerda da tela.

 	- END: Alinha o grid a direita da tela.

 	- SPACE-BETWEEN: Adiciona um espaçamento entre os itens

 	- SPACE-ARROUND: Tenta adicionar um espaçamento no início, meio e fim das colunas.

 	- SPACE-EVENLY: Tenta adicionar um espaçamento mais igual entre os cantos e o meio das colunas.



* ALIGN-CONTENT: Realiza o alinhamento vertical do grid. (Depende da altura do grid. 'HEIGHT')

 	- END: Alinha o grid ao final.

 	- CENTER: Alinha o grid ao centro.

 	- START: Alinha o conteúdo ao início.

 	- SPACE-ARROUND: Tenta adicionar um espaçamento no início, meio e fim das colunas.

 	- SPACE-EVENLY: Tenta adicionar um espaçamento mais igual entre os cantos e o meio das colunas.



* PLACE-CONTENT: Atalho para os comandos ALIGN-CONTENT e JUSTIFY-CONTENT. (Ex.: place-content: space-evenly space-evenly)





##### **COMO REALIZAR O ALINHAMENTO DOS ITENS DOS GRUPOS:**

* ALIGN-ITEMS:

 	- CENTER: Realiza o alinhamento dos itens ao centro da linha em comparação ao elemento maior (Pois é o elemento que ocupa o maior espaço)

 	- START: Realiza o alinhamento sempre no início da linha.

 	- END: Realiza o alinhamento sempre ao final do elemento.

* JUSTIFY-ITEMS: Recebe os mesmos parâmetros descritos acima (start, center e end) mas o eixo de comparação é vertical.
* place-items: Também recebe os mesmos parâmetros conforme descrito mas ele serve tanto para alinhar verticalmente quanto horizontalmente.



##### **ALINHAMENTO INDIVIDUAL DOS ITENS**

* ALIGN-SELF: Realiza o alinhamento individualmente do item usando o eixo vertical. (Parâmetros: start, center e end)
* JUSTIFY-SELF: Realiza o alinhamento individualmente do item utilizando o eixo horizontal (Parâmetros: start, center e end)
* PLACE-SELF: Realiza o alinhamento individualmente do item mas somente com um parâmetro com os eixos vertical e horizontal. (Parâmetros: start, center e end)



###### **Definindo as linhas do grid (Grid Template Rows)**

 	- 'grid-template-rows: 100px auto' Define o tamanho das linhas.

 	- 'grid-auto-rows:' Linhas são adicionadas automaticamente com o valor de auto.

 	- 'grid-row:' Define a linha do item, funciona da mesma forma que o grid-column.



GRID-COLUMN: Define a quantidade de colunas que o elemento irá ocupar

 	EX.: grid-column: 1 / -1 (Ocupará o tamanho máximo)



COMO IR ALINHANDO OS ITENS UM AO LADO DO OUTRO COM O GRID:

 	- Defina o grif-tamplate-columns : repeat(auto-fit, minmax(valor mínimo, valor maximo))





---



#### **FLEXBOX**

 	- **display: flex** = Os filhos passam a ter um tamanho flexível e ficam um ao lado do outro.

 	- **flex-wrap:** wrap = Caso não caiba todos os elementos em uma mesma linha, quebre para a próxima.





###### **PROPIEDADE FLEX**

 	- flex-grow: 1 = Se esse elemento deve crescer para ocupar o espaço vazio. O 0 impede o crescimento, valores maiores que 0 funcionam como a unidade fr do css grid.

 	- flex-basis: 200px = Valor inicial antes de distribuir o espaço em branco.

 	- flex-shrink: 0 = Caso exista um valor de base, o flex-shrink irá determinar se esse valor pode ser reduzido ou não. 0 significa que ele não pode ser reduzido.

 	- flex: 1 = Atalho para flex-grow: 1; flex-shrink: 1; e flex-basis: 0;



---



#### **POSITION**

A propriedade position possui valores que remove o elemento do fluxo padrão do documento. O padrão é o valor static.



* **position: fixed** = Fixa o elemento na tela.

 	**top, right, left, bottom** = Define o posicionamento dos elementos que não estão no fluxo padrão.



* **position: relative** = Mantém o elemento no fluxo padrão, mas permite modificarmos os valores de top, right, bottom e left do mesmo. O espaço ocupado pelo elemento continuará a ser ocupado, mesmo que o elemento seja movimentado.



* **position: absolute** = É posicionado conforme o elemento pai (**se este estiver com um posicionamento diferente de static Ex.:Relative.** remove o elemento do fluxo padrão.



* **z-index** = Define a posição no eixo z (profundidade) dos elementos que foram posicionados fora do fluxo (relative, fixed, absolute).



MAX-WIDTH = Define um tamanho máximo. (Em imagens pode ser 100%)



---



#### **Landmarks - PONTOS DE REFERÊNCIA**

Tags que marcam pontos de referência (landmarks) foram introduzidas no lançamento do HTML5.



##### **MAIN =**

A tag <main> marca o conteúdo principal da página.

Ex.: Blog: conteúdo do artigo. Comércio eletrônico: descrição/imagem/preço do produto.



Obs: Utilize uma por página.





##### **NAV** =

A tag <nav> marca um bloco de navegação.

Ex.: Geralmente utilizado para a navegação primária e secundária do site.



Obs.: Evite o uso de diversas tags nav, use apenas para a navegação essencial.



##### Atributo **aria-label** =

Este atributo pode ser adicionado a tag <nav> para que facilite a usabilidade de leitores de tela.

Ex.: <nav aria-label="primária" ></nav>



##### Atributo **aria-labelledby** =

Caso o título exista na tela, marque o mesmo com um id e use este atributo para criar uma relação entre eles.



##### **ARTICLE =**

A tag article representa uma região do site que é autoexplicativa (não precisa do restante do site para fazer sentido). Geralmente deve conter um título (h's).

Ex.:Lista de produtos do site, um artigo, post na rede social e outros.





#### **SECTION =**

A tag section pode ser utilizada para agrupar o conteúdo do site em diferentes regiões. Geralmente o conteúdo necessita do seu contexto para ser compreendido.



Obs.: O h1 é impactado em termos visuais quando utilizado na section. O section foi criado para melhor lidar com os headings, porém a sua idealização nunca foi implementada (até hoje 2021).



#### **ASIDE =**

A tag aside é utilizada para marcar conteúdo complementar ao principal do site.

Ex.: Lista de posts mais visitados, informações extras como a descrição de um termo usado no artigo e mais.



#### **HEADER =**

A tag <header> marca o cabeçalho do site (banner), onde geralmente estão presentes a marca, navegação do site e as vezes uma informação introdutória.

Ex.: Pode também ser utilizada para marcar o cabeçalho de regiões como o título de um artigo, data, autor e outras informações.



Obs.: Apenas cria uma landmark se não estiver dentro de main, section, article ou aside.



#### **FOOTER =**

A tag <footer> marca o rodapé do site, geralmente contém informação sobre os direitos autorias, quem escreveu e links para documentos relacionados.



Obs.: Apenas cria uma landmark se não estiver dentro de main, section, article ou aside.



---



#### **LISTAS**



**<UL>** - A tag <ul> marca uma lista de itens sem ordem (unordered list). Cada item da lista deve ser marcado com uma <li></li>

**<OL>** - A tag <ol> marca uma lista ordenada (ordered list).

**<DL>** - A tag <dl> marca uma lista de descrições (description list). A lista é criada com dois elementos <dt> e <dd>

 	**<DT>** - Marca o termo/frase a ser definido.

 	**<DD>** - Marca a definição do termo acima.



##### ESTILOS DA LISTA

Possui diferentes valores que definem o estilo dos marcadores da lista (disc, square e outros). O list-style define o tipo / imagem / posição (outside / inside)



---



#### **<BLOCKQUOTE>**

blockquote marca uma citação extensa e recebe um atributo cite com a fonte.





#### **<q>**

<q> marca uma citação inline (no texto).



#### **<CITE>**

<cite> é utilizada para citar o nome de um trabalho, livro, filme, peça ou algo parecido. Não é para citar autor.



#### **<EM>**

<em> é utilizada para dar enfase em uma frase/palavra no texto.



#### **<STRONG>**

strong é utilizada para marcar uma parte importante do conteúdo.



---



#### **UNIDADE DE MEDIDA**



##### **REM**

Unidade relativa ao tamanho da fonte do elemento raiz html. Na maioria dos browsers com configuração padrão 1rem = 16px.





##### **EM (Não recomendada)**

EM é uma unidade relativa ao tamanho da fonte do elemento pai.





##### **VH e VW**

VH representa o tamanho da altura da tela visível (viewport height) e VW a largura (viewport width). 100vw = 100% da tela.



Obs.: Antes do vh só existia a porcentagem. A porcentagem é problemática para definir o height, pois: height: 100%; significa 100% da altura do pai. A altura do pai sempre é definida pelo tamanho do conteúdo, então basicamente 100% de height não muda em nada.





##### **CALC**

**calc()** é uma função de css que retorna um valor com base no cálculo efetuado entre os (). Podemos combinar unidades.

**calc(100vw / 3) -** Representa 1/3 da tela.

**calc(100% - 20px) -** Remove 20px de 100%.



---

#### **TIPOGRAFIA**

**line-height** = Altura da linha (De 1.3 a 1.5)

**text-indent** = Adiciona o espaçamento da primeira linha do paragrafo.

**letter-spacing =** Adiciona espaçamento entre as letras



---

#### **BACKGROUND**

O background pode receber outros valores além de cores sólidas, como imagens e gradientes. A diferença entre img e o background é que a img faz parte do conteúdo, o background apenas do estilo.



##### **Gradiente**

A função **linear-gradient** gera um gradiente linear na propriedade **background-image**.

A função **radial-gradient** gera um gradiente circular na propriedade **background-image**.



Direção: 90deg, 45deg, to left, to right

Cores: #000 0%, blue 50%, #fff 100%. Cor e local de início.



**background-repeat:** **no-repeat** - Caso deseje que a imagem não se repita

**background-size: cover** - Alterar o tamanho da imagem que está sendo apresentada.

background-position: Indica a partir de onde será cortado/expandido a imagem.



---

#### **PSEUDO CLASSES**

###### **ESTADO**

Diferentes estados que um elemento HTML pode ter.



###### **:hover** - Mouse em cima

###### **:focus** - Elemento em foco, usando a tecla (tab).

###### **:active** - Quando clicamos no elemento.

###### **:visited** - Para links que já foram visitados.



**TRANSITION: 0.3** - Tempo de animação.



---

#### **SELETORES**



###### **:FIRST-CHILD** - Seleciona o primeiro elemento

###### **:LAST-CILD** - Selecione o último elemento

###### **:NTH-CHILD(4)** - 4 (quatro elementos), even(pares), odd(ímpares), 3n(de 3 em 3)



###### **:NOT**

###### O **:not** nega a seleção de um elemento específico.



---

#### **PSEUDO ELEMENTS**





###### **::BEFORE /  ::AFTER**

Os pseudo elements :	:before e ::after criam elementos HTML com base no seletor.



**CONTENT** - Definir um conteúdo para o elemento é essencial para ele existir, mesmo que o conteúdo esteja vazio.

**USO** - São utilizados para decorarmos o conteúdo, com eles evitamos o uso de elementos desnecessários no HTML.

