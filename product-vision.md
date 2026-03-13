# **FastQuest \- Visão do Produto**

**Data:** 24/02/2026

## **Observações**

* **O documento de visão deverá ser revisado por diversos envolvidos no projeto**, portanto, mantenha o nível de detalhes gerais suficiente para que todos possam entender. No entanto, ofereça detalhes suficientes para fornecer à equipe as informações necessárias para a modelagem da solução.  
* Caso algum tópico não seja aplicável para o contexto do projeto, o seguinte texto deverá ser inserido logo abaixo do título do tópico: "**Não se aplica**."

## **Sumário**

* [1. Introdução](#1-introdução)  
  * [1.1 Escopo e Alinhamento Estratégico](#11-escopo-e-alinhamento-estratégico)  
  * [1.2 Definições, Acrônimos e Abreviações](#12-definições-acrônimos-e-abreviações)  
* [2. Análise de Contexto](#2-análise-de-contexto)  
  * [2.1 Detalhamento da Necessidade](#21-detalhamento-da-necessidade)  
  * [2.2 Alternativas](#22-alternativas)  
* [3. Partes Interessadas](#3-partes-interessadas)  
  * [3.1 Partes Interessadas](#31-partes-interessadas)  
  * [3.2 Detalhamento dos Representantes das Partes Interessadas](#32-detalhamento-dos-representantes-das-partes-interessadas)  
  * [3.3 Usuários](#33-usuários)  
  * [3.4 Necessidades das Partes Interessadas ou Usuários](#34-necessidades-das-partes-interessadas-ou-usuários)  
* [4. Objetivos de Negócio](#4-objetivos-de-negócio)  
* [5. Visão Geral do Produto](#5-visão-geral-do-produto)  
  * [5.1 Perspectiva do Produto](#51-perspectiva-do-produto)  
  * [5.2 Características-Chave do Produto](#52-características-chave-do-produto)  
  * [5.3 Suposições e Dependências](#53-suposições-e-dependências)  
  * [5.4 Custos](#54-custos)  
  * [5.5 Outros Requisitos do Produto](#55-outros-requisitos-do-produto)  
* [6. Categorização do Projeto](#6-categorização-do-projeto)  
* [7. Restrições](#7-restrições)  
* [8. Riscos](#8-riscos)  
* [9. Documentos de Referência](#9-documentos-de-referência)

# **1\. Introdução**

Um projeto de software é algo complexo por natureza, e o seu sucesso dependerá de inúmeros fatores. Este documento tem por objetivo trazer clareza quanto à necessidade de desenvolver o FastQuest, disponibilizando detalhes sobre as características-chave necessárias para o produto, partes interessadas, restrições e riscos, dentre outras informações relevantes para entendimento da necessidade e do que se pretende alcançar com o projeto.

## **1.1 Escopo e Alinhamento Estratégico**

Este documento de visão delimita as fronteiras do **MVP (Produto Mínimo Viável)** do sistema **FastQuest**, estabelecendo as funcionalidades essenciais para a validação da plataforma de simulados. O documento define o caminho estratégico para a entrega da primeira versão funcional ao cliente, garantindo que o núcleo do sistema — composto pela gestão de questões, questionários e simulados — esteja alinhado às necessidades de estudantes e professores de Direito. Além disso, o escopo abrange o **monitoramento e análise de desempenho**, permitindo que o usuário visualize sua evolução com base nos resultados obtidos, consolidando o FastQuest como uma ferramenta estratégica para a aprovação.

## **1.2 Definições, Acrônimos e Abreviações**

* **MVP (Minimum Viable Product):** Produto Mínimo Viável; a versão mais simples do FastQuest que pode ser lançada com as funcionalidades essenciais.

# **2\. Análise de Contexto**

## **2.1 Detalhamento da Necessidade**

### **2.1.1 Descrição do Problema**

Atualmente, professores e acadêmicos de Direito enfrentam barreiras significativas na preparação para o Exame de Ordem (OAB). O problema central reside na fragmentação de informações: embora existam bases de questões online, falta um ambiente integrado que permita a criação ágil de simulados e listas de exercícios personalizados.

Para os professores, isso resulta em um processo manual exaustivo de curadoria e formatação de avaliações. Para os alunos, a dificuldade está em centralizar provas anteriores e, principalmente, em obter uma análise precisa de desempenho por disciplina, tornando o estudo menos estratégico. O cenário atual carece de uma ferramenta que automatize a organização dessas questões e forneça métricas claras de evolução.

### **2.1.2 Parte(s) afetada(s)**

**1\. Estudantes de Direito (Interna/Direta)**

* **Como são afetados:** Atualmente perdem tempo organizando questões manualmente em PDFs ou sites lentos, sem conseguir identificar quais matérias precisam de mais estudo (ex: Ética vs. Direito Civil).  
* **Por que:** A falta de uma ferramenta de análise de desempenho impede um estudo focado, resultando em menor eficiência na preparação para a OAB.

**2\. Professores e Coordenadores de Curso (Interna/Direta)**

* **Como são afetados:** Gastam horas semanais na curadoria e formatação de simulados e listas de exercícios para os alunos.  
* **Por que:** A ausência de um sistema de gestão de questões centralizado exige um trabalho manual repetitivo de busca e diagramação de provas anteriores.

**3\. Instituições de Ensino / Núcleos de Prática Jurídica (Externa/Indireta)**

* **Como são afetadas:** Podem apresentar índices de aprovação na OAB abaixo do potencial da instituição.  
* **Por que:** Sem dados precisos sobre o desempenho coletivo dos alunos, a coordenação não consegue ajustar a grade curricular ou focar em reforços nas disciplinas onde os alunos têm mais dificuldade.

### **2.1.3 Impacto**

1. **Perda de Produtividade Acadêmica:** O tempo que professores e alunos gastam selecionando questões manualmente e formatando documentos poderia ser utilizado no ensino e aprendizado real. O impacto é um ciclo de preparação ineficiente e burocrático.  
2. **Baixa Assertividade no Estudo:** Sem uma análise de desempenho centralizada, o aluno estuda "no escuro". O impacto direto é a dificuldade em identificar pontos fracos, o que pode levar a reprovações no Exame de Ordem e ao aumento da ansiedade do estudante.  
3. **Defasagem Tecnológica:** A dependência de métodos manuais ou sites de difícil navegação gera um impacto negativo na imagem da instituição ou do método de ensino, que deixa de utilizar o potencial de processamento de dados (como o oferecido pelo PostgreSQL e Go) para personalizar a educação.  
4. **Custo de Oportunidade:** Para o professor, o impacto é o custo de oportunidade: o tempo gasto "montando" um simulado impede que ele foque na análise pedagógica dos erros dos alunos ou na criação de conteúdos inéditos.

### **2.1.4 Solução de Sucesso**

**1\. Características Principais**

* **Centralização de Dados:** Um banco de dados robusto em PostgreSQL contendo o histórico de questões da FGV/OAB de forma organizada.  
* **Alta Performance:** Backend em Go (Golang) capaz de processar grandes volumes de questões e gerar simulados instantaneamente, sem latência para o usuário.  
* **Interface Intuitiva:** Frontend em Vue.js focado na experiência do estudante, evitando distrações e facilitando a navegação entre matérias.

**2\. Recursos Estratégicos (Features)**

* **Gerador Automático de Simulados:** Ferramenta que permite ao professor ou aluno criar testes personalizados por disciplina ou ano, eliminando o trabalho manual de formatação.  
* **Dashboard de Desempenho:** Painel visual com métricas de acertos, erros e tempo médio por questão (ex: gráficos de evolução por matéria).  
* **Sistema de Logs e Progresso:** Persistência de cada tentativa do aluno para que ele possa retomar o estudo de onde parou.

**3\. Benefícios de Negócio**

* **Economia de Tempo:** Redução drástica do tempo gasto por professores na montagem de avaliações.  
* **Estudo Direcionado:** O aluno para de estudar "no escuro" e foca exatamente nas disciplinas onde seu desempenho é menor (ex: focando em Ética se o dashboard mostrar baixo rendimento).  
* **Escalabilidade:** A arquitetura permite que o sistema cresça em número de usuários e questões sem perda de qualidade ou velocidade.

## **2.2 Alternativas**

Durante a concepção do FastQuest, analisamos o mercado para identificar como estudantes e professores de Direito resolvem o problema da preparação para a OAB atualmente. Embora existam diversas ferramentas e métodos disponíveis, notamos que as soluções se dividem entre processos manuais exaustivos ou plataformas engessadas e custosas. Abaixo, listamos as principais alternativas mapeadas, destacando seus pontos fortes e as lacunas que justificam a criação do FastQuest:

### **2.2.1 Status Quo (Processo Manual / Google Workspace)**

* **Descrição:** Professores utilizam o Google Forms ou Word para criar simulados e os alunos buscam provas em PDFs no site da FGV.  
* **Pontos Fortes:** Custo zero imediato e familiaridade com as ferramentas (Google Docs/Forms).  
* **Pontos Fracos:** Trabalho manual exaustivo para o professor; impossibilidade de gerar métricas automáticas de desempenho para o aluno; dificuldade em organizar um banco de dados histórico crescente.

### **2.2.2 Plataformas de Questões Genéricas (Ex: Qconcursos, Gran Cursos)**

* **Descrição:** Sites de larga escala que possuem milhares de questões de diversos concursos.  
* **Pontos Fortes:** Banco de dados imenso e recursos avançados de filtros.  
* **Pontos Fracos:** Muitas vezes possuem interfaces poluídas e genéricas; custo de assinatura elevado para o estudante; não permitem que o professor da instituição crie e gerencie seus próprios simulados personalizados para sua turma específica dentro da plataforma.

### **2.2.3 Software Livre / Repositórios de Provas**

* **Descrição:** Utilização de bancos de questões abertos ou repositórios de arquivos.  
* **Pontos Fortes:** Transparência e acesso gratuito aos dados.  
* **Pontos Fracos:** Falta de uma interface integrada (Frontend em Vue) e de uma lógica de backend robusta (como a que você está fazendo em Go) para processar o progresso do usuário de forma amigável.

# **3\. Partes Interessadas**

O sucesso do FastQuest depende do alinhamento entre as expectativas de quem ensina, quem estuda e quem mantém a plataforma. Esta seção mapeia todos os perfis (stakeholders e usuários finais) que interagem com o sistema, detalhando suas principais necessidades, responsabilidades e os problemas que a aplicação visa resolver para cada um deles.

## **3.1 Partes Interessadas**

| Unidade | Representada por | Envolvimento com o projeto |
| :---- | :---- | :---- |
| **Aluno / Estudante de Direito** | Estudantes | Quem consome os simulados. |
| **Professor / Coordenador** | Docentes | Quem cria os simulados e avalia o desempenho. |

## **3.2 Detalhamento dos Representantes das Partes Interessadas**

| Atributo | Detalhe |
| :---- | :---- |
| **Nome** | *\<nome da pessoa que representa a parte interessada\>* |
| **E-mail institucional** | *\<e-mail institucional do representante\>* |
| **Responsabilidades** | *\<Listar as principais responsabilidades da parte interessada no projeto. Ex: Responsável por fornecer requisitos, validar funcionalidades. Se não houver, colocar "não se aplica"\>* |

## **3.3 Usuários**

| Atributo | Aluno / Estudante de Direito (Usuário Comum) |
| :---- | :---- |
| **Representante(s)** | Estudantes em preparação para o Exame da OAB ou Centros Acadêmicos. |
| **Descrição** | É o usuário principal e foco da experiência de uso (frontend). Precisa de uma interface intuitiva, rápida e sem distrações para resolver questões e acompanhar sua evolução rumo à aprovação. |
| **Responsabilidades** | Resolver questões individuais; executar simulados dentro do tempo estipulado; acompanhar seu próprio dashboard de desempenho; reportar eventuais erros ou desatualizações. |

| Atributo | Professor / Mentor (Usuário Especialista) |
| :---- | :---- |
| **Representante(s)** | Professores universitários, mentores de estudos ou coordenadores de cursos preparatórios. |
| **Descrição** | Interage com o sistema de forma mais estratégica. Utiliza a plataforma como ferramenta pedagógica para otimizar seu tempo de curadoria de material e obter dados reais sobre onde os alunos estão errando mais. |
| **Responsabilidades** | Criar listas de exercícios e simulados personalizados; acessar painéis de estatísticas de desempenho coletivo ou individual; cadastrar novas questões autorais ou sugerir anulações. |

| Atributo | Administrador do Sistema (Superusuário) |
| :---- | :---- |
| **Representante(s)** | Equipe de Desenvolvimento / Mantenedor do Software. |
| **Descrição** | É o responsável por garantir a saúde técnica do ecossistema. Interage com ferramentas de gestão técnica e diretamente com o banco de dados e a infraestrutura do servidor. |
| **Responsabilidades** | Importar blocos massivos de questões de provas anteriores da FGV; gerenciar níveis de permissão; monitorar logs de erro da API; emitir relatórios de uso e métricas gerais. |

## **3.4 Necessidades das Partes Interessadas ou Usuários**

### **3.4.1 Automação na Criação de Simulados**

| Atributo | Detalhe |
| :---- | :---- |
| **Parte(s) Interessada(s)** | Professores e Alunos |
| **Motivadores** | Reduzir drasticamente o tempo gasto selecionando questões uma a uma para montar uma prova com a distribuição correta de matérias. É uma melhoria fundamental na forma de estudo e trabalho. |
| **Situação atual** | Professores e alunos baixam PDFs gigantes de provas anteriores da FGV, procuram as disciplinas, recortam as questões e colam em documentos do Word ou formulários do Google Forms para criar um teste. |
| **Solução ideal** | Uma interface no sistema onde o usuário seleciona filtros (como ano, banca e disciplina), define a quantidade de questões, e o sistema gera o simulado dinamicamente na tela, pronto para ser respondido ou exportado. |

### **3.4.2 Mapeamento Direcionado de Desempenho**

| Atributo | Detalhe |
| :---- | :---- |
| **Parte(s) Interessada(s)** | Alunos (e Professores acompanhando turmas). |
| **Motivadores** | Identificar com precisão milimétrica os pontos fracos do estudante para direcionar as revisões, resolvendo o problema de "estudar no escuro". |
| **Situação atual** | O aluno resolve a prova, corrige manualmente olhando o gabarito em PDF e anota os acertos em um caderno ou planilha do Excel. Muitas vezes ele sabe que foi mal na prova, mas não tem a granularidade de saber exatamente em qual matéria. |
| **Solução ideal** | Um painel (dashboard) automático que processe as respostas e gere relatórios visuais. Ex: O sistema identifica que o aluno acerta bem Ética (questões 1 a 8), mas que seu rendimento cai em Filosofia (9 e 10), gerando um alerta automático de reforço. |

### **3.4.3 Importação em Massa e Gestão do Banco de Questões**

| Atributo | Detalhe |
| :---- | :---- |
| **Parte(s) Interessada(s)** | Administrador do Sistema (Equipe de Desenvolvimento/Conteúdo). |
| **Motivadores** | O Exame de Ordem possui um acervo histórico gigante e ganha novas edições anualmente. A inserção manual de cada questão é inviável, gera gargalos de tempo e está sujeita a falhas. |
| **Situação atual** | Sem um mecanismo automatizado, o administrador precisa copiar e colar os dados de PDFs da FGV diretamente em painéis web lentos ou escrever scripts SQL gigantescos manualmente. |
| **Solução ideal** | Desenvolvimento de uma rotina no backend que permita o upload de arquivos estruturados (JSON/CSV). O sistema deve ser capaz de ler, validar a formatação, categorizar as disciplinas e inserir milhares de questões simultaneamente no banco de dados. |

# **4\. Objetivos de Negócio**

| Objetivo de negócio | Descrição |
| :---- | :---- |
| **Reduzir o tempo de criação de simulados em 80%** | Substituir o processo manual de busca e formatação de provas em PDFs por um gerador automatizado. O sucesso será medido pela capacidade de gerar um caderno personalizado em menos de 2 minutos. |
| **Garantir 100% de precisão no diagnóstico de desempenho** | Entregar um painel analítico que detalhe o rendimento exato do usuário, distinguindo rigorosamente as disciplinas do Exame de Ordem, permitindo revisão direcionada. |
| **Alcançar alta disponibilidade no processamento** | Estabelecer uma infraestrutura backend capaz de processar e entregar simulados sem lentidão. A meta é garantir que as requisições tenham latência inferior a 300ms, especialmente nas semanas de pico. |

# **5\. Visão Geral do Produto**

Esta seção fornece uma visualização de alto nível das capacidades do produto, interfaces para outros aplicativos e configurações dos sistemas.

## **5.1 Perspectiva do Produto**

O FastQuest atua como uma plataforma independente (standalone) do ponto de vista de negócio, operando como uma solução completa em si mesma (SaaS \- Software as a Service) para o preparo no Exame da OAB. Do ponto de vista arquitetural e de engenharia, o produto é um sistema web distribuído:

* **Frontend (Interface do Usuário):** Aplicação Web desenvolvida com o framework Vue.js, atuando como o ponto de contato direto com alunos e professores. É responsável por renderizar os simulados, capturar as interações e exibir os painéis de desempenho.  
* **Backend (API Central):** Serviço desenvolvido em Go (Golang) que atua como o "cérebro" do sistema. Recebe as requisições via rede (HTTP/REST), aplica as regras de negócio e gerencia a segurança e autenticação.  
* **Persistência de Dados:** Servidor de banco de dados relacional PostgreSQL, que interage exclusivamente com a API em Go, armazenando de forma estruturada o acervo histórico, provas e logs.

## **5.2 Características-Chave do Produto**

| Característica-chave | Descrição | Prioridade |
| :---- | :---- | :---- |
| **Gerador Dinâmico de Simulados** | Criação automatizada de cadernos de prova customizáveis focados no padrão FGV/OAB, permitindo filtros por disciplina e ano, com uma interface construída em Vue.js. | Alta |
| **Motor de Análise de Desempenho** | Processamento contínuo do histórico de resoluções para gerar dashboards com métricas precisas de acertos e erros por matéria, mapeando os pontos fracos do estudante. | Alta |
| **Alta Disponibilidade e Baixa Latência** | Arquitetura de backend de alta performance projetada em Go, garantindo respostas rápidas nas buscas do banco de dados (PostgreSQL) e suportando múltiplos acessos. | Alta |
| **Banco e Busca Avançada** | Acervo centralizado com todas as provas da OAB, equipado com um sistema de busca flexível (por edição, ano, disciplina ou textual direta no enunciado). | Alta |

### **5.2.1 Requisitos não Funcionais**

| Tipo | Descrição | Prioridade |
| :---- | :---- | :---- |
| **Desempenho** | O tempo de resposta da API para buscas de questões e geração de simulados deve ser inferior a 500ms. | Alta |
| **Usabilidade** | A interface em Vue.js deve ser responsiva (adaptável a celulares, tablets e desktops) e livre de poluição visual. | Alta |
| **Segurança** | Rotas protegidas por autenticação (ex: tokens JWT). Senhas armazenadas de forma criptografada (hash) no PostgreSQL. | Alta |
| **Disponibilidade** | Arquitetura estável (Go) para garantir um alto tempo de atividade (uptime), especialmente nos meses de pico. | Alta |
| **Manutenibilidade** | Código-fonte modular seguindo boas práticas de engenharia de software para facilitar futuras melhorias (como IA). | Média |

## **5.3 Suposições e Dependências**

* **Suposição de Formato de Dados (FGV/OAB):** Supõe-se que a FGV manterá o padrão estrutural do Exame de Ordem (múltipla escolha com 4 alternativas, divisão por disciplinas). Mudanças drásticas exigiriam refatoração.  
* **Suposição de Acesso:** Supõe-se que os usuários possuam acesso à internet de banda larga para consumir os simulados via navegador web, sem necessidade de instalação local.  
* **Dependência de Infraestrutura:** O projeto depende da manutenção das tecnologias de código aberto utilizadas (**Go, Vue.js e PostgreSQL**).

## **5.4 Custos**

* **Licenciamento de Software:** Zero Custo. Uso de tecnologias Open Source.  
* **Hospedagem Frontend:** Plataformas como Vercel ou Netlify (custo inicial zero/Free Tier).  
* **Hospedagem Backend e DB:** Servidores virtuais (VPS) ou nuvem (AWS, Render). Estimativa inicial em torno de US$ 5 a US$ 15 mensais, devido à alta performance do Go.  
* **Domínio:** Custo anual recorrente (ex: Registro.br, média de R$ 40,00/ano).

## **5.5 Outros Requisitos do Produto**

### **5.5.1 Padrões e Normativos Aplicáveis**

| Padrão ou normativo | Descrição | Acesso |
| :---- | :---- | :---- |
| **LGPD (Lei nº 13.709/2018)** | Regulamenta o tratamento de dados pessoais. O sistema deve garantir privacidade e segurança dos dados cadastrais e desempenho. | planalto.gov.br |
| **Edital do Exame (OAB/FGV)** | Normativo que dita as regras de negócio. O gerador deve estar em conformidade com as diretrizes do edital vigente. | oab.fgv.br |
| **WCAG 2.1 (Acessibilidade)** | Padrões de acessibilidade. A interface deve seguir diretrizes para ser utilizável por estudantes com deficiências. | w3.org/WAI |

### **5.5.2 Requisitos da Solução**

| Tipo | Descrição | Quantidade |
| :---- | :---- | :---- |
| **S.O. (Servidor)** | Distribuição Linux (ex: Ubuntu Server, Debian ou Alpine para Docker). | 1 (Instância/VPS) |
| **Processamento** | Processador virtual (vCPU) para rodar a API em Go. | 1 a 2 vCPUs |
| **Memória RAM** | Memória para sustentar a API e o banco. | 2 GB a 4 GB |
| **SGBD** | Instalação do PostgreSQL para persistência relacional. | 1 (Instância) |
| **Armazenamento** | Disco SSD para o banco de dados e arquivos. | 20 GB a 40 GB |
| **API de Terceiros** | Chave de acesso para a API do Gemini (LLM) para módulo de IA. | 1 (Conta/Projeto) |

### **5.5.3 Requisitos de Documentação**

| Tipo | Descrição | Formato |
| :---- | :---- | :---- |
| **Documentação da API** | Mapeamento completo dos endpoints em Go, rotas, geração de simulados. Deve incluir exemplos (JSON). | Web (Swagger / OpenAPI) |
| **Guia de Implantação** | Instruções de infraestrutura, variáveis de ambiente, DB e build do frontend. | Markdown (README.md) |
| **Manual de Operação** | Guia focado na gestão pedagógica (Professor e Admin) para gerar provas, extrair relatórios, etc. | PDF ou Wiki interna |
| **Onboarding Rápido** | Tutorial interativo para o Estudante na primeira utilização do sistema. | Tooltips integrados |

# **6\. Categorização do Projeto**

| Categoria | Descrição |
| :---- | :---- |
| **Novo Produto** | O projeto classifica-se como "Novo Produto", pois tem como objetivo a construção de uma nova plataforma educacional para atender à demanda de preparação para a OAB. Visa a informatização completa de processos que hoje são manuais. |

# **7\. Restrições**

| Tipo | Nome | Descrição |
| :---- | :---- | :---- |
| **Financeira** | Orçamento Limitado | O projeto não possui financiamento inicial. O ambiente de produção deve caber em *Free Tiers* ou instâncias de baixíssimo custo durante o MVP. |
| **Infraestrutura** | Stack Fixada | Restrito ao uso de **Go** (backend), **Vue.js** (frontend) e **PostgreSQL** (DB). |
| **Regulamentar** | Padrão FGV/OAB | O modelo de dados está amarrado à estrutura atual do Exame de Ordem (4 alternativas, etc). Alterações oficiais exigirão refatoração. |

# **8\. Riscos**

*\<Instrução: Lista todos os riscos percebidos que podem impactar o alcance do objetivo do projeto.\>*

| Nome do Risco | Tipo do Risco | Probabilidade | Impacto |
| :---- | :---- | :---- | :---- |
| **Dificuldade na Extração de Dados (PDFs)** | Operacional / Técnico | Alta | Alto |
| **Custos Imprevistos com API de IA** | Financeiro | Média | Médio |
| **Mudança Estrutural no Edital (OAB/FGV)** | Negócio | Baixa | Alto |
| **Falha na Hospedagem Gratuita** | Infraestrutura / Técnico | Baixa | Médio |

