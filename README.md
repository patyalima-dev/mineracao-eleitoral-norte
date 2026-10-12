# Mineração de Dados Eleitorais 2026 — Deputados Federais da Região Norte

Projeto da disciplina **Aprendizagem de Máquina Não Supervisionada** (Prof. Rogério Lopes).
Da preparação dos dados à detecção de anomalias, com dados reais e abertos do **TSE — Eleições 2026**.

**Recorte do grupo:** cargo **Deputado Federal**, **Região Norte** — AC, AM, AP, PA, RO, RR, TO · **925 candidatos**.

**Integrantes:** Carlos · Patricia · Rafael — Grupo Região Norte, Pós-graduação, Faculdade de Tecnologia e Inovação Senac DF.

---

## Conteúdo

| Arquivo | Descrição |
|---|---|
| **`PROJETO_COMPLETO_Mineracao_Norte.ipynb`** | ⭐ Notebook único com **todo o projeto** (Fase 0 → Fase 4 + desafio + extensão de 4 variáveis), **todas as células executadas, com outputs**. |
| **`Apresentacao_Mineracao_Norte_finalv1.0.pptx`** | Apresentação utilizada pelo grupo. |
| `requirements.txt` | Dependências (versões fixadas). |
| `dados/` | Dados do TSE (ver `dados/LEIA-ME.md`). |

### Fases (dentro do notebook único)
Fase 0 (preparação) · Fase 1 (análise descritiva) · Fase 2 (K-Means e Bisecting K-Means) · Fase 2b (DBSCAN e hierárquico) · Desafio (gasto de campanha + quartis) · Fase 2 estendida (clusterização com 4 variáveis) · Fase 3 (regras de associação — Apriori) · Fase 4 (detecção de anomalias — Isolation Forest).

## Como executar
- **Colab:** abrir o notebook; se faltar biblioteca, rodar `!pip install -q "mlxtend==0.23.1"`.
- **Local (VS Code):** criar o `.venv` a partir do `requirements.txt` e selecionar o kernel.

> **Importante:** use `mlxtend==0.23.1` — versões novas (0.23.2+) quebram o `association_rules` da Fase 3.

## Principais resultados
- **5 perfis socioeconômicos** (Bisecting K-Means, k=5): Prósperos, Batalhadores, Promissores, Recém-chegados, Desassistidos.
- As **regras de associação (Apriori) confirmam os nomes** dos clusters (lift > 6 em várias regras).
- **Isolation Forest (contaminação 5%)**: 47 candidatos atípicos; concentram-se nos grupos de menor escolaridade.
- **Desafio / 4 variáveis:** incluir o **gasto de campanha** melhora a silhueta e é uma dimensão nova (correlação ~0,36 com o patrimônio).

## Fonte dos dados
Portal de Dados Abertos do TSE — Consulta de Candidatos, Bens de Candidatos e Prestação de Contas, Eleições 2026 (`https://dadosabertos.tse.jus.br`).
