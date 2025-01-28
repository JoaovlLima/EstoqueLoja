# EstoqueLoja

```mermaid
erDiagram

  Produto {
    int id
    string nome
    float preco
    int quantidade
  }

  Categoria {
    int id
    string nome
  }

  Venda {
    int id
    datetime data_hora
    float total
  }

  ItemVenda {
    int id
    int quantidade
    float preco_unitario
    float preco_total
  }

  Usuario {
    int id
    string nome
    string email
    string senha
  }

  Pagamento {
    int id
    string tipo
    float valor
    datetime data_hora
  }

  Produto ||--o{ Categoria : "pertence a"
  Produto ||--o{ ItemVenda : "contido em"
  Venda ||--o{ ItemVenda : "contém"
  Venda ||--o{ Pagamento : "relacionado a"
  Venda ||--o| Usuario : "realizada por"
```
