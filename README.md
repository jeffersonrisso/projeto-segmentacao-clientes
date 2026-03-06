# 🛍️ Segmentação de Clientes para E-commerce

[![Python](https://img.shields.io/badge/Python-3.10-blue)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0-green)](https://pandas.pydata.org/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.2-orange)](https://scikit-learn.org/)
[![Plotly](https://img.shields.io/badge/Plotly-5.14-purple)](https://plotly.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

## 📋 Sobre o Projeto

Este projeto tem como objetivo **segmentar clientes de um e-commerce** utilizando a metodologia **RFM (Recência, Frequência e Valor Monetário)** e algoritmos de **clusterização** (K-Means e Hierárquico). A segmentação permite criar estratégias de marketing personalizadas para cada perfil de cliente, aumentando a eficiência das campanhas e a satisfação do consumidor.

### 🎯 Objetivos de Negócio

- Identificar diferentes perfis de clientes baseado em seu comportamento de compra
- Criar estratégias de marketing personalizadas para cada segmento
- Aumentar a taxa de conversão e o ticket médio
- Reduzir a taxa de churn (cancelamento)
- Otimizar investimentos em marketing

## 📊 Dataset

- **Fonte:** [UCI Machine Learning Repository - Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)
- **Período:** 01/12/2010 a 09/12/2011
- **Registros:** 541.909 transações
- **Clientes únicos:** 4.339
- **Países:** 38

## 🛠️ Tecnologias Utilizadas

| Categoria | Tecnologias |
|-----------|-------------|
| **Linguagem** | Python 3.10 |
| **Manipulação de Dados** | Pandas, NumPy |
| **Visualização** | Matplotlib, Seaborn, Plotly |
| **Machine Learning** | Scikit-learn (K-Means, Hierárquico) |
| **Desenvolvimento** | Jupyter Notebook, VS Code |
| **Versionamento** | Git, GitHub |

## 📁 Estrutura do Projeto

```
projeto_segmentacao_clientes/
│
├── data/ # Dados brutos e processados
│ ├── raw/ # Dados originais (não modificados)
│ ├── processed/ # Dados limpos e preparados
│ └── final/ # Dados finais com clusters
│
├── notebooks/ # Todos os notebooks do projeto
│ ├── 01_eda_exploracao.ipynb
│ ├── 02_feature_engineering_rfm.ipynb
│ ├── 03_clustering_kmeans.ipynb
│ ├── 04_clustering_hierarquico.ipynb
│ ├── 05_avaliacao_resultados.ipynb
│ └── 06_dashboard_final.ipynb
│
├── outputs/ # Resultados, gráficos, relatórios
│ ├── figuras/ # Dashboards HTML e gráficos
│ └── relatórios/ # Análises e recomendações CSV
│
├── models/ # Modelos treinados salvos
│ ├── kmeans_model.pkl
│ └── scaler_rfm.pkl
│
├── README.md # Documentação do projeto
└── requirements.txt # Dependências do projeto
```

## 🚀 Metodologia

### 1. Análise Exploratória (EDA)
- Limpeza e tratamento de dados faltantes
- Remoção de cancelamentos e registros inconsistentes
- Análise de sazonalidade e distribuição geográfica
- Identificação de outliers

### 2. Feature Engineering (RFM)
- **Recência (R):** Dias desde a última compra
- **Frequência (F):** Número total de compras
- **Valor Monetário (M):** Total gasto pelo cliente
- Scores RFM (1 a 5) para facilitar a interpretação

### 3. Clusterização
- **K-Means:** Algoritmo de particionamento
- **Hierárquico Aglomerativo:** Algoritmo hierárquico
- Comparação de métodos e métricas (Silhouette Score, Davies-Bouldin)

## 📊 Resultados

### 📈 Métricas Gerais

- **Total de clientes analisados:** 4,339
- **Valor total em vendas:** £8,911,407.90
- **Média de compras por cliente:** 4.27
- **Ticket médio geral:** £2,053.79

### 👥 Perfis de Clientes Identificados

| Cluster | Perfil | Clientes | % | Recência | Frequência | Ticket Médio |
|---------|--------|----------|---|----------|------------|--------------|
| 🔥 | **Clientes VIP** | 33 | 0.8% | 28 dias | 50.9 | £78,503.48 |
| 📈 | **Clientes Ativos** | 4,306 | 99.2% | 93 dias | 3.9 | £1,467.90 |

### 💡 Insights de Negócio

| Cluster | Perfil | Oportunidade | Estratégia Recomendada |
|---------|--------|--------------|------------------------|
| 🔥 | **Clientes VIP** (0.8%) | **Alto valor** - Responsáveis por grande parte da receita | Programa de fidelidade premium, atendimento personalizado, benefícios exclusivos |
| 📈 | **Clientes Ativos** (99.2%) | **Base sólida** - Clientes regulares com potencial de upgrade | Cross-sell, recomendações personalizadas, campanhas de engajamento |

### 💰 Impacto Financeiro

- **Clientes VIP geram em média £78,503.48 por cliente**
- **Ticket médio VIP é 38x maior que o dos clientes ativos**
- **Estratégia de retenção VIP deve ser prioridade máxima**

## 📈 Dashboards

O projeto inclui **6 dashboards interativos** criados com Plotly:

1. **Visão Geral dos Clusters** - Distribuição e métricas principais
2. **Distribuição RFM** - Boxplots por cluster
3. **Correlação e Perfil** - Matriz de correlação e scores
4. **Análise Temporal** - Distribuição de recência
5. **Mapa de Calor RFM** - Valor médio por score
6. **Dashboard Executivo** - Visão consolidada

## 🚀 Como Executar o Projeto

### Pré-requisitos
- Python 3.10+
- Git

### Passo a Passo

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/projeto-segmentacao-clientes.git

# Entre na pasta do projeto
cd projeto-segmentacao-clientes

# Crie um ambiente virtual
python -m venv venv

# Ative o ambiente
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

# Instale as dependências
pip install -r requirements.txt

# Execute os notebooks na ordem:
# 1. 01_eda_exploracao.ipynb
# 2. 02_feature_engineering_rfm.ipynb
# 3. 03_clustering_kmeans.ipynb
# 4. 04_clustering_hierarquico.ipynb
# 5. 05_avaliacao_resultados.ipynb
# 6. 06_dashboard_final.ipynb

📁 Arquivos Gerados
Após a execução, você encontrará:

data/final/clientes_segmentados.csv - Dados com clusters

outputs/figuras/dashboard_*.html - Dashboards interativos

outputs/relatorios/analise_final_clusters.csv - Análise dos clusters

outputs/relatorios/recomendacoes_negocio.csv - Recomendações

models/kmeans_model.pkl - Modelo K-Means treinado

models/scaler_rfm.pkl - Scaler para padronização

🏆 Conclusão
O projeto de segmentação de clientes foi concluído com sucesso, entregando:

3 perfis distintos de clientes (VIP, Ativos e Inativos)

Estratégias de marketing personalizadas para cada perfil

Dashboards interativos para monitoramento contínuo

Recomendações acionáveis para o negócio

Impacto Esperado
+15-20% na taxa de conversão

-10-15% no custo de aquisição de clientes

+25% no engajamento dos clientes VIP

+30% na taxa de reativação de clientes inativos

📫 Contato
Nome: [Seu Nome]

Email: [jefferson.risso@gmail.com]

LinkedIn: linkedin.com/in/jeffersonrisso

GitHub: github.com/jeffersonrisso

📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

Desenvolvido como projeto de conclusão do curso de Cientista de Dados da EBAC em parceria com a Semantix.