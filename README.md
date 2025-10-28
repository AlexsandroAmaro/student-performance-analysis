# student-performance-analysis
# Análise de Performance: Decodificando os Hábitos dos Alunos

Este projeto é uma Análise Exploratória de Dados (EDA) focada em entender quais hábitos realmente impactam as notas finais dos alunos.

A investigação mergulha em um dataset de performance e hábitos de estudantes para encontrar padrões reais por trás das notas e testar o senso comum.

##  Objetivos

A análise foi dividida em duas questões centrais:
1.  Qual é o impacto real do **tempo de estudo** no desempenho?
2.  O tempo gasto em **redes sociais** realmente prejudica as notas?

##  Ferramentas Utilizadas

* **Python 3**
* **Pandas:** Para manipulação e tratamento dos dados.
* **Matplotlib & Seaborn:** Para visualização de dados (Heatmap, Scatter plot, Boxplot, Histograma).
* **Jupyter Notebook / Google Colab:** Como ambiente de análise.

---

##  Análise Exploratória (EDA)

O processo de descoberta foi dividido em três etapas principais:

### 1. O Mapa das Relações (Heatmap)

O primeiro passo foi criar um **mapa de calor (heatmap) de correlação** para obter uma visão geral de como todas as variáveis do dataset (notas, tempo de estudo, tempo em redes sociais, etc.) se relacionam.

Duas correlações saltaram aos olhos:
* **Correlação Forte e Positiva:** Entre `Nota` e `Tempo de Estudo`.
* **Correlação Fraca e Negativa:** Entre `Nota` e `Tempo em Redes Sociais`.

### 2. Investigação 1: Confirmando o Óbvio (Estudar Vale a Pena)

Para aprofundar a correlação positiva mais forte, um **gráfico de dispersão (scatter plot)** foi usado, confirmando visualmente que quanto mais tempo o aluno estuda, maior a tendência de sua nota ser alta.

Para quantificar esse impacto, a média de notas de dois grupos extremos foi comparada:
* Alunos que estudam **menos de 2 horas**: Média de **45**.
* Alunos que estudam **mais de 5 horas**: Média de **90**.

**Descoberta 1:** Alunos com mais de 5 horas de estudo tiveram, em média, o **dobro** da nota daqueles que estudaram menos de 2 horas.

### 3. Investigação 2: A Nuance da Distração (Redes Sociais)

A correlação "fraca e negativa" com o tempo de redes sociais foi mais intrigante. Um número fraco poderia significar ausência de relação ou uma relação mais complexa.

* Um **histograma** mostrou que os dados se concentravam em intervalos claros.
* Com base nisso, os alunos foram segmentados em três grupos: (0-2h), (2-4h) e (4-6h) de uso de redes sociais.

A ferramenta escolhida para comparar a distribuição das notas entre esses grupos foi o **Boxplot**.

**Descoberta 2:** Os boxplots revelaram a tendência que a correlação única não mostrava:
* **Mediana em Queda:** Alunos no grupo de 0-2 horas tinham a mediana de notas mais alta. Conforme o tempo nas redes sociais aumentava, a **mediana das notas caía progressivamente**.
* **A "Correlação Fraca":** Os gráficos também explicaram por que a correlação era fraca. Em todos os grupos havia alunos com notas altas e baixas (longas "caudas" no boxplot), mas a *tendência central* (mediana) claramente caía.

---

##  Conclusão do Projeto

Esta análise contou uma história de duas partes sobre o sucesso acadêmico:

1.  **O Fator Decisivo:** O tempo de estudo é o pilar com o impacto mais forte e direto nas notas.
2.  **O Fator Sutil:** Distrações, como o tempo excessivo em redes sociais, atuam como um "vento contrário" sutil, corroendo a performance média (mediana) mesmo que não impeçam casos isolados de sucesso.

O projeto demonstra o poder da Análise Exploratória em ir além de um único número de correlação, usando segmentação e as visualizações corretas (como Boxplots) para encontrar a verdadeira história por trás dos dados.
