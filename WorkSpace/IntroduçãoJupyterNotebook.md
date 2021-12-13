# Introdução ao Jupyter Notebook

## Let's Code | 15 MAI 2019

![Post image - Introdução ao Jupyter Notebook](https://s3-sa-east-1.amazonaws.com/letscode-ghost-bucket/2021/01/Imagens_blog_45.jpg)

## Introdução

### Sobre os arquivos *notebooks*

Um documento do tipo [*notebook*](https://en.wikipedia.org/wiki/Notebook_interface) é um documento virtual que permite a execução de códigos de uma linguagem de programação juntamente com ferramentas para edição de textos comuns; ou seja, além das rotinas usuais de programação, o usuário pode documentar todo o processo de produção do código. Dessa forma, o notebook permite uma maneira interativa de programar.
Os notebooks também oferecem uma programação mais dinâmica, oferecendo ao usuário o *output* imediato do código; não havendo, assim, a necessidade de compilar ou executar todo o documento.

## Jupyter

O *Jupyter* *Notebook* é um interfarce gráfica que permite a edição de *notebooks* em um navegador web, tais como Google Chrome ou Firefox. O nome Jupyter é um acrônimo criado a partir das linguagens de programação que inicialmente foram aceitas pelo Projeto Jupyter: **Julia**, Python e **R**. Além dessas, hoje, o [Projeto Jupyter](https://jupyter.org/) suporta também C++, Ruby, Fortran e outras.

## Primeiros passos

### Instalação

As principais maneiras de instalar o Jupyter Notebook para a linguagem Python é com o **pip** ou através da distribuição Anaconda. A instalação com o pip segue a rotina simples de instalação de módulos e bibliotecas do python: **pip install jupyter<code>.</code>**

![img](https://blog.letscode.com.br/content/images/2019/05/pip_jupyter.gif)

Já no Anaconda, a instalação padrão da distribuição já inclui o Jupyter Notebook.

### Abrindo o Jupyter

Se você instalou o Jupyter pelo **pip**, você pode abri-lo no terminal: **jupyter notebook**.

![img](https://blog.letscode.com.br/content/images/2019/05/abrir_jupyter.gif)

Esse comando irá abrir a janela inicial do Jupyter no seu navegador padrão. Caso você deseje abrir em outro navegador (ou estiver abrindo o Jupyter de um servidor remoto), você pode usar o endereço fornecido no terminal:

![img](https://blog.letscode.com.br/content/images/2019/05/endereco.gif)

Caso você instalou a distribuição Anaconda, é possível abrí-lo como um programa qualquer do Windows:

![img](https://blog.letscode.com.br/content/images/2019/05/abrindo_jupyter_anaconda.gif)

Feito isso, você será direcionado à página inicial do Jupyter:

![img](https://blog.letscode.com.br/content/images/2019/05/pagina_ini_1.gif)

Com essa página, além de servir como um navegador simples de diretórios, você pode abrir notebooks já existentes, criar novos notebooks, abrir terminais do sistema, criar e deletar diretórios, e criar e editar arquivos de texto (muito útil para visualizar o separador do **.csv** antes de importá-lo como um *dataframe* do Pandas, por exemplo).

### Abrindo ou editando um notebook

Para criar um notebook selecione o botão ***new\*** no canto superior esquerdo da página:

![img](https://blog.letscode.com.br/content/images/2019/05/abrindo_note_1.gif)

O Jupyter dará a opção de você criar um notebook cuja execução será suportada pelo kernel de uma linguagem, no caso da figura abaixo o Python 3:

![img](https://blog.letscode.com.br/content/images/2019/05/abrindo_note_2.gif)

Porém, se você tiver outros kernels instalados, como o Python 2 ou o R, por exemplo, você também poderá escolhe-los:

![img](https://blog.letscode.com.br/content/images/2019/05/dashboard.png)

Para abrir um notebook já existente, basta procurar por um arquivo do tipo .ipynb (de Ipython Notebook) com o auxílio da pasta inicial do Jupyter:

![img](https://blog.letscode.com.br/content/images/2019/05/abrindo_note_3.gif)

Pronto! Agora você pode começar a programar e documentar seu trabalho num novo notebook, ou continuar um trabalho já começado:

![img](https://blog.letscode.com.br/content/images/2019/05/abrindo_note_5.gif)

![img](https://blog.letscode.com.br/content/images/2019/05/abrindo_note_4.gif)

## Dicas Gerais de Uso

### Alterando o nome do notebook

Por padrão o Jupyter nomeia automaticamente os notebooks na criação. Mas, você pode mudar o nome deles no header da página:

![img](https://blog.letscode.com.br/content/images/2019/05/nome_note.gif)

### Modos das células

Uma célula do Jupyter pode assumir dois estados: modo de **edição** ou o modo de **comando**. No modo de edição, o usuário irá apenas editar o conteúdo da célula, seja esse um código ou um texto *markdown*, por exemplo. Já o modo comando permite o usuário manipular a célula: executar o código ou compilar o texto *markdown*, deletar a célula, copiar a célula, recortar a célula, criar uma nova célula, mudar a célula para aceitar código ou para aceitar *markdown*, fundir duas ou mais células, etc.

A célula quando estiver em modo de edição terá uma margem verde:

![img](https://blog.letscode.com.br/content/images/2019/05/edit_mode.png)

Ao passo que uma célula em modo de comando terá margem azul:

![img](https://blog.letscode.com.br/content/images/2019/05/command_mode.png)

## Tipos de células

Existem três tipos de células no Jupyter: código, *markdown* e raw NBconvert. As células de código são aquelas que permitem a execução de códigos de uma determinada linguagem. As células do tipo *markdown* permitem a utilização da linguagem de marcação *Markdown*, que permite a edição de textos. Já as raw NBconvert permitem a execução de códigos externamente, tais como o LaTeX.

A célula de código sempre se apresentará da seguinte forma:

![img](https://blog.letscode.com.br/content/images/2019/05/celula_1.gif)

Após a inserção de um código em uma célula do tipo código, pode-se executá-la com um botão de execução na própria célula, na *toolbar* ou através do teclado (segurando **Ctrl + Enter<code>).</code>**

![img](https://blog.letscode.com.br/content/images/2019/05/celula_2.gif)

![img](https://blog.letscode.com.br/content/images/2019/05/celula_3.gif)

Enquanto a célula estiver “rodando”, um asterisco irá aparecer no seu canto direito para indicar que a célula ainda está executando o código:

![img](https://blog.letscode.com.br/content/images/2019/05/celula_6.gif)

Após a execução da célula, aparecerá um número indicando a da ordem de execução:

![img](https://blog.letscode.com.br/content/images/2019/05/celula_4.gif)Logo abaixo da célula vem o *output* da execução.

## Novas células

Dada qualquer célula no modo de comando, pode-se acrescentar uma nova célula acima ou abaixo dessa célula em questão indo em *insert* e clicando em *insert cell above* (ou apertando a tecla a) ou *insert cell bellow* (ou apertando a tecla b), respectivamente.

![img](https://blog.letscode.com.br/content/images/2019/05/inserindo_cell.gif)

## Parando a execução ou interrompendo o kernel

As vezes executamos algo indesejado. Para consertar isso, podemos interromper a execução de uma determinada célula do Jupyter:
![img](https://blog.letscode.com.br/content/images/2019/05/interrompendo.gif)

Quando a célula é interrompida, uma mensagem de erro é exibida: KeyboardInterrupt.

Outro tipo de acontecimento indesejado é quando o kernel trava. Quando isso ocorre, devemos dar um restart na execução do kernel. Há várias opções aqui:

- um simples restart: para o kernel. Todas as construções do programa que estavam disponíveis na memória são apagadas;
- restart & clear outputs: performa o restart e limpa os resultados de cada uma das células de código;
- restart & run all: performa o restart e roda as células na ordem de leitura do documento (de cima para baixo)

Na última opção (*restart & run all*) é preciso tomar um cuidado: o Jupyter permite que uma célula seja executada acima de outra, mesmo que essa acima necessite de informações que estão abaixo. Porém, quando o kernel é interrompido, a ordem que prevalesse é a de leitura.
No exemplo abaixo, a ordem de execução prevalece: sabemos que a célula marcada com [1] foi executada antes da célula marcada com [2]. Porém se executamos o *restart & run all*, teremos um desastre!

![img](https://blog.letscode.com.br/content/images/2019/05/ordem_1.gif)

![img](https://blog.letscode.com.br/content/images/2019/05/ordem_2.gif)

## Atalhos do teclado

Os seguintes atalhos estão implementados por default para célula no modo comando:

- **Ctrl-Enter**: executa a célula;
- **Shift-Enter**: executa a célula e cria uma nova célula abaixo no modo de comando;
- **Alt-Enter**: executa a célula e cria uma nova célula abaixo no modo de edição;
- **Y**: muda a célula para o tipo código;
- **M**: muda a célula para o tipo *markdown*;
- **A**: insere célula acima;
- **B**: insere célula abaixo;
- **X**: recorta a célula;
- **C**: copia a célula;
- **V**: cola a célula do *clipboard* abaixo;
- **shift-V**: cola a célula do *clipboard* acima;
- **D, D**: deleta uma célula;
- **Z**: desfaz o apagar célula; e
- **L**: ativa a enumeração das linhas.

Os seguintes atalhos estão implementados por default para célula no modo de edição:

- **Tab**: autocompleta durante a digitação; e
- **Shift-Tab**: abre uma minijanela com parte da documentação sobre a parte do código durante a documentação.

A autocompletação durante a digitação permite também que o usuário escolha o que deve ser completado caso haja mais de uma opção:
![img](https://blog.letscode.com.br/content/images/2019/05/autocompl.gif)

O **shift-Tab** é muito útil quando se esquece, por exemplo, os argumentos de execução:

![img](https://blog.letscode.com.br/content/images/2019/05/autocompl_2.gif)

## Comandos do Jupyter

O Jupyter tem diversos comandos próprios que podem acessados com **%** na célula. Por exemplo, **%pwd** mostra o endereço do diretório no qual o notebook se encontra.

### Tempo de execução

O comando **%time** exibe o tempo de execução da célula em que o comando foi executado.

![img](https://blog.letscode.com.br/content/images/2019/05/matplot_4.gif)

### Matplotlib

Diferente do que é feito na linha de comando, o Jupyter não precisa do **plt.show()** para mostrar a figura. Ao executar **%matplotlib inline** em uma das células (só é necessário executá-lo uma vez), a figura é mostrada na própria página, no *output*. Esse comando é necessário, pois do contrário o Jupyter ira exibir apenas a representação do objeto:

![img](https://blog.letscode.com.br/content/images/2019/05/matplot_1.gif)

Após executar o **%matplotlib inline**, o gráfico é exibido abaixo do output:

![img](https://blog.letscode.com.br/content/images/2019/05/matplot_2.gif)

O comando **%matplotlib notebook** permite a criação de uma gráfico interativo, parecido com a janela nativa do Matplotlib:

![img](https://blog.letscode.com.br/content/images/2019/05/matplot_3.gif)

**Porém, isso deixa o programa mais lento.**

## Interagindo com o sistema operacional

Podemos invocar comandos do sistema operacional sem sair do Jupyter. Por exemplo, **dir** é um comando do Windows que lista o conteúdo de um diretório. Assim, podemos invocá-lo com no Jupyter executando o comando **!dir** em alguma célula:

![img](https://blog.letscode.com.br/content/images/2019/05/dir.gif)

Um aplicação muito útil é executar o **pip** direto no Jupyter:

![img](https://blog.letscode.com.br/content/images/2019/05/pip.gif)

## Conclusão

Vários outros truques e macetes de uso podem ser encontrados na documentação do Jupyter:

https://jupyter-notebook.readthedocs.io/en/stable/