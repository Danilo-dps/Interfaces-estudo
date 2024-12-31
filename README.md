# Interfaces

## Car Rental

- Nesse primeiro exemplo de estudo, temos a necessidade de calcular um imposto. Como esse imposto segue regras de acordo com o seu país, os números estão sujeitos a mudanças.
- Para evitar a manipulação em várias partes do código, usamos as interfaces.
- Uma interface permite a definição genérica do que uma classe que a implementa deve ter, mas a interface não se responsabiliza por efetuar a operação. Quem faz a operação é a classe que implementa essa interface.
- Isso cria um baixo acoplamento, pois qualquer classe que implemente essa interface pode ser usada de forma intercambiável, proporcionando flexibilidade ao código.
- A injeção de dependência ocorre quando a instância da classe que implementa essa interface é fornecida a outra classe, geralmente através de um construtor ou de um método set.
- No exemplo do Car Rental, temos a ``Interface TaxService``, que define um método para o cálculo do imposto. Temos também a ``classe RentalService``, que utiliza essa interface para solicitar o cálculo, e a ``classe BrazilTaxService``, que implementa a ``Interface TaxService`` fornecendo a lógica específica para calcular o valor do imposto no Brasil.
- **Interface TaxService:** Define o que será pedido por quem a implementar.
- **Classe BrazilTaxService:** Implementa a **Interface TaxService** e faz a operação de calcular o valor do imposto.
- **Classe RentalService:** Solicita o cálculo do imposto, sem precisar conhecer a implementação da ``classe BrazilTaxService``.

## Installment Service

- Nesse segundo exemplo de estudo, precisamos calcular o valor de cada parcela, baseado na quantidade de parcelas em que o total será dividido.
- Usando da ``interface Online PaymentService`` para definir quais operações a classe que irá implementar deve ter.
- A ``classe PaypalService`` implementa a ``interface Online PaymentService`` para calcular o valor do juros
- A ``classe ContractService`` utiliza a ``interface Online PaymentService`` que faz o uso da ``classe PaypalService``
- A injeção de dependência ocorre quando a instância da classe que implementa essa interface é fornecida a outra classe, geralmente através de um construtor ou de um método set, nesse exemplo está ocorrendo atraves do construtor.

## Shape

- Nesse terceiro exemplo, é feito o uso de interface e classe abstrata, para mostrar que é possivel fazer uma interface, que será implementada por uma classe abstrata, por ser abstrata, isso permite que ela não precise implementar os contratos que a interface obrigaria uma classe comum implementar 
- A ``interface Shape`` é implementada pela ``classe abstrata AbstractShape``, o fato de ser abstrata permite que somente as classes que a herdam implemente os métodos 

## Device

- Nesse quarto exemplo, é mostrado com é feito a implementação de mais de uma interface por outra classe, mostrando que é possível uma classe implementar mais do que uma interface