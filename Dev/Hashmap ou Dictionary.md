#DSA 
Um **Hashmap** é uma estrutura de dados que armazena pares **chave-valor**, permitindo acesso rápido aos valores por meio de suas chaves. Ele utiliza uma **função hash** para mapear as chaves a posições (índices) em um array interno, garantindo eficiência na busca, inserção e remoção.

### **Principais Características:**

- **Tempo de acesso:** O(1) em média, graças ao uso de hashing. Podendo chegar a O(N) se considerarmos colisões, que devemos tratar com outra estrutura de dados, normalmente Linked list
- **Armazena pares chave-valor:** Cada chave é única e mapeia para um único valor.
- **Usa uma função hash:** Converte a chave em um índice do array interno.
- **Gerenciamento de colisões:** Resolve situações onde diferentes chaves geram o mesmo índice.

### **Gerenciamento de Colisões:**

2. **Encadeamento (Chaining):** Usa listas ligadas em cada índice para armazenar múltiplos elementos.
3. **Endereçamento Aberto:** Encontra outro índice disponível dentro do próprio array.

### **Principais Operações:**

- **`put(key, value)` (Inserção/Atualização - O(1) em média)**
    
    - Calcula o índice usando a função hash.
    - Insere o par na posição correta.
    - Em caso de colisão, aplica a estratégia de resolução.
- **`get(key)` (Busca - O(1) em média)**
    
    - Calcula o índice da chave usando a função hash.
    - Retorna o valor correspondente ou `null` se a chave não existir.
- **`remove(key)` (Remoção - O(1) em média)**
    
    - Localiza a chave e remove seu par da estrutura.

### **Vantagens:**

✔️ Acesso rápido a dados.  
✔️ Evita busca sequencial.  
✔️ Ideal para grandes conjuntos de dados.

### **Desvantagens:**

❌ Uso de memória extra devido ao array interno.  
❌ Possíveis colisões podem degradar o desempenho.  
❌ Não mantém ordem dos elementos.