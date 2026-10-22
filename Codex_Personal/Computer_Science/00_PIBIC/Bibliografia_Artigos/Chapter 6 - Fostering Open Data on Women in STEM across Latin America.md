---
lido: completo
resumo: true
slide: false
---
---
# Maciel et al. 2025 – Cap. 6, Fostering Open Data (livro)

## Objetivo do capítulo
Mostrar como a rede ELLAS reúne, organiza e publica como dados abertos
informações sobre mulheres em STEM na Bolívia, no Brasil e no Peru, e
como construiu a plataforma de dados abertos que os disponibiliza.

## Resumo pequeno
- Faltam dados abertos e confiáveis sobre mulheres em STEM na América
  Latina; os que existem estão espalhados ou em formatos não
  estruturados (artigos, redes sociais).
- A rede ELLAS (criada em 2022 por pesquisadores da Bolívia, do Brasil e
  do Peru) reúne dados que já existem e dados novos, gerados por um
  survey.
- Os dados são organizados em políticas, iniciativas, fatores de
  contexto e indicadores de contexto, além do survey.
- Nesse texto, dado "primário" é o não estruturado (artigos, redes
  sociais, survey) e "secundário" é o que já vem estruturado, de
  planilhas oficiais.
- A plataforma tem 3 camadas (dados, processamento e aplicação), usa
  arquivos CSV e ontologias, é gratuita e está em português, espanhol e
  inglês.
- Desafios: dados difíceis de achar, termos diferentes para a mesma
  coisa (inclusive em idiomas diferentes) e buscas em inglês que perdem
  iniciativas locais.
- Trabalho futuro: validar o survey por análise estatística, criar
  documentação e protocolos e ampliar para outros países.

## Como me ajuda
- Mostra onde a minha curadoria entra: o survey é dado primário, que é
  analisado e transformado para a estrutura da ELLAS antes de ir para a
  plataforma.
- O exemplo de padronizar termos (a mesma ideia com nomes diferentes,
  em 3 idiomas) é o mesmo tipo de problema do Data in Brief
  ("Administração Pública" com e sem "Defesa"). Serve de modelo para o
  meu log.
- O processamento da plataforma já usa CSV e JSON, então o meu arquivo
  final nesses formatos é compatível.
- O trabalho futuro cita validar o survey e criar documentação e
  protocolos, o que o meu plano faz nas Etapas 2 a 4. Serve para
  justificar nos relatórios.
- A plataforma mostra visões gerais, não dados pessoais nem contatos. O
  Lumina deve seguir a mesma linha.
- Esclarece os nomes: rede ELLAS (as pessoas), iniciativa/projeto (o que
  foi financiado) e plataforma (o produto).

## Limitações
- O capítulo não tem seção de limitações: é descritivo.
- Os autores contam desafios: dados disponíveis de formas diferentes
  entre os países, dificuldade de definir o que é STEM e de achar dados
  separados por gênero, e buscas em inglês que não achavam iniciativas
  locais (p. 123–124).
- A camada de aplicação ainda estava sendo desenhada (p. 126) e o survey
  ainda seria validado estatisticamente (p. 133).
- Observação minha: não traz resultados de testes de uso da plataforma.

## Citação útil
- Uma plataforma de dados abertos é uma infraestrutura digital que dá
  acesso público a vários conjuntos de dados, com ferramentas para
  buscar, filtrar e visualizar (Maciel et al., 2025, p. 118).
- Para integrar fontes diferentes, a ELLAS padroniza os termos: rótulos
  distintos para a mesma ideia, inclusive em idiomas diferentes, passam a
  ser tratados como sinônimos (Maciel et al., 2025, p. 124).
- Como trabalho futuro, a rede pretende validar o survey por análise
  estatística e criar documentação e protocolos de uso (Maciel et al.,
  2025, p. 133).

## Pendências
- Entender se o CSV do survey e os dados do survey exibidos na
  plataforma são a mesma coisa.

# Resumo de estudo: Cap. 6, Fostering Open Data on Women in STEM across Latin America

## 1. O que é este texto
- É um capítulo de livro (p. 117–137) escrito por 11 autores da rede
  ELLAS.
- Não testa hipóteses. Conta como a rede construiu a plataforma de dados
  abertos. É como o diário de obra do projeto: mostra como os dados
  foram achados, arrumados e publicados.

## 2. Qual é o problema
- Segundo o Banco Mundial, o investimento em dados de gênero na América
  Latina ficou para trás nos últimos 5 anos.
