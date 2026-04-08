# Problema de Negocio
A empresa apresenta um percentual elevado de churn, resultando na perda recorrente de clientes e impacto direto na receita e no crescimento sustentável do negócio

# Solução 
Construir uma solução de Machine Learning para classificação de churn, com foco em prever quais clientes possuem maior propensão a deixar a base. A partir dessas previsões, será possível apoiar a tomada de decisão das áreas de negócio na criação de estratégias preventivas, como campanhas de retenção, ofertas personalizadas e melhorias na experiência do cliente, contribuindo para a redução da taxa de churn e aumento da retenção e receita recorrente.

# Descrição dos Dados

| Atributo          | Descrição                                                      |
| ----------------- | -------------------------------------------------------------- |
| customer_id       | Identificador único do cliente                                 |
| gender            | Gênero do cliente (Male/Female)                                |
| senior_citizen    | Indica se o cliente é idoso (1 = sim, 0 = não)                 |
| partner           | Indica se o cliente possui parceiro(a) (Yes/No)                |
| dependents        | Indica se o cliente possui dependentes (Yes/No)                |
| tenure            | Tempo de permanência do cliente na empresa (em meses)          |
| phone_service     | Indica se o cliente possui serviço telefônico                  |
| multiple_lines    | Indica se o cliente possui múltiplas linhas telefônicas        |
| internet_service  | Tipo de serviço de internet contratado                         |
| online_security   | Indica se possui serviço de segurança online                   |
| online_backup     | Indica se possui backup online                                 |
| device_protection | Indica se possui proteção de dispositivo                       |
| tech_support      | Indica se possui suporte técnico                               |
| streaming_tv      | Indica se possui serviço de streaming de TV                    |
| streaming_movies  | Indica se possui serviço de streaming de filmes                |
| contract          | Tipo de contrato (Month-to-month, One year, Two year)          |
| paperless_billing | Fatura sem papel (Yes/No)                                      |
| payment_method    | Método de pagamento utilizado                                  |
| monthly_charges   | Valor cobrado mensalmente                                      |
| total_charges     | Valor total gasto pelo cliente                                 |
| churn             | Variável alvo: indica se o cliente cancelou o serviço (Yes/No) |

# Estratégia da Solução
Para garantir uma entrega rápida e eficiente do primeiro modelo, com o objetivo de trazer valor para a empresa e permitir decisões ágeis por parte do CCO, foi adotado o método CRISP-DM.

O método CRISP-DM é composto por 9 etapas cíclicas, em que a cada iteração dessas etapas, o resultado de negócio é aprimorado, buscando entregas cada vez mais rápidas e de maior qualidade, com maior precisão. Isso possibilita que as equipes que utilizarão os resultados desenvolvidos tenham um produto minimamente utilizável já na primeira entrega, e que seja aprimorado ao longo do tempo.

