# Facial Emotion Recognition (FER) Model

O código apresentado é uma implementação de um sistema de reconhecimento de emoções faciais utilizando Deep Learning. O objetivo é identificar as emoções expressas em imagens faciais, classificando-as em sete categorias: "Raiva", "Nojo", "Medo", "Feliz", "Triste", "Surpresa" e "Neutro".

## Pré-requisitos

Python 3.x: o código pode ser executado em qualquer IDE compatível com Python. Bibliotecas Python: verifique se as bibliotecas necessárias estão instaladas. Você pode instalá-lo usando o comando pip install -r require.txt. IDE: O código pode ser executado em qualquer IDE que suporte Python, mas o trabalho foi realizado usando Visual Studio Code (VS Code) e Google Colab. Para executar o código neste projeto, recomendamos ter o Python instalado em seu sistema. O Python pode ser baixado e instalado no site oficial: https://www.python.org/

 O VS Code é um IDE gratuito popular que aprimora sua experiência de desenvolvimento para Python e outras linguagens. O VS Code pode ser baixado e instalado no site oficial: https://code.visualstudio.com/

 O Google Colab é uma plataforma baseada em nuvem que permite executar notebooks Jupyter diretamente no navegador. Fornece um ambiente de tempo de execução gratuito para escrever e executar código Python. Você pode acessar o Google Colab em https://colab.research.google.com/.

 Certifique-se de ter uma conexão estável com a Internet para poder baixar as dependências necessárias e acessar recursos externos conforme necessário enquanto seu código está em execução.

### Bibliotecas Usadas

Certifique-se de ter as seguintes bibliotecas instaladas:

- TensorFlow
- Keras
- NumPy
- scikit-learn
- OpenCV
- matplotlib

Caso não tenha-as instaladas, você pode instalá-las executando os seguintes comandos:

pip install tensorflow
pip install keras
pip install numpy
pip install sklearn
pip install opencv-python
pip install scikit-learn
pip install tensorflow-gpu

## Comentários Gerais

O código está dividido em várias seções, sendo cada uma delas demarcada por um cabeçalho iniciado por markdowns. Essas seções contêm explicações e comandos para instalação de bibliotecas, importação de módulos, pré-processamento de dados, treinamento e teste do modelo, criação de uma matriz de confusão e testes em imagens faciais.

O primeiro passo é instalar as bibliotecas necessárias para executar o código. Em seguida, são importados os módulos e pacotes necessários, como pandas, numpy, warnings, sklearn, keras, opencv-python e matplotlib. Essas bibliotecas são utilizadas para carregar e processar os dados, treinar o modelo, realizar testes, criar uma matriz de confusão e exibir os resultados.

A seção "Constants and Variables" define uma variável PATH que armazena o diretório onde os dados estão localizados. Essa variável é utilizada posteriormente para carregar e salvar os dados e modelos.

Na seção "Main", há duas subseções principais: "Pre Processing" e "Model Training". Em "Pre Processing", os dados são carregados a partir de um arquivo CSV, são pré-processados e as imagens são redimensionadas para um tamanho padrão. As características e rótulos dos dados são armazenados em variáveis, e os dados são salvos em arquivos numpy para uso posterior.

Na subseção "Model Training", o modelo de rede neural convolucional (CNN) é definido utilizando a biblioteca Keras. A CNN possui várias camadas convolucionais, de agrupamento, de dropout e totalmente conectadas. O modelo é compilado com otimizador Adam e função de perda categorical crossentropy. Em seguida, o modelo é treinado utilizando os dados pré-processados, e os pesos e arquitetura do modelo são salvos em arquivos para uso posterior.

Após o treinamento, o modelo é testado em um conjunto de dados separado. As previsões do modelo são comparadas com os rótulos verdadeiros, e a precisão do modelo é calculada e exibida.

A seção "Confusion Matrix" cria uma matriz de confusão para avaliar o desempenho do modelo em cada classe de emoção. A matriz é exibida em um gráfico de cores, onde os valores na diagonal principal representam as classificações corretas e os demais valores representam as classificações incorretas.

Finalmente, há duas seções extras: "Image Facial Emotion Recognition Test" e "Live Facial Emotion Recognition". A primeira seção permite testar o modelo em uma única imagem facial, enquanto a segunda seção permite o reconhecimento de emoções em tempo real utilizando a câmera do dispositivo. As emoções são identificadas e mostradas na imagem ou janela de vídeo, respectivamente.



