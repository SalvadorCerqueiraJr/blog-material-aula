---
icon: edit
date: 2024-07-25 20:10:00.00 -3
tag:
  - 'Abstract Factory'
  - gof
category:
  - seminario-1
order: 10
excerpt: Apresentação do Padrão de Projeto Abstract Factory
author: Brenda-Martinez
---
# Abstract Factory


## Brenda Gabriela Martinez Araújo (20221TADSSAJ0001) 

[@Brenda-Martinez](https://github.com/Brenda-Martinez)

<!-- @include: ../../../includes/seminario-1-Brenda-Martinez/README.md -->





## João Augusto

<figure>
  
```plantuml

@startuml
interface Personagem {
    +descricao(): String
}

interface Equipamento {
    +usar(): void
}

interface RPGFactory {
    +criarPersonagem(): Personagem
    +criarEquipamento(): Equipamento
}

class Cavaleiro implements Personagem {
    +descricao(): String
}

class Espada implements Equipamento {
    +usar(): void
}

class Mago implements Personagem {
    +descricao(): String
}

class Cajado implements Equipamento {
    +usar(): void
}

class CavaleiroFactory implements RPGFactory {
    +criarPersonagem(): Personagem
    +criarEquipamento(): Equipamento
}

class MagoFactory implements RPGFactory {
    +criarPersonagem(): Personagem
    +criarEquipamento(): Equipamento
}

RPGFactory <|-- CavaleiroFactory
RPGFactory <|-- MagoFactory
CavaleiroFactory --> Cavaleiro : cria >
CavaleiroFactory --> Espada : cria >
MagoFactory --> Mago : cria >
MagoFactory --> Cajado : cria >
@enduml

```
</figure>


## Salvador

@startuml
interface Button {
    + render(): void
}

interface TextField {
    + render(): void
}

class WindowsButton implements Button {
    + render(): void
}

class WindowsTextField implements TextField {
    + render(): void
}

class MacButton implements Button {
    + render(): void
}

class MacTextField implements TextField {
    + render(): void
}

interface GUIFactory {
    + createButton(): Button
    + createTextField(): TextField
}

class WindowsFactory implements GUIFactory {
    + createButton(): Button
    + createTextField(): TextField
}

class MacFactory implements GUIFactory {
    + createButton(): Button
    + createTextField(): TextField
}

Button <|-- WindowsButton
Button <|-- MacButton
TextField <|-- WindowsTextField
TextField <|-- MacTextField
GUIFactory <|-- WindowsFactory
GUIFactory <|-- MacFactory
@enduml
