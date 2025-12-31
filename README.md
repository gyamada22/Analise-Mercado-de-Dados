
#  Análise do Mercado de Dados: Resumo do Projeto

---

## 1. Metodologia
O projeto mapeou o mercado de dados brasileiro através da extração de informações de vagas reais, utilizando IA para converter descrições textuais em métricas de competências classificadas como **Obrigatório** ou **Diferencial**.

---

## 2. Evolução por Senioridade

<p align="center">
  <img src="./docs/images/junior_project.png" width="700">
</p>

###  Júnior (101 Vagas)
* **Base [Obrigatório]:** Domínio de **Power BI** (27,36%), Excel Avançado (20,27%) e SQL (18,58%).
* **[Diferencial] de Destaque:** **Bibliotecas Python** (8,85%) e Tableau (5,31%) aparecem como as principais ferramentas para superar a concorrência inicial.
* **Visão Técnica:** Sem a tríade básica, **Bibliotecas Python (Pandas, NumPy)** (14,16%) e ETL (6,44%) lideram a lista de exigências.

###  Pleno (137 Vagas)
* **Migração Técnica [Obrigatório]:** **Power BI** (37,50%) e SQL (35,81%) continuam fortes, mas o **Python** (28,38%) torna-se um pilar de sustentação.
* **O Valor do Tableau:** Ocupa um papel estratégico como **[Diferencial]** (7,21%) e sua obrigatoriedade técnica salta para 10,73% quando ignoramos as ferramentas básicas.
* **Novos Requisitos:** ETL e Machine Learning surgem como diferenciais críticos (9,91% cada).

###  Sênior (64 Vagas)
* **Arquitetura e Escala [Obrigatório]:** O foco muda para Cloud (AWS 10,34% como diferencial) e Big Data (9,48%).
* **Especialização:** O ETL atinge seu maior nível de obrigatoriedade técnica (13,26%).
* **Governança e Orquestração:** Machine Learning (8,60%), Git (3,94%) e **Apache Airflow** consolidam-se como requisitos para liderança de projetos.

---

## 3. O Peso Estratégico do Tableau
Embora o **Power BI** seja a ferramenta universal em volume, o Tableau é identificado nos dados como o principal "divisor de águas". Ele atinge seu pico de importância no nível Pleno, onde é o terceiro maior diferencial (7,21%) e apresenta uma obrigatoriedade técnica de 10,73% para vagas que buscam especialização fora do ecossistema Microsoft.

---

## 4. Recomendações de Carreira (Pathing)

1.  **Início (Júnior):** Foque em **Power BI** e SQL, mas estude Tableau para entrar no grupo de elite com diferenciais técnicos.
2.  **Meio (Pleno):** Domine **Bibliotecas Python** (Pandas, NumPy) e processos de ETL. Use o Tableau para visualizações de maior complexidade e performance.
3.  **Fim (Sênior):** Direcione o aprendizado para arquitetura em Nuvem (AWS/Azure) e **Orquestração** de grandes volumes de dados com **Apache Airflow**.

---

## 5. Conclusão
A análise demonstra que o profissional deve evoluir de um perfil de "consumo de dados" (Júnior/BI) para um perfil de "construção de arquitetura" (Sênior/ETL/Cloud). O Tableau atua como uma ponte estratégica nessa evolução, oferecendo um diferencial competitivo sólido para quem busca posições de maior senioridade e especialização técnica.






















-------------------------------------
# Job Market Analysis 

## 🖥️ Descrição do Projeto
- Este projeto tem como objetivo analisar **vagas reais de emprego na área de dados**, coletadas a partir de plataformas de recrutamento (ex: LinkedIn), para extrair insights sobre **skills demandadas, tendências do mercado e gaps de competências**.

- A análise é inicialmente focada no **mercado brasileiro**, com posterior **comparação com dados internacionais**, visando identificar padrões globais e possíveis tendências que podem chegar ao Brasil no futuro.

- O projeto transforma dados não estruturados em **insights analíticos e dashboards interativos**, documentando todo o pipeline de dados de forma clara e profissional.

---

## 🔹 Coleta de Dados
> **Desafio:** LinkedIn possui API fechada, impossibilitando a coleta automatizada de vagas diretamente via Python.

> **Solução:** Para contornar, coletei os dados manualmente, visitando cada vaga e usando prompts de IA para extrair informações estruturadas (empresa, cargo, localização, data e skills).

Essa abordagem garantiu **eficiência e confiabilidade** para o pipeline subsequente.

---

## 🛠️ Tecnologias e Ferramentas

O fluxo do projeto segue:

**Coleta** ![IA](https://img.shields.io/badge/IA-AI-blue) ⟶ **Visualização** ![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoft-excel&logoColor=white) ⟶ **Limpeza** ![Python](https://img.shields.io/badge/Python-3670A0?style=flat&logo=python&logoColor=white) ⟶ **Análise** ![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white) ⟶ **Apresentação** ![Power BI](https://img.shields.io/badge/Dashboard-F2C811?style=flat&logo=power-bi&logoColor=black) ⟶ **Documentação** ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)

| Etapa | Ferramenta | Função |
|-------|------------|------|
| Coleta & extração | IA via prompts | Extrai dados estruturados da vaga |
| Visualização inicial | Excel | Conferência e revisão rápida. Arquivo: **[Raw Data](https://raw.githubusercontent.com/gyamada22/Job-Market-Analysis/main/data/Vagas_Coletadas_Raw.xlsx)** |
| Limpeza e padronização | Python | Padroniza dados, corrige inconsistências e gera Excel/SQL. Arquivo: **[Cleaned Data](https://raw.githubusercontent.com/gyamada22/Job-Market-Analysis/main/data/Vagas_Coletadas_Cleaned.xlsx)**, Script: **[ETL.py](https://github.com/gyamada22/Job-Market-Analysis/blob/main/data/ETL.py)** |
| Modelagem e análise | SQL | Criação de tabelas, views e queries analíticas *(em desenvolvimento)* |
| Dashboards | Power BI | Visualização interativa, insights e storytelling |
| Documentação | GitHub | Registro completo do projeto, metodologia e exemplos de dashboards |

> 💡 Observação: Python permite **automatizar toda a cadeia de transformação**, tornando o fluxo de dados mais eficiente e escalável do que usar Excel para limpeza manual.

---

## 🎯 Objetivos
- Coletar dados de vagas reais: empresa, cargo, localização, data, nível de senioridade e requisitos técnicos.  
- Padronizar e estruturar dados textuais não estruturados (descrições de vagas).  
- Identificar **skills mais demandadas** por área e nível (estágio, júnior, pleno, sênior).  
- Analisar **diferenças e gaps de competências** entre níveis de senioridade.  
- Comparar o mercado brasileiro com dados internacionais para identificar **tendências emergentes**.  
- Criar dashboards interativos que apoiem **decisões de carreira e estudo**.  
- Documentar todo o pipeline: **coleta → limpeza → análise → visualização**.

---

## ✅ Status Atual
- [x] Estrutura de pastas criada  
- [x] Coleta de dados inicial 
- [ ] Modelagem do banco de dados  
- [ ] Primeiras análises  
- [ ] Dashboard inicial  

---

## 🔹 Observações Finais
- Pipeline eficiente, contornando limitações do LinkedIn  
- Uso integrado de IA, Python, SQL, Power BI e Excel
- Documentação clara, garantindo transparência e profissionalismo para portfólio
