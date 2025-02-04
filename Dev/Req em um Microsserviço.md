#DDD #Microsservices
### **Resumo do Caminho de uma Requisição em um Microsserviço**

Quando um cliente faz uma requisição para um microsserviço, ela percorre diversos componentes antes de ser processada e retornar uma resposta. O fluxo típico é:

1️⃣ **Cliente (Frontend ou API Consumer)**

- Um navegador, app móvel ou outro serviço envia a requisição HTTP/HTTPS.

2️⃣ **[[API Gateway]] (Opcional, mas comum)**

- Atua como um ponto central de entrada.
- Faz roteamento, autenticação, logging e balanceamento de carga.

3️⃣ **[[Service Discovery]] (Opcional, usado em arquiteturas dinâmicas)**

- Identifica qual instância do microsserviço está disponível para atender à requisição.

4️⃣ **Microsserviço de Destino**

- Processa a requisição conforme a lógica de negócio.
- Pode validar dados, executar regras ou chamar outros microsserviços.

5️⃣ **Banco de Dados ou [[Cache]]**

- Se necessário, o microsserviço consulta ou altera dados em um banco SQL/NoSQL ou um cache (Redis, Memcached).

6️⃣ **Resposta ao Cliente**

- O microsserviço retorna os dados processados para o cliente via API Gateway ou diretamente.

### **Exemplo Prático** (E-commerce 🛒)

📌 **Usuário solicita detalhes de um produto**

1. O cliente envia um `GET /produto/123` para o API Gateway.
2. O API Gateway encaminha a requisição ao microsserviço de catálogo.
3. O microsserviço busca o produto no banco de dados.
4. A resposta é enviada de volta ao cliente.

Esse fluxo pode incluir **mensageria assíncrona (Kafka, RabbitMQ)** quando há comunicação entre microsserviços sem bloqueio. 🚀