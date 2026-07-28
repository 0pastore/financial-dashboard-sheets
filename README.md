# Dashboard de Orçamento Mensal & Controle Financeiro

Um painel simples de controle financeiro dinâmico e automatizado desenvolvido no **Google Sheets**, criado para centralizar o rastreamento de receitas, despesas (fixas e variáveis) e investimentos com foco em tomada de decisão e planejamento de médio prazo.

---------------------------------

## Funcionalidades Principais

* **Filtros Dinâmicos Temporais:** Visualização instantânea dos dados filtrados por **Ano** e **Mês específico**, além da opção de consolidado anual.
* **Visão Macro e Micro:** 
  * *Gráfico Esquerdo (Macro):* Agrupamento por grandes categorias (Receitas, Despesas Fixas, Despesas Variáveis e Investimentos).
  * *Gráfico Direito (Micro):* Detalhamento por subcategorias para análise profunda dos gastos (ex: custos com projetos pessoais, transporte, lazer, etc.).
* **Tabelas de Apoio Escaláveis:** Uso de funções avançadas para garantir que novas categorias adicionadas reflitam automaticamente no painel sem quebra de layout.

---------------------------------

## Tecnologias e Conceitos Aplicados

Este projeto utiliza ferramentas de manipulação de dados em planilhas eletrônicas:
* **Funções e Soma Condicional:** Uso de `SOMARPRODUTO` para simular lógica relacional de banco de dados sem perda de performance.
* **Tratamento de Textos com Expressões Regulares (`REGEXMATCH`):** Aplicação de padrões Regex (`"Despesas|Investimentos"`) para capturar múltiplas condições de texto ("OU") de forma limpa e otimizada.
* **Validação de Dados Dinâmica:** Uso de `=UNIQUE()` para alimentar listas suspensas e tabelas auxiliares a partir da fonte primária.
* **Desenvolvimento Assistido**: Google Gemini (utilizado para modelagem de fórmulas, tratamento de matrizes e arquitetura de dados do painel).

---------------------------------

## Arquitetura da Planilha

O projeto é estruturado em três abas principais:
1. **`Lançamentos`:** O banco de dados bruto onde são registradas as transações (Data, Descrição, Categoria, Subcategoria e Valor).
2. **`Configurações`:** A base paramétrica contendo as listas padronizadas de categorias e subcategorias.
3. **`Dashboard`:** O painel visual executivo contendo os Cartões de KPI (Total de Entradas, Total de Saídas e Saldo Atual), seletores de data e os gráficos dinâmicos de rosca.

---------------------------------

## Destaques Técnicos & Aprendizados
O desenvolvimento deste projeto permitiu exercitar a modelagem de dados, tratamento de erros de tipo em funções e a criação de interfaces limpas focadas em usabilidade e clareza financeira.
