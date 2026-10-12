---
responsável: eu
lido: completo (PDF)
resumo: pendente
slide: pendente
---
# Guzman 2026 

## Referência (ABNT)
GUZMAN, I. R.; BRANISA, B.; DAVILA, G.; SÁNCHEZ-GUILLÉN, F.; RONDON
PEREIRA, L. R.; MENDES, L.; FRIGO, L. B.; RODRÍGUEZ-RODRIGUEZ, N.; BIM,
S. A.; MACIEL, C. Introducing "ELLAS Survey Dataset" an open resource
about factors that influence career interest and leadership in STEM in
Bolivia, Brazil, and Peru. Data in Brief, v. 66, art. 112721, 2026.
DOI: 10.1016/j.dib.2026.112721.

## Fichamento
Por que leio: descreve o dataset do Brasil que vou curar.

Objetivo: apresentar um dataset aberto e um dicionário de dados
multilíngue para comparar Bolívia, Brasil e Peru sobre interesse por
carreiras em STEM e motivação para liderar.

Problema: estudos anteriores eram qualitativos, de amostra pequena ou de
um só país, o que limitava a comparação regional.

Coleta:
- Survey de 136 perguntas (escalas validadas), em espanhol e português,
  com tradução e retrotradução.
- Amostra intencional, com cotas por idade, gênero e área (STEM ou não).
- Ago/2023 a mar/2024. Online (painéis) no Brasil e no Peru, presencial
  na Bolívia. O Brasil terminou por último (difícil recrutar estudantes).
- Ética no Brasil: CEP-Humanidades/UFMT, aprovado em 06/03/2023, com TCLE.

Dataset: 10.311 observações e 220 indicadores (dados informados pelas
pessoas + dados recodificados pela empresa de pesquisa).

Brasil (Tabela 1):
| Respondentes | 3.788 |
| Sexo ao nascer | fem. 1.916 (51%) · masc. 1.872 (49%) |
| Nascimento | 1997–2005: 36% · 1981–96: 38% · 1965–80: 13% · 1945–64: 13% |
| Estado civil | solteira 47% · casada 47% · divorciada 5% · viúva 1% |
| Carreira STEM | 1.750 (46%) · não STEM 2.038 (54%) |
| Área de TI | 1.442 (38%) · não TI 2.346 (62%) |

Curadoria já feita pelos autores:
- Coluna problem_case = 1 marca registros suspeitos; recomendam excluí-los
  nas análises padrão.
- Critérios: 5+ filhos em uma faixa etária; 9+ filhos menores de 18;
  titulação em idade implausivelmente baixa (graduação antes de 21,
  mestrado antes de 23, doutorado antes de 26, pós-doc antes de 30);
  experiência profissional incompatível com a idade; pós-graduação sem
  graduação.
- Inconsistência entre idiomas: "Public Administration and Defense" nas
  versões em espanhol e só "Public Administration" na versão brasileira.

Como ler uma variável (Tabelas 3 e 4):
- Estrutura: fator + número + tipo + nome. Ex.: b2_d_mentor.
- Tipos: t texto aberto · n numérico · d dummy (0/1) · l Likert 1–7 ·
  c categórica.
- Marcas: R = sugerida inversão de código · X = item de determinação
  complexa. Itens com R precisam de atenção antes de calcular escores.

Onde estão os arquivos:
- Página: https://plataform.ellas.ufmt.br/open-data/1
- CSV: https://plataform.ellas.ufmt.br/survey/surveyELLAS_2025–11–21_.csv
- Dicionário (PDF): https://plataform.ellas.ufmt.br/survey/Data_dictionary-2025-11-21.pdf

Limitações declaradas:
- Amostra intencional: não permite generalização estatística.
- Modos de coleta diferentes entre países (efeito de modo).
- Poucos registros atípicos mesmo após limpeza.
- Nuances de tradução e de classificação profissional.

Atualidade: dados coletados em 2023–2024; arquivo de 21/11/2025.

O que não entendi:
- (preencher depois de abrir o CSV e o dicionário)

Como vou usar:
- Dicionário como base do mapeamento de variáveis (Obj. Específico 1).
- Etapa 2 parte do problem_case: verificar, decidir e registrar no log.
- Lumina deve tratar os números como amostra intencional, não população.

## Resumo (entrega, até 3 páginas, em português)
(escrever com as suas palavras)