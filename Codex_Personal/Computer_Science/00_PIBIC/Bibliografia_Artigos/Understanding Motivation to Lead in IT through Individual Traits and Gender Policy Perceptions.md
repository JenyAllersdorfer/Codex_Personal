---
lido: completo (1 página + referências)
resumo: true
slide: false
---
---
# Guzman et al. 2026 – Motivation to Lead em TI
## Objetivo do artigo
Descrever um estudo planejado para entender o que motiva pessoas em TI
a querer liderar, olhando para características individuais e para o que
elas pensam sobre as políticas de igualdade de gênero.

## Resumo pequeno
- É um resumo estendido de uma página: mostra o plano do estudo e não
  traz resultados.
- Motivação para liderar = o quanto a pessoa quer assumir papéis de
  liderança (por gostar, por dever ou apesar dos custos).
- Hipótese 1: quem tem mais autoeficácia e autoconfiança quer liderar
  mais; quem sente muita desigualdade de gênero tende a querer menos.
- Hipótese 2: quem acha importantes as políticas de igualdade, sabe que
  elas existem e sofreu pela falta delas tende a querer liderar mais.
- Usa só os dados da Bolívia do ELLAS Survey Dataset: 1.599 pessoas de
  TI e 1.590 de fora de TI.
- Usa um método estatístico (modelagem de equações estruturais) que
  testa relações entre conceitos medidos pelo questionário.

## Como me ajuda
- Possível modelo do texto que o prof pediu para imitar (confirmar).
- Mostra como a base que vou tratar já é usada em análises.
- Me diz quais colunas importam nesse tipo de estudo: autoeficácia
  (a2), autoconfiança (a3), desigualdade percebida (a6), motivação para
  liderar (g2) e políticas (g3, g4, g5).

## Limitações
- O texto não tem resultados nem discute limitações, porque é só um
  resumo do estudo planejado.
- Observação minha: um estudo transversal mostra associações, não prova
  causa.

## Citação útil
- Os autores propõem incluir a percepção sobre políticas institucionais
  de igualdade de gênero como um novo fator que influencia a motivação
  para liderar (Guzman et al., 2026, p. 130).

## Pendências
- Perguntar ao prof: "imitar" é seguir a estrutura do texto ou repetir
  a análise com os dados do Brasil?
- Perguntar se existe a versão completa do trabalho.


# Resumo de estudo: Understanding Motivation to Lead in IT

## 1. O que é este texto
- É um *extended abstract* (resumo estendido) de uma página, publicado
  nos anais do SIGMIS-CPR 2026.
- Mostra o plano de um estudo: por que fazer, com quais conceitos e dados,
  e como analisar. Ele não traz resultados (os verbos estão no futuro:
  "será avaliada", "serão conduzidas").
- É o paper da Bolívia que o prof pediu para eu imitar.

## 2. Qual é o problema
- Mulheres são minoria na liderança em TI: segundo o texto, cerca de 18%
  dos cargos de liderança no mundo.
- Há interesse crescente em igualdade de gênero em STEM, mas pouca
  atenção aos fatores psicológicos e institucionais que moldam a vontade
  das mulheres de liderar em TI.
- A "motivação para liderar" já foi ligada a eficácia na liderança e a
  resultados de treinamento, mas quase nunca foi estudada em TI. Essa é
  a lacuna.

## 3. Conceito central: motivação para liderar (MTL)
- Definição de Chan e Drasgow (2001): diferenças entre as pessoas no
  desejo de assumir e exercer papéis de liderança.
- Três formas:
  - **Afetivo-identitária:** gosta de liderar e se enxerga como líder.
  - **Normativo-social:** lidera por dever ou obrigação.
  - **Não calculista:** lidera apesar dos custos pessoais, sem fazer a
    conta de custo e benefício.
- O estudo trabalha com as duas primeiras (a base do ELLAS só mede essas).

