# ETL — Extração, Transformação e Carga de Dados

O script `etl.py` é responsável por **limpar, padronizar e carregar os dados de vagas coletadas** no projeto. Ele abrange desde a padronização de cargos e skills até a atualização do banco SQL Server.

---

## Funcionalidades

1. **Padronização de Dados**
   - Cargos (ex: “analista” → “Analista de Dados”, “cientista” → “Cientista de Dados”)
   - Estados (normalização de siglas e nomes completos, detecta vagas remotas)
   - Skills e requisitos (mapa completo de skills para categorias padrão: Python, SQL, Power BI, Cloud, etc.)
   - Valores obrigatórios ou diferenciais (padronização de "sim", "obrigatório", "não", "diferencial")

2. **Tratamento de Duplicatas**
   - Remove duplicatas no dataframe de skills, mantendo apenas a primeira ocorrência por vaga.

3. **Geração de Arquivo Processado**
   - Cria `Vagas_Coletadas_Cleaned.xlsx` com duas abas: `Vagas` e `Skills`.

4. **Carrega no Banco SQL Server**
   - Conecta ao banco `projeto_vagas` via ODBC
   - Atualiza as tabelas `Vagas` e `Skills` apagando dados antigos e inserindo os novos.

---

## Estrutura do Código

- **Funções principais**
  - `padronizar_cargo(cargo)` → normaliza cargos
  - `padronizar_estado(local)` → normaliza estados e detecta remoto
  - `padronizar_requisito(valor)` → converte valores para "Obrigatório", "Diferencial" ou "Não informado"
  - `padronizar_skill(skill)` → mapeia skills para categorias padronizadas
  - `conectar_banco()` → conecta ao SQL Server
  - `importar_dados(conn, df_vagas, df_skills)` → insere dados limpos no banco

- **Fluxo**
  1. Leitura do Excel bruto (`Vagas_Coletadas_Raw.xlsx`)
  2. Aplicação das funções de padronização
  3. Remoção de duplicatas
  4. Exportação do Excel processado (`Vagas_Coletadas_Cleaned.xlsx`)
  5. Inserção no banco SQL Server

---

## Configuração

Edite o dicionário `CONFIG` para definir caminhos de arquivos e nomes de tabelas:

```python
CONFIG = {
    'server': 'localhost\\SQLEXPRESS',
    'database': 'projeto_vagas',
    'table_vagas': 'Vagas',
    'table_skills': 'Skills',
    'excel_origem': r'C:\MeusProjetos\projeto_vagas\Dados\Vagas_Coletadas_Raw.xlsx',
    'excel_processado': r'C:\MeusProjetos\projeto_vagas\Dados\Vagas_Coletadas_Cleaned.xlsx'
}
