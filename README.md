# *Análise exploratória com dados do Censo 2022*

Análise exploratória sobre características da população brasileira, utilizando dados
fornecidos pelo IBGE no Censo 2022, foram feitos tratamento e análise.

Todos os dados completos do IBGE em: https://censo2022.ibge.gov.br/panorama/?localidade=BR. 
Dados de referência retirados de: 
- https://theglobaleconomy.com/ (Alfabetização)
- https://www.asahi.com/ajw/articles/16030478 (Envelhecimento no Japão)
- https://www.bbc.com/portuguese/geral-47132888 (Expectativa de vida de homens e mulheres)

## *Stack*
- R;
- RMarkdown;
- Tidyverse;
- Scales.

## *Objetivos*

- Realizar análise sobre características da população com base no Censo 2022;
- Comparar informações com outros países, se possível;
- Gerar conclusões com as informações obtidas;
- Documentar passos, conclusões e considerações;
- Apresentar o conhecimento adquirido usando dashboards.

## *Execução*

- Clonagem do repositório;
- Executar `scripts/analysis.Rmd`.

## *Estrutura*

- `data/original`: Dados originais;
- `scripts/analysis.Rmd`: Script responsável pela análise dos dados usando gráficos e tabelas.

## *Considerações do tratamento dos dados*

1. **Os dados vieram em ótimo estado**
   Por se tratar do IBGE, o principal provedor de informações geográficas e estatísticas do
   Brasil, os dados vieram muito bem formatados e claros, o que favorecerá a análise.

   Foram feitas verificações iniciais de estrutura, tipagem e consistência para garantir a
   confiabilidade. 

## *Considerações da análise dos dados*

1. **Nomes mais populares**

   Dentre os 10 nomes mais populares do Brasil, todos são nomes de origem religiosa. Então,
   mesmo que o Brasil seja um país declaradamente laico, é notável a forte influência cristã
   na cultura brasileira. É importante mencionar que os nomes nem sempre têm uso exclusivamente
   religioso.

   O nome mais popular do Brasil é `Maria`, muito comum por causa da devoção à Maria no catolicismo.
   Isso é explicado pelo fato do Brasil ter sido colonizado por Portugal, que por séculos teve a Igreja
   Católica como forte influência, o que também atingiu o Brasil.

   É válido comentar que dentre os 10 nomes mais populares, há uma concentração masculina com 8 nomes,
   contra 2 nomes femininos (os nomes femininos são mais variados?). 

2. **Alfabetização**

   O Brasil, com base no Censo 2022, possui um índice de alfabetização de ~93%. A métrica de alfabetização
   está sendo interpretada como formular e escrever frases simples. É relevante registrar que o Brasil é
   um país em desenvolvimento.
 
   Ainda assim, optei por buscar dados de alfabetização aproximados de países considerados desenvolvidos
   e em desenvolvimento. O resultado foi interessante, pois os países considerados desenvolvidos em sua
   maioria, possuem uma taxa de alfabetização superior à 96%, muitas vezes chegando até 99%.

   Entre países ainda em desenvolvimento, o Brasil possui um índice satisfatório. Mas neste caso, países
   vizinhos como Argentina e Uruguai - também em desenvolvimento - têm números de alfabetização semelhantes
   aos países considerados desenvolvidos.

   Observação: Índia e África do Sul foram retirados como exemplos, mas não representam a totalidade de países
   em desenvolvimento. Para mais informações de países específicos, segue o site utilizado para apoio:
   https://theglobaleconomy.com/.

   É plausível questionar o motivo de Argentina e Uruguai, países vizinhos do Brasil e em desenvolvimento, possuem
   índices maiores que o do Brasil. Por mais que 4% ou 5% não sejam números expressivos à primeira vista, estes
   números representam milhões de pessoas.

   O Brasil enfrenta dificuldades na educação básica? Se sim, onde se encontra o erro?
   
