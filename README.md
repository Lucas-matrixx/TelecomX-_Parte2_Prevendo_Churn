# 📊 Churn Analysis – Previsão de Evasão de Clientes

## 🎯 Objetivo do Projeto

Este projeto tem como objetivo **identificar clientes com maior risco de evasão (churn)**, utilizando modelos preditivos para:

- Antecipar cancelamentos de serviços  
- Implementar estratégias de retenção proativas  
- Melhorar receita recorrente e previsibilidade do negócio  

---

## 🗂 Estrutura do Projeto

- data
    - dados_normalizados_ml.csv
- model
    - modelo_rfb.pkl
- notebook
    - TelecomX_Analise_Evasão_e_Clientes.ipynb



## 🛠 Metodologia

1. **Pré-processamento dos dados**
   - Tratamento de valores nulos (`SimpleImputer`)  
   - Encoding de variáveis categóricas (`OneHotEncoder`)  
   - Normalização de variáveis numéricas (`StandardScaler`)  
   - Divisão treino/teste com `train_test_split(stratify=y)`  

2. **Modelagem**
   - Modelos utilizados:
     - Random Forest Classifier  
     - K-Nearest Neighbors (KNN)  
    
   - Hiperparâmetros otimizados via `GridSearchCV`  
   - Avaliação com cross-validation (`StratifiedKFold`)  

3. **Avaliação**
   - Métricas: Accuracy, Precision, Recall, F1-score  

4. **Interpretabilidade**
   - Feature Importance (Random Forest)  
   - Identificação das variáveis que mais impactam a evasão  


## 📈 Principais Resultados

- **Top features de influência na evasão**:  
  1. `tipo_contrato_mensal` (maior risco de churn)  
  2. `tipo_contrato_bienal`  
  3. `tempo_permanencia` (quanto maior, menor o risco)  
  4. `tipo_internet_fibra_optica`  
  5. `cobranca_mensal`  

- **Insights estratégicos**:  
  - Clientes novos e com contratos mensais têm maior risco → foco em onboarding e retenção inicial  
  - Cobranças mensais e métodos de pagamento específicos impactam churn → oferecer flexibilidade  
  - Primeiros 6 meses críticos → campanhas de fidelização neste período  

---

## 🛠 Como Rodar o Projeto

1. Clonar o repositório:

```bash
git clone https://github.com/Lucas-matrixx/TelecomX-_Parte2_Prevendo_Churn.git

```
## Instruções de instalação 

✔️ 1. Crie (ou ative) seu ambiente virtual no terminal seguindo uma das opções abaixo:

- Windows - com Git bash
```python
python -m venv venv
```
```python
source ./venv/Scripts/activate
```
- Windows - com PowerSheel
```python
python -m venv venv
```
```python
venv\Scripts\Activate.ps1
```
- Linux/Mac
```python
python3 -m venv venv
```
```python
source venv/bin/activate
```


---
✔️ 2. Instale as dependências do requirements.txt

Com o ambiente ativo:

```python
pip install -r requirements.txt
```

📊 Visualizações

Taxa de evasão por tipo de contrato e faixa de permanência

Frequência relativa de clientes ativos (não evadiram)

Feature Importance do Random Forest


📌 Tecnologias Utilizadas

Python 3.11+

Bibliotecas: pandas, numpy, scikit-learn, seaborn, matplotlib

Git e GitHub para versionamento e compartilhamento

💡 Conclusão

O modelo Random Forest permitiu identificar os fatores mais críticos de churn e direcionar estratégias de retenção.
Foco nos primeiros meses, tipo de contrato e tempo de permanência é essencial para reduzir a evasão e aumentar a fidelidade do cliente.

📎 Contato

Projeto desenvolvido por: Lucas Rodrigues
GitHub: https://github.com/Lucas-matrixx
