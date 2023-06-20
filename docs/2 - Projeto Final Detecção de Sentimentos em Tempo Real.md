# Proposta do Projeto Final: Detecção de Sentimentos em Tempo Real

## Alunos

`Nícholas César Figueiredo Pereira`

`Rhian Luis Garcia Moraes`
 
## 1. Descrição Geral da Proposta

O objetivo deste projeto é desenvolver um sistema de análise de sentimento em tempo real, usando técnicas de processamento de imagem e aprendizado de máquina. O objetivo é analisar as expressões faciais das pessoas em imagens para determinar suas principais emoções, como alegria, tristeza, raiva, surpresa, entre outros.

O sistema proposto é baseado em um modelo de aprendizado de máquina treinado no conjunto de dados FER2013 contendo várias expressões faciais marcadas. O modelo pode reconhecer padrões em imagens que correspondem a diferentes expressões faciais e associá-los a diferentes emoções. O desenvolvimento é feito em Python usando bibliotecas de processamento de imagem, como OpenCV e scikit-image, e bibliotecas de aprendizado de máquina, como TensorFlow, Keras e scikit-learn.

O sistema proposto pode ter diversas aplicações práticas, principalmente analisando as reações do público em eventos esportivos, analisando as expressões faciais de pacientes em tratamento de saúde mental e analisando o feedback dos clientes.

Ao final do desenvolvimento, será testada a performance do aprendizado de máquina gerado, monitorando a atividade das pessoas que usam computadores para trabalhar e se divertir. O sistema analisará as expressões faciais de uma pessoa por meio de uma webcam para identificar e categorizar as emoções dominantes em várias atividades, como trabalhar, ler, assistir a vídeos e jogar. Isso fornece informações sobre os níveis de engajamento, satisfação e estresse dos usuários durante a interação com o computador, o que é útil para pesquisa de produtividade, bem-estar e usabilidade.

## 2. Ferramentas Tecnológicas

As seguintes ferramentas técnicas são usadas neste projeto:
- OpenCV: Uma biblioteca para processamento de imagens.
- TensorFlow, Keras, scikit-learn: Bibliotecas para desenvolver e treinar modelos de aprendizado de máquina.
- Conjunto de dados FER2013: Um conjunto de dados contendo imagens de expressões faciais marcadas.
- Matplotlib, Seaborn, Plotly: bibliotecas gráficas para visualizar os resultados da análise de sentimento.
- Jupyter Notebook, Google Colab: Ambiente de desenvolvimento para implementação de um sistema de análise de sentimento de imagem.

A arquitetura da rede neural utilizada será uma Rede Neural Convolucional (CNN) com as seguintes camadas:
- Camada de entrada: Conv2D com ativação ReLU e regularização L2.
- Camadas convolucionais adicionais: Conv2D com ativação ReLU e normalização em lote.
- Camadas de pooling: MaxPooling2D para reduzir a dimensionalidade.
- Camadas de Dropout: para regularização e evitar overfitting.
- Camadas densas: Fully Connected com ativação ReLU.
- Camada de saída: Dense com ativação softmax para classificação multiclasse.

As imagens de treinamento são pré-processadas utilizando uma função personalizada de pré-processamento. No código fornecido, o pré-processamento consiste em normalizar os pixels de cada imagem, dividindo-os pelo valor máximo de 255. Além disso, as variáveis de classe são convertidas em vetores one-hot.

O modelo é treinado por 100 épocas com um tamanho de lote de 64 imagens. Após o treinamento, o modelo treinado é salvo em disco em dois arquivos: um arquivo de modelo JSON e um arquivo de pesos HDF5. Esses arquivos podem ser utilizados posteriormente para carregar o modelo treinado e realizar testes e inferências.

## 3.Link de Implementação de Referência
https://www.kaggle.com/datasets/msambare/fer2013

