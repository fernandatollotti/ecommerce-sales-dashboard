# Dashboard de Business Intelligence (BI) para E-commerce

![Status](https://img.shields.io/badge/status-concluído-brightgreen)
![Tool](https://img.shields.io/badge/Ferramenta-Google%20Sheets-blue)
![Analysis](https://img.shields.io/badge/Análise-KPIs%20|%20Gestão%20de%20Receita-orange)
![License](https://img.shields.io/badge/Licença-MIT-yellow)

**O Dashboard de BI** demonstra a **aplicação prática de análise de dados para otimizar a gestão de um e-commerce.** Desenvolvido como uma ferramenta interativa no Google Sheets, ele transforma dados brutos de pedidos em **KPIs** e **insights visuais** essenciais para tomada de decisão.

---

## Tabela de Conteúdos
* [Visão geral do Dashboard](#visão-geral-do-dashboard)
* [Dados Utilizados](#dados-utilizados)
* [Principais Métricas (KPIs)](#principais-métricas-kpis)
* [Estrutura e Interatividade](#estrutura-e-interatividade)
* [Desafios](#desafios)
* [Ferramentas e Tecnologias](#ferramentas-e-tecnologias)
* [Guia de execução](#guia-de-execução)

---

## Visão geral do Dashboard

**O Dashboard** foi arquitetado para fornecer aos gestores uma visão clara e imediata das alavancas do negócio, com foco em métricas de vendas e eficiência operacional:

* **Análise Temporal (Sazonalidade):** Permite rastrear a performance da Receita Líquida ao longo dos meses, identificando picos de vendas e a tendência geral (Revenue Trend).
* **Ranking de Produtos:** Destaca as categorias **Top Categories by Revenue** e **Volume by Category**, essencial para orientar o estoque e as estratégias de marketing.
* **Métricas Financeiras:** Monitora o **Total Revenue**, **Total Orders** e o crucial **Average Order Value (AOV)** para avaliar a saúde financeira da operação.

---

## Dados Utilizados

O dashboard utiliza o arquivo `sales_report` (uma simulação de dados transacionais de e-commerce) como base.

| Coluna | Descrição | Utilização na Análise |
| :--- | :--- | :--- |
| **ORDER ID** | Identificador único de cada pedido. | Essencial para a contagem de **Total Orders** e para o cálculo do **AOV**. |
| **ORDER DATE** | Data em que o pedido foi realizado. | Base para a criação das dimensões **Mês** e **Ano** e para a análise de Tendência. |
| **PRODUCT CATEGORY** | Categoria do produto vendido. | Dimensão chave para o ranking de **Revenue by Category** e **Volume by Category**. |
| **REVENUE** | Valor total (receita bruta) do item no pedido. | Base para o cálculo de **Total Revenue** e **AOV**. |
| **...** | Outras colunas transacionais que compõem o conjunto de dados. | Usadas nas Tabelas Dinâmicas para garantir o cálculo correto de métricas. |

---

## Principais Métricas (KPIs)

A tela principal do dashboard é construída em torno dos seguintes indicadores de alto impacto:

| KPI | Nome Técnico | Objetivo de Negócio |
| :--- | :--- | :--- |
| **Receita Total** | Net Revenue | Mede o desempenho financeiro global no período. |
| **Total de Pedidos** | Total Orders | Mede o volume de transações e a escala da operação. |
| **Ticket Médio** | AOV (Average Order Value) | Mede a eficiência de vendas por pedido, crucial para otimizar *upselling* e margem. |

---

## Estrutura e Interatividade

O dashboard foi desenvolvido para ser totalmente interativo, permitindo que o usuário filtre todos os gráficos e KPIs simultaneamente:

* **Controle de Dados (Slicer):** Foi implementado um **Controle de Dados Mestre**, vinculado ao campo **ORDER YEAR**, permitindo o filtro rápido por ano em todos os gráficos e Tabelas Dinâmicas.
* **Visualizações:** O layout utiliza Gráfico de Linha (Tendência), Gráficos de Barras (Rankings) e KPI Cards para máxima clareza e rápida leitura.

---

## Desafios

A construção do dashboard exigiu a **Modelagem de Dados** e o tratamento de informações para garantir a integridade e a correta visualização dos dados de vendas:

* **Ordenação Temporal:** Foi necessário modelar o tempo (mês e ano) usando funções de data. Isso garante que o gráfico de tendência seja **ordenado cronologicamente** (Janeiro, Fevereiro...) e não alfabeticamente.
* **Cálculos Confiáveis:** O cálculo preciso do ticket médio (AOV) foi estabelecido por meio de uma Tabela Dinâmica configurada para combinar a **soma da receita** com a **contagem de pedidos**.

---

## Ferramentas e Tecnologias

* **Plataforma:** Google Sheets
* **Fonte de Dados:** Kaggle
* **Habilidades:** tabelas dinâmicas, slicer, validação de dados, linguagem de fórmulas.

---

## Guia de execução

Para quem deseja interagir com o dashboard e entender sua construção:

1.  **Acesso:** Abra o arquivo `sales_report` (a planilha principal).
2.  **Visualização:** Navegue até a aba **"Dashboard"** para ver os KPIs e gráficos. Use o **controle de dados**, localizado no topo, para filtrar os resultados por **ano do pedido (ORDER YEAR)**.
3.  **Reprodução:** As **tabelas dinâmicas** (que alimentam o dashboard) estão na aba **"Calculations"**. 