## 4. As duas teorias e as hipóteses
**Teoria Sociocognitiva** (olha para a pessoa):
- Autoeficácia: acreditar que consegue ter sucesso em STEM.
- Autoconfiança: perceber a própria competência em relação aos outros.
- Desigualdade de gênero percebida: achar que mulheres têm menos
  oportunidades que homens.
- Hipótese: mais autoeficácia e autoconfiança levam a mais motivação
  afetivo-identitária e normativo-social. A percepção forte de
  desigualdade pode reduzir a motivação, por sinalizar um ambiente pouco
  receptivo.

**Teoria Institucional** (olha para a organização):
- Ideia simples: o que a pessoa percebe sobre as regras e políticas da
  sua organização influencia suas aspirações.
- O estudo mede a percepção sobre políticas de igualdade de gênero em
  três pontos: quanto acha importantes, se sabe que existem na sua
  organização e se sofreu consequências pela ausência delas.
- Hipótese: essas percepções se associam positivamente à motivação para
  liderar.

## 5. Dados e amostra
- Usa o ELLAS Survey Dataset, que é público.
- Só os dados da Bolívia: 1.599 pessoas da área de TI e 1.590 de fora
  de TI. A soma (3.189) bate com o total da Bolívia no Data in Brief.
- Estudo quantitativo e transversal (dados de um único momento).
- A amostra inclui homens e mulheres: o estudo controla por gênero, e
  na Bolívia a divisão por sexo ao nascer é de cerca de 50% cada.

## 6. Método (explicado simples)
- **Modelagem de equações estruturais:** testa relações entre conceitos
  que não se medem diretamente, usando as respostas do questionário.
- **Análise fatorial confirmatória:** confere se os itens do
  questionário realmente medem o conceito que deveriam.
- **Confiabilidade composta:** mede se os itens de um mesmo conceito
  "concordam" entre si.
- **Variância média extraída:** mede o quanto do conceito os itens
  conseguem capturar.
- Como as medidas de política são novas, haverá análises exploratórias
  antes da confirmatória.
- Controles: gênero, setor (TI ou não), experiência de liderança e
  geração. Também haverá análises separadas por setor.

## 7. Onde essas variáveis estão no dataset
- Autoeficácia: grupo `a2`
- Autoconfiança: grupo `a3`
- Desigualdade de gênero percebida: grupo `a6`
- Motivação afetivo-identitária: grupo `g2_1`
- Motivação normativo-social: grupo `g2_2`
- Políticas: importância (`g3`), existência (`g4`) e consequências (`g5`)
- Setor TI: `g7_d_it_area`
- Controles prováveis: sexo (`d2_d_sex`), gênero autodeclarado
  (`d3_c_gender`), faixa de geração (`d1_1_c_range`) e situação de
  liderança (`d14_1` a `d14_3`). Conferir no dicionário.

## 8. Contribuição esperada
- Levar o estudo da motivação para liderar para o contexto de TI.
- Incluir a percepção sobre políticas institucionais de igualdade de
  gênero como um fator novo que influencia essa motivação.
- Servir de base para programas de desenvolvimento de liderança e
  políticas organizacionais que apoiem as aspirações das mulheres em
  tecnologia.

## 9. Limitações
- O texto não discute limitações, porque é só o plano do estudo.
- Observação minha: estudo transversal mostra associações, não prova
  causa e efeito.

## 10. O que isso significa para o meu trabalho
- É um modelo de estrutura: problema, conceitos, teoria e hipóteses,
  dados, método e contribuição.
- Mostra como a base que vou tratar é usada em análises.
- Me diz quais grupos de colunas são importantes nesse tipo de estudo.
- O estudo usa a Bolívia. Meu foco é o Brasil, e as mesmas colunas
  existem para os dois países (a diferença é a coluna `country`).

## 11. Glossário rápido
- **MTL:** motivação para liderar.
- **Antecedente:** fator que vem antes e influencia outro.
- **Estudo transversal:** dados coletados em um único momento.
- **Autoeficácia, autoconfiança, desigualdade percebida:** ver seção 4.
- **Modelagem de equações estruturais, análise fatorial confirmatória,
  confiabilidade composta, variância média extraída:** ver seção 6.