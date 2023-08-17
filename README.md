# comandas-backend

``` mermaid
erDiagram
    CLIENTE {
        INT id
        Nome
        Sobrenome
        Telefone
        Email
    }
    
    COMANDA {
        INT id
        IDCliente (FK)
        DataComanda
        ValorTotal
        Status
    }
    
    ITEM_COMANDA {
        INT id
        IDComanda (FK)
        IDItemMenu (FK)
        Quantidade
        Subtotal
    }
    
    ITEM_MENU {
        INT id
        Nome
        Descricao
        Preco
    }
    
    CLIENTE ||--o{ COMANDA : Realiza
    COMANDA ||--|{ ITEM_COMANDA : Contém
    ITEM_MENU ||--o{ ITEM_COMANDA : Aparece em

```
