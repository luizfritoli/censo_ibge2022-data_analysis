# *Análise exploratória com dados do Censo 2022*

Análise exploratória sobre características da população brasileira, utilizando dados
fornecidos pelo IBGE no Censo 2022, foram feitos tratamento e análise.

Todos os dados completos do IBGE em: https://censo2022.ibge.gov.br/panorama/?localidade=BR. 
Dados de referência retirados de: 
- https://theglobaleconomy.com/ (Alfabetização)
- https://www.asahi.com/ajw/articles/16030478 (Envelhecimento no Japão)
- https://www.bbc.com/portuguese/geral-47132888 (Expectativa de vida de homens e mulheres)
- https://data.unhabitat.org/pages/housing-slums-and-informal-settlements (Favelização)

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
- `data/refs`: Dados de referência;
- `data/clean`: Dados tratados;
- `plots/`: Gráficos gerados;
- `scripts/treatment.Rmd`: Script responsável pelo tratamento dos dados;
- `scripts/plots.Rmd`: Script responsável pela geração de gráficos.

## *Considerações do tratamento dos dados*

1. **Os dados vieram em ótimo estado**

   Por se tratar do IBGE, o principal provedor de informações geográficas e estatísticas do
   Brasil, os dados vieram muito bem formatados e claros, o que favorecerá a análise.

   Foram feitas verificações iniciais de estrutura, tipagem e consistência para garantir a
   confiabilidade. 
   
2. **Alteração de nomes de colunas para melhorar legibilidade**
   
   Optei por simplificar os nomes das colunas para melhor legibilidade do código.
   
3. **Mutate realizado antes do plot das pirâmides**

   Realizando a ordenação dos nomes das colunas da pirâmide etária, foi percebido que o gráfico
   ficava corretamente ordenado com o mutate sendo feito logo antes da realização do gráfico,
   a ordenação, antes feita na pasta "treatment.Rmd", quebrava o gráfico.

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
   
   1.1 **Os nomes podem ter relação com a religiosidade brasileira**
   
   Como esperado, o catolicismo é predominante no país, com aproximadamente 100 milhões de brasileiros
   declarados católicos. Então, o fato da maioria dos nomes populares serem de origem religiosa não é por 
   acaso.
   
   Logo atrás da religião católica, vem a religião evangélica com aproximadamente 47 milhões e 400 mil
   brasileiros declarados. Fazendo uma breve pesquisa, nomes bem populares do Brasil como "David", "Gabriel" 
   e"Ana" vêm do envangelho, e também é destacado que, com base no Censo 2022, pessoas sem religião são 
   minoria no Brasil.
   
   Existem bastantes evidências para argumentar que a religião é muito presente na sociedade brasileira.

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
   Quando a barra feminina (azul) ultrapassa a masculina (vermelha), há predominância feminina,
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
   
6. **População residente em favelas**

   Quando o assunto é a população que mora em favelas, entre os países de baixa-média renda,
   o Brasil apresenta um percentual de ~8.07%, e quando comparado à países como Índia (~41.5%)
   e África do Sul (~24.5%), é um percentual satisfatório.
   
   `!`: O percentual de residentes em favelas cresceu de ~6% da população para ~8.07% entre
   os Censos de 2010 e 2022 (o que explica esse aumento? o método do IBGE mudou?).
   
   É importante dizer que estes países são apenas exemplos, e não representam a totalidade de 
   países de renda baixa-média. 
   
   Da mesma forma, é interessante analisar que países desenvolvidos, como Alemanha e Japão
   (utilizados como exemplos), têm a população residente em favelas em números aproximados
   à 0%, o que mostra que países desenvolvidos tendem a ter mais soluções para manter esses
   números baixos.
   
   Em poucos minutos de pesquisa, é possível achar possíveis motivos para poucas pessoas
   residirem em favelas em países desenvolvidos. Podemos citar a a educação, que é
   bastante acessível. E por causa disso, a população tende a ter maior consciência de 
   direitos e qualificação.
   
   Paralelamente, o fator histórico é de suma importância. Países como Brasil e Índia não
   tiveram um desenvolvimento gradual como países da Europa e Japão. Por exemplo, milhões de
   brasileiros saíram dos campos para as cidades em poucas décadas, e como as cidades não
   estavam prontas para receber tanta gente, favelas foram geradas.
   
   6.1 **Comparando favelização usando fonte alternativa**
   
   Utilizando uma fonte alternativa ao Censo feito pelo IBGE, dados levantados pela 
   ONU-Habitat mostram números distintos aos do IBGE. Segundo a pesquisa da ONU-Habitat, 
   aproximadamente ~14.8% da população brasileira reside em favelas (até 2016), uma diferença 
   em torno de 6.73% em relação ao Censo 2022.
   
   É notável dizer que o método mudou entre os dois Censos (2010 e 2022), algumas comunidades 
   antes ficavam de fora por não seguirem um critério técnico muito rígido de 2010.
   
   A ONU-Habitat, até 2016, registrou que o Brasil apresentava leve queda no percentual de
   pessoas residindo em favelas, o oposto do Censo 2022, que registrou um aumento significativo.
   
   Não é possível alcançar o número neste momento, mas é plausível questionar: qual é o dado que 
   mais se aproxima da realidade, tendo em vista que provavelmente foram usados dois métodos
   diferentes?
   
7. **Conclusão**

   O Brasil retratado pelo Censo 2022 é um país ainda em desenvolvimento, com pontos positivos e
   negativos, mas com muitas problemáticas a serem tratadas. Primordialmente, deve-se estabelecer
   um método fixo de análise, para não haver discrepância entre resultados diferentes, como por 
   exemplo, no percentual de deficientes (23.9% em 2010 contra 7.3% em 2022) e favelização (6% em 
   2010 contra 8.07% em 2022 contra 14.8% em 2022 pela ONU-Habitat).
   
   Neste projeto, pode-se ver que dados sem contexto podem enganar, sendo evidenciado por fontes
   externas. Para uma análise estruturada e fugindo de enviesamento, a busca pelo conhecimento, 
   interpretação e o questionamento são de suma importância, como visto nos tópicos anteriores. 
   
   Por fim, comento que O ponto principal deste projeto, e tão importante quanto absorver a 
   informação, foi explicar e comentar sobre o conhecimento obtido neste estudo.
   
   
   
   
   
