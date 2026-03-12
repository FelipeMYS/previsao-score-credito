# Classificação de Score de Crédito - Machine Learning & Scikit-Learn

Este projeto utiliza modelos de Inteligência Artificial para classificar o score de crédito de clientes em três categorias: **Poor (Ruim)**, **Standard (Médio)** ou **Good (Bom)**. O foco é automatizar o processo de análise de risco com base em dados históricos e comportamentais.

## Estrutura do Projeto

O projeto percorre desde o pré-processamento de dados até a comparação de performance entre modelos de Machine Learning:

### 1. Bases de Dados
* **`clientes.csv`**: Base histórica utilizada para o treinamento e teste dos modelos, contendo informações como profissão, salário anual, número de contas, atrasos de pagamento e dívida total.
* **`novos_clientes.csv`**: Base de dados inéditos utilizada para simular a aplicação do modelo em um cenário real de novos cadastros.

### 2. Script de Inteligência Artificial (`main.ipynb`)
Notebook que contém todo o pipeline de ML:
* **Pré-processamento**: Transformação de variáveis categóricas (textos) em números utilizando o `LabelEncoder` para que os modelos possam realizar os cálculos.
* **Divisão de Dados**: Separação da base em conjuntos de **Treino** e **Teste** para validar a eficácia dos algoritmos.
* **Treinamento de Modelos**: Implementação simultânea dos algoritmos **Random Forest (Floresta Decisora)** e **KNN (K-Nearest Neighbors)**.
* **Avaliação de Performance**: Uso da métrica de acurácia para determinar qual modelo obteve o melhor desempenho (neste caso, o Random Forest).
* **Previsão**: Execução do modelo vencedor na base de novos clientes.

## Lógica de Implementação

* **Tratamento de Dados**: O código demonstra conhecimento em engenharia de atributos ao preparar a base para modelos matemáticos.
* **Comparação de Modelos**: A estratégia de testar dois modelos diferentes garante que a solução final seja a mais precisa possível para o problema em questão.
* **Feature Importance**: O projeto identifica quais variáveis (como dias de atraso e mix de crédito) mais impactam a pontuação final do cliente.

## Tecnologias Utilizadas

* **Python 3.x**
* **Pandas**: Manipulação e análise de dados tabulares.
* **Scikit-Learn**: Biblioteca principal para implementação de Machine Learning (Modelos, Pre-processing e Metrics).

## Resultados Obtidos

* O modelo de **Random Forest** apresentou uma acurácia superior (aprox. 82%), sendo selecionado para a produção.
* O sistema é capaz de processar novos clientes automaticamente e atribuir uma categoria de score instantaneamente, otimizando o tempo de análise de crédito.

## Como Utilizar

1. Instale as bibliotecas necessárias:
   ```bash
   pip install pandas scikit-learn