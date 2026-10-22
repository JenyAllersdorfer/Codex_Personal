---
lido: completo (PDF)
resumo: true
slide: false
---
---
# Guzman et al. 2026 – ELLAS Survey Dataset

## Objetivo do artigo
Apresentar o ELLAS Survey Dataset, uma base de dados aberta com
respostas de um questionário na Bolívia, no Brasil e no Peru, e explicar
como ela foi montada para que outras pessoas possam usá-la.

## Resumo pequeno
- O questionário tem 136 perguntas sobre fatores que influenciam o
  interesse por carreiras em STEM e a vontade de liderar.
- Foi aplicado entre ago/2023 e mar/2024, em espanhol e português.
- As pessoas foram escolhidas de propósito, com cotas, e não sorteadas.
  Por isso os números não representam todo o país.
- A base tem 10.311 respostas e 220 colunas. O Brasil tem 3.788.
- Os autores já fizeram uma limpeza e criaram a coluna problem_case,
  que avisa quais respostas parecem estranhas.

## Como me ajuda
- É o artigo sobre a base que eu vou tratar.
- Me mostra como ler os nomes das colunas e quais temas existem.
- Já tem uma limpeza feita, então começo conferindo o problem_case.
- Lembra que o Lumina não deve dizer que os números valem para todo o
  Brasil.
- Meu foco por ora é só o Brasil (coluna country = Brazil).

## Limitações
- A amostra foi escolhida de propósito (não sorteada), então os números
  não valem para o país inteiro.
- A coleta foi online no Brasil e no Peru e presencial na Bolívia, o que
  pode mudar as respostas e atrapalhar a comparação entre países.
- Mesmo depois da limpeza, sobram poucas respostas estranhas (por isso
  existe o problem_case).
- Tradução e classificação de profissões podem ter pequenas diferenças
  de sentido entre idiomas.

## Citação útil
- Os autores recomendam excluir os registros com problem_case = 1 nas
  análises padrão, mas deixam a decisão para quem usa os dados
  (Guzman et al., 2026, p. 3).
- Por ser uma amostra intencional, ela não permite generalização
  estatística (Guzman et al., 2026, p. 11).
## Pendências
- Abrir o CSV e ver quantas linhas do Brasil têm problem_case = 1.
- Confirmar com o prof se uso ou excluo essas linhas.
- Conferir termos de uso e anonimização.

# Resumo de estudo: ELLAS Survey Dataset

## 1. O que é este artigo
É um *data article*. Ele não testa hipóteses: apresenta uma base de
dados e explica como ela foi feita, para outras pessoas poderem usá-la.
É como o manual de um aparelho: o aparelho é o dataset (o CSV) e o
artigo é o manual. A base vem de um questionário aplicado na Bolívia, no
Brasil e no Peru sobre o que influencia o interesse por carreiras em
STEM e a vontade de liderar.

## 2. Por que a base foi criada
- Mulheres são 30% dos pesquisadores no mundo e 24% das líderes de
  tecnologia.
- Na América Latina elas são 48% da força de trabalho, mas menos de um
  terço dos profissionais de STEM, e só 30% dos formados em STEM.
- A maioria dos estudos anteriores era qualitativa, de amostra pequena
  ou de um só país, o que impedia comparar países.
- A solução foi um questionário grande e igual nos três países.
- Ele nasceu de um estudo que mapeou a literatura dos últimos 12 anos e
  documentos da UNESCO e da OCDE. Esse estudo gerou 6 fatores de
  contexto e 196 subfatores, e os autores escolheram quais medir.

## 3. O que a base contém
- 10.311 respostas (linhas) e 220 colunas (indicadores), em dois
  arquivos: o CSV e o dicionário de dados.
- O CSV é descrito como dado bruto.
- Parte das informações foi respondida pela pessoa e parte foi
  codificada pela empresa de pesquisa (por exemplo, o ano de nascimento
  virou faixa de geração).

Perfil dos respondentes:
- **Bolívia:** 3.189 respondentes; 76% em carreira STEM; 50% em TI; 3%
  nascidos em 1945–1964; 21% casadas.
- **Brasil:** 3.788 respondentes; 46% em carreira STEM; 38% em TI; 13%
  nascidos em 1945–1964; 47% casadas.
- **Peru:** 3.334 respondentes; 73% em carreira STEM; 46% em TI; 14%
  nascidos em 1945–1964; 30% casadas.

O que isso significa: a amostra do Brasil tem menos gente de STEM e de TI
e é mais velha e mais casada que a da Bolívia. Ao olhar só o Brasil,
lembre desse perfil.

## 4. Como ler o nome de uma coluna
O nome segue a ordem: letra do fator + número + tipo + nome.
Exemplo: `b2_d_mentor` é do fator acadêmico (b), pergunta 2, tipo
*dummy* (d), sobre ter mentor.

Tipos:
- `t` texto aberto
- `n` número
- `d` sim/não (1/0)
- `l` escala de 1 a 7
- `c` categoria

Duas marcas importam:
- **R (codificação reversa):** em frases negativas, como "sou um grande
  fracasso", concordar muito significa o contrário das outras frases.
  Antes de somar os itens, é preciso inverter a escala (1 vira 7, 2 vira
  6, e assim por diante). A marca R avisa disso.
