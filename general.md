<img src="logo_ceub.jpeg" alt="Logo Ceub" width="2000" height="500">     

**Centro Universitário de Brasília - CEUB**  
**Curso de Ciência da Computação**

# FastQuest

*Website de banco de questões e questionários preparatórios para o exame da ordem*

**ANTHONY PASSOS DOS SANTOS (RA:22305281)**  
**BEATRIZ CAMPELO DA SILVA CALADO (RA:22307574)**  
**GUILHERME MAGARÃO NETO (RA:22309292)**  
**LUIZ HENRIQUE OLIVEIRA ALVES (RA:22306435)**  
**VICTOR ALBUQUERQUE CORDEIRO (RA:22309255)**  
**GABRIEL ANTONIO NAVARRO PAIVA**

**BRASÍLIA**  
**(2025)**

**TRABALHO DE PROJETO INTEGRADOR II:**  
**WEBSITE FASTQUEST**

**CONTATOS**  
luiz.alves@sempreceub.com  
beatriz.calado@sempreceub.com  
anthony.passos@sempreceub.com  
guilherme.magarao@sempreceub.com  
victor.albucorde@sempreceub.com  
gabriel.npaiva@sempreceub.com

**BRASÍLIA**  
**OUTUBRO DE 2025**

## Sumário

