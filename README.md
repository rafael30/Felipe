# Felipe
Apresentação Padrão Projeto
De forma geral todos os padrões Factory (Simple Factory, Factory Method, Abstract
Factory) encapsulam a criação de objetos. O padrão Factory Method por sua vez
encapsula a criação de objetos, no entanto, a diferença é que neste padrão encapsula-se a
criação de objetos deixando as subclasses decidirem quais objetos criar.
Vantagens do Padrão Factory Method
O Factory Method é bastante utilizado em diversos projetos, até mesmo nos casos em
que temos apenas um Creator (diagrama acima), pois mesmo nessas condições o padrão
nos oferece um meio de desligar a implementação de um Product. Adicionando ou
alterando Products isso não irá afetar o Creator, pois eles não estão fortemente ligados.
Com o padrão Factory Method podemos encapsular o código que cria objetos. É muito
comum termos classes que instanciam classes concretas e essa parte do código
normalmente sofre diversas modificações, portanto nesses casos usamos um Factory
Method que encapsula esse comportamento de instanciação.
Usando o Factory Method temos o nosso código de criação em um objeto ou método,
evitando assim a duplicação e além disso temos um local único para fazer manutenção.
O padrão também nos dá um código flexível e extensível para o futuro.
Chain of Responsibility
Intenção e Objetivo:
Este padrão tem como função representar um encadeamento de objetos para realizar o
processamento de um série de requisições diferentes.
Aplicabilidade:
Uma solicitação pode ser tratada por mais de um objeto;
A solicitação poderá ser emitida entre vários objetos e o receptor não é necessário ser
especificado explicitamente;
Vantagens
 Evita acoplamento do transmissor de um requisição com seus receptores, fazendo com
que mais de um projeto tenha a chance de manipular a requisição.
 Encadeia os objetos receptores e passa a requisição ao longo dessa cadeia até que um
objeto possa manipulá-lo.
 Reduz a vinculação.
 Adiciona flexibilidade.
 Permite que um conjunto de classes atue como uma classe; eventos produzidos em uma
classe podem ser enviados para outras classes dentro da composição.
State
Em comparação a classe criada sem o padrão, temos uma classe menor e mais simples,
uma vez que a decisão de qual estado ele vai estar depois da chamada dos métodos não
cabe mais a classe contexto e sim a cada classe encapsulada que representa um estado
do mesmo modo que a execução do método que esta sendo delegado ao estado atual.
Devemos observar também que para setamos qualquer estado estamos utilizamos
“MeuEstado = new [EstadoConcreto]([Contexto])” isso ocorre tanto na criação da
classe contexto quanto nas alterações dos estados.
Em ambas implementações com ou sem design pattern o resultado é o mesmo, então
vocês estão se perguntando, por que eu irei ter um trabalho maior para chegar ao mesmo
resultado?
A resposta é simples, no primeiro se você precisar de mais um estado vai ter que alterar
sua classe Conta podendo alterar um bloco de código de forma errada causando
transtornos, uma vez que a classe conta é a classe principal, agora se estiver no padrão
não necessitaremos de alterar nada na classe conta, e sim na classe do estado especifico
da alteração deixando da forma que estava as demais classes dos estado, e se necessário
criar outra classe para estado as alterações serão pequenas.
