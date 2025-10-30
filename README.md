#  Análise Comparativa de Métodos de Ordenação

**Disciplina:** Resolução de Problemas Estruturados em Computação



##  Algoritmos Desenvolvidos

O projeto contém a implementação manual dos seguintes algoritmos de ordenação:

* **Comb Sort**
* **Gnome Sort**
* **Bucket Sort**
* **Bubble Sort** *(com flag de parada)*
* **Selection Sort**
* **Cocktail Sort**


##  Resultados Obtidos

###  Vetor 1 — Dados Desordenados

| Algoritmo      | Trocas | Iterações |
| -------------- | ------ | --------- |
| Comb Sort      | 22     | 129       |
| Gnome Sort     | 78     | 175       |
| Bucket Sort    | 20     | 20        |
| Bubble Sort    | 78     | 180       |
| Selection Sort | 18     | 190       |
| Cocktail Sort  | 78     | 154       |

**Mais eficiente em trocas:** Selection Sort
**Menos iterações:** Bucket Sort



###  Vetor 2 — Dados Já Ordenados

| Algoritmo      | Trocas | Iterações |
| -------------- | ------ | --------- |
| Comb Sort      | 0      | 110       |
| Gnome Sort     | 0      | 19        |
| Bucket Sort    | 20     | 20        |
| Bubble Sort    | 0      | 19        |
| Selection Sort | 0      | 190       |
| Cocktail Sort  | 0      | 19        |

**Menos trocas:** Empate entre Comb, Gnome, Bubble, Selection e Cocktail
**Menos iterações:** Gnome, Bubble e Cocktail Sort (19)



###  Vetor 3 — Dados em Ordem Decrescente

| Algoritmo      | Trocas | Iterações |
| -------------- | ------ | --------- |
| Comb Sort      | 18     | 129       |
| Gnome Sort     | 190    | 399       |
| Bucket Sort    | 20     | 20        |
| Bubble Sort    | 190    | 190       |
| Selection Sort | 10     | 190       |
| Cocktail Sort  | 190    | 190       |

**Mais econômico em trocas:** Selection Sort
**Menos iterações:** Bucket Sort


##  Desempenho Geral

###  Média de Trocas

| Posição | Algoritmo      | Média |
| ------- | -------------- | ----- |
|  1º   | Selection Sort | 9.33  |
|  2º   | Comb Sort      | 13.33 |
|  3º   | Bucket Sort    | 20.00 |
| 4º      | Cocktail Sort  | 89.33 |
| 5º      | Gnome Sort     | 89.33 |
| 6º      | Bubble Sort    | 89.33 |



###  Média de Iterações

| Posição | Algoritmo      | Média  |
| ------- | -------------- | ------ |
|  1º   | Bucket Sort    | 20.00  |
|  2º   | Gnome Sort     | 197.66 |
|  3º   | Comb Sort      | 122.66 |
| 4º      | Cocktail Sort  | 121.00 |
| 5º      | Bubble Sort    | 129.66 |
| 6º      | Selection Sort | 190.00 |



## Considerações Finais

* **Bucket Sort** foi o mais eficiente em número de iterações, demonstrando quase linearidade em vetores com tamanho controlado.
* **Selection Sort** destacou-se por realizar o menor número de trocas, já que cada posição é ajustada com apenas uma substituição.
* **Comb Sort** apresentou um desempenho equilibrado entre trocas e iterações.
* **Gnome Sort**, **Bubble Sort** e **Cocktail Sort** exibiram comportamentos semelhantes em listas desordenadas, realizando muitas comparações e permutações.
* Em **listas ordenadas**, os algoritmos com otimização de parada (Bubble e Cocktail) e avanço adaptativo (Gnome) evitaram processamento desnecessário.
* Para **listas decrescentes**, o **Selection Sort** manteve eficiência em trocas, mesmo com elevado número de comparações.

