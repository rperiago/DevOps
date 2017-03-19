# O que é DevOps

A comunidade em torno de DevOps tem se unido em torno de um conjunto de princípios geralmente acordados que apoiam a filosofia. Três dos princípios mais comumente aceitos são **Cultura**, **Automação** e **Métricas**. Sem qualquer um desses, seria difícil adotar uma filosofia DevOps.

O termo DevOps é a combinação das palavras "desenvolvimento" e "operações". Seu objetivo é remover as ineficiências encontradas ao longo do pipeline de **desenvolvimento**, **implantação** e **operações**.

O DevOps ajuda a fornecer uma maneira melhor de analisar o pipeline de **desenvolvimento**, **implantação** e **operações**. Faz isso promovendo uma **cultura** de **colaboração** e **automação**. Além de utilizar **métricas** de todos os dados úteis quanto possível. Trazendo assim uma melhor qualidade na entrega do projeto a ser desenvolvido.


### Cultura

DevOps vai de Filosofia a modismo sem uma cultura para sustentá-lo.

Cultura são os valores, crenças e comportamentos de um grupo/equipe, a visão, crenças e hábitos da empresa.

A cultura DevOps tem diversos princípios, como a melhoria contínua, o foco em qualidade, a eliminação de desperdícios, a otimização do todo e o respeito às pessoas.

Pessoas e processos são mais importantes. Se a cultura não estiver presente, qualquer tentativa de **automação** está destinada a falhar.

Com tudo isso é importante lembrar que todos dividimos a responsabilidade. A Filosofia DevOps vem para derrubar a culpa.

A colaboração e o compartilhamento de ideias e conhecimento ajudam a criar a **cultura** necessária para o sucesso com DevOps.

### Automação

Tudo que puder e achar relevante automatize. Libere os humanos para realizar tarefas que exigem criatividade e intuição e deixe as tarefas repetitivas para os computadores, que sabem executá-las rapidamente e de forma bem mais confiável.

O ponto chave aqui é reduzir a interação humana. Você já esteve naquela situação em que quer fazer aquela receita de bolo que sua vó faz tão bem. Você liga pra ela anota a receita detalhadamente e a segue perfeitamente, mas no final o bolo não sai como você imaginou, pois é a aqui que entra a automação. Somos humanos, nos distraímos ou simplesmente não estamos em um dia bom. Talvez possamos ter colocado açúcar de mais, ou pouca farinha, quem sabe? Fato é que a automação evita estes problemas e nos deixa livres para focar em coisas mais importantes.

### Métricas

Uma adoção de DevOps de sucesso irá medir tudo o que for possível, por exemplo: métricas de desempenho, métricas de processo, métricas de negócio etc.

Precisamos saber o que medir para determinar se o nosso pipeline está se tornando mais eficiente e se estamos produzindo com qualidade. Há muitas métricas que ajudam sua equipe. Cada papel na equipe terá métricas diferentes para melhor ajudá-los a fazer seu trabalho, e todas essas métricas devem ser medidos e relatados de volta para quem precisa deles


## Continuous delivery ou CD 

A ideia aqui é apertar um botão e entregar seu código onde quiser (Ambiente de homologação, teste ou produção).

A entrega contínua deve começar pela implantação do software em um ambiente de teste que espelhe a produção.

executar os testes de aceitação automatizados ou testes de regressão são para garantir que nenhuma nova mudança de código quebrou as funcionalidades existentes. Casos os estes teste falharem então o processo deve parar. O desenvolvedor deve ser notificado automaticamente e alguém deve ser imediatamente designado para resolver esses problemas. Quando os testes de aceitação passarem, então todos os testes não-funcionais automatizados podem ser executados. 

Aqui pode ser executados testes de Carga e segurança.

tudo ok então podemos colocar em um ambiente de testes. Supondo que seu software passa todos os testes manuais, então você está pronto para subir para produção.

### Deployment Methods

#### Entrega azul / verde

