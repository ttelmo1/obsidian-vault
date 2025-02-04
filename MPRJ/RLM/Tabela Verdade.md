![[Pasted image 20250204064143.png]]

### Bizu
1. Realizar a potencia de proposições
2. Montar o primeiro obtendo a metade do resultado da potencia
3. Montar o segundo com a metade do primeiro
4. Montar o terceiro com a metade do segundo...
### **Como montar uma tabela-verdade**

5. **Identifique as proposições simples**: Determine quantas proposições existem. Geralmente, são representadas por letras como PPP e QQQ.
6. **Determine o número de linhas**: O número de linhas da tabela é dado por 2n2^n2n, onde nnn é o número de proposições simples. Exemplo:
    - 1 proposição → 2^1 = 2   linhas
    - 2 proposições → 2^2=4   linhas
    - 3 proposições → 2^3=8   linhas
7. **Preencha as colunas das proposições simples**: A primeira metade das linhas é preenchida com "V", e a segunda metade com "F", depois repete o padrão para a próxima proposição dividindo ao meio.
8. **Aplique os operadores lógicos**:
    - **Negação (¬P\neg P¬P)**: Inverte o valor lógico.
    - **Conjunção (P∧QP \land QP∧Q)**: Só é verdadeira se ambas as proposições forem verdadeiras.
    - **Disjunção (P∨QP \lor QP∨Q)**: É verdadeira se pelo menos uma das proposições for verdadeira.
    - **Condicional (P→QP \rightarrow QP→Q)**: Só é falsa quando PPP é verdadeiro e QQQ é falso.
    - **Bicondicional (P↔QP \leftrightarrow QP↔Q)**: Só é verdadeira quando ambas as proposições têm o mesmo valor lógico.

### **Exemplo de tabela-verdade para P∨Q

| P   | Q   | P∨Q |
| --- | --- | --- |
| V   | V   | V   |
| V   | F   | V   |
| F   | V   | V   |
| F   | F   | F   |
