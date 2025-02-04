#DDD #OOP
### **Resumo sobre Value Objects**

###### Value Objects (VOs) são um dos principais conceitos do _Domain-Driven Design_ (DDD) e representam um modelo de objetos que encapsulam atributos, mas não possuem identidade própria. Diferente das **_Entities_, que são identificadas por um identificador único**, os VOs são caracterizados apenas pelos seus valores.

### **Principais Características dos Value Objects:**

- **Imutabilidade**: Uma vez criado, um VO não pode ser modificado. Se necessário, um novo objeto deve ser instanciado.
- **Igualdade por Valor**: Dois Value Objects são considerados iguais se todos os seus atributos forem iguais, independentemente de estarem em instâncias diferentes.
- **Sem Identidade Própria**: Eles não possuem um identificador único, pois sua relevância está no conjunto de valores que carregam.
- **Autocontidos e Coesos**: Devem representar um conceito do domínio de forma clara e coesa, agrupando atributos relacionados.

### **Exemplos de Value Objects**

- **Dinheiro** (`Money`): Contém um valor numérico e uma moeda (`currency`), como `R$ 100,00 BRL`.
- **Endereço** (`Address`): Conjunto de atributos como rua, cidade, estado e CEP.
- **CPF**: Um valor que representa um documento, sendo único, mas sem identidade própria.

### **Vantagens do Uso de Value Objects**

✅ **Código mais limpo e expressivo**  
✅ **Redução de inconsistências no domínio**  
✅ **Facilidade de teste e manutenção**  
✅ **Melhora a modelagem do domínio**