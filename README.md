# Padrões de Projeto

Criacionais
Os padrões de projeto criacionais estão relacionados à criação de objetos de forma flexível e eficiente, sem vincular o código a classes específicas. Eles abstraem o processo de instanciação, tornando-o mais independente das classes concretas envolvidas.

Factory Method (Método de Fábrica)
O padrão Factory Method define uma interface para criar um objeto, mas permite às subclasses alterar o tipo de objetos que serão criados. Isso significa que a instanciação é adiada para as subclasses, fornecendo um método para criar objetos em uma hierarquia de classes.

Problema:
Imagine que você esteja desenvolvendo um sistema de logística que lida com diferentes tipos de veículos para entrega, como carros, bicicletas e caminhões. Em sua implementação, você precisa criar objetos desses veículos conforme necessário. No entanto, você não quer que o código dependa diretamente das classes concretas desses veículos, pois isso tornaria difícil estender ou modificar o sistema no futuro.

Solução:
O padrão Factory Method resolve esse problema definindo uma interface para criar um objeto, mas permite que as subclasses decidam quais classes concretas serão instanciadas. Dessa forma, a lógica de criação é abstraída para as subclasses, fornecendo flexibilidade e desacoplamento do código.

Diagrama UML:
![image](https://github.com/salazar2112/padroes-de-projeto/assets/167459656/68879961-4e26-4ba1-b969-5652b6300ab8)

Estruturais
Os padrões de projeto estruturais se preocupam com a composição de classes e objetos para formar estruturas maiores, facilitando a interação entre essas estruturas. Eles ajudam a garantir que as mudanças na estrutura não afetem as partes dependentes do sistema.

Adapter (Adaptador)
O padrão Adapter converte a interface de uma classe em outra interface que o cliente espera encontrar. Ele permite que classes com interfaces incompatíveis trabalhem juntas, facilitando a reutilização de código existente sem modificar sua fonte.

Exemplo: Suponha que tenhamos uma biblioteca de reprodução de áudio que suporte apenas a reprodução de arquivos MP3. Para reproduzir outros formatos, como WAV ou FLAC, podemos usar o padrão Adapter para criar adaptadores que ajustem a interface desses formatos para a interface esperada pela biblioteca de reprodução de áudio.

Comportamentais
Os padrões de projeto comportamentais se concentram nas interações entre objetos, definindo responsabilidades e comunicação entre eles. Eles ajudam a descrever como os objetos colaboram para cumprir tarefas complexas.

Strategy (Estratégia)
O padrão Strategy define uma família de algoritmos, encapsulando cada um deles e tornando-os intercambiáveis. Isso permite que o algoritmo varie independentemente dos clientes que o utilizam, promovendo a flexibilidade e a reutilização de código.

Exemplo: Considere um sistema de processamento de pagamento que oferece diferentes métodos de pagamento, como cartão de crédito, PayPal ou transferência bancária. O padrão Strategy pode ser usado para encapsular cada método de pagamento em uma estratégia separada, permitindo que o cliente selecione dinamicamente o método desejado.

Este README fornece uma visão geral dos padrões de projeto e como eles podem ser aplicados em diferentes contextos de desenvolvimento de software. Ao entender e aplicar esses padrões de forma apropriada, os desenvolvedores podem escrever código mais flexível, modular e fácil de manter.



