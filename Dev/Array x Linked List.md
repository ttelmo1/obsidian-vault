#DSA 
Arrays e listas ligadas (linked lists) são estruturas de dados usadas para armazenar coleções de elementos, mas possuem diferenças fundamentais em termos de armazenamento, acesso e manipulação.

### **Array**:

- **Armazenamento:** Em blocos contíguos de memória.
- **Acesso:** Rápido (O(1)) por índice.
- **Inserção/remoção:** Lenta (O(n)) se feita no meio ou início, pois requer deslocamento de elementos.
- **Uso de memória:** Tamanho fixo, pode desperdiçar ou necessitar realocação.

### **Linked List**:

- **Armazenamento:** Elementos (nós) espalhados na memória, ligados por ponteiros.
- **Acesso:** Lento (O(n)), pois requer percorrer a lista.
- **Inserção/remoção:** Rápida (O(1)) se feita com ponteiros corretamente ajustados Ou seja anteriormente definidos. Caso contrário devemos considerar **O(N)**.
- **Uso de memória:** Ocupa mais espaço devido aos ponteiros adicionais.
### **Estrutura com Head e Tail:**
Quando implementada usando uma **doubly linked list (lista duplamente ligada)**, a fila possui dois ponteiros principais:

- **Head (Cabeça):** Aponta para o primeiro nó da fila (o próximo a ser removido).
- **Tail (Cauda):** Aponta para o último nó da fila (onde novos elementos são inseridos).

**Resumo:** Arrays são mais eficientes para acesso direto e ocupam menos memória, enquanto listas ligadas são mais flexíveis para inserções/remoções frequentes.

