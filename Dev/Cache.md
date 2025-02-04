#Microsservices 
### **📌 O que é Cache e Cache Distribuído?**

**Cache** é um mecanismo que armazena dados temporariamente para **acelerar o acesso** a informações frequentemente usadas. Em vez de buscar os dados diretamente em um banco de dados ou API (operações mais lentas), o cache os mantém na memória, reduzindo latência e carga no sistema.

✅ **Mais rápido que acessar o banco de dados**  
✅ **Reduz custo computacional**  
✅ **Melhora a escalabilidade**

---

## **📌 Tipos de Cache**

### **1️⃣ Cache em Memória (Local)**

- Armazena os dados **dentro da aplicação**.
- Rápido, mas **não compartilhado** entre múltiplos servidores.  
📌 **Exemplo:**
- Um serviço armazena usuários recentes em um **dicionário** no próprio servidor.

**Tecnologias:** `MemoryCache (C#)`, `Node.js LRU-Cache`

---

### **2️⃣ Cache Distribuído**

- Compartilhado entre **múltiplas instâncias** da aplicação.
- Evita inconsistências e duplicação de cache entre servidores.
- Escala melhor, ideal para **microservices e cloud**.

📌 **Exemplo:**

- Um **e-commerce** armazena os produtos mais acessados no **Redis**, para que qualquer instância do serviço possa acessar rapidamente.

**Principais Tecnologias:**

- **Redis** → Cache em memória, rápido e eficiente
- **Memcached** → Alternativa leve para caching simples
- **Apache Ignite** → Cache distribuído para alta performance

---

## **📌 Estratégias de Expiração do Cache**

1️⃣ **TTL (Time-To-Live)** → Define um tempo para os dados expirarem.  
2️⃣ **LRU (Least Recently Used)** → Remove itens menos usados quando a memória enche.  
3️⃣ **Write-Through** → Atualiza cache e banco de dados ao mesmo tempo.  
4️⃣ **Cache-Aside (Lazy Loading)** → Consulta o cache antes de ir ao banco de dados.