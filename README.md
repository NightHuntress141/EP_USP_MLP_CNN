# 🧠 Deep Learning Foundations — MLP vs CNN

Projeto desenvolvido para explorar, na prática, os fundamentos de **Deep Learning**, com foco na comparação entre arquiteturas **MLP (Multi-Layer Perceptron)** e **CNN (Convolutional Neural Network)** aplicadas a classificação de imagens.

O trabalho enfatiza **experimentação estruturada, análise crítica de resultados e tomada de decisão baseada em evidências**.

### Intergrantes:
- Rebecka Bocci Domingues (@NightHuntress141)
- Yuri
- Eduardo

---

## 🎯 Objetivo

Investigar como diferentes arquiteturas de redes neurais se comportam em tarefas de visão computacional, respondendo perguntas como:

* Quando uma MLP é suficiente?
* Por que CNNs performam melhor em imagens?
* Como escolhas de arquitetura impactam generalização?

---

## 📊 Dataset

**Fashion MNIST**

* 70.000 imagens (28x28, grayscale)
* 10 classes de roupas
* Problema de classificação supervisionada

**Pré-processamento:**

* Normalização (`[0,1]`)
* Split estratificado (treino/validação)

---

## ⚙️ Modelagem

### 🔹 Baselines

**MLP**

```python
Flatten → Dense(10, softmax)
```

**CNN**

```python
Conv2D → MaxPooling → Flatten → Dense(10, softmax)
```

**Configuração:**

* Optimizer: Adam
* Learning rate: 1e-3
* Batch size: 128
* Épocas: 10

---

## 📈 Resultados

| Modelo | Acurácia   |
| ------ | ---------- |
| CNN    | **89.30%** |
| MLP    | 84.06%     |

💡 A CNN apresentou melhor desempenho ao capturar padrões espaciais das imagens, evidenciando sua superioridade para esse tipo de dado.

---

## 🧪 Experimentação

### 🔹 MLP

* Variação de profundidade e número de neurônios
* Avaliação de underfitting vs overfitting

### 🔹 CNN

* Diferentes arquiteturas convolucionais
* Impacto de pooling e profundidade
* Ajustes de capacidade e generalização

Cada experimento inclui:

* Curvas de **loss**
* Curvas de **acurácia**
* Interpretação dos resultados

---

## 🔍 Principais Insights

* CNNs exploram **estrutura espacial**, enquanto MLPs tratam a imagem como vetor
* Aumento de complexidade melhora performance até certo ponto (trade-off com overfitting)
* Escolhas de arquitetura impactam mais que ajustes finos de hiperparâmetros em estágios iniciais

---

## 🛠️ Tecnologias

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib

---

## 🚀 Como Executar

```bash
git clone https://github.com/seu-usuario/seu-repo.git
cd seu-repo
jupyter notebook
```