As cores Azul e Verde são apenas marcadores de posição para representar um grupo de servidores.
A estratégia azul/verde ajuda a subir novos lançamentos, minimizando o tempo de inatividade.
Você tem dois ambientes, chamados verde e azul. E você tem um roteador para escolher qual esta online.

#### Servidor Canário

Um Servidor Canário funciona como um canário das minas de Carvão, é um servidor onde colocamos uma certa porcentagem do trafego apenas para verificar seu comportamento e verificar se o novo release sobrevive.

#### Monólitos e Micro Serviços

#### Servidores mutáveis X imutáveis

Como gerenciar seus servidores, como você gerencia os softwares em execução neles?

Vejamos algumas ferramentas para ajudar neste processo

* [Ansible](https://www.ansible.com/)
* [Chef](https://www.chef.io/)
* [Puppet](https://puppet.com/)


## Continuous Integration, ou CI. 

A CI ajuda com os objetivos de eficiência em nosso desenvolvimento, implantação,  pipeline operacional e o objetivo de um software de qualidade.

O CI é um processo onde os desenvolvedores confirmam seu código ao longo do dia para um repositório compartilhado e cada commit é automaticamente construído e testado, e os resultados são enviados aos desenvolvedores. Ao criar e testar automaticamente cada commit, você pode identificar erros imediatamente.

Segue algumas etapas de um bom CI

* Ambientes espelhados
* Versionamento 
* Linters 
* Migrations
* Testes
* Build

### Versionamento

Entrega contínua e uma Cultura _DevOps_ exigem disciplina e colaboração. O processo de entrega de uma equipe disciplinada sempre começa com um _commit_.

Algumas dicas para um bom uso de versinamento

* commits de pequenas mudanças
* usar um plugin ou metodologia para ajudar a organizar melhor suas colaborações, _[git flow](https://danielkummer.github.io/git-flow-cheatsheet/index.pt_BR.html)_ é um bom exemplo disso
* Hooks de pre e pós commit
* [Versionamento Semântico](http://semver.org/lang/pt-BR/#versionamento-semntico-200)

### Build

O processo de Build é prepara o código para ser entregue em qualquer ambiente seja ele Produção, Teste, homologação ou qualquer outro ambiente.

Este processo se beneficia muito da automação um dos fundamentos da cultura _DevOps_

Podemos fazer uso de ferramentas ou scripts para automatizar este processos exemplo:

* [Jenkins](https://jenkins.io/)
* [Travis CI](https://travis-ci.org/)
* [TeamCity](https://www.jetbrains.com/teamcity/)

Scripts escritos em qualquer linguagens como:

* Shell Script
* Python
* Ruby
* Go
* PHP
* Java



### Testes

* Testes de unidade:
> práticas como TDD e refatoração dão bastante ênfase nesse tipo de teste, que exercita unidades de código isoladamente sem a necessidade de subir e aplicação inteira. Esses testes geralmente rodam bem rápido – na ordem de milissegundos – podendo ser executados com bastante frequência e fornecendo o melhor tipo de feedback para os desenvolvedores.

* Testes de integração ou testes de componente:
> exercitam uma parte da aplicação ou como ela se integra com suas dependências, por exemplo: um banco de dados, um serviço REST, uma fila de mensagens, ou até mesmo os frameworks e bibliotecas utilizados. Dependendo do componente que está sendo testado, a execução desses testes podem exigir que partes do sistema estejam rodando.

* Testes funcionais ou testes de aceitação: 
> exercitam as funcionalidades do sistema como um todo, do ponto de vista externo. Geralmente este tipo de teste exercita a interface gráfica ou simula a interação com o sistema do ponto de vista de um usuário. Esses testes geralmente são mais lentos pois exigem que a maior parte do sistema esteja rodando.


##### Fontes
> * [CloudAcademy](https://cloudacademy.com/)
> * DevOps For Dummies®, 2nd IBM Limited Edition
> * DevOps na prática - entrega de software confiável e automatizada - Casa do Codigo
