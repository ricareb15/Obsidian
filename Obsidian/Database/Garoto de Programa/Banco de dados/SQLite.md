SQLite é um mecanismo de banco de dados. É um software que permite aos usuários interagir com um [banco de dados relacional](https://www.codecademy.com/resources/docs/general/database/relational-database) . 

No SQLite, <mark style="background: #FF5582A6;">um banco de dados é armazenado em um único arquivo</mark> — uma característica que o distingue de outros mecanismos de banco de dados. Isso permite um alto grau de acessibilidade: copiar um banco de dados não é mais complicado do que copiar o arquivo que armazena os dados; compartilhar um banco de dados pode significar enviar um anexo de e-mail.

O SQLite é usado mundialmente para testes, desenvolvimento e em qualquer outro cenário em que faça sentido que o banco de dados esteja no mesmo disco que o código do aplicativo.

## Funções

### strftime
A `strftime()` <mark style="background: #FFF3A3A6;">serve para formatar valores de data e hora</mark> com base em um padrão definido. Ela é inspirada na função homônima da linguagem C e permite extrair partes específicas de uma data, como ano, mês, dia, hora, etc.

```ad-summary
title: Sintaxe
collapse: closed

`strftime`(**format_string**, **time_string** [, **modificadores**...])
- `format_string`: define o formato de saída (ex: `'%Y` - `%m` - `%d'` para "2025-07-01")
- `time_string`: a data/hora de entrada (ex: `'now'`, `'2025-01-01 12:00:00'`)
- `modificadores`: opcionais, usados para ajustar o valor da data/hora

Exemplo prático:
```sql
-- Retorna o ano atual
SELECT strftime('%Y', 'now');

-- Extrai o mês de uma data específica
SELECT strftime('%m', '2025-07-01');

-- Retorna o timestamp atual em segundos desde 1970
SELECT strftime('%s', 'now');
```
- `%Y`retorna o ano (AAAA)
- `%m`retorna o mês (01-12)
- `%d`retorna o dia do mês (1-31)
- `%H`retorna o relógio de 24 horas (00-23)
- `%M`retorna o minuto (00-59)
- `%S`retorna os segundos (00-59)