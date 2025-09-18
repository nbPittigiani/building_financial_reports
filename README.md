# Análise de Índices Financeiros para Empresas de Capital Aberto

## 📝 Visão Geral do Projeto

Este projeto tem como objetivo principal apoiar a tomada de decisão de um gestor de *hedge fund*, transformando dados brutos de demonstrativos financeiros em indicadores de performance acionáveis. A partir de planilhas de Balanço Patrimonial e Demonstrativo de Resultados, o script calcula importantes índices de alavancagem e lucratividade para empresas de diferentes setores.

A análise final responde a questões críticas sobre qual setor possui a menor lucratividade, qual apresenta a maior alavancagem e qual a relação entre esses dois indicadores em um setor específico.

## 📊 Fonte de Dados

Foram utilizados dois arquivos como fonte de dados:
-   `Balance_Sheet.xlsx`: Contém informações do balanço patrimonial, como Dívida Total (`Total Liab`) e Patrimônio Líquido (`Total Stockholder Equity`).
-   `Income_Statement.xlsx`: Contém informações da demonstração de resultados, como Lucro Bruto (`Gross Profit`) e Receita Total (`Total Revenue`).

Ambos os datasets incluem dados de empresas dos setores de **tecnologia (`tech`)**, **bens de consumo não duráveis (`fmcg`)** e **imobiliário (`real_est`)** ao longo de diferentes anos.

## 🚀 Metodologia

O processo de análise foi estruturado da seguinte forma:

1.  **Carregamento de Dados:** Leitura dos arquivos `.xlsx` utilizando a biblioteca Pandas.
2.  **Engenharia de Features (Cálculo de Índices):** Foram criados dois indicadores financeiros fundamentais:
    -   **Índice de Alavancagem (Leverage Ratio):** Calculado pela fórmula:
        $$
        \\text{Alavancagem} = \\frac{\\text{Dívida Total}}{\\text{Patrimônio Líquido}}
        $$
    -   **Índice de Lucratividade (Profitability Ratio / Margem Bruta):** Calculado pela fórmula:
        $$
        \\text{Lucratividade} = \\frac{\\text{Lucro Bruto}}{\\text{Receita Total}}
        $$
3.  **Análise Setorial:** Os dados foram agrupados por tipo de empresa (`comp_type`) para responder a perguntas específicas de negócio.

## 📈 Principais Análises e Resultados

A análise dos índices calculados revelou os seguintes insights:

-   **Menor Lucratividade Média:** O setor **`fmcg`** (Bens de Consumo Não Duráveis) foi o que apresentou, em média, a menor margem de lucratividade.
-   **Maior Alavancagem Média:** O setor **`real_est`** (Imobiliário) demonstrou ser o mais alavancado em média.
-   **Correlação no Setor Imobiliário:** Foi identificada uma **correlação positiva** entre o índice de alavancagem e o de lucratividade para as empresas do setor imobiliário analisadas.

## 💻 Tecnologias Utilizadas

-   **Linguagem:** Python
-   **Bibliotecas:**
    -   Pandas: Para manipulação e análise dos dados.
    -   NumPy: Para operações numéricas.
    -   Seaborn: Para futuras visualizações.
-   **Ambiente:** Jupyter Notebook
