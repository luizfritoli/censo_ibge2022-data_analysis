# *Análise exploratória com dados do Censo 2022*

Análise exploratória sobre características da população brasileira, utilizando dados
fornecidos pelo IBGE no Censo 2022, foram feitos tratamento e análise.

Todos os dados completos do IBGE em: https://censo2022.ibge.gov.br/panorama/?localidade=BR. 
Dados de referência retirados de: https://theglobaleconomy.com/
   -> 
   
   -> 
   
   -> 

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

- `data/original`: Dados originais..
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

   Como esperado,
   
