#DSA
- Fala sobre escalabilidade, e não necessariamente sobre performance
- Pode medir complexidade Temporal e complexidade Espacial

### Temporal diz respeito ao tempo
- Buscar o primeiro elemento em um array de 1 ou de 1 milhão de elementos leva o mesmo tempo
### Espacial diz sobre quanto de memória foi alocado
- Se precisarmos alocar 10 milhões de arrays na memória ele ainda assim será o(1), pois já foi definido a quantidade de memória necessária.

📌**Geralmente vão perguntar mais sobre tempo do que memória

### Tipos de Big O
- O(1) - Constante
- O(Log N) - [[Busca binária]]
- O(N) - Escala na mesma medida que o input aumenta
- O(N Log N) - quicksort, merge sort. Dividir e conquistar
- O(N^2)- For dentro de for
- O(2^N) / O(Raiz de N) Nunca viu cair
- O(N!) - Implementação mal feita de Fibonacci

- O(1): Tempo constante, independentemente do tamanho da entrada.
- O(log n): Crescimento logarítmico, aumenta lentamente à medida que a entrada cresce. 
- O(n log n): Crescimento log-linear, comum em algoritmos de ordenação eficientes.
- O(n^2): Crescimento quadrático, o tempo de execução aumenta exponencialmente com o tamanho da entrada. 
- O(2^n): Crescimento exponencial, o tempo de execução dobra com cada incremento no tamanho da entrada.

