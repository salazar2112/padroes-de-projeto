# Padrões de Projeto

# Criacionais
Os padrões de projeto criacionais estão relacionados à criação de objetos de forma flexível e eficiente, sem vincular o código a classes específicas. Eles abstraem o processo de instanciação, tornando-o mais independente das classes concretas envolvidas.

Factory Method (Método de Fábrica):

O padrão Factory Method define uma interface para criar um objeto, mas permite às subclasses alterar o tipo de objetos que serão criados. Isso significa que a instanciação é adiada para as subclasses, fornecendo um método para criar objetos em uma hierarquia de classes.

Problema:
Imagine que você esteja desenvolvendo um sistema de logística que lida com diferentes tipos de veículos para entrega, como carros, bicicletas e caminhões. Em sua implementação, você precisa criar objetos desses veículos conforme necessário. No entanto, você não quer que o código dependa diretamente das classes concretas desses veículos, pois isso tornaria difícil estender ou modificar o sistema no futuro.

Solução:
O padrão Factory Method resolve esse problema definindo uma interface para criar um objeto, mas permite que as subclasses decidam quais classes concretas serão instanciadas. Dessa forma, a lógica de criação é abstraída para as subclasses, fornecendo flexibilidade e desacoplamento do código.

Diagrama UML:

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/68879961-4e26-4ba1-b969-5652b6300ab8)

imagem retirada do site:https://refactoring.guru/pt-br/design-patterns/factory-method

Código exemplo e explicação(código retirado do: https://refactoring.guru/pt-br/design-patterns/factory-method/python/example):

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/67b7c024-d6bd-41ab-a3f5-aa7b82d6ebfc)

A classe creator é uma classe abstrata que declara o método factory_method(), que deve retornar um objeto de uma classe Product.
Possui um método some_operation() que demonstra como o criador pode usar o objeto Product criado pelo factory_method().
Essa classe é independente das classes concretas de produtos, mantendo o código flexível e extensível.

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/3d186421-4a5a-4af1-9ae5-22a0a2c42ffc)

ConcreteCreator1 e ConcreteCreator2:
São subclasses concretas de Creator que implementam o factory_method() para retornar instâncias de produtos concretos (ConcreteProduct1 e ConcreteProduct2, respectivamente).

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/3c21eda2-f91e-47c4-8397-b24039060216)

Product (Produto):
É uma interface que declara o método operation(), que todos os produtos concretos devem implementar.

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/d6db09b3-eff2-42b4-b1ca-46af8b796644)

ConcreteProduct1 e ConcreteProduct2:
São implementações concretas da interface Product que fornecem diferentes implementações para o método operation().

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/4b66b2f1-65ff-42b8-bf72-b6f248c739ce)

client_code():
É uma função que recebe um objeto Creator e demonstra como o código cliente pode trabalhar com criadores e produtos sem conhecer suas classes concretas.
if __name__ == "__main__"::
É uma maneira de verificar se o script está sendo executado diretamente como um programa e não sendo importado como um módulo.
Aqui, é usado para mostrar como o cliente pode trabalhar com diferentes criadores e produtos.




# Estruturais
Os padrões de projeto estruturais se preocupam com a composição de classes e objetos para formar estruturas maiores, facilitando a interação entre essas estruturas. Eles ajudam a garantir que as mudanças na estrutura não afetem as partes dependentes do sistema.

Adapter (Adaptador)
O padrão Adapter converte a interface de uma classe em outra interface que o cliente espera encontrar. Ele permite que classes com interfaces incompatíveis trabalhem juntas, facilitando a reutilização de código existente sem modificar sua fonte.

Problema:
Imagine que você tenha uma classe existente com uma interface incompatível com a interface que um cliente espera usar. Modificar a classe existente para corresponder à interface desejada pode ser inviável ou indesejável.

Solução:
O padrão Adapter resolve esse problema, permitindo que objetos com interfaces incompatíveis trabalhem juntos. Ele adapta a interface de uma classe existente para outra interface esperada pelo cliente.

Diagrama UML:

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/1eface3b-d162-496c-8850-c9a8f6e658da)

imagem retirada do site:https://refactoring.guru/pt-br/design-patterns/adapter

Código exemplo e explicação(código retirado do: https://refactoring.guru/pt-br/design-patterns/adapter/python/example):

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/f4920e23-bb10-49ae-a339-a6d493cddd77)

Target (Alvo):
Define a interface específica do domínio usada pelo código cliente.
Possui um método request() que define o comportamento padrão do alvo.

Adaptee (Adaptado):
Contém algum comportamento útil, mas sua interface é incompatível com o código cliente existente.
Possui um método specific_request() que representa o comportamento específico do adaptado.

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/93af680e-0e7c-4d7b-91cf-95d24714f007)

Adapter (Adaptador):
Torna a interface do Adaptee compatível com a interface do Target através da herança múltipla.
Implementa o método request() para traduzir e adaptar o comportamento do Adaptee para corresponder ao comportamento esperado pelo código cliente.

client_code():
Suporta todas as classes que seguem a interface Target.
Demonstra como o código cliente pode trabalhar com objetos Target, mas também pode se adaptar para trabalhar com Adaptee usando Adapter.

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/fcf8ce90-e7f1-493f-a1a7-f319c789a772)

if __name__ == "__main__"::
Verifica se o script está sendo executado diretamente como um programa.
No bloco, o cliente demonstra como ele pode trabalhar com objetos Target, Adaptee e Adapter.


# Comportamentais
Os padrões de projeto comportamentais se concentram nas interações entre objetos, definindo responsabilidades e comunicação entre eles. Eles ajudam a descrever como os objetos colaboram para cumprir tarefas complexas.

Strategy (Estratégia)
O padrão Strategy define uma família de algoritmos, encapsulando cada um deles e tornando-os intercambiáveis. Isso permite que o algoritmo varie independentemente dos clientes que o utilizam, promovendo a flexibilidade e a reutilização de código.

Problema:
Você precisa implementar diferentes algoritmos para executar uma tarefa específica e deseja permitir que esses algoritmos variem independentemente do cliente que os utiliza.

Solução:
O padrão Strategy resolve esse problema definindo uma família de algoritmos, encapsulando cada um deles e tornando-os intercambiáveis. Isso permite que o cliente selecione dinamicamente o algoritmo desejado.

Diagrama UML:

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/a5fc6853-34c7-4dfc-927e-eb6d732a97fb)

imagem retirada do site:https://refactoring.guru/pt-br/design-patterns/strategy

Código exemplo e explicação(código retirado do: https://refactoring.guru/pt-br/design-patterns/adapter/python/example):

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/0be2032e-0760-4820-b5d1-35427e3afb63)

Context (Contexto):
Define a interface de interesse para os clientes, mantém uma referência a um objeto Strategy e delega parte do trabalho para esse objeto e pode alterar a estratégia em tempo de execução.

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/7e363888-f386-4370-841c-ea8fe9904664)

Strategy (Estratégia):
Define uma interface comum para todas as versões suportadas de algum algoritmo e é utilizada pelo Context para chamar o algoritmo definido pelas Concrete Strategies.

ConcreteStrategyA e ConcreteStrategyB:
Implementam o algoritmo seguindo a interface base Strategy e são intercambiáveis no Context.

![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/93d83459-39b0-42a0-b748-a50f2de9845b)

if __name__ == "__main__":
O código demonstra como usar o padrão Strategy. Ele instancia um objeto Context, define uma estratégia inicial, executa a lógica de negócios e, em seguida, altera a estratégia e executa a lógica de negócios novamente para demonstrar a flexibilidade de trocar estratégias em tempo de execução.






 
