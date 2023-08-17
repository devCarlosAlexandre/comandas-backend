# comandas-backend

``` mermaid
erDiagram
    CLIENTE {
        IDCliente (PK)
        Nome
        Sobrenome
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
    
    CLIENTE ||--o{ COMANDA : Realiza
    COMANDA ||--|{ ITEM_COMANDA : Contém
    ITEM_MENU ||--o{ ITEM_COMANDA : Aparece em

```