- [1. Introdução](#1-introdução)
  - [1.1. Público Alvo](#11-público-alvo)
  - [1.2. Contexto do Projeto](#12-contexto-do-projeto)
  - [1.3. Declaração de Uso de Inteligência Artificial](#13-declaração-de-uso-de-inteligência-artificial)
- [2. Levantamento de Requisitos](#2-levantamento-de-requisitos)
  - [2.1. Requisitos Funcionais](#21-requisitos-funcionais)
  - [2.2. Requisitos Não Funcionais](#22-requisitos-não-funcionais)
- [3. Arquitetura e Design](#3-arquitetura-e-design)
  - [3.1. Identidade Visual](#31-identidade-visual)
  - [3.2. Paleta de Cores](#32-paleta-de-cores)
- [4. Informações Técnicas](#4-informações-técnicas)
  - [4.1. Ferramentas e Tecnologias Utilizadas](#41-ferramentas-e-tecnologias-utilizadas)
  - [4.2. Estrutura dos Arquivos e Pastas](#42-estrutura-dos-arquivos-e-pastas)
  - [4.3. Estrutura do Backend](#43-estrutura-do-backend)
    - [4.3.1. Rotas e Endpoints](#431-rotas-e-endpoints)
    - [4.3.2. Banco de Dados](#432-banco-de-dados)
- [Conclusão](#conclusão)

## 1. Introdução

FastQuest é um website que tem como objetivo auxiliar estudantes e candidatos à prova da Ordem dos Advogados do Brasil (OAB) na preparação para o exame. A plataforma reúne um banco de questões organizadas por disciplina e tema, oferecendo uma ferramenta prática e acessível para o estudo direcionado e o acompanhamento do desempenho individual.

Além de centralizar questões anteriores e simulados personalizados, o site busca promover uma experiência de aprendizado dinâmica e eficiente. Com uma interface simples e intuitiva, o projeto visa apoiar o aprimoramento do raciocínio jurídico e a consolidação dos conhecimentos necessários para a aprovação no exame.

### 1.1. Público Alvo

O público primário do site é composto por estudantes e bacharéis em Direito, que têm interesse em realizar a prova da Ordem. A idade flutua principalmente entre 20 e 35 anos e os usuários necessitam de um serviço rápido e intuitivo, pois **não possuem muito tempo** disponível.

Esses usuários possuem uma rotina intensa e tempo limitado para revisar o conteúdo, valorizando plataformas que oferecem acesso rápido a questões, simulados e acompanhamento de desempenho. O site foi desenvolvido pensando nesse perfil, com o objetivo de facilitar o aprendizado, otimizar o estudo e contribuir para o sucesso na aprovação no exame da ordem.

### 1.2. Contexto do Projeto

O website foi um pedido da área de direito da universidade, pois precisa de um dinamismo na realização de atividades relacionadas ao exame. Anteriormente, as atividades eram feitas e corrigidas manualmente, o que dificulta o aprendizado e logística de entrega de atividades.

### 1.3. Declaração de Uso de Inteligência Artificial

No desenvolvimento do projeto FastQuest, foram utilizadas ferramentas de Inteligência Artificial Generativa (IA) como recurso tecnológico de apoio no processo de engenharia de software e estruturação do sistema. O uso de IA possui caráter estritamente instrumental e complementar, operando sob permanente supervisão e validação da equipe de desenvolvedores.

**Aplicação Técnica da Ferramenta:**

- **Apoio ao Desenvolvimento:** Utilização de modelos para auxílio na estruturação, refatoração e otimização do código-fonte nas linguagens adotadas no projeto (Golang no backend e Vue.js com TypeScript no frontend), além de suporte no desenho de queries relacionais e otimização para o banco de dados PostgreSQL.
- **Documentação e Modelagem:** Suporte na organização, padronização e revisão textual de documentos acadêmicos e técnicos, como o levantamento de requisitos, especificação da arquitetura e mapeamento de rotas da API (Swagger).

**Supervisão, Qualidade e Responsabilidade:**

- **Revisão e Testes:** Todo código ou estrutura proposta por IA passou por revisão manual, refatoração de regras de negócio e validação prévia antes do envio aos ambientes de desenvolvimento e produção.
- **Integridade dos Dados de Provas:** O acervo de questões, gabaritos e alternativas extraídos passou por curadoria humana para evitar discrepâncias, informações desatualizadas ou inconsistências pedagógicas ("alucinações").
- **Privacidade:** Nossos processos garantem conformidade com a LGPD. Nenhum dado pessoal dos usuários da plataforma é compartilhado ou enviado para processamento em modelos de IA externos.

## 2. Levantamento de Requisitos

### 2.1. Requisitos Funcionais

1. O sistema deve permitir a criação de novas questões com enunciado, alternativas, disciplina, assunto e resposta correta.
2. O autor deve poder atualizar e deletar questões criadas.
3. O usuário deve poder visualizar uma lista de questões disponíveis.
4. O usuário deve poder visualizar o conteúdo completo de uma questão e suas alternativas.
5. O usuário deve poder responder questões individualmente.
6. O sistema deve exibir o gabarito da questão após a resposta.
7. O sistema deve permitir a criação de listas de questões agrupadas por tema ou prova.
8. O usuário deve poder visualizar listas de questões.
9. O sistema deve permitir responder uma lista completa como um simulado.
10. O sistema deve permitir que o autor atualize e delete listas criadas.
11. O usuário deve poder definir se uma lista é pública ou privada.
12. O usuário deve poder pesquisar questões dentro de uma lista.
13. O sistema deve gerar simulados com base em provas da OAB, filtrados por ano.
14. O usuário deve poder escolher disciplinas e assuntos específicos no simulado.
15. O usuário deve poder definir a quantidade de questões no simulado.
16. O sistema deve exibir o tempo restante durante o simulado.
17. O sistema deve permitir pausar e retomar simulados.
18. O sistema deve exibir explicações ou comentários das respostas após o simulado.
19. O sistema deve apresentar o resultado final e a taxa de acertos por disciplina.
20. O sistema deve armazenar o histórico de simulados e desempenho por tema.
21. O sistema deve permitir o compartilhamento de resultados com outros usuários.
22. O sistema deve sugerir novos simulados com base no desempenho anterior.
23. O simulado deve reproduzir as condições reais da prova da OAB.
24. O sistema deve permitir ordenar resultados da pesquisa (por mais recentes, populares etc.).
25. O sistema deve permitir aplicar filtros de pesquisa por tipo de conteúdo, disciplina e assunto.
26. O sistema deve mostrar ao usuário o desempenho recente e total graficamente ou textualmente.

### 2.2. Requisitos Não Funcionais

1. O sistema deve possuir um banco de dados estruturado e migrável.
2. O backend deve ser hospedado em um ambiente estável e seguro.
3. A pesquisa deve retornar resultados de forma rápida e eficiente.
4. A interface deve ser intuitiva, permitindo fácil navegação entre listas, questões e simulados.
5. O sistema deve armazenar os dados dos usuários e resultados de forma segura.
6. O site deve simular adequadamente as condições reais de tempo e formato da prova.

## 3. Arquitetura e Design

### 3.1. Identidade Visual

A identidade visual do projeto foi desenvolvida com foco na simplicidade e na modernidade, buscando transmitir clareza e facilidade de uso desde o primeiro contato do usuário com a plataforma.

Embora o tema central esteja ligado ao Direito, uma área tradicionalmente associada à formalidade, optou-se por equilibrar essa característica com elementos visuais mais leves. Para isso, foram utilizadas imagens e ilustrações lúdicas, que tornam a experiência mais acolhedora e reduzem a rigidez comum em sites jurídicos. O resultado é uma interface que combina profissionalismo com acessibilidade, oferecendo um ambiente visualmente agradável, amigável e motivador para os estudos.

![Identidade visual](imagem-identidade-visual.png)

### 3.2. Paleta de Cores

Cada cor utilizada no projeto foi cuidadosamente selecionada, levando em conta não apenas a estética, mas também as sensações e valores que o website busca transmitir ao usuário. A paleta foi definida para reforçar a seriedade, a tradição jurídica e a clareza necessárias em uma plataforma de estudos para a OAB, além de apoiar a navegação e destacar elementos importantes da interface.

A seguir, apresenta-se a paleta de cores do projeto, acompanhada do significado atribuído a cada uma delas.

| Cor | Código | Significado no contexto do site |
| --- | --- | --- |
| **Preto** | **#000000** | Representa seriedade, autoridade e formalidade, reforçando o caráter profissional e jurídico da plataforma. |
| **Azul escuro** | **#051427** | Simboliza confiança, estabilidade e clareza, transmitindo segurança ao usuário durante o estudo e navegação. |
| **Vermelho Escuro** | **#530F1E** | Remete diretamente ao Direito, evocando tradição, força e o ambiente formal dos estudos jurídicos. |
| **Vermelho terroso** | **#A74223** | Indica foco, energia e atenção, destacando elementos importantes como botões, alertas ou áreas de ação no site. |
| **Amarelo ouro** | **#F6BD03** | Sugere destaque, motivação e progresso, sendo apropriado para indicadores de desempenho, resultados e evolução do estudante. |

## 4. Informações Técnicas

### 4.1. Ferramentas e Tecnologias Utilizadas

- **Frontend:** Vue.js, TypeScript, Tailwind;
- **Backend:** Golang, Swagger, GORM, mux;
- **Banco de Dados:** PostgreSQL.

### 4.2. Estrutura dos Arquivos e Pastas

#### Frontend

```text
.vscode/
└── extensions.json

public/
├── imgs/
└── favicon.ico

src/
├── assets/
├── components/
├── config/
├── models/
├── router/
├── views/
├── App.vue
└── main.ts

.editorconfig
.gitattributes
.gitignore
.prettierrc.json
env.d.ts
eslint.config.ts
index.html
package-lock.json
package.json
README.md
tsconfig.app.json
tsconfig.json
tsconfig.node.json
vite.config.ts
```

#### Backend

```text
database/
└── database.go

docs/
├── docs.go
├── swagger.json
└── swagger.yaml

handlers/
├── h_answers.go
├── h_question_set.go
├── h_questions.go
└── utils.go

migrations/

pkg/
├── models/
│   ├── answers.go
│   ├── comment.go
│   ├── pagination.go
│   ├── question_set.go
│   ├── question.go
│   ├── questionSource.go
│   ├── source.go
│   ├── subject.go
│   ├── topic.go
│   └── user.go
└── filtersMap.go

.gitignore
flashquest
go.mod
go.sum
main.go
README.md
router.go
```

### 4.3. Estrutura do Backend

O backend deste projeto recebe e processa todas as requisições relacionadas às questões, listas e simulados da plataforma. Cada pedido enviado pelo usuário é direcionado para uma rota específica, que aciona o controlador correspondente. O controlador interpreta os dados recebidos, chama os serviços necessários e interage com o banco de dados para criar, listar, atualizar ou remover informações, como questões, listas de questões ou respostas enviadas.

Após o processamento, o backend retorna ao cliente uma resposta estruturada em JSON contendo os dados solicitados, como questões filtradas, detalhes de uma lista ou o resultado de um simulado. Esse fluxo, baseado em rotas bem definidas, modelos estruturados e comunicação direta com o banco de dados, garante um funcionamento organizado, padronizado e eficiente em todas as funcionalidades do sistema.

#### 4.3.1. Rotas e Endpoints

Exemplo de rota:

```go
r.HandleFunc("/questions", handlers.CreateQuestion).Methods("POST")
```

**Rotas de Questões**

| Método | Endpoint | Descrição |
| --- | --- | --- |
| **POST** | `/questions` | Cria uma nova questão. |
| **GET** | `/questions` | Retorna todas as questões cadastradas. |
| **POST** | `/questions/array` | Retorna questões a partir de um conjunto de IDs fornecidos. |
| **GET** | `/questions/{id}` | Retorna os dados de uma questão específica. |
| **DELETE** | `/questions/{id}` | Remove a questão correspondente ao ID informado. |

**Rotas de Respostas**

| Método | Endpoint | Descrição |
| --- | --- | --- |
| **POST** | `/questions/{id}/answers` | Envia a resposta de uma questão. |
| **GET** | `/questions/{id}/answers` | Retorna respostas enviadas para a questão. |

**Rotas de Listas de Questões**

| Método | Endpoint | Descrição |
| --- | --- | --- |
| **POST** | `/question-sets` | Cria uma nova lista de questões. |
| **GET** | `/question-sets` | Retorna todas as listas disponíveis. |
| **GET** | `/question-sets/{id}` | Retorna os dados de uma lista específica. |
| **GET** | `/question-sets/{id}/questions` | Retorna todas as questões pertencentes à lista. |
| **GET** | `/question-sets/{id}/question-ids` | Retorna apenas os IDs das questões pertencentes à lista. |

**Rota de Acesso ao Swagger**

| Método | Endpoint | Descrição |
| --- | --- | --- |
| **GET** | `/swagger/` | Exibe a documentação interativa da API via Swagger. |

#### 4.3.2. Banco de Dados

O banco de dados do sistema foi projetado para estruturar e organizar todas as informações relacionadas às questões, listas, comentários, respostas e demais elementos que compõem a plataforma de estudos para o Exame da OAB. Ele segue um modelo relacional, garantindo consistência, integridade e flexibilidade na manipulação dos dados. A modelagem contempla diversas entidades principais, entidades de apoio e tabelas associativas responsáveis por representar relacionamentos complexos, como conexões many-to-many e registros históricos de interação dos usuários.

A entidade **User** armazena os dados essenciais dos usuários cadastrados na plataforma, incluindo identificador único, nome, email e hash de senha. Todas as ações realizadas no sistema, como criação de questões, formação de listas e envio de respostas, estão vinculadas ao usuário responsável, garantindo rastreabilidade e controle. Complementando esse núcleo, a entidade **Subject** registra as disciplinas pertinentes à OAB, enquanto a entidade **Topic** subdivide essas disciplinas em tópicos específicos, permitindo categorização mais detalhada das questões. Um relacionamento direto entre *Subject* e *Topic* possibilita organizar o conteúdo por áreas do Direito, refletindo a estrutura típica das provas.

A entidade **Question** é uma das centrais no banco, representando cada questão cadastrada. Ela armazena o enunciado, disciplina, autor responsável e metadados de criação e atualização. Essa entidade se relaciona com múltiplos elementos, refletindo a variedade de informações que podem compor uma questão. Um desses elementos é a entidade **Answer**, que contém as alternativas associadas à questão, incluindo indicação de alternativa correta. Há uma relação de um-para-muitos entre *Question* e *Answer*, permitindo que cada questão tenha várias respostas possíveis.

Além disso, o sistema permite que questões sejam ligadas a tópicos e fontes externas. Esses relacionamentos são modelados pelas tabelas associativas `question_topic` e `question_sources`, que implementam conexões many-to-many entre *Question* ↔ *Topic* e *Question* ↔ *Source*. A entidade **Source**, por sua vez, registra referências bibliográficas ou documentais das quais a questão foi retirada, armazenando informações como nome da fonte, tipo e metadados adicionais.

Outra parte fundamental do banco de dados é a entidade **Question_Set**, que representa listas de questões criadas pelos usuários. Cada lista possui nome, tipo, data de criação, indicador de privacidade, descrição e vínculo com seu autor. Essa entidade se relaciona de forma many-to-many com a entidade *Question* por meio da tabela `question_set_question`, que também registra a posição da questão dentro da lista, garantindo ordenação personalizada.

O banco também registra o histórico das interações dos usuários com as questões por meio da entidade `user_response`. Essa tabela armazena a resposta enviada, o usuário que respondeu, a questão associada, a lista (caso a resposta tenha sido dada dentro de uma lista ou simulado), se a resposta está correta e o momento em que foi realizada. Isso permite acompanhar o desempenho individual ao longo do tempo, facilitando funcionalidades como estatísticas, evolução e análise de acertos por disciplina.

A funcionalidade de comentários é suportada pela entidade **Comment**, que registra observações feitas pelos usuários sobre questões, listas ou outras entidades do sistema. Para possibilitar essa flexibilidade, o relacionamento entre comentários e os elementos comentados é administrado pela tabela `comment_relationship`, que registra o identificador do comentário, o identificador da entidade comentada e o tipo dessa entidade, funcionando como um mecanismo genérico e extensível.

De forma geral, o banco de dados foi estruturado para manter coerência entre todas as funcionalidades do sistema e garantir escalabilidade. As relações entre entidades foram definidas de forma a evitar redundâncias, enquanto tabelas associativas foram utilizadas para permitir ligações múltiplas sem perder integridade referencial. O modelo suporta eficientemente operações de consulta, criação, atualização e remoção, atendendo às necessidades de uma plataforma dinâmica e completa para estudo e prática de questões preparatórias para a OAB.

Por limitações da imagem e da formatação do documento, não foi possível colocar uma representação visual do modelo no mesmo. A imagem em questão está [neste link](https://drive.google.com/file/d/1KK0DOqvJzr491I0rXzDwXYPtAylKSE6A/view?usp=drive_link).

## Conclusão

O projeto apresentou uma plataforma completa e funcional para estudo e resolução de questões preparatórias para o Exame da OAB, integrando recursos de criação, organização e realização de simulados de forma dinâmica e acessível.

A estrutura visual simples e moderna, combinada com um backend robusto e um banco de dados bem modelado, garante eficiência no uso e clareza na navegação. As funcionalidades implementadas permitem ao usuário acompanhar seu desempenho, revisar conteúdos e personalizar seus estudos, resultando em uma ferramenta eficaz e coerente com os objetivos propostos. O sistema cumpre plenamente sua finalidade ao oferecer um ambiente intuitivo, organizado e tecnicamente sólido para apoiar a preparação dos candidatos.

Como desfecho, o projeto firma a base para futuras evoluções, como novas formas de recomendação de estudo, análise aprofundada de desempenho e ampliação do acervo de questões e funcionalidades colaborativas. Dessa forma, além de atender às demandas atuais, a plataforma se mantém aberta para aprimoramentos contínuos e maior impacto no processo de preparação para o exame.
