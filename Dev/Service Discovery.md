**Service Discovery** é um padrão usado em arquiteturas distribuídas para permitir que **serviços encontrem automaticamente outros serviços** na rede sem a necessidade de configuração manual.

---

## **📌 Por que é Importante?**

Em ambientes como **microservices** ou **Kubernetes**, os serviços são dinâmicos — eles podem escalar, falhar ou mudar de endereço IP frequentemente. O **Service Discovery** facilita a comunicação entre esses serviços sem depender de **endereços estáticos**.

---

## **📌 Como Funciona?**

### **1️⃣ Registro de Serviço**

Cada serviço se **registra** em um **Service Registry** (registro central), como **Consul**, **Eureka** (Spring Cloud), ou **Etcd**.  
**Exemplo:** O serviço `Pagamento` registra-se com o nome **"servico-pagamento"** e endereço IP.

### **2️⃣ Descoberta de Serviço**
[[EDA]]
Quando o serviço `Pedido` precisa chamar `Pagamento`, ele consulta o **Service Registry** para obter o IP atualizado.

### **3️⃣ Monitoramento de Saúde**

O Service Discovery pode verificar **periodicamente a saúde** dos serviços e **remover** aqueles que estão offline.

---

## **📌 Exemplos Práticos**

### **Exemplo 1: Microservices com Consul**
#Microsservices 

1. **Serviço de Pedidos** se registra no Consul como **"servico-pedido"**.
2. **Serviço de Pagamento** consulta o Consul para encontrar **"servico-pedido"** e obter o IP atual.

### **Exemplo 2: Kubernetes**
#DevOps 

- **Kubernetes DNS** age como um Service Discovery interno.
- Um `Pod` chamado **"api-usuarios"** pode ser acessado por outros `Pods` via **"http://api-usuarios"**.

---

## **📌 Benefícios**

✅ **Automatiza a Conexão** → Sem necessidade de endereços IP fixos.  
✅ **Aumenta a Resiliência** → Evita falhas por mudanças de IP ou escalonamento.  
✅ **Facilita o Escalonamento** → Serviços podem subir ou descer sem reconfiguração manual.