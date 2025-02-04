#Microsservices 
### **O Problema: Dual-Write em [[EDA]]**

Em sistemas baseados em eventos, um serviço pode precisar:  
1️⃣ **Persistir uma mudança no banco de dados** (ex: um novo pedido).  
2️⃣ **Publicar um evento no message broker** (ex: "PedidoCriado" no Kafka).

Se essas operações forem feitas separadamente, podem ocorrer problemas como:  
❌ O banco de dados é atualizado, mas a mensagem não é enviada devido a falha.  
❌ A mensagem é publicada, mas o banco de dados não foi atualizado.

### **📌 Como o Padrão Outbox Resolve Esse Problema?**

O **padrão Outbox** armazena os eventos em uma **tabela dentro do banco de dados** antes de publicá-los. O fluxo é:

1️⃣ **Transação Única:**

- O serviço grava a mudança principal (ex: novo pedido).
- O serviço grava o evento em uma tabela chamada **Outbox** (dentro da mesma transação).

2️⃣ **Publicação Assíncrona:**

- Um **processo separado (Event Publisher)(Worker)** lê periodicamente a tabela **Outbox** e publica os eventos no **message broker**.
- Após a publicação bem-sucedida, os eventos são marcados como processados ou removidos.

### **📌 Considerações**

🔹 O padrão Outbox **aumenta a latência** (pois há um processamento extra antes da publicação).  
🔹 Pode ser combinado com **CDC (Change Data Capture)** para evitar polling constante no banco de dados.