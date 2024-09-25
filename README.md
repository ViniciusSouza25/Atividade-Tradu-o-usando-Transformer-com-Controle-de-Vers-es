
# Neural Machine Translation with Transformer

Este projeto demonstra a implementação e o treinamento de um modelo **Transformer** para realizar tradução automática de português para inglês. O modelo é inspirado no artigo ["Attention is All You Need"](https://arxiv.org/abs/1706.03762) de Vaswani et al. (2017), utilizando a biblioteca **TensorFlow** e **Keras**.

## Objetivo

Criar um sistema de tradução automática de sequências usando a arquitetura Transformer. O foco principal é traduzir frases de português para inglês usando o dataset [TED Talks HRLR](https://www.tensorflow.org/datasets/catalog/ted_hrlr_translate#ted_hrlr_translatept_to_en).

## Estrutura do Projeto

1. **Pré-processamento de Dados**: O dataset utilizado contém pares de sentenças em português e inglês. A pipeline de pré-processamento realiza:
   - Tokenização das frases.
   - Conversão dos tokens para embeddings usando a camada de embedding do Keras.
   - Preparação dos dados de entrada e saída para o modelo Transformer.

2. **Arquitetura do Modelo**:
   - **Encoder**: Lê a sentença de entrada (em português) e gera uma representação vetorial.
   - **Decoder**: Gera a tradução em inglês, palavra por palavra, utilizando a representação do encoder e o mecanismo de atenção.
   - **Atenção**: O modelo usa self-attention para capturar dependências globais na sentença, tanto na entrada quanto na saída.

3. **Treinamento**:
   - Treinamento supervisionado usando as sentenças em português como entrada e suas traduções em inglês como saída.
   - Utilização de técnicas como **masking** para lidar com comprimentos variáveis de frases e o treinamento eficiente com backpropagation.

4. **Avaliação**:
   - O desempenho é avaliado usando métricas de tradução automática, como **BLEU Score**.
   - Testes são realizados em um conjunto de validação separado do conjunto de treinamento.

## Resultados

Os resultados obtidos pelo modelo são comparados com as traduções de referência do dataset. A qualidade da tradução pode ser melhorada com ajustes no tamanho da arquitetura e no número de épocas de treinamento.

## Requisitos

Para rodar o projeto, você precisará dos seguintes pacotes:

- TensorFlow 2.x
- Keras
- NumPy
- Matplotlib
- TensorFlow Datasets

Instale-os com:

```bash
pip install tensorflow numpy matplotlib tensorflow-datasets
```

## alterações feitas
uma diminuição nos hyperparametros para melhor performance do modelo
como a diminuição de camadas, épocas entre outros.

## como executar
1. Clone o repositório ou faça o download do notebook.
2. Abra o notebook no [Google Colab](https://colab.research.google.com) ou localmente em um ambiente Jupyter.
3. Execute todas as células para treinar o modelo e visualizar os resultados.

## Referências

- ["Attention is all you need" - Vaswani et al. (2017)](https://arxiv.org/abs/1706.03762)
- [Google AI Blog: Transformer Model](https://ai.googleblog.com/2017/08/transformer-novel-neural-network.html)
- [TensorFlow Tutorial: Transformer](https://www.tensorflow.org/text/tutorials/transformer)
