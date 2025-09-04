# 🏥 Banco de Dados Hospital - Exercício

Este projeto contém um banco de dados **SQLite** (`hospital.db`) com a tabela `pacientes`. O objetivo é que você pratique consultas **SQL SELECT** e compare seus resultados com as tabelas esperadas.

---

## 📊 Estrutura da Tabela `pacientes`

| Coluna              | Tipo    | Descrição                       |
| ------------------- | ------- | ------------------------------- |
| id                  | INTEGER | Identificador único (PK)        |
| nome                | TEXT    | Nome do paciente                |
| idade               | INTEGER | Idade do paciente               |
| sexo                | TEXT    | Sexo (M/F)                      |
| cidade              | TEXT    | Cidade de origem                |
| telefone            | TEXT    | Telefone de contato             |
| plano\_saude        | TEXT    | Nome do plano de saúde          |
| diagnostico         | TEXT    | Diagnóstico médico              |
| data\_internacao    | TEXT    | Data da internação (YYYY-MM-DD) |
| medico\_responsavel | TEXT    | Médico responsável              |
| quarto              | INTEGER | Número do quarto                |

---

## 🧑‍⚕️ Dados Inseridos

| id | nome           | idade | sexo | cidade         | telefone    | plano\_saude | diagnostico | data\_internacao | medico\_responsavel | quarto |
| -- | -------------- | ----- | ---- | -------------- | ----------- | ------------ | ----------- | ---------------- | ------------------- | ------ |
| 1  | Ana Souza      | 32    | F    | São Paulo      | 11987654321 | Unimed       | Gripe       | 2025-08-10       | Dr. Carlos          | 101    |
| 2  | Bruno Lima     | 45    | M    | Rio de Janeiro | 21912345678 | Amil         | Fratura     | 2025-08-15       | Dra. Fernanda       | 102    |
| 3  | Carla Mendes   | 29    | F    | Belo Horizonte | 31998765432 | Bradesco     | Apendicite  | 2025-08-20       | Dr. João            | 103    |
| 4  | Diego Martins  | 53    | M    | São Paulo      | 11933334444 | Unimed       | Covid-19    | 2025-08-18       | Dra. Ana            | 104    |
| 5  | Eduarda Silva  | 40    | F    | Curitiba       | 41922223333 | SulAmérica   | Hipertensão | 2025-08-22       | Dr. Paulo           | 105    |
| 6  | Felipe Costa   | 36    | M    | Porto Alegre   | 51911112222 | Unimed       | Diabetes    | 2025-08-25       | Dra. Maria          | 106    |
| 7  | Gabriela Rocha | 27    | F    | São Paulo      | 11955556666 | Amil         | Asma        | 2025-08-28       | Dr. Roberto         | 107    |
| 8  | Henrique Alves | 60    | M    | Rio de Janeiro | 21944445555 | Bradesco     | Infarto     | 2025-08-12       | Dra. Camila         | 108    |
| 9  | Isabela Torres | 34    | F    | Belo Horizonte | 31966667777 | Unimed       | Fratura     | 2025-08-14       | Dr. Carlos          | 109    |
| 10 | João Pedro     | 48    | M    | Curitiba       | 41988889999 | SulAmérica   | Covid-19    | 2025-08-17       | Dr. João            | 110    |

---

## 📘 Exercícios (Consultas SQL)

### 1) Selecionar todos os pacientes da cidade de **São Paulo**.

```sql
SELECT | WHERE | FROM ;
```

**Resultado esperado:**

| nome           | cidade    |
| -------------- | --------- |
| Ana Souza      | São Paulo |
| Diego Martins  | São Paulo |
| Gabriela Rocha | São Paulo |

---

### 2) Listar o **nome e diagnóstico** dos pacientes com idade **acima de 40 anos**.

```sql
FROM | WHERE | SELECT
```

**Resultado esperado:**

| nome           | diagnostico |
| -------------- | ----------- |
| Bruno Lima     | Fratura     |
| Diego Martins  | Covid-19    |
| Eduarda Silva  | Hipertensão |
| Henrique Alves | Infarto     |
| João Pedro     | Covid-19    |

---

### 3) Mostrar o **nome e plano de saúde** dos pacientes atendidos pelo plano **Unimed**.

```sql
SELECT | FROM | WHERE 
```

**Resultado esperado:**

| nome           | plano\_saude |
| -------------- | ------------ |
| Ana Souza      | Unimed       |
| Diego Martins  | Unimed       |
| Felipe Costa   | Unimed       |
| Isabela Torres | Unimed       |

---

### 4) Selecionar os pacientes ordenados pela **data de internação (mais antiga primeiro)**.

```sql
SELECT | FROM | ORDER BY | ASC
```

**Resultado esperado:**

| nome           | data\_internacao |
| -------------- | ---------------- |
| Ana Souza      | 2025-08-10       |
| Henrique Alves | 2025-08-12       |
| Isabela Torres | 2025-08-14       |
| Bruno Lima     | 2025-08-15       |
| João Pedro     | 2025-08-17       |
| Diego Martins  | 2025-08-18       |
| Carla Mendes   | 2025-08-20       |
| Eduarda Silva  | 2025-08-22       |
| Felipe Costa   | 2025-08-25       |
| Gabriela Rocha | 2025-08-28       |

---

### 5) Mostrar apenas os pacientes que tiveram **diagnóstico de Fratura**.

```sql
WHERE| SELECT | FROM  
```

**Resultado esperado:**

| nome           | diagnostico |
| -------------- | ----------- |
| Bruno Lima     | Fratura     |
| Isabela Torres | Fratura     |

---

### 6) Selecionar os pacientes que foram atendidos pelo **Dr. João**.

```sql
SELECT | WHERE | FROM
```

**Resultado esperado:**

| nome         | medico\_responsavel |
| ------------ | ------------------- |
| Carla Mendes | Dr. João            |
| João Pedro   | Dr. João            |

---

## 📌 Observação Final

👉 Estes exercícios usam apenas **consultas básicas (`SELECT`, `WHERE`, `ORDER BY`)**.
Nos próximos exercícios veremos **`COUNT`, `AVG`, `JOIN` e funções de agregação**, para análises mais avançadas. 🚀