- A falta de dados abertos e confiáveis sobre mulheres em STEM atrapalha
  fechar a desigualdade. Também faltam dados que cruzem várias
  características das pessoas.
- A região mistura desigualdade econômica, instabilidade política e
  normas de gênero muito enraizadas. Sem dados do contexto local, é
  difícil criar políticas baseadas em evidência.
- Os dados que existem estão espalhados em plataformas do governo e de
  outras organizações, ou escondidos em artigos, relatórios e posts de
  redes sociais.

## 3. Quem faz e o que é a plataforma
- Em 2022, pesquisadores da Bolívia, do Brasil e do Peru criaram a rede
  ELLAS. É uma equipe de 8 universidades, de computação, economia,
  psicologia, ciências sociais e educação.
- A rede lançou a iniciativa "Latin American Open Data for Gender
  Equality Policies Focusing on Leadership in STEM" para reunir dados e
  criar uma plataforma pública.
- Plataforma de dados abertos (ODP) é uma infraestrutura digital que dá
  acesso público a vários conjuntos de dados, com busca, filtros e
  gráficos. Pense numa biblioteca pública de dados, com catálogo.
- Rede = as pessoas; iniciativa ou projeto = o trabalho financiado;
  plataforma = o produto.

## 4. Duas fontes de dados
- Dados que já existem e dados novos, gerados pelo survey.
- Dados "primários": não estruturados. Vêm de artigos, relatórios e
  redes sociais, e do survey.
- Dados "secundários": já estruturados, coletados por outras pessoas
  para outros fins, em geral planilhas de sites oficiais.
- Neste texto, o survey conta como dado primário.

## 5. O caminho dos dados (Figura 1)
1. Identificar os fatores que afetam mulheres em STEM.
2. Procurar dados existentes em nível nacional ou regional.
3. Se existem, são abertos e estruturados: converter para a estrutura da
   ELLAS.
4. Se existem, são abertos, mas não estruturados: analisar e transformar
   em dado estruturado.
5. Se existem, mas não são abertos: os pesquisadores pedem a abertura a
   quem guarda os dados.
6. Se não existem: a pergunta entra no survey, que é aplicado nos 3
   países, analisado e transformado.
7. Tudo é integrado e publicado como "dados abertos ligados".
- Dados abertos ligados seguem boas práticas (Berners-Lee, 2006; padrão
  do W3C) para publicar e conectar dados em grafos de conhecimento. Pense
  numa teia em que cada dado aponta para os relacionados.

## 6. Os conceitos que organizam tudo (Figura 2)
- **Políticas:** leis, planos, financiamentos, ações afirmativas e
  cotas. Em nível nacional ainda são poucas; surgem mais nas
  organizações e instituições.
- **Iniciativas:** programas como mentoria, bolsas, oficinas e redes.
  Ligam-se mais a redes profissionais e universidades do que ao governo.
- **Fatores de contexto:** condições sociais, culturais, econômicas e
  institucionais que podem ser barreiras ou apoios. Foram classificados
  em individual, interpessoal, acadêmico, trabalho, família,
  socioeconômico, social e histórico. Exemplo: um estudo na Bolívia
  achou que papéis de gênero tradicionais, influência da família e
  discriminação no mercado afastam mulheres de STEM, mesmo quando a
  capacidade não é vista como limite.
- **Indicadores de contexto:** variáveis mensuráveis, como diferenças
  de matrículas, de emprego, de salário e de presença em cargos de
  liderança.
- Os dados foram buscados por revisões sistemáticas de artigos,
  documentos oficiais e redes sociais.

## 5b. O survey (p. 123)
- Objetivo: coletar dados quantitativos sobre os fatores que influenciam
  a escolha por carreiras STEM e a motivação para liderar nos 3 países,
  com base nas revisões de literatura.
- Os dados são comparáveis entre países e o questionário é aberto no
  site da ELLAS, então pode ser replicado em outras regiões.
- Está em 3 idiomas (espanhol, português e inglês) e teve mais de 10.000
  respostas.
- As respostas foram analisadas e, em paralelo, dados selecionados
  passaram por curadoria para virar dados abertos na plataforma. É a
  parte que toca o meu trabalho.

## 7. Desafios
- A disponibilidade dos dados varia por país por causa de leis
  diferentes. O Brasil tem a Lei de Acesso à Informação; a Bolívia não
  tem lei parecida.
