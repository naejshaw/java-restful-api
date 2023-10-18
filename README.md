﻿# DIO java-restful-api
 Java RESTful API criada para o Desafio de Projeto DIO.

 ##Diagrama de Classes

 ```mermaid
classDiagram
  class User {
    - name: String
    - account: Account
    - features: Feature[]
    - card: Card
    - news: News[]
  }

  class Account {
    - number: String
    - agency: String
    - balance: Float
    - limit: Float
  }

  class Feature {
    - icon: String
    - description: String
  }

  class Card {
    - number: String
    - limit: Float
  }

  class News {
    - icon: String
    - description: String
  }

  User "1" -- "1" Account : owns
  User "1" -- "many" Feature : has
  User "1" -- "1" Card : has
  User "1" -- "many" News : receives
```
