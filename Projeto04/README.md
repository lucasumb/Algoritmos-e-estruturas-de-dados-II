Este projeto vale 4,0 pontos para a Unidade 2 e 10 para a Unidade 3.
Utilizando o Gephi e bibliotecas em python, aplicar os conhecimentos vistos no curso (Semanas 10 e 11) para analisar a rede de estruturas complexas (Estudo de Caso do Wikipedia) a partir de métricas de centralidade e soluções de otimização.

---

## Base de dados

● A base de dados será a rede de links para o Wikipedia construída de forma similar ao apresentado na semana 11.
● A rede será mesclada (fusão de dados) a partir de 5 SEEDs de páginas de assuntos diferentes.
● O algoritmo de procura de links deverá explorar até o nível 2 (altura < 3). Reforçar, que em sala de aula foi feito uma altura inferior ao nível 2 (altura < 2).

---

## Objetivos

**REQUISITO 1**

● A partir da rede construída gerar figuras similares utilizando o Gephi.
● O tamanho do vértice deverá ser proporcional a quantidade de vizinhos. As cores devem ser relacionadas com o Closeness ou Betweenness ou Eigenvector Centrality.
● Adote um layout que seja razoável perceber a diferença entre as cores do vértices. As figuras devem ser acompanhadas de descrições/explicações.
● Pontuação: 4 pontos na Unidade 2.

**REQUISITO 2**

● A partir da rede construída gerar uma figura similar no gephi destacando o k-core e o k-shell da rede. O layout é de livre escolha. Os vértices devem ter um tamanho proporcional a propriedade degree. A figura deverá estar acompanhada de descrição/explicação.
● Pontuação: 3 pontos na Unidade 3.

**REQUISITO 3**

● A rede deverá estar em produção de forma análoga ao explicado na Semana 11. As cores deverão ser relacionadas ao critério de comunidade e o tamanho do vértice a uma métrica de livre escolha.
● Pontuação: 1 ponto na
Unidade 3.

**REQUISITO 4**

● É notório que durante a geração da rede explorar novos links até o nível 2 (altura < 3) irá demandar uma demanda computacional maior. O trabalho irá propor uma heurística e uma estrutura de dados para tornar isso possível.
● Pontuação: 6 pontos na Unidade 3.

---

## Como Executar o Projeto

Para executar a análise contida no [notebook](https://https://github.com/lucasumb/Algoritmos-e-estruturas-de-dados-II/tree/main/Projeto04/notebooks), siga os passos abaixo:

**1. Pré-requisitos:**
-   Python 3.x
-   Jupyter Notebook ou Google Colab

**2. Dependências:**
As principais bibliotecas utilizadas são:
-   `wikipedia`
-   `networkx`
-   `matplotlib`
-   `operator`

---

## Resultados

Eu decidir por analisar as cidades proximas a cidade em que vivo. Com isso, temos as cidades de:

- Natal, Rio Grande do Norte, Brazil
- Parnamirim, Rio Grande do Norte, Brazil
- São Gonçalo do Amarante, Rio Grande do Norte, Brazil
- Extremoz, Rio Grande do Norte, Brazil
- Macaíba, Rio Grande do Norte, Brazil
- Ceará-Mirim, Rio Grande do Norte, Brazil
- São José de Mipibu, Rio Grande do Norte, Brazil
- Nísia Floresta, Rio Grande do Norte, Brazil

Começando por Natal, após plotarmos a rede de ruas junto com os nós das universidades e bibliotecas públicas, podemos perceber que os caminhos entre elas são bastante próximos, se comparado às outras cidades. Além disso, há uma quantidade alta de bibliotecas em comparação ao número total de universidades, totalizando 15 bibliotecas e 14 universidades.

<center><img width="500" src="results/natal_mst.png"></center>

Em Parnamirim, não foi encontrada nenhuma universidade, mas possuía 51 escolas e 1 biblioteca. Decidiu-se, então, ligar as escolas e a biblioteca. Após plotarmos a rede de ruas junto com os nós, podemos perceber que a existência de uma única biblioteca causou uma maior distância média entre as escolas e ela. É uma região que poderia receber maior investimento em bibliotecas públicas para suprir os alunos daquela região.

<center><img width="500" src="results/parnamirim_mst.png"></center>

Em São Gonçalo do Amarante, foi encontrada 1 universidade e 2 bibliotecas públicas. Após plotarmos a rede de ruas com os nós, percebe-se que, mesmo com poucas instituições, elas são bem espalhadas e a universidade é bem próxima a uma das bibliotecas, o que demonstra uma preocupação em fornecer um local para estudos tanto para universitários quanto para a população. Identifica-se também uma área que poderia receber outra biblioteca para suprir a necessidade da população, mas seria necessário analisar a demografia desta determinada região.

<center><img width="500" src="results/gonçalo_mst.png"></center>

Em Extremoz, foram encontradas 9 universidades, mas nenhuma biblioteca pública. Decidiu-se, então, ligar apenas as universidades. No geral, as universidades estão bem próximas, de modo que, caso tivesse uma biblioteca, seria bem útil para os universitários de Extremoz.

<center><img width="500" src="results/extremoz_mst.png"></center>

Em Macaíba, foi encontrada 1 universidade e 1 biblioteca pública, resultando em um único caminho que as conecta.

<center><img width="500" src="results/macaiba_mst.png"></center>

Em Ceará-Mirim, não foi encontrada nenhuma universidade, mas possuía 30 escolas e 1 biblioteca pública. Decidiu-se, então, ligar as escolas e a biblioteca. Após plotarmos a rede de ruas com os nós, podemos perceber que ela está centralizada no meio da rede, estando próxima de muitas escolas, o que é bastante positivo.

<center><img width="500" src="results/ceara_mst.png"></center>

Em São José de Mipibu, não havia universidades nem bibliotecas, possuindo apenas 2 escolas. As escolas são bem distantes entre si.

<center><img width="500" src="results/saoJose_mst.png"></center>

Por fim, em Nísia Floresta, não havia universidades nem bibliotecas, possuindo 3 escolas. As escolas são próximas entre si, o que seria positivo para se pensar em construir uma biblioteca para suprir a população.

Referente aos resultados das métricas:

Comprimento total do MST (soma dos pesos das arestas no grafo completo de POIs)

Média do peso das arestas do MST

Desvio padrão do peso das arestas do MST

Comprimento total real da rede formada pelas rotas do MST

<center><img width="800" src="results/mst_metrics_table.png"></center>

Parnamirim e Ceará-Mirim destacam-se com os maiores comprimentos totais de MST (242.5 km e 146.2 km, respectivamente), indicando que seus POIs estão geograficamente mais dispersos.

No desvio padrão, as cidades como Macaíba e São José de Mipibu apresentam desvio zero, pois seus mapas revelam que a MST conecta apenas dois pontos. Diferente de Ceará-Mirim que exibe o maior desvio padrão (7.80), um fato explicado pelo seu mapa, que mostra um ponto no centro e vários outros pontos muito isolados.

Por outro lado, municípios como Macaíba (4.8 km) e Nísia Floresta (5.7 km) demonstram a menor dispersão, com pontos altamente concentrados, exigindo as redes de conexão (MST) mais curtas.

### Video explicativo

* [Parte 1](https://www.loom.com/share/6f824931d4ce4951873bb00f10767b6e)

* [Parte 2](https://www.loom.com/share/0746f21ae0d446be9b485c19aafef76c)

