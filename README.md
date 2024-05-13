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


