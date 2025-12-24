# 🧹 Processo de Limpeza e Transformação – Python

**Objetivo:** transformar os dados brutos (`Vagas_Coletadas_Raw.xlsx`) em uma versão **limpa, padronizada e reduzida**, pronta para análise, modelagem SQL e dashboards Power BI.

---

## 1️⃣ Padronização de Cargo
- Converte cargos para minúsculas e aplica regras de padronização:
  - "alis" → "Analista de Dados"
  - "enti" → "Cientista de Dados"
- Coluna `Cargo` atualizada com valores padronizados.

## 2️⃣ Extração e Padronização de Estado
- Mapeia a coluna `Localização` para o estado correto.
- Reconhece variações, abreviações e cidades:
  - "SP", "Barueri" → "São Paulo"
  - "RJ", "Rio de Jan" → "Rio de Janeiro"
  - "remoto" ou "remote" → "Remoto"
- Coluna `Estado` atualizada.

## 3️⃣ Tratamento de Skills
- Padroniza a coluna de requisitos (`Obrigatório/Diferencial`):
  - "sim", "básico", "obrigatório" → "Obrigatório"
  - "não", "diferencial" → "Diferencial"
- Agrupa as skills em categorias padronizadas:
  - Exemplos: Python, SQL, Excel Avançado, Power BI, Tableau
  - Skills não mapeadas recebem "Outra Skill"

## 4️⃣ Redução e Reorganização das Colunas
- **Vagas**: mantidas apenas 7 colunas essenciais
  - `ID`, `Empresa`, `Setor`, `Modalidade`, `Senioridade`, `Cargo`, `Estado`
- **Skills**: mantidas 3 colunas essenciais
  - `ID_Vaga`, `Skill`, `Requisito`

## 5️⃣ Exportação e Carga em SQL
- Exporta os dados limpos para Excel (`analise_vagas.xlsx`)
- Carrega automaticamente no banco SQL (`Vagas` e `Skills`) via pyodbc
- Permite consultas analíticas e integração com dashboards Power BI

---

💡 **Resumo:**  
O script transforma os dados brutos em uma **versão limpa, padronizada e reduzida**, mantendo **rastreabilidade com os dados originais**, pronta para análises, modelagem e visualizações.