- Foi difícil definir quais cursos são STEM e garantir dados separados
  por gênero.
- Buscas só em inglês não achavam iniciativas locais. A equipe usou
  também idiomas locais e redes sociais (Instagram) para achar
  iniciativas de base. No Brasil, poucas pessoas sabem inglês.
- Fontes diferentes usam vocabulários diferentes. Exemplo: "Target
  Audience" em um lugar e "Audience" em outro foram padronizados como a
  mesma relação. E "Undergraduate students", "Estudiantes de pregrado" e
  "Estudantes de Graduação" são reconhecidos como sinônimos.

## 8. Como a plataforma é construída (Figura 4)
- **Camada de dados:** fontes primárias e secundárias, preparadas por
  equipes de várias áreas.
- **Camada de processamento:** arquivos CSV estruturados, modelagem de
  ontologias em 3 idiomas (Protégé e OWL), pipeline com Pentaho e
  Python e integração em grafos de conhecimento. A figura cita os
  formatos CSV, JSON, OWL e RDF.
- **Camada de aplicação:** onde as pessoas buscam, entendem e usam os
  dados. Ainda estava sendo desenhada.
- Usa serviços em nuvem e o site é hospedado pela UFMT.
- Uma ontologia é como um dicionário organizado dos conceitos e de como
  eles se relacionam. Um grafo de conhecimento é uma rede de dados
  ligados.

## 9. Como as pessoas usam a plataforma
- É gratuita, em 3 idiomas, e segue um design sensível a gênero, baseado
  em IHC feminista.
- Dá para buscar por país e por ano, ver mapa, tabela e gráfico, e
  baixar em CSV, PDF e PNG (Figura 5).
- Exemplos de perguntas: que políticas de gênero existem em um país em
  certo ano? Quais iniciativas existem por nível escolar? Qual é o
  gênero das pessoas responsáveis por uma iniciativa, quando é público?
- Privacidade: não mostra contatos individuais, só visões gerais.
- Há espaço para opinar sobre a satisfação e sobre erros.
- Representatividade: a equipe da Bolívia disse não se sentir
  representada nas fotos do primeiro protótipo, então foi incluída uma
  foto de uma cholita (mulher indígena).
- Usos esperados: dados de iniciativas (boas práticas e onde investir),
  de fatores de contexto (entender barreiras), de políticas (criar,
  avaliar e defender mudanças) e do survey (comparar fatores entre os 3
  países).

## 10. Conclusão e trabalho futuro
- O modelo de dados foi pensado para ser conectável, flexível e
  escalável, para outras pessoas contribuírem com novos dados.
- Recomendações: criar plataformas de dados abertos amigáveis e
  sensíveis à cultura, e apoiá-las para que durem.
- Futuro: divulgar a plataforma para públicos diversos, validar o
  survey por análise estatística para ele virar uma ferramenta
  replicável, criar documentação e protocolos de uso, incluir outros
  países da América Latina, do Caribe e do Sul Global, e alinhar com
  padrões abertos de dados.

## 11. Limitações
- O capítulo não tem seção de limitações, porque é descritivo.
- Os próprios autores contam desafios com os dados (seção 7).
- Ainda faltava validar o survey estatisticamente e terminar a camada de
  aplicação.
- Observação minha: não há resultados de testes de uso da plataforma.

## 12. O que isso significa para o meu trabalho
- O survey é dado primário e passa por análise e transformação antes de
  ir para a plataforma. A minha curadoria é essa etapa.
- Padronizar termos e sinônimos entre idiomas é o mesmo tipo de
  problema que vou encontrar no CSV.
- A plataforma já usa CSV e JSON, então o meu arquivo final é
  compatível.
- Validar o survey e criar documentação e protocolos aparece como
  trabalho futuro da rede. O meu plano responde a isso.
- O Lumina deve seguir o princípio de privacidade: visões gerais, sem
  dados pessoais.

## 13. Glossário rápido
- **Dados abertos:** dados de acesso público e livre.
- **Dado estruturado:** organizado em tabela. **Não estruturado:** texto
  solto, como artigos e posts.
- **Dado primário e secundário:** ver seção 4.
- **Dados abertos ligados:** dados publicados de forma conectada, em
  grafos.
- **Ontologia:** dicionário organizado de conceitos e relações.
- **Grafo de conhecimento:** rede de dados ligados.
- **Curadoria:** limpar, padronizar e organizar dados para uso.
- **ODP:** plataforma de dados abertos da ELLAS.