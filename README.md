
📝 README — Análise e Backtest da Estratégia “Magic Formula”
📌 Descrição do Projeto

Este projeto implementa, passo a passo, uma análise quantitativa baseada na estratégia Magic Formula, proposta por Joel Greenblatt.
O objetivo é avaliar o desempenho do método na seleção de ações da B3, construindo uma carteira mensal e comparando sua performance com o índice Ibovespa no mesmo período.

O notebook realiza:

- Limpeza e preparação dos dados financeiros

- Cálculo de retornos mensais

- Filtro de liquidez

- Construção da fórmula de seleção (ranking combinado)

- Criação de carteiras mensais

- Cálculo da rentabilidade acumulada

- Comparação com o Ibovespa

- Visualizações e análises via QuantStats

- Conclusões sobre o modelo

📁 Estrutura do Notebook
1. Carregamento das Bibliotecas

Importação de pacotes essenciais:
pandas, seaborn, matplotlib, quantstats, além de utilidades do Python.

2. Inspeção dos Dados

Carregamento de datasets:

- dados_empresas.csv — informações financeiras e de mercado das empresas.

- Verificação de estrutura, colunas e primeiras linhas.

3. Cálculo dos Retornos Mensais

Agrupamento por ticker e cálculo dos retornos percentuais mensais.
Esse passo gera uma métrica padronizada para comparar empresas no tempo.

4. Filtragem de Liquidez

Remoção de ativos com volume negociado abaixo do limite definido.
O objetivo é evitar ativos ilíquidos que distorcem a carteira e dificultam operação realista.

5. Criação dos Rankings (“Magic Formula”)

A estratégia combina:

- Retorno sobre o capital (ROC)

- Earnings Yield

Os ativos recebem posição em cada critério e um ranking final combinado.

6. Criação das Carteiras

Para cada mês:

- Seleção dos ativos com melhor ranking.

- Criação de carteiras igualmente ponderadas.

- Geração da série de retornos mensais da carteira.

7. Heatmap dos Pesos

Visualização da alocação dos ativos ao longo dos meses (quando aplicável).

8. Cálculo da Rentabilidade do Modelo

Cálculo da evolução financeira da carteira:

- Retorno mensal

- Rentabilidade acumulada

- Comparação visual

9. Rentabilidade do Ibovespa

Carregamento do índice, cálculo do retorno mensal e curva acumulada.
O Ibovespa serve como benchmark para avaliar o modelo.

10. Análise dos Resultados

Uso de QuantStats:

- Estatísticas descritivas da estratégia

- Gráficos de heatmap mensal

- Comparação entre Magic Formula × Ibovespa

- Curva de retorno acumulado

📊 Resultados

O projeto mostra:

- O comportamento da estratégia ao longo do tempo

- Meses de maior e menor retorno

- Estabilidade da carteira

- Comparativo direto com o índice de mercado

- Identificação de períodos favoráveis e desfavoráveis

Na conclusão, o notebook discute a eficácia da estratégia para o mercado brasileiro e possíveis limitações.

📌 Observações Finais

- O notebook foi estruturado de forma didática, com passos numerados e gráficos explicativos.

- A metodologia segue rigor técnico e prática de mercado.

- Pode ser facilmente expandido para incluir outros fatores ou rebalanceamentos.