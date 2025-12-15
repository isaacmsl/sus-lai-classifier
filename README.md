# 🤖 Classificador de Manifestações LAI (Lei de Acesso à Informação) para o Ministério da Saúde

## 🎯 Objetivo

Desenvolver um modelo de Machine Learning para a classificação binária de manifestações da Lei de Acesso à Informação (LAI), determinando se uma solicitação é ou não de competência do Ministério da Saúde (MS).

O projeto lida com um desafio significativo de **extremo desbalanceamento de dados** (aprox. 95% das manifestações não são do MS).

## ✨ Solução Técnica

Para lidar com o desbalanceamento e garantir a confiabilidade da inferência, a solução técnica principal é:

1.  **Pré-processamento e Feature Extraction:** Aplicação de limpeza, lematização e vetorização utilizando **TF-IDF**.
2.  **Métrica de Avaliação:** Uso do **Matthews Correlation Coefficient (MCC)** para avaliar o desempenho de forma justa em dados desbalanceados.
3.  **Modelo Final:** **CalibratedClassifierCV** (com MCC de 0.506115) para garantir que as probabilidades de predição sejam bem calibradas, o que é crucial para uma inferência segura em um ambiente real.

## 🚀 Instalação e Execução

Siga os passos abaixo para configurar o ambiente e executar o projeto:

### Pré-requisitos

Certifique-se de ter o **Python 3.x** instalado em seu sistema.

### 1\. Clonar o Repositório

```bash
git clone https://github.com/isaacmsl/sus-lai-classifier
cd sus-lai-classifier
```

### 2\. Configurar o Ambiente Virtual (Recomendado)

Crie e ative um ambiente virtual para isolar as dependências do projeto:

```bash
python -m venv .venv
# Para Windows:
.\.venv\Scripts\activate
# Para Linux/macOS:
source .venv/bin/activate
```

### 3\. Instalar Dependências

Instale todas as bibliotecas necessárias listadas no `requirements.txt`:

```bash
pip install -r requirements.txt
```

### 4\. Execução

O projeto pode ser explorado e executado através dos *notebooks* na pasta `notebooks/`.

Basta iniciar o Jupyter Lab ou Jupyter Notebook para visualizar o processo de E.D.A., Pré-processamento, Treinamento e Avaliação do Modelo.

```bash
jupyter notebook
# ou
jupyter lab
```

-----

## 📄 Relatório e Documentação

O relatório completo detalhando a fundamentação teórica, a metodologia de calibração do modelo e a análise de resultados está disponível em [`relatorio_oficial.pdf`](https://docs.google.com/document/d/1wd9m0Sf7YmbvGp7FBaHZBVgVBPuewO1HcFsjXeY4gRM/edit?usp=sharing).

## 🧑‍💻 Autor

Isaac Marlon da Silva Lourenço. 

## 📜 Licença

Este projeto está sob a licença MIT.