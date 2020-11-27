<p align="center">
  <img src="https://i.ibb.co/pwNNq14/basic-html-semantic.png" alt="O Básico sobre HTML semântico" border="0">
</p>

## 🚀 Introdução

Um dos recursos mais importantes do [**HTML5**](https://en.wikipedia.org/wiki/HTML5) é sua semântica . HTML semântico refere-se à sintaxe que torna o HTML mais compreensível ao definir melhor as diferentes seções e o layout das páginas da web.

Torna as páginas web mais informativas e adaptáveis, permitindo que os navegadores, leitores de telas e motores de buscas interpretem melhor o conteúdo.

Por exemplo, em vez de usar:

```html
<div id="header"> Esse é o meu cabeçalho </div>
```

Você pode usar uma tag **header** que ficaria assim:

```html
<header> Esse é o meu cabeçalho </header>
```
Você sempre deve utilizar tags semânticas do HTML5 na criação de uma página na web para assim tornar o seu conteúdo mais informativo para os motores de buscas e leitores de telas.

## 🎨 Layout de uma página utilizando HTML semântico

Primeiro vamos observar um modelo de página escrito em HTML não semântico:

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Essa é a página do Gabriel de Jesus</title>
</head>
<body>
  <div id="header">
    Esse é o meu cabeçalho
  </div>

  <div id="main">
    Essa é a parte principal da minha página
  </div>

  <div id="footer">
    Aqui vou colocar o rodapé da minha página
  </div>
</body>
</html>
```

Agora observe como fica a mesma página criada acima utilizando o HTML semântico:

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Essa é a página do Gabriel de Jesus</title>
</head>
<body>
  <header>
    Esse é o meu cabeçalho
  </header>
  
  <main>
    Essa é a parte principal da minha página
  </main>

  <footer>
    Aqui vou colocar o rodapé da minha página
  </footer>
</body>
</html>
```

Você pode observar que a principal diferença entre os exemplos é que substitui as tags **div** por **3 novas tags**: **header**, **main** e **footer**. header, main e footer são tags semânticas , porque elas são usadas para representar diferentes seções em uma página **HTML**.

Observe também que elas são mais descritivas do que as tags div, o que ajuda os motores de buscas a saberem exatamente onde estão as partes da sua página na hora de indexar na web e também ajudam os leitores de tela para deficientes visuais.

## 🕹 Navegação

No HTML5, existe a tag **nav**, que substitui uso da  **div**, na hora da criação do seu menu de navegação.

Por exemplo, o menu de navegação pode ser inserido na seção do **cabeçalho** desse jeito:

```html
<header>
  <img src="logo.png" alt="logo" />
  <nav>
    <a href="index.html">Início</a>
    <a href="about.html">Sobre</a>
    <a href="services.html">Serviços</a>
    <a href="contact.html">Contato</a>
  </nav>
</header>
```

Entretanto, ela também pode ser adicionada após a seção de header

Exemplo:

```html
<header>
  <img src="logo.png" alt="logo" />
</header>
<nav>
  <a href="index.html">Início</a>
  <a href="about.html">Sobre</a>
  <a href="services.html">Serviços</a>
  <a href="contact.html">Contato</a>
</nav>
```

Você pode colocar o menu de navegação em qualquer lugar da página, ele só precisa ser fechado desse jeito:

```html
</nav>
```

No entanto, ele não deve ser colocado dentro da **main**, a menos que a navegação seja específica para aquela página.

Essa restrição existe porque os elementos da main devem ser específicos apenas para a página, embora geralmente o  **header** e **footer** são compartilháveis entre páginas semelhantes.

## 🌐 Conteúdo principal

Para você adicionar algum conteúdo a seção **main**, podemos usar tags como **article** e **section**. Essas tags servem para simplificarem a estrutura do **main**

Observe um exemplo:

```html
<main>
  <article>
    <h1>O Básico sobre HTML</h1>
    <p>HTML é uma linguagem de marcação usada para estruturar...</p>

    <section>
      <h2>Lançamento do HTML5</h2>
      <p>HTML5 foi lançado pela primeira vez em um formulário público em...</p>
    </section>

    <section>
      <h2>Novos recursos do HTML5</h2>
      <p>Muitos novos recursos sintáticos estão incluídos...</p>
    </section>

  </article>
</main>
```

A tag **article** é utilizada para envolver um conteúdo autônomo em uma página. Um conteúdo pode ser considerado autônomo se por exemplo ele puder ser removido da página e colocado em outra página.

A tag **article** pode conter várias tags **section** dentro dela, como no exemplo acima. Então se observarmos uma tag **article** na verdade ela é uma **section** autónoma.

A tag  **section** é bem semelhante à  nossa famosa tag **div**, mas é mais significativa, pois envolve alguns grupos lógicos de conteúdo relacionado *(por exemplo, um capítulo de um artigo)*.

A tag **section** também pode ser utilizada para envolver o próprio artigo, mas nesse caso temos a tag **article** que existe para essa finalidade.

## ➕ Conteúdo adicional
_Seção lateral_

Um conteúdo adicional, sem importância para a compreensão de um artigo, mas relacionado ao artigo, pode ser inserido em uma tag **aside**.

Por exemplo, podemos informar quantas pessoas leram o artigo, quem é o autor do artigo e assim por diante.

Observe um exemplo de um código HTML seguindo esse raciocínio:
```html
<main>
  <article>
    <h1>O Básico sobre HTML</h1>
    <p>HTML é uma linguagem de marcação usada para estruturar...</p>

    <section>
      <h2>Lançamento do HTML5</h2>
      <p>
        HTML5 foi lançado pela primeira vez em um formulário público em...
      </p>
    </section>

    <section>
      <h2>Novos recursos do HTML5</h2>
      <p>Muitos novos recursos sintáticos estão incluídos...</p>
    </section>

    <aside>
      <p>Visto por 102 pessoas</p>
      <p>Autor do post: Gabriel de Jesus</p>
    </aside>
    
  </article>
</main>
```

Como você pode observar no exemplo acima, a tag **aside** permite que os mecanismos de busca extraiam rapidamente informações como autor, visualizações e datas.

Essa tag também pode ser usada para incluir um conteúdo adicional relacionado a uma página inteira, não apenas a um artigo específico.

Por exemplo, a tag **aside** pode envolver em uma barra lateral, anúncios, notas de rodapé e assim por diante.

## 📊 Fluxograma dos elemento do HTML5

Se você não tiver certeza de qual tag semântica usar em um caso específico, você sempre pode seguir este ótimo fluxograma feito pelos autores do [**HTML5Doctor**](http://html5doctor.com/).

<p align="center">
  <img src="http://html5doctor.com/downloads/h5d-sectioning-flowchart.png" alt="Fluxograma dos elemento do HTML5" border="0">
</p>

## 💡 Suporte para navegadores

As tags semânticas do **HTML5** são bem suportadas nas versões mais recentes dos navegadores. Para algumas versões mais antigas do _Internet Explorer_, _Firefox_ e _Safari_, você pode utilizar o [HTML5 Shiv](https://github.com/aFarkas/html5shiv) ou [Modernizr](https://modernizr.com/) (que inclui o HTML5 Shiv).

## 🎁 Recursos adicionais

Para obter mais informações sobre este tópico, você pode ler estes artigos muito úteis:
- [Estrutura HTML5 - div, seção e artigo](http://oli.jp/2009/html5-structure1/)
- [O elemento do artigo](http://html5doctor.com/the-article-element/)
- [Introdução ao schema.org usando microdados](https://schema.org/docs/gs.html)
- [Elementos semânticos HTML5 e Webflow: o guia essencial](https://webflow.com/blog/html5-semantic-elements-and-webflow-the-essential-guide)

## 🏆 Conclusão

Nesse guia tentei abordar algumas vantagens do uso do HTML semântico e aprooveitamos e criamos um layout básico.

Espero que esse guia tenha dado a você uma compreensão de como o HTML semântico pode melhorar uma página da web e a interação dos mecanismos de pesquisa e leitores de telas para deficientes visuais.

E com mais navegadores aceitando **HTML5**, as tags semânticas inevitavelmente se tornarão mais comuns, portanto, dominá-las agora pode trazer recompensas no futuro.

---

<br/>
<br/>


<h2 align="center">📰 Informações e Ajuda</h2>


## 🗃 Histórico de lançamento

* 1.0
    * Estudando a possibilidade de adicionar novos conteúdos
* 0.5
    * Trabalho em progresso

## 📝 Meta

Gabriel de Jesus - [Meu Portfólio](https://www.gabrieldesenvolvedor.com/) - oi@gabrieldesenvolvedor.com

Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.

[https://github.com/devgabrieldejesus/html-semantic](https://github.com/devgabrieldejesus/)

## 🚀 Contribuição

1. Fork em (<https://github.com/devgabrieldejesus/html-semantic/fork>)
2. Crie seu branch de conteúdo (`git checkout -b meu-novo-conteudo`)
3. Faça commit de suas alterações (`git commit -am 'adiconando meu novo conteudo'`)
4. Empurre para o branch (`git push origin meu-novo-conteudo`)
5. Crie uma nova solicitação pull

**Depois que sua solicitação pull for mesclada**, você pode excluir seu branch com segurança.
