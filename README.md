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
- Aqui é feito o uso de herança e interface, para mostrar as duas em uso simultâneo

# Herança VS. Interface

## Aspectos em Comum entre Herança e Interfaces

- **Relação é-um:** É quando a classe que herda uma classe ou implementa uma interface, passa a ser um tipo correspondente a essa classe ou interface, respectivamente.
- **Generalização/especialização:** A generalização identifica características comuns e as agrupa em uma superclasse ou interface. A especialização define comportamentos específicos para as subclasses que herdam ou implementam a interface.
- **Polimorfismo:** É a capacidade de tratar objetos de diferentes classes de maneira uniforme, permitindo que o comportamento de métodos seja diferente conforme a classe específica do objeto em uso.

## Diferença Fundamental

- **Herança (reuso):** Permite reutilizar código existente. Subclasses herdam atributos e métodos da superclasse, e podem adicionar ou modificar comportamento.

- **Interface (contrato a ser cumprido):** Define um conjunto de métodos que uma classe deve implementar, garantindo que certas funcionalidades estarão presentes sem ditar como devem ser implementadas.
