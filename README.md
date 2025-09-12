# 🤖🌟 Machine Learning - Model Telemétricas

## 📖 Descrição  

Este repositório reúne o desenvolvimento de um projeto de **aprendizado de máquina**, cobrindo todas as etapas do ciclo de análise de dados:  

- Definição e contextualização do problema  
- Preparação e exploração dos dados  
- Modelagem e avaliação de algoritmos  
- Interpretação dos resultados e geração de insights  

O objetivo é documentar de forma estruturada todo o processo, permitindo **reprodutibilidade**, **transparência** e **aprendizado contínuo**.  

---

## 🔎 Etapas do Projeto

# 🚀 Sprint 1 — 25/08 até 04/09  

## 1. Problema e Coleta de Dados  

### 📝 Definição do Problema  
- Delimitar claramente o problema a ser tratado nesta fase.  
- Validar **premissas** definidas na **Seção 3 (Sprint 2)**, garantindo consistência para as etapas seguintes.  

### 📥 Coleta de Dados  
- A coleta foi realizada a partir de um **fluxo de dados Gen2** integrado ao **datalake** corporativo.  
- Essa abordagem garante **escalabilidade**, **governança** e **atualização automática** dos dados utilizados no projeto.  

# Sprint 2 04/09 até 11/09
### 2. 📊 Descrição dos Dados
As análises foram realizadas a partir de um conjunto de estações de monitoramento previamente definidas:  
- **AUT-MG050**  
- **AUT-CPM_Ativa**  
- **AUT-MPT-P7**  
- **AUT-MRB01-PT19**  

> Essas estações correspondem às mesmas utilizadas no **Plano de Contingência**.  

As variáveis selecionadas foram aquelas com **menos de 15% de valores ausentes (NAs)**, garantindo melhor qualidade e consistência para o modelo.  

### 📌 Variáveis Selecionadas  

| Variável              | Descrição                                                                 |
|------------------------|---------------------------------------------------------------------------|
| **Alimentação**        | Taxa de entrada de energia ou nutrientes para o sistema monitorado.       |
| **Condutividade**      | Capacidade da água de conduzir corrente elétrica (indicador de sais).     |
| **ORP** (Potencial de Redox) | Mede o potencial de oxirredução da água, associado à qualidade química. |
| **Oxigênio dissolvido**| Concentração de oxigênio disponível para organismos aquáticos.            |
| **Temperatura**        | Temperatura da água, fator que influencia processos físicos e biológicos.|
| **Turbidez**           | Grau de dispersão da luz causado por partículas em suspensão na água.     |
| **pH**                 | Medida da acidez ou alcalinidade da água.                                |

### 3. Premissas
**🔎Hipóteses**:

As hipóteses a seguir buscam explicar os fatores que controlam a dinâmica de metais no Rio Paraopeba, considerando tanto variáveis físico-químicas quanto hidrológicas.  

### 1. Relações entre turbidez e metais  
- A **turbidez** está positivamente correlacionada com a concentração de metais.  
  > Maior turbidez → maior concentração de metais em suspensão.  

### 2. Sazonalidade (chuva x estiagem)  
- **Períodos chuvosos** apresentam concentrações médias mais elevadas de metais em comparação com períodos de estiagem.  
- Alterações rápidas de **nível e vazão** ressuspendem sedimentos ricos em metais.  

### 3. Vazão e dinâmica longitudinal  
- A influência da **vazão** sobre a concentração de metais **diminui ao longo do Rio Paraopeba**.  

### 4. Oxigênio dissolvido (OD) e processos redox  
- **Baixas concentrações de OD** estão associadas a maiores concentrações de ferro e manganês, devido à **redução de minerais em condições anóxicas**.  
  > Fundamentação: em ambientes com baixo OD, Fe e Mn podem ser liberados dos sedimentos por processos redutivos.  

- A **variação vertical de OD** (superfície x fundo) está associada à redistribuição de metais dissolvidos, conectando gradientes de OD à **dinâmica redox**.  

- A **interação entre temperatura e OD** modula a concentração de metais:  
  > Maior temperatura → menor OD → possível aumento da disponibilidade de Fe/Mn.  

### 5. Influência do pH  
- **Condições ácidas** aumentam a solubilidade dos metais.  

### 6. Frações de metais  
- **Fração dissolvida**: controlada principalmente por pH, OD, ORP, temperatura e processos redox.  
- **Fração total**: controlada principalmente por chuva, turbidez, vazão, operação hidráulica e ressuspensão de sedimentos.  

### 7. Hipótese opcional (abordagem em ML)  
- Modelos de **machine learning** (ex.: Random Forest, XGBoost, GAM) que considerem variáveis espaço-temporais  
  (lags, sazonalidade, distância) apresentam **melhor desempenho preditivo** para concentrações de metais do que modelos lineares simples.  


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
- [@Aika Miura](mailto:aika.miura@arcadis.com)
- [@Arthur Ricardo](mailto:arthur.ricardo@arcadis.com)
- [@Gabriella Oliveira](mailto:gabriella.oliveira@arcadis.com)
- [@Karina Silva](mailto:karina.santos@arcadis.com)


© Arcadis
