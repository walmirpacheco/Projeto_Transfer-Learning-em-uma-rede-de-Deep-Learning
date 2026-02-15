# Projeto_Transfer-Learning-em-uma-rede-de-Deep-Learning

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Keras](https://img.shields.io/badge/Keras-2.x-red)
![Dataset](https://img.shields.io/badge/Dataset-198%20imagens-brightgreen)
![License](https://img.shields.io/badge/License-MIT-green)

## 📋 Sumário
- [Sobre o Projeto](#sobre-o-projeto)
- [Dataset](#dataset)
- [Arquitetura do Modelo](#arquitetura-do-modelo)
- [Pré-requisitos](#pré-requisitos)
- [Instalação e Configuração](#instalação-e-configuração)
- [Como Usar](#como-usar)
- [Resultados Obtidos](#resultados-obtidos)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Como Usar o Modelo Treinado](#como-usar-o-modelo-treinado)
- [Contribuições](#contribuições)
- [Licença](#licença)

## 📝 Sobre o Projeto

Este projeto implementa um classificador de imagens usando **Transfer Learning** com a arquitetura **VGG16** pré-treinada no ImageNet. O modelo foi treinado para distinguir entre imagens de gatos e cachorros utilizando um dataset balanceado de **198 imagens** (99 fotos de gatos e 99 fotos de cachorros).

### 🎯 Objetivos Alcançados
- ✅ Aplicar técnicas de Transfer Learning em Deep Learning
- ✅ Utilizar rede VGG16 pré-treinada como extrator de características
- ✅ Implementar fine-tuning para melhorar a performance
- ✅ Desenvolver um pipeline completo de classificação de imagens
- ✅ Trabalhar com dataset limitado (198 imagens) e obter bons resultados

## 📊 Dataset

### Especificações do Dataset Utilizado
- **Total de imagens**: 198 imagens
- **Distribuição**: 
  - 🐱 **Gatos**: 99 imagens
  - 🐶 **Cachorros**: 99 imagens
- **Formatos suportados**: JPG, JPEG, PNG
- **Divisão automática**:
  - **Treino (70%)**: 138 imagens (69 gatos + 69 cachorros)
  - **Validação (15%)**: 30 imagens (15 gatos + 15 cachorros)
  - **Teste (15%)**: 30 imagens (15 gatos + 15 cachorros)

### Data Augmentation (Treino)
Para compensar o dataset relativamente pequeno, foram aplicadas técnicas de data augmentation:

```python
- Rotação: até 20°
- Zoom: até 20%
- Deslocamento horizontal/vertical: 20%
- Cisalhamento: 20%
- Flip horizontal
- Preenchimento: nearest
