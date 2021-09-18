# Perguntas frequentes sobre o Amazon SageMaker

## Geral

**P: O que é o Amazon SageMaker?**

O Amazon SageMaker é um serviço totalmente gerenciado que fornece a todos os desenvolvedores e cientistas de dados a capacidade de criar, treinar e implantar modelos de machine learning (ML) rapidamente. O SageMaker remove o trabalho pesado de cada etapa do processo de machine learning para facilitar o desenvolvimento de modelos de alta qualidade.

**P: Em quais regiões o Amazon SageMaker está disponível?**

Para obter uma lista das regiões da AWS com suporte ao Amazon SageMaker, acesse a [Tabela de regiões da AWS](https://aws.amazon.com/pt/about-aws/global-infrastructure/regional-product-services/) para obter informações sobre toda a infraestrutura global da AWS. Para obter mais informações, consulte [Regiões e endpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html#machinelearning_region) na referência geral da AWS.

**P: Qual é a disponibilidade dos serviços do Amazon SageMaker?**

O Amazon SageMaker foi projetado para oferecer alta disponibilidade. Não há janelas de manutenção nem tempos de inatividade programados. As APIs do SageMaker são executadas nos datacenters comprovados e de alta disponibilidade da Amazon, com replicação da pilha de serviços configurada em três unidades em cada região da AWS para proporcionar tolerância a falhas em caso de falha de servidor ou interrupção de zona de disponibilidade.

**P: Como o Amazon SageMaker protege meu código?**

O Amazon SageMaker armazena código em volumes de armazenamento de Machine Learning, protegidos por security groups e, opcionalmente, criptografados quando ociosos.

**P: Quais as medidas de segurança implementadas no Amazon SageMaker?**

O Amazon SageMaker garante que os artefatos de modelos de machine learning e outros artefatos de sistema sejam criptografados quando em trânsito e quando ociosos. As solicitações para a API e o console do SageMaker são realizadas em uma conexão segura (SSL). Você envia [funções do AWS Identity and Access Management](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html) ao SageMaker para fornecer permissões de acesso a recursos em seu nome para fins de treinamento e implantação. Você pode usar buckets do Amazon S3 criptografados para modelar artefatos e datas, bem como passar uma chave do KMS a notebooks, trabalhos de treinamento e endpoints do SageMaker, para criptografar o volume associado de armazenamento de machine learning. O Amazon SageMaker também oferece suporte à Amazon Virtual Privacy Cloud (VPC) e ao AWS PrivateLink.

**P: O Amazon SageMaker usa ou compartilha modelos, dados de treinamento ou algoritmos?**

O Amazon SageMaker não usa nem compartilha modelos de clientes, dados de treinamento ou algoritmos. Sabemos que os clientes se preocupam muito com a privacidade e a segurança dos dados. É por isso que a AWS oferece a você a propriedade e o controle sobre o seu conteúdo por meio de ferramentas simples e avançadas que permitem determinar onde o conteúdo será armazenado, proteger o conteúdo ocioso e em trânsito e gerenciar o acesso de seus usuários a serviços e recursos da AWS. Também implementamos controles técnicos e físicos responsáveis e sofisticados, projetados para evitar o acesso e a divulgação não autorizados do seu conteúdo. Como cliente, você mantém a propriedade sobre o seu conteúdo e seleciona quais serviços da AWS podem processar, armazenar e hospedar esse conteúdo. Não acessamos seu conteúdo para qualquer finalidade sem o seu consentimento.

**P: Como sou cobrado pelo uso do Amazon SageMaker?**

Você paga pelos recursos de computação, armazenamento e processamento de dados de Machine Learning usados para hospedar o notebook, treinar o modelo, executar previsões e registrar as saídas. O Amazon SageMaker permite selecionar o número e o tipo de instâncias usadas para o notebook hospedado, para treinamento e para hospedagem de modelos. O pagamento é feito conforme o uso. Não há taxas mínimas nem compromissos antecipados. Consulte a [página de definição de preço do Amazon SageMaker](https://aws.amazon.com/pt/sagemaker/pricing/) para obter detalhes.

**P: Como otimizar os custos do Amazon SageMaker, por exemplo, como detectar e interromper recursos ociosos para evitar alterações desnecessárias?
**

Há diversas práticas recomendadas que você pode adotar para otimizar a utilização de recursos do Amazon SageMaker. Algumas abordagens envolvem otimizações de configurações, enquanto outras envolvem soluções programáticas. [Esta publicação de blog](https://aws.amazon.com/pt/blogs/machine-learning/right-sizing-resources-and-avoiding-unnecessary-costs-in-amazon-sagemaker/) oferece um guia completo sobre esse conceito, com tutoriais visuais e amostras de código.

**P: E se eu tiver o meu próprio ambiente de bloco de anotações, treinamento ou hospedagem?**

O Amazon SageMaker oferece um fluxo de trabalho completo e abrangente, mas você pode continuar a usar suas ferramentas atuais com o SageMaker. É possível transferir facilmente os resultados de cada fase para dentro e para fora do SageMaker para atender a requisitos de negócios.

**P: O R é suportado pelo Amazon SageMaker?
**

Sim, o R é suportado pelo Amazon SageMaker. Você pode usar o R nas instâncias do SageMaker Notebook, que incluem um kernel R pré-instalado e a biblioteca de [reticulação](https://rstudio.github.io/reticulate/). A reticulação oferece uma interface R para o Amazon SageMaker Python SDK, permitindo que os profissionais de machine learning construam, treinem, sintonizem e implantem modelos R. 

**P: Como eu posso verificar desequilíbrios em meu modelo?**

O [Amazon SageMaker Clarify](https://aws.amazon.com/pt/sagemaker/clarify/) ajuda a aprimorar a transparência do modelo detectando tendências estatísticas ao longo de todo o fluxo de trabalho de ML. O SageMaker Clarify verifica os desequilíbrios durante a preparação dos dados, após o treinamento e continuamente ao longo do tempo, além de incluir também ferramentas para ajudar a explicar os modelos de ML e suas previsões. As conclusões podem ser compartilhadas por meio de relatórios de explicabilidade.

**P: Que tipos de tendências o Amazon SageMaker Clarify detecta?
**
Medir tendências em modelos de ML é uma primeira etapa na mitigação de tendências. As tendências podem ser medidas antes e depois do treinamento, bem como para inferência para um modelo implantado. Cada medição de tendência corresponde a uma noção diferente de justiça. Mesmo considerando que noções simples de justiça levam a várias medições diferentes aplicáveis em vários contextos. É necessário escolher noções de tendências e métricas que sejam válidas para a aplicação e a situação sob investigação. O SageMaker atualmente é compatível com a computação de diferentes métricas de tendências para treinamento de dados (como parte da preparação de dados do SageMaker), para o modelo treinado (como parte do SageMaker Experiments) e para inferência para um modelo implantado (como parte do SageMaker Model Monitor). Por exemplo, antes do treinamento, fornecemos métricas para a verificação se os dados de treinamento são representativos (ou seja, se um grupo está sub-representado) e se há diferenças na distribuição de rótulos entre os grupos. Após o treinamento ou durante a implantação, nossas métricas podem ser úteis para medir se (e por quanto) a performance do modelo difere entre os grupos. Por exemplo, podemos iniciar comparando as taxas de erro (a probabilidade da previsão de um modelo diferir do rótulo verdadeiro) ou avaliar com ainda mais precisão (a probabilidade de uma previsão positiva ser correta) e a recuperação (a probabilidade de o modelo rotular corretamente um exemplo positivo).

**P: Como o Amazon SageMaker Clarify aprimora a explicabilidade do modelo?
**
O Amazon SageMaker Clarify é integrado aos SageMaker Experiments para fornecer um gráfico de importância do recurso, detalhando a importância de cada entrada para o processo de tomada de decisão geral do seu modelo após o modelo ter sido treinado. Esses detalhes podem ajudar a identificar se uma determinada entrada do modelo exerce mais influência do que deveria no comportamento geral do modelo. O SageMaker Clarify também oferece explicações para previsões individuais disponíveis via API.
 

**P: O que é o Amazon SageMaker Studio?**

O Amazon SageMaker Studio fornece uma interface visual única baseada na Web em que você pode executar todas as etapas de desenvolvimento de ML. O SageMaker Studio fornece acesso, controle e visibilidade completos em cada etapa necessária para criar, treinar e implantar modelos. Você pode fazer a transferência rápida de dados, criar novos blocos de anotações, treinar e ajustar modelos, alternar entre as etapas para ajustar experimentos, comparar resultados e implantar modelos na produção em um único local, tornando-se muito mais produtivo. Todas as atividades de desenvolvimento de ML, incluindo blocos de anotações, gerenciamento de experimentos, criação, depuração e perfilagem automática de modelos e detecção de desvio de modelo, podem ser executadas na interface visual unificada do SageMaker Studio.

**P: Como funciona a definição de preço do Amazon SageMaker Studio?**

Não há custo adicional para o uso do Amazon SageMaker Studio. Você paga apenas as taxas de computação e armazenamento subjacentes referentes aos serviços que utiliza no Amazon SageMaker Studio.

**P: Em quais regiões há suporte ao Amazon SageMaker Studio?**

Você pode encontrar as regiões onde há suporte ao Amazon SageMaker Studio na [documentação aqui](https://docs.aws.amazon.com/sagemaker/latest/dg/regions-quotas.html).

## Machine learning de código de baixo nível

**P: O que é o Amazon SageMaker Autopilot?**

O [Amazon SageMaker Autopilot](https://aws.amazon.com/sagemaker/autopilot/) é o primeiro recurso de machine learning automatizado do setor que oferece controle e visibilidade completos dos seus modelos de ML. O SageMaker Autopilot inspeciona dados brutos, aplica processadores de recursos, escolhe o melhor conjunto de algoritmos, treina e ajusta vários modelos, monitora a performance e os classifica com base na performance, tudo de maneira automática e com apenas alguns cliques. O resultado é o modelo com melhor performance que você pode implantar em uma fração do tempo normalmente necessário para treinar o modelo. Você obtém total visibilidade de como o modelo foi criado e o que ele contém e o SageMaker Autopilot se integra ao Amazon SageMaker Studio. Você pode explorar até 50 modelos diferentes gerados pelo SageMaker Autopilot no SageMaker Studio, facilitando a escolha do melhor modelo para o seu caso de uso. O SageMaker Autopilot pode ser usado por pessoas sem experiência em machine learning para produzir um modelo facilmente. Pode ser usado também por desenvolvedores experientes para desenvolver um modelo de referência em que as equipes podem iterar ainda mais.

**P: Quais algoritmos integrados são permitidos no Amazon SageMaker Autopilot?**

O Amazon SageMaker Autopilot oferece suporte a 2 algoritmos integrados ao ser executado: XGBoost e Linear Learner.

**P: Posso interromper um trabalho do Amazon SageMaker Autopilot manualmente?**

Sim. Você pode interromper um trabalho a qualquer momento. Quando um trabalho do Amazon SageMaker Autopilot é interrompido, todas as avaliações em andamento são interrompidas e nenhuma nova avaliação é iniciada.

**P: Como posso começar a usar o Amazon SageMaker rapidamente?
**
O Amazon SageMaker JumpStart ajuda você a começar a usar machine learning de forma rápida e fácil. O SageMaker JumpStart oferece um conjunto de soluções para os casos de uso mais comuns que podem ser implantados prontamente com apenas alguns cliques. As soluções são totalmente personalizáveis e mostram o uso de modelos do AWS CloudFormation e arquiteturas de referência para que você possa acelerar sua jornada de machine learning. O SageMaker JumpStart também suporta a implantação em um clique e ajuste fino de mais de 150 modelos de origem aberta populares, como transformador, detecção de objetos e modelos de classificação de imagem.
 

**P: Que modelos de código aberto são suportados no Amazon SageMaker JumpStart?
**
O Amazon SageMaker JumpStart inclui mais de 150 modelos de código aberto pré-treinados do PyTorch Hub & TensorFlow Hub. Para tarefas de visão, como classificação de imagens e detecção de objetos, você pode aproveitar modelos como ResNet, MobileNet e Single-Shot Detector (SSD). Para tarefas de texto, como classificação de frases, classificação de textos e respostas a perguntas, você pode usar modelos como BERT, RoBERTa e DistilBERT.



**P: Que soluções já vêm previamente integradas ao Amazon SageMaker Jumpstart?**

O SageMaker JumpStart inclui soluções que são pré-configuradas com todos os serviços da AWS necessários para lançar uma solução em produção. As soluções são totalmente personalizáveis para que você possa modificar facilmente para se adequar ao caso de uso e ao conjunto de dados específicos. Você pode usar soluções para mais de 15 casos de uso, incluindo previsão de demanda, detecção de fraudes e manutenção preditiva, bem como implementar soluções prontamente com apenas alguns cliques. Para obter mais informações sobre todas as soluções disponíveis, visite a página de [conceitos básicos](https://aws.amazon.com/pt/sagemaker/getting-started/) do SageMaker.
 

**P: Como a definição de preços do Amazon SageMaker funciona?
**
Você é cobrado pelos serviços da AWS lançados a partir do SageMaker JumpStart, como trabalhos de treinamento e endpoints, com base na [definição de preço do SageMaker.](https://aws.amazon.com/sagemaker/pricing/) Não há custo adicional para o uso do Amazon SageMaker JumpStart.

## Fluxos de trabalho de machine learning

**P: Como posso fazer um pipeline CI/CD com o Amazon SageMaker?**

O [Amazon SageMaker Pipelines](https://aws.amazon.com/sagemaker/pipelines/) ajuda você a criar fluxos de trabalho de ML totalmente automatizados, da preparação de dados até a implantação do modelo, para que seja possível escalar para milhares de modelos de ML em produção. O SageMaker Pipelines é fornecido com um SDK de Python que se conecta ao SageMaker Studio para que você possa aproveitar as vantagens de uma interface visual para construir cada etapa do fluxo de trabalho. Em seguida, usando uma única API, você pode conectar cada etapa para criar um fluxo de trabalho fim a fim. O SageMaker Pipelines cuida do gerenciamento de dados entre as etapas, empacotando as receitas de código e orquestrando sua execução, reduzindo meses de codificação a algumas horas. Sempre que um fluxo de trabalho é executado, um registro completo dos dados processados e das ações realizadas é mantido para que os cientistas de dados e desenvolvedores de ML possam depurar problemas rapidamente.

**P: Como posso ver todos os meus modelos treinados para escolher o melhor modelo para passar à produção?
**
O Amazon SageMaker Pipelines oferece um repositório central de modelos treinados, chamado de registro de modelos. Você pode descobrir modelos e acessar o registro de modelos visualmente por meio do SageMaker Studio ou programaticamente por meio do SDK de Python, facilitando a escolha do modelo desejado para implantar na produção.

**P: Quais componentes do Amazon SageMaker podem ser adicionados aos pipelines do Amazon SageMaker?
**
Os componentes disponíveis por meio do Amazon SageMaker Studio, incluindo o SageMaker Clarify, SageMaker Data Wrangler, SageMaker Feature Store, SageMaker Experiments, SageMaker Debugger e SageMaker Model Monitor, podem ser adicionados ao SageMaker Pipelines.

**P: Como faço para monitorar os componentes do meu modelo em todo o fluxo de trabalho de ML?
**
O Amazon SageMaker Pipelines rastreia automaticamente todos os constituintes do modelo e mantém uma trilha de auditoria de todas as alterações, eliminando o rastreamento manual e pode ajudar você a atingir as metas de conformidade. Você pode rastrear dados, códigos, modelos treinados e muito mais com o SageMaker Pipelines.

**P: Como funciona a definição de preços do Amazon SageMaker Pipelines?
**
Não há cobrança adicional pelo Amazon SageMaker Pipelines. Você paga apenas pela computação subjacente ou por quaisquer serviços separados da AWS que usar dentro do SageMaker Pipelines.

**P: Posso usar o Kubeflow com o Amazon SageMaker?
**
Sim. O Amazon SageMaker Components para Kubeflow Pipelines consiste em plugins de código aberto que permitem usar o Kubeflow Pipelines para definir fluxos de trabalho de ML, bem como usar o SageMaker para as etapas de rotulagem, treinamento e inferência de dados. O Kubeflow Pipelines é um complemento do Kubeflow que permite criar e implantar pipelines completos de ML fim a fim, portáveis e dimensionáveis. No entanto, quando usam o Kubeflow Pipelines, as equipes de operações de ML precisam gerenciar um cluster do Kubernetes com instâncias de CPU e GPU, bem como manter uma alta utilização constante para reduzir os custos operacionais. A maximização de um cluster entre equipes de ciência de dados é um desafio e adiciona sobrecarga operacional à equipe de operações de ML. Como alternativa ao cluster do Kubernetes otimizado para ML, o Amazon SageMaker Components para Kubeflow Pipelines permite aproveitar recursos avançados do SageMaker, como rotulagem de dados, trabalhos gerenciados de ajuste de hiperparâmetros e de treinamento distribuído em grande escala, implantação segura e dimensionável de modelos com um clique e treinamento econômico usando instâncias spot do Amazon EC2, sem necessidade de configurar e gerenciar clusters do Kubernetes especificamente para a execução de trabalhos de machine learning.

**P: Como a definição de preços do Amazon SageMaker Components para Kubeflow Pipelines funciona?
**
Não há cobrança adicional pelo uso do Amazon SageMaker Components para Kubeflow Pipelines.
 

## Preparar dados

**P: Como o Amazon SageMaker prepara dados para machine learning?
**
O [Amazon SageMaker Data Wrangler](https://aws.amazon.com/sagemaker/data-wrangler/) reduz o tempo de agregação e preparação de dados para machine learning. A partir de uma única interface no SageMaker Studio, você pode importar dados do Amazon S3, Amazon Athena, Amazon Redshift, AWS Lake Formation e [Amazon SageMaker Feature Store](https://aws.amazon.com/sagemaker/feature-store/) e, com apenas alguns cliques, o SageMaker Data Wrangler irá carregar, agregar e exibir automaticamente os dados brutos. Em seguida, ele fará recomendações de conversão com base nos dados de origem, transformará os dados em novos recursos, validará os recursos e fornecerá visualizações com recomendações sobre como remover fontes comuns de erro, como rótulos incorretos. Depois que os dados estiverem preparados, você poderá criar fluxos de trabalho de machine learning totalmente automatizados com o Amazon SageMaker Pipelines ou importar os dados no [Amazon SageMaker Feature Store](https://aws.amazon.com/sagemaker/feature-store/).

**P: Como posso criar recursos de modelos com o Amazon SageMaker Data Wrangler?
**
Sem escrever uma única linha de código, o Amazon SageMaker Data Wrangler pode transformar automaticamente seus dados em novos recursos. O SageMaker Data Wrangler oferece uma seleção de transformações de dados pré-configuradas, como converter tipo de coluna, codificação dinâmica, imputar dados ausentes com média ou mediana, redimensionar colunas e incorporações de dados/tempo. Por exemplo, você pode converter uma coluna de campo de texto em uma coluna numérica com um único clique ou criar transformações personalizadas em PySpark, SQL e Pandas.

**P: Como posso visualizar meus dados no Amazon SageMaker Data Wrangler?
**
O Amazon SageMaker Data Wrangler ajuda você a entender seus dados e identificar erros potenciais e valores extremos com um conjunto de modelos de visualização pré-configurados robustos. Histogramas, gráficos de dispersão e visualizações específicas de ML, como detecção de vazamento de destino, estão todos disponíveis sem necessidade de se escrever uma única linha de código. Você também pode criar e editar suas próprias visualizações.

**P: Como a definição de preços do Amazon SageMaker Data Wrangler funciona?
**
Você paga por todos os recursos de computação, armazenamento e processamento de dados de ML que utiliza para o Amazon SageMaker Data Wrangler. Você pode revisar todos os detalhes da definição de preço do Amazon SageMaker Data Wrangler [aqui](https://aws.amazon.com/sagemaker/pricing/). Como parte do [nível gratuito da AWS](https://aws.amazon.com/free/), você também pode começar a usar o SageMaker Data Wrangler gratuitamente.

**P: Como eu armazeno recursos para meus modelos de ML?
**
A [Amazon SageMaker Feature Store](https://aws.amazon.com/sagemaker/feature-store/) fornece um repositório central de recursos de dados com baixa latência (milissegundos) de leituras e gravações. Os recursos podem ser armazenados, recuperados, descobertos e compartilhados por meio do SageMaker Feature Store para fácil reutilização em modelos e equipes com acesso e controle seguros. A SageMaker Feature Store é compatível com recursos online e offline gerados via pipelines em lote ou de transmissão. Ela é compatível com preenchimento dos recursos e fornece armazenamento online e offline para manter a paridade entre os recursos usados no treinamento do modelo e na inferência.
**
P: Como eu mantenho a consistência entre os recursos online e offline?
**
A Amazon SageMaker Feature Store mantém automaticamente a consistência entre os recursos online e offline sem necessidade de gerenciamento ou código adicional. A SageMaker Feature Store é totalmente gerenciada e mantém a consistência nos ambientes de treinamento e inferência.

**P: Como posso reproduzir um recurso de um determinado momento?
**
A Amazon SageMaker Feature Store mantém registros de data e hora para todos os recursos em todas as instâncias. Isso ajuda você a recuperar recursos a qualquer momento para requisitos de negócios ou de conformidade. Você pode explicar facilmente os recursos do modelo e seus valores desde a primeira vez que foram criados até o presente, reproduzindo o modelo de um determinado momento.

**P: O que são os recursos offline?
**
Os recursos offline são usados para treinamento, pois você precisa acessar volumes muito grandes por um longo período de tempo. Esses recursos são servidos por um repositório de alta vazão e alta largura de banda.

**P: O que são os recursos online?**

Os recursos online são usados em aplicativos necessários para fazer previsões em tempo real. Os recursos online são servidos a partir de um repositório com alta taxa de transferência e latência abaixo de 10 milissegundos para previsões rápidas.

**P: Como a definição de preço da Amazon SageMaker Feature Store funciona?**


Você pode começar a usar a Amazon SageMaker Feature Store gratuitamente como parte do [nível gratuito da AWS](https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc). Com a SageMaker Feature Store, você paga para escrever na loja de recursos e ler e armazenar na loja de recursos online. A [Página de definição de preço do SageMaker](https://aws.amazon.com/sagemaker/pricing/) tem todos os detalhes sobre como funciona a definição de preço para a SageMaker Feature Store.

**P: O que é o Amazon SageMaker Ground Truth?
**
O Amazon SageMaker Ground Truth oferece rotulagem de dados automatizada usando machine learning. Primeiro, o SageMaker Ground Truth selecionará uma amostra aleatória de dados e a enviará para o Amazon Mechanical Turk rotular. Os resultados serão usados para treinar um modelo de rotulagem que tentará rotular uma nova amostra de dados brutos automaticamente. Os rótulos são confirmados quando o modelo consegue rotulá-los com uma pontuação de confiança que atende ou excede o limite que você definiu. Quando a pontuação de confiança fica abaixo desse limite, os dados são enviados para rotulagem por humanos. Alguns dos dados rotulados por humanos são usados para gerar um novo conjunto de dados de treinamento para o modelo de rotulagem. O modelo é treinado automaticamente mais uma vez para melhorar a precisão. Esse processo se repete a cada amostra de dados brutos a ser rotulada. O modelo de rotulagem se tornará mais capaz de rotular automaticamente dados brutos em cada iteração, e menos dados serão encaminhados para pessoas.
 

## Criar modelos

**P: O que são blocos de anotações do Amazon SageMaker Studio?**

Os blocos de anotações do Amazon SageMaker Studio são blocos de anotações do Jupyter colaborativos, flexíveis e gerenciados que são parte do Amazon SageMaker Studio, um ambiente de desenvolvimento totalmente integrado para machine learning.

**P: Qual a diferença entre a oferta de blocos de anotações do SageMaker Studio e blocos de anotações com base em instância?**

Os blocos de anotações do SageMaker Studio oferecem alguns recursos importantes que os diferenciam dos blocos de anotações baseados em instâncias. Com os blocos de anotações do Studio, é possível iniciar rapidamente blocos de anotações sem precisar provisionar uma instância manualmente e esperar que ela fique operacional. O tempo de inicialização da execução da interface de usuário para ler e executar um bloco de anotações é mais rápido do que os blocos de anotações baseados em instância.

Você também tem a flexibilidade de escolher entre uma grande coleção de tipos de instância diretamente da interface do usuário a qualquer momento. Não será mais necessário acessar o Console AWS para iniciar novas instâncias e transferir seus blocos de anotações.

Cada usuário tem um diretório inicial isolado, independente de uma instância específica. Esse diretório é montado automaticamente em todos os servidores de blocos de anotações e kernels à medida que são inicializados, permitindo que você acesse seus blocos de anotações e outros arquivos mesmo que mude de instância para exibir e executar seus blocos de anotações.

Os blocos de anotações do SageMaker Studio são integrados ao AWS SSO, facilitando o uso de suas credenciais organizacionais para acessá-los. O compartilhamento de bloco de anotações é um recurso integrado nos blocos de anotações do SageMaker Studio. Você também pode compartilhar seus blocos de anotações com colegas com um único clique.

**P: Como funcionam os blocos de anotações do Amazon SageMaker Studio?**

Os blocos de anotações do Amazon SageMaker Studio são blocos de anotações do Jupyter que podem ser iniciados rapidamente com um clique. Os recursos de computação subjacentes são totalmente elásticos, portanto, você pode aumentar ou reduzir facilmente os recursos disponíveis, e as alterações ocorrem automaticamente em segundo plano sem interromper seu trabalho. O SageMaker também permite o compartilhamento de blocos de anotações com um clique. Você pode compartilhar facilmente blocos de anotações com outros usuários e eles receberão exatamente o mesmo bloco de anotações, salvo no mesmo local.

Com os blocos de anotações do SageMaker Studio, você pode fazer login com suas credenciais corporativas usando o AWS SSO. É fácil compartilhar blocos de anotações nas equipes e entre elas, pois as dependências necessárias para executar um bloco de anotações são rastreadas automaticamente em imagens de trabalho encapsuladas com o bloco de anotações quando ele é compartilhado.

**P: Como funcionam os blocos de anotações do Amazon SageMaker Studio com outros serviços da AWS?**

Os blocos de anotações do Amazon SageMaker Studio oferecem acesso a todos os recursos do SageMaker, como treinamento distribuído, transformação em lote, hospedagem e gerenciamento de experiências. Você pode acessar outros serviços, como conjuntos de dados no Amazon S3, Amazon Redshift, AWS Glue, Amazon EMR ou AWS Lake Formation a partir dos blocos de anotações do SageMaker.

**P: Como funciona a definição de preço dos blocos de anotações do SageMaker Studio?**

Quando usa blocos de anotação do SageMaker Studio, você paga por computação e armazenamento. Consulte a [definição de preço do Amazon SageMaker](https://aws.amazon.com/pt/sagemaker/pricing/) para ver as taxas por tipo de instância de computação. Seus blocos de anotações e artefatos associados, como arquivos de dados e scripts, são persistidos no Amazon EFS. Consulte a [definição de preço do Amazon EFS](https://aws.amazon.com/pt/efs/pricing/) para taxas de armazenamento. Como parte do [nível gratuito de AWS](https://aws.amazon.com/pt/free/), você pode começar a usar gratuitamente os blocos de anotações do Amazon SageMaker Studio.

**P: Há uma cobrança separada para cada bloco de anotações criado e executado no SageMaker Studio?**

Não. Você pode criar e executar vários blocos de anotações na mesma instância de computação. Você paga apenas pela computação utilizada e não por itens individuais. Leia mais sobre isso em nosso [guia de medição](https://docs.aws.amazon.com/sagemaker/latest/dg/notebooks-usage-metering.html).

Além dos blocos de anotações, você também pode iniciar e executar terminais e shells interativos no Studio, tudo isso na mesma instância de computação. Cada aplicação executa em um contêiner ou em uma imagem. O SageMaker Studio oferece várias imagens predefinidas de propósito específico e pré-configuradas para ciência de dados e machine learning. Você pode ler mais sobre o ambiente do desenvolvedor do Studio em nosso guia sobre o [uso de blocos de anotações do SageMaker Studio](https://docs.aws.amazon.com/sagemaker/latest/dg/notebooks.html).

**P: Como monitoro e encerro os recursos usados pelos meus blocos de anotações?**

Você pode monitorar e encerrar os recursos usados por blocos de anotações do SageMaker Studio usando a interface visual do SageMaker Studio ou o Console de Gerenciamento da AWS. Consulte a [documentação](https://docs.aws.amazon.com/sagemaker/latest/dg/studio-ui.html#studio-ui-nav-bar) para obter mais detalhes.

**P: Estou executando um bloco de anotações do SageMaker Studio. Continuarei sendo cobrado se fechar meu navegador, fechar a guia do bloco de anotações ou deixar o navegador aberto?**

Sim, você continuará a ser cobrado pela computação. Esta situação é semelhante a iniciar instâncias do Amazon EC2 no Console de Gerenciamento da AWS e depois fechar o navegador. As instâncias do Amazon EC2 continuam em execução e você continua a ser cobrado, a menos que encerre explicitamente a instância.

**P: Eu sou cobrado por criar e configurar um domínio do Studio?**

Não. Você não é cobrado por criar ou configurar um domínio do Studio nem por adicionar, atualizar e excluir perfis de usuário.

**P: Como vejo as cobranças discriminadas dos blocos de anotações do Studio ou de outros serviços do SageMaker?**

Como administrador, você pode ver a lista de cobranças discriminadas do SageMaker, incluindo o Studio, no Console de faturamento da AWS. No Console de Gerenciamento da AWS do SageMaker, selecione **Serviços** no menu superior, digite **Faturamento** na caixa de pesquisa, selecione Faturamento na lista suspensa e **Faturas** no painel esquerdo. Na seção Detalhes, você pode clicar em **SageMaker** para ampliar a lista de regiões e detalhar as cobranças por item.

## Treinar modelos

**P: O que é o Amazon SageMaker Experiments?**

O Amazon SageMaker Experiments ajuda a organizar e monitorar iterações para modelos de machine learning. O SageMaker Experiments ajuda a gerenciar as iterações, capturando automaticamente os parâmetros de entrada, as configurações e os resultados, armazenando-os como "experimentos". Você pode trabalhar na interface visual do SageMaker Studio, onde pode procurar experimentos ativos, pesquisar experimentos anteriores pelas características, revisar experimentos anteriores pelos resultados deles e comparar visualmente os experimentos.

**P: O que é o Amazon SageMaker Debugger?**

O Amazon SageMaker Debugger captura automaticamente métricas em tempo real durante o treinamento, como matrizes de confusão e gradientes de aprendizagem, para ajudar a melhorar a precisão do modelo. As métricas do SageMaker Debugger podem ser visualizadas no SageMaker Studio para facilitar o entendimento. O SageMaker Debugger também pode gerar avisos e conselhos de correção quando problemas comuns de treinamento são detectados. O SageMaker Debugger também monitora automaticamente e cria perfis de recursos do sistema, como CPU, GPU, rede e memória, em tempo real, e fornece recomendações sobre a realocação desses recursos. Isso permite que você use seus recursos de forma eficiente durante o treinamento e ajuda a reduzir custos e recursos.

**P: O Amazon SageMaker oferece suporte a treinamento distribuído?
**
Sim. O Amazon SageMaker pode distribuir automaticamente modelos de aprendizado profundo e grandes conjuntos de treinamento em instâncias de GPU da AWS em uma fração do tempo necessário para construir e otimizar essas estratégias de distribuição manualmente. As duas técnicas de treinamento distribuído aplicadas pelo SageMaker são paralelismo de dados e paralelismo de modelos. O paralelismo de dados é aplicado para melhorar as velocidades de treinamento, dividindo os dados igualmente em várias instâncias de GPU, permitindo que cada instância treine simultaneamente. O paralelismo de modelos é útil para modelos muito grandes para serem armazenados em uma única GPU, o que exige que o modelo seja particionado em partes menores antes de ser distribuído em várias GPUs. Com apenas algumas linhas de código adicional em seus scripts de treinamento PyTorch e TensorFlow, o SageMaker aplicará automaticamente o paralelismo de dados ou o paralelismo de modelo para você, permitindo que você desenvolva e implante seus modelos mais rapidamente. O SageMaker determinará a melhor abordagem para dividir seu modelo usando algoritmos de particionamento gráfico para equilibrar a computação de cada GPU, minimizando a comunicação entre instâncias de GPU. O SageMaker também otimiza seus trabalhos de treinamento distribuído por meio de algoritmos que utilizam totalmente a infraestrutura de computação e rede da AWS, a fim de obter eficiência de escalabilidade quase linear, o que permite concluir o treinamento com mais rapidez em comparação com as implementações de código aberto manuais.

**P: O que é Treinamento gerenciado de spots?**

O Treinamento gerenciado de spots com o Amazon SageMaker permite treinar seus modelos de machine learning usando instâncias spot do Amazon EC2 e reduzir o custo do treinamento de seus modelos em até 90%.

**P: Como uso o Treinamento gerenciado de spots?**

Você habilita a opção de Treinamento gerenciado de spots ao enviar suas tarefas de treinamento e também especifica por quanto tempo aguardará a capacidade spot. O Amazon SageMaker usará as instâncias spot do Amazon EC2 para executar sua tarefa e gerenciar a capacidade spot. Você tem total visibilidade do status de sua tarefa de treinamento, tanto enquanto ela está em execução como enquanto ela está aguardando a capacidade.

**P: Como devo usar o Treinamento gerenciado de spots?**

O Treinamento gerenciado de spots é ideal quando você tem a flexibilidade com suas execuções de treinamento e quando quer minimizar o custo de suas tarefas de treinamento. Com o treinamento gerenciado de spots, você pode reduzir o custo de treinamento de modelos de machine learning em até 90%.

**P: Como o treinamento gerenciado de spots funciona?**

O treinamento gerenciado de spots usa instâncias spot do Amazon EC2 para treinamento, e essas instâncias poderão ser pré-esvaziadas quando a AWS precisar de capacidade. Como resultado, as tarefas de Treinamento gerenciado de spots podem ser executadas em pequenos incrementos como e quando a capacidade se tornar disponível. Os trabalhos de treinamento não precisam ser reiniciadas do zero quando há um interrupção já que o Amazon SageMaker pode retomar trabalhos de treinamento usando o ponto de verificação mais recente do modelo. As estruturas integradas e os algoritmos integrados de visão de computador com o Amazon SageMaker habilitam pontos de verificação periódicos, e é possível habitá-los com modelos personalizados.

**P: Preciso usar um ponto de verificação periodicamente com o Treinamento gerenciado de spots?**

Recomendamos usar pontos de verificação periódicos como melhor prática para execução prolongada de tarefas de treinamento. Isso impede que suas tarefas de Treinamento gerenciado de spots sejam reinicializadas se a capacidade for pré-esvaziada. Quando você habilita os pontos de verificação, o Amazon SageMaker retoma suas tarefas de Treinamento gerenciado de spots desde o ponto de verificação mais recente.

**P: Como você calcula a economia de custo com tarefas de Treinamento gerenciado de spots?**

Depois de concluir uma tarefa de Treinamento gerenciado de spots, você pode ver a economia no Console de Gerenciamento da AWS e também calcular a economia de custo como a diferença percentual entre a duração da tarefa de treinamento e a duração que foi faturada.

Independentemente de quantas vezes suas tarefas de Treinamento gerenciado de spots foram interrompidas, você será cobrado somente uma vez com base na quantidade de dados obtidos por download.

**P: Quais instâncias posso usar com o Treinamento gerenciado de spots?**

O Treinamento gerenciado de instâncias pode ser usado com todas as instâncias compatíveis com o Amazon SageMaker.

**P: Que regiões da AWS são compatíveis com o Treinamento gerenciado de spots?**

O Treinamento gerenciado de spots é compatível com todas as regiões da AWS em que o Amazon SageMaker está [disponível](https://aws.amazon.com/pt/about-aws/global-infrastructure/regional-product-services/) atualmente.

**P: Há limite para o tamanho do conjunto de dados que posso usar para treinamento?**

Não há limites fixos para o tamanho do conjunto de dados que pode ser usado para modelos de treinamento com o Amazon SageMaker.

**P: Quais algoritmos são usados pelo Amazon SageMaker para gerar modelos?**

O Amazon SageMaker inclui algoritmos incorporados para regressão linear, regressão logística, agrupamentos k-means, análise de componente principal, máquinas de fatoração, modelagem de tópicos neural, alocação latente de dirichlet, árvores reforçadas com gradiente, sequence2sequence, previsão de séries temporais, word2vec e classificação de imagens. O SageMaker também fornece contêineres otimizados do Apache MXNet, Tensorflow, Chainer, PyTorch, Gluon, Keras, Horovod, Scikit-learn e Deep Graph Library. Além disso, o Amazon SageMaker oferece suporte a algoritmos de treinamento personalizados fornecidos por meio de uma imagem do Docker de acordo com a especificação documentada.

**P: O que é o ajuste automático de modelos?**

A maioria dos algoritmos de machine learning expõe diversos parâmetros que controlam a operação do algoritmo subjacente. Normalmente, esses parâmetros são mencionados como hiperparâmetros e seus valores afetam a qualidade dos modelos treinados. O ajuste automático de modelos é o processo de encontrar um conjunto de hiperparâmetros de um algoritmo que gera um modelo ideal.

**P: Quais modelos podem ser ajustados com o ajuste automático de modelos?**

Você pode executar o ajuste automático de modelos no Amazon SageMaker para qualquer algoritmo, desde que cientificamente viável, incluindo algoritmos incorporados do SageMaker, redes neurais profundas ou algoritmos arbitrários a serem incorporados ao SageMaker na forma de imagens do Docker.

**P: Posso usar o ajuste automático de modelos fora do Amazon SageMaker?**

Não neste momento. A performance e a experiência do ajuste de modelos são melhores dentro do Amazon SageMaker.

**P: Qual é o algoritmo de ajuste subjacente?**

No momento, o nosso algoritmo de ajuste de hiperparâmetros é uma implementação personalizada da otimização bayesiana. Essa implementação pretende otimizar uma métrica de objetivo especificada pelo cliente durante todo o processo de ajuste. Especificamente, a implementação verifica a métrica do objeto para trabalhos de treinamento concluídos e usa esse conhecimento para inferir a combinação de hiperparâmetros para o próximo trabalho de treinamento.

**P: A AWS recomenda hiperparâmetros específicos para ajuste?**

Não. O impacto de determinados hiperparâmetros sobre o desempenho do modelo depende de vários fatores. É difícil afirmar com certeza se um hiperparâmetro é mais importante que os demais e, portanto, precisa de ajuste. Para algoritmos incorporados ao Amazon SageMaker, informamos se um hiperparâmetro é ajustável.

**P: Quanto tempo demora o trabalho de ajuste de um hiperparâmetro?**

A duração do trabalho de ajuste de um hiperparâmetro depende de vários fatores, incluindo o tamanho dos dados, o algoritmo subjacente e os valores dos hiperparâmetros. Além disso, os clientes podem escolher o número de trabalhos de treinamento simultâneos e o seu número total. Todas essas escolhas afetam a duração do trabalho de ajuste de hiperparâmetros.

**P: Posso otimizar simultaneamente vários objetivos como, por exemplo, a velocidade e a precisão de um modelo?**

Não neste momento. Por enquanto, é necessário especificar uma única métrica de objetivo a ser otimizada, ou alterar o código do algoritmo para emitir uma nova métrica (que é uma média ponderada entre duas ou mais métricas úteis) e fazer o processo de ajuste otimizar considerando essa nova métrica de objetivo.

**P: Quanto custa o ajuste automático de modelos?**

O trabalho de ajuste de hiperparâmetros não é cobrado. Serão cobrados os trabalhos de treinamento iniciados pelo trabalho de ajuste de hiperparâmetros, de acordo com a [definição de preço de treinamento do modelo](https://aws.amazon.com/pt/sagemaker/pricing/).

**P: Como escolher entre usar o Amazon SageMaker Autopilot ou o ajuste automático de modelos?**

O Amazon SageMaker Autopilot automatiza tudo em um fluxo de trabalho típico de machine learning, incluindo pré-processamento de recursos, seleção de algoritmos e ajuste de hiperparâmetros, concentrando-se especificamente em casos de uso de classificação e regressão. Por outro lado, o ajuste automático de modelos foi projetado para ajustar qualquer modelo, quer ele se baseie em algoritmos integrados, estruturas de aprendizagem profunda ou contêineres personalizados. Em troca da flexibilidade, você deve escolher manualmente o algoritmo específico, determinar os hiperparâmetros a serem ajustados e os intervalos de pesquisa correspondentes.

**P: O que é aprendizado por reforço?**

O aprendizado por reforço é uma técnica de machine learning que permite que um agente aprenda em um ambiente interativo por tentativa e erro, usando feedback recebido por suas próprias ações e experiências.

**P: Posso treinar modelos de aprendizado por reforço no Amazon SageMaker?**

Sim, você pode treinar modelos de aprendizado por reforço no Amazon SageMaker, além dos modelos de aprendizado supervisionado e não supervisionado.

**P: Qual é a diferença entre o aprendizado por reforço e o aprendizado supervisionado?**

Embora ambos os aprendizados usem mapeamento entre entrada e saída, ao contrário do aprendizado supervisionado em que o feedback fornecido para o agente é o conjunto correto de funções para execução de uma tarefa, o aprendizado por reforço usa um feedback atrasado onde sinais de recompensa são otimizados para garantir um objetivo a longo prazo por meio de uma sequência de ações.

**P: Quando devo usar o aprendizado por reforço?**

Enquanto o objetivo das técnicas de aprendizado supervisionado é encontrar a resposta certa com base nos padrões dos dados de treinamento, o objetivo das técnicas de aprendizado não supervisionado é encontrar semelhanças e diferenças entre os pontos de dados. Em contraste, o objetivo das técnicas de aprendizado por reforço (RL) é aprender como alcançar um resultado desejado mesmo quando não estiver claro o que deve ser feito para isso. Como resultado, o aprendizado por reforço é mais adequado para permitir aplicativos inteligentes, onde um agente pode tomar decisões autônomas, como robótica, veículos autônomos, HVAC, controle industrial e muito mais.

**P: Quais tipos de ambientes posso usar para o treinamento dos modelos de aprendizado por reforço?**

O aprendizado por reforço do Amazon SageMaker oferece suporte a diversos ambientes diferentes para treinamento dos modelos de aprendizado por reforço. Use serviços da AWS, como o AWS RoboMaker, ambientes de código aberto ou ambientes personalizados desenvolvidos usando interfaces Open AI Gym, ou ambientes de simulação comerciais, como o MATLAB e o SimuLink.

**P: Preciso escrever meus próprios algoritmos de agente de aprendizado por reforço para treinar os modelos de aprendizado por reforço?**

Não, o aprendizado por reforço do Amazon SageMaker inclui toolkits de aprendizado por reforço, como Coach and Ray RLLib, que oferecem implementações de algoritmos do agente de aprendizado por reforço, como DQN, PPO, A3C e muito mais.

**P: Posso usar minhas próprias bibliotecas de aprendizado por reforço e implementação de algoritmo, e executar no aprendizado por reforço do Amazon SageMaker?**

Sim, você pode usar suas próprias bibliotecas de aprendizado por reforço e implementações de algoritmo em contêineres Docker e executá-las no aprendizado por reforço do Amazon SageMaker.

**P: Posso fazer lançamentos distribuídos usando o aprendizado por reforço do Amazon SageMaker?**

Sim. Também é possível selecionar um cluster heterogêneo onde o treinamento pode ser executado em uma instância da GPU e as simulações podem ser executadas em várias instâncias da CPU.

## Implantar modelos

**P: O que é o Amazon SageMaker Model Monitor?**

O Amazon SageMaker Model Monitor permite que os desenvolvedores detectem e corrijam o desvio do conceito. O SageMaker Model Monitor detecta automaticamente desvios de conceito nos modelos implantados e fornece alertas detalhados que ajudam a identificar a origem do problema. Todos os modelos treinados no SageMaker emitem automaticamente as principais métricas que podem ser coletadas e visualizadas no SageMaker Studio. No SageMaker Studio, você pode configurar os dados a serem coletados, como são visualizados e quando receber alertas.

**P: Posso acessar a infraestrutura em que o Amazon SageMaker é executado?**

Não. O Amazon SageMaker opera a infraestrutura de computação em seu nome, o que permite executar verificações de integridade, aplicar patches de segurança e realizar outras manutenções de rotina. Você também pode implantar os artefatos do modelo do treinamento com código de inferência personalizado no seu próprio ambiente de hospedagem.

**P: Como posso escalar o tamanho e a performance de um modelo do Amazon SageMaker após implantá-lo em produção?**

A hospedagem do Amazon SageMaker escala automaticamente a performance necessária para o aplicativo usando Application Auto Scaling. Além disso, você pode alterar manualmente o número e o tipo de instâncias sem causar tempo de inatividade por meio da modificação da configuração do endpoint.

**P: Como posso monitorar o ambiente de produção do Amazon SageMaker?**

O Amazon SageMaker emite métricas de performance para o Amazon CloudWatch Metrics para que você possa rastrear métricas, definir alarmes e reagir automaticamente a mudanças no tráfego de produção. Além disso, o Amazon SageMaker escreve logs para o Amazon Cloudwatch Logs, o que permite monitorar e solucionar problemas do ambiente de produção.

**P: Que tipos de modelos podem ser hospedados com o Amazon SageMaker?**

O Amazon SageMaker pode hospedar qualquer modelo que siga a especificação documentada para imagens de Docker de inferência. Isso inclui os modelos criados de artefatos de modelo e código de inferência do Amazon SageMaker.

**P: A quantas solicitações de API concorrentes em tempo real o Amazon SageMaker consegue oferecer suporte?**

O Amazon SageMaker foi criado para escalar para um grande número de transações por segundo. O número preciso varia em função do modelo implantado e do número e do tipo de instâncias nas quais o modelo é implantado.

**P: O que é o Batch Transform?**

O Batch Transform permite que você execute previsões em dados em lotes grandes ou pequenos. Não há necessidade de dividir o conjunto de dados em diversas partes nem gerenciar endpoints em tempo real. Com uma API simples, você pode solicitar previsões para um grande número de registros de dados e transformar os dados de maneira rápida e fácil.

**P: O que é o Amazon SageMaker Edge Manager?
**
O Amazon SageMaker Edge Manager é um recurso do Amazon SageMaker que torna mais fácil otimizar, proteger, monitorar e manter modelos de machine learning em frotas de dispositivos de borda, como câmeras inteligentes, robôs, computadores pessoais e dispositivos móveis. O SageMaker Edge Manager ajuda os desenvolvedores de ML a operar modelos de ML em uma variedade de dispositivos de borda em escala.

**P: Como posso começar a usar o SageMaker Edge Manager?
**
Para começar a usar o SageMaker Edge Manager, você precisa compilar e empacotar seus modelos de ML treinados na nuvem, registrar seus dispositivos e prepará-los com o SDK do SageMaker Edge Manager. Para preparar o seu modelo para implantação, o SageMaker Edge Manager usa o SageMaker Neo para compilar o seu modelo para o hardware de borda de destino. Após o modelo ser compilado, o SageMaker Edge Manager assinará o modelo com uma chave gerada pela AWS e, em seguida, empacotará o modelo com seu tempo de execução e as credenciais necessárias para prepará-lo para a implantação. No lado do dispositivo, você registra seu dispositivo com o SageMaker Edge Manager, baixa o SDK do SageMaker Edge Manager e, em seguida, segue as instruções para instalar o agente SageMaker Edge Manager em seus dispositivos. O bloco de anotações tutorial fornece um exemplo detalhado de como você pode preparar os modelos e conectar seus modelos em dispositivos de borda com SageMaker Edge Manager.

**P: Com quais dispositivos o SageMaker Edge Manager é compatível?
**
O Amazon SageMaker Edge Manager é compatível com dispositivos baseados em CPU (ARM, x86), GPU (ARM, Nvidia) comuns, com sistemas operacionais Linux e Windows. Com o passar tempo, o SageMaker Edge Manager se expandirá para ser compatível com mais processadores integrados e plataformas móveis que também são compatíveis com o SageMaker Neo.

**P: Preciso usar o Amazon SageMaker para treinar meu modelo com o intuito de usar o Amazon SageMaker Edge Manager?
**
Não, você não precisa. Você pode treinar seus modelos em outro lugar ou usar um modelo pré-treinado de código aberto ou de seu fornecedor de modelos.

**P: Preciso usar o Amazon SageMaker Neo para compilar meu modelo para poder usar o Amazon SageMaker Edge Manager?
**
Sim, você precisa. O Amazon SageMaker Neo converte e compila seus modelos em um executável que você pode empacotar e implantar em seus dispositivos de borda. Assim que o pacote do modelo for implantado, o agente Amazon SageMaker Edge Manager desempacotará o pacote do modelo e executará o modelo no dispositivo.

**Q: Como eu implanto modelos nos dispositivos de borda?
**
O Amazon SageMaker Edge Manager armazena o pacote do modelo em seu bucket do Amazon S3 especificado. Você pode usar o recurso de implantação over-the-air (OTA) fornecido pelo AWS IoT Greengrass ou qualquer outro mecanismo de implantação de sua escolha para implantar o pacote de modelo de seu bucket S3 para os dispositivos.

**P: Qual é a diferença entre o SDK do Amazon SageMaker Edge Manager e a runtime (dlr) do SageMaker Neo?
**
A Neo dlr é um runtime de código aberto que executa apenas modelos compilados pelo serviço Amazon SageMaker Neo. Em comparação com a dlr de código aberto, o SDK do SageMaker Edge Manager inclui um agente de nível corporativo no dispositivo com segurança adicional, gerenciamento de modelo e recursos de serviço de modelos. O SDK do SageMaker Edge Manager é adequado para implantação de produção em escala.

**P: Como o Amazon SageMaker Edge Manager se relaciona com o AWS IoT Greengrass?
**
O Amazon SageMaker Edge Manager e o AWS IoT Greengrass podem trabalhar juntos em sua solução de IoT. Quando seu modelo de ML for empacotado com SageMaker Edge Manager, você poderá usar o recurso de atualização OTA do AWS IoT Greengrass para implantar o pacote de modelo no seu dispositivo. O AWS IoT Greengrass permite monitorar seus dispositivos IoT remotamente, enquanto o SageMaker Edge Manager ajuda a monitorar e manter os modelos de ML nos dispositivos.

**P: Como o Amazon SageMaker Edge Manager se relaciona com o AWS Panorama? Quando você deve usar o Amazon SageMaker Edge Manager em vez do AWS Panorama?
**
A AWS oferece a maior amplitude e profundidade de recursos para a execução de modelos em dispositivos de borda. Temos serviços para oferecer suporte a uma ampla variedade de casos de uso, incluindo visão computacional, reconhecimento de voz e manutenção preditiva.

Para empresas que procuram executar visão computacional em dispositivos de borda, como câmeras e aparelhos, você pode usar o AWS Panorama. O Panorama oferece aplicativos prontos para implantar visão computacional para dispositivos de borda. É fácil começar a usar o AWS Panorama fazendo login no console da nuvem, especificando o modelo que você gostaria de usar no Amazon S3 ou no SageMaker e, em seguida, escrevendo a lógica de negócios como um script Python. O AWS Panorama compila o modelo para o dispositivo de destino e cria um pacote de aplicativo para que possa ser implantado em seus dispositivos com apenas alguns cliques. Além disso, os ISVs que desejam construir seus próprios aplicativos personalizados podem usar o SDK do AWS Panorama, e os fabricantes de dispositivos podem usar o Device SDK para certificar seus dispositivos para AWS Panorama.

Os clientes que desejam construir seus próprios modelos e ter um controle mais granular sobre os recursos do modelo podem usar o Amazon SageMaker Edge Manager. O SageMaker Edge Manager é um serviço gerenciado para preparar, executar, monitorar e atualizar modelos de machine learning (ML) em frotas de dispositivos de borda, como câmeras inteligentes, alto-falantes inteligentes e robôs para qualquer caso de uso, como processamento de idioma natural, detecção de fraude, e manutenção preditiva. O SageMaker Edge Manager é para desenvolvedores de borda de ML que desejem controle sobre seu modelo, incluindo a engenharia de diferentes recursos de modelos e modelos de monitor para deriva. Qualquer desenvolvedor de borda de ML pode usar o SageMaker Edge Manager por meio do console do SageMaker e das APIs do SageMaker. O SageMaker Edge Manager traz os recursos do SageMaker para construir, treinar e implantar modelos na nuvem para dispositivos de borda.

**P: Em quais regiões da AWS o Amazon SageMaker Edge Manager está disponível?
**
O Amazon SageMaker Edge Manager está disponível em 6 regiões AWS: Leste dos EUA (Norte da Virgínia), Leste dos EUA (Ohio), Oeste dos EUA (Oregon), Europa (Irlanda), Europa (Frankfurt) e Pacífico Asiático (Tóquio). Consulte os detalhes na [Tabela de regiões da AWS](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/).

**P: O que é o Amazon SageMaker Neo?**

O Amazon SageMaker Neo permite que os modelos de machine learning sejam treinados uma vez executados em qualquer lugar na nuvem e localmente. O SageMaker Neo otimiza automaticamente os modelos criados com estruturas de trabalho populares de deep learning que podem ser usadas para implantação em várias plataformas de hardware. Os modelos otimizados são executados até 25 vezes mais rápido e consomem menos de um décimo dos recursos dos modelos de machine learning usuais.

**P: Como faço para começar a usar o Amazon SageMaker Neo?**

Para começar a usar o Amazon SageMaker Neo, faça login no console do Amazon SageMaker, escolha um modelo de treinamento, siga o exemplo para compilar modelos e implante o modelo resultante na plataforma de hardware de destino.

**P: Quais são os principais componentes do Amazon SageMaker Neo?**

O Amazon SageMaker Neo contém dois componentes principais – um compilador e um tempo de execução. Primeiro, o compilador Neo lê os modelos exportados por estruturas diferentes. Em seguida, ele converte as funções e operações específicas para cada estrutura em uma representação intermediária indiferente à estrutura. Depois, realiza uma série de otimizações. Em seguida, o compilador gera código binário para as operações otimizadas e grava em uma biblioteca de objetos compartilhados. O compilador também salva a definição do modelo e os parâmetros em arquivos separados. Durante a execução, o tempo de execução do Neo carrega os artefatos gerados pelo compilador — definição do modelo, parâmetros e a biblioteca de objetos compartilhados para executar o modelo.

**P: Preciso usar o Amazon SageMaker para treinar meu modelo com o intuito de usar o Amazon SageMaker Neo para converter o modelo?**

Não. Você pode treinar os modelos em outros lugares e usar o Neo para otimizá-los para instâncias de ML do Amazon SageMaker ou dispositivos compatíveis do AWS IoT Greengrass.

**P: A quais modelos o Amazon SageMaker Neo oferece suporte?**

Atualmente, o Amazon SageMaker Neo oferece suporte à maioria dos modelos de aprendizagem profunda que alimentam os aplicativos de visão computacional e os modelos de árvore de decisões mais populares usados no Amazon SageMaker atualmente. O Neo otimiza o desempenho dos modelos AlexNet, ResNet, VGG, Inception, MobileNet, SqueezeNet e DenseNet treinados em MXNet e TensorFlow e modelos de floresta de corte de classificação e aleatórios treinados em XGBoost.

**P: A quais plataformas de hardware o Amazon SageMaker Neo oferece suporte?
**
Você pode encontrar as listas de [instâncias de nuvem](https://docs.aws.amazon.com/sagemaker/latest/dg/neo-supported-cloud.html), [dispositivos de borda](https://docs.aws.amazon.com/sagemaker/latest/dg/neo-supported-devices-edge.html) e versões de framework com suporte na documentação do Amazon SageMaker Neo.



**P: Em quais regiões da AWS o Amazon SageMaker Neo está disponível?**

Para ver uma lista das regiões com suporte, consulte a [tabela de regiões da AWS](https://aws.amazon.com/pt/about-aws/global-infrastructure/regional-product-services/).

**P: Quais opções de implantação o Amazon SageMaker oferece?** 

Depois de construir e treinar modelos, o Amazon SageMaker oferece três opções para implantá-los para que você possa começar a fazer previsões. A inferência em tempo real é adequada para workloads com requisitos de latência de milissegundos, tamanhos de carga útil de até 6MB e tempos de processamento de até 60 segundos. A transformação em lote é ideal para previsões offline em grandes lotes de dados que estão disponíveis antecipadamente. A inferência assíncrona é projetada para workloads sem requisitos de latência de subsegundo, tamanhos de carga útil de até 1GB e tempos de processamento de até 15 minutos. 

**P: O que é a inferência assíncrona do SageMaker?**

O Amazon SageMaker produz filas assíncronas de inferência e as processa de forma assíncrona. Esta opção é ideal para pedidos com grandes tamanhos de carga útil e/ou longos tempos de processamento que precisam ser processados à medida que chegam. Opcionalmente, é possível configurar configurações de autoescalabilidade para reduzir a escala na vertical da instância para zero quando não estiver processando ativamente os pedidos para economizar em custos. 

**P: Como configurar as configurações de autoescalabilidade para reduzir a escala na vertical da contagem de instâncias a zero quando não estiver processando ativamente os pedidos?**

É possível reduzir a escala na vertical a contagem de instâncias de endpoint de inferência assíncrona do Amazon SageMaker para zero a fim de economizar em custos quando você não estiver processando ativamente os pedidos. Você precisa definir uma política de escalabilidade para escalar a métrica personalizada 'ApproximateBacklogPerInstance' e definir o valor 'MinCapacity' para zero. Para obter instruções passo a passo visite a seção [autoescalar um endpoint assíncrono](http://docs.aws.amazon.com/sagemaker/latest/dg/async-inference-autoscale.html) do guia do desenvolvedor. 

## Amazon SageMaker Savings Plans

**P: O que são os Amazon SageMaker Savings Plans?**

O Amazon SageMaker Savings Plans oferece um modelo de preços flexíveis baseado em uso para o Amazon SageMaker em troca de um compromisso com uma quantidade consistente de uso (medida em USD/hora) por um período de um ou três anos. Os Amazon SageMaker Savings Plans fornecem a maior flexibilidade e ajudam a reduzir seus custos em até 64%. Esses planos são aplicados automaticamente a usos de instâncias ML qualificadas do SageMaker, entre elas SageMaker Studio Notebooks, SageMaker On-Demand Notebooks, SageMaker Processing, SageMaker Data Wrangler, SageMaker Training, SageMaker Real-Time Inference e SageMaker Batch Transform, independentemente da família, tamanho ou região das instâncias. Por exemplo, você pode alterar o uso de uma instância de CPU ml.c5.xlarge em execução no Leste dos EUA (Ohio) para uma instância ml.Inf1 no Oeste dos EUA (Oregon) para cargas de trabalho de inferência a qualquer momento e continuar automaticamente a pagar o preço dos Savings Plans.

**Por que devo usar o Amazon SageMaker Savings Plans?**

Se você tem uma quantidade consistente de uso de instâncias do Amazon SageMaker (medida em USD/hora) e usa vários componentes do SageMaker, ou espera que sua configuração de tecnologia (por exemplo, família de instâncias, região) mude ao longo do tempo, o SageMaker Savings Plans simplifica a maximização das suas economias e, ao mesmo tempo, proporciona flexibilidade para alterar a configuração de tecnologia subjacente com base nas necessidades da aplicação ou em inovações. A taxa de Savings Plans é aplicada automaticamente a todo o uso de instâncias de ML qualificadas sem modificações manuais necessárias.

**P: Como posso começar a usar os Amazon SageMaker Savings Plans?**

Você pode começar com os Savings Plans no AWS Cost Explorer no console de gerenciamento ou usando a API/CLI. Você pode facilmente assumir um compromisso de Savings Plans usando as recomendações fornecidas no AWS Cost Explorer para obter as maiores economias. O compromisso por hora recomendado é baseado no uso histórico Sob demanda e na escolha do tipo de plano, vigência contratual e opção de pagamento. Depois de se cadastrar em um Savings Plan, seu uso de computação será cobrado automaticamente pelos preços com desconto para Savings Plans, e qualquer uso além do seu compromisso será cobrado a taxas regulares sob demanda.
**
P: Como o Savings Plans para o Amazon SageMaker difere do Compute Savings Plans para o Amazon EC2?**

A diferença entre o Savings Plans para o Amazon SageMaker e o Savings Plans para o EC2 está nos serviços incluídos. Os SageMaker Savings Plans só se aplicam ao uso de instâncias de ML do SageMaker.

**P: Como os Savings Plans funcionam com o AWS Organizations/Faturamento consolidado?**

Os Savings Plans podem ser adquiridos em qualquer conta dentro de uma família do AWS Organization/Faturamento consolidado. Por padrão, o benefício fornecido pelos Savings Plans é aplicável ao uso em todas as contas de uma família do AWS Organization/faturamento consolidado. No entanto, você também pode optar por restringir o benefício dos Savings Plans apenas à conta que os comprou.