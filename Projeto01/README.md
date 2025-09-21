Este repositório contém o Projeto 1 para a disciplina de **Algoritmos e Estruturas de Dados II**. O objetivo do projeto é modelar e analisar as relações entre instrumentos musicais com base em sua utilização conjunta em obras orquestrais famosas, utilizando a teoria dos grafos.

---

## Objetivo do Projeto

1. Criar uma base de dados a partir de um problema real
2. Transformar a base de dados em um grafo
3. Analisar o grafo usando o conteúdo ministrado
4. Visualizar de forma criativa os resultados
5. Organizar os artefatos gerados em um repositório no github
6. Apresentar os resultados
7. Experimentação com ferramentas de vibe-coding

## Sobre o Projeto

A análise se baseia em um conjunto de dados (`orquestras.csv`) que lista obras clássicas e os instrumentos necessários para sua execução. A partir desses dados, construímos uma rede onde os **instrumentos são os nós** e as **arestas representam a coocorrência** desses instrumentos na mesma obra.

### Estrutura do Dataset

O arquivo `orquestras.csv` possui as seguintes colunas:
* **Obra**: O nome da peça musical.
* **Compositor**: O nome do compositor.
* **Instrumentos**: Uma lista de instrumentos separados por vírgula.

---

## Como Executar o Projeto

Para executar a análise contida neste notebook, siga os passos abaixo:

**1. Pré-requisitos:**
-   Python 3.x
-   Jupyter Notebook ou Google Colab

**2. Instalação das Dependências:**
-   Instalação e adição do arquivo (`orquestras.csv`) no notebook (`projeto1.ipynb`)
-   Executar as linhas de códigos do indice das Dependências do notebook