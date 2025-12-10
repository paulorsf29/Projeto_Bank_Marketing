# Projeto_Bank_Marketing

Este repositório contém a análise e modelagem preditiva aplicadas ao **Bank Marketing Dataset**, disponibilizado pelo **UCI Machine Learning Repository**.  
O objetivo é prever a **subscrição (yes/no)** de depósito a prazo por clientes bancários, com base em dados demográficos, históricos e de campanhas telefônicas.

---


##  Descrição do Projeto

O projeto abrange:

- **EDA** (Análise Exploratória de Dados)
- **Visualização estatística**
- **Pré-processamento e limpeza**
- **Modelagem Preditiva**
- **Comparação de desempenho**
- **Insights sobre conversão e comportamento**

---

##  Resultados Obtidos

| Modelo | Acurácia | ROC-AUC | Observação |
|--------|----------|---------|------------|
| Naive Bayes | ~0.78 | 0.90 | Baseline |
| **Regressão Logística** | **~0.89** | **0.93** | Melhor desempenho |

> A Regressão Logística demonstrou melhor equilíbrio entre **precisão, recall e discriminabilidade (AUC)**, sendo o modelo recomendado.

---

##  Principais Insights

- Campanhas via **celular** obtêm maior conversão do que via telefone fixo.
- **Ligações mais longas** estão relacionadas a maior probabilidade de aceitação.
- `poutcome = success` é o mais forte indicador categórico de conversão.
- Meses com maior taxa de adesão: **mar, set, out, dez**.

---

##  Tecnologias Utilizadas

| Biblioteca | Finalidade |
|------------|------------|
| Pandas | Limpeza e manipulação de dados |
| NumPy | Base numérica |
| Scikit-learn | Modelagem e métricas |
| Seaborn / Matplotlib | Visualização |
| SciPy | Funções estatísticas |
| PyCaret (opcional) | Comparação e otimização automática |

---

##  Instalação e Execução

### 1. Clone o repositório
```bash
git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
```

### 2. Instale as dependências
```bash
pip install -r requirements.txt
```

### 3. Execute o notebook
```bash
jupyter notebook
```
---
## Dataset e Licença

Fonte: UCI Machine Learning Repository – Bank Marketing Dataset
https://archive.ics.uci.edu/dataset/222/bank+marketing

Licença: Creative Commons Attribution 4.0 International (CC BY 4.0)
https://creativecommons.org/licenses/by/4.0/
---

## Limitações e Vieses

Desbalanceamento severo (~88% não / 12% sim).

Variável duration gera data leakage e deve ser analisada com cuidado.

Alta incidência de unknown em poutcome, representando ausência real de histórico.
