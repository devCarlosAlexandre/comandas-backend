# comandas-backend

``` mermaid
erDiagram
    CLIENTE ||--o{ COMANDA : "Realiza"
    COMANDA ||--|{ ITEM_COMANDA : "Contém"
    ITEM_MENU ||--o{ ITEM_COMANDA : "Aparece em"
    CAIXA ||--o{ TRANSACAO_CAIXA : "Registra"
    COMANDA ||--o{ TRANSACAO_CAIXA : "Pagamento"

    CLIENTE {
        INT id
        VARCHAR  nome
        VARCHAR  sobrenome
        VARCHAR  telefone
        VARCHAR  email
    }
    
    COMANDA {
        INT id
        INT id_cliente 
        DATE data_comanda
        DECIMAL valor_total
        ENUM status
    }
    
    ITEM_COMANDA {
        INT id
        INT id_comanda
        INT id_item_menu 
        INT quantidade
        DECIMAL subtotal
    }
    
    ITEM_MENU {
        INT id
        VARCHAR nome
        VARCHAR descricao
        DECIMAL preco
    }

     CAIXA {
        INT id
        TIMESTAMP hora_abertura
        TIMESTAMP hora_fechamento
        TIMESTAMP valor_inicial
        DECIMAL valor_fechamento
        ENUM status
    }
    
    TRANSACAO_CAIXA {
        INT id 
        INT id_caixa
        TIMESTAMP hora_transacao
        TIMESTAMP tipo_transacao
        DECIMAL valor
    }
    
  

```