## 4.Descrição dos Recursos da Implementação Original
O conjunto de dados FER2013, que consiste em uma série de imagens com expressões faciais, foi usado como referência. O conjunto de dados FER2013 consiste em milhares de imagens que capturam diferentes expressões faciais de diferentes indivíduos. Todas as imagens do conjunto de dados são do mesmo tamanho e as faces estão na mesma posição, o que simplifica a implementação do algoritmo neste contexto.

## 5.Descrição da Adaptação da Implementação de Referência
A implementação de referência do modelo de reconhecimento de expressão facial, originalmente baseada no conjunto de dados FER2013, foi significativamente modificada para permitir o reconhecimento em tempo real. O objetivo era capturar e processar expressões faciais diretamente da webcam do dispositivo, proporcionando aos usuários uma experiência interativa em tempo real.

A personalização inclui a integração de bibliotecas e ferramentas especiais para acessar webcams e capturar imagens de vídeo em tempo real. Esses quadros foram processados ​​imediatamente usando um modelo treinado no conjunto de dados FER2013 para identificar as expressões faciais presentes. Isso possibilitou detectar em tempo real as emoções exibidas pelo usuário na frente da câmera.

Com essa correção, o modelo de reconhecimento facial agora pode funcionar em tempo real, analisando os rostos das pessoas enquanto elas se movem e fazendo diferentes expressões faciais. Esse recurso amplia os recursos do seu modelo para que você possa usá-lo em tempo real para interagir com jogos, aplicativos de realidade aumentada, sistemas de segurança e muito mais.

A adaptação bem-sucedida de nossa implementação de referência para capturar e processar imagens de webcam em tempo real representa um grande avanço no campo do reconhecimento de expressões faciais. Essa abordagem fornece aos usuários uma experiência mais imersiva e interativa, permite monitoramento instantâneo e análise de emoções exibidas em tempo real e tem potencial para várias aplicações em entretenimento, saúde mental, ciência comportamental e outros campos relacionados.

## 6.Considerações Finais
Durante o desenvolvimento do projeto, foram feitas tentativas de realizar o ajuste automático dos hiperparâmetros a fim de otimizar o desempenho do modelo. No entanto, devido a limitações de tempo, alguns erros encontrados durante este processo não puderam ser corrigidos antes do envio da tarefa.

Autoajuste de hiperparâmetro refere-se a técnicas e algoritmos que automatizam o processo de encontrar a combinação ideal de valores para parâmetros externos configuráveis ​​de um modelo de aprendizado de máquina. Isso é importante porque os hiperparâmetros afetam o desempenho e o comportamento do modelo.

Existem várias abordagens para otimizar hiperparâmetros automaticamente, incluindo pesquisa em grade, pesquisa aleatória, otimização bayesiana, algoritmos genéticos e otimização de gradiente. Essas técnicas permitem que o sistema encontre com mais eficiência a configuração ideal de hiperparâmetros dadas as métricas de desempenho.

- Exemplo de código usando ajuste automático de hiperparâmetros:
 
from sklearn.datasets import load_iris

from sklearn.model_selection import RandomizedSearchCV

from sklearn.ensemble import RandomForestClassifier

from scipy.stats import randint
 
### Carregando o conjunto de dados Iris
iris = load_iris()
X = iris.data
y = iris.target 
### Definindo o modelo
model = RandomForestClassifier()
### Definindo a grade de valores para os hiperparâmetros
param_dist = {
	'n_estimators': randint(100, 1000),
	'max_depth': randint(1, 10),
	'min_samples_split': randint(2, 20),
	'min_samples_leaf': randint(1, 10)
}
### Criando o objeto RandomizedSearchCV
random_search = RandomizedSearchCV(
	estimator=model,
	param_distributions=param_dist,
	n_iter=10,  # número de combinações de hiperparâmetros a serem testadas
	cv=5,  # número de folds na validação cruzada
	random_state=42
)
### Executando a busca aleatória
random_search.fit(X, y)
 
### Imprimindo os melhores hiperparâmetros encontrados
print("Melhores hiperparâmetros encontrados:")
print(random_search.best_params_)
### Imprimindo a melhor pontuação (métrica de desempenho)
print("Melhor pontuação:", random_search.best_score_)
