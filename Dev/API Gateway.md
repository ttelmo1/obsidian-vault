#Microsservices 
Um **API Gateway** é um ponto central que gerencia, roteia e protege chamadas de API em um sistema distribuído, como uma arquitetura de **microservices**. Ele atua como um **proxy reverso**, recebendo requisições dos clientes e direcionando para os serviços corretos.

---

## **📌 Principais Problemas que um API Gateway Resolve**

### **1️⃣ Excesso de Chamadas Diretas aos Microservices**

- Sem um API Gateway, um cliente precisa conhecer todos os serviços e fazer múltiplas chamadas.
- O Gateway **unifica e otimiza** essas chamadas, reduzindo latência e carga na rede.  
    📌 **Exemplo:** Em um app de e-commerce, um único request pode buscar **dados do usuário, pedidos e pagamentos** ao mesmo tempo.

---

### **2️⃣ Segurança e Autenticação**

- Protege APIs contra ataques como **DDoS, SQL Injection e Cross-Site Scripting**.
- Pode gerenciar **autenticação e autorização** com JWT, OAuth, API Keys etc.  
    📌 **Exemplo:** O API Gateway pode rejeitar requisições não autenticadas antes que atinjam os microservices.
- Esconde as rotas externas da API

---

### **3️⃣ Balanceamento de Carga**

- Distribui as requisições entre múltiplas instâncias do mesmo serviço, melhorando desempenho e escalabilidade.  
    📌 **Exemplo:** Se um serviço de `pagamento` tem 3 instâncias, o Gateway pode balancear chamadas entre elas.

---

### **4️⃣ Monitoramento e Logging**

- Centraliza logs e métricas de chamadas para facilitar **debug e monitoramento**.  
    📌 **Exemplo:** O Gateway pode registrar tempos de resposta e alertar quando um serviço estiver lento.

---

### **5️⃣ Tradução de Protocolos e Versionamento**

- Converte protocolos (ex: REST ↔ GraphQL ↔ gRPC).
- Permite versionamento de APIs sem quebrar clientes antigos.  
    📌 **Exemplo:** Clientes antigos podem continuar usando **v1**, enquanto novos usam **v2** sem afetar a infraestrutura.