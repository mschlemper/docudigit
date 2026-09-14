# DocuDigit: Classificador de Dígitos Manuscritos com Análise Preditiva

## Mini-Projeto Avaliativo - Módulo 2 - Semana 05

### Aluno: Marco Aurelio Schlemper

---

## 💡 O Problema Resolvido

Em diversas aplicações, como automação de leitura de formulários, processamento de cheques bancários ou até mesmo em sistemas de entrada de dados, a capacidade de identificar e classificar automaticamente dígitos manuscritos é crucial. Erros nessa identificação podem levar a ineficiências operacionais, perdas financeiras ou dificuldades na digitalização de informações históricas.

O DocuDigit propõe uma solução robusta para este desafio, construindo um pipeline de Machine Learning capaz de classificar com alta precisão dígitos manuscritos, utilizando o famoso dataset MNIST como base. Além da classificação padrão, o projeto explora a robustez do sistema diante de dados "fora de distribuição" (Out-of-Distribution - OOD) e demonstra a inferência com imagens desenhadas pelo próprio usuário, abordando um problema real de digitalização de documentos e formulários.

---

## 🛠️ Técnicas e Tecnologias Utilizadas

Este projeto é um pipeline de Ciência de Dados ponta a ponta construído em Python, utilizando uma série de bibliotecas e técnicas:

### Linguagem e Ambiente
*   Python: Linguagem de programação principal.
*   Jupyter Notebook (.ipynb): Ambiente interativo para desenvolvimento, documentação e execução do código.

### Bibliotecas Principais
*   `scikit-learn`: Essencial para:
        Carregamento do dataset MNIST (`fetch_openml`).
        Divisão de dados (`train_test_split`).
        Modelos de Machine Learning: `SVC` (Support Vector Machine), `RandomForestClassifier`, `MLPClassifier` (Multi-layer Perceptron).
        Métricas de Avaliação: `accuracy_score`, `precision_score`, `recall_score`, `f1_score`, `confusion_matrix`, `classification_report`.
*   `pandas`: Manipulação e análise de dados, especialmente para visualização da distribuição de classes e comparação de métricas.
*   `numpy`: Computação numérica eficiente, fundamental para manipulação de arrays de pixels.
*   `matplotlib` & `seaborn`: Geração de gráficos para Análise Exploratória de Dados (EDA), visualização de dígitos, matrizes de confusão e resultados de inferência.
*   `Pillow (PIL)`: Processamento de imagens personalizadas (carregamento, conversão de cores, redimensionamento, centralização).

### Conceitos Abordados
*   Análise Exploratória de Dados (EDA): Entendimento da estrutura do dataset MNIST, distribuição de classes e visualização de exemplos.
*   Pré-processamento de Dados: Normalização de pixels (0-255 para 0-1) e justificativa, divisão estratificada em treino, validação e teste.
*   Modelagem Preditiva Multiclasse: Implementação e treinamento de diferentes algoritmos de classificação.
*   Otimização de Hiperparâmetros: Ajuste manual e justificação das escolhas de hiperparâmetros para cada modelo.
*   Avaliação de Modelos: Uso de Matrizes de Confusão, Relatórios de Classificação e tabelas comparativas para análise de desempenho.
*   Generalização Extrema (Out-of-Distribution - OOD): Teste da robustez do modelo em cenários com classes não vistas durante o treinamento, explorando o conceito de "falsa certeza".
*   Pipeline de Inferência: Criação de um fluxo de trabalho completo para pré-processar e prever dígitos em imagens manuscritas externas.

---

## 🚀 Como Executar o Sistema

Para executar este pipeline de Ciência de Dados, siga os passos abaixo:

1.  Clone o Repositório:
    ```bash
    git clone https://github.com/seu-usuario/seu-repositorio.git
    cd seu-repositorio
    ```

2.  Crie e Ative um Ambiente Virtual (Recomendado):
    ```bash
    python -m venv venv
    # No Linux/macOS:
    source venv/bin/activate
    # No Windows:
    .\venv\Scripts\activate
    ```

3.  Instale as Dependências:
    Instale todas as bibliotecas necessárias utilizando o arquivo `requirements.txt` fornecido:
    ```bash
    pip install -r requirements.txt
    ```

4.  Execute o Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
    Isso abrirá uma interface no seu navegador. Navegue até o arquivo `.ipynb` do projeto e abra-o.

5.  Execute as Células:
    Execute todas as células do notebook sequencialmente. O notebook é estruturado para guiar você por todas as fases do projeto, desde o carregamento de dados até a inferência com imagens personalizadas.

6.  Imagens Manuscritas Personalizadas (Desafio C):
    Para o Desafio C da Fase 5, você precisará ter as imagens manuscritas no formato `CARACTERX.png` (onde X é o dígito) na raiz do diretório onde o notebook está sendo executado. As imagens `CARACTER0.png` a `CARACTER9.png` foram utilizadas neste projeto.

---

## 📈 Melhorias Futuras

O projeto DocuDigit pode ser expandido e aprimorado de diversas formas:

*   Ajuste Fino de Hiperparâmetros: Utilizar técnicas mais avançadas como `GridSearchCV` ou `RandomizedSearchCV` para otimização sistemática dos hiperparâmetros dos modelos, potencialmente explorando uma gama maior de valores e diferentes kernels para o SVM, e arquiteturas de camadas ocultas para o MLP.
*   Novos Modelos: Explorar modelos mais avançados de Deep Learning, como Redes Neurais Convolucionais (CNNs), que são especificamente projetadas para dados de imagem e geralmente superam modelos baseados em MLP para o MNIST.
*   Aumento de Dados (Data Augmentation): Aplicar transformações como rotação, translação, zoom e distorção nas imagens de treinamento para aumentar a robustez do modelo e melhorar sua generalização.
*   Detecção de OOD: Implementar algoritmos específicos para detecção de dados fora de distribuição, permitindo que o modelo identifique e sinalize quando uma entrada é desconhecida, em vez de fazer uma previsão "falsa certeza".
*   Interface Gráfica: Desenvolver uma interface gráfica simples (e.g., com `Streamlit`, `Flask` ou `Django`) para permitir que usuários carreguem suas próprias imagens de dígitos e obtenham previsões em tempo real.
*   Exportação do Modelo: Salvar o modelo treinado em um formato persistente (e.g., `pickle`, `joblib` ou `ONNX`) para que possa ser facilmente implantado em outras aplicações.
*   TensorBoard / Ferramentas de Visualização: Integrar ferramentas como TensorBoard para uma visualização mais rica do processo de treinamento de redes neurais (ex: visualização de gráficos de perda, pesos, etc.).

---

