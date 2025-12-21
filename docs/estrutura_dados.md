# Estrutura de Dados para Extração de Vagas do LinkedIn

Este documento descreve a **estrutura de abas do Excel** e o **prompt usado para extrair dados de vagas** do LinkedIn, gerando arquivos prontos para análise no Excel, Python ou SQL.

---

## 1️⃣ Estrutura das abas do Excel

### Aba `vagas`
Colunas:  ID,Empresa,Cargo,Modelo_Trab,Area_Atuacao,Data,Nível,Salario,Link_Vaga,Destaque,Localizacao,Tipo_Contratacao,Num_Candidatos,Idiomas,Beneficios,Departamento,Ferramentas_Específicas,Remoto

### Aba `skills`
Colunas:  Vaga_ID, Skill, Tipo, Nivel_Conhecimento, Obrigatoria, Categoria

---

## 2️⃣ Prompt para extrair dados do LinkedIn

```
**Regras gerais:**
1. Use **data atual (18/01/2024)** se a vaga não especificar data.  
2. Preencha **Nível** apenas se for explícito: "Júnior", "Pleno" ou "Sênior".  
3. Skills **obrigatórias/mínimas**: palavras como "necessário", "obrigatório", "requisito".  
4. Skills **diferenciais/plus**: palavras como "desejável", "diferencial", "plus", "conhecimento em".  
5. Para skills, preencha `Nivel_Conhecimento` se especificado, caso contrário deixar em branco.  
6. Para skills, `Obrigatoria` = "Sim" para obrigatórias, "Não" para diferenciais.  
7. Categorize cada skill de forma geral (ex.: Programação, Banco de Dados, Ferramentas, Soft Skills).  
8. **Responda apenas com os dados**, uma linha para a vaga e múltiplas linhas para skills, **sem repetir colunas ou explicar nada**.  
9. Use `[ID]` único para a vaga e repita o mesmo ID em `Vaga_ID` para todas as skills.

**Aba `vagas` (uma linha):**  
- Formato: `[ID],[Empresa],[Cargo],[Modelo_Trab],[Area_Atuacao],[Data],[Nível],[Salario],[Link_Vaga],[Destaque],[Localizacao],[Tipo_Contratacao],[Num_Candidatos],[Idiomas],[Beneficios],[Departamento],[Ferramentas_Específicas],[Remoto]`  

**Aba `skills` (uma linha por skill):**  
- Formato: `[Vaga_ID],[Skill],[Tipo],[Nivel_Conhecimento],[Obrigatoria],[Categoria]`  

**Descrição da vaga:**  
[COLE AQUI A DESCRIÇÃO COMPLETA]

```
