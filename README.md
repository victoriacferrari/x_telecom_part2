📊 # Análise de Churn de Clientes – Telecomunicações

## Descrição do Projeto

Este projeto tem como objetivo **identificar os fatores que influenciam o cancelamento de clientes (Churn)** em uma empresa de telecomunicações e propor **estratégias de retenção** baseadas em análise de dados e modelagem preditiva.

O estudo utiliza dados históricos de clientes, técnicas de pré-processamento, balanceamento, modelagem com **Regressão Logística, Random Forest e XGBoost**, além de avaliação detalhada de métricas e importância de variáveis.

---

## Principais Fatores que Influenciam o Churn

A análise revelou os fatores mais relevantes que aumentam a probabilidade de um cliente cancelar o serviço:

* **Antiguidade do Cliente (tenure):** Clientes com maior tempo de permanência têm menor risco de churn.
* **Tipo de Contrato:** Contratos de longo prazo (1 ou 2 anos) reduzem significativamente o churn. Clientes com contratos mensais cancelam mais.
* **Tipo de Serviço de Internet:** Clientes com **fibra óptica** apresentam maior risco; clientes apenas com telefone têm menor probabilidade de cancelar.
* **Método de Pagamento:** Uso de **cheque eletrônico** aumenta a probabilidade de churn.
* **Outros fatores secundários:** Gasto total e ausência de serviços adicionais, como suporte técnico ou segurança online.

---

## Modelos Preditivos Avaliados

Foram testados três modelos de classificação:

| Modelo              | Recall (Churn) | AUC-ROC                    | Observações                                                                                             |
| ------------------- | -------------- | -------------------------- | ------------------------------------------------------------------------------------------------------- |
| Regressão Logística | ~80%           | Melhor média               | Melhor para identificar clientes em risco (alto Recall), porém menor Precision (mais falsos positivos). |
| Random Forest       | ~75%           | Boa                        | Modelo estável com validação cruzada.                                                                   |
| XGBoost             | ~76%           | Ligeiramente melhor que RF | Bom desempenho geral e AUC-ROC alto.                                                                    |

**Observações adicionais:**
Não houve sinais significativos de overfitting ou underfitting. O desempenho entre treino e teste foi consistente.

---

## Estratégias de Retenção Recomendadas

Com base nos fatores de risco identificados, as seguintes ações são sugeridas:

1. **Programas de fidelização por antiguidade:** Recompensas ou descontos para clientes de longa data.
2. **Incentivos para contratos de longo prazo:** Descontos ou benefícios para migrar para contratos de 1 ou 2 anos.
3. **Atenção especial a clientes de fibra óptica:** Investigar motivos do churn (preço, serviço, concorrência) e oferecer suporte ou promoções direcionadas.
4. **Promoção de métodos de pagamento automáticos:** Incentivar transferência bancária ou cartão de crédito e reduzir o uso de cheque eletrônico.
5. **Identificação proativa de clientes em risco:** Usar modelos preditivos para aplicar ações específicas (ex.: ofertas personalizadas ou ligações de retenção).
6. **Monitoramento de clientes com baixo gasto:** Foco nos primeiros meses e clientes de menor valor para prevenir churn.
7. **Promoção de serviços adicionais:** Destacar segurança online e suporte técnico, que reduzem o risco de cancelamento.

---

## Recomendação Final

* Monitoramento contínuo do desempenho dos modelos e atualização periódica com novos dados.
* Combinação de análise quantitativa com pesquisas qualitativas para entender os motivos de churn.
* Segmentação de clientes de acordo com o risco identificado e personalização das estratégias de retenção.

---

## Tecnologias Utilizadas

* **Python 3**
* **Pandas, NumPy** – Manipulação e análise de dados
* **Scikit-learn** – Pré-processamento, balanceamento (SMOTE), modelagem e métricas
* **XGBoost** – Modelagem preditiva
* **Seaborn, Matplotlib** – Visualização de dados

