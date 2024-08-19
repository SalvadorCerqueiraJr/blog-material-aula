---
icon: edit
date: 2024-07-25 20:10:00.00 -3
tag:
  - Prototype
  - gof
category:
  - seminario-1
order: 10
excerpt: Apresentação do Padrão de Projeto Prototype
author: GabrielMreira, Redror
---

# Prototype

## Gabriel Moreira Bispo Santos (20221TADSSAJ0020)
[@GabrielMreira](https://github.com/GabrielMreira)

<!-- @include: ../../../includes/seminario-1-GabrielMreira/README.md -->


## Pedro Carlos de Gois Barros Santos (20221TADSSAJ0006)
[@Redror](https://github.com/Redror)

<!-- @include: ../../../includes/seminario-1-Redror/README.md -->
## Salvador

```mermaid
classDiagram
    class  PrototipoInimigo {
        +clone():  PrototipoInimigo
        + getSaude(): int
        +setsaude(saude: int): void
        + getPoderDeAtaque(): int
        +setPoderDeAtaque(PoderDeAtaque: int): void
    }

    class Goblin {
        -saude: int
        -PoderDeAtaque: int
        +clone(): Goblin
        + getSaude(): int
        +setsaude(saude: int): void
        + getPoderDeAtaque(): int
        +setPoderDeAtaque(PoderDeAtaque: int): void
    }

    class Orc {
        -saude: int
        -PoderDeAtaque: int
        +clone(): Orc
        + getSaude(): int
        +setsaude(saude: int): void
        + getPoderDeAtaque(): int
        +setPoderDeAtaque(PoderDeAtaque: int): void
    }

     PrototipoInimigo <|-- Goblin
     PrototipoInimigo <|-- Orc
