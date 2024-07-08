# Desafio-DIO-PowerBI-Parametros

Descrição do Desafio de Projeto
Objetivo:
Criar um relatório dinâmico utilizando parâmetros no Power BI, apresentando duas visões diferentes e seguindo um storytelling para melhor compreensão dos dados.

Diretrizes
Primeira Visão: Parâmetro com base em categorias.
Segunda Visão: Parâmetros com base em valores (profit, sales, ou outros).
Estilização: Sigam a mesma estilização do relatório original.
História: Crie uma história para apresentar essa visão sobre os dados.
Passo a Passo
1. Preparação do Ambiente
Abrir o Power BI:
Carregue os dados que você utilizará para criar o relatório. Pode ser a tabela Financial Sample ou qualquer outra tabela de dados relevante.
2. Criação da Primeira Visão (Parâmetro com Base em Categorias)
Criação de Parâmetro:

Navegue até a seção de Modelagem no Power BI.
Clique em Parâmetros e selecione Novo Parâmetro.
Defina o nome do parâmetro, como "Categoria".
Adicione as categorias relevantes (por exemplo, Segment, Country, Product).
Criação da Tabela de Parâmetros:

Crie uma tabela utilizando o parâmetro para armazenar as opções de categoria.
Criação de Visualizações Dinâmicas:

Utilize o parâmetro criado para filtrar os dados com base na seleção do usuário.
Crie gráficos e tabelas que mudam dinamicamente com base na categoria selecionada.
Exemplos de gráficos: gráfico de barras para vendas por produto, gráfico de pizza para distribuição de vendas por país.
3. Criação da Segunda Visão (Parâmetro com Base em Valores)
Criação de Parâmetro:

Crie um novo parâmetro chamado "Métrica".
Adicione opções como Profit, Sales, Units Sold.
Criação de Medidas Dinâmicas:

Use a função DAX SWITCH para criar uma medida dinâmica que muda com base no parâmetro selecionado.

Métrica Selecionada = 
SWITCH(
    TRUE(),
    SELECTEDVALUE(Parâmetros[Métrica]) = "Profit", SUM(Financials_origem[Profit]),
    SELECTEDVALUE(Parâmetros[Métrica]) = "Sales", SUM(Financials_origem[Sales]),
    SELECTEDVALUE(Parâmetros[Métrica]) = "Units Sold", SUM(Financials_origem[Units Sold])
)


Criação de Visualizações Dinâmicas:

Utilize a medida dinâmica para criar gráficos que mudam com base na métrica selecionada.
Exemplos de gráficos: gráfico de linhas para tendências de vendas/profit ao longo do tempo, gráfico de barras empilhadas para comparar métricas por segmento.
4. Estilização e Storytelling
Estilização Consistente:

Utilize as mesmas cores, fontes e estilos do relatório original para manter a consistência visual.
Posicione os elementos de forma lógica e esteticamente agradável.
Storytelling:

Crie uma história que conecte as diferentes visualizações e ajude o usuário a entender os dados.
Utilize títulos, descrições e anotações para guiar o usuário através do relatório.
Exemplo de Storytelling
Título da Página: Análise de Vendas e Lucros por Categoria e Métrica

Introdução:
"Bem-vindo ao nosso relatório de análise de vendas e lucros. Aqui, você pode explorar diferentes categorias e métricas para obter insights valiosos sobre o desempenho do nosso negócio."

Seção 1: Visão por Categorias

Título: Desempenho por Categoria
Descrição: "Selecione uma categoria no menu à direita para visualizar o desempenho detalhado. Esta seção permite que você veja como diferentes segmentos, países ou produtos estão contribuindo para nossas vendas e lucros."
Gráficos: Gráfico de barras para vendas por produto, gráfico de pizza para distribuição de vendas por país.
Anotação: "Note que o produto X tem o maior volume de vendas no segmento Y, enquanto o país Z representa a maior fatia de nosso mercado."
Seção 2: Visão por Métricas

Título: Desempenho por Métrica
Descrição: "Escolha uma métrica no menu à direita para comparar diferentes aspectos de nosso desempenho financeiro. Esta seção ajuda a identificar tendências e áreas de melhoria."
Gráficos: Gráfico de linhas para tendências de vendas/profit ao longo do tempo, gráfico de barras empilhadas para comparar métricas por segmento.
Anotação: "Observe como o lucro aumentou significativamente no último trimestre, especialmente no segmento A."
Exemplo de README

# Projeto: Relatório Dinâmico de Vendas e Lucros com Power BI

## Descrição

Este projeto consiste na criação de um relatório dinâmico utilizando parâmetros no Power BI para permitir uma análise interativa e personalizada de vendas e lucros. O relatório apresenta duas visões distintas: uma baseada em categorias e outra em métricas de valores.

## Visões do Relatório

### Primeira Visão: Parâmetro com Base em Categorias
- **Descrição:** Permite ao usuário selecionar diferentes categorias como Segment, Country ou Product para analisar o desempenho.
- **Gráficos Incluídos:** Gráfico de barras para vendas por produto, gráfico de pizza para distribuição de vendas por país.

### Segunda Visão: Parâmetros com Base em Valores
- **Descrição:** Permite ao usuário selecionar diferentes métricas como Profit, Sales ou Units Sold para comparar o desempenho financeiro.
- **Gráficos Incluídos:** Gráfico de linhas para tendências de vendas/profit ao longo do tempo, gráfico de barras empilhadas para comparar métricas por segmento.

## Funcionalidades e Fórmulas DAX Utilizadas

- **Parâmetros Dinâmicos:** Criação de parâmetros para categorias e métricas.
- **Medidas Dinâmicas:** Uso da função `SWITCH` para criar medidas que mudam com base no parâmetro selecionado.

## Storytelling

### Título da Página: Análise de Vendas e Lucros por Categoria e Métrica

**Introdução:**
"Bem-vindo ao nosso relatório de análise de vendas e lucros. Aqui, você pode explorar diferentes categorias e métricas para obter insights valiosos sobre o desempenho do nosso negócio."

**Seção 1: Visão por Categorias**
- **Título:** Desempenho por Categoria
- **Descrição:** "Selecione uma categoria no menu à direita para visualizar o desempenho detalhado. Esta seção permite que você veja como diferentes segmentos, países ou produtos estão contribuindo para nossas vendas e lucros."
- **Gráficos:** Gráfico de barras para vendas por produto, gráfico de pizza para distribuição de vendas por país.
- **Anotação:** "Note que o produto X tem o maior volume de vendas no segmento Y, enquanto o país Z representa a maior fatia de nosso mercado."

**Seção 2: Visão por Métricas**
- **Título:** Desempenho por Métrica
- **Descrição:** "Escolha uma métrica no menu à direita para comparar diferentes aspectos de nosso desempenho financeiro. Esta seção ajuda a identificar tendências e áreas de melhoria."
- **Gráficos:** Gráfico de linhas para tendências de vendas/profit ao longo do tempo, gráfico de barras empilhadas para comparar métricas por segmento.
- **Anotação:** "Observe como o lucro aumentou significativamente no último trimestre, especialmente no segmento A."

## Salvamento

- O projeto foi salvo como `relatorio_dinamico_vendas_lucros.pbix`.
- As imagens das páginas foram salvas e incluídas no repositório.

## Submissão

O projeto foi submetido ao GitHub. O link do repositório é:

[Link para o repositório do GitHub](URL_do_repositório)



Conclusão
Seguindo essas etapas, conseguimos criar um relatório dinâmico e interativo no Power BI que permite uma análise aprofundada e personalizada dos dados de vendas e lucros. 
