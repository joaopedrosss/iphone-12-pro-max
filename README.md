# iphone-12-pro-max
Um site promovendo o Iphone 12 Pro Max.
A web site promoting Iphone 12 Pro Max.

## Endereço do Site:
Link longo: https://joaopedrosss.github.io/iphone-12-pro-max/
Link curto: [http://gg.gg/12-iphone](http://gg.gg/12-iphone)

## Para melhor visualizar este conteúdo
Este documento foi escrito em Markdown Language.
[Clique Aqui](https://github.com/joaopedrosss/iphone-12-pro-max/blob/main/README.md) para melhor visualização do conteúdo.

## Integrantes da Equipe

- Antonny Gabriel da Conceição Félix
- Eduardo Romero de Araújo Guilhermino Sousa* 
- João Pedro Simões da Silva Sousa
- Maria Clara Gomes Oliveira

**obs.:** **o aluno Eduardo Romero não está mais participando das nossas aulas de Web*

## IFAL - Resumo das alterações - 12/12/2020

### Considerações Iniciais

Para essa nova versão, destacamos os recursos do framework Bootstrap usados.

Talvez, como pode-se notar a seguir, não tenham sido feitas alterações significativas: o projeto já usava recursos do Bootstrap desde de suas versões iniciais.Assim,muitos dessem vão ser apenas destacados,pois já estavam na versão anterior.

De qualquer forma, para chamar os recursos do Bootstrap, usamos as seguintes tags em todas as páginas:

**Em `<head>`**
```
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css"/> 
```

**Em `<body>`**
```
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
```
### Sistema de Grid
Usamos o sistema de grind em 3 páginas:
**Em `index.html`:**
```
    <div class="row justify-content-center">
        <div class="col-md-7">
            <!--html...-->
        <div class="col-md-5 action-text" onmouseover="return back()" onmouseleave="return back2()" ontouchstart="return back()" ontouchend="return back2()" id="action-text">
             <!--more html...-->
```
Ela foi divida em 2 colunas: das 12 **colunas** em que a `row` é divida, 7 são ocupadas pela imagem inicial do iphone e 5 pelo action-text.

**Em `whats.html`**:
```
    <div class='row justify-content-center'>
        <div class="col-md-6" style='text-align: center; padding-top:3%;align-content: center;'>
            <!--html...-->
        <div class='col-md-6 image' style='align-content: center;'>
            <!--more html...-->
        
```
Neste caso, a tela é dividida ao meio: 6 **colunas médias** são ocupadas pelo texto informativo e restante das 6 é ocupada pela foto do iphone.

**Em `buy.html`**:
```
<section class='row justify-content-center main-section'>
      <div class="col-md-12">
```
Neste caso, a tela é dividida assim: todas as 12 colunas, todas são ocupadas pelo conteúdo principal, que é a tabela.Talvez, uso das colunas neste caso possa parecer desnecessário, pois não há conteúdo um ao lado da outro.

Na verdade, ele usado apenas dar resposividade ao conteúdo da página via o framework Bootstrap.
### Componentes do Bootstrap - img-fluid

Foi usado a classe `img-fluid` para deixa o tamanho da imagem resposiva ao tamanho da tela, como demonstrado no(s) o(s) exemplo(s) a seguir:

**Em `index.html`:**
```
<img class='img-fluid' src="images/iphone -1.png" alt="iphone-12" style='width:auto'>
```

**Em `whats.html`:**
```
<img class='img-fluid' src="https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/iphone-12-pro-max-blue-hero?wid=470&hei=556&fmt=png-alpha&.v=1604021658000" onmouseover="return mudar()" id="iphones" >
```

**Em `hardware.html`:** - *idem para todas as outras imagens*
```
<img class='img-fluid' src="images/tela.jpg" style="border-radius: 20%" />
```

Ainda nesta pagina,como mostrado no último exemplo, foram retirados os atributos `width` e `height` de todas as tag `<img>` para que o tamanho da imagem não fosse fixo, mas sim resposivo ao tamanho da tela.

Com isso,também tivemos que redimensionar todas as imagens nesta página afim de que elas ocupassem menos espaço de memória de forma a diminuir o tempo de loading da página.
### Componentes do Bootstrap - nav-bar

**Todas as páginas tem a mesma tag `<header>`** com a classe do Bootstrap `container-fluid` que configurar um bloco "container" que ocupa todo o comprimento disponível na página - mais espeficamente,no "viewport".

**Nela, temos a  barra de navegação do site - `nav` `nav-item` `nav-link`- *(Início - O que É - Funcionalidades- Peça o Seu - Cadastra-se - Sobre)*** como demonstrado abaixo:

```
    <header class="container-fluid main-header">
      <h1 class="title">Iphone 12 Pro Max</h1>
      <ul class="nav justify-content-center">
        <li class="nav-item">
          <a class="nav-link" href="index.html">Início</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="whats.html">O que é</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="hardware.html">Funcionalidades</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="buy.html">Peça o Seu</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="form.html">Cadastre-se</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="sobre.html">Sobre</a>
        </li>
      </ul>
      <div class="progress">
        <div class="progress-bar" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"
          style="width: 0%;">
        </div>
      </div>
    </header>
```
### Componentes do Bootstrap - progress bar
No tópico anterior, foi dito que o `<header>` era igual a todos as páginas.
Mas isso não é totalmente verdade, pois **há a `div` da classe `progress`, que é o código da barra de progresso/progress bar**, cujo código é descrito abaixo.

```
<div class="progress">
        <div class="progress-bar" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"
          style="width: 0%;">
        </div>
      </div>
```

**O atributo `style="width: 0%;"` indica o progesso da barra azul**- e o seu comprimento.Nas 6 páginas, o progresso de 100% de é dividido por 5: na **primeira** página o progesso é de **0%**;na **segunda**, o progresso aumenta para **20%**;na **terceira**, **40%**...até ser **100%** na **sexta** página.
### Componentes do Bootstrap - button

Usamos o botão -`button`- já disponibilizado pelo Bootstrap em todas as páginas que o usam.

**Em `index.html`:**
```
<a class="btn btn-primary btn-lg" href="whats.html" role="button">Saiba Mais</a>
```

**Em `whats.html`:**
```
<div class='saiba-mais'><a class="btn btn-primary btn-lg" href="hardware.html" role="button">Funcionalidades</a></div>
```

**Em `buy.html`:**
```
<div class='pedir'><a class="btn btn-primary btn-lg" href="" role="button">Pedir</a></div>
```

**Em `form.html`:**
```
<input type="submit" form="cadastro" class='fazer-conta btn btn-primary btn-lg' role="button">
```
### Outras Alterações - botão back to top
Foi colocado um botão de voltar ao topo em `hardware.html`:

**HTML**:
```
<button onclick="goTop()" id="botaoTop">Top</button>
```

**JAVASCRIPT**:
```
var btop = document.getElementById("botaoTop");
window.onscroll = function(){scroll()}

function scroll(){
    if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
    btop.style.display = "block";
  } else {
    btop.style.display = "none";
  }

}
function goTop(){
    document.body.scrollTop = 0;
    document.documentElement.scrollTop = 0;
}
```

**CSS**:
```
#botaoTop {
  display: none;
  position: fixed;
  bottom: 20px;
  right: 30px;
  z-index: 99;
  font-size: 18px;
  border: none;
  outline: none;
  background-color:#0f3abd9d;
  color: rgba(255, 255, 255, 0.637);
  cursor: pointer;
  padding: 15px;
  border-radius: 4px;
}

#botaoTop:hover {
  background-color: #0f3bbd;
  color: white;
}
```
### Outras Alterações - title 
O `<title>` das imagens muda de acordo com a imagem do iphone em `whats.html` de acordo com o código abaixo em `whats.js`.
```
imagem.title = cores[novo]
```
### Considerações Finais
Dadas estas e outras alterações inrelevantes e pontuais, estas foram as alterações mais recentes do projeto.

## IFAL - Resumo das alterações - 6/12/2020

### Introdução

Criou-se a pasta **script** para armazena o código em javscript usado no projeto.O `form.js` tem o codigo de **validação dos formularios**, enquanto os outros - `hard.js` , `index.js`, `sobre.js`,`whats.js`- têm o código das "animações" - isto é, da **interatividade do JavaScript com a DOM** - NamedNodeMap object.

### Validação do Formulário

O código para validar o envio do formulário está em `form.js` como já dito.

Para pegar e manipular todos os elementos da DOM, foi usada uma estrutura semelhante a esta:

```
    var nome = document.cadastro.nome.value;
    if (nome == "" || 
    nome.length < 3){
        alert("O campo NOME precisa ter no mínimo 3 dígitos");
        nome.focus();
        return false;
    };
```

Vale destacar a forma como foi feita a manipulação para pegar elementos `input` do tipo `radio`:

```
    q_receber = -1;
    for (x = receber.length - 1; x > -1; x--){
        if(receber[x].checked){
            q_receber = x;
        }
    };
    if(q_receber == -1){
        alert("Quer receber nossos emails?");
        receber[0].focus();
        return false;
    };
    if (!(termos[0].checked)){
        alert("Precisa aceitar nossos Termos e Condições de Serviço para prosseguir.");
        return false;
    }
```

### Animações

As animações são das mais diversas.

Começando na página index.html - **Início**-, no qual o **"banner" azul fica mais escuro quando o mouse passar por cima**. Não só com mouse, mas **também com o dedo** em um dispositivo com tela touch, afim de manter *a mesma responsividade* indepentente do dispositivo.

Isto de se deve ao uso dos eventos `onmouseover` e `onmouseleave` (desktop) tal como os eventos `ontouchstart` / `ontouchend` (mobile) nos scripts, como mostrado a seguir:

**HTML**:

```
<div 
    class="col-md-5 action-text"
    onmouseover="return back()" 
    onmouseleave="return back2()" 
    ontouchstart="return back()" 
    ontouchend="return back2()" 
    id="action-text">
    (...)
</div>
```

**JAVASCRIPT**:

```
function back(){
    fundo = document.getElementById("action-text")
    fundo.style.background = "#0c0ca583";
}

function back2(){
    fundo = document.getElementById("action-text")
    fundo.style.background = "#0c0ca5";
}
```

Na verdade, *esses eventos são amplamente usados aqui e tem outros usos neste site*.

Um dos outros usos de tais eventos **é quando as letras da maioria da textos mudam de cor com o passar do mouse/dedo por cima delas** nas outras páginas como a seguir:

```
<h2 onmouseover="return color(this)" 
onmouseleave="return uncolor(this)" 
ontouchstart="return color(this)" 
ontouchend="return uncolor(this)">
Front-End desenvolvido por:</h2>
```

Uma animação de destaque se encontra na página `whats.html` - **O que é** - **na qual ao passar o mouse por cima do Iphone, outro Iphone de outra cor aparece no lugar**. Isso serve para mostrar as diferentes cores disponíveis do Iphone 12 Pro Max.

Para da esse efeito, foi usado o (trabalhoso) código em `whats.js` com a função `mudar()`.É dito trabalhoso pois,apesar do código ser pequeno, foi gasto muito tempo para chegar a tal raciocínio.

Em `hardware.html` - **Funcionalidades** - **apenas os títulos mudam de cor** a fim de proporcionar melhor leitura de textos longos aos usuários.

Ainda nesta página, você poderá ter uma surpresa quando **passar o mouse por cima da maçã colorida** ao final da página - uma maçã branca surge no lugar.

Em `sobre.html` as letras também mudam de cor quando em contato com o mouse.Nela, **parece haver um erro**, pois a data de atualização - **29 de novembro de 2020** - está **atrasada**.

Isto foi proposital: **quando se passa o mouse nela,a data logo muda para 6 de dezembro de 2020, a data correta**.Isso foi feito tão somente a fim de colocar em prática um dos requisitos para esta presente entrega/atualização do projeto.

### Outros ajustes

Não houve nenhuma alteração em  `buy.html`- **Peça o Seu**.

Na página `form.html` - **Cadastre-se** - em questão de estilo mudou-se a cor de fundo do do formulário para a cor `rgba(0, 86, 156, 0.157)`.Além disso, foram inseridos novos atributos nos elementos html a fim de achar esses elementos mais tarde no script, como exemplificado no código abaixo:

```
<input class="text" type="password" id="rep_senha" name="rep_senha" placeholder="digite novamente sua senha">
```

Nele, foram inseridos um `id` e um `name`.

Fora outros pequenos ajustes não relevantes,estas foram as alterações feita no projeto.

## IFAL - Resumo das alterações - 29/11/2020

### Formulário
**O formulário se encontrar no documento recém criado** `form.html`.
Para fazer as tags foram usadas as tags `<form>`, `<label>` ,`<input>` ,`<br>`,`<div>`, `<select>` e `<option>`.

Em cada uma das diversas tag `<option>` foi colocada um nome de um país em referência a tag `<select>`,onde o usuário pode selecionar o seu país de origem.

Os nomes países não foram colocados um de cada vez.Para isso pegamos um código já pronto em um [site](https://www.codigofonte.com.br/codigos/lista-de-paises).

Além disso, para as tags `<input>` foram usados os seguintes `types`(tipos):`radio`,`text`, `password`,`email` e `date`. 

E cada tag `<input>` com o atributo `class="text"` conta com o seu próprio atributo `placeholder`.

**A estilização do formulário se encontra em** `form.css` (também recém criado).

### Media Queries
Os documentos `form.css`,`whats.css`,`index.css`,`hardware.css` e `buy.css` **contém media queries** afim de que os elementos do site respondam adequadamente aos diferentes tamanhos de tela.

Como exemplo,este trecho de código que se encontra em `buy.css`:
```
@media (max-width:480px) { /*mobile*/
    body{
        background-image: url("http://tiledwallpaper.com/wallpapers/2018/3/21020836275ab0bc5222aa24.22375899.jpg");
    }
    .dados {
        width:200px;
    }
    input{
        width:200px;
    }
}
@media(min-width:481px) and (max-width:1024px) { /*tablet*/
    body{
        background-image: none;
        background-color: #00043B;
    }
}
@media(min-width:1025px){/*desktop*/
    body{
        background-image: url("https://lh3.googleusercontent.com/pw/ACtC-3e3mO3DMh-YoArEDcXwdnwcgtnf8Rn_BAbv5MHWOy9jMeCeHIHq7-_sMY1o_X-nf1NZKsULQwzETRCw9F3nNkfGfDCtnu8Vjm5CsJUPdC9_2xabZInEkrjyOfaQdUTWDI-F_thIYxxUY5i0XLsFPgHK=w1151-h647-no?authuser=0");
    }
    
}
```

### Outros Ajustes
Foi criada uma pasta *css* a fim de armazenar exclusivamente as Folhas de Estilo Em Cascasta (**CSS Sheets**) dos documentos HTML.

**Ou seja,todos os documentos .css estão na pasta css.**

Agora a imagem de fundo (background-image) de `buy.html` muda de acordo com a largura da tela.Esse variação foi feita com um media query em `buy.css`(no caso, o trecho de código anterior).

Em `sobre.html`, foi mudada a data da último atualização do site - no caso, colocamos a data da entrega mais recente do projeto, embora as tais altualizações já estivessem prontas em **27 de novembro de 2020**.

Fora as mudanças já citadas, foram feitas outras alterações mais pontuais e menos relevantes para este contexto.

## IFAL - Resumo das alterações - 22/11/2020

### sobre.html
Mudamos o nome da antiga pagina `devs.html` para `sobre.html`, bem como seu nome na barra de navegação.Apenas uma mudança de nome,haja visto que seu conteúdo já estava presente na versão anterior.
Além disso, agora ela conta com um link do repositório do projeto no github:

```
<div class='github'>
        <p>
            O código fonte do projeto se encontra em seu <a href='https://github.com/joaopedrosss/iphone-12-pro-max' target='_blank'>Repositório do Github</a>
        </p>
    </div>
```
### devs.css
Foi adicionado um seletor a fim de mudar o estilo no bloco de código anterior:

```
.github{
    text-align: center !important;
    font-size: 1.5rem;
}
```

### index.html
Foi adicionado a tag `<pictures>` a fim de ter imagens responsivas:

```
<picture>
    <source media="(min-width: 900px)" srcset="phone -2.png" >
    <img src="images/iphone -1.png" alt="iphone-12" style='width:auto'>
</picture>
```

### buy.html
Foi criada esta nova página na qual estão inseridas uma imagem de fundo,uma tabela( `class="dados"`) e um título (`h2`).
A tabela tem **Título** (`<caption>Meu Iphone</caption>`),**Cabecalho**(`<thead><tr><td colspan="2">Iphone 12 Pro Max</td></tr></thead>`),com **mesclagem de colunas** incluido.

### buy.css

Foi adicionado uma imagem de fundo a página `buy.html`:
```
body {
    background-image: url("https://lh3.googleusercontent.com/pw/ACtC-3e3mO3DMh-YoArEDcXwdnwcgtnf8Rn_BAbv5MHWOy9jMeCeHIHq7-_sMY1o_X-nf1NZKsULQwzETRCw9F3nNkfGfDCtnu8Vjm5CsJUPdC9_2xabZInEkrjyOfaQdUTWDI-F_thIYxxUY5i0XLsFPgHK=w1151-h647-no?authuser=0");
}
``` 

Além disso, outro recurso disponível é o de **células zebradas**.

```
tbody > tr:nth-child(even){
    background-color: rgba(11, 11, 216, 0.137);
}
tbody > tr:nth-child(odd){
    background-color: #04041b;
}
```

Somando a isso,ainda há todas as outras declarações CSS para estilizar a página.

### index.css
Também foi acrescentado um recurso de **sombreamento** em `index.css` em `<h1 class="title">Chegou o Novo Iphone da Apple</h1>`:

```
.title {
    text-shadow: 2px 2px 5px rgb(78, 73, 73);
}
```

## IFAL - Resumo das alterações - 15/11/2020

### index.html

Em `<body>` , há duas tags delimitadores de conteúdo: `<header>` e `<section>`.
A tag `<header>` ,cuja classe é `main-header`, delimita o **Cabeçalho** da página.
A tag `<header>` e seu conteúdo está presente e é o mesmo em todos os documentos html. 

Foi alterado em `<header>`:
* o nome da página "Especificações" passar a ser "Funcionalidades".

Em `<section>`, da classe `main-section`, é onde fica o conteúdo principal da página.

### index.css

Houve sutis mudanças de cores: foi alterado a cor de fundo da `<div>` da classe `action-text`, além de adicionada na mesma margem no topo de 2%.

Além disso,foi adicionado o seguinte bloco de código:

```
.btn{
    background-color:#0f3bbd;
    outline: none;
   border: none;
}
```

Tal bloco é referente ao botão na `<div>` "Saiba Mais" no qual foram retiradas bordas e contornos, além de mudar a cor de fundo.

### whats.html

Foi adicionado o seguinte bloco de código:

```
<p>
    Conheça mais sobre as funcionalidades que o novo Iphone tem a te oferecer.
</p>
<div class='saiba-mais'>
    <a class="btn btn-primary btn-lg" href="hardware.html" role="button">Funcionalidades</a>
</div>
```

### whats.css

Foi adicionado o seguinte bloco de código:

```
.btn{
    background-color:#0f3bbd;
    outline: none;
   border: none;
}
```
Para o botão de "Funcionalidades".

### devs.html

Foi adicionada uma `<div>`, de classe "devs", e um `<footer>`.

A `<div>` contém os créditos aos desenvolvedores do front-end, com um título `<h2>` e uma lista não ordenada `<ul>`.

Já `<footer>` contém apenas um título `<h4>` com a data da última atualização feita no site.

### devs.html

Foram adicionadas diversas declarações css para melhor estilização dos elementos, definindo:
- margens
- tamanho de fonte
- alinhamento de texto
- estilo de lista

Em especial, vale destacar o seguinte bloco:

```
h4 {
    border: 1px white solid;
    text-align: center;
    margin-left: 5%;
    margin-right: 5%;
    padding: 1%;
}
```

Que define a estilização do título `<h4>` em `<footer>`.

Para `<h4>` , foi adicionada uma**borda**, de 1px de largura, de cor branca e estilo solid.

### Considerações Finais

**Não foi usada nenhum tipo de sombreamento, seja para bordas ou textos, por razões de escolha das estéticas mais apropriadas ao front-end.**

## IFAL - Resumo das alterações - 08/11/2020
O resumo das alterações estão nos comentários em um dos últimos commits feitos disponivel em:
https://github.com/joaopedrosss/iphone-12-pro-max/commit/4f983af5eaa95eb5601d01812a38c95893c75473
