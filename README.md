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

