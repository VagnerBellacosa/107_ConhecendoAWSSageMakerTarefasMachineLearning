# Por que usar Jupyter Notebook?

[![Suzana Viana](https://miro.medium.com/fit/c/56/56/2*zcFnpku6yneupkLCK01aXw.jpeg)](https://suzana-svm.medium.com/?source=post_page-----77d5a59b42a1-----------------------------------)

[Suzana Viana](https://suzana-svm.medium.com/?source=post_page-----77d5a59b42a1-----------------------------------)

[Sep 25, 2017·3 min read](https://suzana-svm.medium.com/por-que-usar-jupyter-notebook-77d5a59b42a1?source=post_page-----77d5a59b42a1-----------------------------------)







![img](https://miro.medium.com/max/2000/1*9bZvLan7WhcgWCiSGqvDKg.png)

O Jupyter Notebook é uma ferramenta de Literate Computing, extremamente eficientes, pois permitem unir código e texto. Assim cada funcionalidade pode ser explicada detalhadamente. Você também pode gerar gráficos “vivos” gerados em tempo real dentro da ferramenta.

O Jupyter Notebook é revolucionário, justamente por unir texto e código. Tenho usado muito para mapear e fazer anotações da minha pesquisa do mestrado e nenhuma ferramenta foi mais simples e eficiente.

Utilizando o Jupyter Notebook é possível descrever a questão da pesquisa, a abordagem do projeto, narrar as etapas importantes na análise. Sempre mesclando explicações e o código de programação. Esses documentos podem ser construídos de forma dinâmica, escrevendo porções do código da narrativa e do software, visualizando os resultados no relatório e continuando a análise com narração e código adicionais ou resumindo os resultados.

Um documento completo de programação também pode ser gerado com todos os componentes críticos do projeto: a descrição da proposta, o código de programação usado para realizá-lo, os resultados e uma discussão.

O Jupyter também tem sido muito utilizado em cursos e workshops de programação, por permitir que os participantes alterem parâmetros do código e rodem ali na própria máquina e já observem o resultado em tempo real.

# **Como instalar o Jupyter Notebook?**

Muito simples, meu caro. Baixe o pacote do Anaconda, que pode ser encontrado neste link: https://www.anaconda.com/download/

Após o download do Anaconda, abra o seu prompt de comando e execute `jupyter notebook`

Você verá imediatamente o nome do seu notebook, uma barra de menus, uma barra de ferramentas e uma célula de código vazia.

Selecione code caso deseje inserir algum código naquela célula, caso queira escrever alguma instrução selecione a opção Markdown.

Você pode criar quantas células você quiser e organiza-las como bem entender.

# **Gerando gráficos vivos no Jupyter Notebook:**

Veja abaixo um exemplo interessante de gráficos gerados em tempo real. Você pode copiar este código para o seu próprio notebook, brinque com os dados insira e remova-os e observe o resultado.

```
import matplotlib.pyplot as plt
%matplotlib inline

data = [1, 2, 5, 10, 12, 15]
plt.figure()
plt.plot(data)
```

O resultado é um gráfico como este:

![img](https://miro.medium.com/max/60/1*YZKawNwJZvAkHq01cgd0fw.png?q=20)

![img](https://miro.medium.com/max/687/1*YZKawNwJZvAkHq01cgd0fw.png)

# **Dicas**

1. Crie um novo notebook para cada versão importante de seu projeto. Assim é possível entender a evolução do projeto como um todo.
2. Tenha atenção ao criar nomes para seus notebooks. Utilize algum tipo de padrão como a data + mês + ano + nome do notebook. Evite utilizar v01,v02,v03, pois estes nomes não transmitem nenhuma informação sobre o conteúdo ou alteração do notebook.
3. Faça da documentação do projeto uma rotina: É muito fácil escrever texto e código com o Jupyter Notebook, tenha disciplina e documente todas as alterações de seu projeto como um hábito.
4. Prefira utilizar gráficos vivos ou seja gerados através de código no Jupyter Notebook do que imagens de gráficos estáticas.
5. A integração Jupyter Notebook e plataforma Latex ainda não funciona da melhor maneira. Não utilize este tipo de exportação de arquivos texto.

Este artigo é o primeiro de uma série sobre o Jupyter Notebook, fique de olho. Caso este artigo tenha sido útil, deixe o seu comentário contando a sua experiência! :)