![image](https://github.com/user-attachments/assets/76d3e2c9-a5e1-4836-92f4-b092fe3d6fea)


CRISP-DM:

1. Problema de Negócio: Esta etapa tem como objtive receber o problema de negócio que será resolvido. É nesta etapa que é recebido a pergutna ou o pedido feito pelo dono do problema.
2. Entendimento de Negócio: Esta etapa tem como objetivo entender a dor do dono do problema e qual a sua real necessidade. Nesta etapa podem surgir protótipos da solução para validar com o dono do problema o que ele deseja como solução.

3. Coleta de Dados: Esta etapa tem como objetivo realizar a coleta dos dados, buscando eles nas tabelas do(s) banco(s) de dados da empresa.

4. Limpeza dos Dados: Esta etapa tem como objetivo remover toda e qualquer sujeira nos dados. Um dado sujo pode ser entendido como um dado que irá atrapalhar a performance final do algoritmo de Machine Learning. Tomando o cuidado entender bem o fenômeno que está sendo estudado para que não sejam removidos dados importantes para a modelagem do problema.

5. Exploração dos Dados: Esta etapa tem como objetivo entender os dados e como eles se relacionam entre si. Normalmente, são criadas hipóteses acionáveis de negócio que são posteriormente validadas utilizando técnicas de análise de dados. Além da criação de novas features que serão utilizadas na etapa de Modelagem de Dados.

6. Modelagem dos Dados: Esta etapa tem como objetivo preparar os dados para que eles sejam utilizados pelos algoritmos de Machine Learning. É nesta etapa que são feitos as transformações e encodign dos dados, a fim de facilitar o aprendizado do algoritmo utilizado.

7. Aplicação de Algoritmos de Machine Learning: Esta etapa tem como objetivo selecionar e aplicar algoritmos de Machine Learning nos dados preparados nas etapas anteriores. É nesta etapa que são selecionados os algoritmos e feito a comparação de performance enetre eles, para selecionar o algoritmos que melhor performou como algoritmo final.

8. Avaliação de Performance: Esta etapa tem como objetivo verificar a performance do algoritmo selecionado na etapa anterior com os resultados atuais, ou base line atual. Neste momento é feito a tradução da performance do algoritmo para perfomance de negócio. Ou seja, quanto a solução criada tratrá de retorno financeiro para a empresa. Caso a performance seja aceitável, o algoritmo é publicado e é retornado para a etapa de entendimento de negócio novamente, a fim entender melhor possíveis lacunas e assim melhorar a performance do algoritmo selecionado. Caso a performance não seja aceitável, o algoritmo não é publicado e é retornado para a etapa de entendimento de negócio para fazer uma nova iteração e assim melhorar a performance da solução.

9. Publicação da Solução: Será gerada uma base semanal para as area com a identificação dos clientes com grande propensão de Churn.

# EDA ( Análise Exploratória )
A partir da exploração inicial dos dados, foram levantadas diversas hipóteses de negócio com o objetivo de identificar padrões e comportamentos relevantes nas features do dataset.
Para cada hipótese, foram conduzidas análises visuais e estatísticas que permitiram investigar relações entre as variáveis e o fenômeno do churn — a saída de clientes da base.


Das análises realizadas, três se destacaram por apresentar padrões consistentes e estatisticamente relevantes, sugerindo forte relação com a probabilidade de um cliente abandonar o serviço. 

## 1.1 Clientes com serviço de Fibra Óptica apresentam os maiores índices de churn.

<img width="708" height="438" alt="image" src="https://github.com/user-attachments/assets/3343129c-30ba-4ad1-ad72-2064d36e20aa" />

## 1.2 O método de pagamento por Cheque Eletrônico concentra quase metade dos casos de churn.

<img width="707" height="438" alt="image" src="https://github.com/user-attachments/assets/b35a2875-50eb-4bda-ba6e-6892e4e61b0c" />

## 1.3 Contratos mensais possuem maior propensão ao churn em relação a contratos de longo prazo.

<img width="708" height="439" alt="image" src="https://github.com/user-attachments/assets/025d4b56-392e-47f9-8aff-fcca4574c9d8" />

# Definição de Modelos de Machine Learning
No primeiro ciclo do projeto, foram selecionados cinco algoritmos para teste, visando identificar o algoritmo com melhor desempenho e custo de implementação. Nessa etapa inicial, optou-se pela simplicidade, considerando que era o primeiro ciclo do projeto e o objetivo principal era entregar uma solução mínima utilizável para a equipe de negócios e pelo CFO.

Os algotitmos selecionados foram:

• KNN

• Logistic Regression

• Random Forest Classification

Após a seleção dos algoritmos, procedemos com o treinamento e teste de cada um deles para avaliar sua performance.Além disso, aplicamos dois métodos de seleção de features — RFE (Recursive Feature Elimination) e Feature Importance e cruzamos os resultados para identificar as variáveis em comum entre ambos. A partir dessa interseção, combinada com as análises exploratórias realizadas anteriormente, definimos as features finais para o modelo.

Nessa fase, os algoritmos foram treinados e submetidos ao processo de Cross Validation para garantir que os resultados não fossem enviesados. Para avaliar a performance dos modelos, utilizamos as seguintes métricas :

• Acurácia        — percentual de predições corretas sobre o total de amostras.

• Precision       — dos clientes classificados como churn, quantos realmente eram churn.

• Recall          — dos clientes que realmente eram churn, quantos o modelo conseguiu capturar.

• F1-Score        — média harmônica entre Precision e Recall, equilibrando as duas métricas.

• AUC-ROC         — capacidade do modelo de separar as classes churn e não-churn.

• Balanced Acc.   — acurácia média por classe, mais justa em datasets desbalanceados.

| Métrica | KNN   | Logistic Regression | Random Forest |
|---|:---:|:---:|:---:|
| Accuracy | 0.7730 | 0.8396 | **0.8550** |
| Precision | 0.5682 | **0.6421** | 0.6389 |
| Recall | 0.3571 | 0.5657 | **0.5829** |
| F1-Score | 0.4386 | 0.5491 | **0.5665** |
| ROC AUC | 0.7550 | 0.8214 | **0.8568** |
| Balanced Accuracy | 0.6338 | 0.6778 | **0.7004** |

> Os valores em **negrito** indicam o melhor resultado por métrica.

# Escolha do Modelo

Apesar de diversos modelos terem sido avaliados durante o processo de validação cruzada, o Random Forest Classifier apresentou o melhor desempenho geral entre os algoritmos testados. Esse modelo obteve os maiores valores nas principais métricas de erro, incluindo Accuracy (0.8550), Recall (0.5829) e ROC AUC (0.8568), indicando maior precisão nas previsões em comparação aos demais modelos.

Dessa forma, o Random Forest Classifier foi selecionado para prosseguimento na etapa de otimização de hiperparâmetros (Hyperparameter Fine Tuning). A escolha se justifica pelo seu desempenho superior durante a fase de validação, demonstrando maior capacidade de capturar padrões complexos nos dados.


# Hiperparâmetros

Foi empregada a técnica de Grid Search para otimizar a busca dos melhores hiperparâmetros. A fim de identificar o parâmetro ideal, optei por utilizar uma amostra referente a um período de 1 ano. Essa escolha permite aumentar o número de iterações em um espaço de tempo reduzido, maximizando a probabilidade de localizar um mínimo global.


# Final Resultado

Foi gerada uma listagem com as previsões do modelo, identificando os usuários com maior probabilidade de churn. A partir dessa segmentação, torna-se possível priorizar clientes mais propensos à evasão e direcionar esforços de forma mais eficiente, aumentando a efetividade das ações de retenção.

Com esses insights, as áreas de negócio podem estruturar campanhas de marketing mais personalizadas, ofertas direcionadas e abordagens proativas via telemarketing, focando em clientes com maior risco de cancelamento. Além disso, o modelo permite apoiar a tomada de decisão com base em dados, substituindo abordagens genéricas por estratégias orientadas a comportamento e probabilidade de saída.


# Proximos Passos 

No Proximo Passo do modelo CRISP-DM, podem ser incrementados:

Testar outros algoritmos de Machine Learning

Trabalhar com outras features

Utilizar outra estratégia para Fine Tuning Hyperparameter







