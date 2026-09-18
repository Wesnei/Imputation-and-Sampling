# Imputação e Amostragem de Dados

Este repositório contém a implementação da atividade prática da disciplina de **Modelos Generativos Profundos** do Programa de Pós-Graduação em Ciência da Computação (PPGCC - IFCE). 

O projeto explora soluções para dois gargalos clássicos no pré-processamento de dados para aprendizado de máquina: a falta de volume (escassez de amostras) e a presença de dados corrompidos (*missing values*).

## 🚀 O que foi desenvolvido

### Parte A: Geração de Amostras (Data Augmentation)
Focada no dataset *Vertebral Column* da UCI, esta etapa compara a geração de dados sintéticos utilizando duas abordagens probabilísticas:
* **Naïve Bayes:** Treinamento com 50% dos dados para amostrar novas instâncias assumindo independência condicional entre os atributos físicos[cite: 13].
* **Método da Rejeição:** Utilização de uma Normal Multivariada como distribuição de proposta, filtrando as amostras aceitas através da fronteira de decisão (função sigmoide) de uma Regressão Logística treinada com a base original completa.

### Parte B: Preenchimento de Lacunas (Imputação de Dados)
A partir do dataset *Iris*, 10% dos valores da matriz (180 dados) foram apagados aleatoriamente. O script reconstrói a base avaliando o erro (RMSE) de três métodos distintos:
* **Valor Esperado (Média)**
* **K-Nearest Neighbors (K-NN)**
* **Regressão Linear (Iterative Imputer)**

Os resultados demonstram estatisticamente a superioridade de abordagens que preservam a correlação linear e a vizinhança espacial na reconstrução dos dados originais.

## 🛠️ Tecnologias Utilizadas
* **Python**
* **Scikit-Learn** (Modelagem, PCA e Imputação)
* **NumPy & Pandas** (Manipulação de matrizes e dataframes)
* **Matplotlib** (Visualização 2D)
* **ucimlrepo** (Extração via API da UCI)

## 👨‍💻 Autor
**Wesnei de Paiva Batista**  
Mestrando em Ciência da Computação (IA) - IFCE
