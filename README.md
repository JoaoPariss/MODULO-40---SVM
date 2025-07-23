# MODULO-40---SVM

Nessa atividade trabalhamos novamente com a base de dados de propensão a compra de carros. Porém dessa vez nós utilizamos o SVM.

O objetivo era verificar como o modelo performava utilizando o SVM linear e poly. E, também, comparar com a perfomance do modelo utilizando o XGBoost, feito no exercício 39.

--

## Etapas 

### 1. Carregamento e verificação inicial dos dados
- Base de dados foi carregada
- Tipo dos dados foi verificado
- Valores nulos foram verificados
- Coluna ID foi removida

### 2. Codificação da coluna Gender
- A coluna Gender foi codificada utilizando o Label Encoder

### 3. Plotagem e análise da matriz de correlação
- Foi verificado quais eram as variáveis mais correlacionadas à target, Purchased.

### 4. Separação da base
- Primeiramente foi separada a base em X e Y
- Após, a base foi separada em treino e teste: y_train, y_test, x_train, x_test

### 5. Treinamento do modelo
- O modelo foi treinado utilizando o kernel linear

### 6. Previsão e avaliação para a base teste
- Foram realizadas as previsões para x_test
- Modelo foi avaliado:
- Foi encontrado uma acurácia relativamente alta: 0.81. Contudo, para a classe 1 foi observado um recall de apenas 0.69, demonstrando uma certa dificuldade para identificar corretamente os casos positivos

### 7. Treinamento do modelo com kernel poly, realização das previsões e avaliações
- Foi feito o treinamento do modelo com o kernel poly e as previsões para x_test
- Modelo foi avaliado:
- O modelo obteve um desempenho inferior ao linear, com uma acurácia de 0.7. O ponto mais crítico com o recall da classe 1 de apenas 0.36, indicando um possível enviesamento do modelo.

### 8. Comparação SVM x XGBoost
- Ao comparar a perfomance dos modelos SVM com o XGBoost pôde-se observar uma perfomance superior do XGBoost. Tanto na acurácia geral: 0.905 a 0.81. Quanto no recall da classe 1: 0.86 a 0.69