3. **Deficiências**
   
   Com base no Censo feito em 2022, o percentual de pessoas declaradas deficientes é de
   7.3%, um valor mais restritivo quando comparado a levantamentos anteriores.
   
   Porém, buscando dados do Censo feito em 2010, é possível notar algo com potencial
   relevância: 23.9% dos brasileiros se declararam deficientes de alguma forma. É 
   evidente que uma diminuição de 16.6% é fora da realidade, em 10 anos é muito
   improvável que o percentual tenha decaído drasticamente.
   
   Buscando mais informações sobre os Censos de 2010 e 2022, o que explica essa
   diferença é o método que foi utilizado.
   
   `Em 2010:` O entrevistador perguntava se o entrevistado tinha dificuldade de ouvir,
   enxergar ou coisas relacionadas. E as respostas eram em níveis: "nenhuma dificuldade",
   "alguma dificuldade", "grande dificuldade" e "não consigo de modo algum". E as pessoas
   que respondiam "alguma dificuldade" ou superior eram consideradas deficientes pelo método
   do IBGE na época.
   
   `Em 2022:` A pergunta era parecida, mas apenas as pessoas que respondiam "grande dificuldade"
   ou superior seriam consideradas.
   
   Sabendo do método utilizado pelo IBGE nas duas pesquisas, é possível ver que o método utilizado
   em 2010 era bem mais amplo que o de 2022, o que reduziu esse número drasticamente. Claro que,
   é um valor mais alinhado a critérios metodológicos mais restritivos, mas é um número considerado mais 
   próximo da realidade do que quase 1/4 da população ser deficiente.
   
4. **Crescimento populacional**

   A população brasileira, entre 1872 e 2022, teve um crescimento contínuo, nunca registrando
   qualquer declínio. É possível que gere um pensamento de que "quanto mais pessoas um país 
   tiver, o crescimento será exponencial", o que nem sempre é verdade, pois países têm inúmeros
   contextos diferentes.
   
   Por isto, foram usados dois países como referência: Rússia e Japão. Russia com uma grande
   quantidade de habitantes e Japão sendo referência em disciplina. Ambos os países estão
   em declínio populacional.
   
   `Na Rússia:` A taxa de natalidade está caindo, pessoas estão tendo menos interesse
   em ter filhos, e muito se deve ao custo de vida e insegurança financeira. Também, a alta
   taxa de mortalidade, devido à problemas de saúde (o consumo de álcool e tabaco na Rússia 
   é grande) e sistemas de saúde que enfrentam desafios em algumas regiões.
   
   `No caso do Japão:` Já é diferente, a população está envelhecendo. Aproximadamente 30% (!) 
   da população japonesa possui 65 anos ou mais, e projeções indicam que essa porcentagem 
   tende a aumentar. Somado a isto, japoneses estão tendo menos filhos por conta do custo de 
   vida, estilo de vida onde há muita pressão no trabalho ou apenas falta de interesse.
   
   E o Brasil, com base no histórico dos Censos, não apresenta nenhum declínio no período
   analisado, embora haja desaceleração no crescimento. É possível levantar a hipótese de que 
   políticas públicas e garantias sociais (Bolsa Família, Pé de Meia, SUS podem ser exemplos) 
   geram maior segurança para as famílias.
   
5. **Pirâmide etária**

   No Brasil, com base nos dados coletados do Censo 2022, possui maior concentração na
   quantidade de pessoas de meia-idade (35-44 anos). Pessoas com mais de 60 anos ainda
   são minoria, mas as faixas não são tão curtas (o Brasil está começando a envelhecer?).
   
   `Informação:` Os dados indicam predominância feminina na população total.
   
   `Importante:` A ‘ponta’ da barra indica qual gênero possui maior valor naquela faixa etária. 
   Quando a barra feminina (vermelha) ultrapassa a masculina (azul), há predominância feminina,
   e vice-versa.
   
   Tendo isto em mente, é de extrema relevância apontar que, a partir de 25-29 anos o gênero
   feminino passa maioria em todas as faixas (!), sendo um sinal de que mulheres tendem a viver 
   mais do que os homens, o que pode ter relação com haver mais mulheres do que homens vivos
   no país.
   
   Com estes fatos, há margem para questionamentos. Por que mulheres vivem mais do que os
   homens? Os homens, historicamente, realizarem trabalhos considerados mais "perigosos" e
   que envolvem força física poderia ser uma justificativa? Mulheres tendem a ter maior
   cuidado com elas mesmas?
   
   Indo atrás de informações, o professor David Gems, do University College London, explicou
   que embriões masculinos morrem em um ritmo maior que os embriões femininos. O que é um dos
   vários fatores que ajudam a explicar a diferença de expectativa de vida.
   
   
   
   
   
   
   
