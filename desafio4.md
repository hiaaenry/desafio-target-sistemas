# Desafio 4

## Tabelas do Banco de Dados

### Client

| Field        | Type       |
| ------------ | ---------- |
| client_id    | PK         |
| company_name | VARCHAR    |
| state_id     | FK (State) |

### Phone

| Field     | Type           |
| --------- | -------------- |
| phone_id  | PK             |
| number    | VARCHAR        |
| type_id   | FK (PhoneType) |
| client_id | FK (Client)    |

### PhoneType

| Field         | Type    |
| ------------- | ------- |
| phone_type_id | PK      |
| description   | VARCHAR |

### State

| Field        | Type    |
| ------------ | ------- |
| state_id     | PK      |
| abbreviation | VARCHAR |

### Relacionamentos:

- **Cada** cliente pode ter **vários** telefones (relacionamento 1
  entre Cliente e Telefone).
- **Cada** telefone tem **um** tipo (relacionamento 1
  entre TipoTelefone e Telefone).
- **Cada** cliente pertence a **um** estado (relacionamento 1
  entre Estado e Cliente).

### Consulta SQL

```sql
SELECT c.id_cliente, c.razao_social, t.numero
FROM Cliente c
JOIN Telefone t ON c.id_cliente = t.id_cliente
JOIN Estado e ON c.estado = e.id_estado
WHERE e.sigla = 'SP';
```
