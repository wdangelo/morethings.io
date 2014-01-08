# morethings.io

morethings.io nasce a partir de uma ideia de compartilhamento de conteúdo atualizado e de qualidade para o público brasileiro.

## Quem faz?

A comunidade! Eu, você, ou qualquer um de nós. O projeto está aberto e feito em `jekyll`, portanto qualquer um pode escrever um post seguindo os passos abaixo e dar um pull request.

## Como rodar o projeto localmente?

Primeiramente você precisa ter o Ruby instalado na sua máquina. Se você tiver num Mac, isso já vai ajudar bastante. Se não tiver, no próprio [site do Ruby](https://www.ruby-lang.org/en/downloads/) explica bem direitinho como instalar em cada ambiente. Com isso, precisa também do jekyll. Caso não tenha ele instalado ainda:

``` bash
gem install jekyll
git clone git@github.com:luiztiago/morethings.io.git && cd morethings.io
bundle install
npm install
grunt
```

O grunt irá se responsabilizar em fazer todas as tasks necessárias para subir o ambiente e você poderá visualizar em http://localhost:4000/ se utiliza as configurações padrões.

## Como contribuir?

Primeiramente você deve forkar o projeto aqui pelo Github. Com isso, você deve configurar o ambiente como explicado anteriormente, porém deve usar o seu repositório forkado.

Para entender a estrutura de pastas, segue abaixo os detalhes.

``` bash
morethings.io/
├── _source/ #em resumo, o código-fonte
|    ├── _includes/
|         ├── browser-upgrade.html  #scripts para atualizar browser em < IE8
|         ├── disqus_comments.html  #js do disqus
|         ├── footer.html  #site footer
|         ├── head.html  #site head
|         ├── navigation.html #site nav
|         └── scripts.html  #jQuery, plugins, GA, etc.
|    ├── _layouts/
|         └── post.html  #articles layout
|         ├── page.html  #page layout
|         └── post.html  #post layout
|    ├── _posts/  # onde ficam os posts e você pode escrever novos posts
|    ├── assets/
|         ├── css/  #preprocessed less styles
|         ├── fonts/  #icon webfonts
|         ├── js/
|         |   ├── _main.js  #arquivo JavaScript main, plugin settings, etc
|         |   ├── plugins  #jQuery plugins
|         |   └── vendor/  #jQuery and Modernizr
|    └── less/
|    ├── images  #images dos posts e pages
|    ├── _config.yml  #Jekyll site options
|    ├── about.md  #about page
|    ├── articles.md  #lists all posts from latest to oldest
|    ├── index.html  #homepage. 10 latest posts
|    ├── tags.html  #lists all posts sorted by tag
|    └── sitemap.xml  #autogenerated sitemap for search engines
```

Para escrever um post, basta acrescentar um arquivo .markdown em _source/_posts como os outros arquivos modelos. Após isso, commita em seu respositório e pull request neste repositório. Done! :)
