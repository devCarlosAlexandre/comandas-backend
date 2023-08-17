# comandas-backend
## Diagrama

``` mermaid
erDiagram
  CLIENTE ||--o{ COMANDA : Realiza
    COMANDA ||--|{ ITEM_COMANDA : Contem
    ITEM_MENU ||--o{ ITEM_COMANDA : Pertence a

    CLIENTE {
        IDCliente (PK)
        PrimeiroNome
        UltimoNome
        Telefone
        Email
    }
    
    COMANDA {
        IDComanda (PK)
        IDCliente (FK)
        DataComanda
        ValorTotal
        Status
    }
    
    ITEM_COMANDA {
        IDItemComanda (PK)
        IDComanda (FK)
        IDItemMenu (FK)
        Quantidade
        Subtotal
    }
    
    ITEM_MENU {
        IDItemMenu (PK)
        Nome
        Descricao
        Preco
    }
    
  

```
