# Jupyter Notebook: Exemplos de Códigos e Como Usar

![Jupyter Notebook Logo](https://www.alura.com.br/artigos/assets/conhecendo-o-jupyter-notebook/img-01.png)

![João Vitor de Miranda](https://github.com/Joaovmir.png?size=200&d=https%3A%2F%2Fwww.gravatar.com%2Favatar%2F2cdc9f19f0cdbd5250eaabade88effee.png%3Fr%3DPG%26size%3D200x200%26date%3D2021-12-12%26d%3Dhttps%253A%252F%252Fcursos.alura.com.br%252Fassets%252Fimages%252Fforum%252Favatar_j.png)

João Vitor de Miranda

24/05/2021

COMPARTILHE

- 
- 
- 
- 

[![img](https://www.alura.com.br/assets/api/formacoes/categorias/data-science.svg)Esse artigo faz parte daFormação Data Science](https://www.alura.com.br/formacao-data-science)



No mundo da programação, estamos familiarizados com editores de textos ou IDEs que facilitam o trabalho da escrita de códigos. São inúmeros os softwares que podemos escolher que vão atender às necessidades.

É de se esperar que, ao trabalhar com ciência de dados, utilizemos alguma dessas IDEs, já que a programação está fortemente ligada à área de ciência de dados. Mas a forma tradicional de escrever o código, em um único bloco com comentários ao longo do caminho, traz algumas desvantagens se comparado aos notebooks utilizados em projetos de ciência de dados.

#### O que são Notebooks?

Um Notebook se parece com um caderno, onde será escrito uma história. Essa história é narrada em partes e segue um fluxo lógico, desde a introdução até a conclusão. Como os projetos de ciência de dados envolvem resolver um problema de negócio, precisamos

escrever uma história com os objetivos, possíveis soluções do problema e a conclusão que chegamos através da exploração dos dados.

Temos a opção de criar blocos de texto e blocos de código no Notebook. Cada bloco é conhecido como uma célula do Notebook.

Através dos blocos de texto, podemos explicar o contexto, o objetivo do nosso projeto, o conhecimento que está sendo extraído dos dados e as conclusões, ou seja, as possíveis soluções para o problema que estamos tentando resolver, ou até mesmo se ainda não conseguimos chegar a nenhuma solução.

Também é possível explorar o conjunto de dados, fazer o tratamento e limpeza, criar gráficos representativos, entre outras coisas. As saídas ou resultados de cada um desses blocos de código podem ser verificados logo abaixo de cada um dos códigos. Além disso, não é necessário rodar todo o seu código anterior todas as vezes, uma vez que o processo fica armazenado na memória e as células vão funcionar de uma forma um pouco independente.

#### Jupyter Notebook

O **Jupyter Notebook** é um ambiente que oferece essa abordagem de Notebooks, com um visual simples e muito fácil de utilizar.

Vamos começar pela sua instalação.

Uma possibilidade seria instalar o Anaconda, que é uma plataforma que disponibiliza. além do **Jupyter Notebook**, alguns outros ambientes como JupyterLab e Spyder.Também dá a possibilidade de criar ambientes virtuais e já instala a linguagem Python e as principais bibliotecas que serão utilizadas para desenvolver projetos em ciência de dados, como a biblioteca numpy e pandas.

Para realizar a instalação dessa forma, basta ir até o [site oficial](https://www.anaconda.com/products/individual) e escolher o instalador de acordo com o sistema operacional.

![Página de download do Anaconda mostrando as opções Windows, MacOs e Linux](https://www.alura.com.br/artigos/assets/conhecendo-o-jupyter-notebook/img-02.png)

Assim que a instalação for concluída, ao abrirmos o Anaconda Navigator, o Jupyter Notebook estará pronto para uso.

![Página inicial do Anaconda Navigator](https://www.alura.com.br/artigos/assets/conhecendo-o-jupyter-notebook/img-03.png)

Outra forma de instalar é através do pip (Gerenciador de pacotes do python). Nesse caso, precisamos instalar o Python em nosso computador e através do terminal do sistema operacional, digitamos o comando:

```
pip install jupyter
```

Caso opte pela segunda forma e não tenha o Python instalado, pode conseguir a versão mais atual no site oficial: https://www.python.org/

O Jupyter Notebook é aberto no navegador, mas funciona localmente. A página inicial dá acesso às pastas do nosso sistema, onde conseguimos abrir Notebooks criados anteriormente e criar novos Notebooks.

![Página de navegação do Jupyter Notebook mostrando as pastas do sistema. No canto superior direito há a opção de criação de notebook](https://www.alura.com.br/artigos/assets/conhecendo-o-jupyter-notebook/img-04.png)

Ao criarmos um novo Notebook, temos acesso às ferramentas de maneira rápida. Na imagem a seguir podemos ver **células** do tipo Markdown, **células** de código e saída dos respectivos códigos, inclusive de gráficos. Temos acesso aos botões de criar novas **células**, rodar o código, mudar o tipo de célula e diversas outras funcionalidades.

![Página principal do Jupyter Notebook, com tipos de célula e exemplos](https://www.alura.com.br/artigos/assets/conhecendo-o-jupyter-notebook/img-05.png)

Há ainda alguns **atalhos** que agilizam o processo. Dentre eles, os mais usados:

- ‘Ctrl + Enter’ : Executa a célula selecionada
- ‘Shift + Enter’ : Executa a célula selecionada e seleciona a próxima célula. Se for a - última célula do Notebook, uma nova célula é criada automaticamente.
- ‘a’ : Cria uma célula antes da célula selecionada
- ‘b’ : Cria uma célula depois da célula selecionada
- ‘d + d : Deleta a célula selecionada
- ‘t’ : Transforma a célula em uma célula de código
- ‘m’ : Transforma a célula em uma célula do tipo Markdown

Repare que para usar alguns dos comandos, a célula precisa estar **selecionada** mas não pode estar sendo editada, caso contrário estaríamos digitando dentro da célula.

![Célula do Jupyter Notebook selecionada, fora edição em leitores de tela](https://www.alura.com.br/artigos/assets/conhecendo-o-jupyter-notebook/img-06.png)

![Célula do Jupyter Notebook sendo editada, edição multilinha nos leitores de tela](https://www.alura.com.br/artigos/assets/conhecendo-o-jupyter-notebook/img-07.png)

#### Alternativas ao Jupyter

Apesar de ser muito utilizado, o **Jupyter Notebook** não é o único a oferecer Notebooks. Nós podemos utilizar o Spyder, o RStudio, o JupyterLab (uma evolução do Jupyter Notebook) e o Google Collaboratory, conhecido também como **Google Colab**. Podemos também rodar o Jupyter Notebook em uma IDE como o VSCode.

O **JupyterLab** é um ambiente mais avançado que possibilita personalizações e acesso a outras ferramentas que não estão presentes no Jupyter Notebook padrão. Para saber mais a respeito dele, leia nosso artigo [Conhecendo o JupyterLab](https://www.alura.com.br/artigos/conhecendo-jupyterlab).

Uma diferença entre o [**Google Colab**](https://colab.research.google.com/) e o Jupyter Notebook é a facilidade de utilizá-lo sem a necessidade de instalar algo em seu computador. Ele roda diretamente da nuvem, bastando acesso à internet e uma conta Google.

É um ambiente muito amigável e logo ao abrir pela primeira vez ele te dá as boas-vindas com um pequeno tutorial de utilização.

![Página inicial do Google Colab com tutorial](https://www.alura.com.br/artigos/assets/conhecendo-o-jupyter-notebook/img-08.png)

Para saber mais sobre o **Google Colab**, leia nosso artigo [Google Colab: o que é e como usar?](https://www.alura.com.br/artigos/google-colab-o-que-e-e-como-usar)

Pronto! Agora com toda essa informação você já pode começar a utilizar um Notebook para os seus projetos de Ciência de Dados e deixar de digitar tudo em um único bloco de código. Verá como é muito mais prático e agradável!