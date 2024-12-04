Segue o código **completo** do markdown atualizado:


# 🖼️ **Classificação de Sexo Biológico em Faces com Redes Neurais Convolucionais**

## 🧠 **Descrição do Projeto**
Este projeto tem como objetivo principal desenvolver um modelo de aprendizado profundo baseado em **redes neurais convolucionais (CNNs)** para classificar imagens de rostos humanos em duas categorias: **masculino (0)** e **feminino (1)**.  

O desafio envolve lidar com um conjunto de dados limitado, extraído do **CUHK Face Sketch Database (CUFS)**, que originalmente foi criado para mapeamento entre fotografias de rostos e seus esboços artísticos correspondentes. Para este projeto, as imagens foram adaptadas para classificação de sexo biológico.  

O pipeline completo inclui etapas de preprocessamento das imagens, desenvolvimento de uma arquitetura CNN personalizada, treinamento do modelo e análise dos resultados por meio de métricas como **F1-Score**, **curva ROC** e **AUC-ROC**.  

---

## 📂 **Sobre o Dataset**

O **CUHK Face Sketch Database (CUFS)** contém um conjunto de imagens faciais que apresentam variabilidades em termos de características como idade, expressões faciais e condições de captura. Para este projeto:
- Foram utilizadas **188 imagens** da pasta `photos`.
- As imagens originais foram analisadas manualmente e rotuladas para indicar sexo biológico:
  - **0:** Masculino.  
  - **1:** Feminino.

### 🔧 **Preprocessamento Realizado**
- **Redimensionamento:** Todas as imagens foram ajustadas para o tamanho padrão de **250x200 pixels**.
- **Normalização:** Os valores RGB foram escalados para o intervalo **[0,1]**.
- **Divisão dos Dados:**
  - **Treinamento:** 50% (94 imagens).
  - **Validação:** 30% (56 imagens).
  - **Teste:** 20% (38 imagens).  
  - Utilizou-se a **seed 23** para garantir a replicabilidade da divisão.

O dataset, apesar de limitado em tamanho, forneceu uma base para explorar as capacidades das redes convolucionais no reconhecimento de padrões faciais.

---

## 🛠️ **Instalação e Execução**

### **1. Requisitos do Sistema**
Antes de começar, certifique-se de que você possui:
- **Python 3.7+** instalado no seu ambiente.
- Google Colab ou um ambiente local configurado para execução de notebooks Jupyter.

### **2. Instalação de Dependências**
Não é necessário criar um arquivo `requirements.txt` separado. Todas as bibliotecas necessárias podem ser instaladas diretamente com o comando:
`bash
pip install numpy pandas matplotlib scikit-learn tensorflow keras jupyter`


### **3. Execução no Google Colab**
1. Faça upload do notebook `Modelo_CNN_Restic.ipynb` no Google Colab.
2. Certifique-se de que as imagens do dataset estão na pasta `photos`, acessível no ambiente de execução.
3. No Colab, altere o ambiente para utilizar GPU:
   - Vá em `Runtime > Change Runtime Type > GPU`.
4. Execute as células do notebook em ordem sequencial.

### **4. Observações**
- Se houver problemas com memória durante o treinamento, considere reiniciar o ambiente do Colab.
- Mantenha o dataset na pasta especificada e use caminhos relativos no código para evitar erros de leitura.

---

## 🗂️ **Estrutura de Arquivos**

A organização do repositório foi projetada para facilitar a navegação e execução do projeto:

```
trabalho_unidade_10/
│
├── photos/                     # Pasta contendo as imagens do dataset
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
│
├── Modelo_CNN_Restic.ipynb     # Notebook principal com o código do projeto
├── README.md                   # Documentação do projeto
```

---

## 🔬 **Tecnologias Utilizadas**

O projeto foi desenvolvido utilizando ferramentas modernas de aprendizado profundo e análise de dados:

1. **Python** 🐍  
   Linguagem de programação principal para implementação do projeto.

2. **Bibliotecas:**
   - **NumPy** 📊: Manipulação de arrays e operações matemáticas.
   - **Pandas** 🐼: Manipulação e análise de dados.
   - **Matplotlib** 📉: Geração de gráficos para visualização dos resultados.
   - **Scikit-learn** 🧮: Avaliação de métricas como F1-Score e ROC.
   - **TensorFlow** 🤖: Framework para construção e treinamento do modelo CNN.
   - **Keras** 🧠: API de alto nível para definição da arquitetura da rede neural.

3. **Google Colab** 💻  
   Ambiente utilizado para executar o notebook com suporte a GPUs gratuitas.

4. **Jupyter Notebook** 📓  
   Estrutura do código implementada no formato interativo de notebooks.

---

## 📊 **Resultados Obtidos**

- **F1-Score:** Indicou um bom equilíbrio entre precisão e recall, validando a capacidade do modelo de identificar corretamente ambas as classes.
- **Curva ROC e AUC-ROC:** Confirmação de que o modelo tem habilidade de discriminar entre as classes, mesmo com dados limitados.
- **Análise de Erros:** As imagens classificadas incorretamente apresentaram desafios como baixa iluminação e ângulos desfavoráveis, destacando limitações no dataset e na arquitetura.

---

## ⚙️ **Limitações e Melhorias Futuras**

### **Limitações:**
1. **Dataset reduzido:** Apenas 188 imagens, o que compromete a capacidade do modelo de generalizar para novos dados.
2. **Execução no Colab:** Problemas de memória e limitações no gerenciamento das células dificultaram experimentações rápidas.

### **Melhorias Futuras:**
1. **Dataset:**
   - Aumentar a quantidade e diversidade das imagens.
   - Aplicar técnicas de **data augmentation** para simular variações e melhorar a robustez.
2. **Modelo:**
   - Implementar arquiteturas mais profundas, adicionando mais blocos convolucionais.
   - Ajustar hiperparâmetros, como taxa de aprendizado, número de filtros e dropout.
3. **Código:**
   - Modularizar funções para melhorar a organização e o reuso do código.
   - Utilizar ambientes locais ou servidores com maior capacidade computacional para evitar problemas de memória.

---

## 💡 **Considerações Finais**

Este projeto demonstrou o poder e os desafios das redes neurais convolucionais na resolução de problemas práticos de classificação de imagens. Apesar das limitações, como o dataset reduzido e as restrições de memória no ambiente Colab, os resultados foram promissores, destacando o potencial de CNNs personalizadas para identificar padrões visuais.

Para trabalhos futuros, as melhorias sugeridas podem expandir a aplicabilidade do modelo, tornando-o mais robusto e capaz de generalizar para condições mais diversas. Este projeto reafirma a importância de um pipeline bem estruturado e incentiva a exploração contínua de tecnologias avançadas no campo do aprendizado profundo.

🎯 **Explorar, aprender e aprimorar:** essa é a essência do aprendizado em projetos como este!
``` 
