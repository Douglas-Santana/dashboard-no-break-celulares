# Projeto: Análise de Desempenho - No Break Celulares

---

## Descrição do Projeto

Este projeto de análise de dados tem como objetivo criar um **Dashboard Interativo** no Power BI para a assistência técnica **No Break Celulares**. A ferramenta permitirá monitorar e analisar o desempenho financeiro e operacional do negócio com base em dados de ordens de serviço.

---

## Objetivos do Projeto

* **Monitoramento de Faturamento:** Visualizar o faturamento total e detalhado (por serviço, peça e mão de obra) para acompanhar a saúde financeira da empresa.
* **Análise de Desempenho:** Identificar os **celulares mais frequentes e lucrativos** (marcas e modelos), ajudando a otimizar o estoque de peças e direcionar o marketing.
* **Gestão de Serviços:** Acompanhar o volume e o status de cada serviço, permitindo uma melhor gestão do fluxo de trabalho e identificação de gargalos.
* **Avaliação de Peças e Serviços:** Analisar quais peças e tipos de serviço (ex: troca de tela, troca de bateria) são os mais solicitados e geram maior receita.
* **Relatórios Dinâmicos:** Oferecer uma visão geral e detalhada do negócio, com a possibilidade de filtrar os dados por período, técnico, tipo de serviço ou forma de pagamento.

---

## O Problema de Negócio

O proprietário da **No Break Celulares** não possui uma visão clara e consolidada sobre a performance financeira e operacional da sua assistência técnica. Ele gerencia o negócio com base em informações fragmentadas, sem um painel centralizado para identificar o faturamento total, os serviços mais lucrativos e os celulares mais recorrentes. Essa falta de dados estruturados dificulta a tomada de decisões estratégicas, como a gestão otimizada de estoque de peças e a identificação de oportunidades de crescimento.

## O Contexto

A assistência técnica **No Break Celulares** lida com um volume crescente de ordens de serviço para reparo de dispositivos móveis. Atualmente, os dados de cada serviço (cliente, modelo do aparelho, tipo de reparo, peças utilizadas e valores) são registrados em uma planilha simples. Para escalar o negócio e garantir um crescimento sustentável, o proprietário precisa migrar de um modelo de gestão reativo para um modelo **orientado por dados**, que transforme as informações brutas em **insights acionáveis**.

## Premissas da Análise

* A planilha de dados fornecida é a fonte única e completa de informações para esta análise.
* O campo **`Total_Faturamento`** representa o valor final de receita para cada serviço, sendo a principal métrica de performance financeira.
* A categorização dos serviços na coluna **`Tipo_Servico`** é consistente e reflete corretamente a natureza do trabalho realizado.

---

## Estratégia de Solução

### Passo 1: Resumir o contexto em uma pergunta aberta

> Como o negócio No Break Celulares está se comportando em termos de faturamento, serviços e clientes?

### Passo 2: Transformar pergunta aberta em fechada

> É possível criar um **dashboard** que nos permita visualizar o faturamento total, identificar os serviços e celulares mais lucrativos, e monitorar o desempenho dos técnicos ao longo do tempo?

### Passo 3: Definição da coluna fato

A principal coluna fato deste projeto é o **`Total_Faturamento`**. Ela quantifica o valor da receita gerada por cada serviço, permitindo a análise de métricas financeiras essenciais como faturamento total, ticket médio e lucratividade por tipo de serviço.

### Passo 4: Identificação das dimensões

As dimensões são os atributos que dão contexto à coluna fato. Para esta análise, as dimensões mais relevantes são:

* **Tempo:** `Data_Entrada`, `Data_Saida`
* **Serviço:** `Tipo_Servico`, `Pecas_Utilizadas`, `Status_Servico`
* **Produto:** `Marca_Celular`, `Modelo_Celular`
* **Pessoas:** `Cliente`, `Tecnico`
* **Finanças:** `Forma_Pagamento`

### Passo 5: Hipóteses analíticas

* **H1:** O serviço de **Troca de Tela** é o principal responsável pela maior parte do faturamento total do negócio.
* **H2:** A marca de celular **Apple** gera o maior ticket médio por serviço, mesmo que não seja a mais reparada em volume.
* **H3:** O técnico com o maior número de serviços concluídos não é necessariamente o que gera o maior faturamento total.
* **H4:** A forma de pagamento **PIX** é a mais utilizada pelos clientes, superando o cartão e dinheiro.
* **H5:** Serviços de **Reparo em Placa** têm uma alta lucratividade, mas um volume baixo de ocorrências.

### Passo 6: Critérios de priorização

Para priorizar as hipóteses, utilizaremos os seguintes critérios:

* **Relevância de Negócio:** Qual hipótese, se confirmada, trará o maior impacto estratégico para o negócio?
* **Viabilidade Técnica:** Quão fácil é testar a hipótese com os dados disponíveis?
* **Tempo de Execução:** Qual hipótese pode ser validada mais rapidamente, gerando insights iniciais de forma ágil?

### Passo 7: Priorização das hipóteses analíticas

* **Prioridade 1 (Alta):** **H1** e **H2** - Elas têm alta relevância de negócio e viabilidade técnica, pois impactam diretamente o estoque e a estratégia de precificação.
* **Prioridade 2 (Média):** **H3** e **H4** - São importantes para a gestão de pessoal e a otimização de processos de pagamento, com viabilidade técnica moderada.
* **Prioridade 3 (Baixa):** **H5** - Embora relevante, pode ser uma análise mais complexa e que exige um volume de dados maior para ser conclusiva.

---

## Insights da Análise

* **Maior Lucratividade:** O serviço de **Troca de Tela** representa **53%** do faturamento total, confirmando a hipótese de que este é o carro-chefe do negócio.
* **Ticket Médio por Marca:** A marca **Apple** apresenta um ticket médio de R$ 350 por serviço, superando em cerca de 41% o de outras marcas como Samsung e 60% Motorola.
* **Desempenho dos Técnicos:** O técnico **Maria** lidera o faturamento total (R$ 3.120), enquanto o técnico **Pedro** tem o maior volume de serviços concluídos, demonstrando um perfil de atendimento mais rápido para serviços de menor valor.
* **Pagamento Preferido:** O **PIX** é a forma de pagamento mais popular, respondendo por 51% das transações, o que sugere a importância de priorizar este método para agilizar o fluxo de caixa.

---

## Resultados

O resultado deste projeto é um **Dashboard Interativo**, dinâmico e visualmente claro, construído no Power BI. Ele transforma a planilha de dados em um centro de inteligência de negócios, permitindo ao proprietário da No Break Celulares tomar decisões estratégicas com base em informações precisas e em tempo real. O dashboard oferece uma visão 360º da empresa, desde o faturamento consolidado até os detalhes operacionais.

---

## Visualização da Análise Completa

A visualização completa foi criada no Power BI, transformando todos os insights e resultados desta análise em gráficos e tabelas interativas, prontas para serem exploradas.
