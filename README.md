
# 🖼️ **Classificação de Sexo Biológico em Faces com Redes Neurais Convolucionais**

## 🧠 **Descrição do Projeto**
Este projeto teve como objetivo principal desenvolver modelos de **redes neurais convolucionais (CNNs)** para classificar imagens de rostos humanos em duas categorias: **masculino (0)** e **feminino (1)**. Durante o desenvolvimento, foram exploradas duas versões do modelo, cada uma com abordagens diferentes, destacando boas práticas e desafios enfrentados no pipeline.

O trabalho utilizou o **CUHK Face Sketch Database (CUFS)**, adaptado para classificação de sexo biológico. O pipeline incluiu preprocessamento das imagens, criação das arquiteturas CNN, treinamento e avaliação com métricas como **F1-Score**, **curva ROC** e **AUC-ROC**.

---

## 📂 **Sobre o Dataset**

O **CUHK Face Sketch Database (CUFS)** contém imagens faciais que variam em características como iluminação, ângulos e expressões. Para este projeto:
- Foram utilizadas **188 imagens** da pasta `photos`.
- Cada imagem foi rotulada manualmente para representar o sexo biológico:
  - **0:** Masculino.
  - **1:** Feminino.

### 🔧 **Preprocessamento Realizado**
- **Redimensionamento:** Imagens ajustadas para **250x200 pixels**.
- **Normalização:** Valores RGB escalados para o intervalo **[0, 1]**.
- **Divisão dos Dados:**  
  - **Treinamento:** 50% (94 imagens).  
  - **Validação:** 30% (56 imagens).  
  - **Teste:** 20% (38 imagens).  
  - Utilizou-se a **seed 23** para replicabilidade.

Embora o dataset seja limitado, ele proporcionou uma base para avaliar o desempenho das CNNs na tarefa de classificação.

---

## 🛠️ **Instalação e Execução**

### **1. Requisitos do Sistema**
- **Python 3.7+**.
- Google Colab ou ambiente local configurado para notebooks Jupyter.

### **2. Instalação de Dependências**
As bibliotecas necessárias podem ser instaladas com o comando:
`bash
pip install numpy pandas matplotlib scikit-learn tensorflow keras jupyter
`

### **3. Execução**
1. Faça upload do notebook desejado (`Modelo_CNN_Restic.ipynb` ou `Trabalho_Unidade_10_CNN_versao_2.ipynb`) para o Google Colab ou ambiente local.
2. Certifique-se de que as imagens do dataset estão na pasta `photos`, acessível no ambiente de execução.
3. Configure o ambiente para GPU no Colab:  
   - Vá em `Runtime > Change Runtime Type > GPU`.
4. Execute as células do notebook em ordem sequencial.

---

## 🗂️ **Estrutura do Repositório**

```
trabalho_unidade_10/
│
├── photos/                     # Pasta contendo as imagens do dataset
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
│
├── Modelo_CNN_Restic.ipynb     # Notebook principal da primeira versão
├── Trabalho_Unidade_10_CNN_versao_2.ipynb  # Notebook da segunda versão
├── README.md                   # Documentação do projeto
```

---

## 🔬 **Tecnologias Utilizadas**

- **Python** 🐍: Linguagem principal.
- **NumPy** 📊: Manipulação de arrays.
- **Pandas** 🐼: Análise de dados.
- **Matplotlib** 📉: Visualização gráfica.
- **Scikit-learn** 🧮: Avaliação de métricas.
- **TensorFlow/Keras** 🤖: Construção e treinamento do modelo.
- **Google Colab** 💻: Execução com suporte a GPU.

---

## 📊 **Resultados Obtidos**

### **Primeira Versão**
- **F1-Score:** Indicou um bom equilíbrio entre precisão e recall.
- **Curva ROC e AUC-ROC:** Confirmaram a capacidade do modelo de discriminar as classes.
- **Análise de Erros:** Limitada pela ausência de ferramentas adequadas para visualização, mas alguns padrões problemáticos foram identificados, como baixa iluminação e ângulos desfavoráveis.

### **Segunda Versão**
- Não conseguiu treinar o modelo devido a problemas na normalização.
- Apresentou melhor modularização e organização do código, facilitando a identificação de problemas e permitindo futuras melhorias.

---

## ⚙️ **Limitações e Melhorias Futuras**

### **Limitações**
- **Dataset reduzido:** Apenas 188 imagens, limitando a capacidade de generalização do modelo.
- **Execução no Colab:** Problemas de memória dificultaram experimentações extensas.

### **Melhorias Futuras**
- **Dataset:** Aumentar a quantidade de imagens e aplicar técnicas de aumento de dados (data augmentation).
- **Modelo:** Implementar arquiteturas mais profundas e ajustar hiperparâmetros como dropout e taxa de aprendizado.
- **Pipeline:** Modularizar ainda mais as etapas e desenvolver ferramentas para análise detalhada de erros.

---

## 💡 **Considerações Finais**

Este projeto demonstrou o potencial das CNNs para classificar imagens de faces, apesar das limitações do dataset e das dificuldades enfrentadas no pipeline. A primeira versão apresentou resultados promissores, enquanto a segunda destacou a importância de uma boa modularização. Com as melhorias sugeridas, o modelo pode se tornar mais robusto e generalizável, permitindo aplicações mais avançadas em classificação de imagens.  
Explore, aprenda e continue aprimorando! 🚀
```
