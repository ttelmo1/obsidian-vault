#DSA 
Python tem uma sintaxe simples e expressiva, sem a necessidade de **ponto e vírgula (`;`)** ou **chaves (`{}`)** – a indentação (espaço/tab) define blocos de código.

### Instalação
[Como Instalar Python e Visual Studio Code no Windows | Python do Jeito Certo 2.0](https://www.youtube.com/watch?v=R9dLGLVqK9Q)

---

## **📌 1. Variáveis e Tipos de Dados**

Em Python, você **não** precisa declarar o tipo da variável explicitamente. A tipagem é **dinâmica** e **forte**.

```
# Inteiro, Float, String, Booleano 
idade = 25       # int 
preco = 19.99    # float 
nome = "Python"  # str 
ativo = True     # bool
```

➡ Em C#: `int idade = 25;`  
➡ Em JavaScript: `let idade = 25;`

---

## **📌 2. Estruturas de Dados (Listas, Tuplas, Dicionários, Conjuntos)**

### **📍 Listas (equivalente a Arrays em C# e JavaScript)**

`numeros = [1, 2, 3, 4, 5] numeros.append(6)  # Adiciona um elemento numeros.remove(3)  # Remove o número 3 print(numeros[0])  # Acessa o primeiro elemento (índice 0)`

➡ Em C#: `List<int> numeros = new List<int> {1, 2, 3, 4, 5};`  
➡ Em JS: `let numeros = [1, 2, 3, 4, 5];`

---

### **📍 Tuplas (Imutáveis, tipo um "readonly array")**

python

CopiarEditar

`coordenadas = (10, 20) x, y = coordenadas  # Desempacotamento`

➡ Em C#: `readonly struct (int x, int y) = (10, 20);`  
➡ Em JS: `const coordenadas = Object.freeze([10, 20]);`

---

### **📍 Dicionários (Equivalente a Objetos em JS ou Dictionary em C#)**

python

CopiarEditar

`pessoa = {"nome": "Alice", "idade": 30} print(pessoa["nome"])  # Acessa o valor da chave "nome" pessoa["cidade"] = "São Paulo"  # Adiciona nova chave-valor`

➡ Em C#: `Dictionary<string, object> pessoa = new() { {"nome", "Alice"}, {"idade", 30} };`  
➡ Em JS: `let pessoa = { nome: "Alice", idade: 30 };`

---

## **📌 3. Estruturas de Controle (If, Loops, Compreensões)**

### **📍 If / Else**

`x = 10 if x > 5:     print("Maior que 5") elif x == 5:     print("Igual a 5") else:     print("Menor que 5")`

➡ Em C#: `if (x > 5) { Console.WriteLine("Maior que 5"); }`  
➡ Em JS: `if (x > 5) { console.log("Maior que 5"); }`

---

### **📍 Loops (For e While)**

#### **For (Percorrendo listas)**

`numeros = [1, 2, 3, 4] for num in numeros:     print(num)`

➡ Em C#: `foreach (var num in numeros) { Console.WriteLine(num); }`  
➡ Em JS: `for (let num of numeros) { console.log(num); }`

#### **While**

`x = 5 while x > 0:     print(x)     x -= 1`

➡ Em C#: `while (x > 0) { Console.WriteLine(x); x--; }`  
➡ Em JS: `while (x > 0) { console.log(x); x--; }`

---

## **📌 4. Funções (Métodos)**


```
def soma(a, b):     
return a + b 
print(soma(3, 4))
```

➡ Em C#: `int Soma(int a, int b) { return a + b; }`  
➡ Em JS: `function soma(a, b) { return a + b; }`

### **Função Lambda (Arrow Function em JS)**

`soma = lambda a, b: a + b print(soma(3, 4))`

➡ Em C#: `Func<int, int, int> soma = (a, b) => a + b;`  
➡ Em JS: `const soma = (a, b) => a + b;


---

## **📌 5. Classes e Objetos**


`class Pessoa:     def __init__(self, nome, idade):         self.nome = nome         self.idade = idade      def saudacao(self):         return f"Olá, meu nome é {self.nome} e tenho {self.idade} anos."  p = Pessoa("Lucas", 25) print(p.saudacao())`

➡ Em C#:


`class Pessoa {     public string Nome { get; }     public int Idade { get; }      public Pessoa(string nome, int idade) {         Nome = nome;         Idade = idade;     }      public string Saudacao() => $"Olá, meu nome é {Nome} e tenho {Idade} anos."; }`

➡ Em JS:

javascript

CopiarEditar

``class Pessoa {     constructor(nome, idade) {         this.nome = nome;         this.idade = idade;     }     saudacao() {         return `Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`;     } }``

---

## **📌 6. Trabalhando com Listas e Compreensões**

python

CopiarEditar

`numeros = [1, 2, 3, 4, 5] quadrados = [x**2 for x in numeros if x % 2 == 0] print(quadrados)  # [4, 16]`

➡ Em C#: `var quadrados = numeros.Where(x => x % 2 == 0).Select(x => x * x).ToList();`  
➡ Em JS: `let quadrados = numeros.filter(x => x % 2 === 0).map(x => x * x);`

---

## **📌 7. Estruturas de Dados para Problemas de Algoritmos**

### **Pilha (Stack)**

python

CopiarEditar

`pilha = [] pilha.append(1)  # Push pilha.append(2) print(pilha.pop())  # Pop (2)`
``

### **Fila (Queue)**

```
from collections import deque  
fila = deque() 
fila.append(1) 
fila.append(2) 
print(fila.popleft())  
# Remove o primeiro elemento (1)
```

### **Heap (Fila de Prioridade)**

```
c
```

```
import heapq  heap = [] 
heapq.heappush(heap, 3) 
heapq.heappush(heap, 1) 
heapq.heappush(heap, 2)  
print(heapq.heappop(heap)) 
# Retorna 1 (menor elemento) 10
```

