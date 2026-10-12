# Dados do TSE

Arquivos usados pelo projeto (todos versionados no repositório — são pequenos):

- `consulta_cand_2026.zip` — cadastro de candidatos (~3 MB)
- `bem_candidato_2026.zip` — bens declarados (~4 MB)
- `candidatos_DEPUTADO_FEDERAL_NORTE_2026.csv` — dataset limpo gerado pela Fase 0 (versão "congelada")
- `prestacao_de_contas_eleitorais_candidatos_2026.zip` — prestação de contas (**apenas os 7 estados da Região Norte**: AC, AM, AP, PA, RO, RR, TO), ~7 MB

> **Observação:** o arquivo original do TSE traz o Brasil inteiro (~134 MB, acima do limite de 100 MB do GitHub). Aqui ele foi **reduzido para conter só a Região Norte** — que é o recorte do projeto e o único que os notebooks leem (despesas contratadas por candidato dos 7 estados). Para reconstruir a versão nacional, baixe pelo navegador:
> `https://cdn.tse.jus.br/estatistica/sead/odsele/prestacao_contas/prestacao_de_contas_eleitorais_candidatos_2026.zip`
