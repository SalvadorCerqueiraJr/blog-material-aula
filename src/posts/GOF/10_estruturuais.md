---
icon: edit
date: 2024-08-15 18:00:00.00 -3
tag:
  - GOF
category:
  - aula
#navbar: false
order: 10
---

# Padrões de projeto estruturais

[^GAMMA]


Os padrões estruturais se preocupam com a forma como classes e objetos são compostos para formar estruturas maiores. Os padrões estruturais de classes utilizam a herança para compor interfaces ou implementações. Dando um exemplo simples, considere como a herança múltipla mistura duas ou mais classes em uma outra. O resultado é uma classe que combina as propriedades das suas classes ancestrais. Esse padrão é particularmente útil para fazer bibliotecas de classes desenvolvidas independentemente trabalharem juntas. Um outro exemplo é a forma de classe do padrão [Adapter]. Em geral, um Adapter faz com que uma interface adaptada (em inglês, adaptee) seja compatível com outra, dessa forma fornecendo uma abstração uniforme de diferentes interfaces. A classe adaptadora (adapter) atinge esse objetivo herdando, privadamente, de uma classe adaptada. O adapter, então, exprime sua interface em termos da interface da classe adaptada.

Em lugar de compor interfaces ou implementações, os padrões estruturais de objetos descrevem maneiras de compor objetos para obter novas funcionalidades. A flexibilidade obtida pela composição de objetos provém da capacidade de mudar a composição em tempo de execução, o que é impossível com a composição estática de classes.

O [Composite] é um exemplo de um padrão estrutural de objetos. Ele descreve como construir uma hierarquia de classes composta para dois tipos de objetos: primitivos e compostos. Os objetos compostos permitem compor objetos primitivos e outros objetos compostos em estruturas arbitrariamente complexas. No padrão [Proxy], um procurador funciona como um substituto ou um marcador para outro objeto. Um proxy (procurador) pode ser usado de várias formas. Ele pode atuar como um representante local para um objeto situado num espaço de endereço remoto. Pode representar um grande objeto que deveria ser carregado por demanda. Pode proteger o acesso a um objeto sensível. Proxies fornecem um nível de referência indireta a propriedades específicas de objetos. Daí eles poderem restringir, aumentar ou alterar essas propriedades.

O padrão [Flyweight]  define uma estrutura para o compartilhamento de objetos. Os objetos são compartilhados por pelo menos duas razões: eficiência e consistência. O Flyweight focaliza o compartilhamento para uso eficiente de espaço. As aplicações que usam uma porção de objetos devem prestar atenção no custo de cada objeto. Pode-se obter economia substancial e usando o compartilhamento de objetos, em lugar de replicá-los. Mas objetos podem ser compartilhados somente se eles não definem estados dependentes do contexto.

Objetos Flyweight não possuem tais estados. Qualquer informação adicional de que necessitem para executar suas tarefas é passada aos mesmos quando necessário. Não tendo estados dependentes de contexto, os objetos Flyweight podem ser compartilhados livremente.

Enquanto o Flyweight mostra o que fazer com muitos objetos pequenos, [Façade] mostra como fazer um único objeto representar todo um subsistema. Um objeto façade (fachada) é uma representação para um conjunto de objetos. Façade executa suas responsabilidades repassando mensagens para os objetos que ela representa. O padrão [Bridge] separa a abstração de um objeto da sua implementação, de maneira que elas possam variar independentemente.

O [Decorator] descreve como acrescentar dinamicamente responsabilidades ao objetos. O Decorator é um padrão estrutural que compõe objetos recursivamente para permitir um número ilimitado de responsabilidades adicionais. Por exemplo, um objeto Decorator que contém um componente de uma interface de usuário pode adicionar uma decoração, como uma borda ou sombra, ao componente, ou pode adicionar uma funcionalidade como rolamento ou zoom. Podemos adicionar duas decorações simplesmente encaixando um objeto Decorator dentro do outro, e assim por diante, para outras decorações adicionais. Para conseguir isto, cada objeto Decorator deve oferecer a mesma interface do seu componente e repassar mensagens para ele. O Decorator pode executar o seu trabalho (tal como desenhar uma borda em volta do componente) antes ou depois de repassar uma mensagem



- **Adapter** Permitir que um objeto seja substituído por outro que, apesar de realizar a mesma tarefa, possui uma interface diferente.
- **Bridge** Separar uma abstração de sua representação, de forma que ambos possam variar e produzir tipos de objetos diferentes.
- **Composite** Agrupar objetos que fazem parte de uma relação parte-todo de forma a tratá-los sem distinção.
- **Decorator** Adicionar funcionalidade a um objeto dinamicamente.
- **Facade** Prover uma interface simplificada para a utilização de várias interfaces de um subsistema.
- **Front Controller** Centralizar todas as requisições a uma aplicação Web.
- **Flyweight** Compartilhar, de forma eficiente, objetos que são usados em grande quantidade.
- **Proxy** Controlar as chamadas a um objeto através de outro objeto de mesma interface.


## Entrega

[Link](https://classroom.github.com/a/hKgAqwgp)

| Padrão           | Aluno                                                                                  |
| ---------------- | -------------------------------------------------------------------------------------- |
| Adapter          | <ul><li>Árlei Nóbrega Oliveira</li><li>Salvador Cerqueira Júnior</li></ul>             |
| Bridge           | <ul><li>Brenda Gabriela Martinez Araújo </li><li>Yuri Pêpe do Espírito Santo</li></ul> |
| Composite        | <ul><li>Gabriel Ferreira Lima Brito </li></ul>                                         |
| Decorator        | <ul><li>Gabriel Moreira Bispo Santos</li></ul>                                         |
| Facade           | <ul><li>Guilherme Sampaio Oliveira</li></ul>                                           |
| Front Controller | <ul><li>João Augusto Moura Peixoto De Jesus</li><li>Rian Silva da Fonseca</li></ul>    |
| Flyweight        | <ul><li>Luis Miguel De Jesus Oliveira</li></ul>                                        |
| Proxy            | <ul><li>Pedro Carlos de Gois Barros Santos</li></ul>                                   |




## Referências

<!-- @include: ../../includes/bib.md -->