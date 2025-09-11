# 🤖🌟 Machine Learning - Model Telemétricas

## 📖 Descrição
Este repositório contém o desenvolvimento de um projeto de aprendizado de máquina, desde a definição do problema até a análise dos resultados.

---

## 🔎 Etapas do Projeto

# Sprint 1 - 25/08 até 04/09
### 1. Problema e Coleta de dados
#### Definir claramente o problema que será tratado.


#### Coleta de dados
- Realizada a partir de um fluxo de dados Gen2 armazenado em um datalake.

# Sprint 2 04/09 até 11/09
### 2. Descrição dos Dados
**Estações selecionadas**: "AUT-MG050", "AUT-CPM_Ativa", "AUT-MPT-P7", "AUT-MRB01-PT19" - São as mesmas estações utilizadas no plano de contingência.
**Variáveis selecionadas**: 'Alimentação', 'Condutividade', 'ORP', 'Oxigênio dissolvido', 'Temperatura', 'Turbidez', 'pH - apenas variáveis com menos de 15% de NAs (valores em brancos), foram selecionadas para dar seguimento ao modelo.

### 3. Premissas
**Hipóteses**:
- A turbidez está positivamente correlacionada com a concentração de metais (maior turbidez → maior concentração).
- Períodos chuvosos apresentam concentrações médias mais elevadas de metais em comparação com a estiagem.
- A influência da vazão na concentração de metais diminui ao longo do Rio Paraopeba.
(opcional, mais ligado ao ML): Modelos de machine learning (ex.: Random Forest, XGBoost, GAM) que considerem variáveis espaço-temporais (lags, sazonalidade, distância) apresentam melhor desempenho na predição da concentração de metais do que modelos lineares simples.
- Concentrações mais baixas de oxigênio dissolvido estão associadas a maiores concentrações de ferro e manganês, devido à redução de minerais em condições anóxicas.
👉 Fundamentação: em ambientes com baixo OD, Fe e Mn podem ser liberados dos sedimentos por processos redutivos.
- A variação do oxigênio dissolvido ao longo da profundidade está associada à redistribuição de metais dissolvidos (gradiente vertical de OD → diferença na mobilidade de Al, Fe e Mn).
👉 Isso conecta OD (superfície x fundo) com dinâmica redox.
- A interação entre temperatura da água e oxigênio dissolvido modula a concentração de metais (maior temperatura → menor OD → possível aumento da disponibilidade de Fe/Mn).
- Condições ácidas aumentam a solubilidade dos metais.
- Alterações rápidas de nível e vazão ressuspendem sedimentos ricos em metais
- Fração dissolvida: controlada principalmente por pH, OD, ORP, temperatura, processos redox.
- Fração total: controlada principalmente por chuva, turbidez, vazão, operação hidráulica, transporte e ressuspensão de sedimentos.

# Sprint 3 11/09 até 18/09
### 4. Planejamento da Solução
- **Limpeza dos Dados**: Verificação de tipos de dados, tratamento de valores nulos, renomeação de colunas, tratamento de outliers.  
- **Feature Engineering**: Criação de novas variáveis a partir das originais para melhorar a performance do modelo.  
- **Exploratory Data Analysis (EDA)**: Exploração inicial para obter insights e identificar variáveis relevantes.  
- **Preparação de Dados**: Normalização, reescalonamento, encoding e transformação de variáveis.  
- **Seleção de Features**: Escolher das variáveis mais relevantes para o modelo.  

# Sprint 4
### 5. Modelagem de Machine Learning
- Treinar modelos: **KNN Classifier, Logistic Regression, ExtraTrees Classifier, XGBoost**  
- Avaliação inicial: **Curva de ganho cumulativo, Lift, Precision@k, Recall@k**  

# Sprint 5
### 6. Ajuste de Hiperparâmetros (Fine-Tuning)
- Grid Search/Random Search para otimizar hiperparâmetros  
- Validação cruzada para reduzir viés de seleção  
- Comparação final entre modelos (Precision@k/Recall@k)  
- Seleção do melhor modelo para teste final  

# Sprint 6
### 7. Performance do Modelo
- Aplicação do modelo final nos dados de teste  
- Avaliação das métricas 
- Tradução dos resultados em impacto para empresa 

# Sprint 7
### 8. Insights e Análise de Hipóteses
Principais descobertas e hipóteses confirmadas ou rejeitadas.  

# Sprint 8
### 9. Modelos de Machine Learning
Resumo dos modelos testados, métricas e comparações.  

# Sprint 9
### 10. Resultados
Principais resultados quantitativos e qualitativos alcançados.  

# Sprint 10
### 11. Conclusões
Reflexão final sobre o projeto e resposta ao problema de negócio.  

# Sprint 11
### 12. Documentação
Ex: Python, Pandas, Scikit-Learn, XGBoost, Matplotlib, Seaborn, Jupyter Notebook 

# 13. Próximos Passos
Sugestões de melhorias, continuidade do projeto e trabalhos futuros.

---

## Contato
- [@Digital BI](mailto:digital.bi@arcadis.com)


© Arcadis
