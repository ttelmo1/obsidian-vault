#Microsservices 
### **Event Driven Architecture - Principais Conceitos**

1. **Eventos**: Representam mudanças de estado ou ocorrências no sistema (exemplo: um pedido foi feito, um pagamento foi aprovado).
2. **Produtores**: Geram e publicam eventos sem precisar saber quem os consome.
3. **Consumidores**: Assinam e reagem aos eventos de acordo com sua lógica de negócios.
4. **Event Brokers (Mensageria)**: Sistemas como Kafka, RabbitMQ e AWS EventBridge atuam como intermediários para distribuir eventos de forma assíncrona.

## **Resumo Visual do Fluxo**
[[Req em um Microsserviço]]
📌 **Usuário finaliza a compra** →  (Captura/Produção do evento)
📌 **Evento "PedidoCriado" é publicado** →  (Comunicação)
📌 **Event Broker transmite para os serviços** →  
📌 **Serviços processam o evento (Pagamento, estoque, notificação)** →  (Consumo)
📌 **Os dados são persistidos no banco de dados** (Persistência do estado)
📌 **Websocket envia automaticamente uma atualização para o frontend**

## **Desafios**
1. Timeout das requisições
2. Integrações com diferentes APIs e equipes

### **Exchange e Routing Key no RabbitMQ**

No **RabbitMQ**, mensagens não são enviadas diretamente para as filas (**queues**), mas sim para um intermediário chamado **Exchange**, que determina para onde a mensagem será roteada. A **Routing Key** é um identificador usado para direcionar mensagens dentro do RabbitMQ, funcionando em conjunto com o tipo de Exchange configurado.

---

## **📌 Conceitos Principais**

### **1️⃣ Exchange (Trocador de Mensagens)**

- Atua como um **roteador** de mensagens para as filas.
- Não armazena mensagens, apenas as encaminha.
- Pode ser configurado em diferentes **tipos** de roteamento.

### **2️⃣ Routing Key (Chave de Roteamento)**

- Uma **string** usada para definir para quais filas a mensagem será enviada.
- É comparada com regras definidas no **Binding** entre Exchanges e Filas.
- Funciona de forma diferente dependendo do tipo de Exchange.

## **📌 Exemplo Prático com Direct Exchange**

### **1️⃣ Configuração**

Temos uma **exchange** chamada `"PedidosExchange"` e duas filas vinculadas:

|Fila|Routing Key|
|---|---|
|`fila_pagamento`|`pagamento`|
|`fila_entrega`|`entrega`|

### **2️⃣ Envio de Mensagem**

Se um produtor enviar uma mensagem com:

`{   "pedidoId": "12345",   "status": "Aguardando Pagamento" }`

E definir a **Routing Key = `"pagamento"`**, o RabbitMQ encaminhará a mensagem **apenas para `fila_pagamento`**.


## **📌 Exemplo com Topic Exchange**

### **1️⃣ Configuração**

Temos uma **exchange** chamada `"LogsExchange"` e duas filas vinculadas:

|Fila|Routing Key (Padrão)|
|---|---|
|`fila_erros`|`log.error`|
|`fila_todos_logs`|`log.#`|

### **2️⃣ Envio de Mensagem**

Se um produtor enviar uma mensagem com **Routing Key = `"log.error.db"`**, ela será roteada para `fila_todos_logs` (pois usa `log.#` que aceita múltiplos termos) e **não** será entregue à `fila_erros` (pois não corresponde exatamente a `"log.error"`).