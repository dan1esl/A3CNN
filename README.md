# A3CNN
Reconhecimento de imagens com redes neurais convolucionais.

# Reconhecimento de Dígitos Manuscritos com Redes Neurais Convolucionais (CNN)

## Descrição

Este projeto implementa uma Rede Neural Convolucional (CNN) para classificação de dígitos manuscritos do dataset MNIST.

O modelo é treinado para reconhecer imagens contendo números de 0 a 9 e realizar previsões em imagens externas.

---

## Objetivos

- Construir uma Rede Neural Convolucional para classificação de imagens com alta acurácia.
- Avaliar o desempenho do modelo utilizando métricas de classificação.
- Testar a capacidade de generalização da rede em imagens externas.

---

## Dataset Utilizado

O projeto utiliza o dataset **MNIST (Modified National Institute of Standards and Technology)**.

Características do conjunto de dados:

- 70.000 imagens em escala de cinza
- 10 classes (dígitos de 0 a 9)
- 60.000 imagens para treinamento
- 10.000 imagens para teste

---

## Tecnologias Utilizadas

- Python 
- TensorFlow
- Keras
- NumPy
- Scikit-Learn
- Matplotlib

---

## Pré-processamento dos Dados

Antes do treinamento, os dados passam pelas seguintes etapas:

1. Carregamento do dataset MNIST.
2. Redimensionamento das imagens para o formato adequado da CNN.
3. Normalização dos pixels para o intervalo [0,1].
4. Conversão das classes para One-Hot Encoding.
5. Separação dos dados em conjuntos de treino e validação.

---

## Arquitetura da CNN

A rede foi construída utilizando a API Sequential do Keras.

### Camadas do Modelo

```text
Input (28x28x1)

Conv2D (32 filtros, ReLU)
BatchNormalization
MaxPooling2D
Dropout 25%

Conv2D (64 filtros, ReLU)
BatchNormalization
MaxPooling2D
Dropout 25%

Conv2D (128 filtros, ReLU)
BatchNormalization
MaxPooling2D
Dropout 25%

Flatten
Dense (128 neurônios, ReLU)
Dropout
Dense (10 neurônios, Softmax)
```

### Técnicas Utilizadas

- Camadas convolucionais
- Max Pooling
- Batch Normalization
- Dropout
- Função de ativação ReLU
- Softmax para classificação multiclasse

---

## Avaliação do Modelo

### Acurácia

Avaliação do desempenho no conjunto de teste.

### Função de Perda (Loss)

Visualização da evolução da perda durante o treinamento e validação.

### Matriz de Confusão

Análise dos acertos e erros de classificação para cada dígito.

---
## Resultados

O modelo apresentou alta taxa de acerto na classificação dos dígitos manuscritos do dataset MNIST.

As métricas de desempenho podem ser observadas ao final da execução do notebook juntamente com:

- Acurácia final
- Loss final
- Gráficos de treinamento
- Matriz de confusão
---

## Como Testar o Projeto no Colab

Para testar o modelo com a sua própria imagem de um número, siga os passos abaixo:

- Fazer o Upload da Imagem
   
- No menu lateral esquerdo do Google Colab, clique no ícone de Pasta (Arquivos).

- Clique no ícone de Fazer upload para o armazenamento de sessão (ícone de uma folha com uma seta para cima).

- Selecione a imagem do número que você deseja que o modelo classifique e copie o caminho (ex: image1.jpg).

- Atualizar o Caminho no Código

- Antes de executar a célula de teste, você precisa atualizar a chamada da função com o nome exato do arquivo que você enviou.

- Procure pela última linha do código:

- prever_numero('/content/image1.jpg')

- Substitua o texto entre aspas pelo caminho da sua imagem. O caminho padrão será /content/ seguido do nome do seu arquivo (por exemplo: /content/foto_teste.png).
---
