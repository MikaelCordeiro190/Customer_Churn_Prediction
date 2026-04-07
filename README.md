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

1. Problema de Negócio: Esta etapa tem como objtive receber o problema de negócio que será resolvido. É nesta etapa que é recebido a pergutna ou o pedido feito pelo dono do problema, que no caso deste projeto, é o CFO da rede Rossmann.

2. Entendimento de Negócio: Esta etapa tem como objetivo entender a dor do dono do problema e qual a sua real necessidade. Nesta etapa podem surgir protótipos da solução para validar com o dono do problema o que ele deseja como solução.

3. Coleta de Dados: Esta etapa tem como objetivo realizar a coleta dos dados, buscando eles nas tabelas do(s) banco(s) de dados da empresa.

4. Limpeza dos Dados: Esta etapa tem como objetivo remover toda e qualquer sujeira nos dados. Um dado sujo pode ser entendido como um dado que irá atrapalhar a performance final do algoritmo de Machine Learning. Tomando o cuidado entender bem o fenômeno que está sendo estudado para que não sejam removidos dados importantes para a modelagem do problema.

5. Exploração dos Dados: Esta etapa tem como objetivo entender os dados e como eles se relacionam entre si. Normalmente, são criadas hipóteses acionáveis de negócio que são posteriormente validadas utilizando técnicas de análise de dados. Além da criação de novas features que serão utilizadas na etapa de Modelagem de Dados.

6. Modelagem dos Dados: Esta etapa tem como objetivo preparar os dados para que eles sejam utilizados pelos algoritmos de Machine Learning. É nesta etapa que são feitos as transformações e encodign dos dados, a fim de facilitar o aprendizado do algoritmo utilizado.

7. Aplicação de Algoritmos de Machine Learning: Esta etapa tem como objetivo selecionar e aplicar algoritmos de Machine Learning nos dados preparados nas etapas anteriores. É nesta etapa que são selecionados os algoritmos e feito a comparação de performance enetre eles, para selecionar o algoritmos que melhor performou como algoritmo final.

8. Avaliação de Performance: Esta etapa tem como objetivo verificar a performance do algoritmo selecionado na etapa anterior com os resultados atuais, ou base line atual. Neste momento é feito a tradução da performance do algoritmo para perfomance de negócio. Ou seja, quanto a solução criada tratrá de retorno financeiro para a empresa. Caso a performance seja aceitável, o algoritmo é publicado e é retornado para a etapa de entendimento de negócio novamente, a fim entender melhor possíveis lacunas e assim melhorar a performance do algoritmo selecionado. Caso a performance não seja aceitável, o algoritmo não é publicado e é retornado para a etapa de entendimento de negócio para fazer uma nova iteração e assim melhorar a performance da solução.

9. Publicação da Solução: Será gerada uma base semanal para as area com a identificação dos clientes com grande propensão de Churn.

