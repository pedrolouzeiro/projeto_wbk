# projeto_wbk

Projeto de Previsão de Inadimplência de Empréstimos da WBK

## Visão Geral do Projeto

A empresa WBK visa revolucionar a forma como as pessoas tomam empréstimos, oferecendo serviços rápidos e baseados em dispositivos móveis. Um foco crucial é fornecer aos clientes informações abrangentes sobre o serviço que estão contratando e reduzir a atual taxa de inadimplência de 35% para pelo menos 25%. Este projeto envolve a análise de dados de empréstimos e o desenvolvimento de um modelo de aprendizado de máquina para prever inadimplências, permitindo que a WBK tome medidas proativas para reduzir a taxa de inadimplência.

## Estrutura do Projeto

O projeto está dividido em cinco partes principais:

1. **Imports e Funções**
2. **Descrição das Colunas**
3. **Análise Exploratória de Dados (EDA)**
4. **Visualização dos Dados**
5. **Aprendizado de Máquina**

### 1. Imports e Funções

Esta seção inclui a importação de bibliotecas necessárias para manipulação de dados, visualização e aprendizado de máquina, bem como a definição de funções auxiliares para conexão ao banco de dados e cálculos de probabilidade.

### 2. Descrição das Colunas

Cada coluna do conjunto de dados é descrita, detalhando as informações que fornece. Isso inclui colunas numéricas e categóricas, essenciais para entender os dados e realizar a análise.

### 3. Análise Exploratória de Dados (EDA)

A EDA envolve:
- Estatísticas descritivas para colunas numéricas e categóricas.
- Tratamento de valores ausentes.
- Extração de insights e hipóteses com base na análise estatística.
- Cálculo de probabilidades para entender a distribuição e relação entre variáveis.

### 4. Visualização dos Dados

Usando `matplotlib.pyplot` e `seaborn`, vários gráficos foram plotados para visualizar os dados. Essas visualizações ajudam a confirmar ou rejeitar hipóteses com base na distribuição e relações identificadas durante a EDA.

### 5. Aprendizado de Máquina

A parte de aprendizado de máquina é dividida em sete etapas:

    1. Pré-processamento de Dados
    
        O pré-processamento de dados envolveu a transformação de variáveis categóricas usando `LabelEncoder`.

    2. Divisão de Treino, Teste
    
        O conjunto de dados foi dividido em conjuntos de treinamento e teste usando `train_test_split` para avaliar o desempenho do modelo em dados não vistos.

    3. Balanceamento
    
        Para abordar o desequilíbrio de classes, foi utilizada a técnica `OverSample`, garantindo que o modelo não seja tendencioso em relação à classe majoritária.
    
    4. Teste de Algoritmos
    
        Para testar qual mais se adequa ao conjunto de dados.
    
    5. Treino do Modelo
    
        Um algoritmo RandomForest foi utilizado para a previsão. Os resultados foram:
                
                Relatório de Classificação:
                                       precision    recall  f1-score   support
            
                                 0       0.79      0.78      0.79       202
                                 1       0.78      0.80      0.79       202
            
                          accuracy                           0.79       404
                         macro avg       0.79      0.79      0.79       404
                      weighted avg       0.79      0.79      0.79       404
             
            
                       Curva Roc: 0.7871287128712872
                       Matriz de Confusão: [[157  45]
                                           [ 41 161]]
                
    
    6. Salvamento do Modelo
    
        O modelo foi salvo usando a biblioteca `joblib` para previsões futuras.

## Principais Insights

### Importância das Etapas

- **Pré-processamento de Dados**: Garante que o modelo possa lidar adequadamente com diferentes tipos de dados.
- **Balanceamento**: Melhora o desempenho do modelo garantindo que todas as características contribuam igualmente e que o modelo não seja tendencioso em relação à classe majoritária.

### Impacto na Taxa de Inadimplência

Com uma precisão de 79%, o modelo pode melhorar significativamente a capacidade da WBK de prever inadimplências. Ao identificar clientes de alto risco antecipadamente, a WBK pode implementar medidas para mitigar o risco, potencialmente reduzindo a taxa de inadimplência de 35% para abaixo de 25%.

## Conclusão

Este projeto demonstra o processo de análise de dados de empréstimos e construção de um modelo preditivo para ajudar a WBK a reduzir as taxas de inadimplência. Ao alavancar técnicas de ciência de dados, a WBK pode oferecer melhores serviços aos seus clientes enquanto gerencia riscos de forma eficaz.


## Contato

Para quaisquer perguntas ou mais informações, entre em contato: 

        Email: pedrolouzeiro100303@gmail.com
        LinkedIn: https://www.linkedin.com/in/pedro-henrique-675b31176/

### Próximos passos:

- Otimizar criação de gráficos.
- Criar função para Pré-Processamento dos Dados.
