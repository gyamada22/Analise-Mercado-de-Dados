# SQL Queries

Este arquivo contém **9 análises principais** feitas com SQL Server, que servem como base para dashboards e insights do projeto:

1. **Volume de vagas por senioridade**  
2. **Top 3 skills obrigatórias por senioridade**  
3. **Top 3 skills diferenciais por senioridade**  
4. **Distribuição de vagas por estado**  
5. **Percentual de vagas por estado**  
6. **Distribuição de vagas por modalidade** (Remoto, Híbrido, Presencial)  
7. **Top 5 setores por quantidade de vagas**  
8. **Top 5 skills obrigatórias por setor** (apenas para os 5 setores com mais vagas)  
9. **Top 5 skills diferenciais por setor** (apenas para os 5 setores com mais vagas)  

## Como usar

- Abrir o arquivo `queries.sql` no SQL Server Management Studio (SSMS)  
- Executar cada bloco de query individualmente  
- Os resultados podem ser exportados para Power BI, facilitando a criação de dashboards.

>  Observação: As queries usam tabelas `Vagas` e `Skills` que foram populadas pelo script `etl.py`.