- **X:** item de determinação complexa, que exige cuidado na
  interpretação.

O dicionário tem uma linha por coluna, com o tipo de fator, o nome, o
código completo, a pergunta em inglês, português e espanhol, as
respostas possíveis e as observações.

## 5. O que o questionário mede
O questionário tem 136 perguntas. Quase tudo é escala de 1 (discordo
totalmente) a 7 (concordo totalmente), adaptada de escalas já validadas
e traduzida com retrotradução para conferir o sentido.

- **Individual (a):** não pertencimento, autoeficácia, autoconfiança,
  independência financeira, identidade de gênero feminina, desigualdade
  de gênero percebida, bullying, sentido do trabalho.
- **Acadêmico (b):** estereótipos sobre quem trabalha em STEM, qualidade
  da mentoria, igualdade de gênero percebida na instituição, relação com
  colegas.
- **Trabalho (c):** cultura da organização, autonomia e impacto no
  trabalho.
- **Social (e):** sexismo sofrido, atitudes sobre mulheres como gestoras,
  estereótipos sobre mulheres.
- **Família (f):** apoio familiar, expectativas dos pais.
- **Interesse em STEM (g1):** 5 frases, como "espero que meu futuro
  emprego seja de STEM".
- **Motivação para liderar (g2):** gostar de liderar e liderar por dever
  (9 itens cada).
- **Políticas de gênero (g3 a g5):** para 11 políticas (salário igual,
  combate ao assédio, cotas, mentoria…): se acha importante, se existe
  na sua organização e se sofreu por ela não existir.
- **Controles:** computador, internet e energia em casa, ter mentor,
  escolaridade dos pais.

Observações:
- As medidas de política são novas e ainda sem confiabilidade
  comprovada, segundo os próprios autores.
- O texto cita três componentes de motivação para liderar, mas a tabela
  traz só dois.

## 6. Como os dados foram coletados
- Os autores contrataram empresas de pesquisa a partir de setembro de
  2022. Queriam uma só empresa para os três países, mas depois de cinco
  meses sem achar nenhuma ficaram com duas: uma para a Bolívia e outra
  para Brasil e Peru.
- A amostra foi intencional, com cotas por idade, gênero e área (STEM
  ou não), em áreas urbanas. A meta mínima era 3.189 pessoas por país.
- A coleta foi de agosto de 2023 a março de 2024: online, por painéis,
  no Brasil e no Peru, e presencial na Bolívia.
- O Brasil terminou por último, pela dificuldade de recrutar estudantes
  variados.

## 7. O problem_case
- É uma coluna de aviso: 0 = nada estranho; 1 = resposta suspeita.
  Nenhuma linha foi apagada.
- Vira 1 quem tem filhos demais, diz ter concluído estudos cedo demais,
  tem experiência de trabalho que não bate com a idade ou tem
  pós-graduação sem graduação.
- Os autores recomendam excluir os casos 1 nas análises padrão.
- As idades foram calculadas com o ano de nascimento e o ano 2024.
- Há diferenças entre as versões de idioma: a opção "Administração
  Pública e Defesa" existe em espanhol, mas em português só aparece
  "Administração Pública".

## 8. Ética
- Brasil: protocolo aprovado pelo CEP-Humanidades/UFMT em 06/03/2023,
  com Termo de Consentimento.
- Peru: aprovado pela Universidad de Lima (22/05/2023).
- Bolívia: aprovado por um comitê da Universidad Mayor de San Andrés
  (27/06/2023).
- A participação foi voluntária.

## 9. Limitações
- Amostra intencional: não permite dizer que vale para toda a
  população.
- Modos de coleta diferentes: online ou presencial pode influenciar as
  respostas e atrapalha comparar países.
- Ainda restam poucos registros atípicos, mesmo depois da limpeza.
- Tradução e classificação de profissões podem ter nuances que mudam o
  sentido.

## 10. Para que serve a base
Para estudos que comparam países ou subgrupos (por etapa de carreira,
setor, gênero) e para apoiar políticas de participação e liderança
feminina em STEM.

## 11. O que isso significa para o meu trabalho
- Meu foco é só o Brasil: a coluna `country` (valor "Brazil") separa
  essas linhas.
- A limpeza já começou: parto do `problem_case`, conto quantas linhas do
  Brasil têm valor 1 e registro cada decisão no log.
- O Lumina não pode afirmar que os percentuais valem para todo o Brasil.
- O dicionário é o meu mapa para entender e agrupar as variáveis.

## 12. Glossário rápido
- **Dataset:** a tabela de dados.
- **CSV:** arquivo de texto que guarda essa tabela.
- **Dicionário de dados:** o que cada coluna significa.
- **Amostra intencional:** pessoas escolhidas de propósito, não
  sorteadas.
- **Escala Likert:** de "discordo totalmente" a "concordo totalmente".
- **Variável *dummy*:** só tem dois valores, 1 (sim) e 0 (não).
- **Retrotradução:** traduzir de volta para conferir se o sentido ficou
  igual.